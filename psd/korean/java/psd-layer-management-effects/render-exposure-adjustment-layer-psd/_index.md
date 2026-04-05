---
date: 2026-04-05
description: Aspose.PSD for Java를 사용하여 PSD 파일에서 노출 조정 레이어를 렌더링하는 방법을 배웁니다. 노출 레이어를
  수정하고 추가하는 단계별 가이드와 코드 예제.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: PSD 파일에서 노출 조정 레이어 렌더링 - Java
second_title: Aspose.PSD Java API
title: PSD 파일에서 노출 조정 레이어 렌더링 - Java
url: /ko/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD 파일에서 노출 조정 레이어 렌더링 - Java

## 소개

Photoshop PSD 파일을 작업하고 있으며 프로그래밍 방식으로 **노출 조정 레이어를 렌더링**해야 합니까? 기존 레이어를 조정하거나 새 레이어를 추가하든, Aspose.PSD for Java는 이러한 작업을 처리하기 위한 강력하고 직관적인 방법을 제공합니다. 이 가이드에서는 Aspose.PSD for Java를 사용하여 PSD 파일에서 노출 조정 레이어를 렌더링하고 수정하는 방법을 단계별로 안내합니다. 튜토리얼이 끝날 때쯤이면 기존 레이어의 노출 설정을 조정하고 PSD 파일에 새로운 노출 조정 레이어를 추가하는 방법을 알게 될 것입니다. 시작해 봅시다!

## 빠른 답변
- **필요한 라이브러리는 무엇입니까?** Aspose.PSD for Java
- **기존 노출 레이어를 편집할 수 있습니까?** 예, 노출, 오프셋 및 감마 보정을 변경할 수 있습니다.
- **새 노출 조정 레이어를 어떻게 추가합니까?** `PsdImage` 인스턴스에서 `addExposureAdjustmentLayer()`를 사용하십시오.
- **PNG 내보내기가 지원됩니까?** 물론입니다 – 결과를 PNG로 저장하려면 `PngOptions`를 사용하십시오.
- **프로덕션에 라이선스가 필요합니까?** 프로덕션 사용을 위해서는 상용 라이선스가 필요하며, 무료 체험판을 사용할 수 있습니다.

## 렌더링 노출 조정 레이어란 무엇입니까?

노출 조정 레이어는 기본 이미지의 밝기, 오프셋 및 감마를 변경하는 비파괴 Photoshop 레이어입니다. 이를 렌더링한다는 것은 해당 설정을 적용하여 시각적 결과가 조정을 반영하도록 하는 것으로, 이후 PNG와 같은 형식으로 내보낼 수 있습니다.

## 왜 Aspose.PSD for Java를 사용하여 노출 조정 레이어를 렌더링합니까?

- **전체 제어** – Photoshop을 열지 않고 레이어 속성을 조작합니다.
- **배치 처리** – 여러 파일에 대한 조정을 자동화합니다.
- **크로스 플랫폼** – JDK가 설치된 모든 시스템에서 실행됩니다.
- **PSD 구조 보존** – 향후 편집을 위해 레이어를 편집 가능 상태로 유지합니다.

## 전제 조건

1. **Java Development Kit (JDK)** – 최소 JDK 8.
2. **Aspose.PSD for Java** – [여기](https://releases.aspose.com/psd/java/)에서 다운로드하십시오.
3. **Basic Java knowledge** – 표준 Java 구문에 익숙해야 합니다.
4. **IDE or Text Editor** – IntelliJ IDEA, Eclipse, VS Code, 또는 원하는 편집기를 사용하십시오.

## 패키지 가져오기

먼저, 필요한 Aspose.PSD 클래스를 가져옵니다:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 노출 조정 레이어 렌더링 방법 – 단계별 가이드

### 단계 1: PSD 파일 로드

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

`"Your Document Directory"`를 PSD 파일이 들어 있는 폴더로 교체하십시오. `Image.load()` 메서드는 문서의 레이어에 전체 접근 권한을 제공하는 `PsdImage` 객체를 반환합니다.

### 단계 2: 기존 노출 조정 레이어 편집

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

루프는 모든 레이어를 순회하면서 `ExposureLayer`를 찾아 세 가지 주요 매개변수를 업데이트합니다. 이것이 사용자 지정 값으로 **노출 조정 레이어를 렌더링**하는 핵심입니다.

### 단계 3: 수정된 PSD 파일 저장

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

수정된 PSD는 모든 원본 레이어를 그대로 유지하지만, 노출 조정은 이제 새로운 설정을 반영합니다.

### 단계 4: 결과를 PNG로 내보내기

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

`TruecolorWithAlpha`와 함께 `PngOptions`를 사용하면 내보낸 PNG가 전체 색 깊이와 PSD의 투명성을 유지합니다.

### 단계 5: 새로운 노출 조정 레이어 추가

기존 문서에 **새 노출 조정 레이어를 추가**해야 하는 경우, 다음 코드를 사용하십시오:
```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

`addExposureAdjustmentLayer` 메서드는 지정된 노출, 오프셋 및 감마 값을 가진 새로운 조정 레이어를 생성하며, 이후 이전과 같이 렌더링하고 내보낼 수 있습니다.

## 일반적인 문제 및 팁

- **레이어를 찾을 수 없음** – PSD에 실제로 `ExposureLayer`가 포함되어 있는지 확인하십시오. `ClassCastException`을 방지하려면 예시와 같이 `instanceof ExposureLayer`를 사용하십시오.
- **파일 경로 오류** – 절대 경로를 사용하거나 `dataDir`이 파일 구분자(` / ` 또는 ` \ `)로 끝나는지 확인하십시오.
- **라이선스 예외** – 유효한 라이선스 없이 실행하면 출력에 워터마크가 추가됩니다. 코드 초기에 라이선스를 등록하십시오 (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## 자주 묻는 질문

### Aspose.PSD for Java란 무엇입니까?

Aspose.PSD for Java는 Java를 사용하여 프로그래밍 방식으로 PSD 파일을 생성, 편집 및 변환할 수 있게 해 주는 라이브러리입니다. Photoshop 문서를 다루기 위한 포괄적인 기능을 제공합니다.

### Aspose.PSD for Java를 사용하여 다른 유형의 레이어를 조작할 수 있습니까?

예, Aspose.PSD for Java는 텍스트 레이어, 조정 레이어, 이미지 레이어 등 다양한 레이어 유형을 지원하여 PSD 파일을 광범위하게 조작할 수 있습니다.

### Aspose.PSD for Java를 시작하려면 어떻게 해야 합니까?

라이브러리를 [웹사이트](https://releases.aspose.com/psd/java/)에서 다운로드하고, 자세한 가이드와 예제를 보려면 [문서](https://reference.aspose.com/psd/java/)를 참조하십시오.

### Aspose.PSD for Java에 대한 무료 체험판이 있습니까?

예, 무료 체험판을 사용할 수 있습니다. [여기](https://releases.aspose.com/)에서 다운로드하십시오.

### Aspose.PSD for Java에 대한 지원을 어떻게 받을 수 있습니까?

지원이 필요하면 [Aspose 지원 포럼](https://forum.aspose.com/c/psd/34)을 방문하여 질문을 하고 커뮤니티로부터 도움을 받을 수 있습니다.

**추가 질문**

**Q: 여러 PSD 파일을 배치 처리할 수 있습니까?**  
A: 물론입니다. 로드, 편집 및 저장 로직을 파일 경로 목록을 반복하는 루프 안에 넣으십시오.

**Q: 새 노출 레이어를 추가할 때 라이브러리가 레이어 계층 구조를 유지합니까?**  
A: 예. 새 레이어는 기존 레이어 위에 추가되어 원래 계층 구조를 유지합니다.

**Q: PNG 외에 어떤 이미지 형식으로 내보낼 수 있습니까?**  
A: Aspose.PSD는 해당 `*Options` 클래스를 통해 JPEG, BMP, TIFF 및 여러 다른 형식을 지원합니다.

---

**마지막 업데이트:** 2026-04-05  
**테스트 환경:** Aspose.PSD for Java 24.10  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
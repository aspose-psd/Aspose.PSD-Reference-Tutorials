---
date: 2026-02-20
description: Aspose.PSD for Java를 사용하여 PSD 색상 모드를 16비트 그레이스케일로 설정하면서 PSD를 PNG로 변환하는
  방법을 배웁니다. 코드 예제가 포함된 단계별 가이드.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Java에서 16비트 그레이스케일 색상 모드로 PSD를 PNG로 변환하는 방법
url: /ko/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 16‑bit 그레이스케일 컬러 모드로 PNG 변환 (Java)

## 소개
그래픽 디자인 및 이미지 조작 세계에 뛰어들 때 **PSD를 PNG로 변환하는 방법**을 아는 것은 비밀 무기를 갖는 것과 같습니다. 16‑bit 그레이스케일 모드를 사용하면 놀라운 깊이와 톤 풍부함을 얻을 수 있어 이미지가 돋보입니다. 이 튜토리얼에서는 **PSD 컬러 모드**를 16‑bit 그레이스케일로 설정한 뒤 Aspose.PSD for Java를 사용해 **PSD를 PNG로 내보내는** 과정을 단계별로 살펴보겠습니다. 이미지 워크플로우를 한 단계 끌어올릴 준비가 되셨나요? 시작해봅시다.

## 빠른 답변
- **“PSD를 PNG로 변환”이란 무엇을 의미하나요?** PSD를 로드하고, 필요에 따라 컬러 모드를 변경한 뒤 PNG 파일로 저장하는 과정입니다.  
- **어떤 Aspose 클래스를 사용해 변환을 수행하나요?** 로딩은 `PsdImage`, 저장은 `PngOptions` 클래스를 사용합니다.  
- **특별한 라이선스가 필요합니까?** 테스트용 트라이얼은 가능하지만, 실제 운영 환경에서는 유료 라이선스가 필요합니다.  
- **PNG에서도 16‑bit 깊이를 유지할 수 있나요?** 네, `PngColorType.GrayscaleWithAlpha`를 사용하면 가능합니다.  
- **지원되는 IDE는 무엇인가요?** IntelliJ IDEA, Eclipse, VS Code 등 모든 Java IDE에서 사용 가능합니다.

## 왜 16‑bit 그레이스케일로 PSD를 PNG로 변환할까요?
* **톤 디테일 보존:** 16‑bit 그레이스케일은 65 536가지 회색 음영을 저장하므로 8‑bit 이미지의 256음영보다 훨씬 풍부합니다.  
* **넓은 호환성:** PNG는 브라우저, 모바일 앱, 데스크톱 툴 전반에 걸쳐 널리 지원되며, 고품질 데이터를 유지합니다.  
* **무손실 워크플로우:** Aspose.PSD를 사용한 변환은 원치 않는 압축 아티팩트가 없으며, 아카이브나 추가 처리에 이상적입니다.

## 전제 조건
튜토리얼을 진행하기 전에 다음 항목을 모두 준비해 주세요:

1. **Java Development Kit (JDK)** – 최신 버전을 설치하세요. [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드할 수 있습니다.  
2. **Aspose.PSD for Java Library** – PSD 파일을 조작할 엔진입니다. [Aspose download page](https://releases.aspose.com/psd/java/)에서 받으세요.  
3. **IDE** – IntelliJ IDEA, Eclipse, Visual Studio Code 등 어느 것이든 상관없습니다.  
4. **기본 Java 지식** – Java 문법에 익숙하면 단계가 더 수월합니다.  
5. **샘플 PSD 파일** – Adobe Photoshop에서 직접 만들거나 온라인에서 무료 샘플을 다운로드하세요.

준비되셨나요? 좋습니다! 이제 필요한 패키지를 가져오고 코딩을 시작해봅시다.

## 패키지 가져오기
먼저 Java 파일에 Aspose.PSD에 필요한 import 구문을 추가합니다:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

이 import 구문을 통해 PSD 파일을 조작하고, 컬러 모드를 설정하며, 결과를 PNG로 내보내는 기능을 사용할 수 있습니다.

## 단계 1: 디렉터리 정의
원본 PSD를 읽을 폴더와 변환된 파일을 쓸 폴더를 설정합니다. 프로그램이 어디서 파일을 읽고 어디에 저장할지 알려주는 역할을 합니다.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

플레이스홀더 문자열을 실제 머신의 경로로 교체하세요.

## 단계 2: 이미지 처리를 위한 메서드 생성
변환 로직을 재사용 가능한 메서드로 캡슐화합니다. 컬러 모드, 비트 깊이, 압축 옵션 등 조정하고 싶은 모든 매개변수를 전달받습니다.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

이 메서드를 통해 **PSD 컬러 모드**를 설정하고 **PSD를 PNG로 내보내는** 작업을 한 번에 수행할 수 있습니다.

## 단계 3: 파일 경로 정의 및 PSD 로드
메서드 내부에서 전체 파일 경로를 구성하고 원본 16‑bit 그레이스케일 PSD를 로드합니다:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix`는 각 출력 파일에 사용된 설정을 추적하는 데 도움이 됩니다.

## 단계 4: 레이어 또는 전체 이미지 처리
이제 특정 레이어에 그리거나 전체 이미지에 그릴 수 있습니다. 예시에서는 결과를 더 잘 보이게 하기 위해 미세한 회색 테두리를 추가합니다.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

사각형은 이미지 크기에 관계없이 중앙에 위치하도록 동적으로 계산됩니다.

## 단계 5: 수정된 PSD 파일 저장
그리기 작업이 끝난 후, 지정한 컬러 모드와 비트 깊이 그대로 PSD를 저장합니다. 이는 **PSD 컬러 모드**를 변환 전에 정확히 설정하는 핵심 단계입니다.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## 단계 6: PSD를 PNG로 변환
마지막으로 새로 저장한 PSD를 로드하고 PNG로 내보냅니다. `PngColorType.GrayscaleWithAlpha`를 사용하면 PNG 파일에서도 16‑bit 깊이를 유지할 수 있습니다.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

이제 **PSD를 PNG로 변환**하면서 고품질 16‑bit 그레이스케일 데이터를 그대로 보존했습니다.

## 일반적인 문제 및 해결책
| 문제 | 발생 원인 | 해결 방법 |
|------|----------|----------|
| **“Unsupported color type” 예외** | 지원되지 않는 채널 구성을 가진 PSD를 저장하려 할 때 발생합니다. | `channelBitsCount`가 실제 비트 깊이(16)와 일치하는지, `channelsCount`가 그레이스케일(1)용으로 올바른지 확인하세요. |
| **파일을 찾을 수 없음** | 소스 디렉터리 경로가 잘못되었습니다. | `sourceDir` 문자열을 다시 확인하고 PSD 파일이 존재하는지 검증하세요. |
| **출력 PNG가 검게 보임** | 알파 채널 처리를 하지 않고 PNG를 저장했기 때문입니다. | 위 예시와 같이 `PngColorType.GrayscaleWithAlpha`를 사용하세요. |

## 자주 묻는 질문

**Q: 16‑bit 그레이스케일 컬러 모드란 무엇인가요?**  
A: 65 536가지 회색 음영을 제공하여 표준 8‑bit(256음영)보다 훨씬 풍부한 톤 디테일을 구현합니다.

**Q: Aspose.PSD를 그레이스케일이 아닌 이미지에도 사용할 수 있나요?**  
A: 물론입니다! Aspose.PSD는 RGB, CMYK, Lab 등 다양한 컬러 모드를 지원합니다.

**Q: Aspose.PSD의 체험판 버전이 있나요?**  
A: 네, 무료 체험판을 사용할 수 있습니다. [Aspose download page](https://releases.aspose.com/)에서 바로 받아보세요.

**Q: Aspose.PSD 사용 예제를 더 보고 싶어요.**  
A: 자세한 예제와 튜토리얼은 [documentation](https://reference.aspose.com/psd/java/)을 참고하세요.

**Q: Aspose.PSD 라이선스는 어떻게 구매하나요?**  
A: [Aspose purchase page](https://purchase.aspose.com/buy)에서 라이선스를 구매할 수 있습니다.

---

**마지막 업데이트:** 2026-02-20  
**테스트 환경:** Aspose.PSD for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
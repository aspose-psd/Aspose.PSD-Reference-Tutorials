---
title: PSD 파일의 렌더 노출 조정 레이어 - Java
linktitle: PSD 파일의 렌더 노출 조정 레이어 - Java
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일의 노출 레이어를 렌더링하고 조정하는 방법을 알아보세요. 노출 레이어 수정 및 추가에 대한 코드 예제가 포함된 단계별 가이드입니다.
weight: 15
url: /ko/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD 파일의 렌더 노출 조정 레이어 - Java

## 소개

Photoshop PSD 파일로 작업 중이며 프로그래밍 방식으로 노출을 조정하거나 노출 조정 레이어를 추가해야 합니까? 기존 레이어를 조정하든 새 레이어를 추가하든 Aspose.PSD for Java는 이러한 작업을 처리하는 강력하고 직관적인 방법을 제공합니다. 이 가이드에서는 Java용 Aspose.PSD를 사용하여 PSD 파일의 노출 조정 레이어를 렌더링하고 수정하는 방법을 안내합니다. 이 튜토리얼을 마치면 기존 레이어의 노출 설정을 조정하고 PSD 파일에 새 노출 조정 레이어를 추가하는 방법을 알게 됩니다. 뛰어들어보자!

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. JDK(Java Development Kit): 컴퓨터에 JDK가 설치되어 있어야 합니다. 이 가이드에서는 JDK 8 이상이 있다고 가정합니다.
2.  Java용 Aspose.PSD: PSD 파일을 사용하려면 Aspose.PSD 라이브러리가 필요합니다. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/psd/java/).
3. Java에 대한 기본 지식: Java 프로그래밍에 익숙하면 쉽게 따라할 수 있습니다.
4. IDE 또는 텍스트 편집기: IntelliJ IDEA, Eclipse 또는 선택한 텍스트 편집기와 같은 IDE를 사용하여 Java 코드를 작성하고 실행합니다.

## 패키지 가져오기

먼저, Java용 Aspose.PSD에서 필요한 패키지를 가져옵니다. 이 단계를 통해 우리 코드는 PSD 파일을 조작하기 위해 라이브러리의 기능을 활용할 수 있습니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 1단계: PSD 파일 로드

시작하려면 PSD 파일을 애플리케이션에 로드해야 합니다. 방법은 다음과 같습니다.

```java
String dataDir = "Your Document Directory";  // 문서 디렉토리 정의
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // 소스 PSD 파일 경로

PsdImage im = (PsdImage) Image.load(sourceFileName);  // PSD 파일 로드
```

 이 코드 조각에서`"Your Document Directory"` PSD 파일이 있는 경로를 사용하세요. 그만큼`Image.load()` 메소드는 PSD 파일을 인스턴스로 로드합니다.`PsdImage`, 해당 레이어를 조작할 수 있습니다.

## 2단계: 기존 노출 조정 레이어 편집

PSD 파일이 로드되면 기존 레이어에 액세스하고 수정할 수 있습니다. 파일에 노출 조정 레이어가 포함되어 있으면 해당 속성을 조정할 수 있습니다.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // 노출 수준 조정
        expLayer.setOffset(-0.25f);  // 오프셋 설정
        expLayer.setGammaCorrection(0.5f);  // 감마 보정 조정
    }
}
```

이 루프에서는 PSD 파일의 모든 레이어를 반복합니다. 우리가`ExposureLayer` , 우리는 그것을 수정합니다`Exposure`, `Offset` , 그리고`GammaCorrection` 속성. 이를 통해 노출 조정 레이어의 시각적 출력을 미세 조정할 수 있습니다.

## 3단계: 수정된 PSD 파일 저장

변경한 후에는 업데이트된 PSD 파일을 저장해야 합니다.

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // 수정된 PSD 파일을 저장할 경로

im.save(psdPathAfterChange);  // PSD 파일에 변경 사항을 저장합니다.
```

이 줄은 수정된 PSD 파일을 지정된 경로에 저장하고 노출 조정을 유지합니다.

## 4단계: PNG로 내보내기

업데이트된 PSD 파일을 PNG로 내보내려면 다음 단계를 따르세요.

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // PNG 파일을 저장할 경로

PngOptions saveOptions = new PngOptions();  // PNG 옵션 만들기
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // 색상 유형을 알파를 사용하여 트루컬러로 설정

im.save(pngExportPath, saveOptions);  // PNG로 저장
```

 여기,`PngOptions` PNG 내보내기 설정을 구성하는 데 사용됩니다.`PngColorType.TruecolorWithAlpha` PNG 파일이 색상 깊이와 투명도를 유지하는지 확인합니다.

## 5단계: 새 노출 조정 레이어 추가

기존 PSD 파일에 새 노출 조정 레이어를 추가하려면 다음 코드를 사용하면 됩니다.

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // 소스 PSD 파일 경로

PsdImage img = (PsdImage) Image.load(sourceFileName);  // PSD 파일 로드

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // 새로운 노출 조정 레이어 추가

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // 수정된 PSD 파일을 저장할 경로
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // PNG 파일을 저장할 경로

img.save(psdPathAfterChange);  // PSD 파일에 변경 사항을 저장합니다.

PngOptions options = new PngOptions();  // PNG 옵션 만들기
options.setColorType(PngColorType.TruecolorWithAlpha);  // 색상 유형을 알파를 사용하여 트루컬러로 설정

img.save(pngExportPath, options);  // PNG로 저장
```

이 단계에서는 지정된 노출, 오프셋 및 감마 보정 값을 사용하여 새로운 노출 조정 레이어가 PSD 파일에 추가됩니다. 그러면 업데이트된 PSD 및 PNG 파일이 저장됩니다.

## 결론

그리고 거기에 있습니다! Java용 Aspose.PSD를 사용하여 PSD 파일의 노출 레이어를 렌더링하고 조정하는 방법을 배웠습니다. 기존 노출 레이어를 수정하고, 새 노출 레이어를 추가하고, 작업을 PNG 파일로 내보내는 방법을 다루었습니다. 사진을 수정하든 디자인 자산을 준비하든 이러한 기술을 사용하면 프로그래밍 방식으로 PSD 파일을 관리하는 능력이 향상됩니다. 즐거운 코딩하세요!

## FAQ

### Java용 Aspose.PSD란 무엇입니까?

Aspose.PSD for Java는 Java를 사용하여 프로그래밍 방식으로 PSD 파일을 생성, 편집 및 변환할 수 있는 라이브러리입니다. Photoshop 문서 작업을 위한 포괄적인 기능을 제공합니다.

### Java용 Aspose.PSD를 사용하여 다른 유형의 레이어를 조작할 수 있나요?

예, Aspose.PSD for Java는 텍스트 레이어, 조정 레이어, 이미지 레이어 등 다양한 유형의 레이어를 지원하므로 PSD 파일을 광범위하게 조작할 수 있습니다.

### Java용 Aspose.PSD를 시작하려면 어떻게 해야 합니까?

 다음에서 라이브러리를 다운로드하여 시작할 수 있습니다.[웹사이트](https://releases.aspose.com/psd/java/) 그리고 다음을 참조하면[선적 서류 비치](https://reference.aspose.com/psd/java/) 자세한 가이드와 예시를 확인하세요.

### Aspose.PSD for Java에 대한 무료 평가판이 있습니까?

 예, 무료 평가판을 사용할 수 있습니다. 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).

### Java용 Aspose.PSD에 대한 지원을 어떻게 받을 수 있나요?

 지원을 받으려면 다음을 방문하세요.[Aspose 지원 포럼](https://forum.aspose.com/c/psd/34) 질문을 하고 커뮤니티로부터 도움을 받을 수 있는 곳입니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

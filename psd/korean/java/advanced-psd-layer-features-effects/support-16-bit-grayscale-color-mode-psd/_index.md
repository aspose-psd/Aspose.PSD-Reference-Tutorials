---
title: PSD에서 16비트 회색조 색상 모드 지원 - Java
linktitle: PSD에서 16비트 회색조 색상 모드 지원 - Java
second_title: Aspose.PSD 자바 API
description: 이 상세한 단계별 튜토리얼을 통해 Java용 Aspose.PSD를 사용하여 PSD 파일에서 16비트 회색조 색상 모드를 구현하는 방법을 알아보세요.
weight: 11
url: /ko/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD에서 16비트 회색조 색상 모드 지원 - Java

## 소개
그래픽 디자인과 이미지 조작의 세계에 뛰어들 때 다양한 색상 모드로 작업하는 방법을 이해하는 것은 비밀 무기를 갖는 것과 같습니다. 특히 16비트 그레이스케일은 이미지에 놀라운 깊이와 디테일을 부여하여 이미지를 더욱 돋보이게 만들어 게임의 판도를 바꿀 수 있습니다. 그렇다면 Java용 Aspose.PSD를 사용하여 이 강력한 기능을 탐색할 준비가 되셨습니까? 코딩 장비가 준비되었으면 바로 시작해 보겠습니다.
## 전제조건
시작하기 전에 이 튜토리얼을 최대한 활용할 수 있도록 모든 것이 설정되어 있는지 확인하겠습니다. 필요한 것은 다음과 같습니다.
1. JDK(Java Development Kit): 최신 버전의 JDK가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[오라클 사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java Library: PSD 파일을 조작하는 데 사용할 라이브러리입니다. 에서 손에 넣을 수 있습니다.[Aspose 다운로드 페이지](https://releases.aspose.com/psd/java/).
3. 통합 개발 환경(IDE): Java를 지원하는 모든 IDE가 가능합니다. 널리 사용되는 선택에는 IntelliJ IDEA, Eclipse 또는 Visual Studio Code가 포함됩니다.
4. Java에 대한 기본 지식: Java 프로그래밍에 익숙하면 원활하게 작업을 진행하는 데 확실히 도움이 됩니다.
5. 샘플 PSD 파일: 작업하려는 PSD 파일이 있는지 확인하세요. PSD가 없으면 Adobe Photoshop과 같은 소프트웨어를 사용하여 간단한 PSD를 만들거나 온라인에서 샘플 파일을 찾아볼 수 있습니다.
준비가 된? 엄청난! 필요한 패키지를 가져오고 코딩을 시작하겠습니다.
## 패키지 가져오기
작업을 시작하려면 Java용 Aspose.PSD로 작업하는 데 필요한 관련 패키지를 가져오겠습니다. Java 파일에 다음 줄을 추가합니다.
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
이러한 가져오기를 통해 PSD 파일을 조작하고, 그래픽을 만들고, 이미지를 다양한 형식으로 저장하는 데 사용할 기능에 액세스할 수 있습니다.
## 1단계: 디렉터리 정의
가장 먼저 하고 싶은 일은 소스 및 출력 디렉터리를 설정하는 것입니다. 여기에서 PSD 파일을 로드하고 저장할 수 있습니다. 방법은 다음과 같습니다.
```java
String sourceDir = "Your Source Directory"; // 소스 디렉터리로 변경
String outputDir = "Your Document Directory"; // 출력 디렉터리로 변경
```
"Your Source Directory" 및 "Your Document Directory"를 PSD 파일이 있고 처리된 파일을 저장하려는 컴퓨터의 실제 경로로 바꾸십시오.
## 2단계: 이미지 처리를 처리하는 방법 만들기
이제 PSD 파일 처리를 처리하는 방법을 만들어 보겠습니다. 이 방법은 일련의 매개변수를 사용하여 PSD 파일의 특성과 회색조 프로세스를 식별합니다.
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
이 방법을 사용하면 파일 이름, 색상 모드, 비트 수, 채널 수, 압축 방법 및 레이어 번호를 지정할 수 있습니다. 이 방법의 기능을 단계별로 분석하겠습니다!
## 3단계: 파일 경로 정의 및 PSD 로드
메서드 내에서 파일 경로를 구성하고 실제로 PSD 이미지를 로드하는 방법을 정의해 보겠습니다.
```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// 사전 정의된 16비트 회색조 PSD 로드
PsdImage image = (PsdImage)Image.load(filePath);
```
여기서는 작업할 PSD 파일에 필요한 경로를 구성하고 수정된 PSD 및 PNG 파일 저장을 준비합니다.
## 4단계: 레이어 또는 전체 이미지 처리
다음으로 선택한 레이어나 전체 이미지에 회색 테두리를 추가하여 그려야 합니다. 이는 가시성을 높이고 이미지에 약간의 감각을 더할 수 있는 멋진 방법입니다.
```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // 레이어 둘레에 회색 내부 테두리를 그립니다.
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
이 부분에서는 Aspose의 Graphics 클래스를 사용하여 그리기 컨텍스트를 만듭니다. 직사각형의 크기는 이미지 크기를 기준으로 계산되므로 중앙에 완벽하게 그려집니다.
## 5단계: 수정된 PSD 파일 저장
그리기가 끝나면 수정 사항을 새 PSD 파일에 저장할 차례입니다. 여기에서 앞서 지정한 옵션을 설정합니다.
```java
    // 특정 특성을 지닌 PSD 사본을 저장하세요.
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```
PSD에 대한 옵션을 설정하면 이미지를 저장할 때 이미지가 어떻게 작동할지 제어할 수 있습니다. 모든 세심한 세부 사항이 보존되도록 보장합니다.
## 6단계: PSD를 PNG로 변환
새로 저장한 PSD를 알파가 포함된 회색조용으로 특별히 설계된 PNG 형식으로 변환하면 금상첨화입니다.
```java
finally {
    image.dispose();
}
// 저장된 PSD를 불러옵니다.
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // 저장된 PSD를 회색조 PNG 이미지로 변환
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // 여기도 예외는 아니어야 해
}
finally {
    image1.dispose();
}
```
변환 프로세스는 간단하며 이미지를 다양한 애플리케이션에서 사용하거나 온라인으로 공유할 수 있도록 해줍니다.
## 결론
그리고 여기까지입니다. Java용 Aspose.PSD를 사용하여 PSD 파일에서 16비트 회색조 색상 모드를 지원하는 방법에 대한 완전한 연습입니다! 환경을 설정하고, 이미지를 처리하고, 다른 형식으로 내보내는 방법도 배웠습니다. 몇 줄의 코드만으로 이렇게 아름다운 결과를 얻을 수 있다는 것이 놀랍지 않나요?
이와 같은 이미지를 조작하는 능력으로 당신이 어떤 모험을 시작할 수 있는지 누가 알겠습니까? 기존 디자인을 향상시키든 완전히 새로운 걸작을 창조하든, 상상력은 한계가 없습니다!

## FAQ
### 16비트 회색조 색상 모드란 무엇입니까?
16비트 회색조는 표준 8비트에 비해 더 포괄적인 범위의 음영을 허용하므로 더 자세한 이미지를 얻을 수 있습니다.
### 회색조가 아닌 이미지에 Aspose.PSD를 사용할 수 있나요?
전적으로! Aspose.PSD는 다양한 색상 모드를 지원하므로 RGB, CMYK 등으로도 작업할 수 있습니다.
### Aspose.PSD의 평가판이 있습니까?
 예, Aspose.PSD의 무료 평가판을 사용해 볼 수 있습니다. 그냥[Aspose 다운로드 페이지](https://releases.aspose.com/).
### Aspose.PSD 사용에 대한 더 많은 예를 어디에서 찾을 수 있나요?
 당신은 확인할 수 있습니다[선적 서류 비치](https://reference.aspose.com/psd/java/) 더 자세한 예제와 튜토리얼을 확인하세요.
### Aspose.PSD 라이선스는 어떻게 구매하나요?
 방문하시면 라이센스를 구매하실 수 있습니다.[구매 페이지 제안](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

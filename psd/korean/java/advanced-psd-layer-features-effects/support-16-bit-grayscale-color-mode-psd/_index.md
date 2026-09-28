---
date: 2026-09-28
description: Aspose.PSD for Java를 사용하여 PSD 색상 모드를 16비트 그레이스케일로 설정하고 PSD를 PNG로 내보내는
  방법을 배웁니다. 단계별 가이드와 코드 예제 포함.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: PSD를 PNG로 내보내기 – 16비트 그레이스케일 – Java
og_description: Aspose.PSD for Java를 사용하여 16비트 그레이스케일로 PSD를 PNG로 내보냅니다. 65,536개의 회색
  음영을 보존하는 단계별 튜토리얼을 따라 보세요.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Java에서 16비트 그레이스케일로 PSD를 PNG로 내보내기 – Aspose.PSD 가이드
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Java에서 16비트 그레이스케일 색상 모드로 PSD를 PNG로 내보내는 방법
url: /ko/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 16‑비트 그레이스케일 색상 모드로 PSD를 PNG로 내보내기

## 소개
PSD를 PNG로 내보내면서 16‑비트 그레이스케일 색상 모드를 유지하면 전문 사진의 깊이와 PNG의 보편적인 호환성을 동시에 얻을 수 있습니다. 이 가이드에서는 **PSD 색상 모드를 16‑비트 그레이스케일로 설정**하고 **Aspose.PSD for Java**를 사용해 PSD를 PNG로 내보내는 방법을 배웁니다. 전제 조건부터 문제 해결까지 모두 다루므로 Java 기반 이미지 파이프라인에 이 워크플로를 쉽게 통합할 수 있습니다.

## 빠른 답변
- **“PSD를 PNG로 내보내기”는 무엇을 의미합니까?** PSD를 로드하고, 필요에 따라 색상 모드를 변경한 뒤 PNG 파일로 저장합니다.  
- **어떤 Aspose 클래스가 변환을 처리합니까?** `PsdImage`는 PSD를 로드하고 `PngOptions`는 PNG 출력 설정을 정의합니다.  
- **프로덕션에 라이선스가 필요합니까?** 예 – 시험용으로는 체험판이 작동하지만, 상업적 사용을 위해서는 유료 라이선스가 필요합니다.  
- **16‑비트 깊이를 PNG에 유지할 수 있나요?** 예, `PngColorType.GrayscaleWithAlpha`를 사용하면 가능합니다.  
- **지원되는 IDE는 무엇입니까?** 모든 Java IDE – IntelliJ IDEA, Eclipse, VS Code, NetBeans 등.

## PSD를 PNG로 내보내기란 무엇입니까?
PSD를 PNG로 내보내는 것은 Adobe Photoshop 문서(PSD)를 Portable Network Graphics(PNG) 파일로 변환하면서 이미지의 픽셀 데이터와 색상 깊이를 보존하는 과정입니다. 이 변환은 웹에서 고품질 그레이스케일 자산을 손실 없이 공유할 때 일반적으로 사용됩니다.

## 왜 16‑비트 그레이스케일로 PSD를 PNG로 내보내야 할까요?
PNG로 내보내면서 16‑비트 그레이스케일을 유지하면 65 536가지 회색 음영을 보존할 수 있어 8‑비트 이미지보다 훨씬 풍부한 톤을 제공합니다. PNG의 보편적인 지원 덕분에 브라우저, 모바일 앱, 데스크톱 편집기에서 파일을 손실 없이 표시할 수 있으며, Aspose.PSD의 무손실 압축은 아티팩트가 발생하지 않음을 보장합니다.

## 사전 요구 사항
시작하기 전에 다음 항목을 준비하십시오:

1. **Java Development Kit (JDK)** – 최신 JDK를 [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 설치하십시오.  
2. **Aspose.PSD for Java 라이브러리** – [Aspose 다운로드 페이지](https://releases.aspose.com/psd/java/)에서 JAR를 다운로드하십시오.  
3. **IDE** – IntelliJ IDEA, Eclipse, Visual Studio Code 중 하나를 사용하면 됩니다.  
4. **기본 Java 지식** – 클래스 생성, 예외 처리, 파일 경로 작업에 익숙해야 합니다.  
5. **샘플 PSD 파일** – Adobe Photoshop에서 만들거나 온라인에서 무료 샘플을 구하십시오.

## PSD를 PNG로 내보내는 단계별 방법

## PSD 색상 모드를 16‑비트 그레이스케일로 설정하는 방법은?
`PsdImage`는 PSD 파일을 메모리로 로드하는 Aspose.PSD 클래스이며, `ColorMode`는 PSD 이미지의 색상 모드를 정의하는 열거형입니다.  

`PsdImage`로 PSD를 로드하고 `ColorMode` 속성을 사용해 색상 모드를 변경한 뒤 수정된 파일을 저장합니다. 이 작업은 전부 메모리 내에서 수행되므로 중간 파일이 필요 없으며 변환이 빠르고 효율적입니다.

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

이러한 import 문을 통해 PSD 파일을 조작하고 색상 모드를 설정한 뒤 PNG로 내보내는 기능에 접근할 수 있습니다.

## 소스 및 출력 디렉터리를 정의하는 방법은?
`File`은 파일 시스템상의 파일 또는 디렉터리 경로를 나타내는 java.io 클래스입니다.  

프로그램에 원본 PSD를 읽을 위치와 변환된 PNG를 쓸 위치를 알려줘야 합니다. 절대 경로나 상대 경로를 사용할 수 있지만, 환경마다 일관되게 유지하여 경로 해석 오류를 방지하십시오.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

플레이스홀더 문자열을 실제 머신의 경로로 교체하십시오.

## 재사용 가능한 메서드에 변환 로직을 캡슐화하는 방법은?
`convertPsdToPng`는 PSD 파일을 PNG로 변환하는 모든 단계를 캡슐화한 사용자 정의 메서드입니다.  

전용 메서드를 만들면 여러 파일이나 다양한 설정에 대해 동일한 변환 단계를 재사용할 수 있습니다. 소스 경로, 대상 폴더, 선택적 압축 수준과 같은 매개변수를 전달해 워크플로를 유연하고 유지 보수하기 쉽게 만듭니다.

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

이 메서드를 사용하면 **PSD 색상 모드를 설정**하고 **PSD를 PNG로 내보내기**를 한 흐름에서 수행할 수 있습니다.

## PSD를 로드하고 16‑비트 그레이스케일 모드를 적용하는 방법은?
`PsdImage`는 PSD 파일을 메모리로 로드하는 Aspose.PSD 클래스입니다.  
`ColorMode.GRAYSCALE_16`은 이미지를 16‑비트 그레이스케일로 설정하는 열거형 값입니다.  
`channelBitsCount`는 채널당 비트 수를 지정하는 속성입니다.  

변환 메서드 내부에서 전체 파일 경로를 구성하고 `PsdImage`를 인스턴스화한 뒤 `ColorMode`를 `ColorMode.GRAYSCALE_16`으로 변경합니다. `channelBitsCount` 속성을 16으로 설정해야 높은 비트 깊이를 유지하여 이미지가 모든 톤 정보를 보존합니다.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix`는 각 내보낸 파일에 사용된 설정을 추적하는 데 도움이 됩니다.

## 이미지에 미세한 테두리를 그리는 방법 (선택 단계)?
`Graphics`는 `PsdImage` 캔버스에 그리기 기능을 제공하는 클래스입니다.  

테스트 중에 출력이 더 잘 보이도록 회색 사각형을 이미지 주변에 그릴 수 있습니다. 이 단계는 레이어와 그래픽 객체를 다루는 방법을 보여주며, 사각형은 이미지 크기에 관계없이 중앙에 위치하도록 동적으로 계산됩니다.

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

## 새로운 색상 모드로 수정된 PSD를 저장하는 방법은?
`PsdOptions`는 색상 모드와 비트 깊이 설정을 포함해 PSD 파일 저장 방식을 제어하는 클래스입니다.  

그리기(또는 생략) 후 `PsdImage` 인스턴스에서 `save`를 호출하고, 16‑비트 그레이스케일 구성을 보존하는 `PsdOptions` 객체를 전달합니다. 이렇게 하면 데이터 손실 없이 원하는 색상 모드가 유지된 PSD가 저장됩니다.

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

## 16‑비트 깊이를 유지하면서 PSD를 PNG로 변환하는 방법은?
`PngOptions`는 색상 유형 및 압축 수준과 같은 PNG 출력 설정을 정의하는 클래스입니다.  
`PngColorType.GrayscaleWithAlpha`는 알파 채널과 함께 16‑비트 그레이스케일 데이터를 저장하는 열거형 값입니다.  

새로 저장한 PSD를 로드하고 `PngOptions`를 `PngColorType.GrayscaleWithAlpha`로 구성한 뒤 `save`를 호출합니다. 이렇게 하면 PNG 파일 내부에 16‑비트 그레이스케일 데이터가 보존되어 손실 없는 고품질 이미지를 얻을 수 있습니다.

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

이제 **PSD를 PNG로 내보내면서** 고품질 16‑비트 그레이스케일 데이터를 유지했습니다.

## 일반적인 문제 및 해결책
| 문제 | 발생 원인 | 해결 방법 |
|------|----------|----------|
| **“Unsupported color type” 예외** | 지원되지 않는 채널 구성을 가진 PSD를 저장하려고 할 때 발생합니다. | `channelBitsCount`가 실제 비트 깊이(16)와 일치하고, 그레이스케일(1) 채널 수가 올바른지 확인하십시오. |
| **파일을 찾을 수 없음** | 소스 디렉터리 경로가 잘못되었습니다. | `sourceDir` 문자열을 다시 확인하고 해당 위치에 PSD 파일이 존재하는지 확인하십시오. |
| **출력 PNG가 검게 표시됨** | 알파 처리가 올바르게 이루어지지 않아 PNG가 저장될 때 발생합니다. | 위와 같이 `PngColorType.GrayscaleWithAlpha`를 사용하십시오. |
| **대용량 PSD에서 메모리 초과** | 전체 파일을 메모리에 로드하기 때문입니다. | `PsdImage.load(inputStream, new LoadOptions())`를 사용해 스트리밍 모드를 활성화하면 대용량 파일을 효율적으로 처리할 수 있습니다. |

## 자주 묻는 질문

**Q: 16‑비트 그레이스케일 색상 모드란 무엇입니까?**  
A: 65 536가지 회색 음영을 제공하여 표준 8‑비트(256음)보다 훨씬 풍부한 톤 디테일을 제공합니다.

**Q: 비그레이스케일 이미지에도 Aspose.PSD를 사용할 수 있나요?**  
A: 물론 가능합니다! Aspose.PSD는 RGB, CMYK, Lab, 인덱스 및 기타 다양한 색상 모드를 지원합니다.

**Q: Aspose.PSD 체험판이 있나요?**  
A: 예, Aspose.PSD의 무료 체험판을 사용할 수 있습니다. [Aspose 다운로드 페이지](https://releases.aspose.com/)로 이동하십시오.

**Q: 더 많은 Aspose.PSD 예제를 어디서 찾을 수 있나요?**  
A: 공식 [문서](https://reference.aspose.com/psd/java/)에서 심층 튜토리얼, API 레퍼런스 및 샘플 프로젝트를 확인하십시오.

**Q: Aspose.PSD 라이선스를 어떻게 구매하나요?**  
A: [Aspose 구매 페이지](https://purchase.aspose.com/buy)에서 라이선스를 구매할 수 있습니다.

**마지막 업데이트:** 2026-09-28  
**테스트 환경:** Aspose.PSD for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.PSD for Java를 사용하여 지정된 비트 깊이로 PSD를 PNG로 변환하기](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Aspose.PSD for Java를 사용하여 레이어 효과와 함께 PSD를 PNG로 내보내기](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Aspose.PSD Java로 PSD를 JPEG로 저장하고 RGB 색상 지원하기](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
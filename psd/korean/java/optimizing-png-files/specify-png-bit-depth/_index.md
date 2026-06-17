---
date: 2026-03-18
description: Aspose.PSD for Java를 사용하여 PSD를 PNG로 변환하고 PNG 비트 깊이를 변경하는 방법을 배우세요 – 단계별
  가이드와 코드 샘플 포함.
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 지정된 비트 깊이로 PSD를 PNG로 변환하는 방법
url: /ko/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 지정된 비트 깊이로 PSD를 PNG로 변환하기

## Introduction
**convert psd to png**가 필요하고 정확한 PNG 비트 깊이를 제어하고 싶다면, 여기서 바로 해결할 수 있습니다. 이 튜토리얼에서는 Aspose.PSD for Java를 사용해 PSD 파일을 PNG 이미지로 저장하면서 png 비트 깊이를 변경하는 방법을 단계별로 안내합니다. 배치 처리 도구, 웹 서비스, 데스크톱 유틸리티 등 어떤 환경에서든 **save png with options**(예: 그레이스케일 색상 유형 및 사용자 정의 비트 깊이)를 활용하면 이미지 품질과 파일 크기를 세밀하게 조정할 수 있습니다.

## Quick Answers
- **Can I change the PNG bit depth?** 예 – `PngOptions.setBitDepth()`를 사용해 1, 2, 4, 8 또는 16 비트를 지정합니다.  
- **Which color types are supported?** `PngColorType`을 통해 그레이스케일, TrueColor, Indexed 등 다양한 색상 유형을 지원합니다.  
- **Do I need a license for Aspose.PSD?** 개발 단계에서는 무료 체험판으로 충분하지만, 실제 운영에서는 상용 라이선스가 필요합니다.  
- **What Java version is required?** Java 8 이상(라이브러리는 최신 JDK와도 호환됩니다).  
- **Is the code runnable as‑is?** 예 – 자리표시자 경로를 자신의 폴더 경로로 교체하면 바로 실행됩니다.

## What is “convert psd to png” with custom bit depth?
PSD 파일을 PNG 이미지로 변환하는 것은 웹 친화적인 포맷이 필요할 때 흔히 수행하는 작업입니다. 비트 깊이를 설정해 **adjust png quality**를 조절하면 시각적 충실도와 파일 크기 사이의 균형을 맞출 수 있어 썸네일, 아이콘 또는 대역폭이 제한된 환경에서 특히 유용합니다.

## Why use Aspose.PSD for Java?
Aspose.PSD for Java는 PSD 포맷의 복잡성을 추상화한 고수준 API를 제공합니다. 이를 통해 **create grayscale png**, **save png with options**를 손쉽게 수행하고 색상 프로파일을 저수준 바이트 조작 없이 처리할 수 있습니다. 라이브러리는 완전 관리형이며 크로스‑플랫폼을 지원하고 정기적으로 업데이트됩니다.

## Prerequisites
코드를 진행하기 전에 아래 항목을 준비하세요:

1. **Java Development Kit (JDK)** – [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드합니다.  
2. **Aspose.PSD for Java** – [this link](https://releases.aspose.com/psd/java/)에서 최신 JAR 파일을 받습니다.  
3. **Basic Java knowledge** – 클래스, 메서드, 예외 처리에 익숙해야 합니다.  
4. **An IDE** such as IntelliJ IDEA or Eclipse (optional but recommended).  
5. **A sample PSD file** – 코드에서 참조할 폴더에 배치합니다.

모두 준비됐나요? 좋습니다 – 이제 필요한 패키지를 가져옵니다.

## Import Packages
필요한 패키지를 Java 파일 상단에 추가하여 환경을 설정합니다. 코딩 환경을 열고 다음 import 문을 삽입하세요:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

이 선언문들은 튜토리얼 전반에 걸쳐 PSD 파일을 로드하고 지정된 비트 깊이로 PNG 이미지로 저장하는 데 사용되는 클래스를 가져옵니다.

## Step 1: Set Up Your Document Directory
이미지 저장 위치를 정의합니다. 이는 작업을 시작하기 전에 미술 도구를 정리하는 것과 같습니다.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the PSD Image
변환하려는 PSD 파일을 로드합니다. 캔버스를 열어 작업을 시작하는 단계라고 생각하면 됩니다.

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

여기서는 `Image.load()` 메서드를 사용해 샘플 PSD 파일을 읽고 `PsdImage`로 캐스팅하여 PSD 전용 속성에 접근합니다.

## Step 3: Create PNG Options
캔버스를 열었으니 이제 이미지를 저장할 옵션을 설정합니다. 이는 그림을 시작하기 전에 색상과 브러시 스타일을 선택하는 것과 같습니다.

```java
PngOptions options = new PngOptions();
```

이 단계에서는 PNG 출력 매개변수를 지정할 수 있는 `PngOptions` 인스턴스를 초기화합니다.

## Step 4: Set the Desired Color Type
최종 PNG 이미지에 어떤 색상을 사용할지 결정합니다. 다채로운 팔레트를 원하시나요, 아니면 단색 스타일을 원하시나요? 여기서 선택합니다!

```java
options.setColorType(PngColorType.Grayscale);
```

예제에서는 색상 유형을 그레이스케일로 설정합니다. 전체 색상을 원한다면 `PngColorType.TrueColor`를 선택할 수 있습니다. 이 단계가 **create grayscale png**를 수행하는 부분입니다.

## Step 5: Specify the Bit Depth
이제 비트 깊이를 지정합니다. 이는 프린터에게 얼마나 세밀하게 인쇄할지를 알려주는 것과 비슷합니다 – 비트가 많을수록 디테일이 살아납니다!

```java
options.setBitDepth((byte)1);
```

여기서는 **1 bit** 비트 깊이를 설정했으며, 이는 단순한 그레이스케일 이미지에 적합합니다. 필요에 따라 2, 4, 8, 16 비트로 변경하여 **change png bit depth**를 구현할 수 있습니다.

## Step 6: Save the PNG Image
마지막으로 작품을 저장합니다! 이 단계에서 편집 캔버스의 작업물을 갤러리 벽에 전시합니다.

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

`PsdImage`의 `save()` 메서드를 사용해 앞서 정의한 옵션을 적용해 변환된 파일을 저장합니다. 이제 이미지가 사용자 정의 비트 깊이로 저장되었습니다.

## Common Issues and Solutions
- **`NullPointerException` when loading the PSD** – `dataDir`이 올바른 폴더를 가리키고 `sample.psd` 파일이 존재하는지 다시 확인하세요.  
- **Unsupported bit depth** – Aspose.PSD는 PNG에 대해 1, 2, 4, 8, 16 비트를 지원합니다. 다른 값을 사용하면 `IllegalArgumentException`이 발생합니다.  
- **Color type mismatch** – 선택한 `PngColorType`과 호환되지 않는 비트 깊이를 지정하면 라이브러리가 자동으로 가장 가까운 지원 설정으로 조정합니다.

## Frequently Asked Questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java는 Java 애플리케이션에서 PSD 파일을 다루기 위한 라이브러리로, 이미지 조작 및 변환 기능을 제공합니다.

**Q: How do I specify different bit depths?**  
A: `options.setBitDepth((byte)n)` 메서드를 사용해 `n`을 원하는 비트 깊이 값으로 교체하면 됩니다.

**Q: Can I use Aspose.PSD for free?**  
A: 예, 무료 체험판을 이용할 수 있으며, 해당 링크에서 확인할 수 있습니다: [here](https://releases.aspose.com/).

**Q: Where can I get a support license for Aspose?**  
A: 임시 라이선스는 여기에서 신청할 수 있습니다: [here](https://purchase.aspose.com/temporary-license/).

**Q: What type of images can I convert?**  
A: Aspose.PSD는 주로 PSD 파일을 다루지만 PNG, JPEG, TIFF 등 다양한 포맷으로 변환을 지원합니다.

## Conclusion
이제 Aspose.PSD for Java를 사용해 **convert psd to png**하면서 PNG 비트 깊이를 제어하는 방법을 익혔습니다. `PngOptions`를 조정하면 **adjust png quality**, **create grayscale png**를 구현하고, 다양한 시나리오에 맞게 파일 크기를 미세 조정할 수 있습니다. 다양한 색상 유형과 비트 깊이를 실험해 보며 최적의 균형을 찾아보세요.

---

**Last Updated:** 2026-03-18  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
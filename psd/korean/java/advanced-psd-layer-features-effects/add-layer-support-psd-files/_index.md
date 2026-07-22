---
date: 2026-07-22
description: Aspose.PSD for Java를 사용하여 PSD 레이어를 추출하고 PSD 레이어를 PNG로 변환하는 방법을 배웁니다.
  강력한 그래픽 조작이 필요한 개발자에게 적합합니다.
keywords:
- extract psd layers
- how to extract psd
- convert psd to png
lastmod: 2026-07-22
linktitle: Aspose.PSD Java를 사용하여 PSD 레이어 추출 및 PSD 파일에 레이어 지원 추가
og_description: Aspose.PSD for Java를 사용하여 PSD 레이어를 추출하고 PNG로 변환합니다. 단계별 가이드를 따라 레이어
  추출 및 이미지 변환을 자동화하세요.
og_image_alt: Developer guide showing Java code to extract PSD layers and save as
  PNG using Aspose.PSD
og_title: PSD 레이어 추출 – Aspose.PSD Java를 사용하여 PSD 파일에 레이어 지원 추가
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  headline: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
    Java
  type: TechArticle
- description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  name: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD Java
  steps:
  - name: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
    text: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
    text: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that allows you to manipulate PSD files
      without having Photoshop installed.
    question: What is Aspose.PSD for Java?
  - answer: Yes! While primarily for PSD files, Aspose offers libraries for a wide
      range of formats, including AI, PDF, and SVG.
    question: Can I use Aspose.PSD for other file formats?
  - answer: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: Access the Aspose forum for PSD‑related questions [here](https://forum.aspose.com/c/psd/34).
    question: Where can I get support if I run into problems?
  - answer: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer,
      and save it with its own `PngOptions`. This yields individual PNG files per
      layer.
    question: Can I convert each layer to a separate PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract psd
- Aspose.PSD
- Java image processing
title: Aspose.PSD Java를 사용하여 PSD 레이어 추출 및 PSD 파일에 레이어 지원 추가
url: /ko/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java를 사용하여 PSD 레이어 추출 및 레이어 지원 추가

## 소개
Photoshop Document(PSD) 파일 작업은 그래픽 디자이너와 개발자 모두에게 일상적인 현실이며, **extract psd layers**는 자산을 재사용하거나 이미지 파이프라인을 자동화하기 위한 첫 번째 단계인 경우가 많습니다. 이 튜토리얼에서는 PSD에서 개별 레이어를 추출하고 전체 레이어 지원을 활성화하며 Aspose.PSD for Java를 사용해 **PSD 레이어를 PNG로 변환**하는 방법을 배웁니다. 환경 설정부터 모범 사례 팁까지 모두 다루므로 몇 분 안에 이 워크플로를 어떤 Java 애플리케이션에도 통합할 수 있습니다.

## 빠른 답변
- **“extract PSD layers”는 무엇을 의미하나요?** PSD 파일을 로드하고 각 개별 레이어에 접근하여 조작하거나 내보내는 것을 의미합니다.  
- **Java에서 이를 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java는 Photoshop 없이도 완전한 PSD 처리를 제공합니다.  
- **PSD 레이어를 한 번에 PNG로 변환할 수 있나요?** 네—적절한 옵션으로 파일을 로드하고 투명성을 보존하는 PNG 옵션으로 저장하면 됩니다.  
- **프로덕션 사용에 라이선스가 필요합니까?** 프로덕션에서는 상용 라이선스가 필요합니다; 평가용 무료 체험판을 이용할 수 있습니다.  
- **필요한 Java 버전은 무엇인가요?** JDK 8 이상 (예제에서는 JDK 11 사용).

## Aspose.PSD for Java를 사용해 PSD 레이어를 추출하는 방법은?
PSD를 로드하고 레이어 효과를 활성화한 뒤 몇 줄의 Java 코드만으로 PNG로 저장합니다. 이 직접적인 접근 방식은 서버에서 Photoshop이 필요 없게 하며 Java 8+을 지원하는 모든 플랫폼에서 동작합니다.  
먼저 `setLoadEffectsResource(true)`와 `setUseDiskForLoadEffectsResource(true)`가 설정된 `PsdLoadOptions` 객체를 만든 뒤 `PsdImage.load(path, options)`로 파일을 로드합니다. 로드 후에는 `image.save(outputPath, new PngOptions())`로 레이어를 병합해 저장하거나 `image.getLayers()`를 순회해 각 레이어를 개별적으로 내보낼 수 있으며, 모든 효과를 유지하면서 메모리 사용량을 최소화합니다.

## PSD 레이어를 추출하고 PNG로 변환하는 이유는?
레이어를 추출하면 **자산 재사용**, **썸네일 자동 생성**, **웹용 그래픽을 위한 투명도 보존**이 가능합니다. Aspose.PSD는 **50개 이상의 입력·출력 포맷**을 지원하며, 디스크 기반 리소스 처리를 통해 전체 파일을 메모리에 로드하지 않고도 수백 페이지 규모의 PSD 파일을 처리할 수 있습니다.

## 전제 조건
시작하기 전에 다음 항목을 준비하세요:

1. **Java 개발 환경** – JDK가 설치되어 있어야 합니다. [Oracle 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드할 수 있습니다.  
2. **Aspose.PSD for Java** – 공식 다운로드 페이지에서 최신 라이브러리를 받으세요: [여기](https://releases.aspose.com/psd/java/).  
3. **기본 Java 지식** – Java 프로그램을 컴파일하고 실행하는 방법에 익숙해야 합니다.  
4. **IDE** – IntelliJ IDEA, Eclipse 또는 선호하는 편집기.  
5. **PSD 파일** – 보유하고 있는 PSD 파일을 사용하거나 테스트용 샘플 PSD를 다운로드하세요.

위 항목을 모두 준비하면 PSD 레이어 추출을 시작할 수 있습니다.

## 패키지 가져오기
워크플로의 핵심은 `PsdImage`, `PsdLoadOptions`, `PngOptions` 클래스입니다.  

`PsdImage`는 메모리 내에서 단일 PSD 파일을 나타내는 Aspose.PSD의 최상위 객체입니다.  

`PsdLoadOptions`는 레이어 효과와 같은 리소스를 어떻게 로드할지 제어합니다.  

`PngOptions`는 PNG 파일의 출력 포맷과 투명도 처리를 정의합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 1단계: 디렉터리 정의
소스 PSD와 출력 PNG의 경로를 설정합니다. `dataDir`을 파일이 위치한 폴더로 지정하세요.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"Your Document Directory"`를 실제 폴더 경로로 교체합니다.  
- `sourceFileName` – 처리하려는 PSD 파일의 전체 경로.  
- `output` – 추출된 레이어가 포함된 PNG가 저장될 대상 경로.

## 2단계: 로드 옵션 설정
`PsdLoadOptions`를 구성하면 모든 레이어 효과와 리소스가 올바르게 로드되어 **extract PSD layers** 작업에 필수적입니다.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – 레이어에 연결된 드롭 섀도우와 같은 추가 효과를 로드합니다.  
- `setUseDiskForLoadEffectsResource(true)` – 무거운 리소스를 디스크에 오프로드해 메모리 압력을 낮춥니다.

## 3단계: PSD 파일 로드
앞서 정의한 옵션을 사용해 `PsdImage` 객체에 PSD를 로드합니다.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

이 시점에서 `image`는 모든 레이어, 마스크, 효과를 포함하고 있어 추출 준비가 완료됩니다.

## 4단계: 저장 옵션 설정
PNG 저장 방식을 구성합니다. `TruecolorWithAlpha`를 사용하면 원본 레이어의 투명도가 보존됩니다.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## 5단계: 이미지 저장 (PSD 레이어를 PNG로 변환)
로드한 PSD(전체 레이어 포함)를 하나의 PNG 파일로 내보냅니다. 이 단계가 바로 **convert psd layers png** 작업입니다.

```java
image.save(output, saveOptions);
```

각 레이어를 개별 PNG로 저장하려면 `image.getLayers()`를 순회하면 되지만, 많은 경우 병합된 PNG 하나면 충분합니다.

## 6단계: 마무리
프로세스가 성공했음을 알리는 친절한 콘솔 메시지를 추가합니다.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## 일반적인 문제 및 팁
- **Out‑of‑Memory 오류:** 매우 큰 PSD를 처리할 경우 `setUseDiskForLoadEffectsResource(true)`를 유지해 임시 데이터를 디스크에 오프로드하세요.  
- **효과 누락:** `setLoadEffectsResource(true)`가 설정되어 있는지 확인하세요. 그렇지 않으면 일부 레이어 효과가 무시될 수 있습니다.  
- **경로 문제:** 플랫폼에 독립적인 경로 처리를 위해 `java.nio.file`의 `Paths.get(...)`를 사용하세요.

## 자주 묻는 질문

**Q: Aspose.PSD for Java란 무엇인가요?**  
A: Aspose.PSD for Java는 Photoshop을 설치하지 않아도 PSD 파일을 조작할 수 있게 해주는 라이브러리입니다.

**Q: 다른 파일 포맷에도 Aspose.PSD를 사용할 수 있나요?**  
A: 네! 주로 PSD용이지만, Aspose는 AI, PDF, SVG 등 다양한 포맷을 위한 라이브러리도 제공합니다.

**Q: 체험판을 사용할 수 있나요?**  
A: 물론입니다! 무료 체험판을 [여기](https://releases.aspose.com/)에서 다운로드할 수 있습니다.

**Q: 문제가 발생하면 어디서 지원을 받을 수 있나요?**  
A: PSD 관련 질문은 Aspose 포럼에서 확인하세요: [여기](https://forum.aspose.com/c/psd/34).

**Q: 각 레이어를 별도의 PNG로 변환할 수 있나요?**  
A: `image.getLayers()`를 순회하면서 각 레이어에 대해 새로운 `Bitmap`을 만들고 고유한 `PngOptions`로 저장하면 레이어당 개별 PNG 파일을 얻을 수 있습니다.

## 결론
이제 **extract PSD layers**, 전체 레이어 지원 활성화, 그리고 Aspose.PSD for Java를 사용해 **PSD 레이어를 PNG로 변환**하는 방법을 익혔습니다. 자동화된 자산 파이프라인을 구축하거나 데스크톱 앱에 그래픽 기능을 추가하든, 이 접근 방식은 Photoshop 없이도 Photoshop 파일을 세밀하게 제어할 수 있게 해줍니다. 필터 적용, 프로그래밍 방식 레이어 병합, 또는 레이어별 개별 내보내기 등 워크플로에 맞게 확장해 보세요.

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose

## 관련 튜토리얼

- [Aspose.PSD for Java를 사용해 PSD를 PNG로 내보내고 새 일반 레이어 추가](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Java에서 레이어 마스크 지원을 포함한 PSD를 PNG로 내보내기](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Java에서 PSD를 이미지로 변환 – Aspose.PSD로 조정 레이어 적용](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}
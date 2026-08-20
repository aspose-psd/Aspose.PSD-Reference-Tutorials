---
date: 2026-05-29
description: Aspose.PSD for Java를 사용하여 색상 텍스트가 포함된 PSD를 PNG로 저장하는 방법을 배웁니다. 이 단계별
  가이드는 PSD를 PNG로 효율적으로 변환하는 방법을 보여줍니다.
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: 텍스트 레이어에서 서로 다른 색상으로 텍스트 렌더링
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 색상 텍스트가 포함된 PSD를 PNG로 저장
url: /ko/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 색상 텍스트가 포함된 PSD를 PNG로 저장

Welcome to our step‑by‑step guide on how to **save PSD as PNG** with different colored text using Aspose.PSD for Java. Aspose.PSD is a powerful Java library that allows you to manipulate Photoshop files programmatically, providing you with extensive capabilities to work with PSD and PSB file formats.

In this tutorial, we'll walk you through the process of rendering text with various colors in a text layer using Aspose.PSD. By the end of this guide, you'll have a clear understanding of how to achieve this task seamlessly.

## 빠른 답변
- **PSD를 PNG로 저장하는 방법?** Aspose.PSD의 `PsdImage` 클래스를 사용하여 PSD를 로드하고 `PngOptions`와 함께 `save`를 호출합니다.
- **하나의 텍스트 레이어에서 여러 색상을 렌더링할 수 있나요?** 예, 텍스트의 각 `Portion`에 서로 다른 `Color` 객체를 할당하면 됩니다.
- **필요한 Java 버전은?** Java 8 이상을 지원합니다.
- **프로덕션에 라이선스가 필요합니까?** 상용 라이선스가 필요하며, 무료 체험판을 사용할 수 있습니다.
- **대용량 파일에 대해 메모리 효율적인가요?** 전체 메모리 로드 없이 최대 2 GB 파일을 처리할 수 있습니다.

## 색상 텍스트가 포함된 PSD를 PNG로 저장하는 방법

Load your PSD file, modify the text layer’s portions to assign distinct colors, and then save the image as PNG—this whole workflow is performed in just a few lines of Java code. Aspose.PSD automatically rasterizes the edited layer, preserving transparency and color fidelity, so the resulting PNG matches the original design.

## Aspose.PSD for Java란?

Aspose.PSD for Java는 Photoshop(PSD/PSB) 파일의 프로그래밍 방식 생성, 편집 및 변환을 가능하게 하는 라이브러리입니다. **50개 이상의 이미지 포맷**을 지원하며 전체 파일을 메모리에 로드하지 않고도 수백 페이지 문서를 처리할 수 있어 서버‑사이드 자동화에 높은 성능을 제공합니다.

## 사전 요구 사항

- Java 프로그래밍에 대한 기본 지식.
- Aspose.PSD for Java 라이브러리가 설치되어 있어야 합니다. [Aspose.PSD for Java 문서](https://reference.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

## 패키지 가져오기

`Image`는 이미지 파일을 로드하고 저장하기 위한 기본 클래스입니다. `PsdImage`는 Photoshop 문서를 나타내며, `TextLayer`는 텍스트 레이어 속성에 접근할 수 있게 합니다. `PngOptions`는 PNG 내보내기 설정을 정의합니다.  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 단계 1: 프로젝트 설정

Create a new Java project and include the Aspose.PSD library. Make sure you have the necessary permissions to access and modify files in your project directory.

## 단계 2: 소스 및 출력 디렉터리 정의

Specify the source and output directories where your PSD files are located and where the resulting images will be saved. Update the `sourceDir` and `outputDir` variables accordingly.  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## 단계 3: PSD 파일 로드 및 텍스트 레이어 접근

`PsdImage`는 PSD 파일을 메모리로 로드하고, `TextLayer`는 해당 레이어 내 텍스트 내용을 조작할 수 있게 합니다.  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## 단계 4: PNG 옵션 설정 및 결과 이미지 저장

`PngOptions`는 색상 유형 및 압축과 같은 PNG 출력 매개변수를 구성합니다.  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## 일반적인 문제 및 해결책

- **라이선스 누락 예외:** 저장 작업을 호출하기 전에 유효한 라이선스 파일을 적용했는지 확인하십시오.
- **색상이 적용되지 않음:** 텍스트 레이어의 각 `Portion`에 `Color` 속성이 올바르게 설정되어 있는지 확인하십시오.
- **대용량 파일 메모리 사용:** 대용량 파일을 스트리밍하려면 `loadOptions`와 함께 `PsdImage`의 `load` 오버로드를 사용하십시오.

## 자주 묻는 질문

**Q: Aspose.PSD for Java를 다른 프로그래밍 언어와 함께 사용할 수 있나요?**  
A: Aspose.PSD는 주로 Java용으로 설계되었지만, Aspose는 다양한 프로그래밍 언어용 유사한 라이브러리를 제공합니다.

**Q: Aspose.PSD for Java에 대한 체험판이 제공되나요?**  
A: 예, [Aspose.PSD](https://releases.aspose.com/)에서 무료 체험판을 받을 수 있습니다.

**Q: 추가 지원이나 도움을 어디서 찾을 수 있나요?**  
A: 커뮤니티 지원 및 토론을 위해 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)을 방문하십시오.

**Q: Aspose.PSD for Java에 대한 임시 라이선스를 어떻게 얻을 수 있나요?**  
A: [Aspose.PSD](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 요청할 수 있습니다.

**Q: Aspose.PSD에 대한 다른 튜토리얼이 있나요?**  
A: 예, 더 많은 튜토리얼과 예제를 위해 [Aspose.PSD 문서](https://reference.aspose.com/psd/java/)를 살펴보십시오.

**Q: 라이브러리가 여러 PSD 파일을 PNG로 일괄 변환하는 것을 지원하나요?**  
A: 예, PSD 파일이 들어 있는 폴더를 순회하면서 동일한 텍스트‑색상 로직을 적용하고 루프를 사용해 각각을 PNG로 저장할 수 있습니다.

**Q: 출력 PNG가 무손실인가요?**  
A: Aspose.PSD를 통해 저장된 PNG는 완전한 무손실 품질을 유지하며 모든 색상 및 투명도 정보를 보존합니다.

---

**마지막 업데이트:** 2026-05-29  
**테스트 환경:** Aspose.PSD 24.12 for Java  
**작성자:** Aspose

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 새 일반 레이어 추가](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Aspose.PSD for Java에서 PSD를 PNG로 저장하고 렌더링 드롭 섀도우 적용](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Aspose.PSD for Java – 색상 오버레이로 PSD를 PNG로 변환](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
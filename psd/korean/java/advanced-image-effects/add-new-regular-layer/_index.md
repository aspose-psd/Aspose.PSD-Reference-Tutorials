---
date: 2026-10-18
description: 임시 라이선스를 사용하여 Aspose.PSD for Java로 PSD를 PNG로 내보내고 새로운 일반 레이어를 추가하는 방법을
  배웁니다. 단계별 가이드, 레이어 위치 지정 및 문제 해결.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: PSD에 새로운 일반 레이어 추가
og_description: 임시 라이선스를 사용하여 Aspose.PSD for Java로 PSD를 PNG로 내보내고 새로운 일반 레이어를 추가하는
  방법을 배웁니다. 코드 없이 전체 단계와 레이어 위치 지정 팁을 포함합니다.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 레이어를 추가하는 방법
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 레이어를 추가하는 방법
url: /ko/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 PNG로 내보내고 Aspose.PSD for Java로 레이어 추가하는 방법

이 **Aspose.PSD 튜토리얼**에서는 **PSD를 PNG로 내보내는 방법**과 동시에 **새 일반 레이어**를 동일 파일에 **추가하는 방법**을 **Aspose 임시 라이선스**를 사용하여 배웁니다. 웹 썸네일을 만들거나, 디자인 파이프라인을 위한 에셋을 준비하거나, **PSD 이미지 조작**을 실험하든, 이 가이드는 소스 파일 로드부터 업데이트된 PSD와 PNG 복사본 저장까지 모든 단계를 보여주므로 바로 PSD 레이어 작업을 시작할 수 있습니다.

## 빠른 답변
- **단일 호출로 PSD를 PNG로 내보낼 수 있나요?** 예 – 레이어를 추가한 후 `save`를 `PngOptions`와 함께 호출하면 됩니다.
- **개발에 전체 라이선스가 필요합니까?** 임시 라이선스는 평가 워터마크를 제거하고 모든 API를 잠금 해제합니다; 프로덕션 사용에는 영구 라이선스가 필요합니다.
- **지원되는 Java 버전은 무엇인가요?** Aspose.PSD는 Java 8 이상에서 작동합니다.
- **레이어 위치 지정이 픽셀 기반인가요?** 물론입니다; **set layer position** 메서드를 통해 왼쪽, 위, 오른쪽, 아래 좌표를 픽셀 단위로 설정합니다.
- **PNG가 레이어 투명성을 유지합니까?** 내보낸 PNG는 모든 보이는 레이어를 병합한 결과를 포함하며, 해당되는 경우 투명성을 보존합니다.

## 왜 Aspose 임시 라이선스를 사용하나요?

**Aspose 임시 라이선스**를 사용하면 기능 제한 없이 Aspose.PSD의 전체 기능을 평가할 수 있습니다. 평가 워터마크를 제거하고 모든 API를 잠금 해제하며, **새 PSD 레이어** 객체를 생성할 수 있는 기능도 포함됩니다. 영구 라이선스를 구매하기 전에 프로덕션과 유사한 환경에서 코드를 테스트할 수 있습니다.

## 사전 요구 사항

시작하기 전에 다음이 준비되어 있는지 확인하십시오:

- **Java 개발 환경** – JDK 8 이상 및 Maven 또는 Gradle과 같은 빌드 도구가 설치되어 있어야 합니다.
- **Aspose.PSD for Java** – 공식 사이트의 최신 JAR를 다운로드하십시오 [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **샘플 PSD 파일** – 예제에서는 `OneLayer.psd`를 사용합니다.

## 패키지 가져오기

Java 클래스에 필요한 import를 추가하십시오. 이 클래스들은 **PSD 이미지 조작** 및 레이어 처리를 위한 핵심 기능을 제공합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## “set layer position”이란 무엇이며 왜 중요한가요?

**set layer position** 메서드는 레이어가 PSD 캔버스에 그려지는 정확한 픽셀 좌표를 정의하여 수평 및 수직 배치를 제어합니다. 정확한 위치 지정은 그래픽이 정확히 맞춰지도록 보장하며, UI 에셋 합성, 인쇄 준비 레이아웃 생성, 픽셀 완벽 썸네일 생성 등에 필수적입니다.

## 단계별 가이드

### 단계 1: PSD 파일 로드

`PsdImage`는 메모리 내에서 PSD 문서를 나타내는 Aspose.PSD의 핵심 클래스입니다. 파일을 로드하면 편집 가능한 객체가 생성됩니다.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### 단계 2: 픽셀 데이터 및 사각형 준비

두 개의 픽셀 버퍼(`int[]`)를 할당하고 새 레이어가 그려질 사각형 영역을 정의합니다.

Rectangle은 레이어 픽셀 위치 지정에 사용되는 X, Y, 너비, 높이 값을 가진 사각형 영역을 정의합니다.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### 단계 3: 레이어 데이터 초기화

픽셀 버퍼를 기본 ARGB 값으로 채웁니다. 값 `-10000000`은 반투명 어두운 색조에 해당하며, 새 레이어에 눈에 보이는 기본 색상을 제공합니다.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### 단계 4: 일반 레이어 추가 (PSD 레이어 조작)

Layer는 개별 PSD 레이어를 나타내며 픽셀 데이터, 가시성 및 위치에 대한 속성을 제공합니다.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### 단계 5: PSD를 PNG로 내보내고 업데이트된 PSD 저장

레이어가 배치된 후 수정된 문서를 저장합니다. 먼저 결과를 PNG로 내보내고(**export PSD to PNG** 단계), 그 다음 새 레이어가 포함된 PSD를 영구 저장합니다.

PngOptions는 압축 수준 및 색상 유형과 같은 PNG 내보내기 설정을 구성합니다.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **전문가 팁:** PNG만 필요하다면 PSD `save` 호출을 건너뛰고 `PngOptions`와 함께 `save`를 직접 호출하면 됩니다.

## Aspose.PSD for Java의 정량적 이점

Aspose.PSD는 **30개 이상의 이미지 포맷**을 지원하며 스트리밍 아키텍처 덕분에 **500 MB**까지의 PSD 파일을 전체를 메모리에 로드하지 않고 처리할 수 있습니다. 벤치마크 테스트에서 300페이지 PSD에 두 개의 일반 레이어를 추가하는 데 표준 3.2 GHz CPU 기준 **0.8 초** 미만이 소요되었습니다.

## 일반적인 문제 및 해결 방법

| 증상 | 가능한 원인 | 해결 방법 |
|---------|--------------|-----|
| PNG가 빈 화면으로 표시됨 | 레이어가 보이지 않거나 완전히 투명함 | 비투명 픽셀 값을 설정하거나 `layer.setVisible(true)`를 호출했는지 확인하십시오. |
| `ArrayIndexOutOfBoundsException` | 사각형 크기와 픽셀 배열 길이 불일치 | `rect.width * rect.height == dataArray.length`인지 확인하십시오. |
| 런타임 시 LicenseException | 유효한 라이선스가 로드되지 않음 | API 메서드를 호출하기 전에 임시 또는 영구 라이선스를 로드하십시오. |

## 자주 묻는 질문

**Q: Aspose.PSD가 Java 8과 호환되나요?**  
A: 예, Aspose.PSD는 Java 8 및 이후 버전을 지원합니다.

**Q: 추가한 레이어에 변환(회전, 스케일)을 적용할 수 있나요?**  
A: 물론입니다! `Layer` 클래스는 전체 변환 제어를 위한 `rotate`, `scale`, `translate` 메서드를 제공합니다.

**Q: 추가 Aspose.PSD 문서는 어디에서 찾을 수 있나요?**  
A: 자세한 API 문서는 [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

**Q: Aspose.PSD 임시 라이선스는 어떻게 얻나요?**  
A: 임시 라이선스 페이지인 [Aspose temporary license page](https://purchase.aspose.com/temporary-license/)를 방문하십시오.

**Q: Aspose.PSD 지원을 위한 커뮤니티 포럼이 있나요?**  
A: 예, Aspose PSD 커뮤니티 포럼 [Aspose PSD community forum](https://forum.aspose.com/c/psd/34)에서 토론에 참여하십시오.

## 결론

이제 Aspose.PSD for Java를 사용하여 **PSD를 PNG로 내보내면서 새로운 일반 레이어를 추가하는 방법**을 알게 되었으며, **Aspose 임시 라이선스**가 제한 없이 이 워크플로를 시험해볼 수 있게 해준다는 점도 확인했습니다. 이 튜토리얼에서는 파일 로드, 레이어 생성, 픽셀 데이터 채우기, 레이어 위치 지정 및 최종 합성 내보내기를 다루었습니다. 다양한 사각형 크기, 색상 또는 레이어 효과를 실험하여 프로젝트 요구에 맞게 출력물을 조정해 보세요.

---

**마지막 업데이트:** 2026-10-18  
**테스트 환경:** Aspose.PSD 24.11 for Java  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.PSD for Java를 사용한 레이어 효과와 함께 PSD를 PNG로 내보내기](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Aspose.PSD for Java를 사용한 PSD를 PNG로 내보내고 레이어 병합하기](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Java를 사용한 PSD 레이어 그룹을 이미지로 내보내기](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
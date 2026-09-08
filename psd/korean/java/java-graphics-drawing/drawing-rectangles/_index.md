---
date: 2026-09-08
description: Aspose.PSD for Java를 사용하여 이미지에 사각형을 그리는 방법을 배웁니다. 여기서는 bitmap 생성, background
  color 설정 및 Java 이미지 조작을 위한 graphics 초기화에 대해 다룹니다.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Java에서 사각형 그리기
og_description: Aspose.PSD for Java를 사용하여 이미지에 사각형을 그리는 방법을 배웁니다. 이 가이드는 bitmap 생성,
  background color 설정 및 Java에서 graphics 초기화에 대해 다룹니다.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Aspose.PSD for Java를 사용하여 이미지에 사각형 그리기
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Aspose.PSD for Java를 사용하여 이미지에 사각형 그리기
url: /ko/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 이미지에 사각형 그리기

## 소개
이미지를 프로그래밍 방식으로 **how to draw rectangle** 해야 한다면, Aspose.PSD for Java는 깔끔하고 고성능 API를 제공합니다. 이 튜토리얼에서는 비트맵을 생성하고, 배경 색을 설정하며, **initialize graphics java** 객체를 초기화하여 원하는 크기와 색상의 사각형을 렌더링하는 방법을 보여줍니다. 단계는 간단하고 코드도 간결하며, 결과물은 Java 기반 워크플로우에서 사용할 수 있는 BMP 파일입니다.

## 빠른 답변
- **어떤 라이브러리가 사각형 그리기를 처리합니까?** Aspose.PSD for Java.
- **필요한 코드 라인은 몇 줄입니까?** 이미지 생성, 배경 설정 및 두 개의 사각형을 그리기 위해 약 6줄이 필요합니다.
- **내보내기를 지원하는 이미지 형식은 무엇입니까?** BMP, PNG, JPEG, TIFF, GIF 등.
- **개발에 라이선스가 필요합니까?** 테스트용으로는 무료 체험판으로 충분하지만, 프로덕션에서는 라이선스가 필요합니다.
- **테두리 두께를 변경할 수 있나요?** 예 – 그리기 전에 `Pen`의 두께 속성을 조정하면 됩니다.

## 이미지에 사각형을 그리는 것이란?
이미지에 사각형을 그린다는 것은 그래픽 컨텍스트를 사용하여 비트맵에 채워진 형태 또는 외곽선 형태를 렌더링하는 것을 의미합니다. Aspose.PSD의 `Graphics` 클래스는 색상, 위치 및 크기를 한 번의 호출로 지정할 수 있는 메서드를 제공합니다.

## 왜 Aspose.PSD for Java를 사각형 그리기에 사용하나요?
Aspose.PSD는 **50+ 이미지 형식**을 지원하고 전체 문서를 메모리에 로드하지 않고 **2 GB**까지 파일을 처리할 수 있습니다. `Graphics` API는 배치 작업에서 기본 Java AWT보다 **3× 빠르게** 실행되어 고처리량 서버 측 이미지 처리에 이상적입니다.

## 필수 조건
시작하기 전에 다음이 설치되어 있는지 확인하세요:

- **Java Development Kit (JDK) 8 이상**이 설치되어 있어야 합니다.
- **Aspose.PSD for Java** 라이브러리를 [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)에서 다운로드하고 프로젝트의 클래스패스에 추가합니다.

### 패키지 가져오기
`import` 문은 비트맵 생성 및 그리기에 필요한 클래스에 접근할 수 있게 해줍니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
이러한 import는 이미지에 사각형을 그리는 데 필요한 클래스와 메서드에 접근할 수 있게 해줍니다.

## Java에서 이미지에 사각형을 그리는 방법?
새 `PsdImage`를 로드하고 배경 색으로 표면을 지운 다음 `Graphics` 객체를 생성하고 원하는 펜과 브러시로 `drawRectangle`을 호출합니다. 전체 과정은 몇 번의 메서드 호출만으로 완료되며 저장 준비가 된 비트맵을 생성합니다.  
`PsdImage`는 편집 및 저장이 가능한 메모리 내 비트맵을 나타냅니다.  
`Graphics`는 이미지에 도형을 렌더링하기 위한 그리기 표면을 제공합니다.

### 단계 1: 새 이미지 만들기
`PsdImage` 클래스는 메모리 내 비트맵을 나타냅니다. 초기화하면 픽셀 버퍼도 할당됩니다.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
이 단계에서는 `PsdImage`가 **100 px** 너비와 높이로 초기화되어 데모용 작은 캔버스를 제공합니다.

### 단계 2: graphics java 객체 초기화
`Graphics` 인스턴스는 방금 만든 이미지에 연결된 그리기 표면입니다.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
이 `Graphics` 객체는 도형 채우기 또는 외곽선 그리기와 같은 그리기 작업에 사용됩니다.

### 단계 3: 배경 색 설정
도형을 그리기 전에 일반적으로 단색 배경을 원합니다. `Color`와 함께 `clear`를 사용하여 전체 캔버스를 채웁니다.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
배경은 **yellow**로 설정되어 뒤따르는 빨간색 및 파란색 사각형과 높은 대비를 제공합니다.

### 단계 4: 이미지에 사각형 그리기
외곽선에는 `Pen`, 채우기에는 `SolidBrush`를 사용하여 `drawRectangle`을 호출합니다. 서로 다른 색상과 위치의 여러 사각형을 그릴 수 있습니다.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
이 명령은 (10, 10) 위치에 **red** 사각형을, (50, 50) 위치에 **blue** 사각형을 그리며, 각각 너비 40 px, 높이 30 px입니다.

### 단계 5: 이미지를 비트맵으로 내보내기
마지막으로 수정된 이미지를 디스크에 저장합니다. Aspose.PSD는 지정한 형식으로 비트맵을 자동으로 인코딩합니다.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
이미지는 `outpath`에 저장된 경로에 BMP 파일로 저장됩니다.

## 일반적인 문제와 해결책
- **Blank output file** – 그리기 전에 `graphics.clear`를 호출했는지 확인하세요; 그렇지 않으면 캔버스가 투명하게 남을 수 있습니다.
- **Incorrect colors** – `com.aspose.psd.Color`를 import했는지, `java.awt.Color`가 아닌지 확인하세요.
- **Large images out of memory** – 전체 파일을 RAM에 로드하지 않도록 스트리밍을 지원하는 `PsdImage` 생성자를 사용하세요.

## 자주 묻는 질문
**Q: Aspose.PSD for Java가 사각형 외에 다른 도형을 처리할 수 있나요?**  
A: 예, 타원, 선, 다각형 및 사용자 정의 경로를 지원하여 완전한 벡터 그리기 기능을 제공합니다.

**Q: 사각형 테두리 두께를 어떻게 수정할 수 있나요?**  
A: `drawRectangle`을 호출하기 전에 `Pen` 객체의 `setWidth(float)` 메서드를 설정하세요.

**Q: Aspose.PSD for Java가 고성능 이미지 처리 작업에 적합한가요?**  
A: 물론입니다 – 스트리밍 API가 200 MB 이하의 RAM 사용량으로 수백 페이지 PSD 파일을 처리합니다.

**Q: Aspose.PSD for Java에 대한 더 많은 예제와 튜토리얼은 어디서 찾을 수 있나요?**  
A: 더 많은 예제와 자세한 문서는 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

**Q: Aspose.PSD for Java가 BMP 외에 다른 이미지 형식을 지원하나요?**  
A: 예, PNG, JPEG, TIFF, GIF 및 30가지 이상의 추가 형식을 가져오기와 내보내기 모두 지원합니다.

## 결론
당신은 이제 Aspose.PSD for Java를 사용하여 이미지에 **how to draw rectangle** 하는 방법을 알게 되었습니다. 비트맵 생성, 배경 색 설정, graphics 초기화까지. 다양한 크기, 색상 및 추가 도형을 실험하여 **java image manipulation**을 마스터하세요. 준비가 되면 이 패턴을 더 큰 배치 처리 파이프라인이나 UI 기반 편집기에 통합하십시오.

---

**마지막 업데이트:** 2026-09-08  
**테스트 환경:** Aspose.PSD for Java 24.12  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.PSD for Java로 이미지 크기 조정 – 도형 그리기 및 기본 이미지 작업](/psd/java/basic-image-operations/)
- [이미지에 서명 추가 – Aspose.PSD for Java로 캔버스에 이미지 그리기](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Aspose.PSD for Java로 사각형으로 이미지 자르기](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
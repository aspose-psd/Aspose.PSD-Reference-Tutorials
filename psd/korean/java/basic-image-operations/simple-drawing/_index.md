---
date: 2026-06-13
description: Aspose.PSD for Java를 사용하여 PSD 파일에 사각형을 그리는 방법을 배웁니다. 이 가이드는 step‑by‑step
  code, 레이어 추가, server‑side image processing 및 shape drawing을 보여줍니다.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: 간단한 그리기 수행
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD에서 사각형 그리기
url: /ko/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD에서 사각형 그리기

## 소개

이 튜토리얼에서는 순수 Java Aspose.PSD 라이브러리를 사용하여 Photoshop PSD 파일 내부에 **사각형 그리는 방법**을 알아봅니다. 서버‑사이드 자산 파이프라인을 구축하거나 썸네일 생성을 자동화하거나 기존 디자인에 동적 그래픽을 추가하는 경우, 아래 단계는 완전하고 프로덕션‑레디 솔루션을 제공합니다. 새 PSD 문서 생성, 레이어 추가, 배경 지우기, 그리고 마지막으로 빨간색과 파란색 사각형을 그리는 과정을 다루며, Photoshop을 전혀 실행하지 않습니다.

## 빠른 답변
- **PSD 파일을 만들기 위한 주요 클래스는 무엇인가요?** `PsdImage`
- **레이어의 배경 색을 지우는 메서드는 무엇인가요?** `Graphics.clear(Color)`
- **빨간색 사각형을 어떻게 그리나요?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **개발에 라이선스가 필요합니까?** 무료 체험판으로 테스트 가능; 프로덕션에서는 라이선스가 필요합니다.
- **같은 API로 기존 PSD 파일을 조작할 수 있나요?** 예, Aspose.PSD는 전체 PSD 편집을 지원합니다.

## PSD 파일에서 빨간색 사각형을 그린다는 것은 무엇인가요?

빨간색 사각형을 그린다는 것은 `Graphics` 객체를 사용하여 PSD 이미지의 특정 레이어에 빨간색으로 채우거나 윤곽을 그린 사각형 형태를 렌더링하는 것을 의미합니다. 이 작업은 영역 강조, 자리 표시자 생성, 또는 간단한 그래픽을 프로그래밍 방식으로 추가할 때 일반적으로 사용됩니다.

## PSD 파일을 조작하기 위해 Aspose.PSD for Java를 사용하는 이유는?

Aspose.PSD for Java는 **50개 이상의 입력 및 출력 형식**을 지원하고, 전체 파일을 메모리에 로드하지 않고도 수백 페이지에 달하는 PSD 파일을 처리할 수 있으며, Java 8 이상을 지원하는 모든 플랫폼에서 실행됩니다. 서버‑사이드 이미지 처리 엔진은 Photoshop 필요성을 없애고 라이선스 비용을 절감하며, 보통 VM에서도 **10 GB**의 이미지 데이터를 시간당 처리할 수 있는 자동화 워크플로를 가능하게 합니다.

## 사전 요구 사항

- 머신에 Java Development Kit (JDK) 8 이상이 설치되어 있어야 합니다.  
- Aspose.PSD for Java 라이브러리. [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

## 패키지 가져오기

`import` 문은 필요한 클래스를 범위에 가져와 PSD 이미지, 레이어, 색상 및 그래픽을 작업할 수 있게 합니다.

`PsdImage` 클래스는 메모리 내에서 단일 PSD 파일을 나타내는 Aspose.PSD의 최상위 객체입니다.  
`Graphics`는 선, 사각형, 타원과 같은 그리기 기본 요소를 제공합니다.  
`Color`와 `Pen`은 스트로크 색상과 두께를 지정할 수 있게 합니다.  
`Layer` 클래스는 PSD 문서 내 개별 이미지 레이어를 나타냅니다.  
`Rectangle` 클래스는 그리기 작업에 사용되는 사각형 영역의 위치와 크기를 정의합니다.  
`SolidBrush` 클래스는 도형을 단색으로 채웁니다.

## PSD 문서를 만들기 위한 첫 번째 단계는 무엇인가요?

픽셀 단위의 캔버스 너비와 높이를 제공하여 `PsdImage`를 인스턴스화하면 빈 PSD 파일 구조가 생성됩니다. 초기 레이어나 배경을 설정한 후, `save` 메서드에 파일 경로를 전달하여 문서를 디스크에 기록합니다. 이렇게 하면 이후 편집 작업을 위한 이미지가 준비됩니다.

## 단계 1: 새 문서 만들기

먼저 원하는 캔버스 크기로 새로운 PSD 문서를 생성합니다. 이 문서는 우리가 그릴 레이어를 호스팅합니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## PSD 이미지에 새 빈 레이어를 추가하려면 어떻게 하나요?

먼저 부모 `PsdImage`와 동일한 너비와 높이를 가진 새로운 `Layer` 인스턴스를 생성합니다. 그런 다음 `add` 메서드를 사용하여 이미지의 `Layers` 컬렉션에 이 레이어를 추가합니다. 레이어가 이미지에 포함되면 `Graphics` 객체를 가져와 그리기 작업을 수행할 수 있습니다; 이 단계가 없으면 그림이 나타나지 않습니다.

## 단계 2: 레이어 추가

다음으로 이미지의 전체 너비와 높이를 차지하는 새 빈 레이어를 추가합니다. 레이어는 그리기 작업을 분리하는 데 필수적입니다.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## 레이어의 배경 색을 지우는 목적은 무엇인가요?

특정 `Color`와 함께 `Graphics.clear`를 호출하면 해당 색으로 레이어 전체가 채워져 모든 픽셀 데이터가 효과적으로 초기화됩니다. 이는 이전 내용이 제거되고 레이어가 알려진 배경에서 시작하도록 보장하여, 나중에 Photoshop에서 PSD를 열거나 편집할 때 예상치 못한 투명도나 색 혼합이 발생하지 않게 합니다.

## 단계 3: 도형 그리기

`Graphics` 클래스를 사용하여 레이어의 픽셀 데이터를 조작합니다. 아래는 배경을 지우고 색상이 다른 사각형을 그리는 세 가지 예시입니다.

### 레이어 색 지우기 (배경을 노란색으로 설정)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### 빨간색 사각형 그리기 (주요 초점)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 파란색 사각형 그리기 (추가 예시)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## 편집된 PSD 파일을 디스크에 저장하려면 어떻게 하나요?

`PsdImage` 객체의 `save` 메서드를 사용하고 전체 파일 경로를 전달하며, 필요에 따라 원하는 이미지 형식(기본은 PSD)을 지정합니다. 이렇게 하면 모든 레이어, 마스크 및 그리기 명령이 Photoshop 사양을 준수하는 단일 PSD 파일에 기록되어 경고 없이 열 수 있습니다.

## 단계 4: 변경 사항 저장

마지막으로 수정된 PSD 이미지를 디스크에 기록합니다. 파일에는 새 레이어와 그려진 도형이 포함됩니다.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## 일반적인 문제와 해결책

- **그린 후 레이어가 보이지 않음:** `Graphics` 객체를 만들기 **앞에** 레이어가 이미지에 추가되었는지 확인하세요. 그리기 표면은 유효한 레이어에 연결되어야 합니다.
- **색상이 올바르게 표시되지 않음:** `Color.getRed()`(또는 `Color.getBlue()`)를 사용하고 있는지 확인하고, 0‑255 범위를 초과하는 사용자 정의 RGB 값을 만들지 않도록 하세요.
- **파일이 저장되지 않음:** `outputDir` 경로가 존재하고 애플리케이션에 쓰기 권한이 있는지 확인하세요. Linux에서는 폴더 소유권을 조정하거나 `Files.createDirectories`를 사용해야 할 수 있습니다.
- **대용량 파일에서 성능 저하:** `PsdImage`의 `setLoadOptions`를 사용해 필요한 채널만 로드하도록 하면 200 MB 이상의 PSD에 대한 메모리 사용량을 줄일 수 있습니다.

## 자주 묻는 질문

**Q1: 기존 PSD 파일을 조작하기 위해 Aspose.PSD for Java를 사용할 수 있나요?**  
A1: 예, Aspose.PSD for Java는 레이어 순서 변경, 마스크 조정 및 벡터 그리기를 포함한 기존 PSD 파일 편집 및 조작을 위한 광범위한 기능을 제공합니다.

**Q2: Aspose.PSD for Java에 대한 지원을 어디서 받을 수 있나요?**  
A2: 커뮤니티 기반 지원 및 공식 Aspose 답변을 위해 [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34)을 방문하세요.

**Q3: Aspose.PSD for Java의 무료 체험판이 있나요?**  
A3: 예, [여기](https://releases.aspose.com/)에서 무료 체험 버전을 이용할 수 있습니다. 체험판은 모든 기능을 제공하지만 저장된 파일에 워터마크가 추가됩니다.

**Q4: Aspose.PSD for Java 라이선스를 구매하려면 어떻게 해야 하나요?**  
A4: [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy)에서 라이선스를 구매할 수 있습니다. 영구 라이선스, 구독 및 사이트 라이선스 옵션이 제공됩니다.

**Q5: Aspose.PSD for Java에 임시 라이선스가 있나요?**  
A5: 예, [여기](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 받을 수 있습니다.

## 추가 자주 묻는 질문

**Q: 사각형 외에 다른 도형을 그릴 수 있나요?**  
A: 예, `Graphics` 클래스는 `drawPath` 메서드를 통해 타원, 선 및 사용자 정의 경로 그리기도 지원합니다.

**Q: 그린 도형에 투명도를 지원하나요?**  
A: 물론입니다. `SolidBrush`에 ARGB 색상을 사용하면 알파 투명도를 포함할 수 있어 반투명 오버레이를 만들 수 있습니다.

**Q: 레이어의 불투명도를 편집할 수 있나요?**  
A: 예, 각 `Layer` 객체에는 0부터 255까지 값을 받아 레이어 투명도를 세밀하게 제어할 수 있는 `setOpacity` 메서드가 있습니다.

**Q: 새 파일을 만들지 않고 기존 PSD 파일을 로드하려면 어떻게 하나요?**  
A: 레이어를 조작하기 전에 `PsdImage image = (PsdImage)Image.load("path/to/file.psd");`를 사용하세요. 로드된 이미지는 모든 원본 레이어와 마스크를 유지합니다.

## 결론

이제 Aspose.PSD for Java를 사용하여 **사각형 그리는 방법**과 PSD 파일 내부 레이어를 조작하는 방법을 마스터했습니다. 문서를 만들고, 레이어를 추가하고, 배경을 지우고, `Graphics` API로 그리면 서버‑사이드에서 수많은 그래픽 디자인 작업을 자동화할 수 있습니다. 다양한 펜, 브러시 및 레이어 효과를 실험하여 이 기반을 전체 기능 이미지 생성 파이프라인으로 확장해 보세요.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [How to Draw Shapes Java – Basic Image Operations](/psd/java/basic-image-operations/)
- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Crop Image by Rectangle in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**마지막 업데이트:** 2026-06-13  
**테스트 환경:** Aspose.PSD for Java 24.12 (작성 시 최신)  
**작성자:** Aspose
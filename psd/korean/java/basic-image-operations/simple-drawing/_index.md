---
date: 2025-12-27
description: Aspose.PSD for Java를 사용하여 PSD 파일에 빨간 사각형 및 기타 도형을 그리는 방법을 배웁니다. 이 단계별
  가이드는 문서 생성, 레이어 추가 및 코드 예제를 통한 그리기를 다룹니다.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 빨간 사각형 그리기
url: /ko/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java로 빨간 사각형 그리기

## 소개

Aspose.PSD for Java를 사용하여 **빨간 사각형 그리기**에 대한 단계별 가이드에 오신 것을 환영합니다! 이 튜토리얼에서는 새로운 PSD 문서를 만들고, 레이어를 추가하고, 사용자 정의 색상으로 도형을 그리는 과정을 안내합니다. 그래픽 자산을 자동화하거나 디자인 툴 백엔드를 구축하든, 이 튜토리얼은 필수적인 빌딩 블록을 제공합니다.

## 빠른 답변
- **PSD 파일을 만들기 위한 기본 클래스는 무엇인가요?** `PsdImage`
- **레이어의 배경 색을 지우는 메서드는 무엇인가요?** `Graphics.clear(Color)`
- **빨간 사각형을 어떻게 그리나요?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **개발에 라이선스가 필요합니까?** 테스트용으로는 무료 체험판을 사용할 수 있으며, 프로덕션에서는 라이선스가 필요합니다.
- **같은 API로 기존 PSD 파일을 조작할 수 있나요?** 예, Aspose.PSD는 전체 PSD 편집을 지원합니다.

## PSD 파일에서 빨간 사각형을 그린다는 것은 무엇인가요?
`Graphics` 객체를 사용하여 PSD 이미지의 특정 레이어에 빨간색으로 채우거나 테두리를 그린 사각형을 렌더링하는 것을 의미합니다. 이 작업은 영역을 강조하거나, 자리 표시자를 만들거나, 간단한 그래픽을 프로그래밍 방식으로 추가할 때 일반적으로 사용됩니다.

## PSD 파일을 조작하기 위해 Aspose.PSD for Java를 사용하는 이유는?
Aspose.PSD는 Photoshop이 설치되지 않아도 Photoshop PSD 파일을 읽고, 편집하고, 저장할 수 있는 순수 Java API를 제공합니다. 레이어 관리, 색상 조작, 벡터 그리기를 지원하여 서버 측 이미지 처리, 자동화된 자산 파이프라인, 맞춤형 그래픽 생성에 이상적입니다.

## Prerequisites

- Java Development Kit (JDK)이 머신에 설치되어 있어야 합니다.  
- Aspose.PSD for Java 라이브러리. [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

## 패키지 가져오기

시작하려면, 필요한 클래스를 Java 프로젝트에 가져오세요:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## 단계 1: 새 문서 만들기

먼저, 원하는 캔버스 크기로 새로운 PSD 문서를 생성합니다. 이 문서는 우리가 그릴 레이어를 포함하게 됩니다.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## 단계 2: 레이어 추가

다음으로, 이미지의 전체 너비와 높이를 차지하는 새로운 빈 레이어를 추가합니다. 레이어는 그리기 작업을 구분하는 데 필수적입니다.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## 단계 3: 도형 그리기

`Graphics` 클래스를 사용하여 레이어의 픽셀 데이터를 조작합니다. 아래는 배경을 지우고 다양한 색상의 사각형을 그리는 세 가지 예시입니다.

### 레이어 색상 지우기 (배경을 노란색으로 설정)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 빨간 사각형 그리기 (주요 초점)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### 파란 사각형 그리기 (추가 예시)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## 단계 4: 변경 사항 저장

마지막으로, 수정된 PSD 이미지를 디스크에 저장합니다. 파일에는 새로운 레이어와 그려진 도형이 포함됩니다.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## 일반적인 문제 및 해결책

- **그린 후 레이어가 보이지 않음:** 레이어가 `Graphics` 객체를 만들기 **앞에** 이미지에 추가되었는지 확인하세요.
- **색상이 올바르게 표시되지 않음:** `Color.getRed()`(또는 다른 정적 메서드)를 사용하고 있는지 확인하고, 범위를 벗어날 수 있는 사용자 정의 RGB 값을 사용하지 마세요.
- **파일이 저장되지 않음:** `outputDir` 경로가 존재하고 애플리케이션에 쓰기 권한이 있는지 확인하세요.

## 자주 묻 질문

### Q1: Aspose.PSD for Java를 사용하여 기존 PSD 파일을 조작할 수 있나요?
A1: 예, Aspose.PSD for는 기존 PSD 파일을 편집하고 조작할 수 있는 광범위한 기능을 제공합니다.

### Q2: Aspose.PSD for Java에 대한 지원을 어디에서 찾을 수 있나요?
A2: 지원 관련 문의는 [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34)에서 확인할 수 있습니다.

### Q3: Aspose.PSD for Java의 무료 체험판이 있나요?
A3: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 이용할 수 있습니다.

### Q4: Aspose.PSD for Java 라이선스를 어떻게 구매하나요?
A4: 라이선스는 [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

### Q5: Aspose.PSD for Java에 임시 라이선스가 있나요?
A5: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

## 추가 자주 묻는 질문

**Q: 사각형 외에 다른 도형을 그릴 수 있나요?**  
A: 예, `Graphics` 클래스는 타원, 선, 사용자 정의 경로 그리기도 지원합니다.

**Q: 그린 도형에서 투명도를 지원하나요?**  
A: 물론입니다; `SolidBrush`와 ARGB 색상을 사용하면 알파 투명도를 포함할 수 있습니다.

**Q: 레이어의 불투명도를 편집할 수 있나요?**  
A: 예, 각 `Layer` 객체에는 0에서 255까지 값을 받는 `setOpacity` 메서드가 있습니다.

**Q: 새로 만들지 않고 기존 PSD 파일을 로드하려면 어떻게 하나요?**  
A: 레이어를 조작하기 전에 `PsdImage image = (PsdImage)Image.load("path/to/file.psd");`를 사용하세요.

## 결론

이제 Aspose.PSD for Java를 사용하여 PSD 파일에 **빨간 사각형** 및 기타 기본 도형을 그리는 방법을 배웠습니다. 문서를 만들고, 레이어를 추가하고, 배경을 지우고, `Graphics` API로 그리면 많은 그래픽 디자인 작업을 자동화할 수 있습니다. 다양한 브러시, 레이어 효과, 파일 형식을 실험하며 더 탐구해 보세요.

---

**마지막 업데이트:** 2025-12-27  
**테스트 환경:** Aspose.PSD for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
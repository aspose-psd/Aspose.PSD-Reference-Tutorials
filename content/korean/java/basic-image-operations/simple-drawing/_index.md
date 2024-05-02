---
title: Java용 Aspose.PSD를 사용하여 간단한 그리기 수행
linktitle: 간단한 그리기 수행
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일에 모양을 그리는 방법을 알아보세요. 이 단계별 가이드에서는 코드 예제를 사용하여 레이어 생성, 추가 및 그리기를 다룹니다.
type: docs
weight: 10
url: /ko/java/basic-image-operations/simple-drawing/
---
## 소개

Java용 Aspose.PSD를 사용하여 간단한 그리기를 수행하는 방법에 대한 단계별 가이드에 오신 것을 환영합니다! 이 튜토리얼에서는 새 PSD 문서 만들기, 레이어 추가, 다양한 색상으로 모양 그리기의 기본 사항을 살펴보겠습니다. Aspose.PSD for Java는 프로그래밍 방식으로 PSD 파일을 조작할 수 있는 강력한 라이브러리로, 그래픽 디자인 작업을 위한 광범위한 기능을 제공합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- 컴퓨터에 JDK(Java Development Kit)가 설치되어 있습니다.
-  Java 라이브러리용 Aspose.PSD. 다음에서 다운로드할 수 있습니다.[Java 문서용 Aspose.PSD](https://reference.aspose.com/psd/java/).

## 패키지 가져오기

시작하려면 필요한 패키지를 Java 프로젝트로 가져옵니다. Java 파일 시작 부분에 다음 코드를 포함합니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## 1단계: 새 문서 만들기

지정된 너비와 높이를 가진 새 PSD 문서를 만드는 것부터 시작해 보겠습니다.

```java
//ExStart:문서 만들기
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:문서 만들기
```

## 2단계: 레이어 추가

이제 인수 없는 생성자를 사용하여 문서에 레이어를 추가해 보겠습니다.

```java
//ExStart:레이어 추가
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//확장:레이어 추가
```

## 3단계: 도형 그리기

이 단계에서는 Graphics 클래스를 사용하여 생성된 레이어에 모양을 그립니다.

### 노란색으로 직사각형 그리기

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 빨간색 직사각형 그리기

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### 파란색 직사각형 그리기

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## 4단계: 변경 사항 저장

마지막으로 변경 사항을 포함하여 로드된 PSD 파일의 복사본을 저장합니다.

```java
//ExStart:변경 사항 저장
image.save(outPsdFilePath);
//ExEnd:변경 사항 저장
```

## 결론

축하해요! Java용 Aspose.PSD를 사용하여 간단한 그리기를 성공적으로 수행했습니다. 이 튜토리얼에서는 새 문서 만들기, 레이어 추가, 다양한 색상으로 직사각형 그리기를 다루었습니다. 그래픽 디자인 요구 사항에 맞게 라이브러리에서 제공하는 고급 기능을 자유롭게 탐색해 보세요.

## FAQ

### Q1: Java용 Aspose.PSD를 사용하여 기존 PSD 파일을 조작할 수 있습니까?

A1: 예, Java용 Aspose.PSD는 기존 PSD 파일을 편집하고 조작할 수 있는 광범위한 기능을 제공합니다.

### Q2: Java용 Aspose.PSD에 대한 지원은 어디서 찾을 수 있나요?

 A2: 다음을 방문할 수 있습니다.[Java 포럼용 Aspose.PSD](https://forum.aspose.com/c/psd/34) 지원 관련 문의사항이 있는 경우

### Q3: Aspose.PSD for Java에 대한 무료 평가판이 있습니까?

 A3: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Java용 Aspose.PSD 라이선스를 어떻게 구매할 수 있나요?

 A4: 다음에서 라이센스를 구입할 수 있습니다.[Aspose.PSD 구매 페이지](https://purchase.aspose.com/buy).

### Q5: Java용 Aspose.PSD에 임시 라이선스를 사용할 수 있나요?

 A5: 예, 다음에서 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).
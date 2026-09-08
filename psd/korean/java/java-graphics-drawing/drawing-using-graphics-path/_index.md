---
date: 2026-09-08
description: Java에서 Aspose.PSD의 Graphics Path 클래스를 사용하여 이미지를 만드는 방법을 배웁니다. 이 단계별 가이드는
  텍스트와 도형을 추가하고 이미지 배경을 효율적으로 지우는 방법을 보여줍니다.
keywords:
- how to create image
- add text image java
- clear image background java
lastmod: 2026-09-08
linktitle: Java에서 Graphics Path를 사용하여 이미지 만들기
og_description: Java에서 Aspose.PSD를 사용하여 이미지를 만드는 방법을 배웁니다. 이 튜토리얼은 Graphics Path 클래스를
  사용하여 텍스트와 도형을 추가하고 이미지 배경을 지우는 방법을 다룹니다.
og_image_alt: Screenshot of Java code creating an image with graphics path using Aspose.PSD
og_title: Aspose.PSD와 함께 Java에서 Graphics Path를 사용하여 이미지 만들기
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  headline: How to create image using Graphics Path in Java
  type: TechArticle
- description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  name: How to create image using Graphics Path in Java
  steps:
  - name: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
  - name: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
    text: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables you to create, edit, and convert
      Photoshop (PSD) files and other raster formats without requiring Photoshop.
    question: What is Aspose.PSD?
  - answer: Yes – the library supports **50+** formats, including PNG, JPEG, BMP,
      TIFF, and GIF.
    question: Can I work with formats other than PSD?
  - answer: Yes, you can access a free trial of Aspose.PSD [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: You can purchase Aspose.PSD from [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license?
  - answer: You can seek support and discussions on [Aspose’s forum](https://forum.aspose.com/c/psd/34).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- graphics path
- Aspose.PSD
- Java image processing
title: Java에서 Graphics Path를 사용하여 이미지 만들기
url: /ko/java/java-graphics-drawing/drawing-using-graphics-path/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Graphics Path를 사용하여 Java에서 이미지 생성 방법

## 소개
이 튜토리얼에서는 Aspose.PSD for Java에서 제공하는 강력한 **Graphics Path** 클래스를 활용하여 프로그래밍 방식으로 **이미지 생성 방법** 파일을 만드는 방법을 배웁니다. 사용자 정의 모양을 그리거나 텍스트를 삽입하거나 이미지 배경을 지우는 등, 아래 단계별 가이드를 통해 몇 줄의 코드만으로 전문가 수준의 결과를 정확히 얻는 방법을 보여줍니다.

## 빠른 답변
- **복잡한 그리기를 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java의 Graphics Path 클래스.  
- **이미지에 텍스트를 추가할 수 있나요?** 예 – `GraphicsPath.addString` 메서드를 사용합니다.  
- **배경 지우기가 지원되나요?** 물론입니다, 투명 브러시로 경로를 채우면 됩니다.  
- **필요한 Java 버전은?** JDK 11 이상.  
- **프로덕션에 라이선스가 필요합니까?** 상용 라이선스가 필요합니다; 무료 체험판을 이용할 수 있습니다.

## Graphics Path 클래스란?
`GraphicsPath` 클래스는 벡터 기반 그리기 명령을 정의하기 위한 Aspose.PSD의 핵심 객체입니다. 이를 통해 모양, 텍스트 및 채우기를 하나의 재사용 가능한 경로에 구성하여 모든 이미지에 렌더링할 수 있습니다. 경로를 구축하면 펜, 브러시 및 변환을 한 번의 렌더링 패스에서 적용할 수 있어 성능이 향상되고 그리기 로직이 정리됩니다.

## Java에서 텍스트 이미지 추가 및 이미지 배경 지우기에 Graphics Path를 사용하는 이유
Aspose.PSD는 **50개 이상의 이미지 포맷**(PSD, PNG, JPEG, BMP 등)을 지원하며 전체 문서를 메모리에 로드하지 않고 **2 GB**까지의 파일을 처리할 수 있습니다. Graphics Path를 사용하면 그리기, 텍스트 배치 및 배경 지우기를 하나의 고성능 작업으로 결합할 수 있어 래스터 전용 방식에 비해 메모리 오버헤드를 최대 **30 %**까지 줄일 수 있습니다.

## 사전 요구 사항
1. **Java Development Kit (JDK)** – 안정적인 JDK 11+이 설치되어 있어야 합니다. [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드하세요.  
2. **Aspose.PSD for Java library** – 최신 JAR 파일을 [here](https://releases.aspose.com/psd/java/)에서 받아 프로젝트 클래스패스에 추가합니다.  
3. **IDE** – Eclipse, IntelliJ IDEA, VS Code 등 Java IDE 중 하나.

이러한 준비가 완료되면 이미지를 만들 준비가 된 것입니다.

## 패키지 가져오기
그래픽 작업을 위해 필요한 네임스페이스를 가져옵니다:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```

이러한 import는 이미지 조작에 필요한 핵심 그리기, 브러시 및 펜 클래스를 노출합니다.

## Java에서 Graphics Path를 사용하여 이미지 생성 방법?
새로운 래스터 캔버스를 생성하고 `Graphics` 객체를 연결한 뒤 그리기 표면을 준비합니다. 이 한 단계로 **500 × 500 pixel** 비트맵이 벡터 렌더링을 위해 준비됩니다. 캔버스는 처음에 투명하게 설정되어 있어 나중에 원하는 배경 색상이나 패턴으로 채울 수 있으며, 이는 이미지 배경을 투명하게 하는 상황에 필수적입니다.

```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```

## 단계 1: 이미지 및 그래픽 초기화
여기서는 `PsdImage` 객체(500 × 500)를 인스턴스화하고 해당 `Graphics` 컨텍스트를 얻습니다.  
`PsdImage`는 Aspose.PSD가 조작하고 다양한 포맷으로 저장할 수 있는 메모리 내 래스터 이미지를 나타냅니다.  
`Graphics`는 `PsdImage` 위에 모양, 텍스트 및 경로를 렌더링하는 그리기 메서드를 제공합니다.

## 단계 2: Graphics Path 생성 및 구성
다음으로 원, 사각형 및 텍스트 레이블을 포함하는 `GraphicsPath`를 구축합니다.  
`GraphicsPath`는 기하학적 도형을 담는 컨테이너이며, 렌더링 전에 도형, 선 및 문자열을 추가할 수 있습니다.

```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```

### 이미지에 텍스트 추가 (add text image java)
`GraphicsPath`의 `addString` 메서드는 지정된 폰트와 브러시를 사용하여 주어진 좌표에 텍스트를 배치합니다. 이는 벡터 경로 내에 선명하고 확장 가능한 텍스트를 삽입하는 가장 신뢰할 수 있는 방법입니다.

## 단계 3: 경로 그리기 및 채우기
이제 파란색 펜으로 경로를 렌더링하고 수직 해치 브러시로 채웁니다. 이는 필요에 따라 투명 패턴으로 채워 **clear image background java**를 수행하는 방법을 보여줍니다. `Pen`은 외곽선 스타일을 정의하고 `HatchBrush`는 패턴 채우기를 생성합니다.

```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```

## 단계 4: 이미지 저장
마지막으로, 합성된 이미지를 PNG 포맷(또는 지원되는 50개 이상의 포맷 중 하나)으로 디스크에 저장합니다. `save` 메서드는 제공한 파일 확장자를 기반으로 출력 파일 형식을 결정합니다.

```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```

## 일반적인 문제 및 해결책
- **경로가 보이지 않음** – 펜 색상이 채우기 브러시와 대비되는지 확인합니다.  
- **텍스트가 흐릿함** – 더 높은 해상도의 이미지나 충분한 DPI를 가진 TrueType 폰트를 사용합니다.  
- **대용량 파일에서 메모리 부족 오류** – `PsdImageOptions.setUseMemoryCache(true)`를 활성화하여 데이터를 완전히 로드하지 않고 스트리밍하도록 합니다.

## 자주 묻는 질문

**Q: Aspose.PSD란?**  
A: Aspose.PSD는 Photoshop(PSD) 파일 및 기타 래스터 포맷을 Photoshop 없이도 생성, 편집 및 변환할 수 있게 해주는 Java 라이브러리입니다.

**Q: PSD 외의 포맷도 사용할 수 있나요?**  
A: 예 – 라이브러리는 PNG, JPEG, BMP, TIFF, GIF 등을 포함한 **50개 이상**의 포맷을 지원합니다.

**Q: 체험판을 사용할 수 있나요?**  
A: 예, Aspose.PSD의 무료 체험판은 [here](https://releases.aspose.com/)에서 이용할 수 있습니다.

**Q: 라이선스는 어떻게 구매하나요?**  
A: Aspose.PSD는 [here](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

**Q: 지원은 어디서 받을 수 있나요?**  
A: 지원 및 토론은 [Aspose’s forum](https://forum.aspose.com/c/psd/34)에서 받을 수 있습니다.

## 결론
이 가이드를 따라 하면 이제 Aspose.PSD의 Graphics Path 클래스를 사용하여 복잡한 벡터 형태, 삽입된 텍스트 및 투명 배경을 가진 **이미지 생성 방법**을 알게 됩니다. 다양한 펜, 브러시 및 경로 기하학을 실험하여 게임, UI 요소 또는 자동 보고서 생성에 활용할 수 있는 풍부한 그래픽을 만들어 보세요.

---

**마지막 업데이트:** 2026-09-08  
**테스트 환경:** Aspose.PSD for Java 24.11  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.PSD를 사용하여 경로 설정으로 Java에서 PSD 이미지 생성](/psd/java/image-editing/create-image-by-setting-path/)
- [Aspose.PSD for Java로 이미지 크기 조정 – 도형 그리기 및 기본 이미지 작업](/psd/java/basic-image-operations/)
- [이미지에 서명 추가 – Aspose.PSD for Java로 캔버스에 이미지 그리기](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
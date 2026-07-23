---
date: 2026-03-04
description: Aspose.PSD를 사용하여 Java에서 그래픽 객체를 생성하고 PSD 파일에 대각선 워터마크를 추가하는 방법을 배웁니다.
  이 단계별 가이드는 Java 이미지 워터마크 라이브러리 사용법을 다룹니다.
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: Java에서 그래픽 객체 만들기 – PSD용 대각선 워터마크
url: /ko/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 PSD 파일에 대각선 워터마크 추가

## 소개
이 튜토리얼에서는 **그래픽 객체 java 생성**을 작성하여 PSD 파일에 방향 워터 마크를 하는 방법을 배웁니다. 디자이너가 광물을 보호하거나 마케터가 이미지를 브랜딩하려는 경우, 번거로운 마크는 작업을 전문적으로 안전하게 찾는 사람들입니다. 각 단계를 설명하면 여러분의 프로젝트에 바로 적용할 수 있습니다.

## 빠른 답변
- **어떤 라이브러리가 필요합니까?** Java용 Aspose.PSD(강력한 Java 이미지 워터마크 라이브러리).
- **이 튜토리얼에서는 어떤 기본 키워드를 다루나요?** 그래픽 개체 java를 만듭니다.
- **라이센스가 필요합니까?** 무료 평가판을 사용하여 테스트할 수 있습니다. 생산을 위해서는 상업용 라이센스가 필요합니다.
- **워터마크 텍스트와 스타일을 변경할 수 있습니까?** 예 – 글꼴, 색상, 불투명도 및 회전을 사용자 정의할 수 있습니다.
- **어떤 출력 형식이 지원됩니까?** 예제는 PNG로 저장되지만 Aspose.PSD는 PSD, JPEG, BMP 등으로 내보낼 수 있습니다.

## Java의 그래픽 객체란 무엇입니까?
**그래픽**은 이미지의 드로잉 표면을 제거합니다. 그래픽을 생성하면, 도형 및 기타 요소를 비트맵이나 PSD 캔버스에 연결할 수 있는 방법에 직접 접근할 수 있습니다. 이것이 기본 키워드 **그래픽 객체 생성 java**의 핵심 컨셉입니다.

## 워터마킹에 Aspose.PSD를 사용하는 이유는 무엇입니까?
Aspose.PSD는 Adobe Photoshop 없이도 동작한다고 말합니다 **java 이미지 워터마크 라이브러리**입니다. 레이어는 서버측 처리나 배치 작업에 있어 확실하게 제어할 수 있습니다.

## 전제 조건
코드 작성을 시작하기 전에 다음 항목을 준비하세요:

### 1. 자바 개발 환경
최신 JDK를 [Java 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 설치합니다.

### 2. Aspose.PSD 라이브러리
[Aspose 다운로드 페이지](https://releases.aspose.com/psd/java/)에서 라이브러리를 다운로드합니다. Maven, Gradle 또는 수동 클래스 추가를 통해 JAR를 프로젝트에 포함시키세요.

### 3. 자바의 기본 이해
클래스, 파일 및 파일 I/O에 대한 기본 지식이 있으면 관련히 따라올 수 있습니다.

### 4. IDE 설정
IntelliJ IDEA, Eclipse 또는 NetBeans 중 하나를 사용하기 쉽게 코딩할 수 있습니다.

## 패키지 가져오기
PSD 파일을 조작하기 위해 필요한 Aspose.PSD 클래스를 가져옵니다:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

필요한 사전 작업과 패키지 임포트가 완료되었으니, 이제 PSD 파일에 대각선 워터마크를 추가하는 단계로 넘어갑니다.

## 1단계: 디렉토리 설정
```java
String dataDir = "Your Document Directory";
```
`"Your Document Directory"` 를 PSD 원본 파일이 위치한 폴더 경로로 교체하세요.

## 2단계: PSD 파일 불러오기
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
`Image.load` 메서드는 파일을 읽고 `PsdImage` 로 캐스팅하여 PSD‑전용 기능을 사용할 수 있게 합니다.

## 3단계: 그래픽 개체 생성
```java
Graphics graphics = new Graphics(psdImage);
```
여기서 **create graphics object java** 를 생성합니다 — 워터마크를 그릴 캔버스가 됩니다.

## 4단계: 워터마크용 글꼴 생성
```java
Font font = new Font("Arial", 20.0f);
```
설치된 폰트 중 하나를 선택하고, 크기로 워터마크의 눈에 띄는 정도를 조절합니다.

## 5단계: 워터마크용 브러시 생성
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
`alpha` 값(첫 번째 매개변수)은 투명도를 설정합니다. `alpha` 가 50이면 은은하고 반투명한 효과를 얻을 수 있습니다.

## 6단계: 변형 행렬 설정
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
이미지 중심을 기준으로 그리기 표면을 45° 회전시켜 대각선 효과를 만듭니다.

## 7단계: 문자열 정렬 정의
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
중앙 정렬을 사용하면 회전된 사각형 중앙에 워터마크가 깔끔하게 배치됩니다.

## 8단계: 워터마크 그리기
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
`"Some watermark text"` 를 브랜드명이나 저작권 문구로 교체하세요. 사각형은 텍스트가 렌더링될 영역을 정의합니다.

## 9단계: 이미지 저장
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
출력은 PNG 형식으로 저장되지만 Aspose.PSD가 지원하는 모든 포맷으로 선택할 수 있습니다.

## 일반적인 사용 사례
- **브랜드 보호:** 무단 재사용을 방지하기 위해 반투명 로고를 추가합니다.
- **일괄 처리:** 서버에서 거래소 이미지 라이브러리를 자동으로 워터마크 처리합니다.
- **크리에이티브 미리보기:** 원본 파일은 그대로, 클라이언트에게 워터마크가 적용된 초안을 보여줍니다.

## 문제 해결 및 팁
- **투명도가 보이지 않나요?** 투명도가 보호되는 면 `alpha` 값을 높이세요(예: `100`) 물을 더 많이 관리하세요.
- **워터마크가 중심에서 벗어난 것처럼 보입니까?** 회전 기준점 이미지를 사용할 수 없음/높이 승객인지 확인하세요.
- **성능 문제:** 여러 이미지를 루프에서 처리할 때 해당 `그래픽`이 생성되면 성능이 향상됩니다.

## FAQ
### Aspose.PSD란 무엇인가요?
Aspose.PSD는 Adobe Photoshop 없이도 PSD 파일을 작업하고 할 수 있게 해 주는 Java 클래스입니다.

### 워터마킹에 다른 글꼴을 사용할 수 있나요?
예를 들어, 시스템에 모든 통화를 표시할 수 있습니다.

### 워터마크 투명도를 맞춤설정할 수 있는 방법이 있나요?
물론입니다! `SolidBrush`의 `alpha` 값을 사용하면 투명도를 보호할 수 있습니다.

### 워터마크를 여러 개 추가할 수 있나요?
예, `drawString` 방법을 여러 번 호출하고 물 특수 목적을 특별 지정하면 여러 마크를 추가할 수 있습니다.

### Aspose.PSD에 대한 자세한 정보는 어디서 찾을 수 있나요?
문서는 [여기](https://reference.aspose.com/psd/java/)에서 받아볼 수 있습니다.

---

**최종 업데이트:** 2026-03-04
**테스트 대상:** Java용 Aspose.PSD 24.12
**저자:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
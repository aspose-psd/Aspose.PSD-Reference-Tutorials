---
date: 2026-01-14
description: Aspose.PSD for Java를 사용하여 PSD 파일에서 그라디언트 스트로크 레이어를 만들고 스트로크 그라디언트를 사용자
  정의하는 방법을 단계별 튜토리얼로 배워보세요.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Java에서 그라디언트 스트로크 레이어를 만드는 방법
url: /ko/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 그라디언트 스트로크 레이어 만들기

## 소개
Java를 사용하여 PSD 파일에 **그라디언트 스트로크 레이어**를 만드는 방법이 궁금하신가요? 바로 여기서 답을 찾으실 수 있습니다! 오늘은 Aspose.PSD for Java라는 강력한 라이브러리를 활용해 PSD 파일을 손쉽게 조작하는 방법을 살펴보겠습니다. 그래픽 프로그래밍이 처음이든 기존 디자인을 미세 조정하고 싶든, 이 가이드는 단계별로 스트로크 그라디언트를 추가하고 커스터마이징하는 과정을 안내합니다.

## 빠른 답변
- **주된 목표는?** PSD 파일에 그라디언트 스트로크 레이어를 생성하는 것.  
- **필요한 라이브러리는?** Aspose.PSD for Java.  
- **라이선스가 필요합니까?** 예, 프로덕션 사용을 위해 유효한(또는 임시) 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** Java 8 이상.  
- **구현 소요 시간은?** 기본 그라디언트 스트로크의 경우 대략 10‑15 분.

## 그라디언트 스트로크 레이어란?
그라디언트 스트로크 레이어는 도형이나 텍스트 주변에 색상이 부드럽게 전환되는 벡터 윤곽선입니다. Aspose.PSD를 사용하면 스트로크의 색상, 불투명도, 각도 및 유형(선형, 방사형 등)을 프로그래밍 방식으로 정의할 수 있습니다.

## 왜 Aspose.PSD for Java를 사용해야 할까요?
- **전체 PSD 지원** – Photoshop 없이 PSD 파일을 읽고, 편집하고, 저장할 수 있습니다.  
- **풍부한 이펙트 API** – 스트로크, 그림자, 글로우 등 다양한 레이어 효과에 접근할 수 있습니다.  
- **크로스‑플랫폼** – Java를 지원하는 모든 OS에서 동작합니다.  
- **네이티브 의존성 없음** – 순수 Java 기반이라 CI 파이프라인에 쉽게 통합됩니다.

## 전제 조건
1. **Java Development Kit (JDK)** – 최신 JDK를 [Oracle 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html)에서 설치합니다.  
2. **Aspose.PSD for Java** – [Aspose.PSD 다운로드 페이지](https://releases.aspose.com/psd/java/)에서 라이브러리를 다운로드합니다.  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans 중 하나.  
4. **라이선스** – 전체 라이선스가 없을 경우 [임시 라이선스](https://purchase.aspose.com/temporary-license/)를 획득합니다.

## 패키지 가져오기
PSD를 로드하고, 이펙트에 접근하며, 그라디언트 채우기를 구성하는 데 필요한 클래스를 먼저 가져옵니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

이제 과정을 명확한 단계로 나누어 보겠습니다.

## 단계 1: PSD 파일 로드
소스 PSD를 로드하고 스트로크 이펙트를 사용할 수 있도록 이펙트 리소스를 활성화합니다.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## 단계 2: 스트로크 이펙트 접근
수정하려는 스트로크가 세 번째 레이어(인덱스 2)에 있다고 가정하고, 해당 레이어의 `StrokeEffect`를 가져옵니다.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## 단계 3: 스트로크 이펙트 속성 확인
변경을 적용하기 전에 기존 설정을 확인하여 정확히 어떤 부분을 업데이트할지 파악합니다.

```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```

## 단계 4: 그라디언트 채우기 설정 수정
색상, 불투명도, 혼합 모드 및 기타 속성을 변경하여 원하는 외관을 구현합니다.

```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```

## 단계 5: 색상 및 투명도 포인트 추가 및 수정
새로운 색상 및 투명도 포인트를 추가하고, 기존 포인트를 조정해 그라디언트를 형태화합니다.

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## 단계 6: 수정된 PSD 파일 저장
모든 조정이 끝나면 업데이트된 파일을 디스크에 다시 씁니다.

```java
im.save(exportPath);
```

## 단계 7: 수정 내용 검증
저장된 파일을 다시 로드하고, 모든 속성이 적용된 대로 반영되었는지 확인합니다.

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## 결론
이제 Aspose.PSD for Java를 사용해 PSD 파일에 **그라디언트 스트로크 레이어** 효과를 만드는 방법을 알게 되었습니다. PSD를 로드하고, 스트로크 이펙트에 접근한 뒤, 그라디언트 채우기 설정을 조정하고, 결과를 저장함으로써 Photoshop을 전혀 열지 않고도 전문적인 그래픽을 프로그래밍적으로 생성할 수 있습니다.

## FAQ
### Aspose.PSD for Java란?
Aspose.PSD for Java는 Java 애플리케이션에서 PSD 파일을 작업할 수 있게 해 주는 라이브러리로, PSD 파일을 생성, 조작 및 변환하는 기능을 제공합니다.

### Aspose.PSD for Java를 사용하려면 라이선스가 필요합니까?
예, Aspose.PSD for Java를 사용하려면 유효한 라이선스가 필요합니다. 평가용으로는 [임시 라이선스](https://purchase.aspose.com/temporary-license/)를 받을 수 있습니다.

### Aspose.PSD for Java로 처음부터 PSD 파일을 만들 수 있나요?
물론입니다! Aspose.PSD for Java는 프로그래밍 방식으로 PSD 파일을 생성하고 조작할 수 있는 포괄적인 API를 제공합니다.

### Aspose.PSD for Java를 사용해 다른 이펙트를 적용할 수 있나요?
예, 그림자, 글로우 등 다양한 이펙트를 Aspose.PSD for Java를 통해 적용할 수 있습니다.

### Aspose.PSD for Java 문서는 어디서 찾을 수 있나요?
문서는 [여기](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2026-01-14  
**테스트 환경:** Aspose.PSD for Java 24.11  
**작성자:** Aspose
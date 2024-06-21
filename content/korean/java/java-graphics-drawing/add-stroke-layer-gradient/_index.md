---
title: Java에서 스트로크 레이어 그라디언트를 추가하는 방법
linktitle: Java에서 스트로크 레이어 그라디언트를 추가하는 방법
second_title: Aspose.PSD 자바 API
description: 이 포괄적인 단계별 튜토리얼을 통해 Java용 Aspose.PSD를 사용하여 PSD 파일에 스트로크 레이어 그라데이션을 추가하고 사용자 정의하는 방법을 알아보세요.
type: docs
weight: 10
url: /ko/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## 소개
Java를 사용하여 이미지에 획 레이어 그라데이션을 추가하는 방법이 궁금하신가요? 글쎄, 당신은 바로 이곳에 있어요! 오늘 우리는 PSD 파일을 쉽게 조작하는 데 도움이 되는 강력한 라이브러리인 Aspose.PSD for Java의 세계에 대해 알아봅니다. 초보자이든 숙련된 개발자이든 이 단계별 가이드는 PSD 파일에 스트로크 레이어 그래디언트를 추가하는 과정을 안내합니다. 그러니 버클을 채우고 그래픽 편집 기술을 향상할 준비를 하세요!
## 전제조건
시작하기 전에 준비해야 할 몇 가지 사항이 있습니다. 다음 사항이 있는지 확인하세요.
1.  JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[오라클의 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Java 라이브러리용 Aspose.PSD: 다음에서 다운로드할 수 있습니다.[Aspose.PSD 다운로드 페이지](https://releases.aspose.com/psd/java/).
3. 통합 개발 환경(IDE): IntelliJ IDEA, Eclipse 또는 NetBeans와 같은 모든 IDE가 작동합니다.
4.  유효한 라이센스:[임시면허](https://purchase.aspose.com/temporary-license/) 완전한 것이 없다면.
## 패키지 가져오기
먼저 필요한 패키지를 가져오겠습니다. 이를 통해 PSD 파일을 조작하는 데 필요한 클래스와 메서드를 사용할 수 있습니다.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
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
이제 더 나은 이해를 위해 예제를 여러 단계로 나누어 보겠습니다.
## 1단계: PSD 파일 로드
 먼저 수정하려는 PSD 파일을 로드해야 합니다. 우리는`PsdLoadOptions` 효과 리소스를 로드하도록 지정합니다.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## 2단계: 획 효과에 액세스
다음으로 관심 있는 레이어의 획 효과에 액세스해야 합니다. 여기서는 해당 레이어가 PSD 파일의 세 번째 레이어(인덱스 2)라고 가정합니다.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## 3단계: 획 효과 속성 확인
변경하기 전에 획 효과의 속성을 확인하여 올바른 설정을 수정하고 있는지 확인해 보겠습니다.
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
## 4단계: 그라데이션 채우기 설정 수정
이제 요구 사항에 따라 그라데이션 채우기 설정을 수정해야 합니다. 색상, 불투명도, 혼합 모드 및 기타 속성을 변경하겠습니다.
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
## 5단계: 색상 및 투명도 포인트 추가 및 수정
새로운 색상 및 투명도 포인트를 추가하고 기존 포인트를 수정하여 원하는 그라데이션 효과를 얻으세요.
```java
// 새로운 컬러 포인트 추가
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// 이전 포인트 위치 변경
fillSettings.getColorPoints()[1].setLocation(1899);
// 새 투명도 포인트 추가
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// 이전 투명점 위치 변경
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## 6단계: 수정된 PSD 파일 저장
필요한 모든 수정을 마친 후 PSD 파일을 저장해야 합니다.
```java
im.save(exportPath);
```
## 7단계: 수정 사항 확인
마지막으로 저장된 PSD 파일을 로드하고 변경 사항이 올바르게 적용되었는지 확인해 보겠습니다.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// 컬러 포인트 확인
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
// 투명 포인트 확인
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
그리고 거기에 있습니다! 이제 Java용 Aspose.PSD를 사용하여 PSD 파일에 스트로크 레이어 그라데이션을 추가하고 조작하는 방법을 알았습니다. 이 튜토리얼에서는 PSD 파일 로드, 획 효과 액세스 및 수정, 변경 사항 저장에 대해 다뤘습니다. 이러한 기술을 사용하면 시각적으로 매력적인 그라디언트를 만들고 필요에 맞게 PSD 파일을 사용자 정의할 수 있습니다.
## FAQ
### Java용 Aspose.PSD란 무엇입니까?
Aspose.PSD for Java는 개발자가 Java 애플리케이션에서 PSD 파일을 작업할 수 있도록 하는 라이브러리로, PSD 파일을 생성, 조작 및 변환하는 기능을 제공합니다.
### Java용 Aspose.PSD를 사용하려면 라이센스가 필요합니까?
 예, Aspose.PSD for Java를 사용하려면 유효한 라이센스가 필요합니다. 당신은 얻을 수 있습니다[임시면허](https://purchase.aspose.com/temporary-license/) 평가 목적으로.
### Java용 Aspose.PSD를 사용하여 PSD 파일을 처음부터 만들 수 있나요?
전적으로! Aspose.PSD for Java는 프로그래밍 방식으로 PSD 파일을 생성하고 조작할 수 있는 포괄적인 API를 제공합니다.
### Aspose.PSD for Java를 사용하여 다른 효과를 적용할 수 있나요?
예, Java용 Aspose.PSD를 사용하여 그림자, 광선 등과 같은 다양한 효과를 적용할 수 있습니다.
### Java용 Aspose.PSD에 대한 설명서는 어디에서 찾을 수 있나요?
 문서를 찾을 수 있습니다[여기](https://reference.aspose.com/psd/java/).
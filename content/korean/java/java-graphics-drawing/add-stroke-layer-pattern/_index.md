---
title: Java에서 스트로크 레이어 패턴을 추가하는 방법
linktitle: Java에서 스트로크 레이어 패턴을 추가하는 방법
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일에 스트로크 레이어 패턴을 추가하는 방법을 알아보세요. 이미지를 쉽게 향상하려면 이 단계별 가이드를 따르십시오.
type: docs
weight: 11
url: /ko/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## 소개
Java에서 이미지에 획 레이어 패턴을 추가하는 것은 어려운 작업처럼 들릴 수 있지만 Java용 Aspose.PSD를 사용하면 생각보다 쉽습니다. 그래픽을 디자인하든 사진 편집 응용 프로그램을 사용하든 이 가이드는 프로세스를 단계별로 안내합니다. 시작할 준비가 되셨나요? 뛰어들어보자!
## 전제조건
시작하기 전에 몇 가지 사항이 필요합니다.
- JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요.
-  Java용 Aspose.PSD: 다음에서 라이브러리를 다운로드하세요.[여기](https://releases.aspose.com/psd/java/) 프로젝트에 포함시키세요.
- IDE: IntelliJ IDEA 또는 Eclipse와 같이 선호하는 IDE(통합 개발 환경)를 사용하세요.
## 패키지 가져오기
먼저, 필요한 패키지를 Java 프로젝트로 가져와야 합니다. 이 패키지는 Aspose.PSD 작업에 필수적입니다.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## 1단계: PSD 파일 로드
획 레이어 패턴을 추가하는 첫 번째 단계는 편집하려는 PSD 파일을 로드하는 것입니다.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
이제 PSD 파일을 로드하면 해당 레이어와 효과에 액세스하고 조작할 수 있습니다.
## 2단계: 새 패턴 데이터 준비
다음으로 스트로크 레이어에 적용할 새 패턴 데이터를 준비해야 합니다.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
이 패턴 데이터는 새로운 획 효과를 만드는 데 사용됩니다.
## 3단계: 획 효과에 액세스
획 효과를 수정하려면 특정 레이어와 해당 레이어의 혼합 옵션에 액세스해야 합니다.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
이렇게 하면 올바른 레이어와 효과로 작업할 수 있습니다.
## 4단계: 획 효과 수정
이제 새로운 패턴 데이터로 획 효과를 수정해 보겠습니다.
### 획 효과 속성 업데이트
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### 패턴 리소스 업데이트
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
이 코드 조각은 패턴 리소스를 새 패턴 데이터로 업데이트합니다.
## 5단계: 새 패턴 적용
마지막으로 새 패턴을 획 효과에 적용하고 변경 사항을 저장합니다.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
이렇게 하면 새 패턴이 올바르게 적용되고 파일이 변경 사항과 함께 저장됩니다.
## 6단계: 변경 사항 확인
모든 것이 제대로 작동하는지 확인하려면 파일을 다시 로드하고 변경 사항을 확인하세요.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
이 단계에서는 패턴 데이터가 획 효과에 올바르게 적용되었는지 확인합니다.
## 결론
그리고 거기에 있습니다! Java용 Aspose.PSD를 사용하여 PSD 파일에 스트로크 레이어 패턴을 성공적으로 추가했습니다. 다음 단계를 따르면 이미지를 쉽게 사용자 정의하고 향상할 수 있습니다. 즐거운 코딩하세요!
## FAQ
### Java용 Aspose.PSD란 무엇입니까?
Aspose.PSD for Java는 개발자가 프로그래밍 방식으로 PSD(Photoshop Document) 파일을 생성, 편집 및 변환할 수 있는 라이브러리입니다.
### 상용 프로젝트에서 Java용 Aspose.PSD를 사용할 수 있나요?
 예, 상업용 프로젝트에 사용할 수 있습니다. 다음에서 라이센스를 구입할 수 있습니다.[여기](https://purchase.aspose.com/buy).
### Aspose.PSD for Java에 대한 무료 평가판이 있습니까?
 예, 다음에서 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).
### Java용 Aspose.PSD에 대한 지원을 어떻게 받을 수 있나요?
 Aspose 커뮤니티 포럼에서 지원을 받을 수 있습니다.[여기](https://forum.aspose.com/c/psd/34).
### Java용 Aspose.PSD의 시스템 요구 사항은 무엇입니까?
개발을 위해서는 JDK가 설치되어 있어야 하고 IDE가 필요합니다. 라이브러리는 Windows, Linux 및 macOS를 포함한 여러 운영 체제를 지원합니다.
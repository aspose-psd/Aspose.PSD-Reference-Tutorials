---
date: 2026-01-17
description: Aspose.PSD for Java를 사용하여 스트로크 패턴을 추가하는 방법을 배워보세요. 이 단계별 가이드를 따라 PSD
  이미지를 빠르게 향상시키세요.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Aspose.PSD를 사용하여 Java에서 스트로크 패턴 추가하는 방법
url: /ko/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD를 사용하여 Java에서 스트로크 패턴 추가하는 방법

## Introduction
Photoshop 파일에 **스트로크 패턴을 Java** 로 추가해야 할 경우, Aspose.PSD for Java를 사용하면 놀라울 정도로 간단합니다. 그래픽 디자인 툴을 만들든, 배치 편집을 자동화하든, 레이어 효과를 실험하든, 이 튜토리얼은 PSD를 로드하는 단계부터 새로운 패턴을 검증하는 단계까지 모든 과정을 안내합니다. 이제 바로 시작해서 이미지를 빠르게 향상시키는 방법을 살펴보세요.

## Quick Answers
- **필요한 라이브러리는?** Aspose.PSD for Java  
- **지원되는 Java 버전은?** JDK 8 이상  
- **테스트에 라이선스가 필요합니까?** 개발 단계에서는 무료 체험판으로 충분하며, 운영 단계에서는 라이선스가 필요합니다  
- **구현 시간은 얼마나 걸립니까?** 기본 패턴 스트로크의 경우 대략 10‑15 분 정도  
- **여러 레이어에 패턴을 재사용할 수 있나요?** 예, 동일한 `PattResource`를 다른 레이어에 할당하면 됩니다  

## What is add stroke pattern java?
Java에서 스트로크 패턴을 추가한다는 것은 레이어의 스트로크 효과에 사용자 정의 채우기(보통 반복되는 비트맵)를 적용하는 것을 의미합니다. 이 기술을 사용하면 대시 라인, 벽돌 텍스처, 맞춤 그래픽 테두리 등 스타일화된 외곽선을 PSD 파일 내부에서 바로 만들 수 있으며, Photoshop을 열 필요가 없습니다.

## Why Use Aspose.PSD for add stroke pattern java?
- **Full PSD fidelity** – 모든 레이어 효과, 리소스 및 블렌드 모드가 그대로 유지됩니다.  
- **No native Photoshop required** – JDK가 설치된 모든 OS에서 작동합니다.  
- **Programmatic control** – 배치 처리 자동화 또는 서버‑사이드 서비스에 통합할 수 있습니다.  
- **Rich API** – 전역 리소스, 패턴 채우기, 블렌드 모드 등을 하나의 유창한 인터페이스에서 사용할 수 있습니다.

## Prerequisites
- **Java Development Kit (JDK)** – JDK 8 이상 설치를 확인하세요.  
- **Aspose.PSD for Java** – 라이브러리를 [here](https://releases.aspose.com/psd/java/)에서 다운로드하고 JAR를 프로젝트 클래스패스에 추가합니다.  
- **IDE** – IntelliJ IDEA, Eclipse 또는 선호하는 편집기.

## Import Packages
먼저 PSD 파일, 색상, 사각형 및 스트로크 효과를 처리하는 데 필요한 클래스를 가져옵니다.

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

## Step 1: Load the PSD File
소스 PSD를 로드하여 레이어와 리소스를 작업할 수 있게 합니다.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Step 2: Prepare New Pattern Data
스트로크에 사용할 간단한 4 × 4 픽셀 패턴을 생성합니다.

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

## Step 3: Access the Stroke Effect
대상 레이어(예시에서는 네 번째 레이어)에서 스트로크 효과를 찾습니다.

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Step 4: Modify the Stroke Effect
### Update Stroke Effect Properties
불투명도와 블렌드 모드를 조정하여 새로운 패턴이 시각적으로 어떻게 적용되는지 확인합니다.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Update the Pattern Resource
기존 전역 패턴 리소스를 방금 만든 리소스로 교체합니다.

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

## Step 5: Apply the New Pattern
업데이트된 패턴 리소스를 스트로크 효과에 바인딩하고 PSD를 저장합니다.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Step 6: Verify the Changes
파일을 다시 로드하고 새로운 패턴, 불투명도 및 블렌드 모드가 올바르게 적용되었는지 확인합니다.

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

## Common Issues and Solutions
| 문제 | 원인 | 해결 방법 |
|------|------|-----------|
| 패턴이 표시되지 않음 | `PatternId` 참조 오류 | `PattResource`에 설정한 `PatternId`가 `PatternFillSettings`에서 사용된 것과 일치하는지 확인합니다. |
| 저장 후 스트로크가 사라짐 | 불투명도가 0이거나 효과가 숨김 | `setOpacity` 값이 0‑255 사이인지, `isVisible()`이 `true`인지 확인합니다. |
| 색상이 예상과 다름 | 블렌드 모드 불일치 | 디자인 의도에 맞는 `BlendMode.Color`(또는 다른 모드)를 사용합니다. |

## FAQ's
### What is Aspose.PSD for Java?
Aspose.PSD for Java는 개발자가 프로그래밍 방식으로 PSD(Photoshop Document) 파일을 생성, 편집 및 변환할 수 있게 해주는 라이브러리입니다.

### Can I use Aspose.PSD for Java in a commercial project?
예, 상업 프로젝트에서도 사용할 수 있습니다. 라이선스는 [here](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

### Is there a free trial available for Aspose.PSD for Java?
예, 무료 체험 버전을 [here](https://releases.aspose.com/)에서 다운로드할 수 있습니다.

### How can I get support for Aspose.PSD for Java?
Aspose 커뮤니티 포럼에서 지원을 받을 수 있습니다: [here](https://forum.aspose.com/c/psd/34).

### What are the system requirements for Aspose.PSD for Java?
JDK가 설치된 개발 환경과 IDE만 있으면 됩니다. 이 라이브러리는 Windows, Linux, macOS 등 다양한 운영 체제를 지원합니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose
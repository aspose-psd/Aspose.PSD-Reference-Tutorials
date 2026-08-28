---
date: 2026-08-28
description: Aspose.PSD를 사용하여 Java에서 레이어에 pattern을 추가합니다. 이 단계별 가이드를 따라 stroke layer
  effect를 적용하고, pattern resources를 구성하며, PSD files를 효율적으로 저장하세요.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Java에서 Stroke Layer Pattern을 추가하는 방법
og_description: Aspose.PSD를 사용하여 Java에서 레이어에 pattern을 추가합니다. 이 간결한 가이드를 따라 stroke
  layer effect를 적용하고, pattern resources를 구성하며, PSD files를 효율적으로 저장하세요.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Java에서 레이어에 pattern 추가 – Aspose.PSD 튜토리얼
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Java에서 레이어에 pattern을 추가하는 방법
url: /ko/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 레이어에 패턴 추가하기

## 소개
Java에서 레이어에 패턴을 추가하는 것은 Photoshop PSD 파일에 사용자 정의 스트로크 효과를 적용해야 할 때 흔히 요구되는 작업입니다. Aspose.PSD for Java를 사용하면 이 작업이 간단해지며, 라이브러리를 처음 사용하는 경우에도 쉽게 할 수 있습니다. 이 튜토리얼에서는 PSD를 로드하고, 패턴 리소스를 생성한 뒤, 스트로크 효과에 연결하고, 결과를 저장하는 방법을 단계별로 명확하게 배울 수 있습니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.PSD for Java.  
- **구현에 걸리는 시간은?** 기본 패턴의 경우 약 10‑15 minutes.  
- **라이선스가 필요한가요?** 개발에는 무료 체험판을 사용할 수 있으며, 프로덕션에는 상용 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** JDK 8 이상.  
- **웹 서비스에서 사용할 수 있나요?** 예, API는 플랫폼에 구애받지 않으며 모든 Java 환경에서 작동합니다.

## 레이어에 패턴을 추가한다는 것은 무엇인가요?
레이어에 패턴을 추가한다는 것은 스트로크 또는 채우기 효과에 타일형 비트맵을 할당하여 그래픽이 도형의 외곽을 따라 반복되도록 하는 것을 의미합니다. 이 기법은 장식용 테두리, 텍스처, 브랜드 오버레이 등에 널리 사용되며, 디자이너가 각 요소를 수동으로 그리지 않고도 일관된 시각적 테마를 만들 수 있게 합니다.

## 이 작업에 Aspose.PSD를 사용하는 이유는?
Aspose.PSD는 **30개 이상의 이미지 포맷**을 지원하며 전체 문서를 메모리에 로드하지 않고도 **2 GB**까지의 PSD 파일을 조작할 수 있어 일반 서버 하드웨어에서도 빠른 성능을 제공합니다. 직관적인 API를 통해 레이어 효과를 프로그래밍 방식으로 다룰 수 있어 자동화 파이프라인에서 Photoshop이 필요하지 않습니다.

## 전제 조건
- Java Development Kit (JDK) 8 이상 설치.
- Aspose.PSD for Java – **Aspose.PSD for Java download page**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/))에서 다운로드하고 JAR를 프로젝트 클래스패스에 추가합니다.
- IntelliJ IDEA 또는 Eclipse와 같은 IDE를 사용하여 샘플 코드를 편집하고 실행합니다.
- 수정하려는 도형 레이어가 포함된 샘플 PSD 파일.

## 패키지 가져오기
먼저, PSD 객체, 리소스 및 효과에 접근할 수 있는 네임스페이스를 가져옵니다.

```
// No actual code block is added to preserve original placeholders.
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
```

## Java에서 레이어에 패턴을 추가하는 방법은?

대상 PSD를 로드하고, 패턴 리소스를 생성한 뒤, 원하는 레이어의 스트로크 효과에 연결하고, 마지막으로 파일을 저장합니다. 이 전체 흐름은 몇 줄의 코드만으로 구현 가능하며 벡터 도형 레이어가 포함된 표준 PSD라면 모두 작동합니다.

### 단계 1: PSD 파일 로드
문서를 로드하면 레이어 계층 구조와 효과 컬렉션에 접근할 수 있습니다.  
`PsdLoadOptions`는 PSD 읽기 방식을 설정하고, `PsdImage`는 메모리 내에 로드된 파일을 나타냅니다.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

PSD 파일을 로드함으로써 이제 레이어와 효과를 접근하고 조작할 수 있습니다.

### 단계 2: 새로운 패턴 데이터 준비
`PatternResource`를 생성하여 스트로크 패턴으로 사용할 비트맵을 저장합니다.  
`PatternResource`는 반복 비트맵 패턴을 저장하는 PSD 전역 리소스이며, `Rectangle`은 패턴의 경계를 정의하고 `UUID`는 고유 식별자를 제공합니다.

```
// Placeholder for original code.
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
```

이 패턴 데이터는 새로운 스트로크 효과를 만드는 데 사용됩니다.

### 단계 3: 스트로크 효과 접근
이미 스트로크가 적용된 도형 레이어를 식별한 뒤, 해당 레이어의 `StrokeEffect` 객체를 가져옵니다.  
`StrokeEffect`는 도형 레이어에 적용된 스트로크 레이어 효과를 나타냅니다.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

이를 통해 올바른 레이어와 효과를 작업하고 있음을 확인할 수 있습니다.

### 단계 4: 스트로크 효과 수정
이제 스트로크 속성을 업데이트하여 새로운 패턴 리소스를 참조하도록 합니다.

#### 스트로크 효과 속성 업데이트
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### 패턴 리소스 업데이트
`PattResource`는 패턴 데이터를 저장하는 PSD 전역 레이어 리소스입니다.

```
// Placeholder for original code.
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
```

이 코드 조각들은 기존 패턴을 제공한 패턴으로 교체합니다.

### 단계 5: 새로운 패턴 적용
`PatternFillSettings`는 패턴 기반 스트로크 효과의 채우기 설정을 보유합니다. 변경 사항을 레이어에 커밋하고 업데이트된 PSD를 디스크에 저장합니다.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

이를 통해 새로운 패턴이 올바르게 적용되고 파일이 변경 사항과 함께 저장됩니다.

### 단계 6: 변경 사항 확인
파일을 다시 로드하고 스트로크를 검사하여 패턴이 예상대로 표시되는지 확인합니다.

```
// Placeholder for original code.
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
```

이 단계는 패턴 데이터가 스트로크 효과에 올바르게 적용되었는지 확인합니다.

## 일반적인 문제 및 해결 방법
- **패턴이 보이지 않음:** 패턴 이미지의 DPI가 PSD 해상도와 일치하는지, 스트로크의 `Enabled` 플래그가 `true`로 설정되어 있는지 확인하세요.  
- **대용량 PSD 파일로 OutOfMemoryError 발생:** `PsdImage.load(..., LoadOptions)`를 사용하고 `LoadOptions.setLoadAllLayers(false)`로 레이어를 필요할 때만 로드하도록 합니다.  
- **잘못된 레이어 선택:** 효과에 접근하기 전에 레이어 인덱스 또는 이름을 확인하세요; `psdImage.getLayers()`를 열거하여 사용 가능한 레이어를 확인할 수 있습니다.

## 자주 묻는 질문

**Q: Aspose.PSD for Java란 무엇인가요?**  
A: Aspose.PSD for Java는 개발자가 PSD(Photoshop Document) 파일을 프로그래밍 방식으로 생성, 편집 및 변환할 수 있게 해주는 라이브러리입니다.

**Q: Aspose.PSD for Java를 상업 프로젝트에 사용할 수 있나요?**  
A: 예, 상업 프로젝트에 사용할 수 있습니다. **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy))에서 라이선스를 구매할 수 있습니다.

**Q: Aspose.PSD for Java의 무료 체험판이 있나요?**  
A: 예, **Aspose releases page**([Aspose releases page](https://releases.aspose.com/))에서 무료 체험 버전을 다운로드할 수 있습니다.

**Q: Aspose.PSD for Java에 대한 지원은 어떻게 받을 수 있나요?**  
A: Aspose 커뮤니티 포럼 **here**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34))에서 지원을 받을 수 있습니다.

**Q: Aspose.PSD for Java의 시스템 요구 사항은 무엇인가요?**  
A: JDK가 설치되어 있어야 하며 개발을 위한 IDE가 필요합니다. 이 라이브러리는 Windows, Linux, macOS를 지원합니다.

## 결론
이제 Aspose.PSD를 사용하여 Java에서 레이어에 패턴을 추가하는 방법을 배웠습니다. 위 단계들을 따라 하면 커스텀 스트로크 패턴으로 PSD 파일을 프로그래밍 방식으로 향상시키고, 브랜드 워크플로를 자동화하며, 그래픽 처리를 모든 Java 기반 애플리케이션에 통합할 수 있습니다. 레이어 병합, 색상 조정, PNG 또는 JPEG로 내보내기와 같은 다른 Aspose.PSD 기능도 살펴보며 이미지 처리 툴킷을 더욱 확장해 보세요.

---

**마지막 업데이트:** 2026-08-28  
**테스트 환경:** Aspose.PSD 24.11 for Java  
**작성자:** Aspose

## 관련 튜토리얼

- [패턴 채우기 레이어 PSD 파일 렌더링](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [패턴 오버레이 PSD: Aspose.PSD for Java로 효과 추가](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Java에서 Aspose.PSD를 사용하여 스트로크 색상 변경 방법](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}
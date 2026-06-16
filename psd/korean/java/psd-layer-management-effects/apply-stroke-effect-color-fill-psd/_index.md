---
date: 2026-04-03
description: Aspose.PSD for Java를 사용하여 스트로크 효과와 색상 채우기가 적용된 PSD를 PNG로 저장하는 방법을 배워보세요.
  이 단계별 가이드는 PSD를 PNG로 빠르게 내보내는 방법을 보여줍니다.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: 스트로크 효과가 적용된 PSD를 PNG로 저장 – Java
second_title: Aspose.PSD Java API
title: 스트로크 효과와 함께 PSD를 PNG로 저장 – Java
url: /ko/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 PNG로 저장하고 스트로크 효과 및 색상 채우기 적용 – Java

## 소개

이 가이드에서는 Aspose.PSD for Java를 사용하여 스트로크 효과와 색상 채우기를 적용하면서 **PSD를 PNG로 저장**하는 방법을 배웁니다. 숙련된 개발자이든 이제 시작하는 개발자이든, 단계별 튜토리얼을 통해 작업을 쉽게 수행할 수 있습니다. 환경 설정부터 최종 이미지 내보내기까지 모든 과정을 다루므로, 자신의 프로젝트에서 빠르게 **PSD를 PNG로 내보낼** 수 있습니다.

## 빠른 답변
- **이 튜토리얼의 목표는 무엇인가요?** 사용자 정의 가능한 스트로크 효과를 적용한 후 PSD 파일을 PNG로 저장하는 방법을 보여줍니다.  
- **사용된 라이브러리는?** Aspose.PSD for Java.  
- **라이선스가 필요한가요?** 테스트용 무료 체험판을 사용할 수 있지만, 프로덕션에서는 라이선스가 필요합니다.  
- **스트로크 색상을 변경할 수 있나요?** 예 – `ColorFillSettings`를 통해 원하는 색상을 설정할 수 있습니다.  
- **배치 처리가 가능한가요?** 물론입니다 – 코드를 루프에 감싸 여러 PSD 파일을 처리할 수 있습니다.

## “PSD를 PNG로 저장”이란?
PSD를 PNG로 저장한다는 것은 Photoshop의 고유 레이어 파일을 평면화된 웹 친화적인 이미지 형식으로 변환하면서 시각적 충실도를 유지하는 것을 의미합니다. 이는 PSD 콘텐츠를 웹사이트, 모바일 앱 또는 PSD 파일을 직접 지원하지 않는 플랫폼에 표시해야 할 때 유용합니다.

## 색상 채우기와 함께 스트로크 효과를 적용하는 이유는?
스트로크는 레이어 내용 주위에 선명한 외곽선을 추가하여 복잡한 배경 위에서도 그래픽이 돋보이게 합니다. 이를 사용자 정의 채우기 색상과 결합하면 이미지를 브랜드화하거나 UI 요소를 강조하거나 눈길을 끄는 썸네일을 만들 수 있습니다.

## 사전 요구 사항

1. **Java Development Kit (JDK) 8+** – `java`가 PATH에 있는지 확인하세요.  
2. **Aspose.PSD for Java** – [website](https://releases.aspose.com/psd/java/)에서 다운로드하세요.  
3. **IDE** – IntelliJ IDEA, Eclipse 또는 선호하는 편집기.  
4. **샘플 PSD** – 이미 스트로크 효과가 포함된 파일(또는 Photoshop에서 추가).  
5. **기본 Java 지식** – 몇 줄의 코드를 작성하게 되지만 복잡한 내용은 없습니다.

이 준비가 되면 코딩을 시작할 수 있습니다.

## 패키지 가져오기

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

이 임포트는 PSD를 로드하고, 스트로크를 수정하며, PSD와 PNG 출력을 저장하는 데 필요한 모든 클래스를 포함합니다.

## 스트로크 효과와 함께 PSD를 PNG로 저장하는 방법

### 단계 1: PSD 파일 로드

먼저, 원본 PSD가 있는 폴더를 지정합니다.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"`를 실제 머신의 경로로 교체하세요.

이제 기존 효과 리소스를 보존하면서 파일을 로드합니다:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 단계 2: 스트로크 색상 설정 (및 선택적으로 너비 커스터마이징)

아래 루프는 각 레이어를 순회하면서 첫 번째 `StrokeEffect`를 가져와 채우기 색상을 변경합니다. **스트로크 너비를 커스터마이징**해야 하는 경우 `StrokeEffect` 객체의 `setWidth` 또는 `setPosition`을 조정할 수도 있습니다.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **팁:** `Color.getDeepPink()`은 예시일 뿐입니다. 사용자 정의 RGB 값은 `new Color(r, g, b)`를 사용하세요.

### 단계 3: 수정된 PSD 저장 (선택 사항)

업데이트된 스트로크가 적용된 PSD 버전을 보관하려면 다음과 같이 저장합니다:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### 단계 4: 이미지를 PNG로 내보내기 (핵심 “PSD를 PNG로 저장” 단계)

마지막으로, 편집된 PSD를 웹 사용에 적합한 PNG 파일로 변환합니다:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

PNG는 앞서 설정한 딥 핑크 스트로크를 유지하며, `TruecolorWithAlpha` 옵션은 투명도가 보존되도록 합니다.

## 일반적인 문제 및 해결책

| Issue | Reason | Fix |
|-------|--------|-----|
| **`ArrayIndexOutOfBoundsException`** | 레이어에 효과가 없거나 첫 번째 효과가 `StrokeEffect`가 아닙니다. | 레이어에 실제로 스트로크가 포함되어 있는지 확인하거나 `getEffects()`를 순회하여 올바른 유형을 찾으세요. |
| **Color not changing** | 설정 복사본을 편집하고 원본을 수정하지 않았을 가능성이 있습니다. | `effect.getFillSettings()`에서 직접 `ColorFillSettings`로 캐스팅했는지 확인하세요. |
| **PNG appears blank** | 레이어를 래스터화하지 않은 상태로 PSD를 로드했습니다. | 모든 수정 후 `im.save(..., new PngOptions())`를 호출하고, 변경 전 원본 `im`을 저장하는 것을 피하세요. |

## 자주 묻는 질문

**Q: Aspose.PSD for Java를 사용하여 단일 레이어에 여러 효과를 적용할 수 있나요?**  
A: 예, 레이어의 블렌딩 옵션에 접근하여 그림자, 글로우, 스트로크 등 필요한 만큼 효과를 추가할 수 있습니다.

**Q: PSD 파일 여러 개에 대해 프로세스를 자동화할 수 있나요?**  
A: 물론입니다. 로드, 효과 적용 및 저장 로직을 디렉터리의 파일들을 순회하는 `for‑each` 루프로 감싸면 됩니다.

**Q: PSD 파일에 적용한 변경을 어떻게 되돌릴 수 있나요?**  
A: 수정 사항을 저장하기 전에 원본 파일을 다시 로드하세요; Aspose.PSD는 언두 스택을 제공하지 않습니다.

**Q: 스트로크 너비와 위치를 커스터마이징할 수 있나요?**  
A: 예. `effect.setWidth(float)`와 `effect.setPosition(StrokeEffect.Position)`을 사용하여 두께와 배치를 (안쪽, 바깥쪽, 중앙) 제어할 수 있습니다.

**Q: Aspose.PSD for Java 라이브러리를 무료로 사용할 수 있나요?**  
A: 평가용 무료 체험판이 제공됩니다. 전체 기능을 사용하려면 라이선스를 구매해야 합니다. 자세한 내용은 [구매 옵션](https://purchase.aspose.com/buy)을 참조하세요.

---

**Last Updated:** 2026-04-03  
**테스트 환경:** Aspose.PSD 24.12 for Java  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
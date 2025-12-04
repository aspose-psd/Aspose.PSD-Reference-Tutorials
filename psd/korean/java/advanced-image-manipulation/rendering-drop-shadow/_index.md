---
date: 2025-12-04
description: Aspose.PSD for Java를 사용하여 PSD를 PNG로 저장하고 렌더링 드롭 섀도우를 적용하는 방법을 배웁니다. 이
  가이드는 섀도우 추가, PSD를 PNG로 변환, 그리고 Java에서 드롭 섀도우 적용 방법을 다룹니다.
language: ko
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Aspose.PSD Java로 PSD를 PNG로 저장하고 그림자 추가
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 PNG로 저장하고 Aspose.PSD Java로 그림자 추가

## 소개

Java에서 Photoshop 파일을 다룰 때 **PSD를 PNG로 저장**하면서 전문적인 그림자를 추가하는 것은 흔한 요구사항입니다. Aspose.PSD를 사용하면 몇 줄의 코드만으로 **PSD를 PNG로 변환**하고 **Java에서 그림자 적용**을 손쉽게 수행할 수 있습니다. 이번 튜토리얼에서는 PSD 파일을 로드하고 최종 PNG에 그림자 효과를 렌더링하여 내보내는 전체 과정을 단계별로 살펴보겠습니다.

## 빠른 답변
- **“PSD를 PNG로 저장”이란 무엇인가요?** 레이어가 있는 Photoshop 파일을 평면 PNG 이미지로 변환하여 투명성을 유지합니다.  
- **변환하면서 그림자를 추가할 수 있나요?** 네—Aspose.PSD를 사용하면 레이어 효과를 수정한 뒤 내보낼 수 있습니다.  
- **코드를 실행하려면 라이선스가 필요합니까?** 평가용 무료 체험판으로 테스트할 수 있으며, 실제 운영 환경에서는 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** Java 8 이상.  
- **그림자 효과를 커스터마이징할 수 있나요?** 물론입니다—색상, 불투명도, 거리, 크기, 각도 등 다양한 파라미터를 조정할 수 있습니다.

## 사전 요구 사항

시작하기 전에 다음을 준비하십시오:

- **Java 개발 환경** – JDK 8 이상 설치.  
- **Aspose.PSD 라이브러리** – 공식 사이트에서 최신 JAR 파일을 [여기](https://releases.aspose.com/psd/java/)에서 다운로드.  
- **PSD 파일** – 그림자를 적용하고 싶은 레이어가 최소 하나 이상 포함된 파일.  

## Java에서 PSD를 PNG로 저장하고 그림자를 추가하는 방법

아래는 단계별 가이드입니다. 각 단계마다 간단한 설명과 복사해서 사용할 수 있는 정확한 코드를 제공합니다.

### 단계 1: 필요한 패키지 가져오기

이미지 로드, 효과 처리 및 PNG 내보내기에 필요한 클래스를 import합니다.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### 단계 2: 문서 디렉터리 정의

소스 PSD와 결과 PNG가 위치할 폴더를 지정합니다.

```java
String dataDir = "Your Document Directory";
```

### 단계 3: PSD 및 PNG 파일 경로 설정

입력 PSD와 출력 PNG의 전체 경로를 지정합니다.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### 단계 4: 효과가 활성화된 상태로 PSD 파일 로드

**loadEffectsResource**를 활성화하면 레이어 효과(그림자 등)를 조작할 수 있습니다.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 단계 5: 드롭 섀도우 효과 접근

두 번째 레이어(인덱스 1)에 적용된 첫 번째 효과를 가져옵니다. 여기서 그림자 파라미터를 읽거나 수정합니다.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### 단계 6: 그림자 효과 속성 검증 (선택 사항이지만 유용)

기존 속성을 확인하면 변경이 필요한지 판단할 수 있습니다. 아래 어설션은 기본값을 확인합니다.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **전문가 팁:** 맞춤 설정으로 **그림자 추가**를 원한다면 `shadowEffect`의 속성을 저장하기 전에 수정하세요(예: `shadowEffect.setColor(Color.getRed());`).

### 단계 7: 수정된 이미지를 PNG로 저장

마지막으로 PSD(렌더링된 그림자 포함)를 PNG 파일로 내보냅니다. `TruecolorWithAlpha` 옵션은 투명성을 유지합니다.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

이제 **PSD를 PNG로 변환**하고 **Java에서 그림자 적용**까지 한 번에 완료되는 전체 워크플로우가 완성되었습니다.

## Aspose.PSD를 사용하는 이유

- **Photoshop이 필요 없음** – Java를 지원하는 모든 플랫폼에서 동작합니다.  
- **완전한 PSD 충실도** – 모든 레이어 정보, 마스크, 효과가 보존됩니다.  
- **세밀한 제어** – 내보내기 전에 그림자 각 파라미터를 자유롭게 조정할 수 있습니다.  
- **고성능** – 대용량 파일 및 배치 처리에 최적화되었습니다.

## 일반적인 문제 및 해결 방법

| 증상 | 가능 원인 | 해결 방법 |
|------|-----------|-----------|
| `NullPointerException` 발생 on `shadowEffect` | 대상 레이어에 효과가 없거나 인덱스가 잘못됨 | 레이어 인덱스(`im.getLayers()[i]`)를 확인하고 효과가 존재하는지 확인 |
| 내보낸 PNG가 빈 화면 | PNG 옵션이 올바르게 설정되지 않았거나 이미지가 저장되지 않음 | `PngColorType.TruecolorWithAlpha` 사용 및 `im.save()` 경로가 쓰기 가능한지 확인 |
| 그림자 색상이 보이지 않음 | 그림자 불투명도가 0이거나 배경과 색상이 동일 | `shadowEffect.setOpacity(255);` 로 설정하고 대비되는 색상 선택 |

## 자주 묻는 질문

**Q: 여러 레이어에 동시에 그림자를 적용할 수 있나요?**  
A: 가능합니다. `im.getLayers()`를 순회하면서 각 레이어의 `DropShadowEffect`를 필요에 따라 수정하면 됩니다.

**Q: ‘Spread’ 파라미터는 무엇을 의미하나요?**  
A: 그림자가 완전히 불투명한 상태에서 투명해지는 전환 정도를 제어합니다. 값이 높을수록 그림자 가장자리가 더 뚜렷해집니다.

**Q: Aspose.PSD가 모든 Photoshop 버전을 지원하나요?**  
A: 초기 버전부터 최신 Photoshop CC 파일까지 광범위한 PSD 버전을 지원합니다.

**Q: 문제가 발생하면 어디서 도움을 받을 수 있나요?**  
A: [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)에서 커뮤니티와 공식 지원을 받을 수 있습니다.

**Q: 구매 전에 Aspose.PSD를 체험해볼 수 있나요?**  
A: 물론입니다. [Aspose 웹사이트](https://releases.aspose.com/)에서 무료 체험판을 다운로드하세요.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**마지막 업데이트:** 2025-12-04  
**테스트 환경:** Aspose.PSD 24.12 for Java  
**작성자:** Aspose  

---
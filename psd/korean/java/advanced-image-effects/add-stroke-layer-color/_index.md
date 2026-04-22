---
date: 2026-04-22
description: Aspose.PSD for Java를 사용하여 스트로크 색상을 변경하는 방법을 배워보세요. 이 단계별 가이드를 따라 스트로크
  레이어 색상, 불투명도 등을 수정하세요.
keywords:
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
- add stroke layer psd
linktitle: 스트로크 레이어 색상 추가
second_title: Aspose.PSD Java API
title: Aspose.PSD를 사용하여 Java에서 스트로크 색상 변경 방법
url: /ko/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 Aspose.PSD를 사용하여 스트로크 색상 변경 방법

## 소개

프로그램matically 포토샵 문서에서 **change stroke color java**를 변경해야 한다면, Aspose.PSD for Java가 이를 간단하게 해줍니다. 이 튜토리얼에서는 스트로크 레이어를 추가하고, 색상을 변경하고, 불투명도를 조정하고, 결과를 저장하는 과정을 단계별로 안내합니다. 마지막에는 기존 레이어의 스트로크를 수정하는 방법도 확인하여 Java 코드에서 완전한 창의적 제어를 할 수 있게 됩니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.PSD for Java (최신 버전).  
- **스트로크 색상을 변경할 수 있나요?** 예 – `ColorFillSettings`를 사용하여任意의 `Color`를 설정합니다.  
- **라이선스가 필요합니까?** 평가용으로는 임시 라이선스로 충분하지만, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** Java 8 이상.  
- **구현 시간은 얼마나 걸리나요?** 기본 스트로크 변경은 보통 10분 미만 소요됩니다.

## PSD에서 스트로크 레이어란?

스트로크 레이어는 레이어 내용 주위에 외곽선을 그리는 벡터 효과입니다. 색상, 두께, 불투명도, 블렌드 모드 등으로 맞춤 설정할 수 있습니다. 이 효과를 프로그래밍으로 수정하면 자동 브랜딩, 일괄 처리, 동적 그래픽 생성이 가능해집니다.

## 스트로크 색상 변경에 Aspose.PSD를 사용하는 이유

- **Photoshop 불필요** – 전적으로 Java에서 작업합니다.  
- **전체 PSD 사양 호환** – 최신 PSD 기능을 모두 지원합니다.  
- **고성능** – 대용량 파일을 빠르게 처리합니다.  
- **크로스‑플랫폼** – JVM이 있는 모든 OS에서 실행됩니다.

## Java에서 스트로크 색상을 프로그래밍으로 변경하는 방법

아래는 Aspose.PSD for Java를 사용하여 스트로크 색상을 정확히 변경하는 방법을 단계별로 간결하게 보여줍니다. 각 단계는 짧은 설명과 원본 코드 블록(변경 없음)을 포함합니다.

### 사전 요구 사항

- **Aspose.PSD 라이브러리** – [공식 문서](https://reference.aspose.com/psd/java/)에서 다운로드합니다.  
- **Java Development Kit (JDK)** – 버전 8 이상.  
- **IDE** – Eclipse, IntelliJ IDEA 또는 Java 호환 편집기.

### 패키지 가져오기

먼저, 필요한 클래스를 가져옵니다. 이를 통해 프로젝트에서 PSD 처리 및 스트로크 효과 API에 접근할 수 있습니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

### 단계 1: 프로젝트 설정

새 Java 프로젝트를 생성하고, Aspose.PSD JAR 파일을 빌드 경로에 추가한 뒤, 라이브러리가 오류 없이 로드되는지 확인합니다.

### 단계 2: PSD 파일 로드

스트로크 정보를 사용할 수 있도록 효과 리소스 로딩을 활성화합니다.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### 단계 3: 스트로크 효과 레이어 접근

두 번째 레이어(인덱스 1)에서 첫 번째 스트로크 효과를 가져옵니다.

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### 단계 4: 스트로크 속성 검증

변경하기 전에 기존 속성을 확인합니다. 이는 예상치 못한 결과를 방지하는 데 도움이 됩니다.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### 단계 5: 색상 및 불투명도 설정 (스트로크 색상 변경 방법)

여기서는 스트로크 색상을 노란색으로 **변경**하고 불투명도를 50 % (127 / 255)로 낮춥니다.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### 단계 6: 수정된 PSD 저장

업데이트된 이미지를 디스크에 저장합니다. 새 파일에는 수정된 스트로크가 포함됩니다.

```java
im.save(exportPath);
```

## 스트로크 불투명도 수정 방법

원래 색상을 유지하면서 불투명도만 조정하려면 `setOpacity` 값을 (0‑255)로 변경합니다. 예를 들어, `colorStroke.setOpacity((byte)200);`은 스트로크를 약 78 % 불투명하게 만듭니다.

## 스트로크 효과 적용 방법

이미 스트로크 효과가 없는 레이어에 새 스트로크 효과를 추가하려면 `StrokeEffect` 인스턴스를 생성하고, `ColorFillSettings`를 구성한 뒤 레이어의 `BlendingOptions`에 연결합니다. 외관을 정의할 때는 동일한 `setColor`와 `setOpacity` 메서드를 사용합니다.

## PSD 스트로크 튜토리얼: PSD에 스트로크 레이어 추가

위 단계는 기존 레이어에 스트로크를 추가하는 방법을 보여줍니다. 완전히 새로운 스트로크 레이어를 만들려면 대상 레이어를 복제한 뒤 `StrokeEffect`를 적용합니다. 이 방법은 원본 레이어를 그대로 두고 싶을 때 유용합니다.

## 스트로크 색상 변경의 일반적인 사용 사례

- **브랜딩 자동화:** 단일 배치 실행으로 수백 개의 PSD 자산에 기업 색상을 로고에 적용합니다.  
- **동적 UI 생성:** 웹 기반 디자인 도구에서 사용자가 선택한 테마에 따라 실시간으로 스트로크 색상을 변경합니다.  
- **프리플라이트 준비:** 인쇄소에 파일을 보내기 전에 모든 스트로크 색상이 인쇄 사양을 충족하는지 확인합니다.

## 일반적인 함정 및 팁

- **Null 검사** – 캐스팅하기 전에 `getEffects()`가 null이 아닌 배열을 반환하는지 항상 확인합니다.  
- **레이어 인덱스** – PSD 레이어는 0부터 시작하므로 올바른 레이어를 대상으로 해야 합니다.  
- **색상 형식** – `Color.getYellow()`는 예시일 뿐이며, `new Color(r, g, b)`로 사용자 정의 색상을 만들 수 있습니다.  
- **불투명도 범위** – 불투명도는 바이트(0–255)이며, 255를 초과하는 값은 클램프됩니다.  
- **리소스 로딩** – `loadOptions.setLoadEffectsResource(true)`를 빼먹으면 `null` 효과 배열이 반환됩니다.

## 자주 묻는 질문

**Q: Aspose.PSD를 다른 Java 그래픽 라이브러리와 함께 사용할 수 있나요?**  
A: 예, Aspose.PSD는 Apache Commons Imaging이나 Java2D와 같은 라이브러리와 결합하여 기능을 확장할 수 있습니다.

**Q: Aspose.PSD가 최신 PSD 파일 형식과 호환되나요?**  
A: 물론입니다. 라이브러리는 최신 Photoshop 사양을 지원하도록 정기적으로 업데이트됩니다.

**Q: Aspose.PSD 사용 중 예외를 어떻게 처리하나요?**  
A: 자세한 문제 해결 및 예외 처리 샘플 코드는 [지원 포럼](https://forum.aspose.com/c/psd/34)을 참고하세요.

**Q: 구매 전에 Aspose.PSD를 체험할 수 있나요?**  
A: 물론입니다! 모든 기능을 살펴보려면 [무료 체험](https://releases.aspose.com/)을 이용하세요.

**Q: Aspose.PSD의 임시 라이선스는 어디서 얻을 수 있나요?**  
A: 개발 환경에서 라이브러리를 평가하려면 [임시 라이선스](https://purchase.aspose.com/temporary-license/)를 받으세요.

---

**마지막 업데이트:** 2026-04-22  
**테스트 환경:** Aspose.PSD 24.11 for Java  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
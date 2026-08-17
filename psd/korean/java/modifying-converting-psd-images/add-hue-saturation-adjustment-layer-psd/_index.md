---
date: 2026-03-13
description: Aspose.PSD for Java를 사용하여 PSD 파일에 색조·채도 레이어를 추가하는 방법을 배웁니다. 이 가이드는 또한
  PSD 파일을 일괄 처리하고 프로그래밍 방식으로 색조 조정 레이어를 만드는 방법을 보여줍니다.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Add Hue Saturation Layer to PSD with Aspose.PSD for Java
url: /ko/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD에 색조·채도 레이어 추가

## 소개
그래픽 디자인에서 색상 조작은 핵심적인 역할을 합니다—특히 색조, 채도, 밝기를 조정하면 이미지의 분위기와 품질을 크게 바꿀 수 있습니다. 이를 달성하는 효과적인 방법 중 하나는 Photoshop(PSD 파일)의 조정 레이어를 사용하는 것입니다. Java를 사용해 프로그래밍 방식으로 **add hue saturation layer**를 추가하려면 Aspose.PSD 라이브러리가 도움이 됩니다! 이 튜토리얼에서는 PSD 파일에 Hue Saturation Adjustment Layer를 추가하는 단계별 방법을 안내하여 작업 흐름을 보다 생산적이고 효율적으로 만들 수 있도록 합니다.

## 빠른 답변
- **Java에서 hue saturation layer를 추가할 수 있는 라이브러리는 무엇인가요?** Aspose.PSD for Java.  
- **Photoshop을 설치해야 하나요?** No, the library works independently of Photoshop.  
- **이 방법으로 PSD 파일을 일괄 처리할 수 있나요?** Yes—once you automate the steps you can apply them to many files.  
- **필요한 Java 버전은 무엇인가요?** JDK 8 or later.  
- **프로덕션 사용에 라이선스가 필요합니까?** Yes, a commercial license is required after the trial period.

## “add hue saturation layer” 작업이란 무엇인가요?
**add hue saturation layer** 작업은 원본 픽셀 데이터를 변경하지 않고 색조, 채도, 밝기 값을 수정할 수 있는 비파괴 조정 레이어를 생성합니다. 전체 구성이나 특정 색상 범위의 색을 미세 조정하는 데 이상적입니다.

## 왜 Aspose.PSD for Java를 사용하나요?
- **No Photoshop dependency** – Java가 실행되는 모든 플랫폼에서 작동합니다.  
- **Full PSD fidelity** – 모든 레이어 정보, 마스크 및 효과를 보존합니다.  
- **Batch‑ready** – 폴더를 순회하면서 동일한 조정을 수십 개 파일에 적용할 수 있습니다.  
- **Performance‑focused** – 대용량 문서와 서버 측 자동화를 위해 최적화되었습니다.

## 전제 조건
코드에 들어가기 전에 다음 사항이 준비되어 있는지 확인하세요:

1. **Java Development Kit (JDK):** 머신에 JDK 8 이상이 설치되어 있는지 확인하세요. [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html)에서 다운로드할 수 있습니다.  
2. **Aspose.PSD for Java Library:** Aspose.PSD 라이브러리가 필요합니다. [download here](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.  
3. **IDE:** IntelliJ IDEA 또는 Eclipse와 같은 적합한 통합 개발 환경(IDE)입니다.  
4. **Basic Java Knowledge:** Java 프로그래밍에 익숙하면 좋지만, 걱정하지 마세요—각 줄을 자세히 안내합니다.

이제 전제 조건이 준비되었으니, 재미있는 부분인 코딩으로 넘어갑시다!

## 패키지 가져오기
Aspose.PSD 라이브러리를 사용하려면 먼저 필요한 클래스를 가져와야 합니다. Java 파일에서 다음과 같이 할 수 있습니다:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

프로젝트에 적절한 라이브러리를 추가하여 이러한 import가 원활히 작동하도록 하세요.

## Step 1: 문서 디렉터리 설정
모든 프로젝트에는 시작점이 필요하며, 우리도 예외는 없습니다. PSD 파일이 저장된 디렉터리를 지정해야 합니다. 이는 이미지를 올바르게 로드하고 저장하는 데 필수적입니다.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Step 2: 기존 PSD 파일 로드
기존 PSD 파일을 조작하려면 먼저 프로그램에 로드해야 합니다. 다음과 같이 할 수 있습니다:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

이 코드에서 `"HueSaturationAdjustmentLayer.psd"`를 편집하려는 기존 PSD 파일 이름으로 교체하세요.

## Step 3: Hue/Saturation 레이어 편집
다음으로, 로드된 PSD 이미지의 레이어를 순회하여 기존 Hue/Saturation 레이어를 찾아 편집합니다. 이 단계에서는 색조, 채도, 밝기 값을 수정합니다.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

이 예시에서:  
- 색조를 **-25**, 채도를 **-12**, 밝기를 **+67**로 조정하고 있습니다.  
- `getRange(2)` 메서드를 사용하면 원하는 특정 색상 범위를 조정할 수 있습니다.

## Step 4: 수정된 PSD 파일 저장
조정을 마친 후 다음 단계는 파일을 저장하는 것입니다. 이는 변경 사항이 손실되지 않도록 하는 중요한 과정입니다.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Step 5: 새 Hue/Saturation 레이어 추가
처음부터 **create hue adjustment layer**가 필요하면, 다른 PSD 파일에 완전 새로운 Hue/Saturation 조정 레이어를 추가할 수 있습니다. 동일한 로드 방식을 따르되 `addHueSaturationAdjustmentLayer()` 메서드를 사용하세요.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Step 6: 새 레이어에 새로운 Hue/Saturation 값 설정
이제 새 레이어를 만들었으니, 이전과 같이 원하는 색조, 채도, 밝기 설정을 적용하세요.

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## Step 7: 업데이트된 PSD 파일 저장
마지막으로, 추가된 Hue/Saturation 레이어가 포함된 PSD 파일을 저장하여 변경 사항을 확인하세요.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

축하합니다! Aspose.PSD for Java를 사용해 PSD 파일을 성공적으로 조작했습니다. 이제 다양한 이미지와 더 깊은 변형을 실험하여 그래픽 디자인 프로젝트에 생명을 불어넣을 수 있습니다.

## 색조 조정을 사용해 PSD 파일을 일괄 처리하는 방법
위 코드는 완전히 스크립트화할 수 있으므로 폴더 내 모든 `.psd` 파일을 순회하는 루프에 전체 과정을 감쌀 수 있습니다. 이를 통해 **batch process psd files**를 수행하고 동일한 색조, 채도, 밝기 조정을 한 번에 적용할 수 있어 대규모 브랜드 업데이트에 적합합니다.

## 일반적인 문제 및 해결책
- **NullPointerException when loading a file:** `dataDir`이 적절한 파일 구분자(`/` 또는 `\`)로 끝나는지, 파일 이름이 올바른지 확인하세요.  
- **Adjustment values out of range:** 색조, 채도, 밝기는 -255에서 255 사이의 값을 허용합니다. 이 범위 내에서 값을 유지하세요.  
- **Layer not found:** PSD에 Hue/Saturation 레이어가 없으면 `instanceof` 검사가 해당 블록을 건너뜁니다. 먼저 `addHueSaturationAdjustmentLayer()`를 사용해 레이어를 생성하세요.

## 자주 묻는 질문

**Q: Hue Saturation Adjustment Layer란 무엇인가요?**  
A: 이미지의 색상 속성을 원본 픽셀을 영구적으로 변경하지 않고 수정할 수 있습니다.

**Q: Aspose.PSD를 사용하려면 Photoshop을 설치해야 하나요?**  
A: 아니요, Aspose.PSD는 Photoshop과 독립적으로 작동하는 독립형 라이브러리입니다.

**Q: Aspose.PSD를 사용해 일괄 처리할 수 있나요?**  
A: 예, Aspose.PSD를 사용해 여러 PSD 파일을 자동화하고 일괄 처리할 수 있습니다.

**Q: Aspose.PSD는 무료인가요?**  
A: Aspose.PSD는 무료 체험을 제공하지만, 장기 사용을 위해서는 라이선스가 필요합니다. 가격은 [here](https://purchase.aspose.com/buy)에서 확인할 수 있습니다.

## 결론
그래픽을 프로그래밍 방식으로 다루면 다양한 가능성이 열립니다. Aspose.PSD for Java를 사용해 **add hue saturation layer**와 **create hue adjustment layer**를 수행하면 디자인 워크플로우를 간소화할 수 있는 유연성과 효율성을 제공합니다. 프로젝트용 사진을 보정하거나 멋진 시각 콘텐츠를 만들 때, 이 도구들을 마스터하면 결과물을 크게 향상시킬 수 있습니다.

[documentation](https://reference.aspose.com/psd/java/)에서 Aspose.PSD의 더 많은 기능을 살펴보거나, 라이브러리의 전체 기능을 테스트하기 위해 [temporary license](https://purchase.aspose.com/temporary-license/)를 받아보세요.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2026-03-13  
**테스트 환경:** Aspose.PSD for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose  

---
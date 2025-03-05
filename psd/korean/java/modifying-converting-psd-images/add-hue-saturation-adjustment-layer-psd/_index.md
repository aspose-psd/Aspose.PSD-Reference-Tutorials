---
title: PSD에 색조 채도 조정 레이어 추가
linktitle: PSD에 색조 채도 조정 레이어 추가
second_title: Aspose.PSD 자바 API
description: 이 포괄적인 단계별 튜토리얼에서 Java용 Aspose.PSD를 사용하여 PSD에 색조 채도 조정 레이어를 추가하는 방법을 알아보세요. 그래픽 디자인 작업흐름을 향상시키세요.
type: docs
weight: 14
url: /ko/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## 소개
그래픽 디자인의 경우 색상 조작이 중추적인 역할을 합니다. 특히 색상, 채도, 밝기를 조정하면 이미지의 분위기와 품질이 크게 바뀔 수 있습니다. 이를 달성하는 한 가지 효과적인 방법은 Photoshop(PSD 파일)에서 조정 레이어를 사용하는 것입니다. Java를 사용하여 프로그래밍 방식으로 PSD 파일을 향상시키려는 경우 Aspose.PSD 라이브러리가 도움이 될 것입니다! 이 튜토리얼에서는 PSD 파일에 색조 채도 조정 레이어를 추가하여 작업 흐름을 더욱 생산적이고 효율적으로 만드는 단계를 안내합니다.
이 가이드에서는 필요한 패키지 가져오기부터 코드 예제의 핵심 세부 정보까지 모든 내용을 다룹니다.
## 전제조건
코드를 시작하기 전에 다음 사항이 준비되어 있는지 확인하세요.
1.  JDK(Java Development Kit): 컴퓨터에 JDK 8 이상이 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[Java SE 개발 키트 다운로드](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Java 라이브러리용 Aspose.PSD: Aspose.PSD 라이브러리가 있어야 합니다.[여기서 다운로드하세요](https://releases.aspose.com/psd/java/). 
3. IDE: IntelliJ IDEA 또는 Java 개발용 Eclipse와 같은 적합한 통합 개발 환경(IDE)입니다.
4. 기본 Java 지식: Java 프로그래밍에 익숙하면 도움이 되지만 걱정하지 마세요. 코드를 단계별로 안내해 드리겠습니다.
이제 전제 조건이 정렬되었으므로 재미있는 부분인 코딩으로 넘어가겠습니다!
## 패키지 가져오기
Aspose.PSD 라이브러리 작업을 시작하려면 첫 번째 단계는 필요한 클래스를 가져오는 것입니다. Java 파일에서 이를 수행하는 방법은 다음과 같습니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
이러한 가져오기가 원활하게 작동하도록 프로젝트에 적절한 라이브러리를 추가했는지 확인하세요.
## 1단계: 문서 디렉토리 설정
모든 프로젝트에는 출발점이 필요하며 우리 프로젝트도 예외는 아닙니다. PSD 파일이 저장되는 디렉터리를 지정해야 합니다. 이는 이미지를 올바르게 로드하고 저장하는 데 중요합니다.
```java
String dataDir = "Your Document Directory"; // 이 경로를 실제 디렉터리로 업데이트하세요.
```
## 2단계: 기존 PSD 파일 로드
기존 PSD 파일을 조작하려면 먼저 해당 파일을 프로그램에 로드해야 합니다. 그렇게 하는 방법은 다음과 같습니다.
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 이 코드에서 업데이트`"HueSaturationAdjustmentLayer.psd"` 편집하려는 기존 PSD 파일의 이름으로 변경하세요.
## 3단계: 색조/채도 레이어 편집
다음으로 로드된 PSD 이미지의 레이어를 반복하여 기존 색조/채도 레이어를 찾아 편집하겠습니다. 이 단계에는 색조, 채도 및 밝기 값을 수정하는 작업이 포함됩니다.
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
이 예에서는 다음과 같습니다.
- 색조를 -25로, 채도를 -12로, 밝기를 +67로 조정합니다.
-  그만큼`getRange(2)` 방법을 사용하면 원하는 대로 특정 색상 범위를 조정할 수 있습니다.
## 4단계: 수정된 PSD 파일 저장
조정 후 다음 단계는 파일을 저장하는 것입니다. 이는 변경 사항이 손실되지 않도록 하는 프로세스의 중요한 부분입니다.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## 5단계: 새 색조/채도 레이어 추가
다음으로 다른 PSD 파일에 새로운 색조/채도 조정 레이어를 추가할 수 있습니다. 이전에 사용한 것과 동일한 접근 방식을 따르지만 다른 PSD 파일을 사용하면 됩니다.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## 6단계: 새 레이어에 대한 새 색조/채도 값 설정
이제 이 새 레이어를 만들었으므로 이전과 마찬가지로 원하는 색조, 채도 및 밝기 설정을 적용합니다.
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
## 7단계: 업데이트된 PSD 파일 저장
마지막으로 Hue/Saturation 레이어가 추가된 PSD 파일을 저장하여 변경 사항을 확인할 수 있습니다.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
축하해요! Java용 Aspose.PSD를 사용하여 PSD 파일을 성공적으로 조작했습니다. 이제 다양한 이미지와 심층적인 변경을 실험하여 그래픽 디자인 프로젝트에 생기를 불어넣을 수 있습니다.
## 결론
프로그래밍 방식으로 그래픽 작업을 하면 가능성의 세계가 열립니다. Java용 Aspose.PSD를 사용하여 색조 채도 조정 레이어를 추가하고 수정하면 디자인 작업 흐름을 간소화할 수 있는 유연성과 효율성이 제공됩니다. 프로젝트를 위해 사진을 향상시키거나 놀라운 시각적 콘텐츠를 생성하든 이러한 도구를 익히면 결과물을 크게 향상시킬 수 있습니다.
 Aspose.PSD의 더 많은 기능을 탐색해 보세요.[선적 서류 비치](https://reference.aspose.com/psd/java/) 아니면 걸림돌을 고려해보세요[임시면허](https://purchase.aspose.com/temporary-license/) 라이브러리의 모든 기능을 테스트합니다.
## FAQ
### 색조 채도 조정 레이어란 무엇입니까?
색조 채도 조정 레이어를 사용하면 원본 픽셀을 영구적으로 변경하지 않고도 이미지의 색상 속성을 수정할 수 있습니다.
### Aspose.PSD를 사용하려면 Photoshop을 설치해야 합니까?
아니요, Aspose.PSD는 Photoshop과 독립적으로 작동하는 독립형 라이브러리입니다.
### 일괄 처리에 Aspose.PSD를 사용할 수 있나요?
예, Aspose.PSD를 사용하면 여러 PSD 파일을 자동화하고 일괄 처리할 수 있습니다.
### Aspose.PSD는 무료인가요?
Aspose.PSD는 무료 평가판을 제공하지만 장기간 사용하려면 라이센스가 필요합니다. 가격을 보실 수 있습니다[여기](https://purchase.aspose.com/buy).
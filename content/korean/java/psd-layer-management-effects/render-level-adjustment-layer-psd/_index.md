---
title: PSD 파일의 렌더링 레벨 조정 레이어 - Java
linktitle: PSD 파일의 렌더링 레벨 조정 레이어 - Java
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 이미지 대비와 생동감을 손쉽게 향상시키는 방법을 알아보세요. 이 단계별 가이드를 통해 마스터 레벨 조정 레이어를 알아보세요.
type: docs
weight: 17
url: /ko/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---
## 소개

대비나 생동감이 부족한 이미지를 찾기 위해 PSD 파일을 연 적이 있습니까? 두려워하지 마세요, 이미지 편집 전사 여러분! Java용 Aspose.PSD는 강력한 레벨 조정 레이어 조작 기능을 통해 구출됩니다. 이 가이드는 레벨을 사용하여 이미지를 쉽게 미세 조정할 수 있는 지식을 제공합니다. 

## 전제조건

- JDK(Java Development Kit): 시스템에 최신 버전의 JDK가 설치되어 있는지 확인하십시오. Oracle 웹사이트([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Java 라이브러리용 Aspose.PSD: 다운로드 페이지([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). 전체 기능을 사용하려면 유효한 라이센스가 필요하지만 시작하려면 무료 평가판을 사용할 수 있습니다([https://releases.aspose.com/](https://releases.aspose.com/)).

## 패키지 가져오기

코드를 살펴보기 전에 PSD 파일과 상호 작용하는 데 필요한 Aspose.PSD 클래스를 가져와야 합니다. 필요한 것은 다음과 같습니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 그만큼`com.aspose.psd` 패키지는 PSD 조작 기능에 대한 액세스를 제공하는 반면`com.aspose.psd.imaging.PngOptions` 이미지를 PNG로 저장할 때 옵션을 정의할 수 있습니다.

이제 레벨 조정 모험을 시작해 보겠습니다.

## 1단계: 파일 경로 설정:

- 문서 디렉터리에 대한 변수를 정의합니다(`dataDir`), 소스 PSD 파일 이름(`sourceFileName`), 수정 후 대상 PSD 파일 이름(`psdPathAfterChange`) 및 최종 PNG 내보내기 경로(`pngExportPath`). 코드 가독성을 높이려면 설명이 포함된 이름을 사용하는 것이 좋습니다.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## 2단계: PSD 이미지 로드:

-  사용`Image.load` 소스 PSD 파일을 열고 저장하는 방법`PsdImage`물체 (`im`). Aspose.PSD는 파일 형식을 자동으로 감지합니다.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## 3단계: 레이어 반복:

- PSD 내에서 레벨 조정 레이어를 찾아야 합니다. Aspose는 루프를 사용하여 모든 레이어를 반복하는 편리한 방법을 제공합니다.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (레벨 레이어를 확인하는 코드가 여기에 추가됩니다)
}
```

## 4단계: 레벨 레이어 식별:

- 루프 내부에서 현재 레이어(`im.getLayers()[i]` )는`LevelsLayer` 을 사용하는 수업`instanceof` 연산자. 
-  그렇다면 레이어를`LevelsLayer` 추가 조작에 대한 이의를 제기합니다.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (레벨을 조정하는 코드가 여기에 추가됩니다)
   }
}
```
## 5단계: 레벨 미세 조정(계속):

-  다음을 사용하여 출력 레벨을 조정합니다.`setOutputShadowLevel` 그리고`setOutputHighlightLevel` 결과 이미지의 어두움과 밝기를 제어합니다. 이 값은 출력 범위에 매핑될 입력 레벨의 범위를 결정합니다.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // 입력 레벨 조정(0-255):
	   channel.setInputShadowLevel((short) 10); // 그림자를 약간 어둡게 합니다.
	   channel.setInputMidtoneLevel(2.0f);     // 중간톤 증가
	   channel.setInputHighlightLevel((short) 230); // 하이라이트 줄이기

	   // 출력 레벨 조정(0-255):
	   channel.setOutputShadowLevel((short) 20); // 그림자를 더 어둡게 하세요
	   channel.setOutputHighlightLevel((short) 200); //하이라이트를 밝게
   }
}
```

## 6단계: 수정된 PSD 저장:

-  사용`save` 의 방법`PsdImage` 수정된 이미지를 지정된 경로(`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## 7단계: PNG로 내보내기(선택 사항):

-  조정된 이미지의 PNG 버전이 필요한 경우`PngOptions` 개체를 선택하고 색상 유형을 다음으로 설정합니다.`TruecolorWithAlpha` . 그런 다음`save` PNG 내보내기 경로 및 옵션을 사용하여 다시 메서드를 사용합니다.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

그리고 거기에 있습니다! Java용 Aspose.PSD를 사용하여 PSD 파일에서 레벨 조정 레이어를 성공적으로 조정했습니다. 이러한 단계를 이해하고 다양한 값을 실험해 보면 이미지의 대비와 전체적인 모양을 향상시킬 수 있습니다.

## 결론

Java용 Aspose.PSD를 사용하면 이미지 편집 프로세스를 제어할 수 있습니다. 레벨 조정 레이어를 마스터하면 사진과 디자인에 새로운 생명을 불어넣을 수 있습니다. 연습이 완벽함을 만든다는 점을 기억하십시오. 따라서 이 강력한 도구의 잠재력을 최대한 활용하고 실험하는 것을 주저하지 마십시오.
 
## FAQ

### 개별 색상 채널(RGB)을 별도로 조정할 수 있나요? 
예, 다음을 사용하여 각 색상 채널에 액세스할 수 있습니다.`getChannel` 의 방법`LevelsLayer` 개체를 만들고 해당 레벨을 독립적으로 수정합니다.

### PSD에서 여러 레벨 조정 레이어를 어떻게 처리합니까?
코드는 모든 레이어를 반복하므로 이미지에 있는 추가 레벨 레이어를 자동으로 처리합니다.

### 레벨 외에 이미지 대비를 조정하는 다른 방법이 있습니까?
전적으로! Aspose.PSD는 곡선, 밝기/대비 등과 같은 다양한 이미지 조정 도구를 제공합니다.

### 여러 이미지에 대해 이 프로세스를 자동화할 수 있나요? 
예, 이 코드를 루프 또는 일괄 처리 스크립트에 통합하여 여러 PSD 파일을 효율적으로 처리할 수 있습니다.

### 자세한 정보와 지원은 어디서 찾을 수 있나요?
Aspose는 광범위한 문서를 제공합니다([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) 및 지원 포럼([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) 발생할 수 있는 질문이나 문제에 대해 문의해 주세요.
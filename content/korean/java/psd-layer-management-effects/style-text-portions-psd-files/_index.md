---
title: Java를 사용하여 PSD 파일의 텍스트 부분 스타일 지정
linktitle: Java를 사용하여 PSD 파일의 텍스트 부분 스타일 지정
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 텍스트 스타일을 마스터하세요. 텍스트 부분을 손쉽게 수정, 생성 및 스타일 지정하는 방법을 알아보세요. PSD 디자인을 향상시키세요.
type: docs
weight: 22
url: /ko/java/psd-layer-management-effects/style-text-portions-psd-files/
---
## 소개

PSD 파일의 텍스트 레이어에 추가적인 매력을 추가하고 싶었던 적이 있습니까? Java용 Aspose.PSD는 텍스트를 조작할 뿐만 아니라 개별 부분의 스타일을 놀라울 정도로 정밀하게 지정할 수 있는 기능을 제공합니다. 이 포괄적인 가이드는 환경 설정부터 PSD 내에서 멋진 스타일의 텍스트 요소를 만드는 것까지 프로세스를 단계별로 안내합니다.

## 전제조건

자세히 알아보기 전에 다음 사항이 있는지 확인하세요.

- JDK(Java Development Kit): 우리가 탐색할 코드를 실행하려면 시스템에 JDK가 설치되어 있어야 합니다. Java 웹사이트([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)) 다운로드 및 설치 지침을 확인하세요.
- Aspose.PSD for Java Library: 이 라이브러리를 사용하면 PSD 파일과 프로그래밍 방식으로 상호 작용할 수 있습니다. Aspose 웹사이트([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)라이브러리를 다운로드합니다. 전체 기능을 사용하려면 라이선스가 필요하지만 시작하려면 무료 평가판을 사용할 수 있습니다.

## 패키지 가져오기

모든 설정이 완료되면 즐겨 사용하는 Java IDE를 열고 코딩을 시작해 보겠습니다. 첫 번째 단계는 Java용 Aspose.PSD에서 필요한 패키지를 가져오는 것입니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.fileformats.psd.layers.text.IText;
import com.aspose.psd.fileformats.psd.layers.text.ITextParagraph;
import com.aspose.psd.fileformats.psd.layers.text.ITextPortion;
import com.aspose.psd.fileformats.psd.layers.text.ITextStyle;
import com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline;
import com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps;
```

이러한 가져오기를 통해 PSD 파일 작업에 필요한 클래스와 기능에 액세스할 수 있습니다.

이제 진짜 마법에 빠져봅시다! 다음은 PSD 파일 내의 텍스트 부분 스타일 지정과 관련된 단계에 대한 설명입니다.

## 1단계: PSD 파일 로드

먼저 수정하려는 텍스트 레이어가 포함된 PSD 파일을 로드해야 합니다. 수행 방법은 다음과 같습니다.

```java
String sourceDir = "yourSourceDirectory";
String inPsdFilePath = sourceDir + "text212.psd";

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

이 코드 조각은 소스 PSD 파일의 경로를 정의합니다(`inPsdFilePath` ) 그런 다음`Image.load` 파일을 로드하는 방법`PsdImage` 물체.

## 2단계: 텍스트 레이어에 접근하기

PSD 파일에는 다양한 유형의 레이어가 포함될 수 있습니다. 구체적으로 텍스트 작업을 하려면 텍스트 레이어 개체에 액세스해야 합니다. 방법은 다음과 같습니다.

```java
TextLayer textLayer = (TextLayer)psdImage.getLayers()[1];
```

이 코드는 첫 번째 레이어(`psdImage.getLayers()[1]`). PSD 파일의 레이어 순서는 다를 수 있으므로 텍스트 레이어가 다른 위치에 있는 경우 그에 따라 색인을 조정하십시오.

## 3단계: 텍스트 데이터 작업

 그만큼`TextLayer` 개체는 텍스트 내용과 서식에 대한 모든 정보를 보유합니다. 우리는 다음을 통해 이 정보에 접근할 수 있습니다.`getTextData` 방법:

```java
IText textData = textLayer.getTextData();
```

 그만큼`IText`물체 (`textData`)은 레이어의 텍스트 내용을 나타냅니다. 텍스트 자체와 스타일을 조작하는 기능을 제공합니다.

## 4단계: 기본 스타일 정의(선택 사항)

꼭 필요한 것은 아니지만 텍스트와 단락의 기본 스타일을 정의하면 작업 흐름을 간소화할 수 있습니다. 이를 통해 특정 부분에 대해 쉽게 재정의할 수 있는 기준 스타일을 설정할 수 있습니다.

```java
ITextStyle defaultStyle = textData.producePortion().getStyle();
defaultStyle.setFillColor(Color.getDimGray());
defaultStyle.setFontSize(51);

ITextParagraph defaultParagraph = textData.producePortion().getParagraph();
```

 이 코드는 새로운`ITextStyle`물체 (`defaultStyle` ) 채우기 색상 및 글꼴 크기와 같은 속성을 설정합니다. 마찬가지로, 새로운`ITextParagraph`물체 (`defaultParagraph`)는 기본 단락 설정을 정의하기 위해 생성됩니다.

## 5단계: 기존 텍스트 부분 스타일 지정

레이어 내 기존 텍스트의 특정 부분에 취소선 효과를 추가한다고 가정해 보겠습니다. 이를 달성하는 방법은 다음과 같습니다.

```java
textData.getItems()[1].getStyle().setStrikethrough(true);
```

이 코드는 두 번째 텍스트 부분(`textData.getItems()[1]` ) 그리고 이를 설정합니다.`strikethrough`재산`true` . 마찬가지로 다른 부분에 액세스하고 다음에서 제공하는 다양한 방법을 사용하여 해당 스타일을 수정할 수 있습니다.`ITextStyle` 인터페이스.

## 6단계: 스타일을 사용하여 새 텍스트 부분 만들기

처음부터 특정 스타일이 적용된 새로운 텍스트 요소를 추가하고 싶으십니까? Java용 Aspose.PSD를 사용하면 그렇게 할 수도 있습니다!

```java
String[] newTextStrings = {"E=mc2", "Bold", "Italic", "Lowercasetext"};
ITextPortion[] newTextPortions = textData.producePortions(newTextStrings, defaultStyle, defaultParagraph);
```

이 코드는 문자열 배열(`newTextStrings` ) 새 부분에 대한 텍스트 내용이 포함되어 있습니다. 그런 다음 사용합니다.`textData.producePortions` 배열을 생성하려면`ITextPortion` 객체, 적용`defaultStyle` 그리고`defaultParagraph` 각 부분에.

## 7단계: 새 텍스트 부분 사용자 정의

새 텍스트 부분이 있으면 개별 부분에 특정 스타일을 적용할 수 있습니다.

```java
newTextPortions[0].getStyle().setUnderline(true); // "E=mc2"에 밑줄을 긋습니다.
newTextPortions[1].getStyle().setFauxBold(true); // "굵게"에 대해 굵게 표시
newTextPortions[2].getStyle().setFauxItalic(true); // "기울임체"에 대한 이탤릭체
newTextPortions[3].getStyle().setFontCaps(FontCaps.SmallCaps); //"소문자 텍스트"에 대한 작은 대문자
```

여기서는 처음 세 개의 새로운 텍스트 부분의 스타일을 사용자 정의합니다. 요구사항에 따라 다양한 스타일링 옵션을 적용할 수 있습니다.

## 8단계: 레이어에 새 텍스트 부분 추가

새 텍스트 부분을 사용자 정의한 후 텍스트 레이어에 추가해야 합니다.

```java
for (ITextPortion newTextPortion : newTextPortions) {
    textData.addPortion(newTextPortion);
}
```

 이 코드는`newTextPortions` 배열하고 각 부분을`textData` 물체.

## 9단계: 레이어에 변경 사항 적용

PSD 레이어의 텍스트 데이터에 대한 수정 사항을 반영하려면 레이어를 업데이트해야 합니다.

```java
textData.updateLayerData();
```

 이 호출은`textLayer` 변경된 내용으로`textData`.

## 10단계: 수정된 PSD 파일 저장

마지막으로 수정된 PSD 파일을 새 위치에 저장합니다.

```java
String outputDir = "yourOutputDirectory";
String outPsdFilePath = outputDir + "Output_text212.psd";

psdImage.save(outPsdFilePath);
```

 이 코드는 출력 파일 경로를 생성하고`psdImage` 지정된 위치로 개체를 이동합니다.

## 결론

그리고 거기에 있습니다! Java용 Aspose.PSD를 사용하여 PSD 파일 내 텍스트 부분의 스타일을 성공적으로 지정했습니다. 다음 단계를 수행하고 사용 가능한 다양한 스타일 옵션을 탐색하면 PSD에 시각적으로 매력적이고 사용자 정의된 텍스트 요소를 만들 수 있습니다.

기억하세요, 이것은 단지 시작점일 뿐입니다. Aspose.PSD for Java는 고급 서식 지정, 단락 제어 등을 포함하여 텍스트 조작을 위한 광범위한 기능을 제공합니다. 실험하고 창의력을 발휘하여 원하는 결과를 얻으세요!

## FAQ

### 특정 텍스트 부분의 글꼴을 변경할 수 있나요?
 예, 다음을 사용하여 텍스트 부분의 글꼴을 변경할 수 있습니다.`setFontName` 의 방법`ITextStyle` 물체.

### 단락 내에서 텍스트 정렬을 어떻게 조정합니까?
 그만큼`ITextParagraph` 객체는 다음과 같은 속성을 제공합니다.`setAlignment` 단락 내의 텍스트 정렬을 제어합니다.

### 텍스트의 문자 간격을 수정할 수 있나요?
 예, 다음을 사용하여 문자 간격을 조정할 수 있습니다.`setCharacterSpacing` 의 방법`ITextStyle` 물체.

### 단일 텍스트 부분의 다른 부분에 다른 스타일을 적용할 수 있나요?
직접적으로 지원되지는 않지만 동일한 전체 부분 내에 여러 텍스트 부분을 만들어 비슷한 효과를 얻을 수 있습니다.

### 처리할 수 있는 텍스트 부분이나 문자 수에 제한이 있나요?
실제 제한 사항은 시스템 리소스와 PSD 파일의 복잡성에 따라 달라집니다. 그러나 Java용 Aspose.PSD는 대용량 PSD 파일을 효율적으로 처리하도록 설계되었습니다.
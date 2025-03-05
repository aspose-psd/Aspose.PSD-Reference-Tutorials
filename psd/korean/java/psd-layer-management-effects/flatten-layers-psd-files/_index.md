---
title: Aspose.PSD Java를 사용하여 PSD 파일의 레이어 병합
linktitle: Aspose.PSD Java를 사용하여 PSD 파일의 레이어 병합
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일의 레이어를 쉽게 병합하고 병합할 수 있습니다. PSD 파일 관리를 단순화하려면 이 단계별 가이드를 따르십시오.
type: docs
weight: 13
url: /ko/java/psd-layer-management-effects/flatten-layers-psd-files/
---
## 소개

Photoshop 파일로 작업하면서 복잡한 레이어를 더 쉽게 관리할 수 있는 방법을 원한 적이 있습니까? 글쎄, 당신은 운이 좋다! 오늘 우리는 PSD 파일을 프로그래밍 방식으로 쉽게 작업할 수 있게 해주는 강력한 도구인 Java용 Aspose.PSD의 세계에 대해 알아봅니다. 우리가 살펴볼 편리한 기능 중 하나는 레이어를 병합하는 것입니다. 전체 이미지를 병합하려는 경우나 특정 레이어를 선택적으로 병합하려는 경우 Java용 Aspose.PSD를 사용하면 됩니다. 이 튜토리얼에서는 프로세스를 단계별로 안내하여 PSD 파일을 자신 있게 다룰 수 있도록 준비합니다.

## 전제조건

코드를 시작하기 전에 필요한 모든 것이 있는지 확인하겠습니다.

1. JDK(Java Development Kit): 시스템에 JDK 8 이상이 설치되어 있는지 확인하십시오.
2.  Java용 Aspose.PSD: Aspose.PSD 라이브러리를 다운로드하여 프로젝트에 추가하세요. 당신은 그것을 찾을 수 있습니다[여기](https://releases.aspose.com/psd/java/).
3. 통합 개발 환경(IDE): IntelliJ IDEA 또는 Eclipse와 같은 IDE는 코딩 경험을 더욱 원활하게 만들어줍니다.
4. Java 기본 지식: 이 튜토리얼은 초보자에게 적합하지만 Java에 대한 몇 가지 기본 지식이 있으면 더 쉽게 따라갈 수 있습니다.
5. 샘플 PSD 파일: 실험할 PSD 파일을 준비합니다. 평탄화 프로세스를 보여주기 위해 여러 레이어가 있는 레이어를 사용하겠습니다.

이제 필수 사항을 모두 마쳤으므로 재미있는 부분인 코드 작업을 시작해 보겠습니다.

## 패키지 가져오기

시작하려면 필요한 패키지를 Java 프로젝트로 가져와야 합니다. 이 패키지를 사용하면 Java용 Aspose.PSD를 사용하여 PSD 파일로 작업할 수 있습니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

이러한 가져오기를 통해 PSD 파일을 로드하고, 레이어를 조작하고, 변경 사항을 저장할 수 있습니다. 이제 레이어를 병합하는 프로세스를 관리 가능한 단계로 나누어 보겠습니다.

## 1단계: 전체 PSD 이미지 병합

첫 번째 작업은 전체 PSD 이미지를 병합하는 것입니다. 이는 모든 레이어를 단일 레이어로 결합하여 이미지를 더 쉽게 관리하고 내보내려는 경우에 유용합니다.

### 1.1 PSD 파일 로드

 먼저 PSD 파일을 프로그램에 로드합니다. 이 파일은 프로젝트 디렉터리에 있어야 합니다.`Your Document Directory`.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

이 코드 조각은 다음과 같은 PSD 파일을 로드합니다.`ThreeRegularLayersSemiTransparent.psd` 지정된 디렉토리에서.

### 1.2 이미지 병합

다음으로 전체 이미지를 병합하겠습니다. 병합은 표시되는 모든 레이어를 단일 배경 레이어로 결합합니다.

```java
im.flattenImage();
```

이 단일 라이너를 사용하면 PSD 파일의 모든 레이어가 하나로 병합됩니다.

### 1.3 병합된 이미지 저장

마지막으로 병합된 이미지를 새 파일에 저장하겠습니다.

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

 이렇게 하면 병합된 PSD 파일이 새 이름으로 저장됩니다.`ThreeRegularLayersSemiTransparentFlattened.psd`. 축하해요! Java용 Aspose.PSD를 사용하여 첫 번째 PSD 이미지를 평면화했습니다.

## 2단계: 특정 레이어 병합

때로는 전체 이미지를 병합하지 않고 특정 레이어만 병합하고 싶을 수도 있습니다. 어떻게 이를 달성할 수 있는지 살펴보겠습니다.

### 2.1 PSD 파일 다시 로드

다른 작업을 수행하고 있으므로 PSD 파일을 다시 로드하여 시작하세요.

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

그러면 레이어별 작업에 사용할 준비가 된 동일한 PSD 파일이 로드됩니다.

### 2.2 레이어 식별 및 선택

특정 레이어를 병합하려면 먼저 병합할 레이어를 식별하고 선택하세요.

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

여기서는 PSD 파일의 첫 번째, 두 번째, 세 번째 레이어를 선택합니다. 이러한 레이어는 배열에 저장되며 해당 인덱스를 통해 액세스할 수 있습니다.

### 2.3 레이어 병합

이제 선택한 레이어를 병합해 보겠습니다. 먼저 아래쪽 레이어와 중간 레이어를 병합한 다음 결과를 위쪽 레이어와 병합하겠습니다.

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

이 코드는 레이어를 순차적으로 병합하여 단일 결합 레이어를 만듭니다.

### 2.4 기존 레이어를 병합된 레이어로 교체

병합 후에는 이미지의 기존 레이어를 새로 병합된 레이어로 교체해야 합니다.

```java
img.setLayers(new Layer[]{layer2});
```

이 단계를 수행하면 이제 이미지에 병합된 레이어만 포함됩니다.

### 2.5 업데이트된 PSD 파일 저장

마지막으로 병합된 레이어와 함께 업데이트된 PSD 파일을 저장합니다.

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

이렇게 하면 병합된 레이어와 함께 PSD가 새 이름으로 저장되므로 원본 파일을 그대로 유지할 수 있습니다.

## 결론

PSD 파일의 레이어 작업은 종종 미로를 탐색하는 것처럼 느껴질 수 있지만 Java용 Aspose.PSD를 사용하면 손에 지도를 들고 있는 것과 같습니다. 전체 이미지를 병합해야 하거나 선택한 레이어를 신중하게 병합해야 하는 경우 Aspose.PSD는 프로세스를 단순화하여 어려운 작업을 간단한 작업으로 전환합니다. 이 튜토리얼을 따르면 이제 Java를 사용하여 PSD 파일의 레이어 조작을 편안하게 처리할 수 있습니다. 그렇다면 여러분 자신의 프로젝트로 시도해 보고 얼마나 많은 시간과 노력을 절약하는지 확인해 보는 것은 어떨까요?

## FAQ

### Aspose.PSD에서 레이어 병합을 취소할 수 있나요?  
아니요. Aspose.PSD를 사용하여 레이어를 병합하면 해당 작업을 되돌릴 수 없습니다. 항상 원본 파일의 백업을 보관하는 것이 좋습니다.

### 보이는 레이어만 병합할 수 있나요?  
 예, 가시성에 따라 어떤 레이어를 병합할지 제어할 수 있습니다. 사용하기 전에 병합하려는 레이어만 표시되는지 확인하세요.`flattenImage` 방법.

### 레이어를 병합하면 파일 크기가 줄어듭니까?  
레이어를 병합하면 특히 복잡한 레이어가 많은 경우 파일 크기를 줄일 수 있습니다. 그러나 정확한 감소량은 레이어의 내용에 따라 달라집니다.

### 다양한 혼합 모드로 레이어를 병합할 수 있나요?  
예, Aspose.PSD를 사용하여 다양한 혼합 모드로 레이어를 병합할 수 있으며 결과 레이어는 병합된 레이어의 모양을 유지합니다.

### 인접하지 않은 레이어를 병합하려고 하면 어떻게 되나요?  
Aspose.PSD를 사용하면 레이어 스택의 순서에 관계없이 모든 레이어를 병합할 수 있습니다. 병합 프로세스는 선택한 레이어를 지정된 대로 결합합니다.
---
title: Java를 사용하여 PSD 파일에 조정 레이어 적용
linktitle: Java를 사용하여 PSD 파일에 조정 레이어 적용
second_title: Aspose.PSD 자바 API
description: 개발자를 위한 이 완전한 단계별 가이드에서 Java용 Aspose.PSD를 사용하여 PSD 파일에 조정 레이어를 적용하는 방법을 알아보세요.
type: docs
weight: 15
url: /ko/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---
## 소개
PSD 파일에 저장된 이미지를 향상시키려는 Java 개발자이신가요? 그렇다면, 당신은 바로 이곳에 있습니다! 이 기사에서는 Java용 Aspose.PSD 라이브러리를 사용하여 PSD 파일에 조정 레이어를 적용하는 방법을 살펴보겠습니다. 개인 프로젝트에서 작업하든 전문 응용 프로그램에서 작업하든 PSD 파일을 조작하는 방법을 이해하면 소프트웨어 기능을 크게 향상시킬 수 있습니다. 

## 전제조건
코드로 이동하여 해당 조정 레이어 적용을 시작하기 전에 필요한 몇 가지 전제 조건이 있습니다.
1. JDK(Java Development Kit): 컴퓨터에 JDK가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[오라클의 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD 라이브러리: 아직 다운로드하지 않았다면 Java용 Aspose.PSD 라이브러리를 다운로드해야 합니다. 당신은 그것을 찾을 수 있습니다[여기](https://releases.aspose.com/psd/java/).
3. 개발 환경: 코드를 작성하고 실행할 IntelliJ IDEA 또는 Eclipse와 같은 Java 통합 개발 환경(IDE)을 설정합니다.
4. Java에 대한 기본 지식: Java 프로그래밍에 대한 일반적인 이해는 원활하게 진행하는 데 도움이 됩니다.
5. PSD 파일: 테스트 목적으로 두 개의 PSD 파일을 준비하십시오. Adobe Photoshop을 사용하여 일부를 만들거나 인터넷에서 샘플 파일을 다운로드할 수 있습니다.
## 패키지 가져오기
코딩을 시작하기 전에 어떤 패키지를 가져와야 하는지 명확히 하겠습니다. Aspose.PSD를 사용하면 다양한 방법으로 Photoshop 파일을 사용할 수 있으므로 PSD 이미지 및 조정 레이어를 처리하는 데 필요한 클래스를 살펴보겠습니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
이제 패키지가 준비되었으므로 예제를 단계별로 분석해 보겠습니다.
## 1단계: PSD 파일 로드
여정의 첫 번째 단계는 PSD 파일을 로드하는 것입니다. 이것은 조정 레이어를 적용하기 위해 작업할 파일입니다.
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
 이 코드 조각에서는 PSD 파일이 있는 디렉터리를 정의하고 조작하려는 특정 파일을 로드합니다. 꼭 교체하세요`"Your Document Directory"` 컴퓨터에 있는 PSD 파일의 실제 경로를 사용하세요.
## 2단계: 레이어 반복
이제 PSD 파일을 로드했으므로 해당 레이어를 반복하여 조정 레이어를 찾습니다.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
 이 단계에서는 PSD 파일의 각 레이어를 반복하여 다음과 같은 레이어를 식별합니다.`AdjustmentLayer` 유형. 하나를 찾으면 일반적으로 첫 번째 레이어인 기본 레이어(`im.getLayers()[0]`). 이 병합 프로세스는 조정 내용을 이미지에 효과적으로 적용합니다. 
## 3단계: 수정된 PSD 파일 저장
레이어를 수정한 후에는 변경 사항을 저장하는 것이 중요합니다. 다음 단계에서 이 작업을 수행하겠습니다.
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
 여기에서는 수정된 PSD 파일의 내보내기 경로를 지정하고`save()` 변경 사항을 디스크에 기록하는 방법입니다.
## 4단계: 레벨 조정 레이어
다른 유형의 조정 레이어인 레벨 조정 레이어에 대해 프로세스를 반복해 보겠습니다. 
### 레벨 조정 레이어 PSD 로드
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
이전과 마찬가지로 레벨 조정 레이어가 포함된 PSD 파일을 로드합니다. 
### 레벨 레이어를 통해 반복
다음으로 이전과 마찬가지로 레이어를 다시 반복하지만 이제는 다른 PSD 파일을 사용하여 작업합니다.
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
이 코드는 이전 반복과 유사하게 작동합니다. 현재 PSD 파일 내에서 조정 레이어를 검색하여 사용 가능한 모든 조정을 적용할 수 있습니다.
## 레벨 조정 레이어 PSD 저장
마지막으로 조정 사항을 적용한 후 이 새 파일을 저장하겠습니다.
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
이제 레벨 조정 레이어를 성공적으로 처리했습니다!
## 결론
축하해요! Java 및 Aspose.PSD 라이브러리를 사용하여 PSD 파일에 조정 레이어를 적용하는 방법을 배웠습니다. 색상을 조정하든 레벨을 조정하든 이제 프로그래밍 방식으로 PSD 파일을 조작할 수 있는 기본 기술을 갖추게 되었습니다.
Aspose.PSD를 사용하면 이미지 편집 작업 흐름을 크게 간소화할 수 있어 기존 도구가 할 수 없는 방식으로 자동화 및 사용자 정의가 가능해집니다. 주저하지 말고 라이브러리를 더 자세히 살펴보고 다양한 유형의 레이어를 실험하여 어떤 창의적인 가능성이 있는지 확인하세요.
## FAQ
### Aspose.PSD 라이브러리란 무엇입니까?
Aspose.PSD는 개발자가 Java 애플리케이션에서 Photoshop PSD 파일을 로드, 조작 및 저장할 수 있는 라이브러리입니다.
### Aspose.PSD를 무료로 사용할 수 있나요?
 예! Aspose는 라이브러리를 탐색할 수 있는 무료 평가판을 제공합니다. 가입하실 수 있습니다[여기](https://releases.aspose.com/).
### Aspose.PSD를 사용하려면 Photoshop을 설치해야 합니까?
아니요, Photoshop이 필요하지 않습니다. Aspose.PSD는 프로그래밍 방식으로 PSD 파일을 조작하기 위해 독립적으로 작동합니다.
### Aspose.PSD에 대한 문서는 어디서 찾을 수 있나요?
문서 페이지를 방문할 수 있습니다.[여기](https://reference.aspose.com/psd/java/) 기능, 클래스 및 방법을 탐색합니다.
### Aspose 제품에 대한 지원은 어떻게 받나요?
 다음을 통해 지원에 액세스할 수 있습니다.[포럼을 Aspose](https://forum.aspose.com/c/psd/34) 질문을 하고 해결책을 찾을 수 있는 곳입니다.
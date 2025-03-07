---
title: PSD에 레벨 조정 레이어 추가
linktitle: PSD에 레벨 조정 레이어 추가
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일에 레벨 조정 레이어를 효과적으로 추가하는 방법을 알아보세요. 이미지 편집 기술을 향상해보세요.
weight: 16
url: /ko/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD에 레벨 조정 레이어 추가

## 소개
이미지 편집의 경우 레벨을 관리하면 사진의 생동감과 선명도가 크게 달라질 수 있습니다. Photoshop 무기고에 있는 편리한 도구 중 하나는 이미지의 색조 범위와 색상 균형을 조정할 수 있는 "레벨 조정 레이어"입니다. 이 가이드에서는 Java용 Aspose.PSD를 사용하여 PSD 파일에 레벨 조정 레이어를 구현하는 방법을 안내합니다. 이제 Java IDE를 구입하세요.
## 전제조건
레벨 조정의 세계로 뛰어들기 전에 원활한 라이딩을 보장하기 위해 몇 가지 사항을 설정해야 합니다.
1.  JDK(Java Development Kit): 컴퓨터에 JDK가 설치되어 있는지 확인하세요. 없으시면 에서 가져가시면 됩니다[오라클 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 또는 OpenJDK를 사용하세요.
2.  Java 라이브러리용 Aspose.PSD: PSD 파일을 조작하려면 Aspose.PSD 라이브러리를 다운로드해야 합니다. 여기에서 최신 버전을 얻을 수 있습니다[다운로드 링크](https://releases.aspose.com/psd/java/) 프로젝트 라이브러리에 JAR이 포함되어 있는지 확인하세요.
3. Java에 대한 기본 지식: 이 튜토리얼 전체에서 코드 조각을 자세히 알아볼 것이므로 Java 프로그래밍에 대한 기본적인 이해가 있으면 도움이 됩니다.
4. IDE 설정: IntelliJ IDEA, Eclipse, NetBeans 등 원하는 Java IDE를 사용하여 코드를 작성하고 실행할 수 있습니다. Java 프로젝트를 설정하고 Aspose.PSD 라이브러리를 추가했는지 확인하세요.

## 패키지 가져오기
코드 작성을 시작하기 전에 Aspose.PSD 라이브러리에서 필요한 패키지를 가져와야 합니다. 방법은 다음과 같습니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
이러한 패키지를 가져오면 PSD 파일을 로드, 수정 및 저장하는 데 필요한 클래스에 액세스할 수 있습니다.

이제 프로세스를 소화 가능한 단계로 나누어 보겠습니다. PSD 파일을 로드하고, 레벨을 조정하고, 변경 사항을 저장하는 과정을 따라해보세요. 
## 1단계: 파일 경로 설정
첫 번째 단계는 PSD 파일의 위치와 수정된 출력을 저장할 위치를 정의하는 것입니다. 필요에 맞게 디렉터리 경로를 사용자 정의할 수 있습니다.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 여기서 교체하세요`"Your Document Directory"`PSD 파일이 저장된 시스템의 실제 경로를 사용하세요. 이것은 우리가 다음에 할 모든 일의 무대를 설정합니다.
## 2단계: PSD 파일 로드
 이제 다음을 사용하여 PSD 파일을 로드해 보겠습니다.`PsdImage` 수업. 이 단계는 레이어에 접근하고 조작할 수 있게 해주기 때문에 필수적입니다.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 당신이 전화할 때`Image.load()` , PSD 파일을 읽고 다음 인스턴스를 생성합니다.`PsdImage` 당신이 함께 일할 수 있는 것입니다.
## 3단계: 레이어를 통해 반복
레벨 조정 레이어를 조정하고 싶기 때문에 PSD 파일의 각 레이어를 반복해야 합니다. 이는 수정하려는 특정 레이어를 찾는 데 도움이 됩니다.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // 여기서 추가 조작이 진행됩니다...
    }
}
```
 이 루프에서는`instanceof LevelsLayer` 현재 레이어가 레벨 조정 레이어인지 확인합니다. 그렇다면 해당 속성을 계속 조정할 수 있습니다.
## 4단계: 레벨 채널 설정 조정
올바른 레이어를 식별하면 해당 레이어의 입력 및 출력 레벨을 수정할 수 있습니다. 이곳이 바로 마법이 일어나는 곳입니다! 다양한 매개변수를 조정하여 이미지에 어떤 영향을 미치는지 확인하세요.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
각 매개변수의 역할은 다음과 같습니다.
- 입력 중간톤 레벨: 중간톤을 조정합니다.
- 입력 그림자 레벨: 이미지의 어두운 영역을 조정합니다.
- 입력 하이라이트 레벨: 이미지의 밝은 영역을 변경합니다.
- 출력 그림자 수준: 어두운 그림자가 나타나는 정도를 설정합니다.
- 출력 하이라이트 레벨: 밝은 하이라이트가 나타나는 방식을 설정합니다.
다양한 값을 자유롭게 실험해보세요!
## 5단계: 수정된 PSD 파일 저장
이제 조정을 마쳤으므로 수정된 PSD 파일을 저장할 차례입니다. 이 단계는 변경 사항을 적용하고 저장하는 데 중요합니다.
```java
im.save(psdPathAfterChange);
```
 이제 지정된 위치에서 조정된 PSD 파일을 찾을 수 있습니다.`psdPathAfterChange`. 
## 결론
Java용 Aspose.PSD를 사용하여 PSD 파일에 레벨 조정 레이어를 추가하는 방법을 배웠습니다! 이 가이드를 따르면 이미지의 색조 품질을 손쉽게 조정하여 더욱 생생하고 시각적으로 매력적인 출력을 위한 기반을 마련할 수 있습니다. 연습하면 완벽해진다는 점을 기억하세요. 자유롭게 조정 사항을 조정하고 다양한 PSD 파일을 탐색하여 변경 사항의 효과를 확인하세요.
## FAQ
### 레벨 조정 레이어란 무엇입니까?
레벨 조정 레이어를 사용하면 이미지의 색조 범위를 수정하고 그림자, 중간톤 및 하이라이트의 균형을 맞출 수 있습니다.
### 구매하지 않고도 Aspose.PSD를 사용할 수 있나요?
예! Aspose는 구매하기 전에 라이브러리를 테스트할 수 있는 무료 평가판을 제공합니다.
### Aspose.PSD에 대한 문서는 어디서 찾을 수 있나요?
 문서를 찾을 수 있습니다[여기](https://reference.aspose.com/psd/java/).
### Aspose 제품에 대한 커뮤니티 지원이 있나요?
 전적으로! 질문을 하고 지원을 받을 수 있습니다.[포럼을 Aspose](https://forum.aspose.com/c/psd/34).
### Aspose.PSD의 임시 라이센스를 어떻게 얻을 수 있나요?
 임시면허를 신청할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

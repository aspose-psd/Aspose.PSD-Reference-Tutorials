---
title: Java를 사용하여 PSD에서 노출 조정 레이어 관리
linktitle: Java를 사용하여 PSD에서 노출 조정 레이어 관리
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 Java로 손쉽게 PSD 이미지를 향상하세요. 노출 조정 레이어를 단계별로 관리하려면 이 가이드를 따르세요.
type: docs
weight: 23
url: /ko/java/psd-image-modification-conversion/manage-exposure-adjustment-layer-psd/
---
## 소개
Photoshop 파일을 프로그래밍 방식으로 작업할 때, 특히 이미지 편집이나 조작을 할 때 Java용 Aspose.PSD 라이브러리는 진정한 게임 체인저입니다. 활용할 수 있는 강력한 기능 중 하나는 노출 조정 레이어로, 이를 통해 이미지의 노출 설정을 간단하고 효과적으로 향상하거나 수정할 수 있습니다. 이 튜토리얼은 Java를 사용하여 PSD 파일 내의 노출 조정 레이어를 관리하는 모든 단계를 안내합니다.
## 전제조건
PSD 파일을 조작하는 흥미로운 여정을 시작하기 전에 몇 가지 설정이 필요합니다.
### 자바 환경
1.  JDK(Java Development Kit): 컴퓨터에 JDK가 설치되어 있는지 확인하세요. 그렇지 않은 경우 다음에서 다운로드하십시오.[오라클 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. 원하는 IDE: IntelliJ IDEA, Eclipse 또는 간단한 텍스트 편집기와 같은 IDE를 사용하여 Java 코드를 작성하세요.
3.  Aspose.PSD 라이브러리: Java용 Aspose.PSD 라이브러리가 필요합니다. 다음에서 다운로드할 수 있습니다.[Aspose 릴리스 페이지](https://releases.aspose.com/psd/java/).
4. Java에 대한 기본 지식: Java 프로그래밍에 대한 기본적인 이해는 이 튜토리얼에서 다루는 개념을 이해하는 데 큰 도움이 됩니다.
모든 설정이 완료되면 PSD 파일에 노출 조정 레이어를 추가, 수정 및 저장하는 핵심을 알아볼 수 있습니다!
## 패키지 가져오기
PSD 파일을 편집하기 전에 Aspose.PSD에서 제공하는 필수 패키지를 가져와야 합니다. 이를 수행하는 방법은 다음과 같습니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
```
이러한 가져오기를 통해 PSD 파일을 조작하는 데 필요한 핵심 기능에 액세스할 수 있습니다.
## 1단계: 문서 디렉토리 설정
 먼저 PSD 파일이 있는 디렉터리를 정의해 보겠습니다. 당신은 교체하고 싶어 할 것입니다`"Your Document Directory"` 로컬 디렉토리 경로로.
```java
String dataDir = "Your Document Directory";
```
여기서는 기본적으로 애플리케이션을 위한 작업 공간을 준비하고 있습니다. 이는 DIY 프로젝트를 시작하기 전에 워크스테이션을 설정하는 것과 같습니다. 모든 것이 딱 맞아야 합니다!
## 2단계: 편집을 위해 PSD 파일 로드
이제 노출을 조정하려는 PSD 파일을 로드해 보겠습니다. 우리는 다음과 같은 이름의 예제 파일을 사용하여 작업할 것입니다.`ExposureAdjustmentLayer.psd`. 
```java
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
이것이 바로 우리가 파일에 참여하는 순간입니다! 이는 책을 열고 페이지 속으로 뛰어들 준비를 하는 것과 같습니다. 각 레이어는 전해지기를 기다리는 이야기입니다.
## 3단계: 기존 노출 조정 레이어 수정
다음으로 PSD 파일의 각 레이어를 반복하여 노출 조정 레이어가 있는지 확인합니다. 하나를 찾으면 해당 속성을 수정하겠습니다!
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);
        expLayer.setOffset(-0.25f);
        expLayer.setGammaCorrection(0.5f);
    }
}
```
여기서 마법이 일어납니다. 완벽한 사운드를 얻기 위해 오래된 라디오의 다이얼을 조정하는 것과 같다고 생각하십시오. 이제 노출 수준을 조정하면 됩니다!
## 4단계: 수정된 PSD 파일 저장
 노출을 원하는 대로 조정한 후에는 편집된 파일을 저장할 차례입니다. 다른 이름으로 저장하겠습니다.`ExposureAdjustmentLayerChanged.psd`.
```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
방금 만든 완벽한 레시피를 저장하는 것과 같습니다. 이를 저장하면 모든 노력이 헛되지 않을 것입니다!
## 5단계: 새 노출 조정 레이어 추가
이제 기존 레이어를 수정했으므로 다른 PSD 파일에 새로운 노출 조정 레이어를 추가해 보겠습니다.`PhotoExample.psd`. 
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```
그림을 그릴 다른 캔버스를 고르는 것과 마찬가지로 또 다른 PSD 문서를 준비하고 있습니다!
## 6단계: 새 노출 레이어 구성
원하는 설정으로 새 노출 레이어를 만들고 구성하겠습니다.
```java
ExposureLayer newlayer = img.addExposureAdjustmentLayer(10, -0.25f, 2f);
```
이는 걸작에 새로운 페인트를 칠하는 것과 비슷합니다. 이미지를 강화하고 활력을 불어넣어 깊이와 개성을 더해줍니다.
## 7단계: 새 PSD 파일 저장
 마지막으로 새로 편집한 이미지를 다음과 같이 저장해 보겠습니다.`PhotoExampleAddedExposure.psd`.
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";
img.save(psdPathAfterChange);
```
그렇게 해서 우리는 새로운 창작물을 선보일 준비가 된 또 다른 프로젝트를 마무리했습니다!
## 결론
Aspose.PSD for Java를 사용하여 PSD 파일의 노출 조정 레이어를 관리하는 것은 효율적일 뿐만 아니라 그것은 힘을 실어줍니다. 창의적인 비전이 빛을 발하도록 하면서 기존 레이어를 수정하거나 새 레이어를 추가할 수도 있습니다. 위에 설명된 단계를 따르면 단 몇 줄의 코드만으로 이미지를 효과적으로 조작할 수 있습니다.
Aspose를 사용하여 이미지 관리 및 조작 가능성을 계속 탐색하면서 각 조정은 완벽한 이미지 제작을 향한 단계임을 기억하세요.
## FAQ
### Java용 Aspose.PSD란 무엇입니까?
Aspose.PSD for Java는 Photoshop 파일을 프로그래밍 방식으로 작업하여 레이어 조작, 렌더링 및 변환과 같은 기능을 활성화할 수 있는 라이브러리입니다.
### 웹 애플리케이션에서 Aspose.PSD를 사용할 수 있나요?
예, Aspose.PSD는 웹 애플리케이션에 통합되어 서버 측 이미지 조작이 가능합니다.
### Aspose.PSD를 사용하려면 라이센스가 필요한가요?
 예, 무료 평가판이 제공되지만 장기간 사용하려면 유효한 라이센스가 필요합니다. 임시면허를 취득할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD에 대한 지원은 어떻게 받을 수 있나요?
 Aspose 포럼에서 커뮤니티 지원에 액세스할 수 있습니다.[여기](https://forum.aspose.com/c/psd/34).
### 시작하는 데 사용할 수 있는 샘플 프로젝트가 있나요?
 예, 다음에서 샘플 프로젝트와 문서를 찾을 수 있습니다.[Aspose.PSD 참조 페이지](https://reference.aspose.com/psd/java/).
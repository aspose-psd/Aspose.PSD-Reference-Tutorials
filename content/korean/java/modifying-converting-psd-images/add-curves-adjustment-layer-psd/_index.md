---
title: Java를 사용하여 PSD에 곡선 조정 레이어 추가
linktitle: Java를 사용하여 PSD에 곡선 조정 레이어 추가
second_title: Aspose.PSD 자바 API
description: 이 자세한 튜토리얼에서 Java용 Aspose.PSD를 사용하여 PSD 파일에 곡선 조정 레이어를 추가하는 방법을 알아보세요. 이미지를 쉽게 향상시키세요.
type: docs
weight: 11
url: /ko/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/
---
## 소개
PSD 형식의 이미지를 조작하려고 할 때 막힌 적이 있습니까? 신예 그래픽 디자이너이든 숙련된 전문가이든 Photoshop 파일을 사용하여 작업하는 것은 때때로 미로를 탐색하는 것처럼 느껴질 수 있습니다. 다행히 이 프로세스를 단순화하는 도구인 Aspose.PSD for Java가 있습니다. 이 튜토리얼에서는 Aspose.PSD를 사용하여 PSD 파일에 곡선 조정 레이어를 추가하여 이미지 편집 작업을 더 쉽고 효율적으로 만드는 방법을 자세히 살펴보겠습니다. 단계별 안내를 통해 전통적으로 이미지 조작과 관련된 복잡성에 얽매이지 않고 전문가처럼 이미지를 향상시킬 수 있습니다.
## 전제조건
코드를 살펴보기 전에 모든 준비가 완료되었는지 확인하겠습니다. 필요한 전제 조건은 다음과 같습니다.
1. JDK(Java Development Kit): 컴퓨터에 JDK가 설치되어 있어야 합니다. 최고의 호환성을 위해 최신 버전인지 확인하세요.
2. Java 라이브러리용 Aspose.PSD: PSD 파일을 조작하려면 Aspose.PSD 라이브러리를 다운로드하여 프로젝트에 포함해야 합니다. 잡아도 돼[여기](https://releases.aspose.com/psd/java/).
3. IDE: IntelliJ IDEA, Eclipse 또는 간단한 텍스트 편집기와 같은 Java IDE를 사용하여 코드를 작성하세요.
4. Java에 대한 기본 이해: Java 프로그래밍에 익숙하면 원활하게 작업을 진행하는 데 도움이 됩니다.
모든 것을 얻었나요? 엄청난! 재미있는 부분을 살펴보겠습니다.
## 패키지 가져오기
먼저, 필요한 패키지를 가져와야 합니다. 이를 수행하는 방법은 다음과 같습니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
```
이러한 패키지를 가져오면 PSD 파일을 조작하고 특히 곡선 조정 레이어와 작업하는 데 필요한 클래스에 대해 Java 애플리케이션에 알리게 됩니다.
이제 모든 설정이 완료되었으므로 코드를 분석하고 곡선 조정 레이어를 단계별로 추가하는 방법을 살펴보겠습니다.
## 1단계: 데이터 디렉터리 정의
첫 번째 단계는 PSD 파일을 저장할 위치를 결정하는 것입니다. 모든 것을 체계적으로 정리하려면 디렉토리를 설정하세요.
```java
String dataDir = "Your Document Directory"; // 이 경로 업데이트
```
 생각하다`dataDir`귀하의 작업 공간으로; 모든 마법이 일어나는 곳이에요! 꼭 교체하세요`Your Document Directory` PSD 파일이 있거나 위치하게 될 실제 경로를 사용합니다.
## 2단계: PSD 파일 로드
다음으로 편집하려는 PSD 파일을 로드해야 합니다. 이는 다음 코드를 사용하여 수행됩니다.
```java
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
```
 이 코드 조각에서는`sourceFileName` 원본 PSD 파일을 가리키고,`psdPathAfterChange` 수정된 파일을 저장하는 곳입니다. 추가하는 것을 잊지 마세요`.psd` 나중에 코드에서.
## 3단계: 레이어 반복
이제 PSD 파일의 레이어를 살펴보겠습니다. 곡선 조정 레이어를 찾기 위해 각 레이어를 반복합니다.
```java
for (int j = 1; j < 2; j++) {
    String fileName = sourceFileName + ".psd";
    PsdImage im = (PsdImage) Image.load(fileName);
    
    for(int k = 0; k < im.getLayers().length; k++) {
        if (im.getLayers()[k] instanceof CurvesLayer) {
            // 곡선 레이어 처리가 여기로 이동됩니다.
        }
    }
}
```
무슨 일이 일어나고 있는지 분석해 보면 다음과 같습니다.
-  먼저 PSD 파일을`PsdImage` 명명된 객체`im`.
-  다음으로 다음을 사용하여 이미지의 모든 레이어를 반복합니다.`im.getLayers().length` . 이를 통해 우리는 각 레이어에 접근할 수 있으며, 해당 레이어가 레이어인지 확인할 수 있습니다.`CurvesLayer`.
## 4단계: 곡선 레이어 수정
 다음을 확인하는 루프 내부`CurvesLayer`에서는 곡선을 수정하는 논리를 추가합니다. 그 방법은 다음과 같습니다.
```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager) curvesLayer.getCurvesManager();
    for (int i = 10; i < 50; i++) {
        manager.setValueInPosition(0, (byte) i, (byte) (15 + (i * 2)));
    }
} else {
    CurvesContinuousManager manager = (CurvesContinuousManager) curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte) 0, (byte) 50, (byte) 100);
    manager.addCurvePoint((byte) 0, (byte) 150, (byte) 130);
}
```
이 세그먼트에서:
- 곡선 레이어가 이산 관리자를 사용하는지, 연속 관리자를 사용하는지 확인합니다.
- 개별 관리자인 경우 각 직위에 대해 10에서 49까지 새로운 값을 설정합니다.
- 반대로 연속 관리자를 사용하면 곡선 점을 추가하여 필요에 따라 곡선을 조정합니다.
## 5단계: 수정된 PSD 저장
조정 후 마지막 단계는 수정된 PSD 파일을 저장하는 것입니다.
```java
im.save(psdPathAfterChange + Integer.toString(j) + ".psd");
```
 이 줄은 조정된 PSD를 이전에 정의한 경로에 저장합니다. 수정할 때마다 루프 카운터를 기반으로 다른 접미사를 가진 새 파일이 생성됩니다.`j`.
## 결론
축하해요! Java용 Aspose.PSD를 사용하여 PSD 파일에 곡선 조정 레이어를 추가하는 방법을 성공적으로 배웠습니다. 몇 가지 단계만 거치면 이미지를 향상시키고 필요에 따라 조작할 수 있습니다. 이 라이브러리는 유연성을 제공하므로 PSD 파일을 사용하는 모든 사람에게 매우 유용한 도구입니다. 이제 다양한 곡선을 실험하고 창의력을 발휘해 보세요.
## FAQ
### Aspose.PSD란 무엇인가요?
Aspose.PSD는 Java를 포함한 다양한 프로그래밍 언어로 Photoshop PSD 파일을 처리하기 위한 라이브러리입니다.
### Aspose.PSD를 무료로 사용할 수 있나요?
 예, Aspose는 구매하기 전에 살펴볼 수 있는 무료 평가판을 제공합니다. 확인해보세요[무료 평가판 다운로드](https://releases.aspose.com/) 링크.
### 포토샵은 꼭 설치해야 하나요?
아니요, Aspose.PSD를 사용하기 위해 컴퓨터에 Photoshop을 설치할 필요는 없습니다.
### 곡선 조정 레이어 이외의 레이어를 조작할 수 있나요?
전적으로! Aspose.PSD를 사용하면 PSD 파일의 다양한 레이어 유형을 조작할 수 있습니다.
### 추가 문서는 어디서 찾을 수 있나요?
 자세한 문서를 보려면 다음을 방문하세요.[Java 문서용 Aspose.PSD](https://reference.aspose.com/psd/java/).
---
title: PSD에서 사진 필터 조정 레이어 관리 - Java
linktitle: PSD에서 사진 필터 조정 레이어 관리 - Java
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일의 사진 필터 조정 레이어를 관리하는 방법을 알아보세요. 필터를 손쉽게 편집하고 추가하려면 이 가이드를 따르세요.
weight: 24
url: /ko/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD에서 사진 필터 조정 레이어 관리 - Java

## 소개
Java를 사용하여 그래픽 편집 기능을 향상시키려는 개발자이십니까? 글쎄, 당신은 바로 이곳에 있어요! 오늘은 Aspose.PSD for Java를 사용하여 사진 필터 조정 레이어를 관리하는 방법을 살펴보겠습니다. 이 강력한 라이브러리를 사용하면 PSD 파일을 원활하게 조작할 수 있어 그래픽 디자인의 효율적인 작업 흐름이 가능해집니다. 효과를 추가하거나 기존 레이어를 편집하려는 경우 프로세스를 단순화하는 단계별 가이드를 제공합니다.
## 전제조건
이 여정을 시작하기 전에 필요한 모든 것이 갖추어져 있는지 확인하십시오.
### 필수 소프트웨어
1.  JDK(Java Development Kit): 컴퓨터에 호환 가능한 버전의 JDK가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[오라클의 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java: PSD 파일을 조작하려면 Aspose.PSD 라이브러리가 필요합니다. 다음에서 다운로드할 수 있습니다.[Aspose 릴리스 페이지](https://releases.aspose.com/psd/java/) 꼭 확인해 보세요.[Aspose 문서](https://reference.aspose.com/psd/java/) 자세한 내용은
3. IDE(통합 개발 환경): IntelliJ IDEA 또는 Eclipse와 같은 좋은 IDE는 코딩 경험을 더욱 원활하게 만들어줍니다.
### 기본 사항 이해
Java 프로그래밍에 익숙하고 PSD 파일 작동 방식에 대한 기본적인 이해가 있으면 도움이 됩니다. Java에서 라이브러리를 처음 사용하는 경우 프레임워크를 가져오고 활용하는 데 익숙해지는 것이 좋습니다.
## 패키지 가져오기
시작하려면 Aspose.PSD 라이브러리에서 필요한 클래스를 가져와야 합니다. 다음은 Java 파일 시작 부분에 필요한 간단한 import 문입니다.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
이를 Java 파일 상단에 붙여넣기만 하면 PSD 이미지 작업을 시작할 수 있습니다!
## 기존 포토 필터 레이어 편집
### 1단계: 데이터 디렉터리 설정
 먼저 PSD 파일이 저장되는 디렉터리를 정의해야 합니다. 바꾸다`"Your Document Directory"` 실제 경로와 함께. 모든 것을 정리하는 방법은 다음과 같습니다.
```java
String dataDir = "Your Document Directory";
```
### 2단계: PSD 파일 로드
 이제 편집하려는 PSD 파일을 로드해 보겠습니다. 다음을 확인하세요.`PhotoFilterAdjustmentLayer.psd`지정된 디렉토리에 존재합니다.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```
### 3단계: 이미지 개체 초기화
Aspose의 내장 기능을 사용하여 이미지를 프로젝트에 로드합니다.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
### 4단계: 레이어를 통해 반복
 다음으로 PSD 파일 내의 레이어를 살펴보겠습니다. 우리의 목표는`PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // 레이어를 변경합니다.
    }
}
```
### 5단계: 사진 필터 레이어 사용자 정의
 마법이 일어나는 곳은 바로 여기입니다! 다음을 수정할 수 있습니다.`Color` 그리고`Density`. 예를 들어 색상을 생생한 빨간색으로 설정하고 밀도를 조정할 수 있습니다.
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```
### 6단계: 편집된 PSD 파일 저장
마지막으로 변경 사항을 저장하여 조정 내용이 포함된 새 PSD 파일을 만듭니다.
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
PSD 파일에서 포토 필터 조정 레이어를 편집했습니다.
## 새 사진 필터 레이어 추가
### 1단계: 디렉터리 경로 설정
이전과 마찬가지로 데이터 디렉터리를 정의하는 것부터 시작합니다.
```java
String dataDir = "Your Document Directory";
```
### 2단계: 소스 파일 로드
이 예에서는 새 사진 필터를 추가하려는 다른 PSD 파일을 로드해 보겠습니다.
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```
### 3단계: 이미지 개체 다시 초기화
 우리는 새로운 것을 창조해야 합니다.`PsdImage` 인스턴스이므로 파일을 로드합니다.
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```
### 4단계: 사진 필터 레이어 추가
이제 사용자 정의된 색상으로 새 사진 필터 레이어를 추가할 수 있습니다. 수행 방법은 다음과 같습니다.
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```
### 5단계: 새 PSD 파일 저장
다시 한 번 변경 사항을 저장할 차례입니다. 이를 수행하는 라인은 다음과 같습니다.
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
PSD 파일에 새 사진 필터 레이어를 성공적으로 추가했습니다.
## 결론
Java용 Aspose.PSD를 사용하여 PSD 파일의 사진 필터 조정 레이어를 관리하는 것은 간단할 뿐만 아니라 그래픽 편집에 대한 가능성의 세계를 열어줍니다. 이러한 단계별 가이드를 따르면 생생한 필터로 PSD 파일을 향상하고 멋진 그래픽을 만들 수 있습니다. 애플리케이션에서 이러한 기능을 테스트해 보세요. 당신은 확실히 당신의 프로젝트에 효율적이라는 것을 알게 될 것입니다!
## FAQ
### Aspose.PSD란 무엇인가요?
Aspose.PSD는 PSD 파일을 생성, 편집 및 변환하는 .NET 및 Java 라이브러리입니다.
### Aspose.PSD를 무료로 사용해 볼 수 있나요?
 예, Aspose는 무료 평가판을 제공합니다. 확인해 보세요[여기](https://releases.aspose.com/).
### 문서는 어디서 찾을 수 있나요?
 다음에서 전체 문서를 찾을 수 있습니다.[Aspose의 참조 페이지](https://reference.aspose.com/psd/java/).
### Aspose.PSD를 어떻게 구매할 수 있나요?
 다음에서 소프트웨어를 구입할 수 있습니다.[이 링크](https://purchase.aspose.com/buy).
### Aspose.PSD에 대한 지원이 제공됩니까?
 전적으로! Aspose 지원 포럼을 통해 지원을 받을 수 있습니다.[여기](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

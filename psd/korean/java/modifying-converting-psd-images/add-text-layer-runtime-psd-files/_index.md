---
title: Java를 사용하여 PSD 파일의 런타임에 텍스트 레이어 추가
linktitle: Java를 사용하여 PSD 파일의 런타임에 텍스트 레이어 추가
second_title: Aspose.PSD 자바 API
description: Aspose.PSD와 함께 Java를 사용하여 PSD 파일에 텍스트 레이어를 동적으로 추가하는 방법을 알아보세요. 흥미로운 자동화 가능성을 알아보려면 이 단계별 튜토리얼을 따르십시오.
weight: 17
url: /ko/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 PSD 파일의 런타임에 텍스트 레이어 추가

## 소개
Photoshop을 사용해 본 적이 있다면 Photoshop이 이미지 편집에 얼마나 강력한지 알 것입니다. 하지만 Java를 사용하여 이러한 작업 중 일부를 자동화할 수 있다고 말하면 어떻게 될까요? 프로그래밍 방식으로 PSD 파일에 텍스트 레이어를 동적으로 추가한다고 상상해 보세요. 정말 멋지죠? 이 튜토리얼에서는 Java용 Aspose.PSD 라이브러리를 사용하여 PSD 파일에 텍스트 레이어를 즉시 추가하는 방법을 자세히 살펴보겠습니다. 자, 소매를 걷어붙이고 바로 시작해 보세요!
## 전제조건
코드를 살펴보기 전에 시작하는 데 필요한 모든 것이 갖추어져 있는지 확인하겠습니다. 필요한 사항은 다음과 같습니다.
1.  JDK(Java Development Kit): 컴퓨터에 JDK가 설치되어 있는지 확인하세요. 당신은 할 수 있습니다[여기에서 다운로드하세요](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Java 패키지용 Aspose.PSD: Aspose.PSD 라이브러리를 다운로드하여 프로젝트에 통합해야 합니다. 에서 가져오시면 됩니다[Aspose 릴리스 페이지](https://releases.aspose.com/psd/java/).
3. 통합 개발 환경(IDE): 모든 텍스트 편집기를 사용할 수 있지만 IntelliJ IDEA 또는 Eclipse와 같은 IDE는 프로젝트 관리 도구를 제공하여 작업을 훨씬 쉽게 만들어줍니다.
4. 기본 Java 지식: 이 튜토리얼을 원활하게 진행하려면 핵심 Java 개념을 이해하는 것이 필요합니다.
5.  PSD 파일: 재생할 수 있는 기본 PSD 파일을 준비합니다. 우리는 이름이 지정된 것을 사용하겠습니다.`OneLayer.psd` 우리의 출발점으로.
## 패키지 가져오기
모든 것이 준비되면 프로세스의 첫 번째 단계는 Java 파일에 필요한 패키지를 가져오는 것입니다. 포함해야 할 사항은 다음과 같습니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```
이러한 가져오기는 Aspose.PSD 라이브러리를 사용하여 PSD 파일을 조작하는 데 필요한 모든 중요한 클래스를 가져옵니다.
이제 PSD 파일에 텍스트 레이어를 추가하는 핵심을 살펴보겠습니다. 각 단계를 철저하게 이해할 수 있도록 이를 관리 가능한 단계로 나누어 보겠습니다.
## 1단계: 문서 디렉토리 설정
먼저 Adobe Photoshop Document(PSD) 파일이 상주할 작업 공간을 설정해야 합니다. 간단한 문자열로 PSD 파일의 위치를 정의하세요.
```java
String dataDir = "Your Document Directory"; 
```
 여기서는`"Your Document Directory"` PSD 파일이 저장된 실제 경로와 함께.
## 2단계: 소스 PSD 파일 로드
다음으로 PSD 파일을 애플리케이션에 로드해야 합니다. 이것이 마법이 시작되는 곳입니다. 사용`Image.load()` 파일을 재생하는 방법입니다.
```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```
 이 코드 조각은`OneLayer.psd` 파일을`img` 물체. 경로가 정확하면 PSD가 로드되어 조작할 준비가 된 것입니다.
## 3단계: PsdImage로 전송
 이미지가 로드되면 이미지를 캐스팅해야 합니다.`PsdImage` 왜냐하면 우리는 특히 Photoshop 파일을 다루고 있기 때문입니다.
```java
PsdImage im = (PsdImage)img;
```
캐스팅하면 이 튜토리얼에서 필요한 PSD 조작과 관련된 모든 방법에 액세스할 수 있습니다.
## 4단계: 텍스트 레이어의 직사각형 정의
이제 텍스트 레이어를 표시할 위치를 지정할 차례입니다. 텍스트의 위치와 크기를 설정하는 직사각형을 정의합니다.
```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```
이 예에서 직사각형은 이미지 너비의 절반과 높이의 절반을 차지하도록 설정되어 아래쪽과 가로 방향의 1/4 지점에 배치됩니다. 텍스트를 원하는 위치에 정확히 배치하려면 이 값을 자유롭게 조정하세요!
## 5단계: 텍스트 레이어 추가
 이제 최고의 저항을 위해 — 텍스트를 추가해보세요! 사용`addTextLayer()` 지정된 직사각형에서 원하는 텍스트를 생생하게 표현하는 방법입니다.
```java
TextLayer layer = im.addTextLayer("Added text", rect);
```
이 경우에는 "텍스트 추가"라는 텍스트 레이어를 추가하기만 하면 됩니다. 이것을 원하는 문자열로 바꿀 수 있습니다.
## 6단계: 업데이트된 PSD 파일 저장
마지막 단계는 변경 사항을 새 PSD 파일에 다시 저장하는 것입니다. 이를 수행하는 방법은 다음과 같습니다.
```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```
 원본 PSD 파일을 덮어쓰지 않도록 새 파일 이름을 지정해야 합니다. 이제 지정된 디렉토리를 확인하면 다음과 같이 표시됩니다.`ImageWithTextLayer.psd` 새로 추가된 텍스트와 함께!
## 결론
그리고 그것은 마무리입니다! Aspose.PSD 라이브러리와 함께 Java를 사용하여 PSD 파일에 텍스트 레이어를 동적으로 추가하는 방법을 배웠습니다. Photoshop 기능을 응용 프로그램에 통합하려는 모든 개발자에게 획기적인 변화입니다. 디자이너를 위한 프로젝트 관리자로 작업하든 그래픽 작업을 자동화하든 이 기술을 사용하면 많은 시간을 절약할 수 있습니다.
더 자세히 살펴보고 싶으신가요? 추가 기능과 고급 기능에 대해서는 Java용 Aspose.PSD 문서를 확인하세요.
## FAQ
### 여러 텍스트 레이어를 추가할 수 있나요?
전적으로! 추가하려는 각 텍스트 레이어에 대해 4단계와 5단계를 반복하세요.
### 내 PSD 파일에 여러 레이어가 있으면 어떻게 되나요?
Aspose.PSD는 복잡한 레이어 PSD 파일을 처리할 수 있습니다. 레이어를 조작할 때 올바른 레이어를 참조했는지 확인하세요.
### 텍스트 스타일을 지정하는 방법이 있나요?
 예! 의 기능을 탐색할 수 있습니다.`TextLayer` Aspose.PSD 문서를 살펴보고 글꼴 크기, 색상 등을 변경하는 클래스입니다.
### 웹 애플리케이션에서 이것을 사용할 수 있나요?
예. Java 백엔드가 있으면 웹 애플리케이션에서 이 접근 방식을 활용할 수 있습니다.
### 문제가 발생하면 어디서 지원을 받을 수 있나요?
 확인해 보세요[Aspose 지원 포럼](https://forum.aspose.com/c/psd/34) 커뮤니티와 Aspose 팀이 도움을 드릴 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

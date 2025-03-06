---
title: PSD 레이어의 밝기 및 대비 관리 - Java
linktitle: PSD 레이어의 밝기 및 대비 관리 - Java
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일의 밝기와 대비를 쉽게 조정하는 방법을 알아보세요. 개발자와 그래픽 디자이너에게 이상적입니다.
weight: 21
url: /ko/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD 레이어의 밝기 및 대비 관리 - Java

## 소개

PSD(Photoshop Document) 파일을 자주 작업하는 그래픽 디자이너 또는 개발자이신가요? 이러한 파일에서 레이어의 밝기와 대비를 조정해야 하는데 Java를 사용하여 이 작업을 자동화하는 노하우가 부족합니까? 글쎄, 당신은 운이 좋다! 이 튜토리얼에서는 Java용 Aspose.PSD 라이브러리를 사용하여 PSD 레이어의 밝기와 대비를 관리하는 방법을 살펴보겠습니다. 이렇게 하면 시간을 절약할 수 있을 뿐만 아니라 창의적인 작업 흐름도 향상됩니다. 소매를 걷어붙이고 시작해보자!

## 전제조건

Java로 PSD 파일을 조작하는 흥미로운 여정을 시작하기 전에 필요한 모든 것이 올바르게 설정되었는지 확인하는 것이 중요합니다. 이 튜토리얼을 성공적으로 완료하는 데 필요한 사항은 다음과 같습니다.

1.  JDK(Java Development Kit): 컴퓨터에 JDK 8 이상이 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[오라클의 웹사이트](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).

2. Java 라이브러리용 Aspose.PSD: PSD 파일로 작업하려면 Aspose.PSD 라이브러리가 필요합니다. 최신 버전은 다음 사이트에서 다운로드할 수 있습니다.[릴리스 페이지](https://releases.aspose.com/psd/java/).

3. 원하는 IDE: Java 코드를 작성하고 실행하려면 IntelliJ IDEA, Eclipse 또는 NetBeans와 같은 통합 개발 환경(IDE)이 선호됩니다.

4. Java에 대한 기본 지식: Java 프로그래밍에 익숙하면 작업할 코드 조각을 이해하는 데 도움이 됩니다.

이러한 전제 조건이 충족되면 계속 진행할 준비가 된 것입니다. 이제 즐겨 사용하는 코드 편집기를 들고 코딩을 시작해 보세요!

## 패키지 가져오기

코딩 여정의 첫 번째 단계는 필요한 패키지를 가져오는 것입니다. Aspose.PSD에서 제공하는 기능을 활용하려면 먼저 라이브러리가 클래스 경로에 있는지 확인해야 합니다. 그렇게 하는 방법은 다음과 같습니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

이 단계를 완료하면 PSD 파일을 효과적으로 작업할 수 있는 환경이 설정됩니다!

이제 모든 설정이 완료되었으므로 튜토리얼의 핵심인 PSD 레이어의 밝기 및 대비 조정에 들어갈 시간입니다. 우리는 귀하가 쉽게 따라할 수 있도록 이 프로세스를 명확한 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 정의

PSD 파일이 있는 디렉터리를 정의하는 것부터 시작하세요. 이 단계는 파일을 효율적으로 정리하는 데 도움이 됩니다.

```java
String dataDir = "Your Document Directory";
```

 바꾸다`"Your Document Directory"` PSD 파일 디렉터리의 실제 경로를 사용합니다.

## 2단계: 소스 및 대상 파일 이름 지정

다음으로 PSD의 소스 파일 이름과 편집된 PSD가 저장될 대상 파일을 지정해야 합니다.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

 이 예에서는 다음과 같은 PSD 파일이 있다고 가정합니다.`BrightnessContrastModern.psd` 귀하의 디렉토리에.

## 3단계: PSD 파일 로드

이제 PSD 파일을 조작할 수 있도록 애플리케이션에 로드할 차례입니다.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

 이 코드 줄은 다음의 인스턴스를 생성합니다.`PsdImage` PSD 파일을 나타냅니다. 이를 통해 이제 PSD의 모든 레이어에 액세스할 수 있습니다.

## 4단계: 레이어를 통해 반복

다음 단계에는 PSD 파일의 각 레이어를 반복하여 밝기 및 대비 설정을 찾고 조작하는 작업이 포함됩니다.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

 그만큼`for` 루프는 PSD의 각 레이어를 통과합니다. 레이어가 다음의 인스턴스인지 확인하고 있습니다.`BrightnessContrastLayer`. 이는 올바른 레이어의 밝기와 대비만 변경하려고 시도하는 데 필수적입니다.

## 5단계: 밝기 및 대비 조정

 루프 내에서 이제 각각의 밝기와 대비를 설정할 수 있습니다.`BrightnessContrastLayer`. 

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

 이 예에서는 밝기와 대비를 다음과 같이 설정합니다.`50`. 요구 사항에 따라 이러한 값을 조정할 수 있습니다. 숫자가 높을수록 밝기/대비가 증가하고 숫자가 낮을수록 감소합니다.

## 6단계: 변경 사항 저장

마지막 단계는 변경 사항을 PSD 파일에 저장하는 것입니다. 수정된 이미지를 지정된 대상에 다시 쓰고 싶을 것입니다.

```java
im.save(psdPathAfterChange);
```

이 코드 줄은 편집된 PSD 파일을 새로운 밝기 및 대비 설정으로 저장합니다.

## 결론

축하해요! Java용 Aspose.PSD를 사용하여 PSD 레이어의 밝기와 대비를 관리하는 방법을 성공적으로 배웠습니다. 이러한 조정을 자동화하면 작업 흐름을 개선할 뿐만 아니라 생산성도 높일 수 있습니다. 다음에 해당 이미지를 조정해야 할 때 새로운 Java 기술로 작업을 처리할 수 있는 준비가 잘 갖추어진 것입니다. 그럼 다음에는 무엇을 만들까요?

## FAQ

### Java용 Aspose.PSD란 무엇입니까?
Aspose.PSD for Java는 개발자가 PSD 파일을 프로그래밍 방식으로 조작하여 Photoshop 관련 작업을 자동화할 수 있는 라이브러리입니다.

### 여러 레이어의 밝기와 대비를 한 번에 조정할 수 있나요?
 예, 이 튜토리얼에서 사용된 접근 방식은 PSD의 모든 레이어를 반복하여 여러 레이어를 조정할 수 있습니다.`BrightnessContrastLayer` 인스턴스.

### Aspose.PSD에 대한 임시 라이선스는 어떻게 얻나요?
 방문하시면 임시면허증을 받으실 수 있습니다.[임시 라이센스 페이지](https://purchase.aspose.com/temporary-license/).

### Aspose.PSD에 대한 무료 평가판이 있습니까?
 예, 다음에서 Aspose.PSD 무료 평가판을 다운로드할 수 있습니다.[릴리스 페이지](https://releases.aspose.com/).

### Aspose.PSD에 대한 추가 지원은 어디서 찾을 수 있나요?
 Aspose.PSD에 대한 지원을 받을 수 있습니다.[지원 포럼](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

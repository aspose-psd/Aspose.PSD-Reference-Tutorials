---
title: Java용 Aspose.PSD를 사용하여 PSD에 새 일반 레이어 추가
linktitle: PSD에 새 일반 레이어 추가
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일에 새로운 일반 레이어를 추가하는 방법을 알아보세요. 원활한 PSD 조작을 위한 단계별 가이드를 따르세요.
type: docs
weight: 11
url: /ko/java/advanced-image-effects/add-new-regular-layer/
---
## 소개

PSD 파일에 새로운 일반 레이어를 추가하기 위해 Java용 Aspose.PSD를 사용하는 포괄적인 튜토리얼에 오신 것을 환영합니다. Aspose.PSD는 개발자가 PSD 파일을 효율적으로 조작하고 작업할 수 있게 해주는 강력한 Java 라이브러리입니다. 이 튜토리얼에서는 PSD 파일에 새로운 일반 레이어를 추가하는 과정을 안내하고 자세한 단계와 코드 예제를 제공합니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Java 개발 환경: 시스템에 Java 개발 환경이 설정되어 있는지 확인하십시오.
-  Aspose.PSD 라이브러리: Java 라이브러리용 Aspose.PSD를 다운로드하여 설치합니다. 도서관을 찾으실 수 있습니다[여기](https://releases.aspose.com/psd/java/).

## 패키지 가져오기

시작하려면 필요한 패키지를 Java 프로젝트로 가져옵니다. 이 패키지는 Aspose.PSD 기능을 사용하는 데 필수적입니다. Java 파일 시작 부분에 다음 줄을 포함합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 1단계: PSD 파일 로드

다음 코드를 사용하여 편집하려는 PSD 파일을 로드합니다.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## 2단계: 데이터 배열 및 직사각형 준비

다음과 같이 두 개의 int 배열과 두 개의 Rectangle 객체를 준비합니다.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## 3단계: 레이어 데이터 초기화

기본값으로 데이터 배열을 초기화합니다.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## 4단계: 일반 레이어 추가

PSD 이미지에 두 개의 일반 레이어를 추가합니다.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## 5단계: PSD 및 PNG 저장

수정된 PSD와 추가 PNG 파일을 저장합니다.

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

축하해요! Java용 Aspose.PSD를 사용하여 PSD 파일에 새로운 일반 레이어를 성공적으로 추가했습니다.

## 결론

이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 PSD 파일에 새로운 일반 레이어를 추가하는 과정을 다루었습니다. 이 강력한 라이브러리는 PSD 조작을 단순화하여 Java 개발자가 액세스할 수 있도록 해줍니다. Aspose.PSD의 잠재력을 최대한 활용하기 위해 다양한 매개변수와 기능을 실험해보세요.

## FAQ

### Q1: Aspose.PSD는 Java 8과 호환됩니까?

A1: 예, Aspose.PSD는 Java 8 이상 버전을 지원합니다.

### Q2: 추가된 레이어에 변형을 적용할 수 있나요?

A2: 물론이죠! Aspose.PSD는 레이어에 대한 다양한 변환 옵션을 제공합니다.

### Q3: 추가 Aspose.PSD 문서는 어디서 찾을 수 있나요?

 A3: 설명서를 참조할 수 있습니다.[여기](https://reference.aspose.com/psd/java/).

### Q4: Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?

 A4: 방문[이 링크](https://purchase.aspose.com/temporary-license/) 임시 라이센스 옵션의 경우.

### Q5: Aspose.PSD 지원을 위한 커뮤니티 포럼이 있습니까?

 A5: 예, 지원과 토론을 찾을 수 있습니다.[여기](https://forum.aspose.com/c/psd/34).
---
title: Java용 Aspose.PSD에서 이미지 회전
linktitle: 이미지 회전
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 Java에서 이미지 회전을 손쉽게 탐색해 보세요. PSD 파일을 쉽게 회전하고 뒤집고 저장할 수 있습니다.
type: docs
weight: 19
url: /ko/java/advanced-image-manipulation/rotate-image/
---
## 소개

Aspose.PSD for Java는 이미지 작업을 위한 강력한 기능 세트를 제공하므로 개발자는 PSD 파일을 효율적으로 조작하고 처리할 수 있습니다. 이 튜토리얼에서는 이미지 회전이라는 하나의 특정 작업에 중점을 둘 것입니다. 사진 편집 애플리케이션을 구축하거나 단순히 이미지 방향을 조정해야 하는 경우 Aspose.PSD를 사용하면 프로세스가 간단해집니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  Java 라이브러리용 Aspose.PSD: Java 라이브러리용 Aspose.PSD를 다운로드하여 설치했는지 확인하세요. 라이브러리와 자세한 문서를 찾을 수 있습니다[여기](https://reference.aspose.com/psd/java/).

- Java 개발 환경: 컴퓨터에 Java 개발 환경이 설정되어 있는지 확인하십시오.

-  샘플 PSD 파일: 회전하려는 샘플 PSD 파일을 준비합니다. 조정하다`sourceFile` PSD 파일 경로가 포함된 예제 코드의 변수입니다.

## 패키지 가져오기

Aspose.PSD의 기능을 활용하기 위해 필요한 패키지를 가져오는 것부터 시작하세요.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 1단계: 이미지 로드

 기존 이미지를 인스턴스에 로드합니다.`Image` 수업:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## 2단계: 이미지 회전

 다음을 사용하여 이미지를 회전합니다.`rotateFlip` 방법. 이 예에서는 이미지를 270도 회전합니다.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## 3단계: 회전된 이미지 저장

 회전된 이미지를 다음을 사용하여 저장합니다.`save` 방법 및 출력 형식 지정(이 경우 JPEG):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## 결론

축하해요! Java용 Aspose.PSD를 사용하여 이미지를 성공적으로 회전했습니다. 이 간단하면서도 강력한 라이브러리는 Java 애플리케이션에서 이미지 조작의 가능성을 열어줍니다.

## FAQ

### Q1: Aspose.PSD는 다른 이미지 형식과 호환됩니까?

A1: 예, Aspose.PSD는 PSD, JPEG, PNG 등을 포함한 다양한 이미지 형식을 지원합니다.

### Q2: 미리 정의된 뒤집기뿐만 아니라 사용자 정의 회전도 적용할 수 있나요?

A2: 물론이죠! Aspose.PSD는 특정 요구 사항을 충족하기 위해 사용자 지정 회전을 적용할 수 있는 유연성을 제공합니다.

### Q3: 추가 지원이나 도움은 어디서 찾을 수 있나요?

 A3: 질문이나 문제가 있는 경우[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 지역 사회 지원을 위해.

### Q4: 무료 평가판이 제공됩니까?

 A4: 예, Aspose.PSD를 탐색할 수 있습니다.[무료 평가판](https://releases.aspose.com/).

### Q5: 임시 라이센스는 어떻게 얻나요?

 A5: 임시 라이센스가 필요한 경우 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).
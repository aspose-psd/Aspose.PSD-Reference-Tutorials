---
title: Java용 Aspose.PSD에서 직사각형으로 이미지 자르기
linktitle: 직사각형으로 이미지 자르기
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 Java의 원활한 이미지 자르기 기능을 살펴보세요. Java용 Aspose.PSD를 사용하여 이미지를 쉽게 자르려면 단계별 가이드를 따르세요.
weight: 15
url: /ko/java/image-editing/crop-image-by-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.PSD에서 직사각형으로 이미지 자르기

## 소개

Java 개발 세계에서 이미지 조작은 일반적인 작업이며 Java용 Aspose.PSD는 이미지 처리를 위한 강력한 솔루션을 제공합니다. 이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 이미지를 직사각형으로 자르는 과정을 안내합니다. 이를 쉽게 달성하려면 아래 단계를 따르십시오.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- 컴퓨터에 JDK(Java Development Kit)가 설치되어 있습니다.
- Java 라이브러리용 Aspose.PSD. 다음에서 다운로드할 수 있습니다.[웹사이트](https://releases.aspose.com/psd/java/).

## 패키지 가져오기

Java용 Aspose.PSD의 기능을 활용하려면 Java 프로젝트에 필요한 패키지를 포함해야 합니다. Java 파일 시작 부분에 다음 가져오기 문을 추가합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

이제 Java용 Aspose.PSD를 사용하여 이미지를 직사각형으로 자르는 과정을 안내하기 위해 프로세스를 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 설정

```java
String dataDir = "Your Document Directory";
```

 바꾸다`"Your Document Directory"` PSD 파일이 있는 실제 경로를 사용합니다.

## 2단계: 소스 및 대상 파일 지정

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

소스 PSD 파일과 대상 JPEG 파일의 경로를 정의합니다.

## 3단계: 이미지 로드 및 캐시

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 PSD 이미지를`RasterImage` 인스턴스를 생성하고 해당 데이터를 캐시합니다.

## 4단계: 자르기 직사각형 생성 및 정의

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 인스턴스를 생성합니다.`Rectangle` 자르기에 원하는 크기의 클래스입니다.

## 5단계: 이미지 자르기 및 저장

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

지정된 사각형을 사용하여 자르기 작업을 수행하고 결과를 JPEG 파일로 저장합니다.

필요에 따라 이 단계를 반복하고 특정 요구 사항에 따라 매개변수를 조정합니다.

## 결론

이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 이미지를 직사각형으로 자르는 과정을 살펴보았습니다. 다음 단계를 수행하면 강력한 이미지 조작 기능을 Java 애플리케이션에 쉽게 통합할 수 있습니다.

## FAQ

### Q1: 다른 Java 프레임워크와 함께 Java용 Aspose.PSD를 사용할 수 있습니까?

A1: 예, Java용 Aspose.PSD는 다양한 Java 프레임워크와 통합되어 개발 프로젝트에 유연성을 제공할 수 있습니다.

### Q2: Aspose.PSD for Java에 대한 무료 평가판이 있습니까?

 A2: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: 추가 지원이나 도움은 어디서 찾을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 커뮤니티 지원 및 토론을 위해.

### Q4: Java용 Aspose.PSD의 임시 라이선스를 어떻게 얻나요?

 A4: 임시 라이센스를 취득할 수 있습니다[여기](https://purchase.aspose.com/temporary-license/).

### Q5: Java용 Aspose.PSD에서 자르기에 지원되는 이미지 형식은 무엇입니까?

A5: Java용 Aspose.PSD는 PSD, PNG, JPEG 등을 포함한 다양한 이미지 형식을 지원합니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

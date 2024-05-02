---
title: Java용 Aspose.PSD를 사용하여 이미지 확장 및 자르기
linktitle: 이미지 확장 및 자르기
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 Java에서 이미지를 확장하고 자르는 방법을 알아보세요. 효율적인 이미지 처리를 위한 단계별 가이드입니다.
type: docs
weight: 18
url: /ko/java/image-editing/expand-and-crop-images/
---
## 소개

이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 이미지를 효율적으로 확장하고 자르는 방법을 살펴보겠습니다. Aspose.PSD는 Java 애플리케이션에서 PSD 파일 작업을 위한 광범위한 기능을 제공하는 강력한 라이브러리입니다. 이 가이드에서는 필요한 전제 조건, 패키지 가져오기를 다루고 자세한 설명과 함께 각 단계를 세분화합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. Java 개발 환경: 시스템에 Java가 설치되어 있는지 확인하십시오.

2.  Aspose.PSD 라이브러리: Aspose.PSD 라이브러리를 다운로드하여 설치합니다. 도서관을 찾으실 수 있습니다[여기](https://releases.aspose.com/psd/java/).

## 패키지 가져오기

이제 필수 구성 요소가 준비되었으므로 Java용 Aspose.PSD 작업을 시작하는 데 필요한 패키지를 가져옵니다. Java 코드에 다음 줄을 추가합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

이 패키지는 Aspose.PSD를 사용하여 이미지 처리를 위한 필수 클래스와 메서드를 제공합니다.

## 1단계: 문서 디렉터리 설정

PSD 파일이 있는 디렉터리를 설정하여 시작하세요. "Your Document Directory"를 실제 경로로 바꾸십시오.

```java
String dataDir = "Your Document Directory";
```

## 2단계: 원본 및 대상 경로 지정

소스 PSD 파일과 출력 이미지의 대상 경로를 정의합니다.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## 3단계: 이미지 로드 및 캐시

 PSD 파일을`RasterImage` 개체를 만들고 해당 데이터를 캐시합니다.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## 4단계: 자르기 위한 직사각형 만들기

 인스턴스화`Rectangle` 개체를 선택하고 해당 X, Y 좌표, 너비 및 높이를 정의합니다. 이 직사각형은 잘리는 영역을 결정합니다.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

## 5단계: 자른 이미지 저장

 정의된 직사각형과`JpegOptions` 수업.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

축하해요! Java용 Aspose.PSD를 사용하여 이미지를 성공적으로 확장하고 자릅니다.

## 결론

이 튜토리얼에서는 Java 라이브러리용 Aspose.PSD를 사용하여 이미지를 확장하고 자르는 과정을 살펴보았습니다. 강력한 기능을 갖춘 Aspose.PSD는 이미지 조작 작업을 단순화하므로 Java 개발자에게 탁월한 선택입니다.

## FAQ

### Q1: Aspose.PSD는 다른 Java 버전과 호환됩니까?

A1: 예, Aspose.PSD는 다양한 Java 버전을 지원하여 다양한 개발 환경과의 호환성을 보장합니다.

### Q2: Aspose.PSD를 상업용 프로젝트에 사용할 수 있나요?

A2: 물론 Aspose.PSD는 개발자에게 상업용 라이선스를 제공하므로 개인 및 상업용 프로젝트 모두에서 사용할 수 있습니다.

### Q3: 지원되는 이미지 파일 형식에 제한이 있나요?

 A3: Aspose.PSD는 PSD, JPEG, PNG 등을 포함한 다양한 이미지 파일 형식을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/psd/java/) 전체 목록을 보려면.

### Q4: Aspose.PSD 관련 쿼리에 대한 지원을 어떻게 받을 수 있나요?

 A4: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 커뮤니티나 Aspose 지원팀의 도움을 구하세요.

### Q5: 무료 평가판이 제공됩니까?

 A5: 예, 무료 평가판을 통해 Aspose.PSD를 탐색할 수 있습니다. 다운로드 해[여기](https://releases.aspose.com/).
---
date: 2026-01-01
description: Aspose.PSD for Java를 사용하여 Java에서 이미지를 자르는 방법을 살펴보세요. PSD 파일을 로드하고, 이미지
  사각형을 자르고, PSD를 JPEG로 변환하는 단계별 가이드를 따라가세요.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Java 이미지 자르기: Aspose.PSD를 사용한 사각형으로 이미지 자르기'
url: /ko/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: 사각형으로 이미지 자르기 with Aspose.PSD

## 소개

그래픽을 다루는 것은 **java image processing**의 일상적인 작업이며, Aspose.PSD for Java는 PSD 파일을 다루기 위한 깔끔하고 고성능 API를 제공합니다. 이 튜토리얼에서는 사각형을 사용해 **how to crop image**하는 방법, PSD 파일을 로드하는 방법, 그리고 결과를 JPEG로 변환하는 방법을 몇 줄의 Java 코드만으로 배울 수 있습니다.

## 빠른 답변
- **“crop image java”는 무엇을 의미하나요?** Java 코드를 사용해 정의된 사각형으로 이미지를 잘라내는 것을 말합니다.  
- **어떤 라이브러리가 이 작업을 처리하나요?** Aspose.PSD for Java가 필요한 클래스를 제공합니다.  
- **테스트에 라이선스가 필요하나요?** 무료 체험판을 사용할 수 있으며, 실제 운영 환경에서는 라이선스가 필요합니다.  
- **잘라낸 PSD를 JPEG로 변환할 수 있나요?** 예—저장 시 `JpegOptions`를 사용하면 됩니다.  
- **구현에 얼마나 걸리나요?** 기본 시나리오의 경우 보통 10 분 이내에 완료됩니다.

## Java에서 이미지 사각형 자르기란?

이미지 사각형 자르기는 특정 영역( X, Y, 너비, 높이 로 정의)을 선택하고 그 영역 밖의 모든 것을 버리는 작업을 의미합니다. 이 작업은 큰 PSD 문서에서 특정 부분에 집중해야 할 때 흔히 사용됩니다.

## 왜 이 작업에 Aspose.PSD를 사용하나요?

- **외부 종속성 없음** – 순수 Java만으로 동작합니다.  
- **PSD, PNG, JPEG 등 다양한 포맷 지원** – **convert PSD to JPEG**를 즉시 수행할 수 있습니다.  
- **고충실도 렌더링** – 자르는 동안 레이어 정보와 색상 프로필을 유지합니다.  

## 전제 조건

- Java Development Kit (JDK) 설치 완료.  
- Aspose.PSD for Java 라이브러리 – [website](https://releases.aspose.com/psd/java/)에서 다운로드합니다.  

## 패키지 가져오기

Java 프로젝트에서 Aspose.PSD for Java의 기능을 활용하려면 필요한 패키지를 포함해야 합니다. Java 파일의 시작 부분에 다음 import 구문을 추가하세요:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

이제 Aspose.PSD for Java를 사용해 사각형으로 이미지를 자르는 과정을 여러 단계로 나누어 살펴보겠습니다.

## 단계 1: 문서 디렉터리 설정

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"`를 PSD 파일이 실제로 위치한 경로로 교체하세요.

## 단계 2: 소스 및 대상 파일 지정

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

소스 PSD 파일과 대상 JPEG 파일의 경로를 정의합니다.

## 단계 3: 이미지 로드 및 캐시

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

여기서는 PSD 파일을 `RasterImage` 인스턴스로 **load PSD file**하고, 성능 향상을 위해 데이터를 캐시합니다.

## 단계 4: 자르기 사각형 생성 및 정의

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

`Rectangle` 클래스를 사용해 원하는 크기의 사각형 인스턴스를 생성합니다. 매개변수는 각각 **X**, **Y**, **width**, **height**를 나타냅니다.

## 단계 5: 이미지 자르고 저장

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

지정한 사각형으로 자르기 작업을 수행하고, `JpegOptions`를 사용해 **convert PSD to JPEG**하면서 결과를 저장합니다.

필요에 따라 매개변수를 조정해 이 단계를 반복하면 됩니다.

## 일반적인 문제 및 팁

- **사각형이 이미지 경계를 벗어남** – 사각형 좌표가 원본 이미지 크기 내에 있는지 확인하세요.  
- **메모리 사용량** – 작업이 끝난 후 `rasterImage.dispose()`를 호출해 네이티브 리소스를 해제합니다.  
- **품질 제어** – `JpegOptions.setQuality(int)`를 사용해 출력 JPEG의 압축 수준을 조절할 수 있습니다.

## 결론

이 튜토리얼에서는 Aspose.PSD for Java를 사용해 사각형으로 **crop image java**하는 전체 과정을 살펴보았습니다. 이 단계를 따르면 PSD 파일을 로드하고, 특정 영역을 자르고, 결과를 JPEG로 변환하는 강력한 이미지 조작 기능을 Java 애플리케이션에 손쉽게 통합할 수 있습니다.

## FAQ

### Q1: Aspose.PSD for Java를 다른 Java 프레임워크와 함께 사용할 수 있나요?

A1: 예, Aspose.PSD for Java는 다양한 Java 프레임워크와 통합될 수 있어 개발 프로젝트에 유연성을 제공합니다.

### Q2: Aspose.PSD for Java의 무료 체험판을 이용할 수 있나요?

A2: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 다운로드할 수 있습니다.

### Q3: 추가 지원이나 도움이 필요하면 어디서 찾을 수 있나요?

A3: 커뮤니티 지원 및 토론을 위해 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)을 방문하세요.

### Q4: Aspose.PSD for Java의 임시 라이선스는 어떻게 얻나요?

A4: 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 신청할 수 있습니다.

### Q5: Aspose.PSD for Java에서 지원하는 이미지 포맷은 무엇인가요?

A5: Aspose.PSD for Java는 PSD, PNG, JPEG 등 다양한 이미지 포맷을 지원합니다.

**마지막 업데이트:** 2026-01-01  
**테스트 환경:** Aspose.PSD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
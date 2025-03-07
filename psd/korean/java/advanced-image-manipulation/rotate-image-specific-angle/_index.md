---
title: Java용 Aspose.PSD를 사용하여 특정 각도로 이미지 회전
linktitle: 특정 각도로 이미지 회전
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 Java에서 이미지 회전을 살펴보세요. 특정 각도로 이미지를 쉽게 회전할 수 있습니다.
weight: 20
url: /ko/java/advanced-image-manipulation/rotate-image-specific-angle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.PSD를 사용하여 특정 각도로 이미지 회전

## 소개

Java 개발의 역동적인 세계에서 이미지 조작은 다양한 애플리케이션에 대한 일반적인 요구 사항입니다. Java용 Aspose.PSD는 강력한 솔루션으로 등장하여 이미지 회전을 쉽게 처리할 수 있는 강력한 기능을 제공합니다. 이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 이미지를 특정 각도로 회전하는 과정을 안내합니다. 세부 사항을 살펴보기 전에 몇 가지 전제 조건을 설정해 보겠습니다.

## 전제조건

이 이미지 회전 여정을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

### 1. 자바 개발 환경
시스템에 Java 개발 환경이 설정되어 있는지 확인하십시오.

### 2. Java 라이브러리용 Aspose.PSD
 Java 라이브러리용 Aspose.PSD를 다운로드하여 설치합니다. 필요한 라이브러리와 문서를 찾을 수 있습니다[여기](https://reference.aspose.com/psd/java/).

### 3. 샘플 이미지
회전하려는 샘플 이미지(예: "sample.psd")를 준비합니다. 문서 디렉토리에 넣으세요.

## 패키지 가져오기

이제 이미지 회전 프로세스를 시작하는 데 필요한 패키지를 가져오겠습니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

이제 이미지를 특정 각도로 회전하는 과정을 일련의 따라하기 쉬운 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 정의

```java
String dataDir = "Your Document Directory";
```

"Your Document Directory"를 문서 디렉터리의 실제 경로로 바꾸십시오.

## 2단계: 원본 및 대상 파일 경로 지정

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

소스 파일 경로를 샘플 이미지 위치로 설정하고 회전된 이미지의 대상 파일 경로를 지정합니다.

## 3단계: 이미지 로드

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

Aspose.PSD를 사용하여 샘플 이미지를 로드합니다.

## 4단계: 이미지 데이터 캐시

```java
if (!image.isCached())
{
    image.cacheData();
}
```

회전 중 성능 향상을 위해 이미지 데이터를 캐시합니다.

## 5단계: 이미지 회전

```java
image.rotate(20f, true, Color.getRed());
```

비례적인 크기를 유지하고 빨간색 배경색을 사용하여 20도 각도로 회전합니다.

## 6단계: 결과 저장

```java
image.save(destName, new JpegOptions());
```

지정된 옵션(이 경우 JpegOptions 사용)을 사용하여 회전된 이미지를 새 파일에 저장합니다.

축하해요! Java용 Aspose.PSD를 사용하여 이미지를 특정 각도로 성공적으로 회전했습니다.

## 결론

이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 이미지를 회전하는 원활한 프로세스를 살펴보았습니다. 라이브러리의 강력한 기능을 통해 Java 개발자는 이미지를 쉽게 조작할 수 있어 수많은 창의적 가능성의 문을 열 수 있습니다.

## FAQ

### Q1: Java용 Aspose.PSD를 사용하여 투명하게 이미지를 회전할 수 있나요?

예, Java용 Aspose.PSD는 투명도가 있는 이미지 회전을 지원합니다. 코드에서 투명도 관련 옵션을 적절하게 처리해야 합니다.

### Q2: 회전이 지원되는 이미지 파일 형식에 제한이 있나요?

아니요, Java용 Aspose.PSD는 PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF 등을 포함한 광범위한 이미지 파일 형식을 지원합니다.

### Q3: 이미지를 음의 각도로 회전할 수 있나요?

 틀림없이! 음의 각도를 지정할 수 있습니다.`image.rotate()` 이미지를 반대 방향으로 회전시키는 방법.

### Q4: Java용 Aspose.PSD는 회전 중에 실시간 이미지 미리보기를 제공합니까?

Java용 Aspose.PSD는 주로 백엔드 이미지 처리에 중점을 둡니다. 실시간 이미지 미리보기를 위해서는 다른 기술을 사용하여 프런트엔드 솔루션을 구현해야 할 수도 있습니다.

### Q5: 도움을 구할 수 있는 Aspose.PSD 커뮤니티 포럼이 있나요?

 네, 방문하실 수 있습니다[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 커뮤니티에 참여하고, 질문하고, 도움을 구하세요.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

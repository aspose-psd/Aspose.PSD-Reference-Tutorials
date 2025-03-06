---
title: Java용 Aspose.PSD를 사용하여 이미지 크기를 비례적으로 조정
linktitle: 이미지 크기를 비례적으로 조정
second_title: Aspose.PSD 자바 API
description: Aspose.PSD로 Java 애플리케이션을 강화하세요. 저희 가이드를 따라 이미지 크기를 비례적으로 쉽게 조정하세요. 지금 이미지 처리 능력을 향상시키십시오.
weight: 17
url: /ko/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.PSD를 사용하여 이미지 크기를 비례적으로 조정

## 소개

Java용 Aspose.PSD를 사용하여 이미지 크기를 비례적으로 조정하는 방법에 대한 단계별 가이드에 오신 것을 환영합니다. 효율적인 이미지 크기 조정 기능으로 Java 애플리케이션을 향상시키려는 경우 제대로 찾아오셨습니다. 이 튜토리얼에서는 명확하고 간결한 단계를 사용하여 프로세스를 안내합니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. Java 환경: 시스템에 Java가 설치되어 있는지 확인하십시오.
2.  Aspose.PSD 라이브러리: Aspose.PSD 라이브러리를 다운로드하여 설치합니다. 필요한 자료를 찾을 수 있습니다[여기](https://releases.aspose.com/psd/java/).

## 패키지 가져오기

필수 구성 요소를 정렬한 후 필요한 패키지를 Java 프로젝트로 가져옵니다. Aspose.PSD 라이브러리가 프로젝트에서 올바르게 참조되는지 확인하세요.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## 1단계: 이미지 로드

크기를 조정하려는 이미지를 Java 애플리케이션에 로드하는 것부터 시작하세요.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## 2단계: 너비와 높이 지정

크기가 조정된 이미지의 새로운 너비와 높이를 결정합니다. 이 예에서는 이미지 크기를 원래 크기의 절반으로 조정합니다.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## 3단계: 크기가 조정된 이미지 저장

형식 옵션(이 경우 PNG)을 지정하여 크기가 조정된 이미지를 원하는 위치에 저장합니다.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

그리고 거기에 있습니다! Java용 Aspose.PSD를 사용하여 이미지 크기를 비례적으로 성공적으로 조정했습니다.

## 결론

이 튜토리얼에서는 Java용 Aspose.PSD 라이브러리를 사용하여 이미지 크기를 비례적으로 조정하는 필수 단계를 다루었습니다. 이제 이미지 처리 개선을 위해 이 기능을 Java 애플리케이션에 쉽게 통합할 수 있습니다.

## FAQ

### Q1: Aspose.PSD는 모든 이미지 형식과 호환됩니까?

 A1: Aspose.PSD는 PSD, PNG, JPEG 등을 포함한 다양한 이미지 형식을 지원합니다. 확인해보세요[선적 서류 비치](https://reference.aspose.com/psd/java/) 포괄적인 목록을 보려면

### Q2: Aspose.PSD를 상업용 프로젝트에 사용할 수 있나요?

 A2: 네, 가능합니다. 방문[구매 페이지](https://purchase.aspose.com/buy) 라이선스 세부정보를 확인하세요.

### Q3: 테스트 목적으로 임시 라이센스를 사용할 수 있습니까?

 A3: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/) 평가를 위해.

### Q4: Aspose.PSD에 대한 지원은 어디서 찾을 수 있나요?

 A4: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 지역 사회 지원 및 지원을 위해.

### Q5: Aspose.PSD 문서에 어떻게 액세스할 수 있나요?

 A5: 자세한 문서를 참조하세요.[여기](https://reference.aspose.com/psd/java/).
`
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

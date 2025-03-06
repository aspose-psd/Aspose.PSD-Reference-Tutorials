---
title: Java용 Aspose.PSD에 가우시안 및 위너 필터 적용
linktitle: 가우스 및 위너 필터 적용
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 Java 이미지 처리를 강화하세요. 놀라운 시각적 결과를 위해 가우시안 및 위너 필터를 단계별로 적용하는 방법을 알아보세요.
weight: 10
url: /ko/java/image-processing/apply-gaussian-wiener-filters/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.PSD에 가우시안 및 위너 필터 적용

## 소개

Java용 Aspose.PSD에서 Gaussian 및 Wiener 필터를 적용하는 방법에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다! 이 가이드에서는 이러한 강력한 필터를 사용하여 이미지를 향상시키는 과정을 안내합니다. Aspose.PSD for Java는 이미지 처리를 위한 강력한 기능 세트를 제공하며 Gaussian 및 Wiener 필터를 적용하면 더욱 부드럽고 세련된 이미지를 얻을 수 있습니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Java 개발 환경: 컴퓨터에 Java 개발 환경이 설정되어 있는지 확인하십시오.

- Java 라이브러리용 Aspose.PSD: Java 라이브러리용 Aspose.PSD를 다운로드하여 설치합니다. 다운로드 링크를 찾을 수 있습니다[여기](https://releases.aspose.com/psd/java/).

## 패키지 가져오기

Java 프로젝트에서 Aspose.PSD에 필요한 패키지를 가져옵니다. 시작하기 위한 샘플 import 문은 다음과 같습니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

이제 가우시안 필터와 위너 필터를 적용하기 위해 예제를 여러 단계로 나누어 보겠습니다.

## 1단계: 이미지 로드

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

이 단계에서는 지정된 디렉터리에서 PSD 이미지 파일을 로드합니다.

## 2단계: RasterImage 확인

```java
if (rasterImage == null) {
    return;
}
```

로드된 이미지가 유효한 RasterImage인지 확인하세요. 그렇지 않으면 프로세스가 종료됩니다.

## 3단계: 필터 옵션 구성

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

GaussWienerFilterOptions 인스턴스를 생성하고 반경 크기와 평탄화 값을 설정하고 필터를 회색조로 적용할지 여부를 지정합니다.

## 4단계: 필터 적용 및 저장

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

마지막으로 구성된 Gaussian 및 Wiener 필터를 RasterImage에 적용하고 결과 이미지를 GIF 형식으로 저장합니다.

## 결론

축하해요! Java용 Aspose.PSD를 사용하여 Gaussian 및 Wiener 필터를 적용하는 방법을 성공적으로 배웠습니다. 원하는 이미지 향상을 달성하기 위해 다양한 매개변수를 실험해 보십시오.

## FAQ

### Q1: PSD 이외의 형식의 이미지에 이러한 필터를 적용할 수 있나요?

A1: 예, Java용 Aspose.PSD는 PSD 이외의 다양한 이미지 형식을 지원합니다.

### Q2: Aspose.PSD for Java 평가판에 제한 사항이 있나요?

A2: 평가판에는 제한 사항이 있으며 유효한 라이센스를 취득하면 전체 기능을 탐색할 수 있습니다.

### Q3: Java용 Aspose.PSD에 대한 지원을 어떻게 받을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 커뮤니티 지원 및 토론을 위해.

### Q4: 테스트 목적으로 사용할 수 있는 임시 라이센스가 있습니까?

 A4: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: Java용 Aspose.PSD에 대한 자세한 문서는 어디에서 찾을 수 있습니까?

 A5: 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/psd/java/) 자세한 정보를 확인하세요.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

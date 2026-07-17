---
date: 2026-07-17
description: Aspose.PSD를 사용한 Java 이미지 처리 튜토리얼로, Gaussian 및 Wiener 필터를 단계별로 적용하여 놀라운
  시각 효과를 얻는 방법을 배웁니다.
keywords:
- java image processing tutorial
- export png java
- gaussian filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: Gaussian 및 Wiener 필터 적용
og_description: Aspose.PSD for Java와 함께 Java 이미지 처리 튜토리얼에서 Gaussian 및 Wiener 필터 적용
  방법을 시연하며, PNG 등 다양한 포맷으로 내보내는 방법도 포함합니다.
og_image_alt: 'Developer guide: Apply Gaussian and Wiener filters to images in Java
  using Aspose.PSD'
og_title: Java 이미지 처리 튜토리얼 – Gaussian 및 Wiener 필터 적용
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Java image processing tutorial using Aspose.PSD learn how to apply
    Gaussian and Wiener filters step‑by‑step for stunning visual results.
  headline: Java Image Processing Tutorial – Apply Gaussian & Wiener Filters
  type: TechArticle
- questions:
  - answer: It smooths an image by averaging neighboring pixels, reducing high‑frequency
      noise.
    question: What does the Gaussian filter do?
  - answer: It performs adaptive smoothing, preserving edges while diminishing noise.
    question: What is the Wiener filter?
  - answer: Aspose.PSD for Java provides built‑in support for both filters.
    question: Which library is used?
  - answer: A trial works for testing, but a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes—Aspose.PSD supports PNG, JPEG, BMP, and many more.
    question: Can I output formats other than GIF?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- gaussian filter
- wiener filter
- export png java
title: Java 이미지 처리 튜토리얼 – Gaussian 및 Wiener 필터 적용
url: /ko/java/image-processing/apply-gaussian-wiener-filters/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 이미지 처리 튜토리얼 – Aspose.PSD를 사용한 가우시안 및 와이너 필터 적용

## 소개

Aspose.PSD for Java를 사용하여 가우시안 및 와이너 필터를 적용하는 방법을 보여주는 **java image processing tutorial**에 오신 것을 환영합니다. 노이즈가 많은 사진을 정리하거나 웹 전송용 그래픽을 준비할 때, 이 필터들은 부드럽고 전문적인 결과를 제공합니다. 다음 몇 분 안에 PSD 파일을 로드하고 필터링된 출력을 GIF로 저장하는 전체 워크플로우를 확인하게 됩니다.

## 빠른 답변
- **Gaussian 필터는 무엇을 하나요?** 이미지를 인접 픽셀을 평균 내어 고주파 노이즈를 감소시켜 부드럽게 합니다.  
- **Wiener 필터란?** 적응형 스무딩을 수행하여 가장자리를 보존하면서 노이즈를 감소시킵니다.  
- **어떤 라이브러리를 사용하나요?** Aspose.PSD for Java는 두 필터 모두에 대한 내장 지원을 제공합니다.  
- **라이선스가 필요합니까?** 시험판은 테스트에 사용할 수 있지만, 실제 운영을 위해서는 상용 라이선스가 필요합니다.  
- **GIF 외에 다른 형식으로 출력할 수 있나요?** 예—Aspose.PSD는 PNG, JPEG, BMP 등 다양한 형식을 지원합니다.

## Java 이미지 처리 튜토리얼이란?

Java 이미지 처리 튜토리얼은 개발자에게 이미지를 로드하고, 필터 적용이나 크기 조정과 같은 변환을 수행한 뒤 원하는 형식으로 저장하는 필수 단계를 안내합니다. 명확한 코드 예제와 설명을 제공함으로써 이미지 조작 기능을 Java 애플리케이션에 직접 통합할 수 있게 하여 외부 도구에 대한 의존성을 줄여줍니다.

## 가우시안 및 와이너 필터를 사용하는 이유

이미지를 로드하고 결합된 Gaussian‑Wiener 필터를 적용하면 입자가 크게 감소하면서 주요 가장자는 선명하게 유지됩니다—웹 그래픽이나 아카이브 스캔을 준비할 때 이상적입니다. Gaussian 부분은 고주파 노이즈를 제거하고, Wiener 부분은 지역 분산에 적응하여 중요한 디테일을 보존합니다.

## 전제 조건

- Java 개발 환경 (JDK 8 이상).  
- Aspose.PSD for Java 라이브러리. **[here](https://releases.aspose.com/psd/java/)**에서 다운로드할 수 있습니다.  
- Java 구문 및 객체 지향 개념에 대한 기본적인 이해.

## 패키지 가져오기

import 문은 Aspose.PSD 클래스를 범위에 가져와 래스터 이미지, 필터 옵션 및 출력 형식을 다룰 수 있게 합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

이러한 import를 통해 이미지 로드, 래스터 조작, 필터 옵션 및 출력 형식에 접근할 수 있습니다.

## 단계 1: 이미지 로드

`RasterImage` 클래스는 픽셀 단위로 처리할 수 있는 래스터 기반 이미지를 나타냅니다.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

지정된 디렉터리에서 PSD 파일을 로드하고 이를 `RasterImage`로 캐스팅하여 픽셀 데이터에 접근합니다.

## 단계 2: RasterImage 확인

안전 검사를 통해 로드된 파일이 래스터 기반인지 확인합니다; 그렇지 않으면 루틴이 정상적으로 종료됩니다.

```java
if (rasterImage == null) {
    return;
}
```

## 단계 3: 필터 옵션 구성

`GaussWienerFilterOptions` 클래스는 하나의 객체에서 Gaussian 및 Wiener 매개변수를 세밀하게 조정할 수 있게 합니다.

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

- 첫 번째 인수(`12`)는 Gaussian 커널의 반경 크기를 정의합니다.  
- 두 번째 인수(`3`)는 Wiener 알고리즘에서 사용되는 스무스 값을 설정합니다.  
- `setGrayscale(true)`는 필터가 그레이스케일로 작업하도록 지정하며, 이는 노이즈 감소에 더 깨끗한 결과를 제공하는 경우가 많습니다.

## 단계 4: 필터 적용 및 저장

`filter` 메서드는 구성된 Gaussian‑Wiener 조합을 이미지 전체 영역에 적용합니다. 마지막으로 `GifOptions`를 사용하여 처리된 이미지를 GIF로 저장합니다. `GifOptions`를 `PngOptions`, `JpegOptions` 등으로 교체하면 **export PNG Java** 또는 다른 형식으로 내보낼 수 있습니다.

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

## 일반적인 문제 및 팁

- **Null RasterImage:** 소스 파일이 PSD 또는 다른 래스터 호환 형식인지 확인하십시오.  
- **Performance:** 큰 이미지일 경우 시간이 오래 걸릴 수 있으니 반경을 줄이거나 먼저 축소된 복사본을 처리하는 것을 고려하십시오.  
- **Color vs. Grayscale:** 색상을 유지해야 하면 `options.setGrayscale(false)`로 설정하십시오.

## 자주 묻는 질문

**Q1: 이 필터를 PSD가 아닌 다른 형식의 이미지에도 적용할 수 있나요?**  
A1: 예, Aspose.PSD for Java는 PNG, JPEG, BMP, GIF 등 PSD 외의 다양한 이미지 형식을 지원합니다.

**Q2: Aspose.PSD for Java 체험판에 제한이 있나요?**  
A2: 체험판은 출력 크기를 제한하고 워터마크를 추가합니다. 전체 기능을 사용하려면 유효한 라이선스를 획득하십시오.

**Q3: Aspose.PSD for Java에 대한 지원을 어떻게 받을 수 있나요?**  
A3: 커뮤니티 지원 및 공식 답변을 위해 **[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)**을 방문하십시오.

**Q4: 테스트용 임시 라이선스를 제공하나요?**  
A4: 예, **[here](https://purchase.aspose.com/temporary-license/)**에서 임시 라이선스를 얻을 수 있습니다.

**Q5: Aspose.PSD for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?**  
A5: 심층 API 레퍼런스와 추가 예제를 위해 **[documentation](https://reference.aspose.com/psd/java/)**을 참고하십시오.

## 결론

이제 Aspose.PSD for Java를 사용하여 **Gaussian** 및 Wiener 필터를 **apply**하는 전체 **java image processing tutorial**을 완료했습니다. 다양한 반경 및 스무스 값을 실험하고, 그레이스케일을 전환하며, PNG와 같은 다른 출력 형식도 시도해 보면서 필터가 이미지에 어떤 영향을 주는지 확인하십시오. 즐거운 코딩 되세요!

---

**Last Updated:** 2026-07-17  
**Tested With:** Aspose.PSD for Java 23.12 (latest at time of writing)  
**Author:** Aspose

## 관련 튜토리얼

- [단계별 필터 - Aspose.PSD for Java를 사용한 모션 와이너 필터 적용](/psd/java/image-processing/apply-motion-wiener-filters/)
- [단계별 필터 - Median 및 Wiener 필터 적용 (Java)](/psd/java/image-processing/apply-median-wiener-filters/)
- [Aspose.PSD for Java에서 PNG 파일 필터링 방법](/psd/java/optimizing-png-files/apply-filters-png-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
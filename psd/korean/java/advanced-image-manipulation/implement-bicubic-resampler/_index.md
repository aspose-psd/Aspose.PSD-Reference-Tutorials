---
date: 2025-12-01
description: Aspose.PSD의 Bicubic Resampler를 사용하여 Java에서 고품질 이미지 스케일링을 구현하는 방법을 배워보세요.
  뛰어난 결과를 위한 단계별 가이드를 따라가세요.
language: ko
linktitle: Implement Bicubic Resampler
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java에서 Bicubic Resampler를 사용한 고품질 이미지 스케일링
url: /java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java에서 Bicubic Resampler를 사용한 고품질 이미지 스케일링

## 소개

고품질 이미지 스케일링은 시각적 충실도를 손상시키지 않고 그래픽을 크기 조정해야 할 때 자주 요구됩니다. Aspose.PSD for Java는 **Bicubic Resampler**를 제공하여 PSD 파일 및 기타 지원 형식에 대해 부드럽고 선명한 결과를 제공합니다. 이 튜토리얼에서는 Bicubic Resampler를 단계별로 구현하는 방법을 정확히 배워, 오늘 바로 Java 애플리케이션에 고품질 이미지 스케일링을 적용할 수 있습니다.

## 빠른 답변
- **Bicubic Resampler는 무엇을 하나요?** 이미지 크기를 조정할 때 세부 정보를 보존하는 정교한 보간 알고리즘을 적용합니다.  
- **사용 가능한 ResizeType 값은 무엇인가요?** `CubicConvolution`과 `Bell`은 Aspose.PSD에서 제공하는 두 가지 Bicubic 옵션입니다.  
- **코드를 실행하려면 라이선스가 필요합니까?** 평가용으로는 임시 라이선스로 동작하지만, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **필요한 Java 버전은 무엇인가요?** 최신 Aspose.PSD 라이브러리와 호환되는 Java 8 이상 런타임이면 됩니다.  
- **같은 API로 다른 이미지 형식(PNG, JPEG)도 크기 조정할 수 있나요?** 예, Aspose.PSD는 여러 이미지 유형을 지원하지만 예제는 PSD에 초점을 맞춥니다.

## 고품질 이미지 스케일링이란 무엇인가요?

고품질 이미지 스케일링은 이미지의 가장자리 선명도, 부드러운 그라데이션, 정확한 색상 표현을 유지하면서 크기를 조정하는 것을 의미합니다. Bicubic Resampler는 주변 픽셀 값을 고려(큐빅 컨볼루션 또는 Bell 알고리즘 사용)하여 각 새로운 픽셀을 계산함으로써, 최근접 이웃이나 bilinear 방식에 비해 보다 자연스러운 결과를 제공합니다.

## 고품질 이미지 스케일링에 Bicubic Resampler를 사용하는 이유는?

- **세부 정보 보존:** 섬세한 텍스처와 선 작업이 큰 크기 변경 후에도 선명하게 유지됩니다.  
- **아티팩트 감소:** 단순한 알고리즘에서 흔히 발생하는 링잉 및 블러링을 최소화합니다.  
- **쉬운 통합:** 한 줄 메서드 호출(`image.resize`)로 코드를 다시 작성하지 않고도 알고리즘을 전환할 수 있습니다.  

## 전제 조건

시작하기 전에 다음이 준비되어 있는지 확인하세요:

- **Aspose.PSD for Java** – 최신 JAR 파일을 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)에서 다운로드합니다.  
- **Java Development Kit** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.  
- **Sample PSD file** – 테스트 이미지(예: `sample_bicubic.psd`)를 알려진 디렉터리에 배치합니다.  

## 패키지 가져오기

Java 클래스에 필요한 import 구문을 추가합니다. 이는 핵심 Aspose.PSD 클래스와 `ResizeType` 열거형을 가져옵니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 1단계: 이미지 로드

먼저, 크기 조정하려는 원본 PSD 파일을 로드합니다. `Your Document Directory`를 실제 경로로 교체하세요.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

## 2단계: Cubic Convolution으로 리사이즈 (고품질)

이제 **Cubic Convolution** 알고리즘을 적용합니다. 이는 고품질 이미지 스케일링을 제공하는 두 가지 Bicubic 옵션 중 하나입니다. 예제에서는 이미지를 300 × 300 픽셀로 리사이즈합니다.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

## 3단계: Bell 알고리즘으로 리사이즈 (대안 고품질)

조금 다른 스무딩 효과를 제공하는 **Bell** 알고리즘을 선호한다면 동일한 방식으로 사용할 수 있습니다. 비교를 공정하게 유지하기 위해 원본 이미지를 다시 로드하는 점에 유의하세요.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

다른 크기나 파일 형식으로 실험해도 좋습니다—그에 맞게 매개변수만 조정하면 됩니다.

## 일반적인 함정 및 팁

- **잘못된 경로:** `dataDir`이 OS에 맞는 파일 구분자(`/` 또는 `\`)로 끝나는지 확인하세요.  
- **라이선스 예외:** 유효한 라이선스 없이 실행하면 출력 이미지에 워터마크가 추가될 수 있습니다.  
- **메모리 사용량:** 큰 PSD 파일은 상당한 메모리를 소모할 수 있으므로 저장 후 이미지(`image.dispose()`)를 해제하는 것을 고려하세요.  

## 자주 묻는 질문

**Q: Aspose.PSD for Java를 다른 이미지 형식과 함께 사용할 수 있나요?**  
A: 예, 라이브러리는 PSD, PNG, JPEG, TIFF, BMP 등 다양한 형식을 지원합니다.

**Q: Aspose.PSD for Java용 임시 라이선스를 제공하나요?**  
A: 예, [여기](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 받을 수 있습니다.

**Q: Aspose.PSD for Java에 대한 지원은 어디서 찾을 수 있나요?**  
A: 지원 관련 문의는 Aspose.PSD 포럼 [여기](https://forum.aspose.com/c/psd/34)에서 확인하세요.

**Q: Aspose.PSD for Java 라이브러리를 다운로드할 수 있나요?**  
A: 예, 릴리스 페이지 [여기](https://releases.aspose.com/psd/java/)에서 라이브러리를 다운로드하세요.

**Q: Aspose.PSD for Java를 어떻게 구매하나요?**  
A: 구매 페이지 [여기](https://purchase.aspose.com/buy)에서 Aspose.PSD for Java를 구매할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2025-12-01  
**테스트 환경:** Aspose.PSD for Java 24.11 (작성 시 최신 버전)  
**작성자:** Aspose
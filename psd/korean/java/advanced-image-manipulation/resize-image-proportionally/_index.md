---
date: 2025-12-08
description: Aspose.PSD를 사용하여 Java에서 PSD를 PNG로 변환하고 이미지를 비례적으로 리사이즈하는 방법을 배웁니다. 이
  단계별 튜토리얼에서는 이미지 캐싱, 리사이즈 및 PNG 저장에 대해 다룹니다.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD를 PNG로 변환하고 비율에 맞게 크기 조정하는 방법
url: /ko/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 PNG로 변환하고 Java용 Aspose.PSD로 비례적으로 크기 조정하는 방법

## 소개

원본 종횡비를 유지하면서 **PSD를 PNG로 변환**해야 한다면, 올바른 곳에 오셨습니다. 이 튜토리얼에서는 Java에서 이미지 파일을 비례적으로 **크기 조정하는 방법**을 보여주는 **Aspose.PSD 튜토리얼**을 전체적으로 살펴보고, 최적 성능을 위해 이미지를 캐시한 뒤 최종적으로 PNG로 저장하는 과정을 안내합니다. 끝까지 따라오시면 이 워크플로를 모든 Java 기반 이미지 처리 파이프라인에 통합할 수 있게 됩니다.

## 빠른 답변
- **Aspose.PSD가 PSD를 PNG로 변환할 수 있나요?** 예 – PSD를 로드하고 `PngOptions`로 저장하면 됩니다.
- **라이브러리가 비례적 크기 조정을 지원하나요?** 물론입니다; `resizeWidthProportionally`와 `resizeHeightProportionally`를 사용하세요.
- **이미지를 먼저 캐시해야 하나요?** 캐시(`image.cacheData()`)는 큰 PSD 파일의 성능을 향상시킵니다.
- **필요한 Java 버전은?** Java 8 이상이면 완전히 지원됩니다.
- **프로덕션에 라이선스가 필요합니까?** 예, 상업용 라이선스를 사용하면 평가 워터마크가 제거됩니다.

## “PSD를 PNG로 변환”이란 무엇이며 왜 중요한가요?

포토샵 문서(PSD)를 포터블 네트워크 그래픽스(PNG) 파일로 변환하면 레이어 디자인을 가볍고 웹 친화적인 형식으로 공유할 수 있습니다. PNG는 투명성을 유지하고 무손실 품질을 제공하므로 UI 자산, 썸네일 또는 이미지 품질이 중요한 모든 상황에 이상적입니다.

## Java에서 이미지를 비례적으로 크기 조정하는 이유는?

종횡비를 왜곡하지 않고 **이미지를 비례적으로 크기 조정**하면 다양한 화면에서 그래픽이 자연스럽게 보입니다. `Aspose.PSD` API는 비례 스케일링을 위한 전용 메서드를 제공하며, 자동으로 맞는 높이 또는 너비를 계산해 수동 계산 오류를 방지합니다.

## 전제 조건

코드에 들어가기 전에 다음이 준비되어 있는지 확인하세요:

1. **Java Development Kit (JDK)** – Java 8 이상이 설치되어 있어야 합니다.
2. **Aspose.PSD for Java** – 공식 사이트에서 최신 JAR를 [here](https://releases.aspose.com/psd/java/)에서 다운로드하세요.
3. 프로젝트에서 참조할 수 있는 디렉터리에 샘플 PSD 파일(`sample.psd`)을 배치합니다.

## 패키지 가져오기

Java 클래스에 필요한 import를 추가하세요. 이 클래스들은 이미지 로드, 캐시, 크기 조정 및 PNG 출력 옵션에 접근할 수 있게 해줍니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## 단계 1: PSD 이미지 로드

먼저, 원본 PSD 파일을 로드합니다. 파일이 크면 이미지 데이터를 캐시하여 이후 작업 시 메모리 사용량을 줄일 수 있습니다.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## 단계 2: 이미지 비례적으로 크기 조정 (Java)

이제 새로운 크기를 결정합니다. 이 예제에서는 종횡비를 유지하면서 이미지를 원본 크기의 **절반**으로 축소합니다. 필요에 따라 목표 너비나 높이를 조정할 수 있습니다.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Pro tip:** `resizeWidthProportionally` *또는* `resizeHeightProportionally` 중 하나를 사용하세요—라이브러리가 자동으로 다른 차원을 계산해 이미지가 비례를 유지합니다.

## 단계 3: 크기 조정된 이미지를 PNG로 저장

마지막으로, 크기 조정된 이미지를 PNG 형식으로 내보냅니다. 이 단계가 **PSD를 PNG로 변환** 워크플로를 완성합니다.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

코드를 실행하면 원본 PSD의 절반 크기이면서 동일한 시각적 품질과 왜곡이 없는 PNG 파일을 찾을 수 있습니다.

## 일반적인 문제 및 해결책

| Issue | Cause | Fix |
|-------|-------|-----|
| **OutOfMemoryError** | 큰 PSD가 캐시되지 않음 | `image.cacheData()`를 호출하여 크기 조정 전에 캐시합니다. |
| **Blank PNG output** | 잘못된 파일 경로 | `dataDir`와 쓰기 권한을 확인합니다. |
| **Aspect ratio looks off** | 너비와 높이를 수동으로 모두 사용 | Aspose.PSD에서 제공하는 비례 메서드를 사용합니다. |

## 자주 묻는 질문

**Q: Aspose.PSD가 모든 이미지 형식과 호환되나요?**  
A: Aspose.PSD는 PSD, PNG, JPEG, BMP, GIF 등 다양한 형식을 지원합니다. 전체 목록은 [문서](https://reference.aspose.com/psd/java/)에서 확인하세요.

**Q: Aspose.PSD를 상업 프로젝트에 사용할 수 있나요?**  
A: 예. [Aspose 스토어](https://purchase.aspose.com/buy)에서 상업용 라이선스를 구매하세요.

**Q: 테스트용 임시 라이선스를 제공하나요?**  
A: 물론입니다 – 평가용으로 임시 라이선스를 [here](https://purchase.aspose.com/temporary-license/)에서 요청하세요.

**Q: 커뮤니티 지원은 어디서 찾을 수 있나요?**  
A: 질문을 하고 솔루션을 공유하기에 좋은 곳은 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)입니다.

**Q: 전체 API 레퍼런스는 어떻게 확인하나요?**  
A: 자세한 API 문서는 [here](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

## 결론

이제 **PSD를 PNG로 변환**, 이미지를 비례적으로 크기 조정, 그리고 Aspose.PSD for Java를 사용한 효율적인 캐시 처리를 할 수 있게 되었습니다. 이러한 단계를 애플리케이션에 통합하면 네이티브 포토샵 설치 없이도 빠르고 고품질의 이미지 처리를 제공할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2025-12-08  
**테스트 환경:** Aspose.PSD 24.12 for Java  
**작성자:** Aspose
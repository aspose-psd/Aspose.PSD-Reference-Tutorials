---
date: 2026-02-09
description: Aspose.PSD를 사용하여 Java에서 PSD를 PNG로 변환하고 이미지를 비례적으로 크기 조정하는 방법을 배웁니다. 이
  단계별 튜토리얼에서는 이미지 캐싱, 크기 조정 및 PNG로 저장하는 내용을 다룹니다.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD를 PNG로 변환하고 비율에 맞게 크기 조정하는 방법
url: /ko/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD를 PNG로 변환하고 더욱 효과적으로 크기를 조정하는 방법

## 소개

원본 종횡비를 유지하면서 **PSD를 PNG로 변환**해야 하며, 여기가 바로 원하는 곳입니다. 이 **Aspose.PSD Java** 튜토리얼에서는 **java 이미지 처리 튜토리얼** 전체를 샘플을 따라가며 **이미지 크기만큼 조정** 방법, 성능을 향상하는 이미지 캐시, 그리고 최종적으로 PNG로 저장하는 커뮤니케이션을 보여줍니다. 튜토리얼을 마치면 파이프플로우를 모든 Java 기반 이미지 처리라인에 통합할 수 있습니다.

## 빠른 답변
- **Aspose.PSD가 PSD를 PNG로 변환할 수 있나요?** 예 – PSD를 로드한 후 `PngOptions`로 생성하면 됩니다.
- **라이브러가 규모의 조정을 지원하는데요?** 물론입니다; `resizeWidthProportional`과 `resizeHeightProportional`을 사용하세요.
- **이미지를 먼저 캐시해야 합니까?** 캐시(`image.cacheData()`)를 사용하면 디스플레이 PSD 파일의 성능이 향상됩니다.
- **Java 버전이 필요합니까?** Java8이 있으면 확실히 지원됩니다.
- **프로덕션에서 권한이 필요한가요?** 예, 워터 머신을 사용하면 평가용 마크가 제거됩니다.

## "PSD를 PNG로 변환"이란 무엇이며 왜 중요한가요?

Photoshop 문서(PSD)를 사용하여 포터블 그래픽(PNG) 파일로 변환하면 레이어 디자인을 편리한 웹 기반 형식으로 공유할 수 있습니다. PNG는 투명도를 유지하고 부정적인 품질을 제공하므로 UI ​​자산, 썸네일 또는 이미지 품질이 모든 상황에 중요합니다.

## Java에서 이미지 크기를 비례적으로 조정하는 이유는 무엇입니까?

**이미지가 작은 크기**는 종횡비를 조정하지 않고 그래픽이 다양한 화면에서 크기를 보여줍니다. `Aspose.PSD` API는 **비례적으로 이미지 크기를 조정**하는 것을 환영합니다. 따라서, 높은 또는 더 나은 방법을 선택하는 다른 사람들이 자동으로 힘쓰는 습관을 들이는 것을 거부합니다.

## 이것이 개발자에게 중요한 이유

- **PSD 파일 크기 감소** – 게이밍 PSD를 변환하면 축소될 수 있습니다.
- **일관된 UI 렌더링** – 충분한 크기는 아이콘과 그래픽이 기기마다 표시 균형을 유지하도록 합니다.
- **Photoshop 종속성 없음** – 서버나 CI 파이프라인에서 Photoshop을 설치하지 않는 해당 작업을 수행할 수 있습니다.

## 전제 조건

코드 작성을 시작하기 전에 다음을 준비하세요:

1. **JDK(Java Development Kit)** – Java8이 설치되어 있어야 합니다.
2. **Aspose.PSD for Java** – 공식 사이트[여기](https://releases.aspose.com/psd/java/)에서 최신 JAR을 다운로드합니다.
3. 프로젝트에서 참조할 수 있는 원본 PSD 파일(`sample.psd`)을 배치합니다.

## 패키지 가져오기

Java 클래스에 import 문을 추가해야 합니다. 이 클래스들은 이미지 로드, 캐시, 크기 및 PNG 반환 옵션에 접근할 수 있을 것 같습니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```
## 1단계: PSD 이미지 불러오기

먼저 원본 PSD 파일을 로드합니다. 파일이 크다면 이미지 데이터를 캐시하면 이후 작업 시 메모리 사용량이 감소합니다.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## 2단계: 이미지 크기 비례 조정 (Java)

새로운 차원을 결정합니다. 이 예제에서는 원본 크기의 **절반**으로 축소하면서 종횡비를 유지합니다. 필요에 따라 목표 너비 또는 높이를 조정하면 됩니다.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **전문가 팁:** `resizeWidthProportionally` *또는* `resizeHeightProportionally` 중 하나만 사용하면, 라이브러리가 자동으로 다른 차원을 계산해 이미지가 비례를 유지하도록 합니다.

## 3단계: 크기 조정된 이미지를 PNG로 저장

마지막으로 크기 조정된 이미지를 PNG 형식으로 내보냅니다. 이 단계가 **convert PSD to PNG** 워크플로우를 완성합니다.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

코드가 실행되면 원본 PSD의 절반 크기이면서 동일한 시각적 품질을 유지하고 왜곡이 없는 PNG 파일이 생성됩니다.

## 일반적인 문제 및 솔루션

| 문제 | 원인 | 치료방법 |
|------|------|------------|
| **메모리 부족 오류** | 큰 PSD가 캐시되지 않음 | Resize 전에 `image.cacheData()` 호출 |
| **빈 PNG 출력** | 잘못된 파일 경로 | `dataDir`와 쓰기 권한 확인 |
| **가로세로 비율이 떨어져 보임** | 너비와 높이를 모두 수동으로 사용 | Aspose.PSD에서 제공하는 방법 사용 |

## PSD 파일 크기를 줄이기 위한 팁

- 파일을 불러오기 전에 **불필요한 레이어를 잘라내세요**.
- 치수를 조기에 축소하려면 위와 같이 **비례적으로 크기를 조정**하세요.
- 과도한 데이터를 방지하려면 **적절한 비트 깊이의 PNG로 저장**하세요.

## 자주 묻는 질문

**Q: Aspose.PSD가 모든 이미지 형식을 지원하고 있습니까?**
A: Aspose.PSD는 PSD, PNG, JPEG, BMP, GIF 등 다양한 형식을 지원합니다. 전체 목록은 [문서](https://reference.aspose.com/psd/java/)를 참고하세요.

**Q: Aspose.PSD를 프로젝트에 사용할 수 있나요?**
답: 예. [Aspose 스토어](https://purchase.aspose.com/buy)에서 기계를 구매하세요.

**Q: 테스트용 인스턴스를 제공합니까?**
A: 물론입니다 – 평가용으로 [여기](https://purchase.aspose.com/temporary-license/)에서 인스턴스를 요청하세요.

**Q: 커뮤니티 지원을 거부할 수 있나요?**
A: [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)에서 질문하고 솔루션을 공유할 수 있습니다.

**Q: 전체 API는 어떻게 지내나요?**
A: 별도의 API 문서는 [여기](https://reference.aspose.com/psd/java/)에서 처리할 수 있습니다.

## 결론

이제 **PSD를 PNG로 변환**, **이미지 크기 조정**, 그리고 Java용 Aspose.PSD를 사용하여 효율적으로 처리하는 방법을 더 많이 얻습니다. 이러한 단계를 통합하면 Photoshop 설치 없이도 빠른 고품질의 이미지 처리를 제공할 수 있습니다. 이 **aspose psd java** 방식 방식은 모든 **java 이미지 처리 튜토리얼**의 특별한 수 있는 부분이며, PSD 파일 크기를 제어하면서 표시도를 유지하는 데 도움이 됩니다.

---

**최종 업데이트:** 2026-02-09
**테스트 대상:** Java용 Aspose.PSD 24.12
**저자:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

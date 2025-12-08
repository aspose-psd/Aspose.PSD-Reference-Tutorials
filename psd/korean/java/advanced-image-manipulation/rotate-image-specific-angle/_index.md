---
date: 2025-12-08
description: Aspose.PSD를 사용하여 Java에서 특정 각도로 이미지를 회전하는 방법을 배워보세요. 이 가이드에서는 Java 이미지
  회전, 특정 각도 회전, 배경 처리 등 다양한 내용을 다룹니다.
language: ko
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 특정 각도로 이미지 회전하는 방법
url: /java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 특정 각도로 이미지 회전하기

## 소개

Java 애플리케이션에서 프로그래밍 방식으로 **이미지 회전 방법**이 필요하다면, Aspose.PSD for Java는 무거운 작업을 처리해 주는 깔끔하고 고성능의 API를 제공합니다. 사진 편집기 구축, 썸네일 생성, 웹 서비스용 자산 준비 등, 정확한 각도로 이미지를 회전하는 것은 흔한 요구사항입니다. 이 튜토리얼에서는 PSD 파일을 로드하고 회전된 결과를 저장하는 전체 과정을 단계별로 살펴보면서 캐싱 및 배경 처리와 같은 모범 사례도 강조합니다.

> **빠른 답변**  
> - **Java에서 이미지를 회전하기에 가장 좋은 라이브러리는?** Aspose.PSD for Java.  
> - **임의의 각도로 회전할 수 있나요?** 예, `rotate` 메서드는 `float` 각도(양수 또는 음수)를 받습니다.  
> - **개발에 라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있지만, 프로덕션에서는 라이선스가 필요합니다.  
> - **지원되는 이미지 포맷은?** PSD, JPEG, PNG, TIFF, GIF, BMP 등 다수.  
> - **빈 공간의 배경 색을 어떻게 지정하나요?** `rotate` 메서드에 `Color` 인스턴스를 전달하면 됩니다.

## Java에서 이미지 회전이란?

이미지 회전은 픽셀 매트릭스를 피벗 포인트(보통 중심)를 기준으로 주어진 각도만큼 돌리는 것을 의미합니다. Java에서는 `Graphics2D`를 사용해 수동으로 구현할 수 있지만, Aspose.PSD는 수학 연산을 추상화하고 색 깊이 차이를 처리하며 PSD 파일 작업 시 레이어 정보를 보존합니다.

## 이미지 회전에 Aspose.PSD를 사용하는 이유

- **정밀도:** 품질 손실 없이 소수점 단위 각도 회전 가능.  
- **성능:** 내장 캐싱(`image.cacheData()`)으로 대용량 파일 처리 속도 향상.  
- **배경 제어:** 회전으로 생긴 빈 공간을 채울 배경 색 지정 가능.  
- **포맷 유연성:** PSD 로드 후 JPEG, PNG 등 지원 포맷으로 출력.

## 전제 조건

시작하기 전에 다음을 준비하세요:

1. **Java Development Kit (JDK 8 이상)** – 작동 중인 Java IDE 또는 커맨드라인 환경.  
2. **Aspose.PSD for Java** – 최신 JAR 파일을 [Aspose.PSD Java 페이지](https://reference.aspose.com/psd/java/)에서 다운로드.  
3. **샘플 PSD 파일** – 예: 코드에서 참조할 수 있도록 `sample.psd`를 폴더에 배치.

## 패키지 가져오기

먼저 필요한 클래스를 가져옵니다. 회전 각도와 관계없이 이 임포트는 동일합니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 단계별 가이드

### Step 1: Define Your Document Directory

소스 PSD가 위치하고 출력 파일이 저장될 폴더 경로를 설정합니다.

```java
String dataDir = "Your Document Directory";
```

> **프로 팁:** 절대 경로나 `System.getProperty("user.dir")`를 사용하면 상대 경로로 인한 예기치 않은 문제를 방지할 수 있습니다.

### Step 2: Specify Source and Destination File Paths

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

출력 파일 이름(`destName`)을 `.png`, `.tiff` 등 지원되는 확장자로 자유롭게 변경할 수 있습니다.

### Step 3: Load the Image

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load`는 파일 포맷을 자동으로 감지하고 래스터 기반 작업을 위한 구체적인 `RasterImage` 객체를 반환합니다.

### Step 4: Cache Image Data (Optional but Recommended)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

이미지를 메모리에 캐시하면 이후 변환 작업이 빨라집니다—특히 대용량 PSD 파일에 유용합니다.

### Step 5: Rotate the Image

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – 회전 각도(도)이며 `float` 형식입니다. 원하는 각도로 바꾸세요(예: `-45f`는 시계 반대 방향).  
- **true** – 원본 종횡비를 유지하면서 회전된 이미지를 모두 담을 수 있도록 캔버스를 확장합니다.  
- **Color.getRed()** – 회전으로 생긴 빈 코너를 채울 배경 색입니다. 필요에 따라 `Color.getWhite()` 등으로 교체하세요.

### Step 6: Save the Result

```java
image.save(destName, new JpegOptions());
```

`JpegOptions`를 사용해 품질, 압축 등 JPEG 전용 설정을 제어할 수 있습니다. 무손실 출력을 원한다면 `PngOptions`로 교체하면 됩니다.

## 일반적인 문제와 해결책

| 문제 | 원인 | 해결 방법 |
|------|------|-----------|
| **회전 후 빈 코너가 검게 보임** | 배경 색이 지정되지 않음 | `rotate`에 `Color`(예: `Color.getWhite()`)를 전달하세요. |
| **대용량 PSD 처리 시 메모리 부족** | 이미지가 캐시되지 않음 | 처리 전에 `image.cacheData()`를 호출하세요. |
| **각도 방향이 예상과 다름** | 양수/음수 각도 혼동 | 시계 방향 회전은 음수 값을 사용(또는 좌표계에 따라 반대)하세요. |
| **변경 사항이 저장되지 않음** | `save` 호출 누락 | 회전 후 반드시 `image.save(...)`를 실행하세요. |

## 자주 묻는 질문

**Q: Aspose.PSD for Java로 투명도를 유지한 채 이미지를 회전할 수 있나요?**  
A: 가능합니다. 불투명한 배경 색을 지정하지 않으면 알파 채널이 보존되어 투명한 코너가 유지됩니다.

**Q: 회전이 지원되지 않는 이미지 포맷이 있나요?**  
A: 없습니다. Aspose.PSD는 PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF 등 대부분의 포맷을 지원합니다.

**Q: 음수 각도로 회전할 수 있나요?**  
A: 물론입니다. `rotate`에 음수 `float` 값을 전달하면 시계 방향 회전이 됩니다(예: `-30f`).

**Q: 회전 중 실시간 이미지 미리보기를 제공하나요?**  
A: API는 서버 측 전용입니다. 실시간 미리보기가 필요하면 회전된 비트맵을 Swing, JavaFX 등 UI 프레임워크에 적용하고 뷰를 갱신하세요.

**Q: Aspose.PSD 커뮤니티 포럼이 있나요?**  
A: 네, 질문과 경험을 공유하려면 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)을 방문하세요.

## 결론

이제 Aspose.PSD for Java를 사용해 특정 각도로 이미지 파일을 회전하는 방법을 알게 되었습니다. 캐싱, 배경 색 제어, 유연한 출력 옵션을 활용하면 어떤 Java 기반 이미지 워크플로에도 정밀 회전 기능을 손쉽게 통합할 수 있습니다.

---

**Last Updated:** 2025-12-08  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-02-12
description: Aspose.PSD를 사용하여 Java에서 특정 각도로 이미지를 회전하는 방법을 배웁니다. 이 가이드는 이미지 회전, 각도별
  이미지 회전 및 배경 색상 처리 방법을 보여줍니다.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 특정 각도로 이미지 회전하는 방법
url: /ko/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 특정 각도로 이미지 회전하는 방법

## 소개

Java 애플리케이션에서 프로그래밍 방식으로 **이미지를 회전하는 방법**이 필요하다면, Aspose.PSD for Java는 무거운 작업을 처리해주는 깔끔하고 고성능 API를 제공합니다. 사진 편집기 구축, 썸네일 생성, 웹 서비스용 자산 준비 등 정확한 각도로 이미지를 회전하는 것은 흔한 요구 사항입니다. 이 튜토리얼에서는 PSD 파일을 로드하고 회전된 결과를 저장하는 전체 과정을 단계별로 살펴보면서 캐싱 및 배경 처리와 같은 모범 사례도 강조합니다.

## 빠른 답변
- **Java에서 이미지를 회전하기에 가장 적합한 라이브러리는 무엇인가요?** Aspose.PSD for Java.  
- **임의의 각도로 회전할 수 있나요?** 예, `rotate` 메서드는 `float` 각도(양수 또는 음수)를 허용합니다.  
- **개발에 라이선스가 필요합니까?** 무료 체험판으로 테스트가 가능하며, 프로덕션에서는 라이선스가 필요합니다.  
- **지원되는 이미지 형식은 무엇인가요?** PSD, JPEG, PNG, TIFF, GIF, BMP 등 다수.  
- **빈 공간의 배경 색상을 어떻게 설정하나요?** `rotate` 메서드에 `Color` 인스턴스를 전달합니다.

## Java에서 이미지 회전이란?

이미지 회전은 픽셀 매트릭스를 기준점(보통 중심) 주위로 주어진 각도만큼 회전시키는 것을 의미합니다. Java에서는 `Graphics2D`를 사용해 수동으로 구현할 수 있지만, Aspose.PSD는 수학을 추상화하고 다양한 색상 깊이를 처리하며 PSD 파일 작업 시 레이어 정보를 보존합니다.

## 이미지 회전에 Aspose.PSD를 사용하는 이유

- **정밀도:** 품질 손실 없이 임의의 소수 각도로 회전합니다.  
- **성능:** 내장 캐싱(`image.cacheData()`)으로 대용량 파일을 빠르게 처리합니다.  
- **배경 제어:** 회전으로 생긴 빈 공간을 채우기 위해 배경 색상을 지정합니다.  
- **포맷 유연성:** PSD를 로드하고 JPEG, PNG 등 지원되는 포맷으로 출력합니다.

## 전제 조건

시작하기 전에 다음이 준비되어 있는지 확인하세요:

1. **Java Development Kit (JDK 8 이상)** – 작동하는 Java IDE 또는 명령줄 환경.  
2. **Aspose.PSD for Java** – 최신 JAR를 [Aspose.PSD Java 페이지](https://reference.aspose.com/psd/java/)에서 다운로드합니다.  
3. **샘플 PSD 파일** – 예: 코드에서 참조할 수 있는 폴더에 `sample.psd`를 배치합니다.

## 패키지 가져오기

먼저, 필요한 클래스를 가져옵니다. 회전 각도와 관계없이 이 import 구문은 동일합니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 단계별 가이드

### 단계 1: 문서 디렉터리 정의

소스 PSD가 위치하고 출력이 기록될 폴더를 설정합니다.

```java
String dataDir = "Your Document Directory";
```

> **팁:** 절대 경로 또는 `System.getProperty("user.dir")`를 사용하여 상대 경로로 인한 문제를 방지하세요.

### 단계 2: 소스 및 대상 파일 경로 지정

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

`destName`을 출력 요구에 따라 지원되는 확장자(`.png`, `.tiff` 등)로 변경할 수 있습니다.

### 단계 3: 이미지 로드

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load`는 파일 형식을 자동으로 감지하고 래스터 기반 작업을 위한 구체적인 `RasterImage`를 반환합니다.

### 단계 4: 이미지 데이터 캐시(선택 사항이지만 권장)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

캐싱은 이미지 픽셀을 메모리에 저장하여 이후 변환을 빠르게 수행합니다—특히 대용량 PSD 파일에 유용합니다.

### 단계 5: 이미지 회전

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – 회전 각도(도, float). 이 값을 변경하여 원하는 각도로 회전할 수 있습니다. 예: 반시계 방향은 `-45f`.  
- **true** – 회전된 이미지를 맞추기 위해 캔버스를 확장하면서 원본 종횡비를 유지합니다.  
- **Color.getRed()** – 회전으로 생긴 빈 코너를 채우는 배경 색상. 필요에 따라 `Color.getWhite()` 또는 다른 색상으로 교체합니다.

#### Java에서 각도로 이미지 회전

`rotate` 메서드는 모든 부동소수점 값을 허용하므로 `30f`, `90f`, `-15f`와 같이 **각도로 이미지 회전**이 가능합니다. 양수 값은 시계 방향, 음수 값은 반시계 방향으로 회전합니다.

#### Aspose.PSD를 사용한 특정 각도 이미지 회전

메서드가 `float`를 사용하므로 그래픽 디자인 워크플로우에서 정밀 제어를 위해 `22.5f`와 같은 **특정 각도 이미지 회전**을 지정할 수 있습니다.

#### Java 이미지 회전 예제 요약

위 단계들은 파일 로드부터 회전된 출력 저장까지 전체 **rotate image java** 워크플로우를 보여줍니다.

### 단계 6: 결과 저장

```java
image.save(destName, new JpegOptions());
```

`JpegOptions`를 사용하면 품질, 압축 및 기타 JPEG 전용 설정을 제어할 수 있습니다. 무손실 출력을 원한다면 `PngOptions`로 교체하세요.

## 일반적인 문제 및 해결책

| Issue | Cause | Fix |
|-------|-------|-----|
| **회전 후 빈 코너** | 배경 색상이 제공되지 않음 | `rotate`에 `Color`(예: `Color.getWhite()`)를 전달합니다. |
| **대용량 PSD에서 메모리 부족 오류** | 이미지가 캐시되지 않음 | 처리 전에 `image.cacheData()`를 호출합니다. |
| **잘못된 각도 방향** | 음수와 양수 각도 혼동 | 시계 방향 회전을 위해 음수 값을 사용합니다(좌표계에 따라 반대일 수도 있음). |
| **저장되지 않은 변경 사항** | `save` 호출을 잊음 | 회전 후 `image.save(...)`가 실행되는지 확인합니다. |

## 자주 묻는 질문

**Q: Aspose.PSD for Java를 사용해 투명도를 유지한 채로 이미지를 회전할 수 있나요?**  
A: 예. 라이브러리는 알파 채널을 보존합니다; 투명한 코너를 원한다면 불투명 배경 색상을 지정하지 않으면 됩니다.

**Q: 회전에 지원되는 이미지 파일 형식에 제한이 있나요?**  
A: 없습니다. Aspose.PSD는 PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF 등 다수를 지원합니다.

**Q: 음수 각도로 이미지를 회전할 수 있나요?**  
A: 물론입니다. `rotate`에 음수 `float`(예: `-30f`)를 전달하면 시계 방향으로 회전합니다.

**Q: 회전 중 실시간 이미지 미리보기를 제공하나요?**  
A: API는 서버 측 전용입니다. 실시간 미리보기가 필요하면 회전된 비트맵을 UI 프레임워크(Swing, JavaFX)와 통합하고 뷰를 새로 고칩니다.

**Q: 도움을 받을 수 있는 Aspose.PSD 커뮤니티 포럼이 있나요?**  
A: 예, 질문을 올리고 경험을 공유하려면 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)을 방문하세요.

## 결론

이제 Aspose.PSD for Java를 사용해 특정 각도로 **이미지를 회전하는 방법**을 알게 되었습니다. 캐싱, 배경 색상 제어 및 유연한 출력 옵션을 활용하면 Java 기반 이미지 워크플로우에 정밀 회전 기능을 손쉽게 통합할 수 있습니다.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
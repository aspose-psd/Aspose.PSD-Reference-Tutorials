---
date: 2026-01-07
description: Aspose.PSD for Java를 사용하여 Java에서 이미지를 자르는 방법을 배워보세요. 이미지 자르기, 크기 조정 및
  PSD를 JPEG로 변환하는 단계별 가이드.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: '이미지 자르기 Java: Aspose.PSD for Java를 사용한 이미지 확대 및 자르기'
url: /ko/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 이미지 자르기 Java: Aspose.PSD for Java로 이미지 확장 및 자르기

## 소개

이 튜토리얼에서는 Aspose.PSD 라이브러리를 사용하여 **crop image java** 를 수행하는 방법을 알아봅니다. 캔버스를 확장하거나 원하지 않는 가장자리를 잘라내거나 PSD 파일을 JPEG 로 변환해야 할 때, 아래 단계가 깔끔하고 반복 가능한 프로세스를 안내합니다. 전제 조건, import 문, 각 코딩 단계와 명확한 설명을 다루어 실제 프로젝트에 적용할 수 있도록 합니다.

## 빠른 답변
- **crop image java 를 처리하는 라이브러리는?** Aspose.PSD for Java.  
- **개발에 라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있으며, 운영 환경에서는 상용 라이선스가 필요합니다.  
- **PSD 를 JPEG 로 변환하면서 자를 수 있나요?** 예, `JpegOptions` 와 자르기 사각형을 함께 사용하면 가능합니다.  
- **Java 8 을 지원하나요?** Aspose.PSD 는 Java 8 및 이후 버전을 지원합니다.  
- **구현에 얼마나 걸리나요?** 기본적인 자르기 작업은 보통 10분 이내에 완료됩니다.

## “crop image java” 란?

Java 에서 이미지를 자른다는 것은 원본 사진의 사각형 영역을 선택하고 나머지를 버리는 것을 의미합니다. Aspose.PSD 를 사용하면 `Rectangle` 객체로 이 영역을 정의한 뒤 JPEG 와 같은 다른 형식으로 저장할 수 있습니다.

## Aspose.PSD for Java 로 이미지 자르기를 사용하는 이유

- **전체 PSD 지원** – 레이어가 포함된 PSD 파일을 변환 없이 직접 작업합니다.  
- **고성능 래스터 처리** – 대용량 이미지에 대한 메모리 사용 효율이 뛰어납니다.  
- **내장 변환** – 자르기 또는 캔버스 확장을 적용하면서 JPEG, PNG, BMP 등으로 손쉽게 내보낼 수 있습니다.  
- **크로스 플랫폼** – Java 가 실행되는 모든 시스템에서 동작합니다.

## 전제 조건

시작하기 전에 다음을 준비하십시오:

1. **Java Development Kit (JDK)** – Java 8 이상이 설치되어 있어야 합니다.  
2. **Aspose.PSD for Java** – 공식 사이트 **[여기](https://releases.aspose.com/psd/java/)** 에서 라이브러리를 다운로드하십시오.  

> **팁:** Aspose.PSD JAR 를 프로젝트의 classpath 혹은 Maven/Gradle 의존성에 추가하면 `ClassNotFoundException` 을 방지할 수 있습니다.

## 패키지 Import

Java 소스 파일에 필요한 import 문을 추가합니다. 이 클래스들은 이미지 로드, 래스터 조작, 사각형 정의 및 JPEG 내보내기 옵션에 접근할 수 있게 해줍니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 단계 1: 문서 디렉터리 설정

소스 PSD 파일이 들어 있는 폴더를 지정합니다. 자리표시자를 실제 경로로 교체하십시오.

```java
String dataDir = "Your Document Directory";
```

## 단계 2: 소스 및 대상 경로 지정

PSD 를 읽어올 위치와 자른 JPEG 를 저장할 위치를 정의합니다.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## 단계 3: 이미지 로드 및 캐시

PSD 를 `RasterImage` 객체에 로드합니다. 캐시를 사용하면 자르기와 같은 후속 작업의 성능이 향상됩니다.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## 단계 4: 자르기용 Rectangle 생성

보존하고 싶은 영역을 설명하는 `Rectangle` 을 생성합니다. 좌표를 음수로 지정하면 **캔버스를 확장**하면서 자를 수 있어 원본 이미지 주변에 테두리를 추가할 때 유용합니다.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **음수 좌표를 사용하는 이유?**  
> 음수 X/Y 값은 자르기 영역을 왼쪽/위쪽으로 이동시켜, 최종 자르기 전에 원본 콘텐츠 주변에 빈 공간(확장)을 추가합니다.

## 단계 5: 자른 이미지 저장

마지막으로 `JjpegOptions` 를 사용해 결과 이미지를 저장합니다. 이 단계는 자르기 사각형을 적용하면서 **convert psd jpeg** 를 수행하는 예시이기도 합니다.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **결과:** `jpeg_out.jpg` 는 각 면이 200 px씩 확장된 뒤 정의된 사각형으로 잘라진 300 × 300 픽셀 이미지가 됩니다.

축하합니다! 몇 줄의 코드만으로 **java image cropping** 을 성공적으로 수행하고, 캔버스를 확장했으며, PSD 파일을 JPEG 로 변환했습니다.

## 일반적인 사용 사례

- **웹용 에셋 준비** – 스크린샷이나 디자인을 업로드하기 전에 자르고 크기 조정합니다.  
- **썸네일 생성** – 대형 PSD 에서 특정 영역을 추출해 미리보기용으로 사용합니다.  
- **자동 배치 처리** – 폴더에 있는 PSD 파일들을 순회하면서 동일한 자르기 사각형을 적용합니다.

## 문제 해결 및 팁

| 문제 | 권장 해결책 |
|------|-------------|
| 큰 PSD 로드 시 `OutOfMemoryError` 발생 | `rasterImage.cacheData()` 를 초기에 호출하고 JVM 힙 크기(`-Xmx`) 를 늘리는 것을 고려하십시오. |
| 자른 영역이 중앙에서 벗어남 | 사각형의 X/Y 오프셋을 확인하십시오; 음수 값은 캔버스를 확장한다는 점을 기억하세요. |
| 출력 JPEG 가 흐릿함 | `JpegOptions` 의 품질 설정을 조정하십시오(예: `new JpegOptions { Quality = 90 }`). |

## 자주 묻는 질문

### Q1: Aspose.PSD 가 다양한 Java 버전과 호환되나요?

A1: 예, Aspose.PSD 는 여러 Java 버전을 지원하므로 다양한 개발 환경에서 호환됩니다.

### Q2: Aspose.PSD 를 상업 프로젝트에 사용할 수 있나요?

A2: 물론입니다. Aspose.PSD 는 개인 및 상업 프로젝트 모두에 사용할 수 있는 상용 라이선스를 제공합니다.

### Q3: 지원되는 이미지 파일 형식에 제한이 있나요?

A3: Aspose.PSD 는 PSD, JPEG, PNG 등을 포함한 다양한 이미지 형식을 지원합니다. 전체 목록은 [문서](https://reference.aspose.com/psd/java/) 를 참고하십시오.

### Q4: Aspose.PSD 관련 문의에 대한 지원은 어떻게 받나요?

A4: [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 에 방문하여 커뮤니티 또는 Aspose 지원 팀에 도움을 요청하십시오.

### Q5: 무료 체험판을 이용할 수 있나요?

A5: 예, 무료 체험판을 이용할 수 있습니다. [여기](https://releases.aspose.com/) 에서 다운로드하십시오.

---

**마지막 업데이트:** 2026-01-07  
**테스트 환경:** Aspose.PSD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
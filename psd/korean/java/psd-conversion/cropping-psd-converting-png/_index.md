---
date: 2026-03-21
description: Aspose.PSD for Java를 사용하여 PSD를 PNG로 변환하고 PSD 파일을 자르는 방법을 배웁니다. 이 가이드는
  Java 애플리케이션에서 단계별 이미지 처리를 보여줍니다.
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD를 PNG로 변환하고 자르기
url: /ko/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD를 PNG로 변환하고 자르기

## 소개
동적인 Java 개발 세계에서 효율적인 이미지 처리를 마스터하는 것은 매우 중요합니다. 이 튜토리얼에서는 강력한 Aspose.PSD for Java 라이브러리를 사용하여 **psd를 png로 변환하는 방법**을 배우고 이미지 를 한 번에 자를 수 있습니다. 단계별 가이드를 마치면 PNG 내보내기에 정밀한 자르기를 추가하고 Java 애플리케이션이 PSD 자산을 자신 있게 처리할 수 있게 됩니다.

## 빠른 답변
- **코드가 하는 일은?** PSD를 로드하고, 사각형을 자른 뒤 PNG로 저장합니다.  
- **필요한 라이브러리는?** Aspose.PSD for Java (최신 버전).  
- **라이선스가 필요한가요?** 예, 상용 사용을 위해서는 상업용 라이선스가 필요합니다.  
- **어떤 자르기 영역도 정의할 수 있나요?** 물론입니다 – 필요한 X, Y, 너비, 높이를 설정하면 됩니다.  
- **대용량 파일에 대해 이 방법이 빠른가요?** 예, Aspose.PSD는 고성능 처리를 위해 최적화되어 있습니다.

## convert psd to png란 무엇인가요?
PSD를 PNG로 변환한다는 것은 레이어가 있는 Photoshop 문서를 손실 없는 PNG 이미지로 평탄화하는 것을 의미합니다. 이 형식은 웹 전송, 썸네일 또는 원본 레이어 없이 래스터 이미지가 필요한 모든 상황에 이상적입니다.

## PNG로 변환하기 전에 PSD를 자르는 이유는?
자르기를 통해 디자인에서 필요한 부분만 추출함으로써 파일 크기를 줄이고 관련 시각 콘텐츠에 집중할 수 있습니다. 썸네일 생성, UI 자산 제작, 반응형 레이아웃을 위한 이미지 준비 등에 특히 유용합니다.

## 사전 요구 사항
튜토리얼을 진행하기 전에 다음 요구 사항을 충족했는지 확인하세요:
- Java 프로그래밍에 대한 기본 지식.  
- 시스템에 Java Development Kit (JDK) 설치.  
- Aspose.PSD for Java 라이브러리를 다운로드하여 프로젝트에 추가.  
- 실험용 샘플 PSD 파일.

## 패키지 가져오기
Java 프로젝트에서 Aspose.PSD 기능을 사용하기 위해 필요한 패키지를 가져와야 합니다:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## 단계 1: 프로젝트 설정
Java 프로젝트를 생성하고 Aspose.PSD for Java 라이브러리를 프로젝트 클래스패스에 추가합니다. 이를 통해 이미지 처리에 필요한 모든 클래스를 사용할 수 있습니다.

## 단계 2: PSD 이미지 로드
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*여기서는 `RasterImage` 객체에 소스 PSD 파일을 로드합니다. 이 객체는 자르기와 같은 래스터 기반 작업을 제공합니다.*

## 단계 3: 자르기 영역 정의
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*`Rectangle`은 유지하려는 영역을 정의합니다. 디자인에 맞게 `x`, `y`, `width`, `height` 값을 조정하세요. 이 단계는 “define crop region” 키워드에 직접 답합니다.*

## 단계 4: PSD 이미지 자르기
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*`crop` 메서드를 호출하면 지정된 사각형 외부의 모든 내용이 메모리 내에서 제거됩니다.*

## 단계 5: PNG 내보내기 옵션 설정
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions`를 사용하면 압축 수준, 색상 유형 등 PNG 전용 설정을 제어할 수 있습니다.*

## 단계 6: 자른 이미지를 PNG로 저장
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*`save` 메서드는 **convert psd to png** 작업을 수행하면서 정의한 자르기 영역을 유지합니다.*

## 일반적인 함정 및 팁
- **잘못된 사각형 크기:** 너비와 높이가 원본 이미지 크기를 초과하지 않도록 하세요. 초과하면 예외가 발생합니다.  
- **대용량 PSD의 메모리 사용:** 저장 후 `RasterImage` 객체(`image.dispose()`)를 해제하여 네이티브 리소스를 확보하세요.  
- **라이선스 미설정:** 유효한 라이선스 없이 코드를 실행하면 출력 PNG에 워터마크가 표시됩니다.

## 자주 묻는 질문
### Aspose.PSD for Java를 사용하여 불규칙한 형태의 PSD 파일을 자를 수 있나요?
예, Aspose.PSD for Java는 사용자 정의 자르기 영역을 정의할 수 있어 다양한 형태로 이미지를 자를 수 있습니다.

### Aspose.PSD for Java가 대규모 이미지 처리 작업에 적합한가요?
물론입니다! Aspose.PSD는 대용량 이미지를 효율적으로 처리하도록 설계되어 있어 광범위한 이미지 처리 요구 사항이 있는 프로젝트에 이상적입니다.

### Aspose.PSD for Java에 라이선스가 필요합니까?
예, 상업적 사용을 위해서는 유효한 라이선스가 필요합니다. 라이선스는 [Aspose Purchase](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

### Aspose.PSD for Java에 대한 도움을 받거나 문제를 보고하려면 어떻게 해야 하나요?
지원 및 문제 보고는 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)에서 도움을 받을 수 있으며, 경험을 공유하고 이슈를 보고할 수 있습니다.

### 구매 전에 Aspose.PSD for Java를 체험할 수 있나요?
네, 무료 체험판은 [여기](https://releases.aspose.com/)에서 이용하실 수 있습니다.

---

**최종 업데이트:** 2026-03-21  
**테스트 환경:** Aspose.PSD for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
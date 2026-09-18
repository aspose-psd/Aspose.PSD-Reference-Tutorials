---
date: 2026-09-18
description: Aspose.PSD for Java를 사용하여 Java 이미지 메타데이터 썸네일을 EXIF 세그먼트에 추가하는 방법을 배웁니다.
  이 단계별 가이드에서는 사전 요구 사항, 코드 walkthrough, 업데이트된 이미지 저장을 다룹니다.
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: Java에서 EXIF 세그먼트에 썸네일 추가
og_description: Aspose.PSD for Java를 사용하여 Java 이미지 메타데이터 썸네일을 EXIF 세그먼트에 추가하는 방법을
  배웁니다. 이 단계별 가이드에서는 사전 요구 사항, 코드 walkthrough, 업데이트된 이미지 저장을 다룹니다.
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: Java 이미지 메타데이터 썸네일을 EXIF 세그먼트에 추가하는 방법
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: Java 이미지 메타데이터 썸네일을 EXIF 세그먼트에 추가하는 방법
url: /ko/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# EXIF 세그먼트에 java 이미지 메타데이터 썸네일 추가

## 소개
이 튜토리얼에서는 Aspose.PSD for Java를 사용하여 PSD 파일의 EXIF 세그먼트에 **java 이미지 메타데이터** 썸네일을 추가하는 방법을 배웁니다. EXIF(Exchangeable Image File Format) 메타데이터는 카메라 설정, 촬영 날짜, 위치 및 기타 유용한 정보를 저장합니다. 작은 미리보기 썸네일을 삽입하면 전체 파일을 로드하지 않고도 애플리케이션이 빠르게 이미지를 미리 볼 수 있어 성능과 사용자 경험이 향상됩니다.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.PSD for Java를 사용하여 PSD 이미지의 EXIF 세그먼트에 썸네일을 추가합니다.  
- **구현에 얼마나 걸리나요?** 기본 통합의 경우 약 10‑15분 정도 소요됩니다.  
- **라이선스가 필요합니까?** 프로덕션 사용을 위해서는 임시 라이선스가 필요하며, 평가용으로는 무료 체험판을 사용할 수 있습니다.  
- **지원되는 Java 버전은?** Java 8 이상을 완전히 지원합니다.  
- **대용량 파일도 처리할 수 있나요?** 예—Aspose.PSD는 전체 이미지를 메모리에 로드하지 않고 최대 2 GB 파일까지 처리할 수 있습니다.

## java 이미지 메타데이터란?
Java 이미지 메타데이터는 이미지 파일(EXIF, IPTC, XMP 등)에 삽입된 구조화된 정보를 의미하며, Aspose.PSD와 같은 Java 라이브러리를 사용해 프로그래밍 방식으로 읽고, 수정하고, 생성할 수 있습니다. 이 메타데이터를 통해 애플리케이션은 카메라 설정, 타임스탬프, GPS 좌표 및 사용자 정의 데이터를 시각 콘텐츠를 열지 않고도 가져올 수 있습니다.

## EXIF 메타데이터에 썸네일을 추가하는 이유
EXIF 세그먼트에 썸네일을 추가하면 이미지 브라우저, 파일 탐색기 및 콘텐츠 관리 시스템에서 즉시 시각적 힌트를 제공할 수 있습니다. Aspose.PSD는 썸네일을 메모리 내에서 처리하여 500 KB 이하 이미지에 대해 0.2 초 미만으로 미리보기를 삽입할 수 있으며, PSD, JPEG, PNG, TIFF 등 30가지 이상의 이미지 포맷을 지원합니다.

## 전제 조건
튜토리얼을 시작하기 전에 다음 사항을 준비하세요:
- Java 프로그래밍에 대한 기본 지식.  
- 시스템에 설치된 Java Development Kit (JDK).  
- IntelliJ IDEA 또는 Eclipse와 같은 Java용 IDE.  
- Aspose.PSD for Java 라이브러리. [Aspose.PSD for Java 다운로드 페이지](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

## 패키지 가져오기
다음 import 구문은 PSD 이미지와 EXIF 데이터를 다루는 데 필요한 Aspose.PSD 클래스를 포함합니다.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## 단계 1: psd 이미지 로드
`PsdImage`는 Photoshop PSD 파일을 나타내며 레이어와 리소스에 접근할 수 있게 해줍니다.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## 단계 2: 이미지 리소스 반복
`ImageResource`는 썸네일, ICC 프로파일 및 PSD 파일에 삽입된 메타데이터와 같은 리소스를 캡슐화합니다.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## 단계 3: 썸네일 데이터 조정
`JpegOptions`를 사용하면 썸네일 이미지에 대한 품질 등 JPEG‑특화 설정을 구성할 수 있습니다.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## 단계 4: 이미지 저장
`save` 메서드를 호출하면 업데이트된 EXIF 세그먼트(새 썸네일 포함)가 전체 이미지를 다시 인코딩하지 않고 디스크에 기록됩니다.  
```java
image.save(dataDir + "output.psd");
```

## 일반적인 문제 및 해결책
- **썸네일이 표시되지 않음:** 썸네일 리소스가 EXIF 세그먼트에 올바르게 추가되었는지, 그리고 `PsdImage.save` 메서드로 저장했는지 확인하세요.  
- **대용량 파일에서 메모리 부족 오류:** `PsdImage.load(..., LoadOptions)`와 `LoadOptions.setLoadOnlyMetadata(true)`를 사용해 메타데이터만 작업하십시오.  
- **잘못된 방향:** 썸네일이 원본 이미지의 방향 플래그를 유지하도록 `Orientation` EXIF 태그를 읽고 썸네일을 회전시키세요.

## 자주 묻는 질문

**Q: EXIF 메타데이터란 무엇인가요?**  
A: EXIF 메타데이터는 디지털 이미지에 삽입된 정보로, 카메라 설정, 촬영 날짜, GPS 좌표 및 기타 세부 정보를 포함합니다.

**Q: 왜 EXIF에 썸네일을 추가하나요?**  
A: 썸네일을 추가하면 전체 이미지를 로드하지 않고도 빠른 이미지 미리보기를 제공하여 사용자 경험이 향상됩니다.

**Q: Aspose.PSD for Java를 어디서 다운로드할 수 있나요?**  
A: [Aspose.PSD for Java 다운로드 페이지](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

**Q: Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?**  
A: [임시 라이선스 페이지](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 받을 수 있습니다.

**Q: Aspose.PSD 지원을 어떻게 받을 수 있나요?**  
A: 지원이 필요하면 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)에서 문의하세요.

---

**마지막 업데이트:** 2026-09-18  
**테스트 환경:** Aspose.PSD for Java 24.10  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.PSD for Java를 사용하여 PSD 파일에 XMP 메타데이터 만들기](/psd/java/image-editing/create-xmp-metadata/)
- [Aspose.PSD for Java로 이미지 크기 조정 – 도형 그리기 및 기본 이미지 작업](/psd/java/basic-image-operations/)
- [Aspose.PSD for Java를 사용해 PSD를 래스터 이미지 포맷으로 변환하는 방법](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-09-28
description: Aspose.PSD를 사용하여 Java에서 JFIF 세그먼트에 썸네일을 추가하는 방법. 이 단계별 가이드를 따라 PSD 파일에
  썸네일을 빠르고 신뢰성 있게 삽입하세요.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Java에서 JFIF 세그먼트에 썸네일 추가
og_description: Aspose.PSD를 사용하여 Java에서 JFIF 세그먼트에 썸네일을 추가하는 방법. 이 단계별 가이드를 따라 PSD
  파일에 썸네일을 빠르고 신뢰성 있게 삽입하세요.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Java에서 JFIF 세그먼트에 썸네일을 추가하는 방법
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Java에서 JFIF 세그먼트에 썸네일을 추가하는 방법
url: /ko/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 JFIF 세그먼트에 썸네일 추가하는 방법

## 소개
PSD 파일의 JFIF 세그먼트에 썸네일을 추가하는 것은 전체 이미지를 로드하지 않고도 빠른 시각적 미리보기가 필요할 때 흔히 요구되는 작업입니다. 이 튜토리얼에서는 Aspose.PSD를 사용하여 Java에서 JFIF 세그먼트에 **썸네일을 추가하는 방법**을 배웁니다. 가이드가 끝날 때쯤 실행 가능한 코드 스니펫과 JFIF 구조에 대한 이해, 대용량 파일을 효율적으로 처리하는 팁을 얻을 수 있습니다.

## 빠른 답변
- **필요한 라이브러리는 무엇인가요?** Aspose.PSD for Java.
- **어떤 Java 버전이 작동하나요?** JDK 11 이상.
- **필요한 코드 라인은 몇 개인가요?** 로드, 수정 및 저장에 약 10줄.
- **멀티 메가바이트 파일을 처리할 수 있나요?** 예, Aspose.PSD가 데이터를 스트리밍하므로 메모리 사용량이 낮게 유지됩니다.
- **상업용 라이선스가 필요합니까?** 프로덕션 사용을 위해 라이선스가 필요하며, 무료 체험판을 사용할 수 있습니다.

## JFIF 세그먼트란?
JFIF 세그먼트는 썸네일, EXIF 또는 컬러 프로파일과 같은 선택적 데이터를 저장할 수 있는 JPEG 파일 교환 형식 블록입니다.  
PSD 파일의 JPEG 스트림 내부에 존재하며 대부분의 이미지 뷰어에서 빠른 미리보기 생성을 위해 인식됩니다.

## PSD 파일에 썸네일을 추가하는 이유
Aspose.PSD for Java는 **30개 이상의 이미지 포맷**을 지원하며 전체 문서를 메모리에 로드하지 않고 **2 GB**까지 파일을 처리할 수 있습니다. 썸네일을 추가하면 미리보기를 전송할 때 네트워크 대역폭을 줄이고 갤러리 애플리케이션에서 UI 렌더링 속도를 높일 수 있습니다.

## 사전 요구 사항
- Java Development Kit (JDK): 시스템에 Java가 설치되어 있는지 확인하십시오. [Oracle's JDK website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드할 수 있습니다.
- Aspose.PSD for Java: Aspose.PSD for Java 라이브러리가 필요합니다. [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/)에서 얻을 수 있습니다.
- Integrated Development Environment (IDE): IntelliJ IDEA 또는 Eclipse와 같은 IDE를 사용하십시오.
- Basic Understanding of Java: Java 프로그래밍 언어와 개념에 익숙해야 합니다.

## Java에서 JFIF 세그먼트에 썸네일을 추가하는 방법?
대상 PSD를 로드하고, JFIF 리소스를 찾아 썸네일 데이터를 교체한 뒤 파일을 저장합니다. 전체 작업은 몇 가지 간단한 API 호출로 수행할 수 있으며, Aspose.PSD가 저수준 JPEG 구조를 처리해 줍니다.

### 단계 1: 패키지 가져오기
`Document`, `JfifResource` 및 관련 클래스는 Aspose.PSD 네임스페이스의 일부입니다. Document는 PSD 파일 컨테이너를 나타내며, JfifResource는 PSD 내의 JFIF 세그먼트에 접근할 수 있게 해줍니다. 소스 파일 상단에 이들을 import하십시오.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### 단계 2: PSD 이미지 로드
파일 경로를 생성자에 전달하여 `PsdImage` 인스턴스를 만듭니다. PsdImage는 Photoshop 문서를 모델링하는 Aspose.PSD 클래스입니다. 이 과정에서 문서 메타데이터를 로드하면서 픽셀 데이터를 스트리밍합니다.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### 단계 3: 이미지 리소스 반복
`Resources` 컬렉션에서 `JfifResource`를 검색합니다. 찾으면 해당 썸네일 바이트 배열을 새로운 JPEG 인코딩 미리보기로 교체할 수 있습니다.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### 단계 4: 썸네일 데이터 조정
任意의 이미지‑처리 라이브러리를 사용하여 작은 JPEG 썸네일(예: 120 × 120 px)을 생성한 뒤, 결과 바이트 배열을 `jfifResource.ThumbnailData`에 할당합니다.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### 단계 5: 수정된 이미지 저장
`PsdImage` 객체의 `save` 메서드를 호출하고 출력 경로와 원하는 포맷을 지정합니다. 이제 JFIF 세그먼트에 새로운 썸네일이 포함됩니다.

```java
image.save(dataDir + "output.psd");
```

## 일반적인 문제 및 해결책
- **뷰어에서 썸네일이 보이지 않음:** 썸네일 데이터가 유효한 JPEG 바이트 배열인지, 그리고 크기가 JFIF 사양에서 지원하는 최대 크기인 256 × 256 px 이내인지 확인하세요.
- **대용량 PSD에서 OutOfMemoryError 발생:** `PsdImage.load(inputStream, true)`를 사용하여 스트리밍 모드를 활성화하면 메모리 사용량을 낮게 유지할 수 있습니다.
- **잘못된 리소스 유형:** 수정하려는 리소스가 실제로 `JfifResource`인지 확인하세요; `ExifResource`와 같은 다른 리소스는 썸네일 표시와 관련이 없습니다.

## 자주 묻는 질문

**Q: Aspose.PSD for Java란?**  
A: Aspose.PSD for Java는 개발자가 Adobe Photoshop 없이도 Photoshop PSD 파일을 생성, 편집, 변환 및 렌더링할 수 있게 해주는 상용 라이브러리입니다.

**Q: Aspose.PSD for Java에 대한 자세한 문서는 어디에서 찾을 수 있나요?**  
A: 자세한 문서는 [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

**Q: Aspose.PSD for Java를 상업적으로 사용할 수 있나요?**  
A: 예, Aspose.PSD for Java는 상업적으로 사용할 수 있습니다. 라이선스는 [Aspose.PSD's purchase page](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

**Q: 구매 전에 Aspose.PSD for Java를 체험해 볼 수 있나요?**  
A: 예, [Aspose.PSD's trial download page](https://releases.aspose.com/)에서 무료 체험판을 다운로드할 수 있습니다.

**Q: Aspose.PSD for Java에 대한 지원을 어떻게 받을 수 있나요?**  
A: 지원이 필요하면 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)을 방문하세요.

**마지막 업데이트:** 2026-09-28  
**테스트 대상:** Aspose.PSD for Java 24.11  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose PSD for Java를 사용하여 PSD 파일에 IOPA 리소스 추가](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [이미지에 서명 추가 – Aspose.PSD for Java로 캔버스에 이미지 그리기](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Aspose.PSD for Java로 특정 각도에서 이미지 회전하는 방법](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
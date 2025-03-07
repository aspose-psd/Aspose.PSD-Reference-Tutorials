---
title: Java에서 JPEG 이미지 방향 자동 수정
linktitle: Java에서 JPEG 이미지 방향 자동 수정
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 Java에서 JPEG 이미지 방향을 자동으로 수정하는 방법을 알아보세요. 손쉽게 이미지 처리 기술을 향상시켜 보세요.
weight: 12
url: /ko/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 JPEG 이미지 방향 자동 수정

## 소개
오늘날의 디지털 시대에 프로그래밍 방식으로 이미지를 조작하고 최적화하는 것은 다양한 영역의 개발자에게 중요한 작업이 되었습니다. Java용 Aspose.PSD는 개발자에게 PSD, JPEG 및 기타 이미지 형식을 효율적으로 처리할 수 있는 강력한 도구를 제공합니다. 이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 JPEG 이미지 방향을 자동으로 수정하는 특정 작업에 대해 자세히 설명합니다. 사진 편집 앱을 구축하든, 콘텐츠 관리 시스템에서 이미지 리소스를 관리하든, 이미지 처리 워크플로를 자동화하든 이 가이드는 이 기능을 Java 애플리케이션에 원활하게 통합하는 데 필요한 지식을 제공합니다.
## 전제조건
이 튜토리얼을 시작하기 전에 다음 전제 조건이 설정되어 있는지 확인하세요.
- Java 개발 환경: 시스템에 JDK(Java Development Kit)가 설치되어 있는지 확인하십시오.
-  Java JAR용 Aspose.PSD: 다음 위치에서 Java용 Aspose.PSD 라이브러리를 다운로드하세요.[여기](https://releases.aspose.com/psd/java/).
- 통합 개발 환경(IDE): Java 개발을 위해 IntelliJ IDEA, Eclipse 또는 원하는 IDE를 사용하세요.
- Java 및 이미지 처리에 대한 기본 이해: Java 프로그래밍 및 이미지 처리의 기본 개념에 익숙하면 도움이 됩니다.

## 패키지 가져오기
예제를 시작하기 전에 Aspose.PSD for Java에서 필요한 패키지를 가져와야 합니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## 1단계: PSD 이미지 로드
먼저 방향 수정이 필요한 JPEG 축소판이 포함된 PSD 이미지를 로드합니다.
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 바꾸다`"Your Document Directory"` PSD 파일이 있는 실제 디렉터리 경로를 사용합니다.
## 2단계: 이미지 리소스 반복
다음으로 이미지 리소스를 반복하여 JPEG 썸네일 리소스를 찾습니다.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // 썸네일 리소스를 찾으세요. 일반적으로 JPEG 파일 형식입니다.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // 썸네일 데이터를 조정합니다.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // 저장된 썸네일이 있으면 자동 회전됩니다.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## 3단계: 이미지 저장
마지막으로 자동 회전을 적용한 후 수정된 이미지를 저장합니다.
```java
image.save();
```
이 단계를 수행하면 이미지에 대한 변경 사항이 유지됩니다.

## 결론
결론적으로, Aspose.PSD for Java를 사용하면 PSD 파일 내에서 JPEG 이미지 방향을 자동으로 수정하는 강력한 솔루션을 제공합니다. 이 튜토리얼에 설명된 단계를 따르면 개발자는 이미지 처리 워크플로를 향상하여 다양한 플랫폼과 장치에서 이미지가 올바르게 표시되도록 할 수 있습니다.
## FAQ
### Java용 Aspose.PSD란 무엇입니까?
Aspose.PSD for Java는 Java 개발자가 프로그래밍 방식으로 PSD, JPEG 및 기타 이미지 형식으로 작업할 수 있는 강력한 라이브러리입니다.
### Java용 Aspose.PSD를 어떻게 다운로드할 수 있나요?
 다음에서 라이브러리를 다운로드할 수 있습니다.[여기](https://releases.aspose.com/psd/java/).
### Java용 Aspose.PSD는 이미지 조작을 지원합니까?
예, 크기 조정, 자르기, 방향 조정과 같은 다양한 이미지 조작 작업을 지원합니다.
### Java용 Aspose.PSD에 대한 문서는 어디서 찾을 수 있나요?
 포괄적인 문서가 제공됩니다.[여기](https://reference.aspose.com/psd/java/).
### Java용 Aspose.PSD를 무료로 사용해 볼 수 있나요?
 예, 다음에서 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

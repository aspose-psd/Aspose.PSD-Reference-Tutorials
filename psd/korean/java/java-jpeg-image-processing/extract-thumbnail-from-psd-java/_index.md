---
title: Java의 PSD에서 썸네일 추출
linktitle: Java의 PSD에서 썸네일 추출
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일에서 썸네일을 추출하는 방법을 알아보세요. 이 단계별 가이드에서는 설정부터 추출된 이미지 저장까지 모든 것을 다룹니다.
type: docs
weight: 15
url: /ko/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## 소개
이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 PSD 파일에서 썸네일을 추출하는 방법을 살펴보겠습니다. 축소판은 빠른 미리 보기 또는 PSD 문서에 포함된 이미지의 작은 버전을 만드는 데 유용할 수 있습니다. Aspose.PSD를 사용하여 이를 달성하는 데 필요한 단계를 살펴보겠습니다.
## 전제조건
시작하기 전에 다음이 설정되어 있는지 확인하세요.
- 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
-  Java 라이브러리용 Aspose.PSD. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/psd/java/).
- Java 프로그래밍에 대한 기본 지식.
## 패키지 가져오기
시작하려면 Java 클래스에 필요한 Aspose.PSD 패키지를 포함하세요.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## 1단계: PSD 파일 로드
먼저 추출하려는 썸네일이 포함된 PSD 파일을 로드합니다.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 바꾸다`"Your_Document_Directory/"` PSD 파일이 있는 디렉터리 경로와`"your_file.psd"` PSD 파일 이름으로.
## 2단계: 이미지 리소스 반복
이미지 리소스를 반복하여 썸네일 리소스를 찾습니다.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // 썸네일 데이터 추출
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // 추출된 썸네일 데이터로 새 이미지를 생성합니다.
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // 추출된 썸네일을 별도의 JPEG 파일로 저장
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // 성공 메시지 출력
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // 썸네일을 찾아 처리하면 루프를 종료합니다.
    }
}
```
## 3단계: 추출된 썸네일 저장
추출된 썸네일을 별도의 이미지 파일(이 경우 JPEG 파일)로 저장합니다.
## 4단계: 다양한 썸네일 유형 처리
 PSD 파일에 다음과 같은 여러 유형의 축소판이 포함될 수 있는 경우`Thumbnail4Resource`, 이러한 경우를 유사하게 처리하도록 논리를 확장할 수 있습니다.

## 결론
이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 PSD 파일에서 썸네일을 추출하는 방법을 살펴보았습니다. 위에 설명된 단계를 따르면 PSD 문서에 포함된 축소판을 효율적으로 검색하고 저장할 수 있습니다.

## FAQ
### Aspose.PSD란 무엇인가요?
Aspose.PSD는 개발자가 프로그래밍 방식으로 PSD 및 기타 이미지 파일 형식으로 작업할 수 있도록 하는 Java 라이브러리입니다.
### Java용 Aspose.PSD에 대한 추가 문서는 어디서 찾을 수 있나요?
 당신은[선적 서류 비치](https://reference.aspose.com/psd/java/) 자세한 API 참조 및 예시를 확인하세요.
### 구매하기 전에 Aspose.PSD를 무료로 사용해 볼 수 있나요?
 예, 다음을 다운로드할 수 있습니다.[무료 평가판](https://releases.aspose.com/) 도서관의 능력을 평가합니다.
### Aspose.PSD에 대한 임시 라이선스를 어떻게 얻을 수 있나요?
 임시 라이센스는 다음에서 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD는 상업용으로 적합합니까?
예, Aspose.PSD는 라이선스 조건에 따라 개인 및 상업용 프로젝트 모두에 사용할 수 있습니다.
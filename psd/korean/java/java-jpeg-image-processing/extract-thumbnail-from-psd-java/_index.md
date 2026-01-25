---
date: 2026-01-25
description: Aspose.PSD for Java를 사용하여 PSD 파일에서 썸네일을 추출하는 방법을 배워보세요. 로드, 추출 및 썸네일을
  빠르게 저장하는 단계별 가이드를 따라가세요.
linktitle: Extract Thumbnail from PSD in Java
second_title: Aspose.PSD Java API
title: Java에서 PSD 썸네일 추출
url: /ko/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 PSD 썸네일 추출하기

## 소개
이 튜토리얼에서는 Aspose.PSD for Java 라이브러리를 사용하여 **PSD에서 썸네일을 추출하는 방법**을 배웁니다. 썸네일은 PSD 문서에 삽입된 작은 미리보기 이미지이며, 이를 추출하면 빠른 미리보기를 생성하거나 이미지 갤러리를 만들거나 원본 아트워크의 작은 표현만 필요할 때 저장 용량을 줄일 수 있습니다. 프로젝트 설정부터 추출된 썸네일을 표준 이미지 파일로 저장하는 과정까지 모두 안내합니다.

## 빠른 답변
- **이 튜토리얼에서 다루는 내용은?** Aspose.PSD for Java를 사용하여 PSD 파일에서 썸네일 이미지를 추출하고 저장합니다.  
- **필요한 라이브러리는?** Aspose.PSD for Java (공식 Aspose 사이트에서험판을 사용할 수 있습니다.  
- **사용되는 출력 형식은?** 예제에서는 썸네일을 JPEG 읽는 것을 의미합니다. 이 미리보기는 전체 캔버스의 저해상도 버전으로, 파일 탐색기나 웹 갤러.

## 왜 Aspose.PSD로  
- **Automation:** 대규모 이미지 라이브러리를 배치 처리하기에 최적입니다.  
- **Cross‑platform:** Photoshop 없이도 Java를 지원하는 모든 OS에서 동작합니다.  
- **Format flexibility:** 썸네일을 JPEG, PNG 또는 Aspose.PSD가 지원하는 다른 형식으로 변환할 수 있습니다.

## 전제 조건
시작하기 전에 다음이 준비되어 있는 (JDK)가 설치되어 있어야 합니다.  
- Aspose.PSD for Java 라이브러리. [here](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.  
- Java 프로그래밍에 대한 기본 지식.

## 패키지 가져오기
시작하려면 Java 클래스에 필요한 Aspose.PSD 패키지를 포함합니다:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Aspose.PSD for Java를 사용하여 PSD에서 썸네일 추출하는 방법
아래는 단계별 가이드입니다. 각 단계마다 간단한 설명과 복사해서 사용할 정확한 코드가 제공됩니다.

### 1단계: PSD 파일 로드
먼저 추출하려는 썸네일이 포함된 PSD 파일을 로드합니다.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
`"Your_Document_Directory/"`를 PSD 파일이 위치한 디렉터리 경로로, `"your_file.psd"`를 PSD 파일 이름으로 교체하세요.

### 2단계: 이미지 리소스 반복
썸네일 리소스를 찾기 위해 이미지 리소스를 반복합니다.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```

###
이전 단계의 코드는 이미 동일한 디렉터리에식을 변경할 수 있습니다.

### 4단계: 다양한 썸네일 유형 처리
PSD 파일에 `Thumbnail4Resource`와 같이 여러 유형의 썸네일이 포함될 수 있는 경우, 루프 내부에 `instanceof Thumbnail4Resource` 검사를 추가하고 동일한 패턴으로 처리하면 됩니다.

## 일반적인 문제 및 해결책
- **No thumbnail found:** 모든 PSD 파일에 썸네일 리소스가 있는 것은 아닙니다. Photoshop에서 파일을 확인하세요(File → Export → Thumbnail) 프로그램matically PSD서한 API 레퍼런스와 예제는 [documentation](https://reference.aspose.com/psd/java/)을 참고하세요.

**Q: 구매 전에 Aspose.PSD를 무료로 체험할 수 있나요?**  
A: 네, [free trial](https://releases.aspose.com/)을 다운로드하여 라이브러리 기능을 평가할 수 있습니다.

**Q: Aspose.PSD의 임시 라이선스는 어떻게 얻나요?**  
A: 임시 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

**Q: Aspose.PSD를 상업적으로 사용할 수 있나요?**  
A: 네, Aspose.PSD는 개인 및 상업 프로젝트 모두에서 라이선스 조건에 따라 사용할 수 있습니다.

## 결론
이 튜토리얼에서는 Aspose.PSD for Java를 사용네 있어 빠른 미리보기와 간소화된 이미지 워크플로우를 구현할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2026-01-25  
**테스트 환경:** Aspose.PSD for Java (latest release)  
**작성자
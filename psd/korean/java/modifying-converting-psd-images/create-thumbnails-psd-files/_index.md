---
title: Java를 사용하여 PSD 파일에서 축소판 만들기
linktitle: Java를 사용하여 PSD 파일에서 축소판 만들기
second_title: Aspose.PSD 자바 API
description: Java 및 Aspose.PSD를 사용하여 PSD 파일에서 썸네일을 쉽게 만드는 방법을 알아보세요. 원활한 이미지 처리를 위한 단계별 가이드를 따르세요.
weight: 24
url: /ko/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 PSD 파일에서 축소판 만들기

## 소개
그래픽 디자인 세계에서는 PSD(Photoshop Document) 파일로 작업하는 것이 흔한 일입니다. 노련한 개발자, 그래픽 디자이너 또는 이미지 처리에 대해 자세히 알고 싶은 사람이라면 PSD 파일에서 썸네일을 만들면 시간을 절약하고 작업 흐름을 간소화할 수 있습니다. 이 튜토리얼은 Aspose.PSD for Java를 사용하는 전체 프로세스를 안내합니다. Aspose.PSD는 Photoshop 파일 관리를 위한 강력한 라이브러리일 뿐만 아니라 작업을 직관적이고 관리하기 쉽게 만듭니다. PSD 파일에서 썸네일을 효율적으로 만드는 방법을 배울 준비가 되셨습니까?
## 전제조건
썸네일 생성의 핵심을 살펴보기 전에 시작하는 데 필요한 사항을 알아보겠습니다.
### 자바 개발 환경
-  Java JDK: 컴퓨터에 JDK(Java Development Kit)가 설치되어 있는지 확인하십시오. 다운로드할 수 있습니다.[여기](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: IntelliJ IDEA, Eclipse 또는 NetBeans와 같은 통합 개발 환경(IDE)을 사용하면 코딩이 더 쉬워집니다.
### Aspose.PSD 라이브러리
- 프로젝트에 Aspose.PSD 라이브러리를 포함해야 합니다. 당신은 할 수 있습니다[여기서 최신 버전을 다운로드하세요](https://releases.aspose.com/psd/java/).
### 자바의 기본 지식
- Java 기본 사항에 익숙하면 예제 코드를 보다 효과적으로 탐색하는 데 도움이 됩니다. 클래스, 객체, 루프와 같은 개념이 자주 사용됩니다.
## 패키지 가져오기
Aspose.PSD 라이브러리에서 필요한 클래스를 가져오는 것부터 시작하세요. 이 단계는 코드에서 라이브러리의 기능을 활용할 수 있게 해주기 때문에 매우 중요합니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
전제 조건을 마치고 메인 이벤트에 뛰어 들자! PSD 파일에서 썸네일을 만드는 데는 몇 가지 간단한 단계가 포함되며, 제가 그 과정을 자세히 설명해 드리겠습니다.
## 1단계: 환경 설정
프로젝트를 시작하고 썸네일 생성을 준비하는 방법은 다음과 같습니다.
1. 자바 프로젝트를 생성합니다:
   - IDE를 열고 새 Java 프로젝트를 만듭니다.
   - "PsdThumbnailGenerator"와 같은 이름을 지정합니다.
2. Aspose.PSD 라이브러리 포함:
   -  Aspose.PSD JAR 파일을 프로젝트의 빌드 경로에 추가합니다. Maven을 사용하는 경우 Maven을`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## 2단계: PSD 파일 로드
다음으로 썸네일을 만들려는 PSD 파일을 로드해야 합니다. 
1. 문서 디렉토리를 지정하십시오:
   PSD 파일이 있는 디렉터리를 정의합니다.
   ```java
   String dataDir = "Your Document Directory"; // 귀하의 경로로 바꾸십시오.
   ```
2. PSD 파일을 로드합니다:
    사용`PsdImage` PSD 파일을 로드하는 클래스입니다.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 여기,`sample.psd` PSD 파일의 이름입니다. 파일 이름에 따라 이를 조정하세요.
## 3단계: PSD 리소스 반복
이제 PSD 이미지가 로드되었으므로 다음 단계는 해당 리소스를 검사하는 것입니다.
1. 자원 수 가져오기:
   PSD 파일의 모든 리소스를 반복해 보겠습니다.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // 자원 처리
   }
   ```
   
2. 썸네일 리소스 식별:
   루프 내에서 리소스가 썸네일인지 확인하세요.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // 썸네일 처리
   }
   ```
## 4단계: 썸네일 처리
썸네일 리소스를 식별한 후에는 그에 따라 처리해야 합니다.
1. 썸네일 형식 검색 및 확인:
   리소스가 실제로 썸네일인 경우 해당 리소스를 검색하고 형식을 확인하세요.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // 썸네일 생성 및 저장
   }
   ```
## 5단계: 썸네일 생성 및 저장
이곳이 바로 마법이 일어나는 곳입니다! 썸네일 데이터에서 새로운 이미지를 생성하고 저장하겠습니다.
1. 새 이미지 만들기:
   썸네일 리소스의 너비와 높이를 사용하여 새 비트맵 이미지를 만듭니다.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. 새 이미지에 픽셀을 저장합니다.
   썸네일 데이터를 새로 생성된 이미지로 전송합니다.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. 썸네일 이미지 저장:
   마지막으로 축소판 이미지를 고유한 이름으로 문서 디렉토리에 저장합니다.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## 결론
Java 및 Aspose.PSD를 사용하여 PSD 파일에서 썸네일을 만드는 것은 관리 가능한 단계로 분류하면 간단한 작업이 될 수 있습니다. 이 튜토리얼을 사용하면 이제 PSD 파일에서 썸네일을 쉽게 추출할 수 있어 작업 흐름을 향상시킬 수 있는 멋진 도구를 얻을 수 있습니다. 그럼 무엇이 당신을 막고 있나요? 일부 PSD 파일을 손에 넣고 사용해 보세요!
## FAQ
### Aspose.PSD란 무엇인가요?
Aspose.PSD는 개발자가 Photoshop 파일 작업을 할 수 있게 해주는 Java 라이브러리로, 프로그래밍 방식으로 PSD 파일을 더 쉽게 조작하고 관리할 수 있습니다.
### Aspose.PSD를 무료로 사용할 수 있나요?
예, Aspose는 라이선스를 구매하기 전에 라이브러리를 테스트하는 데 사용할 수 있는 무료 평가판을 제공합니다.
### 썸네일을 어떤 형식으로 저장할 수 있나요?
이 예에서는 썸네일을 BMP 형식으로 저장했지만 Aspose.PSD는 다양한 다른 형식도 지원합니다.
### Aspose.PSD를 사용하려면 Photoshop을 설치해야 합니까?
아니요, Aspose.PSD는 Photoshop과 독립적으로 작동합니다.
### Aspose.PSD에 대한 자세한 정보는 어디서 찾을 수 있나요?
 당신은 확인할 수 있습니다[Aspose.PSD 문서](https://reference.aspose.com/psd/java/) 자세한 내용, 튜토리얼, 리소스를 확인하세요.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

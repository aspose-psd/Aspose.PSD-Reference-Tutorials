---
title: Java에서 AI를 JPG로 변환
linktitle: Java에서 AI를 JPG로 변환
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 AI 파일을 Java에서 JPG로 손쉽게 변환하세요. 고품질 이미지 변환을 위한 단계별 가이드를 따르세요.
weight: 11
url: /ko/java/java-ai-to-image-format-conversion/convert-ai-to-jpg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 AI를 JPG로 변환

## 소개
Java를 사용하여 AI(Adobe Illustrator) 파일을 JPG 형식으로 변환하려고 하시나요? 더 이상 보지 마세요! 이 종합 가이드에서는 이미지 조작을 쉽게 만들어주는 강력하고 유연한 라이브러리인 Aspose.PSD for Java를 사용하는 전체 프로세스를 안내합니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 튜토리얼은 여러분이 알아야 할 모든 것을 제공합니다.
## 전제조건
코드를 살펴보기 전에 모든 것이 설정되어 있고 준비가 되었는지 확인하세요. 필요한 것은 다음과 같습니다.
1. JDK(Java Development Kit): JDK 8 이상이 설치되어 있는지 확인하세요.
2.  Java용 Aspose.PSD: 다음에서 라이브러리를 다운로드하세요.[여기](https://releases.aspose.com/psd/java/).
3. 개발 환경: IntelliJ IDEA, Eclipse 또는 원하는 텍스트 편집기와 같은 IDE.
4. AI 파일: 변환하려는 Adobe Illustrator 파일(.ai)입니다.
5. 기본 Java 지식: Java 프로그래밍 기본 사항에 익숙합니다.
## 패키지 가져오기
먼저, 이미지 변환 작업을 처리하는 데 필요한 패키지를 가져와야 합니다. 방법은 다음과 같습니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.ImageOptionsBase;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.JpegOptions;
```
이러한 가져오기는 AI 파일을 로드하고 JPG로 저장하기 위한 필수 클래스를 가져옵니다.
변환 프로세스를 간단하고 관리 가능한 단계로 나누어 보겠습니다. AI 파일을 쉽게 JPG로 변환하려면 따라해보세요.
## 1단계: 환경 설정
코딩을 시작하기 전에 개발 환경이 올바르게 설정되었는지 확인하세요. 프로젝트에 Java 라이브러리용 Aspose.PSD가 추가되어 있는지 확인하세요.
-  JDK 다운로드 및 설치: 아직 JDK를 다운로드하여 설치하지 않은 경우 다음 위치에서 JDK를 다운로드하여 설치하세요.[오라클 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html).
-  Aspose.PSD 다운로드: 다음에서 라이브러리를 가져옵니다.[Aspose 릴리스 페이지](https://releases.aspose.com/psd/java/).
- 프로젝트에 Aspose.PSD 추가: 프로젝트의 빌드 경로에 JAR 파일을 포함합니다.
## 2단계: AI 파일 로드
코드의 첫 번째 단계는 다음을 사용하여 AI 파일을 로드하는 것입니다.`AiImage` 수업. 이 클래스를 사용하면 Adobe Illustrator 파일을 원활하게 작업할 수 있습니다.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "34992OStroke.ai";
AiImage image = (AiImage) Image.load(sourceFileName);
```
 여기,`dataDir` AI 파일이 저장된 디렉토리입니다.`sourceFileName` AI 파일의 전체 경로입니다.
## 3단계: JPG 옵션 설정
 다음으로 JPG 출력에 대한 옵션을 설정해야 합니다. 그만큼`JpegOptions` 클래스는 JPG 파일의 품질 및 기타 설정을 구성하는 데 도움이 됩니다.
```java
JpegOptions options = new JpegOptions();
options.setQuality(85); // JPG의 품질을 설정하세요
```
이 예에서는 파일 크기와 이미지 품질의 균형을 맞추는 85로 품질을 설정했습니다. 요구 사항에 따라 이 값을 조정할 수 있습니다.
## 4단계: AI 파일을 JPG로 저장
 마지막으로 불러온 AI 파일을 JPG로 저장할 차례입니다. 우리는`save` 의 방법`AiImage` 이를 위해 수업을 합니다.
```java
String outFileName = dataDir + "34992OStroke.jpg";
image.save(outFileName, options);
```
이 코드 줄은 원하는 품질 설정으로 지정된 디렉터리에 이미지를 저장합니다.
## 5단계: 프로그램 실행
모든 설정이 완료되었으면 이제 Java 프로그램을 실행할 수 있습니다. IDE 또는 명령줄이 올바른 파일 경로와 클래스 이름을 가리키는지 확인하세요.
```java
public class AiToJpgConverter {
    public static void main(String[] args) {
        String dataDir = "Your Document Directory";
        String sourceFileName = dataDir + "34992OStroke.ai";
        String outFileName = dataDir + "34992OStroke.jpg";
        AiImage image = (AiImage) Image.load(sourceFileName);
        JpegOptions options = new JpegOptions();
        options.setQuality(85);
        image.save(outFileName, options);
        System.out.println("AI file converted to JPG successfully!");
    }
}
```
이 클래스를 실행하면 지정된 디렉터리에서 AI 파일이 JPG로 변환된 것을 볼 수 있습니다.
## 결론
Aspose.PSD 라이브러리를 사용하면 Java에서 AI 파일을 JPG로 변환하는 것이 간단합니다. 이 가이드에 설명된 단계를 따르면 출력 이미지의 품질을 제어하면서 이러한 변환을 쉽게 수행할 수 있습니다. Aspose.PSD for Java는 이미지 조작을 위한 광범위한 기능을 제공하는 강력한 도구로, 모든 개발자의 툴킷에 귀중한 추가 기능을 제공합니다.
## FAQ
### Java용 Aspose.PSD란 무엇입니까?
Aspose.PSD for Java는 Photoshop 및 Illustrator 파일 작업을 위한 Java API로, 이미지 조작을 위한 다양한 기능을 제공합니다.
### 출력 JPG에 대해 서로 다른 품질 수준을 설정할 수 있습니까?
 예, 다음에서 품질 설정을 조정할 수 있습니다.`JpegOptions` 출력 JPG의 품질과 크기를 제어합니다.
### Java용 Aspose.PSD는 무료로 사용할 수 있나요?
Aspose.PSD는 무료 평가판을 제공하지만 전체 기능을 사용하려면 라이센스를 구입해야 합니다. 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).
### 이 라이브러리를 사용하려면 Adobe Illustrator를 설치해야 합니까?
아니요, Adobe Illustrator를 설치할 필요가 없습니다. Aspose.PSD는 파일 형식을 독립적으로 처리합니다.
### Java용 Aspose.PSD에 대한 추가 문서는 어디서 찾을 수 있나요?
 포괄적인 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

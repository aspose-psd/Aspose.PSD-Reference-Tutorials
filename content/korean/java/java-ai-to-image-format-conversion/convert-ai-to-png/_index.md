---
title: Java에서 AI를 PNG로 변환
linktitle: Java에서 AI를 PNG로 변환
second_title: Aspose.PSD 자바 API
description: 이 가이드와 함께 Aspose.PSD를 사용하여 Java에서 AI를 PNG로 쉽게 변환하세요. 손쉽게 AI 파일을 로드하고, 옵션을 설정하고, PNG 이미지로 저장하는 방법을 알아보세요.
type: docs
weight: 13
url: /ko/java/java-ai-to-image-format-conversion/convert-ai-to-png/
---
## 소개
Java를 사용하여 Adobe Illustrator(.AI) 파일을 PNG 이미지로 변환하려고 하시나요? 당신은 올바른 장소에 왔습니다! 이 튜토리얼에서는 강력한 Java 라이브러리용 Aspose.PSD를 사용하여 프로세스를 단계별로 안내합니다. 이 가이드는 단 몇 줄의 코드만으로 AI 파일을 고품질 PNG로 원활하게 변환하는 방법을 이해하는 데 도움이 됩니다. 바로 뛰어 들어 봅시다!
## 전제조건
시작하기 전에 준비해야 할 몇 가지 사항이 있습니다.
1. JDK(Java Development Kit): 컴퓨터에 JDK 8 이상이 설치되어 있는지 확인하세요.
2.  Java용 Aspose.PSD: Java용 Aspose.PSD 라이브러리가 필요합니다. 다음에서 다운로드할 수 있습니다.[Aspose 릴리스 페이지](https://releases.aspose.com/psd/java/) 아니면[무료 시험판](https://releases.aspose.com/).
3. 통합 개발 환경(IDE): IntelliJ IDEA, Eclipse 또는 NetBeans와 같은 모든 Java IDE.
4. Java 기본 지식: Java 프로그래밍에 대한 기본적인 이해가 도움이 됩니다.
## 패키지 가져오기
먼저 필요한 Aspose.PSD 패키지를 Java 프로젝트로 가져와야 합니다. 환경을 설정해 보겠습니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```
이제 환경이 설정되었으므로 변환 프로세스를 따라하기 쉬운 단계로 나누어 보겠습니다.
## 1단계: AI 파일 로드
변환 프로세스의 첫 번째 단계는 Aspose.PSD 라이브러리를 사용하여 AI 파일을 Java 애플리케이션에 로드하는 것입니다.
```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage)Image.load(sourceFileName);
```
## 2단계: PNG 옵션 설정
다음으로 PNG 옵션을 설정해야 합니다. 여기에는 색상 유형 및 PNG 파일과 관련된 기타 설정을 정의하는 작업이 포함됩니다.
```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
```
## 3단계: 이미지를 PNG로 저장
마지막으로 지정된 옵션을 사용하여 로드된 AI 파일을 PNG 이미지로 저장합니다.
```java
String outFileName = dataDir + "34992OStroke.png";
image.save(outFileName, options);
```
그리고 그게 다야! AI 파일이 PNG로 성공적으로 변환되었습니다.
## 결론
Aspose.PSD를 사용하면 Java에서 AI 파일을 PNG로 쉽게 변환할 수 있습니다. 이 가이드에 설명된 단계를 따르면 이 기능을 Java 애플리케이션에 쉽게 통합할 수 있습니다. 그래픽 응용 프로그램에서 작업 중이거나 파일을 일괄 변환해야 하는 경우 Aspose.PSD는 작업을 효율적으로 완료하는 데 필요한 도구를 제공합니다.
## FAQ
### Aspose.PSD란 무엇인가요?
Aspose.PSD는 개발자가 PSD(Photoshop) 및 기타 Adobe 파일 형식으로 작업할 수 있도록 하는 Java 라이브러리입니다. 편집, 변환, 렌더링 등 다양한 작업을 지원합니다.
### Aspose.PSD를 무료로 사용할 수 있나요?
 Aspose.PSD를 다음과 함께 사용할 수 있습니다.[무료 시험판](https://releases.aspose.com/) , 그러나 전체 기능을 사용하려면 라이센스를 구입해야 합니다. 당신은 또한[임시면허](https://purchase.aspose.com/temporary-license/) 평가 목적으로.
### Aspose.PSD는 어떤 파일 형식을 지원합니까?
Aspose.PSD는 PSD, PSB, AI 및 기타 Adobe 파일 형식을 지원합니다. PNG, JPEG, BMP, TIFF 등 다양한 이미지 형식으로 변환할 수 있습니다.
### Aspose.PSD는 모든 Java 버전과 호환됩니까?
Aspose.PSD는 JDK 8 이상과 호환됩니다. 적절한 JDK 버전이 설치되어 있는지 확인하십시오.
### 추가 문서는 어디서 찾을 수 있나요?
 자세한 문서는 다음에서 찾을 수 있습니다.[Aspose.PSD 문서 페이지](https://reference.aspose.com/psd/java/).
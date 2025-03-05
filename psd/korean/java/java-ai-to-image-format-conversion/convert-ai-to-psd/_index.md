---
title: Java에서 AI를 PSD로 변환
linktitle: Java에서 AI를 PSD로 변환
second_title: Aspose.PSD 자바 API
description: 쉬운 단계별 가이드를 통해 Aspose.PSD를 사용하여 Java에서 AI를 PSD로 변환하세요. 빠르고 원활한 파일 변환이 필요한 개발자에게 적합합니다.
type: docs
weight: 14
url: /ko/java/java-ai-to-image-format-conversion/convert-ai-to-psd/
---
## 소개
Java를 사용하여 AI(Adobe Illustrator) 파일을 PSD(Adobe Photoshop) 파일로 변환하려고 하시나요? 글쎄, 당신은 바로 이곳에 있어요! 오늘은 강력한 Java용 Aspose.PSD 라이브러리를 사용하여 이 작업을 수행하는 방법을 살펴보겠습니다. 이 가이드는 전제 조건부터 자세한 단계별 지침까지 알아야 할 모든 것을 안내합니다. 디자인 파일을 원활하게 살펴보고 변환해 보세요.
## 전제조건
시작하기 전에 준비해야 할 몇 가지 사항이 있습니다.
1. JDK(Java Development Kit): 시스템에 JDK 8 이상이 설치되어 있는지 확인하십시오.
2.  Java용 Aspose.PSD: 다음에서 Java용 Aspose.PSD 라이브러리를 다운로드하세요.[다운로드 페이지](https://releases.aspose.com/psd/java/).
3. IDE(통합 개발 환경): Java 코드를 작성하고 실행하는 IntelliJ IDEA 또는 Eclipse와 같은 IDE입니다.
4. AI 파일: 변환하려는 Adobe Illustrator 파일입니다.
5.  Aspose 임시 라이센스(선택 사항): 제한 없이 전체 기능을 사용하려면[임시면허](https://purchase.aspose.com/temporary-license/).
## 패키지 가져오기
먼저 필요한 패키지를 가져와서 프로젝트를 설정해 보겠습니다. 프로젝트의 클래스 경로에 Java용 Aspose.PSD를 포함해야 합니다. 수행 방법은 다음과 같습니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
 또는 다음 위치에서 JAR 파일을 다운로드할 수 있습니다.[Java 다운로드 페이지용 Aspose.PSD](https://releases.aspose.com/psd/java/) 프로젝트에 수동으로 추가하세요.
프로세스를 간단하고 관리 가능한 단계로 나누어 보겠습니다.
## 1단계: 프로젝트 설정
먼저, 원하는 IDE에서 프로젝트를 설정하세요.
### 새 프로젝트 만들기
1. IDE를 열고 새 Java 프로젝트를 만듭니다.
2. 프로젝트 이름을 "AItoPSDConverter"와 같이 의미 있는 이름으로 지정하세요.
### Aspose.PSD 라이브러리 추가
1. JAR 파일을 다운로드한 경우 프로젝트의 빌드 경로에 추가하세요.
2.  Maven을 사용하는 경우 종속성이 올바르게 추가되었는지 확인하세요.`pom.xml`.
## 2단계: AI 파일 로드
이제 프로젝트가 설정되었으므로 변환하려는 AI 파일을 로드해 보겠습니다.
```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage) Image.load(sourceFileName);
```
## 3단계: PSD 옵션 설정
다음으로 PSD 출력에 대한 옵션을 설정해야 합니다.
```java
PsdOptions options = new PsdOptions();
```
## 4단계: AI 파일을 PSD로 저장
AI 파일이 로드되고 옵션이 설정되면 이제 PSD 파일로 저장할 수 있습니다.
```java
String outFileName = dataDir + "34992OStroke.psd";
image.save(outFileName, options);
```
## 결론
그리고 거기에 있습니다! Java용 Aspose.PSD를 사용하여 AI 파일을 PSD 파일로 성공적으로 변환했습니다. 이 강력한 라이브러리를 사용하면 Java 애플리케이션에서 복잡한 파일 변환을 간단하게 처리할 수 있습니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 가이드는 AI에서 PSD로의 변환 기능을 프로젝트에 쉽게 통합하는 데 도움이 될 것입니다.
## FAQ
### Java용 Aspose.PSD란 무엇입니까?
Aspose.PSD for Java는 개발자가 Adobe Photoshop 없이도 Java 애플리케이션 내에서 Photoshop 파일(PSD 및 PSB)을 생성, 편집 및 변환할 수 있는 강력한 라이브러리입니다.
### Java용 Aspose.PSD를 무료로 사용할 수 있나요?
 Aspose.PSD for Java는 다음에서 다운로드할 수 있는 무료 평가판을 제공합니다.[무료 평가판 페이지](https://releases.aspose.com/) . 전체 기능을 사용하려면[특허](https://purchase.aspose.com/buy) 필요합니다.
### Java용 Aspose.PSD의 임시 라이센스를 얻으려면 어떻게 해야 합니까?
 임시면허를 취득할 수 있습니다.[임시 라이센스 페이지](https://purchase.aspose.com/temporary-license/).
### PSD 파일을 다시 AI 파일로 변환할 수 있나요?
현재 Java용 Aspose.PSD는 PSD 파일을 AI 파일로 다시 변환하는 것을 지원하지 않습니다. PSD 및 PSB 파일 처리에 중점을 둡니다.
### 더 많은 예제와 문서는 어디에서 찾을 수 있나요?
 다음에서 포괄적인 문서와 예제를 찾을 수 있습니다.[Java 문서 페이지용 Aspose.PSD](https://reference.aspose.com/psd/java/).
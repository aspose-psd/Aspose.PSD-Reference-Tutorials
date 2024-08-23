---
title: Java에서 PSB를 JPG로 변환
linktitle: Java에서 PSB를 JPG로 변환
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 Java에서 PSB를 JPG로 쉽게 변환할 수 있습니다. 원활한 이미지 변환을 위한 자세한 가이드를 따르세요. Aspose.PSD를 다운로드하여 사용해 보고 구입하세요.
type: docs
weight: 10
url: /ko/java/java-psb-to-image-format-conversion/convert-psb-to-jpg-java/
---
## 소개
Java용 Aspose.PSD를 사용하여 PSB 파일을 JPG 형식으로 변환하는 방법에 대한 종합 가이드에 오신 것을 환영합니다! 대용량의 레이어가 있는 Photoshop 파일인 PSB 파일을 처리하고 이를 보다 보편적으로 지원되는 JPG 형식으로 변환해야 한다면 잘 찾아오셨습니다. 이 튜토리얼에서는 프로세스를 단계별로 안내해 드립니다. 결국에는 PSB 파일을 JPG로 쉽게 원활하게 변환할 수 있게 됩니다.
## 전제조건
튜토리얼을 시작하기 전에 전제 조건을 살펴보겠습니다. 시작하는 데 필요한 사항은 다음과 같습니다.
-  JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[오라클 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html).
-  Java 라이브러리용 Aspose.PSD: 다음에서 Java 라이브러리용 Aspose.PSD를 다운로드하세요.[다운로드 페이지](https://releases.aspose.com/psd/java/).
- 개발 환경: IntelliJ IDEA, Eclipse 또는 원하는 텍스트 편집기와 같은 IDE.
- PSB 파일: 변환하려는 PSB 파일입니다.
## 패키지 가져오기
먼저 필요한 패키지를 가져오겠습니다. 이러한 가져오기는 Aspose.PSD 라이브러리 작업 및 이미지 변환 처리에 필수적입니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.JpegOptions;
```
## 1단계: 프로젝트 설정
코딩을 시작하기 전에 Java 프로젝트를 설정하십시오. IDE에서 새 프로젝트를 만들고 프로젝트의 빌드 경로에 Java용 Aspose.PSD 라이브러리를 추가하세요. 이를 통해 Aspose.PSD에서 제공하는 클래스와 메서드를 사용할 수 있습니다.
## 2단계: PSB 파일 로드
 PSB 파일을 로드하려면 파일 경로를 지정하고 다음을 사용해야 합니다.`PsdLoadOptions` 로딩 프로세스를 구성합니다. 방법은 다음과 같습니다.
```java
String dataDir = "Your Document Directory"; // 디렉터리 경로로 바꾸세요.
String sourceFileName = dataDir + "Simple.psb";
PsdLoadOptions options = new PsdLoadOptions();
PsdImage image = (PsdImage) Image.load(sourceFileName, options);
```
 이 단계에서는 PSB 파일이 있는 디렉터리를 설정하고 해당 파일을`PsdImage` 객체를 사용하여`PsdLoadOptions`.
## 3단계: JPG 옵션 구성
이제 PSB 파일이 로드되었으므로 JPG 변환 옵션을 설정해야 합니다. 여기에는 JPG 출력 품질 지정이 포함됩니다.
```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(95);
```
여기서는`JpegOptions` 개체를 선택하고 품질을 95로 설정합니다. 이 값을 조정하여 출력 이미지의 압축 및 품질을 제어할 수 있습니다.
## 4단계: 이미지를 JPG로 저장
옵션을 설정하면 PSB 파일을 JPG로 저장할 수 있습니다. 실제 변환이 일어나는 곳입니다.
```java
image.save(dataDir + "Simple_output.jpg", jpgOptions);
```
이 명령은 로드된 PSB 이미지를 정의된 품질 설정을 사용하여 지정된 디렉터리에 JPG로 저장합니다.
## 5단계: 이미지를 PSB로 저장(선택 사항)
수정된 이미지를 PSB 파일로 다시 저장하려면 비슷한 명령을 사용하면 됩니다.
```java
image.save(dataDir + "Simple_output.psb");
```
이 단계는 선택 사항이지만 변환된 JPG와 함께 원본 PSB 파일의 계층 형식을 유지해야 하는 경우 유용합니다.
## 결론
축하해요! Java용 Aspose.PSD를 사용하여 PSB 파일을 JPG로 성공적으로 변환했습니다. 이 튜토리얼에서는 프로젝트 설정, PSB 파일 로드, JPG 옵션 구성 및 변환된 이미지 저장 과정을 안내했습니다. 다음 단계를 수행하면 Java 애플리케이션에서 PSB에서 JPG로의 변환을 쉽게 처리할 수 있습니다.
이미지 처리 애플리케이션을 개발하는 개발자이거나 가끔씩 PSB 파일을 변환해야 하는 경우 Aspose.PSD for Java는 귀하의 요구에 맞는 강력한 솔루션을 제공합니다.
## FAQ
### Java용 Aspose.PSD란 무엇입니까?
Aspose.PSD for Java는 개발자가 Java 애플리케이션 내에서 PSD 및 PSB 파일을 조작하고 변환할 수 있는 라이브러리입니다. Photoshop 파일 로드, 편집, 저장 등 다양한 기능을 지원합니다.
### 구매하기 전에 Java용 Aspose.PSD를 사용해 볼 수 있나요?
 예, 다음에서 Java용 Aspose.PSD 무료 평가판을 다운로드할 수 있습니다.[다운로드 페이지](https://releases.aspose.com/). 이를 통해 구매하기 전에 라이브러리와 해당 기능을 평가할 수 있습니다.
### Java용 Aspose.PSD의 임시 라이센스를 얻으려면 어떻게 해야 합니까?
 임시면허를 취득할 수 있습니다.[임시 라이센스 페이지](https://purchase.aspose.com/temporary-license/). 이를 통해 제한된 기간 동안 라이브러리의 모든 기능을 사용할 수 있습니다.
### 문제가 발생하면 지원을 받을 수 있나요?
 전적으로! 다음을 통해 지원에 액세스할 수 있습니다.[Aspose.PSD 지원 포럼](https://forum.aspose.com/c/psd/34). 지원팀은 귀하가 가질 수 있는 모든 문제나 질문에 대해 신속하게 대응하고 도움을 드릴 준비가 되어 있습니다.
### JPG 출력 품질을 조정할 수 있나요?
 예, 설정을 통해 JPG 출력 품질을 조정할 수 있습니다.`Quality` 에 있는 재산`JpegOptions` 물체. 값 범위는 0에서 100까지이며, 값이 높을수록 품질이 좋고 압축률이 낮음을 나타냅니다.
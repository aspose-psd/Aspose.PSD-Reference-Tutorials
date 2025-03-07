---
title: Java를 사용하여 PSD 파일의 레이어 회전
linktitle: Java를 사용하여 PSD 파일의 레이어 회전
second_title: Aspose.PSD 자바 API
description: 이 단계별 가이드를 통해 Java용 Aspose.PSD를 사용하여 PSD 파일의 레이어를 쉽게 회전하는 방법을 알아보세요.
weight: 21
url: /ko/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 PSD 파일의 레이어 회전

## 소개
그래픽 디자인 세계에서는 Photoshop 파일(PSD) 작업이 일반적인 활동입니다. 숙련된 디자이너이거나 이제 막 이미지 조작을 시작하는 경우 PSD 파일에서 레이어를 회전하는 방법을 알면 시간을 절약할 수 있습니다. 하지만 여기서 까다로워지는 부분이 있습니다. 모든 사람이 Adobe Photoshop에 액세스할 수 있는 것은 아니며 복잡한 인터페이스를 배우고 싶어하지도 않습니다. 이것이 바로 Java가 등장하여 프로그래밍 방식으로 PSD 파일을 더 쉽게 조작할 수 있게 해줍니다. 이 기사에서는 레이어 회전을 포함하여 PSD 파일을 원활하게 작업할 수 있는 강력한 Java용 Aspose.PSD 라이브러리를 살펴보겠습니다. 이제 소매를 걷어붙이고 디자인 작업 흐름을 더욱 원활하게 만드는 방법에 대해 알아보세요!
## 전제조건
시작하기 전에 준비해야 할 몇 가지 사항이 있습니다.
### JDK(자바 개발 키트)
 컴퓨터에 JDK가 설치되어 있는지 확인하십시오. 아직 다운로드하지 않았다면 다음에서 다운로드하세요.[오라클 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html).
### 통합 개발 환경(IDE)
IntelliJ IDEA, Eclipse 또는 NetBeans와 같은 IDE를 사용하면 코딩 경험이 훨씬 더 즐거워질 수 있습니다.
### Java 라이브러리용 Aspose.PSD
 프로젝트에 Java 라이브러리용 Aspose.PSD를 다운로드하여 포함하세요. 에서 받으실 수 있습니다.[릴리스 페이지](https://releases.aspose.com/psd/java/).
### 자바의 기본 지식
Java 프로그래밍을 잘 이해하는 것이 필수적입니다. 클래스, 패키지, 객체 지향 프로그래밍과 같은 개념에 익숙해야 합니다.
## 패키지 가져오기
Java용 Aspose.PSD를 시작하려면 먼저 필요한 패키지를 가져와야 합니다. 방법은 다음과 같습니다.
## 1단계: Java 프로젝트 설정
즐겨 사용하는 IDE에서 새 Java 프로젝트를 만든 다음 Aspose.PSD 라이브러리를 프로젝트의 빌드 경로에 추가하세요.
## 2단계: 필수 클래스 가져오기
Java 파일 상단에서 다음 클래스를 가져와야 합니다.
```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```
이러한 가져오기를 통해 코드 전체에서 활용할 핵심 기능에 대한 액세스를 제공합니다. 

이제 환경을 설정하고 필요한 패키지를 가져왔으므로 PSD 파일에서 레이어를 회전하는 프로세스를 단계별로 분석해 보겠습니다.
## 1단계: 파일 경로 설정

먼저 PSD 파일의 위치와 수정된 이미지를 저장할 위치를 정의해야 합니다. 
```java
String dataDir = "Your Document Directory"; // 이를 실제 문서 디렉토리로 변경하십시오.
String sourceFile = dataDir + "1.psd"; // 소스 PSD 파일
String pngPath = dataDir + "RotateFlipTest2617.png"; // 출력 PNG 파일 경로
String psdPath = dataDir + "RotateFlipTest2617.psd"; // 출력 PSD 파일 경로
```
 여기에서 업데이트를 확인하세요.`"Your Document Directory"` PSD 파일이 저장된 경로로 이동하세요.
## 2단계: PSD 파일 로드

다음으로 PSD 파일을 프로그램에 로드하여 조작할 수 있도록 하겠습니다.
```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```
 사용하여`Image.load()` , 우리는 파일을 조작 가능한 파일로 쉽게 변환할 수 있습니다.`PsdImage` 물체.
## 3단계: 이미지 회전

 이제 재미있는 부분입니다! 로드된 PSD 이미지를 회전해 보겠습니다. 그만큼`RotateFlipType` 클래스는 이미지 회전 및 뒤집기에 대한 다양한 옵션을 제공합니다. 우리의 경우에는`Rotate270FlipXY`.
```java
int flipType = RotateFlipType.Rotate270FlipXY; // 회전 유형을 선택하세요
im.rotateFlip(flipType); // 이미지 회전
```
이 선은 이미지를 효과적으로 270도 회전시킵니다. 제공되는 다양한 옵션을 자유롭게 실험해 보세요.`RotateFlipType`!
## 4단계: 이미지를 PNG로 저장

회전한 후에는 조작된 이미지를 저장해야 합니다. 레이어의 투명도를 유지하기 위해 PNG 형식으로 저장하겠습니다.
```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // 투명성 유지
im.save(pngPath, options); // 회전된 이미지 저장
```
 색상 유형을 다음과 같이 설정하는 것이 중요합니다.`TruecolorWithAlpha` PNG 파일로 저장할 때 투명도 안정성을 유지합니다.
## 5단계: 수정된 PSD 저장

변경 사항과 함께 원본 PSD 파일을 보존하려면 수정된 이미지를 새 PSD 파일로 다시 저장할 수 있습니다.
```java
im.save(psdPath);
```
이제 지정된 디렉토리에 PNG와 수정된 PSD 파일이 모두 있습니다!
## 결론
Java 라이브러리용 Aspose.PSD를 활용하면 PSD 파일의 레이어를 회전하는 작업이 간단해집니다. 이 가이드를 통해 PSD 파일을 조작하는 방법을 배웠을 뿐만 아니라 Java 기술도 연마할 수 있습니다. 프로그래밍을 통해 디자인 작업 흐름을 간소화할 수 있다는 점이 멋지지 않나요? 그래서, 당신은 무엇을 기다리고 있습니까? PSD 파일을 가져와 실험을 시작하세요!
## 자주 묻는 질문
### PSD 파일에서 특정 레이어를 회전할 수 있나요?
 예, 사용할 수 있습니다`Layer.rotateFlip()` 레이어를 반복한 후 특정 레이어에 대한 메서드`PsdImage`.
### Java용 Aspose.PSD에 성능 제한이 있습니까?
일반적으로 성능은 좋지만 매우 큰 파일을 처리하려면 충분한 메모리 리소스가 필요할 수 있습니다. 광범위한 프로젝트의 경우 항상 미리 테스트하십시오.
### Aspose.PSD는 무료로 사용할 수 있나요?
 Aspose는 무료 평가판을 제공하지만 장기간 사용하려면 유료 라이선스가 필요합니다. 확인해 보세요[임시면허](https://purchase.aspose.com/temporary-license/) 테스트용.
### 자세한 문서는 어디서 찾을 수 있나요?
 다음에서 포괄적인 문서를 찾을 수 있습니다.[Aspose.PSD 문서](https://reference.aspose.com/psd/java/).
### Aspose.PSD를 사용하는 동안 문제가 발생하면 어떻게 되나요?
 다음을 통해 도움을 요청하세요.[Aspose 지원 포럼](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

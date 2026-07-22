---
date: 2026-02-17
description: Aspose.PSD for Java를 사용하여 PSD 레이어를 추출하고 PSD 레이어를 PNG로 변환하는 방법을 배웁니다.
  강력한 그래픽 조작이 필요한 개발자에게 적합합니다.
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: Aspose.PSD Java를 사용하여 PSD 레이어 추출 및 PSD 파일에 레이어 지원 추가
url: /ko/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java를 사용하여 PSD 레이어 추출 및 PSD 파일에 레이어 지원 추가

## 소개
Photoshop Document (PSD) 파일 작업은 그래픽 디자이너와 개발자 모두에게 일상적인 현실입니다. 가장 일반적인 작업 중 하나는 **PSD 레이어를 추출**하여 편집, 재활용 또는 PNG와 같은 형식으로 변환하는 것입니다. Java에서는 Aspose.PSD가 이 과정을 간단하고 코드로 만들기 시작합니다. 이 튜토리얼에서는 PSD 레이어를 추출하고 레이어 지원을 활성화하며 **PSD 레이어를 PNG로 변환**하는 방법을 명확한 설명과 실용적인 팁과 함께 살펴보겠습니다.

## 빠른 답변
- **“PSD 레이어 추출”은 무엇을 의미합니까?** PSD 파일을 로드하고 개별 레이어에 접근하여 처리하는 것을 의미합니다.
- **Java에서 처리하는 것은?** Aspose.PSD for Java는 Photoshop이 필요하지 않은 완전한 PSD 처리 기능을 제공합니다.
- **PSD 레이어를 한 번에 PNG로 변환할 수 있습니까?** 네—적절한 옵션으로 파일을 로드하고 이를 유지하는 PNG 옵션으로 저장하면 됩니다.
- **프로덕션 사용에 필요한 권한이 있습니까?**
- **필요한 Java 버전은?** JDK 8 이상(튜토리얼 예시로 JDK 11을 사용합니다).

## Aspose.PSD for Java를 사용하여 PSD 레이어를 추출하는 방법
하단 환경 설정부터 최종 PNG 저장까지 모든 과정을 마치고 안내합니다. 번호가 매겨진 각 단계를 따라 몇 분 안에 작동하는 솔루션을 만들 수 있습니다.

## PSD 레이어를 추출하여 PNG로 변환하는 이유는 무엇입니까?
- **자산 재활용:** 마스터 PSD에서 아이콘, 버튼, UI 요소 등을 수동으로 제거하고 추출합니다.
- **자동화:** 썸네일이나 웹용 이미지를 즉시 생성합니다.
- **투명성 반대:** PNG는 알파 채널을 유지하므로 웹 그래픽에 적합합니다.
- **크로스 플랫폼:** 서버에는 Photoshop이 필요하지 않으며 Aspose.PSD는 Java가 실행되는 독립적인 동작입니다.

## 필수 조건
시작하기 전에 다음 사항을 확인하세요.

1. **Java 개발 환경** – JDK가 설치되어 있어야 합니다. [오라클 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드할 수 있습니다.

2. **Aspose.PSD for Java** – 공식 다운로드 페이지 [여기](https://releases.aspose.com/psd/java/)에서 최신 라이브러리를 다운로드하세요.

3. **기본적인 Java 지식** – Java 프로그램을 컴파일하고 실행하는 데 익숙해야 합니다.

4. **IDE** – IntelliJ IDEA, Eclipse 또는 원하는 편집기를 사용하세요.

5. **PSD 파일** – 가지고 있는 PSD 파일을 사용하거나 테스트용 샘플 PSD 파일을 다운로드하세요.

위의 준비가 완료되면 PSD 레이어 추출을 시작할 수 있습니다.

## 패키지 가져오기
먼저 Aspose.PSD 라이브러리에서 필요한 클래스를 가져옵니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 1단계: 디렉터리 정의
원본 PSD 파일과 출력 PNG 파일의 경로를 설정합니다. `dataDir`이 파일이 있는 폴더를 가리키도록 조정하세요.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"문서 디렉터리"`를 실제 폴더 경로로 바꾸세요.
- `sourceFileName` – 처리할 PSD 파일의 전체 경로입니다.
- `output` – 추출된 레이어가 포함될 PNG 파일의 저장 경로입니다.

## 2단계: 로드 옵션 설정
`PsdLoadOptions`를 구성하면 모든 레이어 효과와 리소스가 올바르게 로드됩니다. 이는 PSD 레이어를 추출할 때 매우 중요합니다.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – 레이어에 추가 효과(예: 그림자 효과)를 로드합니다.
- `setUseDiskForLoadEffectsResource(true)` – 용량이 큰 리소스를 디스크로 오프로드하여 메모리 사용량을 줄입니다.

## 3단계: PSD 파일 불러오기
이제 위에서 정의한 옵션을 사용하여 PSD 파일을 `PsdImage` 객체로 불러옵니다.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

이 시점에서 `image` 객체에는 모든 레이어, 마스크 및 효과가 포함되어 추출 준비가 완료됩니다.

## 4단계: 저장 옵션 설정
PNG 저장 방식을 구성합니다. `TruecolorWithAlpha`를 사용하면 원본 레이어의 투명도가 유지됩니다.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## 5단계: 이미지 저장 (PSD 레이어를 PNG로 변환)
불러온 PSD 파일(모든 레이어 포함)을 단일 PNG 파일로 내보냅니다. 이 단계는 PSD 레이어를 한 번에 **PNG로 변환**하는 작업입니다.

## 5단계: 이미지 저장 (PSD 레이어를 PNG로 변환)
불러온 PSD 파일(모든 레이어 포함)을 단일 PNG 파일로 내보냅니다. 이 단계는 PSD 레이어를 한 번에 **PNG로 변환**하는 작업입니다.

```java
image.save(output, saveOptions);
```

각 레이어를 별도의 PNG 파일로 저장해야 하는 경우 `image.getLayers()`를 반복하여 사용할 수 있지만, 대부분의 경우 병합된 PNG 파일로 충분합니다.

## 6단계: 마무리
프로세스가 성공적으로 완료되었음을 알리는 콘솔 메시지를 추가합니다

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## 일반적인 문제 및 팁
- **메모리 부족 오류:** 매우 큰 PSD 파일을 처리하는 경우, 임시 데이터를 오프로드하기 위해 `setUseDiskForLoadEffectsResource(true)`를 활성화 상태로 유지하세요.

- **효과 누락:** `setLoadEffectsResource(true)`가 설정되어 있는지 확인하세요. 그렇지 않으면 일부 레이어 효과가 무시될 수 있습니다.

- **경로 문제:** 플랫폼에 관계없이 경로를 처리하려면 `java.nio.file`의 `Paths.get(...)`을 사용하세요.

## 자주 묻는 질문

**질문: Aspose.PSD for Java란 무엇인가요?**
답변: Aspose.PSD for Java는 Photoshop이 설치되어 있지 않아도 PSD 파일을 조작할 수 있는 라이브러리입니다.

**질문: Aspose.PSD를 다른 파일 형식에도 사용할 수 있나요?**
답변: 네! Aspose는 주로 PSD 파일용으로 개발되었지만, 다양한 다른 파일 형식용 라이브러리도 제공합니다.

**질문: 체험판이 있나요?**
답변: 네, 물론입니다! [여기](https://releases.aspose.com/)에서 무료 체험판을 다운로드하실 수 있습니다.

**질문: 도움이 필요할 경우 어디에서 지원을 받을 수 있나요?**
답변: Aspose 포럼 [여기](https://forum.aspose.com/c/psd/34)에서 지원을 받으실 수 있습니다.

**질문: PNG 파일을 PSD 파일로 다시 변환할 수 있나요?**
답변: Aspose.PSD 라이브러리는 다른 형식을 PSD로 변환하는 기능보다는 PSD 파일을 읽고 조작하는 데 더 중점을 두고 있습니다.

**질문: 각 레이어를 개별 PNG 파일로 추출하려면 어떻게 해야 하나요?**
답변: `image.getLayers()`를 반복하여 각 레이어에 대해 새로운 `Bitmap` 객체를 생성하고, 각 레이어의 `PngOptions` 속성을 지정하여 저장하면 레이어별 개별 PNG 파일을 얻을 수 있습니다.


## 결론
이제 Aspose.PSD for Java를 사용하여 **PSD 레이어 추출**, 전체 레이어 지원 활성화, **PSD 레이어를 PNG로 변환**하는 방법을 배웠습니다. 자동화된 에셋 파이프라인을 구축하든 데스크톱 앱에 그래픽 기능을 추가하든, 이 접근 방식을 통해 Photoshop 자체 없이도 Photoshop 파일을 세밀하게 제어할 수 있습니다. 필터 적용, 레이어 병합, 각 레이어 개별 내보내기 등 더 자세한 내용을 살펴보세요.

---

**최종 업데이트:** 2026년 2월 17일
**테스트 환경:** Aspose.PSD for Java 24.11 (작성 시점 기준 최신 버전)
**제작자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-09-23
description: Aspose.PSD for Java를 사용하여 PSD 벡터 형태를 수정하고 PSD 파일을 일괄 처리하는 방법을 배웁니다. 완전한
  솔루션을 위한 자세한 단계, 팁 및 코드 자리표시자가 제공됩니다.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: PSD에서 Length Record Data 속성 지원 - Java
og_description: Aspose.PSD for Java를 사용하여 PSD 벡터 형태를 수정하고 PSD 파일을 일괄 처리하는 방법을 배웁니다.
  코드 자리표시자와 전문가 팁이 포함된 단계별 가이드.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Aspose.PSD for Java를 사용하여 PSD 벡터 형태 수정
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Aspose.PSD for Java를 사용하여 PSD 벡터 형태 수정
url: /ko/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD 벡터 모양 수정

## 소개
프로그래밍 방식으로 **PSD 벡터 모양을 수정**해야 하는 경우, Aspose.PSD for Java는 Java 코드에서 직접 Photoshop 파일을 완전히 제어할 수 있게 해줍니다. 이 튜토리얼에서는 벡터 모양 레이어를 편집할 때 필수적인 단계인 length record 속성 지원 방법을 안내합니다. 끝까지 진행하면 PSD를 열고, 벡터 모양 데이터를 조정한 뒤, Photoshop을 실행하지 않고도 업데이트된 파일을 저장할 수 있게 됩니다.

## 빠른 답변
- **“modify PSD vector shapes”는 무엇을 의미합니까?** PSD 파일 내부의 벡터 기반 레이어의 기하학, 경로 연산 또는 기타 속성을 조정하는 것을 의미합니다.  
- **어떤 라이브러리가 이를 처리합니까?** Aspose.PSD for Java.  
- **라이선스가 필요합니까?** 무료 체험판으로 평가가 가능하며, 상용 라이선스는 프로덕션에 필요합니다.  
- **구현에 얼마나 걸립니까?** 기본적인 모양 수정 스크립트의 경우 약 10‑15분 정도 소요됩니다.  
- **주요 전제 조건은 무엇입니까?** Java JDK, Aspose.PSD for Java, 및 샘플 PSD 파일.

## “support length record properties”란 무엇입니까?
length record properties 지원은 PSD 내부의 각 벡터 경로를 설명하는 `LengthRecord` 객체에 접근하고 이를 업데이트하는 것을 의미합니다. 이러한 레코드는 경로의 길이, 유형 및 다른 경로와의 연결 방식과 같은 정보를 저장합니다. 이를 변경하면 모양이 결합, 교차 또는 서로 빼는 방식을 제어할 수 있어 정밀한 벡터 편집이 가능해집니다.

## 왜 Aspose.PSD for Java를 사용하여 length record properties를 지원합니까?
Photoshop 없이 PSD를 로드하고, 벡터 데이터를 편집하고, 저장할 수 있습니다. Aspose.PSD는 일반 서버에서 수백 페이지 PSD를 2초 미만에 처리하며, 150개 이상의 클래스(30개 이상의 벡터 관련 타입 포함)를 제공하고, Windows, Linux, macOS에서 JDK 11+와 함께 실행됩니다. 이 성능 중심 라이브러리는 비용이 많이 드는 데스크톱 소프트웨어의 필요성을 없애줍니다.

## 전제 조건
1. **Java Development Kit (JDK)** – [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드하거나 선호하는 패키지 관리자를 사용하십시오.  
2. **Aspose.PSD for Java** – 최신 JAR 파일을 [Aspose releases page](https://releases.aspose.com/psd/java/)에서 받으세요.  
3. **IDE** – IntelliJ IDEA, Eclipse 또는 Java 호환 편집기.  
4. **PSD 파일** – Photoshop에서 만들거나 실험용 샘플 PSD를 가져오세요.  
5. **기본 Java 지식** – 클래스, 객체 및 예외 처리에 익숙함.

## 패키지 가져오기
import 문은 `PsdImage`, `VsmsResource`, `LengthRecord`와 같은 핵심 Aspose.PSD 클래스를 범위에 가져옵니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 1단계: 소스 및 출력 디렉터리 설정
원본 PSD가 위치한 경로와 수정된 파일을 쓸 경로를 정의합니다.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 2단계: PSD 파일 로드
`Image.load`를 사용하여 파일을 열고 PSD 전용 기능을 위해 `PsdImage`로 캐스팅합니다.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 3단계: 레이어에서 Vsms 리소스 찾기
`VsmsResource`는 레이어의 벡터 모양 데이터를 저장하는 컨테이너입니다. 두 번째 레이어의 리소스를 순회하여 이를 찾습니다.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 4단계: length 레코드 접근
`LengthRecord`는 개별 벡터 경로를 나타냅니다. 수정하려는 레코드를 가져옵니다.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 5단계: 경로 연산 속성 수정
`PathOperations`는 개별 모양이 어떻게 상호 작용하는지 정의합니다(예: 제외, 교차, 뺄셈). 이러한 값을 변경하면 벡터 레이어의 시각적 구성이 업데이트됩니다.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 6단계: 수정된 PSD 파일 저장
변경 사항을 새 파일에 저장합니다.

```java
psdImage.save(outPsdFilePath);
```

## 7단계: 리소스 정리
메모리를 해제하고 리소스 누수를 방지하기 위해 `PsdImage` 인스턴스를 폐기합니다.

```java
psdImage.dispose();
```

## length record properties를 지원하여 PSD 파일을 배치 처리하는 방법
단일 파일 워크플로를 루프로 감싸서 PSD 디렉터리를 순회하면서 각 파일에 대해 `inPsdFilePath`와 `outPsdFilePath`를 업데이트합니다. 이 방법을 사용하면 수십 또는 수백 개의 파일에 동일한 벡터 모양 조정을 몇 분 안에 적용할 수 있어 자동화된 자산 파이프라인에 이상적입니다.

## 일반적인 함정 및 팁
- **Null 체크** – 멤버에 접근하기 전에 `resource`가 `null`이 아닌지 항상 확인하세요.  
- **경로 인덱스 범위** – 사용 중인 인덱스(예: `[2]`, `[7]`, `[11]`)가 편집 중인 특정 PSD에 존재하는지 확인하세요.  
- **라이선스** – 유효한 라이선스 없이 실행하면 저장된 PSD에 워터마크가 삽입됩니다.

## 결론
이제 Aspose.PSD for Java를 사용하여 length record properties를 지원함으로써 **PSD 벡터 모양을 수정**하는 완전한 엔드‑투‑엔드 예제가 준비되었습니다. 자산 파이프라인을 자동화하거나 맞춤형 디자인 도구를 구축하든, 이러한 API를 통해 수동 Photoshop 작업 없이 벡터 레이어를 조작할 수 있는 유연성을 얻을 수 있습니다. 다른 `PathOperations` 값을 실험하거나 여러 `LengthRecord` 편집을 결합하여 복잡한 모양을 만들어 보세요.

## 자주 묻는 질문

**Q: 벡터 모양 레이어가 없는 PSD를 어떻게 처리합니까?**  
A: `VsmsResource`가 없으므로 `resource`는 `null` 상태로 남습니다. 체크를 추가하고 수정 단계를 건너뛰거나 사용자에게 알리세요.

**Q: 채우기 색상이나 스트로크 두께와 같은 다른 속성을 변경할 수 있습니까?**  
A: 예, `LengthRecord`는 채우기, 스트로크 및 불투명도에 대한 setter를 제공합니다. 전체 목록은 API 문서를 참조하세요.

**Q: 여러 PSD 파일을 배치 처리할 수 있습니까?**  
A: 물론 가능합니다. 코드를 루프로 감싸서 PSD 파일 디렉터리를 순회하면서 매번 입력 및 출력 경로를 조정하면 됩니다.

**Q: 파일 경로에서 로드할 때 스트림을 수동으로 닫아야 합니까?**  
A: `Image.load`는 파일 스트림을 자동으로 처리하지만, `InputStream`에서 로드하는 경우 사용 후 닫는 것을 기억하세요.

**Q: 이러한 API를 사용하려면 어떤 버전의 Aspose.PSD가 필요합니까?**  
A: `LengthRecord`와 `PathOperations` 클래스는 Aspose.PSD 20.10부터 제공되었습니다. 최신 버전(작성 시 24.11) 사용을 권장합니다.

---

**마지막 업데이트:** 2026-09-23  
**테스트 환경:** Aspose.PSD for Java 24.11  
**작성자:** Aspose

## 관련 튜토리얼

- [PSD를 PNG로 변환하고 Java에서 벡터 마스크 만들기 – PSD 파일의 Vmsk 리소스](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Aspose.PSD for Java를 사용하여 레이어 마스크 지원으로 PSD를 PNG로 변환](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [PSD 파일에 레이어 지원 추가](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
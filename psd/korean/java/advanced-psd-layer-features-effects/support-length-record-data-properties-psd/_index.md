---
date: 2026-02-20
description: Aspose.PSD for Java를 사용하여 길이 레코드 속성을 지원하고 PSD 파일을 일괄 처리하는 방법을 배워보세요.
  코드 예제가 포함된 단계별 가이드.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: 길이 레코드 속성 지원 – PSD 벡터 형태 수정 (Java)
url: /ko/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---



All good.

Now produce final output with all content. Ensure shortcodes remain.

Let's assemble.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 길이 레코드 속성 지원 – PSD 벡터 형태 수정 (Java)

## 소개
프로그램matically **PSD 벡터 형태**를 수정해야 한다면, Aspose.PSD for Java 라이브러리를 통해 Java 코드만으로 Photoshop 파일을 완전히 제어할 수 있습니다. 이 튜토리얼에서는 **길이 레코드 속성 지원**에 대해 알아야 할 모든 것을 단계별로 안내합니다—벡터 형태 레이어를 편집하려는 경우 필수적인 단계입니다. 튜토리얼을 마치면 PSD를 열어 벡터 형태 속성을 조정하고, IDE를 떠나지 않고도 업데이트된 파일을 저장할 수 있게 됩니다. 시작해 봅시다!

## 빠른 답변
- **“PSD 벡터 형태 수정”이란 무엇을 의미하나요?** PSD 파일 내부의 벡터 기반 레이어의 기하학, 경로 연산 또는 기타 속성을 조정하는 것을 의미합니다.  
- **어떤 라이브러리가 이를 처리하나요?** Aspose.PSD for Java.  
- **라이선스가 필요합니까?** 평가용으로는 무료 체험판을 사용할 수 있지만, 실제 운영을 위해서는 상용 라이선스가 필요합니다.  
- **구현에 얼마나 걸리나요?** 기본 형태 수정 스크립트의 경우 약 10‑15분 정도 소요됩니다.  
- **주요 사전 요구 사항은 무엇인가요?** Java JDK, Aspose.PSD for Java, 그리고 샘플 PSD 파일입니다.

## “길이 레코드 속성 지원”이란?
길이 레코드 속성을 지원한다는 것은 PSD 내부의 각 벡터 경로를 설명하는 `LengthRecord` 객체에 접근하고 이를 업데이트하는 것을 의미합니다. 이러한 레코드를 변경하면 형태가 서로 결합, 교차 또는 차감되는 방식을 제어할 수 있습니다.

## 왜 Aspose.PSD for Java를 사용해 길이 레코드 속성을 지원해야 할까요?
- **Photoshop 불필요** – 서버에서 직접 PSD 파일을 작업합니다.  
- **풍부한 API** – 강력히 타입이 지정된 클래스를 사용해 레이어, 리소스 및 벡터 데이터를 접근합니다.  
- **크로스 플랫폼** – Windows, Linux, macOS 어느 환경에서도 JDK와 함께 실행됩니다.  
- **성능 중심** – 효율적인 메모리 관리와 빠른 저장 작업을 제공합니다.  

## 사전 요구 사항
1. **Java Development Kit (JDK)** – [Oracle 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드하거나 선호하는 패키지 관리자를 사용하세요.  
2. **Aspose.PSD for Java** – 최신 JAR 파일을 [Aspose 릴리스 페이지](https://releases.aspose.com/psd/java/)에서 받으세요.  
3. **IDE** – IntelliJ IDEA, Eclipse 또는 Java와 호환되는 편집기.  
4. **PSD 파일** – Photoshop에서 만들거나 실험용 샘플 PSD를 구하세요.  
5. **기본 Java 지식** – 클래스, 객체 및 예외 처리에 익숙해야 합니다.

## 패키지 가져오기
먼저, PSD 파일 및 벡터 형태 리소스를 다루는 데 필요한 클래스를 가져옵니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 단계 1: 소스 및 출력 디렉터리 설정
원본 PSD가 위치한 경로와 수정된 파일을 저장할 경로를 정의합니다.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 단계 2: PSD 파일 로드
`Image.load`를 사용해 파일을 열고, PSD 전용 기능을 위해 `PsdImage`로 캐스팅합니다.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 단계 3: 레이어에서 Vsms 리소스 찾기
벡터 형태 데이터는 `VsmsResource` 내부에 있습니다. 두 번째 레이어의 리소스를 순회하며 이를 찾습니다.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 단계 4: Length Record 접근
각 `LengthRecord`는 개별 벡터 경로를 나타냅니다. 수정하려는 레코드를 가져옵니다.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 단계 5: Path Operation 속성 수정
이제 `PathOperations`를 변경하여 **PSD 벡터 형태**를 수정할 수 있습니다. 이는 형태가 어떻게 상호 작용하는지(예: 배제, 교차, 차감)를 결정합니다.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 단계 6: 수정된 PSD 파일 저장
변경 사항을 새 파일에 저장합니다.

```java
psdImage.save(outPsdFilePath);
```

## 단계 7: 리소스 정리
메모리를 해제하기 위해 `PsdImage`를 폐기합니다.

```java
psdImage.dispose();
```

## 길이 레코드 속성을 지원하면서 PSD 파일을 배치 처리하는 방법
여러 PSD에 동일한 벡터 형태 조정을 적용해야 한다면, 위 코드를 파일 디렉터리를 순회하는 루프에 감싸세요. 각 반복마다 `inPsdFilePath`와 `outPsdFilePath`를 업데이트하면 **PSD 파일을 배치 처리**할 수 있습니다.

## 일반적인 함정 및 팁
- **Null 검사** – 경로에 접근하기 전에 `resource`가 `null`이 아닌지 항상 확인하세요.  
- **경로 인덱스 범위** – 사용 중인 인덱스(`[2]`, `[7]`, `[11]`)가 편집 중인 PSD에 존재하는지 확인하세요.  
- **라이선스** – 유효한 라이선스 없이 실행하면 저장된 PSD에 워터마크가 삽입됩니다.  

## 결론
이제 Aspose.PSD for Java를 사용해 길이 레코드 속성을 지원하면서 **PSD 벡터 형태**를 **수정**하는 완전한 엔드‑투‑엔드 예제를 보유하게 되었습니다. 자산 파이프라인을 자동화하거나 맞춤형 디자인 도구를 구축하든, 이 API를 통해 수동 Photoshop 작업 없이도 벡터 레이어를 자유롭게 조작할 수 있습니다. 다른 `PathOperations`를 실험하거나 복합 형태를 위해 여러 `LengthRecord` 편집을 결합해 보면서 더 탐구해 보세요.

## 자주 묻는 질문

**Q: 벡터 형태 레이어가 없는 PSD를 어떻게 처리하나요?**  
A: `VsmsResource`가 없으므로 `resource`는 `null` 상태로 남습니다. 체크를 추가해 수정 단계를 건너뛰거나 사용자에게 알리세요.

**Q: 채우기 색상이나 스트로크 두께와 같은 다른 속성을 변경할 수 있나요?**  
A: 네, `LengthRecord`는 채우기, 스트로크 및 불투명도에 대한 추가 setter를 제공합니다. 자세한 내용은 API 문서를 참고하세요.

**Q: 여러 PSD 파일을 배치 처리할 수 있나요?**  
A: 물론 가능합니다. 코드를 PSD 파일 디렉터리를 순회하는 루프에 감싸고, 매번 입력 및 출력 경로를 조정하면 됩니다.

**Q: 파일 경로에서 로드할 때 스트림을 수동으로 닫아야 하나요?**  
A: `Image.load` 메서드는 파일 스트림을 내부적으로 처리하지만, `InputStream`에서 로드할 경우 사용 후 닫는 것을 잊지 마세요.

**Q: 이러한 API를 사용하려면 어떤 버전의 Aspose.PSD가 필요합니까?**  
A: `LengthRecord`와 `PathOperations` 클래스는 Aspose.PSD 20.10부터 제공됩니다. 최신 버전을 사용하는 것이 권장됩니다.

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
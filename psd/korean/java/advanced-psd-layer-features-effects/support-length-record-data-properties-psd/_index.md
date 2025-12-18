---
date: 2025-12-17
description: Aspose.PSD for Java를 사용하여 길이 레코드 데이터 속성을 지원함으로써 PSD 벡터 형태를 수정하는 방법을 배웁니다.
  단계별 가이드와 코드 예제.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: PSD 벡터 도형을 수정하는 방법 – Java에서 Support Length 레코드 데이터 속성 지원
url: /ko/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD에서 Length Record Data Properties 지원 - Java

## 소개
프로그래밍 방식으로 **PSD 벡터 형태**를 수정해야 한다면, Aspose.PSD for Java 라이브러리를 통해 Java 코드에서 바로 Photoshop 파일을 완벽하게 제어할 수 있습니다. 이 튜토리얼에서는 벡터 형태 레이어를 편집하려 할 때 필수적인 단계인 length record data properties를 지원하는 방법을 모두 안내합니다. 튜토리얼을 마치면 PSD를 열어 벡터 형태 속성을 조정하고, IDE를 떠나지 않고도 업데이트된 파일을 저장할 수 있게 됩니다. 바로 시작해 보세요!

## 빠른 답변
- **“modify PSD vector shapes”는 무엇을 의미하나요?**  
  PSD 파일 내 벡터 기반 레이어의 기하학, 경로 연산 또는 기타 속성을 조정하는 것을 의미합니다.  
- **어떤 라이브러리가 이를 처리하나요?**  
  Aspose.PSD for Java.  
- **라이선스가 필요합니까?**  
  평가용으로는 무료 체험판을 사용할 수 있으며, 실제 운영 환경에서는 상용 라이선스가 필요합니다.  
- **구현에 얼마나 걸립니까?**  
  기본적인 형태 수정 스크립트의 경우 약 10‑15분 정도 소요됩니다.  
- **주요 전제 조건은 무엇인가요?**  
  Java JDK, Aspose.PSD for Java, 그리고 샘플 PSD 파일.

## “modify PSD vector shapes”란 무엇인가요?
PSD 벡터 형태를 수정한다는 것은 기본 벡터 경로 데이터(예: length records 및 path operations)를 변경하여 형태의 시각적 모습이 그에 맞게 업데이트되도록 하는 것을 말합니다. 이는 자동화된 그래픽 파이프라인, 배치 처리 또는 맞춤형 디자인 도구에 특히 유용합니다.

## 왜 Aspose.PSD for Java를 사용해 PSD 벡터 형태를 수정하나요?
- **No Photoshop required** – 서버 어디서든 PSD 파일을 직접 다룰 수 있습니다.  
- **Rich API** – 강력한 타입의 클래스를 통해 레이어, 리소스 및 벡터 데이터를 접근할 수 있습니다.  
- **Cross‑platform** – Windows, Linux, macOS 어느 환경에서든 JDK만 있으면 실행됩니다.  
- **Performance‑focused** – 메모리 관리가 효율적이며 저장 속도가 빠릅니다.

## 전제 조건
1. **Java Development Kit (JDK)** – [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드하거나 선호하는 패키지 관리자를 사용하세요.  
2. **Aspose.PSD for Java** – 최신 JAR 파일은 [Aspose releases page](https://releases.aspose.com/psd/java/)에서 얻을 수 있습니다.  
3. **IDE** – IntelliJ IDEA, Eclipse 또는 Java와 호환되는 편집기.  
4. **PSD 파일** – Photoshop에서 직접 만들거나 샘플 PSD를 사용해 실험하세요.  
5. **기본 Java 지식** – 클래스, 객체 및 예외 처리에 익숙해야 합니다.

## 패키지 가져오기
먼저 PSD 파일과 벡터 형태 리소스를 다루는 데 필요한 클래스를 가져옵니다.

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
`Image.load`를 사용해 파일을 열고, PSD‑전용 기능을 사용하려면 `PsdImage`로 캐스팅합니다.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 단계 3: 레이어에서 Vsms 리소스 찾기
벡터 형태 데이터는 `VsmsResource` 안에 들어 있습니다. 두 번째 레이어의 리소스를 순회하면서 해당 리소스를 찾습니다.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 단계 4: Length Records 접근
각 `LengthRecord`는 개별 벡터 경로를 나타냅니다. 수정하려는 레코드를 가져옵니다.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 단계 5: Path Operation 속성 수정
이제 `PathOperations`를 변경하여 **modify PSD vector shapes**를 수행할 수 있습니다. 이는 형태 간의 상호 작용(예: 제외, 교차, 차감)을 결정합니다.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 단계 6: 수정된 PSD 파일 저장
변경 내용을 새로운 파일에 저장합니다.

```java
psdImage.save(outPsdFilePath);
```

## 단계 7: 리소스 정리
메모리 해제를 위해 `PsdImage`를 Dispose합니다.

```java
psdImage.dispose();
```

## 일반적인 함정 및 팁
- **Null checks** – `resource`가 `null`이 아닌지 항상 확인한 뒤 경로에 접근하세요.  
- **Path index bounds** – 사용하려는 인덱스(`[2]`, `[7]`, `[11]`)가 현재 편집 중인 PSD에 존재하는지 확인하세요.  
- **License** – 유효한 라이선스 없이 실행하면 저장된 PSD에 워터마크가 삽입됩니다.  

## 결론
이제 Aspose.PSD for Java를 사용해 length record data properties를 지원하면서 **modify PSD vector shapes**를 수행하는 완전한 엔드‑투‑엔드 예제를 보유하게 되었습니다. 자산 파이프라인을 자동화하거나 맞춤형 디자인 도구를 구축하든, 이 API를 통해 수동 Photoshop 작업 없이도 벡터 레이어를 자유롭게 조작할 수 있습니다. 다른 `PathOperations`를 실험하거나 여러 `LengthRecord` 편집을 결합해 복잡한 형태를 만들어 보세요.

## 자주 묻는 질문

**Q: 벡터 형태 레이어가 전혀 없는 PSD를 어떻게 처리하나요?**  
A: `VsmsResource`가 없으므로 `resource`는 `null` 상태가 됩니다. 체크를 추가해 수정 단계를 건너뛰거나 사용자에게 알리세요.

**Q: 채우기 색상이나 스트로크 두께와 같은 다른 속성을 변경할 수 있나요?**  
A: 네, `LengthRecord`는 채우기, 스트로크, 불투명도 등을 설정할 수 있는 추가 메서드를 제공합니다. 자세한 내용은 API 문서를 참고하세요.

**Q: 여러 PSD 파일을 배치‑처리할 수 있나요?**  
A: 물론입니다. 코드를 루프 안에 넣어 디렉터리 내 PSD 파일들을 순회하면서 입력·출력 경로만 각각 조정하면 됩니다.

**Q: 파일 경로에서 로드할 때 스트림을 수동으로 닫아야 하나요?**  
A: `Image.load` 메서드는 파일 스트림을 내부적으로 처리하지만, `InputStream`으로 로드할 경우 사용 후 반드시 닫아야 합니다.

**Q: 이 API를 사용하려면 어떤 버전의 Aspose.PSD가 필요하나요?**  
A: `LengthRecord`와 `PathOperations` 클래스는 Aspose.PSD 20.10부터 제공됩니다. 최신 버전을 사용하는 것이 권장됩니다.

---

**마지막 업데이트:** 2025-12-17  
**테스트 환경:** Aspose.PSD for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
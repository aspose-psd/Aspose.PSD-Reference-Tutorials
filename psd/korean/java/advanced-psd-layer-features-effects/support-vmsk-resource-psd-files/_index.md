---
date: 2025-12-18
description: Aspose.PSD for Java를 사용하여 PSD 파일에서 벡터 마스크(Vmsk 리소스)를 만드는 방법을 배워보세요. 이
  단계별 튜토리얼에서는 벡터 마스크 추가, PSD를 PNG로 변환 등 다양한 방법을 보여줍니다.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Java를 사용하여 PSD 파일에서 벡터 마스크(Vmsk 리소스) 만들기
url: /ko/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java로 PSD 파일에서 벡터 마스크(Vmsk 리소스) 만들기

## 소개
Photoshop(PSD) 파일 내부에 ** 장치 마스크**(Vmsk)를 사용하여 **생성**해야 하는 경우, Java용 Aspose.PSD는 개인 프로그래밍 방식으로 이를 수행할 수 있는 방법을 제공합니다. 설계 자동화 도구를 구축하거나 기존 그래픽 파이프라인에 마스크 지원을 추가하려고 할 때 이 튜토리얼은 PSD 로드, Vmskler 그리기, 속성, 결과 저장까지 모든 단계를 안내합니다. 마치 면 벡터 마스크를 사용하는 사람, PSD를 PNG로 변환하며, 파일에 외부 벡터 데이터를 확장하는 작업에 사용할 수 있습니다.

## 빠른 답변
- **Vmsk 리소스란?** PSD 파일 내부에 저장된 벡터 마스크 데이터로, 레이어의 혼합 벡터 형태를 정의합니다.
- **어떤 라이브러리가 지원하는가?** Aspose.PSD for Java가 Vmsk 시리즈에 대한 완전한 읽기/쓰기 접속을 제공합니다.
- **라이선스를 사용하는 것이 필요합니까?** 무료 체험판을 사용할 수 있고, 허브 사용을 불러오기가 필요합니다.
- **편집한 PSD를 PNG로 변환할 수 있습니까?** 예—저장 후 PSD를 로드하고 동일한 API로 PNG 내로보낼 수 있습니다.
- **Maven 지원이 없나요?** 물론입니다; Aspose.PSD를 Maven 의존성으로 추가할 수 있습니다(“aspose psd maven” 키워드 참고).

## 벡터 마스크(Vmsk 리소스)란 무엇입니까?
벡터 마스크(Vmsk)는 베이스형이 아닌 마스크로, 베지어 외계인과 이동형 캐리어의 투명하고 범위를 명확하게 합니다. 벡터 기반이기 때문에 관계에 관계 없이 품질 감소 없이 확대·축소가 가능해 그래픽에 적합합니다.

## Aspose.PSD로 벡터 마스크를 만드는 이유는 무엇입니까?
- **자동화:** Photoshop을 열지하는 방식으로 마스크를 추가·수정할 수 있습니다.
- **일관성:** 모든 PSD가 동일한 마스크 규칙을 생성하는 것을 방지합니다.
- **크로스 플랫폼:** Java를 지원하는 모든 OS에서 동작합니다.
- **통합:** 또 다른 Aspose API(e.g., PSD→PNG 변환)와 참여해 투입‑투‑엔드코어 플로우를 공유할 수 있습니다.

## 전제 조건
코드 형태에 따라 항목을 준비하시기 바랍니다.

### 필요한 것
- Java Development Kit (JDK): 머신에 JDK가 설치되어 있는지 확인하세요. 설치하지 않으시면 [Oracle 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html)에서 다운로드하실 수 있습니다.
- Aspose.PSD for Java Library: PSD 파일 관리를 버퍼링합니다. [Aspose 출시 페이지](https://releases.aspose.com/psd/java/)에서 다운로드하세요. 전 체험을 통해 [무료 평가판](https://releases.aspose.com/)도 가능합니다.
- IDE: IntelliJ IDEA, Eclipse 등 Java IDE라면 어느 것이든 프로젝트에 사용할 수 있습니다.

### 작업 공간 설정
1. **새 Java 프로젝트 생성** – 선호하는 IDE를 대상으로 하는 새 프로젝트를 시작합니다.
2. **Aspose 라이브러리 추가** – Aspose JAR을 다운로드한 후 프로젝트 빌드에 추가하여 PSD 관련 클래스를 사용할 수 있습니다.

환경 설정이 실제로 구현되도록 하겠습니다.

## Java를 사용하여 PSD 파일에 벡터 마스크를 만드는 방법
아래는 단계별 가이드입니다. 코드 블록은 원본 튜토리얼과 동일하게 유지되며, 각 단계의 이해를 돕기 위해 설명을 추가했습니다.

## 패키지 가져오기
PSD 파일 작업에 필요한 Aspose.PSD 클래스들을 임포트합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

준비가 끝났으니 이제 각 작업을 차례대로 살펴보겠습니다.

## 1단계: PSD 파일 불러오기
먼저 PSD 파일을 로드합니다. 모든 작업의 시작점입니다.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir`을 PSD 파일이 위치한 디렉터리로 설정합니다.  
- `sourceFileName` 문자열을 디렉터리와 PSD 파일 이름을 결합해 생성합니다.  
- 마지막으로 `Image.load()`를 사용해 PSD 파일을 `PsdImage` 객체로 로드합니다.

## 2단계: Vmsk 리소스 가져오기
PSD 이미지가 로드되었으니 Vmsk 리소스를 가져옵니다.

```java
VmskResource resource = getVmskResource(im);
```

- 이미지에서 Vmsk 리소스를 검색·추출하는 `getVmskResource()` 메서드를 호출합니다.

## 3단계: Vmsk 리소스 속성 유효성 검사
수정에 앞서 Vmsk 리소스가 예상 상태인지 검증합니다.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Vmsk 리소스의 다양한 속성을 확인합니다. 비활성화, 반전, 연결 해제 상태가 아니며, 경로 수가 올바른지 확인합니다.

## 4단계: 각 경로에 접근하여 유효성을 검사합니다
Vmsk 리소스 내부의 경로들을 자세히 살펴보고 검증합니다.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- 특정 세 개의 경로 레코드를 추출하고, 타입 및 속성이 기준에 부합하는지 검증합니다.

## 5단계: Vmsk 리소스 편집
이제 Vmsk 리소스의 속성을 필요에 따라 수정합니다.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- 여러 속성을 `true` 로 토글하여 마스크가 PSD 파일에서 어떻게 동작할지 제어합니다.

## 6단계: 베지어 매듭점 수정
베지어 매듭은 벡터 경로의 핵심 요소입니다. 여기서 값을 변경해 보세요.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 특정 `BezierKnotRecord` 경로에 접근해 포인트를 변경함으로써 벡터 마스크 형태를 재구성합니다.

## 7단계: 수정된 PSD 파일 저장
모든 편집이 끝났으면 수정된 PSD 파일을 저장합니다.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- 내보낼 PSD 파일 경로를 지정하고 `im.save()`를 호출해 변경 내용을 새 파일에 기록합니다.

## 8단계: 자원 정리
작업이 끝난 뒤에는 리소스를 정리해 메모리 누수를 방지합니다.

```java
im.dispose();
```

- 사용이 끝난 리소스를 반드시 `dispose()` 하여 메모리를 해제합니다.

## 결론
축하합니다! Aspose.PSD for Java를 사용해 PSD 파일에 **벡터 마스크**(Vmsk) 리소스를 생성하고 편집하는 전체 과정을 마쳤습니다. 이미지 로드, Vmsk 리소스 조회·검증·수정, 수정된 PSD 저장까지의 흐름을 이해했으니 이제 디자인 파이프라인을 자동화하거나, 다른 Aspose API(e.g., PSD → PNG 변환)와 결합해 맞춤형 그래픽 툴을 구축할 수 있습니다.

## 자주 묻는 질문
**질문: 기존 레이어에 새 벡터 마스크를 어떻게 추가하나요?**
A: `VmskResource`를 생성하고 필요한 위치 기록(예: `BezierKnotRecord`)을 채운 뒤, 레이어의 컬렉션에 첨부합니다.

**Q: Photoshop을 열지 않고도 편집한 PSD를 PNG로 직접 변환할 수 있나요?**
A: 예—PSD를 저장한 후 `Image.load()`로 다시 로드하고 `im.save("output.png")`를 호출해 PNG 형식으로 내보낼 수 있습니다.

**Q: CI/CD 파이프라인에서 이를 자동화할 수 있는 방법이 있습니까?**
A: 물론입니다. 순수 Java 프로세스는 Maven/Gradle 빌드, Docker 컨테이너 또는 Java를 지원하는 모든 CI 시스템을 통합할 수 있습니다.

**Q: 어떤 버전의 Aspose.PSD가 Java 11+와 호환됩니까?**
A: 최신 릴리스(2024‑2025) 모두 Java 8 이상을 지원하며, Java 11, 17 및 최신 LTS 버전에서도 동작합니다.

**Q: 개발 빌드에는 라이선스가 필요합니까?**
A: 개발 및 테스트 단계에서는 무료로 평가할만 합니다. 배치에는 전원이 필요합니다.

---

**최종 업데이트:** 2025-12-18
**테스트 대상:** Java용 Aspose.PSD 24.11
**저자:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

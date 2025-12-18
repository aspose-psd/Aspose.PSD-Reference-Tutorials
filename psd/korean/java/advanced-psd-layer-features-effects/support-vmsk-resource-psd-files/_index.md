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

## Introduction
Photoshop(PSD) 파일 내부에 **벡터 마스크**(Vmsk) 리소스를 **생성**해야 할 경우, Aspose.PSD for Java는 깔끔하고 프로그래밍 방식으로 이를 수행할 수 있는 방법을 제공합니다. 디자인 자동화 도구를 구축하거나 기존 그래픽 파이프라인에 맞춤형 마스크 지원을 추가하고자 할 때, 이 튜토리얼은 PSD 로드, Vmsk 리소스 읽기, 속성 조정, 결과 저장까지 모든 단계를 안내합니다. 튜토리얼을 마치면 벡터 마스크를 다루고, PSD를 PNG로 변환하며, 파일에 추가적인 벡터 데이터를 확장하는 작업에 익숙해질 수 있습니다.

## Quick Answers
- **Vmsk 리소스란?** PSD 파일 내부에 저장된 벡터 마스크 데이터로, 레이어의 복잡한 벡터 형태를 정의합니다.  
- **어떤 라이브러리가 지원하나요?** Aspose.PSD for Java가 Vmsk 리소스에 대한 완전한 읽기/쓰기 접근을 제공합니다.  
- **라이선스가 필요합니까?** 무료 체험판을 사용할 수 있으며, 상용 사용을 위해서는 상업용 라이선스가 필요합니다.  
- **편집한 PSD를 PNG로 변환할 수 있나요?** 예—저장 후 PSD를 로드하고 동일한 API로 PNG로 내보낼 수 있습니다.  
- **Maven 지원이 있나요?** 물론입니다; Aspose.PSD를 Maven 의존성으로 추가할 수 있습니다(“aspose psd maven” 키워드 참고).

## What is a Vector Mask (Vmsk Resource)?
벡터 마스크(Vmsk)는 픽셀 기반이 아닌 마스크로, 베지어 곡선과 경로 레코드를 사용해 레이어의 투명 및 불투명 영역을 정의합니다. 벡터 기반이기 때문에 해상도에 관계없이 품질 손실 없이 확대·축소가 가능해 고해상도 그래픽에 적합합니다.

## Why Create a Vector Mask with Aspose.PSD?
- **Automation:** Photoshop을 열지 않고도 프로그래밍 방식으로 마스크를 추가·수정할 수 있습니다.  
- **Consistency:** 생성하는 모든 PSD가 동일한 마스크 규칙을 따르도록 보장합니다.  
- **Cross‑platform:** Java를 지원하는 모든 OS에서 동작합니다.  
- **Integration:** 다른 Aspose API(e.g., PSD → PNG 변환)와 결합해 엔드‑투‑엔드 워크플로우를 구현할 수 있습니다.

## Prerequisites
코드 구현에 앞서 아래 항목들을 준비해 주세요.

### What You Need
- Java Development Kit (JDK): 머신에 JDK가 설치되어 있는지 확인하세요. 설치되지 않았다면 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html)에서 다운로드할 수 있습니다.  
- Aspose.PSD for Java Library: PSD 파일 관리를 위한 강력한 라이브러리입니다. [Aspose release page](https://releases.aspose.com/psd/java/)에서 다운로드하세요. 구매 전 체험을 원한다면 [free trial](https://releases.aspose.com/)도 가능합니다.  
- An IDE: IntelliJ IDEA, Eclipse 등 Java IDE라면 어느 것이든 프로젝트에 사용할 수 있습니다.

### Setting Up Your Workspace
1. **Create a New Java Project** – 선호하는 IDE를 열고 새 프로젝트를 시작합니다.  
2. **Add the Aspose Library** – Aspose JAR를 다운로드한 뒤 프로젝트 빌드 경로에 추가하여 PSD 관련 클래스를 사용할 수 있게 합니다.

환경 설정이 완료되면 실제 구현으로 넘어갑니다.

## How to create vector mask in PSD files with Java
아래는 단계별 가이드입니다. 코드 블록은 원본 튜토리얼과 동일하게 유지되며, 각 단계의 이해를 돕기 위해 설명을 추가했습니다.

## Import Packages
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

## Step 1: Load Your PSD File
먼저 PSD 파일을 로드합니다. 모든 작업의 시작점입니다.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir`을 PSD 파일이 위치한 디렉터리로 설정합니다.  
- `sourceFileName` 문자열을 디렉터리와 PSD 파일 이름을 결합해 생성합니다.  
- 마지막으로 `Image.load()`를 사용해 PSD 파일을 `PsdImage` 객체로 로드합니다.

## Step 2: Retrieve the Vmsk Resource
PSD 이미지가 로드되었으니 Vmsk 리소스를 가져옵니다.

```java
VmskResource resource = getVmskResource(im);
```

- 이미지에서 Vmsk 리소스를 검색·추출하는 `getVmskResource()` 메서드를 호출합니다.

## Step 3: Validate Vmsk Resource Properties
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

## Step 4: Access Each Path and Validate
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

## Step 5: Edit the Vmsk Resource
이제 Vmsk 리소스의 속성을 필요에 따라 수정합니다.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- 여러 속성을 `true` 로 토글하여 마스크가 PSD 파일에서 어떻게 동작할지 제어합니다.

## Step 6: Modify the Bezier Knot Points
베지어 매듭은 벡터 경로의 핵심 요소입니다. 여기서 값을 변경해 보세요.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 특정 `BezierKnotRecord` 경로에 접근해 포인트를 변경함으로써 벡터 마스크 형태를 재구성합니다.

## Step 7: Save the Modified PSD File
모든 편집이 끝났으면 수정된 PSD 파일을 저장합니다.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- 내보낼 PSD 파일 경로를 지정하고 `im.save()`를 호출해 변경 내용을 새 파일에 기록합니다.

## Step 8: Clean Up Resources
작업이 끝난 뒤에는 리소스를 정리해 메모리 누수를 방지합니다.

```java
im.dispose();
```

- 사용이 끝난 리소스를 반드시 `dispose()` 하여 메모리를 해제합니다.

## Conclusion
축하합니다! Aspose.PSD for Java를 사용해 PSD 파일에 **벡터 마스크**(Vmsk) 리소스를 생성하고 편집하는 전체 과정을 마쳤습니다. 이미지 로드, Vmsk 리소스 조회·검증·수정, 수정된 PSD 저장까지의 흐름을 이해했으니 이제 디자인 파이프라인을 자동화하거나, 다른 Aspose API(e.g., PSD → PNG 변환)와 결합해 맞춤형 그래픽 툴을 구축할 수 있습니다.

## FAQ's
### What is a Vmsk resource?
Vmsk 리소스는 PSD 파일 내에 포함된 벡터 마스크로, 복잡한 벡터 형태와 편집 기능을 제공합니다.

### Can I use Aspose.PSD in a Maven project?
예, Aspose.PSD를 Maven 의존성으로 추가하여 프로젝트에 사용할 수 있습니다.

### What format can I save my modified PSD files in?
수정된 파일을 PSD 형식으로 다시 저장하거나 PNG, JPEG 등 다른 포맷으로 내보낼 수 있습니다.

### Is there a free trial available for Aspose.PSD?
예, Aspose.PSD의 무료 체험판을 이용해 기능을 테스트할 수 있습니다. 자세한 내용은 [free trial link](https://releases.aspose.com/)를 참고하세요.

### How can I get support for Aspose.PSD?
지원 및 문제 해결을 위해 [Aspose forum](https://forum.aspose.com/c/psd/34)에서 도움을 받을 수 있습니다.

## Frequently Asked Questions
**Q: How do I add a new vector mask to an existing layer?**  
A: `VmskResource`를 생성하고 필요한 경로 레코드(e.g., `BezierKnotRecord`)를 채운 뒤, 레이어의 리소스 컬렉션에 첨부합니다.

**Q: Can I convert the edited PSD directly to PNG without opening Photoshop?**  
A: 예—PSD를 저장한 뒤 `Image.load()`로 다시 로드하고 `im.save("output.png")`를 호출해 PNG 형식으로 내보낼 수 있습니다.

**Q: Is there a way to automate this in a CI/CD pipeline?**  
A: 물론입니다. 순수 Java 프로세스이므로 Maven/Gradle 빌드, Docker 컨테이너, 혹은 Java를 지원하는 모든 CI 시스템에 통합할 수 있습니다.

**Q: What versions of Aspose.PSD are compatible with Java 11+?**  
A: 최신 릴리스(2024‑2025) 모두 Java 8 이상을 지원하며, Java 11, 17 및 최신 LTS 버전에서도 동작합니다.

**Q: Do I need a license for development builds?**  
A: 개발 및 테스트 단계에서는 무료 평가 라이선스로 충분합니다. 프로덕션 배포 시에는 상업용 라이선스가 필요합니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose
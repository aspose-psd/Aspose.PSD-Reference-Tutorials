---
title: Java를 사용하여 PSD 파일에서 Vmsk 리소스 지원
linktitle: Java를 사용하여 PSD 파일에서 Vmsk 리소스 지원
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일의 Vmsk 리소스를 손쉽게 관리하세요. 개발자와 디자이너 모두에게 이상적인 포괄적인 단계별 튜토리얼입니다.
weight: 23
url: /ko/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 PSD 파일에서 Vmsk 리소스 지원

## 소개
PSD(Photoshop 문서) 파일 작업 시 리소스 관리는 매우 중요하며, 특히 Vmsk(벡터 마스크) 리소스와 같은 특수 기능을 통합할 때는 더욱 그렇습니다. Vmsk 리소스는 복잡한 벡터 모양을 추가하여 디자이너가 손쉽게 멋진 그래픽을 만들 수 있도록 지원합니다. 이 가이드에서는 Java용 Aspose.PSD를 사용하여 PSD 파일에서 Vmsk 리소스를 지원하는 방법을 보여주기 위해 실무적인 접근 방식을 취하겠습니다. 애플리케이션을 향상시키려는 개발자이거나 자동화를 원하는 디자이너라면 이 튜토리얼에서는 프로세스를 단계별로 안내하여 쉽게 따라하고 구현할 수 있습니다.
## 전제조건
Vmsk 리소스 처리에 대한 자세한 내용을 살펴보기 전에 원활한 경험을 위한 모든 것이 준비되어 있는지 확인하겠습니다.
### 당신에게 필요한 것
-  JDK(Java Development Kit): 컴퓨터에 JDK가 설치되어 있는지 확인하세요. 그렇지 않은 경우 다음에서 다운로드할 수 있습니다.[오라클 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD for Java Library: PSD 파일 관리를 위한 강력한 라이브러리입니다. 다음에서 다운로드할 수 있습니다.[Aspose 릴리스 페이지](https://releases.aspose.com/psd/java/) . 구매하기 전에 시험해 보고 싶은 분들은[무료 평가판](https://releases.aspose.com/).
- IDE: 모든 Java용 IDE(예: IntelliJ IDEA, Eclipse 등)가 이 프로젝트에 작동합니다.
### 작업 공간 설정
1. 새 Java 프로젝트 만들기: 선호하는 IDE를 시작하고 새 Java 프로젝트를 만듭니다. 이것은 코드 작업을 위한 놀이터입니다.
2. Aspose 라이브러리 추가: Aspose 라이브러리를 다운로드한 후 프로젝트 라이브러리에 jar 파일을 추가합니다. 이 단계는 Aspose.PSD의 모든 유용한 기능을 활용할 수 있게 해주기 때문에 매우 중요합니다.
이러한 필수 구성 요소가 준비되면 Vmsk 리소스를 사용하여 PSD 파일 생성, 수정 및 관리를 시작할 수 있습니다. 프로그래밍에 바로 들어가자!
## 패키지 가져오기
PSD 파일 작업을 시작하기 전에 필요한 패키지를 가져와야 합니다. 이는 Aspose.PSD 라이브러리가 제공하는 다양한 클래스와 메서드에 대한 액세스를 제공하는 코드의 백본입니다.
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
이제 무대를 마련했으므로 행동할 시간입니다! 이 섹션에서는 코드를 관리 가능한 단계로 나누어 보겠습니다. 이 단계에서는 PSD 파일을 읽고, Vmsk 리소스를 처리하고, 편집하는 과정을 안내합니다.
## 1단계: PSD 파일 로드
가장 먼저 하고 싶은 일은 PSD 파일을 로드하는 것입니다. 모든 마법이 시작되는 곳입니다.
```java
String dataDir = "Your Document Directory"; // 이 경로 업데이트
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  우리는`dataDir` PSD 파일 디렉터리로 이동합니다. 
-  우리는`sourceFileName`, 디렉토리를 PSD 파일 이름과 결합합니다.
-  마지막으로 PSD 파일을`PsdImage` 객체를 사용하여`Image.load()`.
## 2단계: Vmsk 리소스 검색
이제 PSD 이미지가 로드되었으므로 Vmsk 리소스를 가져오겠습니다.
```java
VmskResource resource = getVmskResource(im);
```

-  우리는`getVmskResource()` 이미지에서 Vmsk 리소스 검색 및 검색을 처리하는 메서드입니다.
## 3단계: Vmsk 리소스 속성 유효성 검사
수정을 진행하기 전에 Vmsk 리소스가 예상된 상태인지 확인하는 것이 중요합니다.
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- 여기서는 Vmsk 리소스의 다양한 속성을 확인합니다. 우리는 그것이 비활성화되거나 반전되거나 연결되지 않았는지 확인하고 올바른 수의 경로가 있는지 확인하고 싶습니다.
## 4단계: 각 경로에 액세스하고 유효성을 검사합니다.
좀 더 자세히 살펴보고 Vmsk 리소스 내의 경로를 살펴보겠습니다.
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

- 우리는 세 가지 특정 경로 레코드를 추출하고 해당 유형과 속성의 유효성을 검사하여 기준을 충족하는지 확인하고 있습니다.
## 5단계: Vmsk 리소스 편집
이제 우리는 수정 부분에 들어갑니다! 필요에 따라 Vmsk 리소스의 속성을 조정할 수 있습니다.
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- 이 블록에서는 Vmsk 리소스의 다양한 속성을 전환합니다. 이를 true로 설정하면 PSD 파일에서 마스크가 작동하는 방식을 제어할 수 있습니다.
## 6단계: 베지어 매듭 포인트 수정
베지어 매듭은 벡터 경로에 매우 중요합니다. 여기서 몇 가지 값을 변경해 보겠습니다.
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  우리는 특정 항목에 액세스하고 있습니다`BezierKnotRecord` 경로를 변경하고 점을 변경하여 잠재적으로 벡터 마스크의 모양을 변경할 수 있습니다.
## 7단계: 수정된 PSD 파일 저장
모든 편집이 완료되면 수정된 PSD 파일을 저장할 차례입니다. 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  내보낸 PSD 파일의 경로를 설정한 다음 호출합니다.`im.save()` 이 새 파일에 변경 사항을 기록합니다.
## 8단계: 리소스 정리
마지막으로, 리소스를 확보하기 위해 이미지를 적절하게 폐기해야 합니다.
```java
im.dispose();
```

- 작업이 끝나면 항상 리소스를 폐기하는 것이 좋습니다. 이는 애플리케이션에서 메모리 누수를 방지하는 데 도움이 됩니다.
## 결론
축하해요! Java용 Aspose.PSD를 사용하여 PSD 파일에서 Vmsk 리소스를 지원하는 자세한 프로세스를 진행했습니다. 이미지 로드, Vmsk 리소스 검색 및 유효성 검사, 해당 속성 편집, 수정된 PSD 저장 등 필수 사항을 다뤘습니다. 이러한 기술을 사용하면 PSD 파일 내의 다양한 리소스를 효율적으로 관리하고 활용하여 그래픽 디자인 프로젝트 또는 자동화 스크립트를 향상시킬 수 있습니다.
## FAQ
### Vmsk 리소스란 무엇입니까?
Vmsk 리소스는 복잡한 벡터 모양과 편집 기능을 허용하는 PSD 파일의 벡터 마스크입니다.
### Maven 프로젝트에서 Aspose.PSD를 사용할 수 있나요?
예, 저장소의 좌표를 사용하여 Aspose.PSD를 Maven 프로젝트의 종속성으로 포함할 수 있습니다.
### 수정된 PSD 파일을 어떤 형식으로 저장할 수 있나요?
PSD 파일로 다시 저장하거나 PNG, JPEG 등과 같은 다른 형식으로 내보낼 수 있습니다.
### Aspose.PSD에 대한 무료 평가판이 있습니까?
 예, Aspose.PSD 무료 평가판에 액세스하여 기능을 테스트할 수 있습니다. 방문[무료 평가판 링크](https://releases.aspose.com/).
### Aspose.PSD에 대한 지원은 어떻게 받을 수 있나요?
 당신은[포럼을 Aspose](https://forum.aspose.com/c/psd/34)지원 및 문제 해결 도움을 받으려면
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

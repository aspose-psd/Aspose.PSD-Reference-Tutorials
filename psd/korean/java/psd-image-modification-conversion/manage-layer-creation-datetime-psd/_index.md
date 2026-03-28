---
date: 2026-03-28
description: Aspose.PSD for Java를 사용하여 새로운 PSD 레이어를 생성하고 생성 날짜·시간을 관리하는 방법을 배웁니다.
  이 단계별 가이드는 레이어 로드, 읽기, 검증 및 추가에 대해 다룹니다.
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: Java에서 새 PSD 레이어 만들기 및 생성 날짜/시간 관리
url: /ko/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 새 PSD 레이어 생성 및 생성 날짜/시간 관리

## 소개
프로그램으로 Photoshop (PSD) 파일을 다룰 때, **create new PSD layer** 객체를 생성하고 그 생성 타임스탬프를 추적할 수 있다면 큰 변화를 가져옵니다. 디자인 자산에 대한 버전 관리 시스템을 구축하거나, 배치 편집을 자동화하거나, 협업 프로젝트에 대한 감사 로그가 필요하든, 레이어 생성 날짜를 읽고 설정하는 방법을 알면 모든 변경 사항의 전체 출처를 유지할 수 있습니다. 이 튜토리얼에서는 Aspose.PSD for Java를 사용하여 PSD를 로드하고, 레이어의 생성 날짜를 가져오고, 이를 검증한 뒤, 새 조정 레이어를 추가하는 전체 과정을 단계별로 살펴보겠습니다.

## 빠른 답변
- **Java에서 PSD 파일을 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java  
- **레이어의 생성 날짜를 읽을 수 있나요?** Yes, using `layer.getLayerCreationDateTime()`  
- **새 조정 레이어를 추가할 수 있나요?** Absolutely – `im.addLevelsAdjustmentLayer()` creates one  
- **프로덕션 사용을 위해 라이선스가 필요합니까?** A commercial license is required for non‑trial deployments  
- **지원되는 Java 버전은 무엇인가요?** JDK 8 or later  

## “create new PSD layer”란 무엇인가요?
새 PSD 레이어를 생성한다는 것은 프로그램적으로 새로운 레이어 객체(조정 레이어, 텍스트 레이어 또는 픽셀 레이어 등)를 기존 PSD 문서에 삽입하는 것을 의미합니다. 이 작업을 통해 Photoshop을 직접 열지 않고도 이미지에 레이어를 추가하거나 수정할 수 있습니다.

## 왜 레이어 생성 DateTime을 관리해야 할까요?
각 레이어의 생성 DateTime을 추적하면 다음에 도움이 됩니다:
- **수정 내역 감사** – 레이어가 정확히 언제 추가되었는지 알 수 있습니다.  
- **자산 동기화** – 타임스탬프를 비교하여 팀 간에 자산을 동기화합니다.  
- **워크플로 자동화** – 시간 기반 규칙에 따라 (예: 한 달 이상 된 레이어 숨기기) 워크플로를 자동화합니다.  

## 전제 조건
시작하기 전에 다음 항목이 준비되어 있는지 확인하세요:

1. **Java Development Kit (JDK)** – 버전 8 이상.  
2. **IDE** – IntelliJ IDEA, Eclipse, NetBeans 또는 원하는 편집기.  
3. **Aspose.PSD for Java** – 설치를 위해 [여기에서 다운로드](https://releases.aspose.com/psd/java/) 할 수 있습니다.  
4. **Basic Java knowledge** – Java가 처음이라도 걱정하지 마세요; 코드는 충분히 주석이 달려 있습니다.  

모든 준비가 되었나요? 멋집니다! 이제 코딩의 재미있는 부분으로 들어갑시다.

## 패키지 가져오기
먼저, 필요한 Aspose.PSD 클래스와 Java 유틸리티를 가져옵니다. 이러한 import는 이미지 처리, 레이어 조작 및 날짜 형식 지정에 접근할 수 있게 해줍니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## 1단계: 문서 디렉터리 설정
작업하려는 PSD가 들어 있는 폴더를 지정합니다. 자리표시자를 머신의 절대 경로로 교체하세요.

```java
String dataDir = "Your Document Directory";
```

## 2단계: PSD 파일 로드
`PsdImage` 인스턴스를 대상 파일을 로드하여 생성합니다. 이 객체는 모든 레이어 작업의 진입점입니다.

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## 3단계: 레이어와 그 생성 날짜에 접근
첫 번째 레이어(index 0)를 가져와 그 생성 타임스탬프를 조회합니다. 이 날짜는 이후에 비교하거나 로그에 기록할 날짜입니다.

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## 4단계: 생성 날짜 포맷 지정
원시 `Date` 객체를 사람이 읽을 수 있는 문자열로 변환합니다. 다른 형식을 원한다면 패턴을 조정하세요.

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## 5단계: 생성 날짜 검증
데모를 위해, 조회한 날짜를 예상 값과 비교합니다. 실제 프로젝트에서는 데이터베이스 레코드나 설정 파일과 비교할 수 있습니다.

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## 6단계: 새 레이어 생성
이제 실제로 **create new PSD layer** 객체를 생성합니다. 여기서는 Levels 조정 레이어를 추가하는데, 원본 픽셀을 변경하지 않고 톤 범위를 조정할 수 있습니다.

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **팁:** The `now` variable captures the moment you add the layer, which you can later store as metadata if you need a custom timestamp.

## 일반적인 문제와 해결책
| 문제 | 발생 원인 | 해결 방법 |
|-------|----------------|-----|
| `NullPointerException` on `layer.getLayerCreationDateTime()` | PSD에 레이어가 없거나 레이어 인덱스가 범위를 벗어났습니다. | `im.getLayers().length > 0`인지 확인한 후 접근하세요. |
| 검증 시 날짜 불일치 | `Date` 생성자가 문자열을 로케일에 따라 파싱합니다. | 신뢰할 수 있는 파싱을 위해 `SimpleDateFormat.parse("2018/07/17 08:57:24")`를 사용하세요. |
| 새 레이어가 Photoshop에 보이지 않음 | 조정 레이어가 기본적으로 숨겨져 있을 수 있습니다. | 생성 후 `createdLayer.setVisible(true);`를 호출하세요. |

## 결론
이제 **create new PSD layer** 객체를 생성하고, 생성 타임스탬프를 읽으며, 해당 타임스탬프를 검증하고, 조정 레이어를 추가하는 방법을 알게 되었습니다—모두 Aspose.PSD for Java를 사용합니다. 이 기능을 통해 Java 기반 이미지 처리 파이프라인에서 정교한 자동화, 감사 로그 및 협업 워크플로를 구현할 수 있습니다.

이 튜토리얼이 도움이 되었다면, 레이어 병합, 필터 적용, 다양한 포맷으로 내보내기 등 다른 Aspose.PSD 기능을 살펴보세요. 가능성은 무한합니다!

## FAQ
### Aspose.PSD란?
Aspose.PSD는 프로그램으로 Photoshop (PSD) 파일을 다루기 위한 강력한 라이브러리입니다.

### Aspose.PSD를 무료로 사용할 수 있나요?
예! 무료 체험을 [여기](https://releases.aspose.com/)에서 시작할 수 있습니다.

### 장기 사용을 위해 라이선스를 구매해야 하나요?
예, 준비가 되면 [여기](https://purchase.aspose.com/buy)에서 라이선스를 구매할 수 있습니다.

### Aspose.PSD에 대한 자세한 정보를 어디서 찾을 수 있나요?
자세한 가이드와 API 레퍼런스는 [문서](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

### Aspose.PSD 사용 중 문제가 발생하면 어떻게 지원을 받을 수 있나요?
커뮤니티 지원을 위해 [지원 포럼](https://forum.aspose.com/c/psd/34)을 방문해 보세요.

---

**마지막 업데이트:** 2026-03-28  
**테스트 환경:** Aspose.PSD for Java 24.10  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
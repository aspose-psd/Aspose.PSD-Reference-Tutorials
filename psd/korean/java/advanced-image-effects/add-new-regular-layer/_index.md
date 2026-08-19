---
date: 2026-04-08
description: Aspose.PSD for Java와 Aspose 임시 라이선스를 사용하여 PSD를 PNG로 내보내고 새로운 PSD 레이어를
  만드는 방법을 배웁니다. 이 단계별 튜토리얼은 PSD 이미지 조작 및 레이어 위치 설정을 다룹니다.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: PSD에 새 일반 레이어 추가
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 새 일반 레이어 추가 – Aspose 임시 라이선스
url: /ko/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 새 일반 레이어 추가

## 소개

이 **aspose psd tutorial**에서는 **export PSD to PNG**와 동시에 동일 파일 내에 **new regular layer**를 **aspose temporary license**를 사용하여 만드는 방법을 알아봅니다. 웹 준비 썸네일을 생성하거나 디자인 파이프라인을 위한 에셋을 준비하거나 단순히 **psd image manipulation**을 실험하고자 할 때, Aspose.PSD for Java는 완전한 프로그래밍 제어를 제공합니다. 소스 파일을 로드하는 단계부터 업데이트된 PSD와 PNG 복사본을 저장하는 단계까지 모든 과정을 단계별로 안내하므로 바로 PSD 레이어를 조작할 수 있습니다.

## 빠른 답변
- **한 번의 호출로 PSD를 PNG로 내보낼 수 있나요?** Yes, after adding layers you can call `save` with `PngOptions`.
- **개발에 라이선스가 필요합니까?** A temporary license works for testing; a full license is required for production.
- **지원되는 Java 버전은 무엇입니까?** Aspose.PSD works with Java 8 and newer.
- **레이어 위치 지정이 픽셀 기반인가요?** Yes, you set left, top, right, bottom coordinates in pixels using the **set layer position** methods.
- **PNG가 레이어 투명성을 유지합니까?** The PNG will contain the merged result of all visible layers.

## 왜 aspose 임시 라이선스를 사용해야 하나요?

**aspose temporary license**를 사용하면 기능 제한 없이 Aspose.PSD의 전체 기능을 평가할 수 있습니다. 평가 워터마크가 제거되고 모든 API가 잠금 해제되며, **create new psd layer** 객체를 만들 수 있는 기능도 포함됩니다. 영구 라이선스를 구매하기 전에 프로덕션과 유사한 환경에서 코드를 테스트할 수 있습니다.

## 전제 조건

- **Java Development Environment** – JDK 8+ 및 빌드 도구(Maven/Gradle)가 설치되어 있어야 합니다.
- **Aspose.PSD for Java** – 공식 사이트에서 최신 JAR를 [here](https://releases.aspose.com/psd/java/)에서 다운로드하십시오.
- **A sample PSD file** – 예제에서는 `OneLayer.psd`를 사용합니다.

## 패키지 가져오기

Java 클래스에 필요한 import를 추가하십시오. 이러한 클래스들은 **psd image manipulation** 및 레이어 처리를 위한 핵심 기능을 제공합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## “set layer position”이란 무엇이며 왜 중요한가요?

새 레이어를 추가할 때 캔버스에서 해당 레이어가 나타날 위치를 정의해야 합니다. `setLeft`, `setTop`, `setRight`, `setBottom` 메서드는 픽셀 좌표로 **set layer position**을 설정합니다. 정확한 위치 지정은 그래픽이 기대한 대로 정확히 정렬되도록 보장하며, UI 에셋 합성이나 인쇄용 파일 준비와 같은 작업에 필수적입니다.

## 단계별 가이드

### 1단계: PSD 파일 로드

먼저 수정하려는 기존 PSD를 로드합니다. 이렇게 하면 작업할 수 있는 `PsdImage` 객체가 생성됩니다.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### 2단계: 픽셀 데이터 및 사각형 준비

두 개의 픽셀 버퍼(`int[]`)를 만들고 새 레이어가 그려질 사각형 영역을 정의합니다. 이는 **creating a new psd layer**의 기반이 됩니다.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### 3단계: 레이어 데이터 초기화

픽셀 버퍼를 기본 ARGB 값으로 채웁니다. 값 `-10000000`은 반투명 어두운 색조에 해당합니다.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### 4단계: 일반 레이어 추가 (Manipulate PSD Layers)

이제 PSD 이미지에 **add regular layers**를 추가하고 left, top, right, bottom 속성을 사용하여 **set layer position**을 설정합니다. 이는 프로그램matically **manipulate PSD layers**하는 방법을 보여줍니다.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### 5단계: PSD를 PNG로 내보내고 업데이트된 PSD 저장

레이어가 배치된 후 수정된 문서를 저장합니다. 먼저 결과를 PNG로 내보내고(**export psd to png** 단계), 그 다음 새 레이어가 포함된 PSD를 저장합니다.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** PNG만 필요하면 PSD `save` 호출을 건너뛰고 `PngOptions`와 함께 `save`를 직접 호출하면 됩니다.

## 일반적인 문제 및 해결 방법

| 증상 | 가능한 원인 | 해결 방법 |
|---------|--------------|-----|
| PNG가 비어 있음 | 레이어가 보이지 않거나 완전히 투명함 | 비투명 픽셀 값을 설정하거나 `layer.setVisible(true)`를 호출했는지 확인하십시오. |
| `ArrayIndexOutOfBoundsException` | 사각형 크기와 픽셀 배열 길이가 일치하지 않음 | `rect.width * rect.height == dataArray.length`인지 확인하십시오. |
| 런타임 시 LicenseException | 유효한 라이선스가 로드되지 않음 | API 메서드를 호출하기 전에 임시 또는 영구 라이선스를 로드하십시오. |

## 자주 묻는 질문

**Q: Aspose.PSD가 Java 8과 호환되나요?**  
A: 예, Aspose.PSD는 Java 8 및 이후 버전을 지원합니다.

**Q: 추가된 레이어에 변환(회전, 스케일)을 적용할 수 있나요?**  
A: 물론입니다! `Layer` 클래스는 `rotate`, `scale`, `translate`와 같은 메서드를 제공하여 전체 변환을 제어합니다.

**Q: 추가 Aspose.PSD 문서는 어디에서 찾을 수 있나요?**  
A: 자세한 API 문서는 [here](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

**Q: Aspose.PSD 임시 라이선스를 어떻게 얻을 수 있나요?**  
A: 임시 라이선스 페이지를 [here](https://purchase.aspose.com/temporary-license/)에서 방문하십시오.

**Q: Aspose.PSD 지원을 위한 커뮤니티 포럼이 있나요?**  
A: 예, Aspose 포럼에서 토론에 참여하십시오 [here](https://forum.aspose.com/c/psd/34).

## 결론

이제 Aspose.PSD for Java를 사용하여 **export PSD to PNG**와 **add new regular layers**를 수행하는 방법을 배웠으며, **aspose temporary license**가 제한 없이 이 워크플로를 시험할 수 있게 해줌을 확인했습니다. 이 튜토리얼은 핵심 **psd image manipulation** 기능을 보여줍니다: 파일 로드, 레이어 생성, 픽셀 데이터 채우기, 최종 합성물 내보내기. 다양한 사각형 크기, 픽셀 색상 또는 레이어 효과를 실험하여 프로젝트 요구에 맞게 출력물을 조정해 보세요.

---

**마지막 업데이트:** 2026-04-08  
**테스트 환경:** Aspose.PSD 24.11 for Java  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
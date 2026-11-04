---
date: 2026-11-04
description: Aspose.PSD for Java를 사용하여 invert adjustment layer를 적용하고, PSD 이미지를 배치
  처리하며, 네거티브 이미지 PSD 파일을 만드는 방법을 배웁니다.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Aspose.PSD for Java를 사용하여 invert adjustment layer를 추가하고, PSD 이미지를
  배치 처리하며, 네거티브 이미지 PSD를 만드는 방법을 안내합니다. 단계별 가이드를 따라 주세요.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Java에서 Aspose.PSD를 사용하여 invert adjustment layer를 추가하는 방법
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Java에서 Aspose.PSD를 사용하여 invert adjustment layer를 추가하는 방법
url: /ko/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD를 사용하여 Java에서 반전 조정 레이어를 추가하는 방법

## 소개

만약 강력한 **image processing java library**를 찾고 있다면, Aspose.PSD for Java는 시장에서 가장 다재다능한 옵션 중 하나입니다. 이 튜토리얼에서는 **Aspose 사용 방법**을 보여드리며, PSD 파일에 **Invert Adjustment Layer**를 삽입하고, 다른 조정 레이어와 스택하며, 수십 개의 파일에 걸쳐 작업을 실행하는 방법을 다룹니다. 배치 처리 도구, 서버 측 이미지 서비스, 혹은 단일 이미지 편집기를 구축하든, 아래 단계들을 따라 하면 소스 PSD를 몇 분 안에 완전히 편집 가능한 네거티브 이미지로 변환할 수 있습니다.

## 빠른 답변
- **Invert Adjustment Layer는 무엇을 하나요?** 선택 영역의 모든 RGB 값을 뒤집어 이미지를 사진 네거티브로 변환합니다.  
- **어떤 라이브러리가 이 기능을 제공하나요?** Aspose.PSD, 선도적인 **image processing java library**입니다.  
- **다른 조정과 함께 스택할 수 있나요?** 예 – 밝기/대비, 색조/채도 등과 같은 **여러 조정 레이어를 적용**할 수 있습니다.  
- **개발에 라이선스가 필요합니까?** 무료 체험판을 사용할 수 있으며, 프로덕션 사용에는 라이선스가 필요합니다.  
- **구현에 얼마나 걸립니까?** 기본 사용 사례의 경우 일반적으로 10분 이내입니다.

## Invert Adjustment Layer란 무엇인가요?

Invert Adjustment Layer는 영향을 받는 모든 픽셀의 색상 값을 반전시키는 비파괴 편집입니다. 레이어 스택의 최상위에 위치하기 때문에 원본 이미지 데이터를 영구적으로 변경하지 않고도 가시성을 전환하거나 순서를 재배열할 수 있습니다. 이는 **negative image PSD** 파일을 만들거나 클래식 필름 네거티브 효과를 얻는 가장 빠른 방법입니다.

## 왜 Aspose.PSD를 이미지 처리 java 라이브러리로 사용하나요?

Aspose.PSD는 **200개 이상의 PSD 기능**을 지원하며, 포토샵 없이도 Photoshop 파일을 읽고 쓸 수 있고, 500 MB 미만의 힙 메모리로 수백 페이지 문서를 처리합니다. Java 런타임(Java 6 이상)에서 실행되므로 Windows, Linux, macOS 서버에서 **batch process psd images**에 이상적입니다.

## 전제 조건

시작하기 전에 다음을 확인하십시오:

1. **Aspose.PSD for Java** – 공식 사이트에서 최신 JAR을 다운로드하십시오 [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 이상이 설치되어 `PATH`에 설정되어 있어야 합니다.  

## 패키지 가져오기

`PsdImage` 클래스는 메모리 내 전체 Photoshop 문서를 나타내며, 조정 레이어 클래스는 `com.aspose.psd.layers.adjustments` 패키지에 있습니다.

`PsdImage` 클래스는 PSD 파일의 구조와 픽셀 데이터를 캡슐화하는 Aspose.PSD의 최상위 객체입니다. 네임스페이스를 가져오면 PSD 파일을 로드, 편집 및 저장할 수 있습니다.

## Step 1: 문서 디렉터리 설정

소스 PSD 파일이 있는 폴더와 출력이 저장될 폴더를 정의합니다. 절대 경로를 사용하면 작업 디렉터리가 변경될 때 발생할 수 있는 `NullPointerException`을 방지할 수 있습니다.

## Step 2: PSD 파일 로드

소스 파일을 `PsdImage` 객체에 로드합니다. 이 객체는 메모리 내 전체 레이어 계층 구조를 보유하여 비파괴 편집을 가능하게 합니다.

`PsdImage` 클래스는 파일 헤더를 읽고 형식을 검증한 뒤, 조작 준비가 된 메모리 내 표현을 생성하는 정적 `load` 메서드를 제공합니다.

## Step 3: 반전 조정 레이어 추가

내장 메서드를 호출하여 현재 레이어 스택 최상단에 Invert Adjustment Layer를 삽입합니다. 이후에 더 많은 레이어(예: 밝기, 색조)를 추가하여 **여러 조정 레이어를 적용**할 수 있습니다.

`addInvertAdjustmentLayer()`는 PSD의 레이어 컬렉션에 Invert Adjustment Layer를 추가합니다.

## Step 4: 출력 저장

수정된 PSD를 디스크에 저장합니다.  

`save()`는 모든 레이어와 메타데이터를 포함한 PSD 파일을 지정된 경로에 씁니다.

저장은 모든 조정 레이어, 마스크 및 메타데이터를 포함한 전체 문서를 지정된 형식으로 쓰는 동일한 `save` 메서드를 사용합니다.

### 무슨 일이 일어났나요?

PSD 파일이 `PsdImage` 객체에 로드되고, `InvertAdjustmentLayer`가 최상위 레이어로 생성 및 추가된 후 문서가 저장되었습니다. 이 순서는 원본 이미지 데이터를 보존하면서 나중에 토글하거나 순서를 바꿀 수 있는 비파괴적인 반전 효과를 추가합니다.

이제 **image processing java library**인 Aspose.PSD를 사용하여 PSD 파일을 성공적으로 조작했습니다.

## 반전 조정을 사용하여 PSD 이미지를 배치 처리하는 방법

`for` 루프 안에서 각 파일을 로드하고 동일한 단계를 적용한 뒤 각 반복마다 `save`를 호출합니다. Aspose.PSD가 스트리밍 방식으로 파일을 처리하므로 동일한 `PsdImage` 인스턴스를 재사용하여 메모리 사용량을 300 MB 이하로 유지하면서 **수백 개의 PSD**를 처리할 수 있습니다.

## PSD를 네거티브 이미지로 변환하는 방법

Invert Adjustment Layer를 최상위 항목으로 추가하고 문서를 저장하면 – 이 작업은 **convert PSD to negative**와 동일합니다. 이후에 레이어를 비활성화하거나 삭제하여 원본 파일을 다시 로드하지 않고도 원래 모습으로 되돌릴 수 있습니다.

## 일반적인 문제 및 팁

| 문제 | 원인 | 해결책 |
|-------|-------|----------|
| **`Image.load`에서 NullPointerException** | 잘못된 파일 경로 또는 파일 누락 | `dataDir`와 파일 이름을 확인하고, 테스트 시 절대 경로를 사용하십시오. |
| **레이어 순서가 예상과 다름** | 기존 레이어 뒤에 레이어를 추가하면 스택 순서가 변경됩니다 | 다른 조정 전에 반전 레이어를 삽입하거나 `psdImage.getLayers().move()`를 사용해 순서를 재배열하십시오. |
| **대형 PSD에서 성능 저하** | 매우 큰 파일을 메모리로 로드함 | JVM 힙을 늘리세요 (`-Xmx2g`) 또는 `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)`를 사용해 파일을 청크로 처리하십시오. |

## 자주 묻는 질문

**Q: Aspose.PSD가 모든 Java 버전과 호환되나요?**  
A: 예, Java 6.0 이상을 지원하며 Java 8, 11, 17도 포함됩니다.

**Q: 단일 작업에서 여러 조정 레이어를 적용할 수 있나요?**  
A: 물론입니다. 반전 레이어를 추가한 후 `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()` 등을 호출하여 효과를 스택할 수 있습니다.

**Q: 전체 API 레퍼런스는 어디에서 찾을 수 있나요?**  
A: 전체 문서는 [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

**Q: Aspose.PSD의 무료 체험판이 있나요?**  
A: 예, 체험 버전을 다운로드할 수 있습니다 [Aspose.PSD trial download](https://releases.aspose.com/).

**Q: 테스트용 임시 라이선스를 어떻게 얻나요?**  
A: 임시 라이선스를 요청하십시오 [temporary license request page](https://purchase.aspose.com/temporary-license/).

---

**마지막 업데이트:** 2026-11-04  
**테스트 환경:** Aspose.PSD 24.12 for Java  
**작성자:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## 관련 튜토리얼

- [Aspose.PSD for Java를 사용하여 PSD 파일에 레벨 조정 레이어 추가](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [PSD에서 조정 레이어 – 채널 믹서 추가 (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [PSD 편집 - Java를 사용하여 커브 조정 레이어 추가](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
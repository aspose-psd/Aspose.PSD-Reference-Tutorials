---
date: 2026-04-22
description: 이미지 처리 Java 라이브러리 Aspose.PSD를 사용하여 반전 조정 레이어를 포함한 여러 조정 레이어를 적용하고 원활한
  PSD 조작을 수행하는 방법을 배워보세요.
keywords:
- image processing java library
- how to add invert
- invert colors psd
- batch process psd images
- apply multiple adjustment layers
linktitle: 반전 조정 레이어
second_title: Aspose.PSD Java API
title: '이미지 처리 Java 라이브러리: Aspose.PSD를 사용한 레이어 반전'
url: /ko/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java에서 반전 조정 레이어

## 소개

강력한 **image processing java library**를 찾고 있다면 Aspose.PSD for Java는 시장에서 가장 다재다능한 옵션 중 하나입니다. 이 튜토리얼에서는 PSD 파일에 **Invert Adjustment Layer**를 추가하는 방법을 단계별로 안내합니다. 이 기술은 다른 조정 레이어와 결합하여 정교한 시각 효과를 구현할 수 있습니다. 배치‑처리 도구, 서버‑사이드 이미지 서비스, 혹은 단일 이미지 편집기를 구축하든, 이 가이드는 작업을 빠르고 안정적으로 수행할 수 있는 명확한 절차를 제공합니다.

## 빠른 답변
- **Invert Adjustment Layer는 무엇을 하나요?** 선택 영역의 모든 색상 값을 반전시켜 네거티브 이미지 효과를 만듭니다(즉, **PSD를 네거티브로 변환**합니다).  
- **어떤 라이브러리가 이 기능을 제공하나요?** Aspose.PSD, 선도적인 **image processing java library**입니다.  
- **다른 조정과 함께 쌓아 사용할 수 있나요?** 예 – Brightness/Contrast, Hue/Saturation 등 **여러 조정 레이어를 적용**할 수 있습니다.  
- **개발에 라이선스가 필요하나요?** 무료 체험판을 사용할 수 있으며, 프로덕션 사용 시 라이선스가 필요합니다.  
- **구현에 얼마나 걸리나요?** 기본 사용 사례는 보통 10분 이내에 완료됩니다.

## Invert Adjustment Layer란?

Invert Adjustment Layer는 비파괴 편집으로, 영향을 받는 모든 픽셀의 RGB 값을 뒤집습니다. 레이어 스택 위에 위치하기 때문에 가시성을 토글하거나 순서를 변경해도 원본 이미지 데이터는 영구적으로 변경되지 않습니다. 이는 **invert colors PSD** 파일이나 사진 네거티브를 만들 가장 쉬운 방법입니다.

## 왜 Aspose.PSD를 이미지 처리 Java 라이브러리로 선택해야 할까요?

- **Full PSD support** – Photoshop이 설치되지 않아도 Photoshop 파일을 읽고, 편집하고, 저장할 수 있습니다.  
- **Cross‑platform** – 모든 Java 런타임(Java 6 이상)에서 작동합니다.  
- **Rich adjustment features** – 다양한 일반 편집을 위한 내장 메서드를 제공해 **여러 조정 레이어를 한 워크플로우에서 적용**하기 쉽습니다.  
- **Performance‑optimized** – 대용량 파일을 효율적으로 처리하므로 **batch process psd images**에 필수적입니다.  

## 전제 조건

시작하기 전에 다음을 준비하세요:

1. **Aspose.PSD Library** – 공식 사이트 [here](https://releases.aspose.com/psd/java/)에서 다운로드합니다.  
2. **Java Development Environment** – JDK 6.0 이상이 설치되고 구성되어 있어야 합니다.  

이제 코드를 살펴보겠습니다.

## Import Packages

필요한 클래스를 가져옵니다. 이 임포트는 핵심 이미지 처리 API와 PSD 전용 기능에 접근할 수 있게 해줍니다.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Step 1: Set Up Document Directory

소스 PSD 파일이 있는 폴더와 출력 파일을 저장할 폴더를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load PSD File

소스 파일을 `PsdImage` 객체로 로드합니다. 이 객체는 메모리 내 전체 PSD 문서를 나타냅니다.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Step 3: Add Invert Adjustment Layer

내장 메서드를 호출해 현재 레이어 스택 위에 Invert Adjustment Layer를 삽입합니다. 이후에 다른 레이어(예: Brightness, Hue)를 추가해 **여러 조정 레이어를 적용**할 수 있습니다.

```java
im.addInvertAdjustmentLayer();
```

## Step 4: Save the Output

수정된 PSD를 디스크에 저장합니다. 저장된 파일에는 Invert Adjustment Layer가 포함되어 있으며 Photoshop이나 PSD 호환 뷰어에서 열 수 있습니다.

```java
im.save(outputPath);
```

### 방금 무슨 일이 일어났나요?

- PSD가 메모리로 로드되었습니다.  
- Invert Adjustment Layer가 최상위 레이어로 추가되었습니다.  
- 이미지가 저장되어 비파괴 편집이 보존되었습니다.

이제 **image processing java library**인 Aspose.PSD를 사용해 PSD 파일을 성공적으로 조작했습니다.

## Invert Adjustment를 활용한 PSD 이미지 배치 처리

수십 개 또는 수백 개의 파일에 동일한 반전 효과를 적용해야 할 경우, 위 코드를 간단한 루프에 넣어 PSD 디렉터리를 순회하면 됩니다. 라이브러리가 **performance‑optimized**이므로 대용량 배치도 빠르게 처리할 수 있으며, 같은 루프에서 밝기, 색조 등 다른 조정과도 결합할 수 있습니다.

## PSD를 네거티브 이미지로 변환하기

Invert Adjustment Layer는 본질적으로 **convert PSD to negative** 작업입니다. 이 레이어를 최상위에 추가하면 원본 픽셀 데이터를 영구적으로 변경하지 않고 전체 네거티브 효과를 얻을 수 있습니다. 이후 레이어를 제거하거나 비활성화하면 원래 모습으로 복구됩니다.

## Common Issues & Tips

| 문제 | 원인 | 해결책 |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | 잘못된 파일 경로 또는 파일이 없음 | `dataDir`와 파일 이름을 확인하고, 테스트를 위해 절대 경로를 사용하세요 |
| **Layer order not as expected** | 기존 레이어 뒤에 레이어를 추가하면 스택 순서가 변경됩니다 | `im.addInvertAdjustmentLayer()`를 다른 조정 레이어를 추가하기 전에 사용하거나, `im.getLayers()`를 통해 레이어 순서를 재정렬하세요 |
| **Performance slowdown on large PSDs** | 매우 큰 파일을 메모리에 로드함 | 페이지를 청크로 처리하거나 JVM 힙 크기(`-Xmx2g`)를 늘리는 것을 고려하세요 |

## Frequently Asked Questions

**Q: Aspose.PSD가 모든 Java 버전과 호환되나요?**  
A: Aspose.PSD는 Java 6.0 이상 버전을 지원합니다.

**Q: 단일 작업에서 여러 조정 레이어를 적용할 수 있나요?**  
A: 예, Invert, Brightness, Hue/Saturation 등 여러 조정 레이어를 쌓아 복합 효과를 만들 수 있습니다.

**Q: Aspose.PSD에 대한 추가 문서는 어디서 찾을 수 있나요?**  
A: 포괄적인 가이드와 API 레퍼런스를 제공하는 문서 [here](https://reference.aspose.com/psd/java/)를 참고하세요.

**Q: Aspose.PSD의 무료 체험판이 있나요?**  
A: 예, 무료 체험판을 [here](https://releases.aspose.com/)에서 확인할 수 있습니다.

**Q: Aspose.PSD 임시 라이선스는 어떻게 얻나요?**  
A: 임시 라이선스를 [here](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

---

**Last Updated:** 2026-04-22  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
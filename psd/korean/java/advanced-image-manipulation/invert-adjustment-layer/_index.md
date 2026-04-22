---
date: 2026-02-07
description: 이미지 처리 Java 라이브러리 Aspose.PSD를 사용하여 인버트 조정 레이어를 포함한 여러 조정 레이어를 적용하고 원활하게
  PSD를 조작하는 방법을 배우세요.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: '이미지 처리 Java 라이브러리: Aspose.PSD를 이용한 레이어 반전'
url: /ko/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java에서 Invert Adjustment Layer 사용하기

## 소개

견고한 **image processing java library**를 찾고 있다면, Aspose.PSD for Java는 시장에서 가장 다재다능한 옵션 중 하나입니다. 이 튜토리얼에서는 PSD 파일에 **Invert Adjustment Layer**를 추가하는 방법을 단계별로 안내합니다. 이 기술은 다른 조정 레이어와 결합하여 정교한 시각 효과를 만들 수 있습니다. 배치 처리 도구를 만들든 단일 이미지 편집기를 만들든, 이 가이드는 작업을 빠르게 완료할 수 있는 명확한 절차를 제공합니다.

## 빠른 답변
- **Invert Adjustment Layer는 무엇을 하나요?** 선택 영역의 모든 색상 값을 반전시켜 네거티브 이미지 효과를 만듭니다.  
- **어떤 라이브러리가 이 기능을 제공하나요?** Aspose.PSD, 선도적인 **image processing java library**입니다.  
- **다른 조정과 함께 쌓을 수 있나요?** 네 – **apply multiple adjustment layers**와 같이 Brightness/Contrast, Hue/Saturation 등 여러 레이어를 적용할 수 있습니다.  
- **개발에 라이선스가 필요합니까?** 무료 체험판을 사용할 수 있으며, 프로덕션 사용 시 라이선스가 필요합니다.  
- **구현에 얼마나 걸립니까?** 기본 사용 사례의 경우 보통 10분 이내에 완료됩니다.

## Invert Adjustment Layer란?

Invert Adjustment Layer는 영향을 받는 모든 픽셀의 RGB 값을 뒤집는 비파괴 편집입니다. 레이어 스택 위에 위치하기 때문에 원본 이미지 데이터를 영구적으로 변경하지 않고도 가시성을 토글하거나 순서를 재배열할 수 있습니다.

## Aspose.PSD를 사용하여 레이어 반전하기

아래에서는 PSD 파일에서 **how to invert layer**하는 정확한 방법을 보여줍니다. 개념에 집중할 수 있도록 단계는 의도적으로 간단하게 구성했습니다.

## 왜 Aspose.PSD를 이미지 처리 Java 라이브러리로 사용해야 할까요?

- **Full PSD support** – Photoshop이 설치되지 않아도 Photoshop 파일을 읽고, 편집하고, 저장할 수 있습니다.  
- **Cross‑platform** – 모든 Java 런타임(Java 6 이상)에서 작동합니다.  
- **Rich adjustment features** – 다양한 일반 편집을 위한 내장 메서드를 제공하므로 **apply multiple adjustment layers**를 단일 워크플로우에서 쉽게 적용할 수 있습니다.  
- **Performance‑optimized** – 대용량 파일을 효율적으로 처리하여 배치 처리에 필수적입니다.

## 전제 조건

시작하기 전에 다음이 준비되어 있는지 확인하십시오:

1. **Aspose.PSD Library** – 공식 사이트 [here](https://releases.aspose.com/psd/java/)에서 다운로드합니다.  
2. **Java Development Environment** – JDK 6.0 이상이 설치되고 구성되어 있어야 합니다.  

이제 코드를 살펴보겠습니다.

## 패키지 가져오기

필요한 클래스를 가져옵니다. 이러한 임포트는 핵심 이미지 처리 API와 PSD‑특화 기능에 접근할 수 있게 해줍니다.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## 단계 1: 문서 디렉터리 설정

소스 PSD 파일이 있는 폴더와 출력이 저장될 위치를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

## 단계 2: PSD 파일 로드

소스 파일을 `PsdImage` 객체에 로드합니다. 이 객체는 메모리 내 전체 PSD 문서를 나타냅니다.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## 단계 3: Invert Adjustment Layer 추가

현재 레이어 스택 위에 Invert Adjustment Layer를 삽입하는 내장 메서드를 호출합니다. 이후에 Brightness, Hue 등 다른 레이어를 추가하여 **apply multiple adjustment layers**를 할 수 있습니다.

```java
im.addInvertAdjustmentLayer();
```

## 단계 4: 출력 저장

수정된 PSD를 디스크에 저장합니다. 저장된 파일에는 Invert Adjustment Layer가 포함되어 있으며 Photoshop이나 PSD‑호환 뷰어에서 열 수 있습니다.

```java
im.save(outputPath);
```

### 방금 무슨 일이 일어났나요?

- PSD가 메모리로 로드되었습니다.  
- Invert Adjustment Layer가 최상위 레이어로 추가되었습니다.  
- 이미지가 저장되어 비파괴 편집이 보존되었습니다.

이제 **image processing java library**인 Aspose.PSD를 사용해 PSD 파일을 성공적으로 조작했습니다.

## 일반적인 문제 및 팁

| Issue | Cause | Solution |
|-------|-------|----------|
| **`Image.load`에서 NullPointerException** | 파일 경로가 잘못되었거나 파일이 없습니다 | `dataDir`와 파일 이름을 확인하고, 테스트 시 절대 경로를 사용하세요 |
| **레이어 순서가 예상과 다름** | 기존 레이어 뒤에 레이어를 추가하면 스택 순서가 바뀝니다 | 다른 조정을 추가하기 전에 `im.addInvertAdjustmentLayer()`를 사용하거나, `im.getLayers()`로 레이어 순서를 재배열하세요 |
| **대용량 PSD에서 성능 저하** | 매우 큰 파일을 메모리로 로드함 | 페이지를 청크로 처리하거나 JVM 힙 크기(`-Xmx2g`)를 늘리는 것을 고려하세요 |

## 자주 묻는 질문

**Q: Aspose.PSD가 모든 Java 버전과 호환되나요?**  
A: Aspose.PSD는 Java 6.0 이상을 지원합니다.

**Q: 한 번에 여러 조정 레이어를 적용할 수 있나요?**  
A: 네, Invert, Brightness, Hue/Saturation 등 여러 조정 레이어를 쌓아 복잡한 효과를 만들 수 있습니다.

**Q: Aspose.PSD에 대한 추가 문서는 어디서 찾을 수 있나요?**  
A: 문서는 [here](https://reference.aspose.com/psd/java/)에서 확인하세요.

**Q: Aspose.PSD의 무료 체험판이 있나요?**  
A: 네, 무료 체험판은 [here](https://releases.aspose.com/)에서 이용할 수 있습니다.

**Q: Aspose.PSD 임시 라이선스를 어떻게 얻나요?**  
A: 임시 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
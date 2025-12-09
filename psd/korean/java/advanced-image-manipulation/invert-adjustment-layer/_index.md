---
date: 2025-12-02
description: 이미지 처리 Java 라이브러리 Aspose.PSD를 사용하여 인버트 조정 레이어를 포함한 여러 조정 레이어를 적용하고 원활한
  PSD 조작을 수행하는 방법을 배워보세요.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: '이미지 처리 Java 라이브러리: Aspose.PSD를 사용한 레이어 반전'
url: /ko/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java에서 Invert Adjustment Layer 적용하기

## 소개

강력한 **image processing java library**를 찾고 있다면, Aspose.PSD for Java는 시장에서 가장 다재다능한 옵션 중 하나입니다. 이 튜토리얼에서는 PSD 파일에 **Invert Adjustment Layer**를 추가하는 방법을 단계별로 살펴보며, 다른 조정 레이어와 결합해 정교한 시각 효과를 구현하는 방법을 소개합니다. 배치 처리 도구를 만들든 단일 이미지 편집기를 만들든, 이 가이드는 작업을 빠르게 완료할 수 있는 명확한 절차를 제공합니다.

## 빠른 답변
- **Invert Adjustment Layer는 무엇을 하나요?** 선택된 영역의 모든 색상 값을 반전시켜 네거티브 이미지 효과를 만듭니다.  
- **어떤 라이브러리가 이 기능을 제공하나요?** Aspose.PSD, 선도적인 image processing java library입니다.  
- **다른 조정 레이어와 함께 사용할 수 있나요?** 예 – **Brightness/Contrast**, **Hue/Saturation** 등 여러 조정 레이어를 **apply multiple adjustment layers** 할 수 있습니다.  
- **개발에 라이선스가 필요하나요?** 무료 체험판을 제공하며, 프로덕션 사용 시 라이선스가 필요합니다.  
- **구현에 얼마나 걸리나요?** 기본 사용 사례는 보통 10분 이내에 완료됩니다.

## Invert Adjustment Layer란?

Invert Adjustment Layer는 비파괴 편집으로, 영향을 받는 모든 픽셀의 RGB 값을 뒤집습니다. 레이어 스택 위에 위치하기 때문에 가시성을 토글하거나 순서를 변경해도 원본 이미지 데이터는 영구적으로 변경되지 않습니다.

## 왜 Aspose.PSD를 이미지 처리 Java 라이브러리로 선택해야 할까요?

- **전체 PSD 지원** – Photoshop이 설치되지 않아도 Photoshop 파일을 읽고, 편집하고, 저장할 수 있습니다.  
- **크로스‑플랫폼** – 모든 Java 런타임(Java 6 이상)에서 동작합니다.  
- **풍부한 조정 기능** – 다양한 일반 편집을 위한 내장 메서드를 제공하므로 **apply multiple adjustment layers** 를 단일 워크플로우에서 쉽게 수행할 수 있습니다.  
- **성능 최적화** – 대용량 파일을 효율적으로 처리하므로 배치 처리에 필수적입니다.

## 사전 요구 사항

시작하기 전에 다음 항목을 준비하세요:

1. **Aspose.PSD Library** – 공식 사이트 [here](https://releases.aspose.com/psd/java/)에서 다운로드합니다.  
2. **Java 개발 환경** – JDK 6.0 이상이 설치되고 설정되어 있어야 합니다.  

그럼 코드를 살펴보겠습니다.

## 패키지 가져오기

필요한 클래스를 가져옵니다. 이 임포트는 핵심 이미지 처리 API와 PSD 전용 기능에 접근할 수 있게 해줍니다.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## 1단계: 문서 디렉터리 설정

소스 PSD 파일이 위치한 폴더와 출력 파일을 저장할 위치를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

## 2단계: PSD 파일 로드

소스 파일을 `PsdImage` 객체에 로드합니다. 이 객체는 메모리 내 전체 PSD 문서를 나타냅니다.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## 3단계: Invert Adjustment Layer 추가

내장 메서드를 호출해 현재 레이어 스택 최상단에 Invert Adjustment Layer를 삽입합니다. 이후에 다른 레이어(예: Brightness, Hue)를 추가해 **apply multiple adjustment layers** 할 수 있습니다.

```java
im.addInvertAdjustmentLayer();
```

## 4단계: 출력 저장

수정된 PSD를 디스크에 저장합니다. 저장된 파일에는 Invert Adjustment Layer가 포함되어 있으며 Photoshop이나 PSD 호환 뷰어에서 열 수 있습니다.

```java
im.save(outputPath);
```

### 방금 무슨 일이 일어났나요?

- PSD가 메모리로 로드되었습니다.  
- Invert Adjustment Layer가 최상위 레이어로 추가되었습니다.  
- 이미지가 저장되어 비파괴 편집이 유지되었습니다.

이제 **image processing java library**인 Aspose.PSD를 사용해 PSD 파일을 성공적으로 조작했습니다.

## 일반적인 문제 및 팁

| Issue | Cause | Solution |
|-------|-------|----------|
| **`Image.load`에서 NullPointerException** | 파일 경로가 잘못되었거나 파일이 없음 | `dataDir`와 파일 이름을 확인하고, 테스트 시 절대 경로를 사용 |
| **레이어 순서가 기대와 다름** | 기존 레이어 뒤에 레이어를 추가하면 스택이 변경됨 | 다른 조정을 추가하기 전에 `im.addInvertAdjustmentLayer()`를 호출하거나 `im.getLayers()`를 통해 레이어 순서를 재조정 |
| **대용량 PSD에서 성능 저하** | 매우 큰 파일을 메모리로 로드함 | 페이지를 청크로 처리하거나 JVM 힙 크기(`-Xmx2g`)를 늘리는 것을 고려 |

## 자주 묻는 질문

**Q: Aspose.PSD는 모든 Java 버전과 호환되나요?**  
A: Aspose.PSD는 Java 6.0 이상을 지원합니다.

**Q: 한 번에 여러 조정 레이어를 적용할 수 있나요?**  
A: 예, Invert, Brightness, Hue/Saturation 등 여러 조정 레이어를 스택하여 복합 효과를 만들 수 있습니다.

**Q: Aspose.PSD에 대한 추가 문서는 어디서 찾을 수 있나요?**  
A: 포괄적인 가이드와 API 레퍼런스는 문서 [here](https://reference.aspose.com/psd/java/)를 참고하세요.

**Q: 무료 체험판을 이용할 수 있나요?**  
A: 예, 무료 체험판은 [here](https://releases.aspose.com/)에서 확인할 수 있습니다.

**Q: Aspose.PSD 임시 라이선스를 어떻게 얻나요?**  
A: 임시 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

---

**마지막 업데이트:** 2025-12-02  
**테스트 환경:** Aspose.PSD 24.12 for Java  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
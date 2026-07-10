---
date: 2026-03-28
description: Aspose.PSD for Java를 사용하여 사진 필터 레이어를 만들고 조정 레이어 PSD 파일을 추가하는 방법을 배워보세요.
  이 가이드를 따라 편집 및 필터 추가를 손쉽게 수행하세요.
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: Java를 사용하여 PSD에서 사진 필터 레이어 만들기
url: /ko/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD에서 사진 필터 조정 레이어 관리 - Java

## 소개
Java 개발자로서 PSD 파일 안에 **create photo filter layer** 객체를 만들고 싶다면, 바로 여기가 맞는 곳입니다. 이 튜토리얼에서는 Aspose.PSD for Java를 사용하여 기존 Photo Filter Adjustment Layer를 편집하고 새로운 레이어를 추가하는 방법을 단계별로 안내합니다. 끝까지 읽으면 **create photo filter layer**를 정확히 생성하고, 속성을 조정하며, 심지어 **add adjustment layer PSD** 파일을 프로그래밍 방식으로 추가하는 방법을 알게 되어 그래픽 디자인 작업 흐름을 가속화할 수 있습니다.

## 빠른 답변
- **Java에서 PSD 레이어를 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java  
- **기존 Photo Filter 레이어를 편집할 수 있나요?** 예 – PSD를 로드하고 `PhotoFilterLayer`를 찾아 속성을 수정합니다.  
- **새 필터 레이어를 어떻게 추가하나요?** `PsdImage` 인스턴스에서 `addPhotoFilterLayer(Color)`를 사용합니다.  
- **프로덕션에 라이선스가 필요합니까?** 상업용 라이선스가 필요합니다; 무료 체험판을 사용할 수 있습니다.  
- **지원되는 Java 버전은 무엇인가요?** JDK 8 이상 (JDK 11 권장).  

## Photo Filter Adjustment Layer란 무엇인가요?
Photo Filter Adjustment Layer는 선택한 색상으로 전체 이미지를 색조하는 비파괴 효과이며, 사진 필터를 적용하는 것과 유사합니다. 자체 레이어에 존재하므로 색상, 밀도, 밝기를 원본 픽셀을 변경하지 않고 조정할 수 있습니다.

## 왜 Aspose.PSD를 사용해 photo filter layer를 생성하나요?
- **Full control** Adobe Photoshop 없이 PSD 구조를 완전히 제어합니다.  
- **Cross‑platform** Java API가 Windows, Linux, macOS에서 작동합니다.  
- **No COM interop** – 순수 Java이며 서버 측 처리에 이상적입니다.  
- **Supports PSD version 1‑8**, 레이어 효과와 마스크를 보존합니다.  

## 전제 조건
### 필수 소프트웨어
1. Java Development Kit (JDK): 머신에 호환되는 JDK 버전이 설치되어 있는지 확인하세요. [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드할 수 있습니다.  
2. Aspose.PSD for Java: PSD 파일을 조작하려면 Aspose.PSD 라이브러리가 필요합니다. [Aspose releases page](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다. 자세한 내용은 [Aspose documentation](https://reference.aspose.com/psd/java/)을 확인하세요.  
3. IDE (Integrated Development Environment): IntelliJ IDEA 또는 Eclipse와 같은 좋은 IDE를 사용하면 코딩 경험이 원활해집니다.  

### 기본 이해
Java 프로그래밍에 익숙하고 PSD 파일이 어떻게 작동하는지 기본적인 이해가 있으면 도움이 됩니다. Java에서 라이브러리를 처음 사용하는 경우, 프레임워크를 가져오고 활용하는 방법에 익숙해지는 것이 좋습니다.

## 패키지 가져오기
시작하려면 Aspose.PSD 라이브러리에서 필요한 클래스를 가져와야 합니다. 다음은 Java 파일 시작 부분에 필요한 간단한 import 문입니다:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
Simply paste this at the top of your Java file, and you’re set to begin working with PSD images!

## 기존 Photo Filter 레이어 편집
### 단계 1: 데이터 디렉터리 설정
먼저, PSD 파일이 저장된 디렉터리를 정의해야 합니다. `"Your Document Directory"`를 실제 경로로 교체하세요. 이렇게 하면 모든 것이 정리됩니다:
```java
String dataDir = "Your Document Directory";
```

### 단계 2: PSD 파일 로드
이제 편집하려는 PSD 파일을 로드합니다. 지정한 디렉터리에 `PhotoFilterAdjustmentLayer.psd`가 존재하는지 확인하세요.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### 단계 3: 이미지 객체 초기화
Aspose의 내장 기능을 사용하여 이미지를 프로젝트에 로드합니다:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 단계 4: 레이어 순회
다음으로 PSD 파일 내 레이어를 검사합니다. 목표는 `PhotoFilterLayer`를 찾는 것입니다:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### 단계 5: Photo Filter 레이어 사용자 정의
여기서 마법이 일어납니다! `Color`와 `Density`를 수정할 수 있습니다. 예를 들어, 색상을 선명한 빨강으로 설정하고 밀도를 조정할 수 있습니다:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### 단계 6: 편집된 PSD 파일 저장
마지막으로 변경 사항을 저장하여 조정된 새로운 PSD 파일을 생성합니다:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
방금 PSD 파일에서 Photo Filter Adjustment Layer를 편집했습니다.

## 새로운 Photo Filter 레이어 추가
### 단계 1: 디렉터리 경로 설정
앞과 같이 데이터 디렉터리를 정의합니다:
```java
String dataDir = "Your Document Directory";
```

### 단계 2: 소스 파일 로드
이 예제에서는 **add adjustment layer PSD**를 추가하려는 다른 PSD 파일을 로드합니다:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### 단계 3: 이미지 객체 다시 초기화
새 `PsdImage` 인스턴스를 생성해야 하므로 파일을 로드합니다:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 단계 4: Photo Filter 레이어 추가
이제 사용자 정의 색상으로 새로운 Photo Filter 레이어를 추가할 수 있습니다. 방법은 다음과 같습니다:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### 단계 5: 새로운 PSD 파일 저장
다시 한 번 변경 사항을 저장할 시간입니다. 이를 수행하는 코드는 다음과 같습니다:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
새로운 photo filter 레이어를 PSD 파일에 성공적으로 추가했습니다.

## 일반적인 문제 및 해결책
- **`ClassCastException` when loading the image** – 로드하는 파일이 PSD인지 확인하세요; 다른 형식은 다른 클래스를 필요로 합니다.  
- **Color values appear incorrect** – 각 구성 요소가 0‑255인 `Color.fromArgb(alpha, red, green, blue)`를 사용하세요.  
- **Layer not found** – 소스 PSD에 실제로 `PhotoFilterLayer`가 포함되어 있는지 확인하세요. 디버깅을 위해 `im.getLayers().length`를 사용합니다.  

## 자주 묻는 질문
### Aspose.PSD란?
Aspose.PSD는 PSD 파일을 생성, 편집 및 변환하기 위한 .NET 및 Java 라이브러리입니다.

### Aspose.PSD를 무료로 체험할 수 있나요?
예, Aspose는 무료 체험 버전을 제공합니다. [여기](https://releases.aspose.com/)에서 확인하세요.

### 문서는 어디에서 찾을 수 있나요?
전체 문서는 [Aspose의 레퍼런스 페이지](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

### Aspose.PSD를 어떻게 구매하나요?
[이 링크](https://purchase.aspose.com/buy)에서 소프트웨어를 구매할 수 있습니다.

### Aspose.PSD에 대한 지원이 있나요?
물론입니다! Aspose 지원 포럼 [여기](https://forum.aspose.com/c/psd/34)에서 지원을 받을 수 있습니다.

---

**마지막 업데이트:** 2026-03-28  
**테스트 환경:** Aspose.PSD for Java 24.11 (latest as of 2026)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
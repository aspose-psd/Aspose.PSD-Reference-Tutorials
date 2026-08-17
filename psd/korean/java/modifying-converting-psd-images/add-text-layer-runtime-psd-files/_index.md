---
date: 2026-03-07
description: Java와 Aspose.PSD를 사용하여 런타임에 PSD 파일에 텍스트를 추가하는 방법을 배워보세요. 이 단계별 가이드를 따라
  빠르게 PSD에 텍스트 레이어를 생성하세요.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Java를 사용하여 런타임에 PSD 파일에 텍스트 추가
url: /ko/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 런타임에 PSD 파일에 텍스트 추가

## Introduction
수동으로 Photoshop 문서를 편집해 본 적이 있다면 레이어가 얼마나 강력한지 알 수 있습니다. Java 애플리케이션에서 **PSD에 텍스트를 추가**할 수 있다면 어떨까요? Aspose.PSD for Java 라이브러리를 사용하면 런타임에 PSD에 텍스트 레이어를 생성할 수 있어 배치 처리, 동적 그래픽 생성 및 자동화된 브랜딩 워크플로우의 문을 열어줍니다. 이 튜토리얼에서는 프로젝트 설정부터 업데이트된 파일 저장까지 전체 과정을 단계별로 살펴보겠습니다.

## Quick Answers
- **필요한 라이브러리는?** Aspose.PSD for Java.  
- **기존 PSD에 텍스트를 추가할 수 있나요?** 예 – 파일을 로드하고 `TextLayer`를 추가한 뒤 저장하면 됩니다.  
- **프로덕션에 라이선스가 필요합니까?** 비평가용이 아닌 경우 상업용 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** JDK 8 이상 (최신 LTS 버전을 권장합니다).  
- **웹 백엔드에 적합한가요?** 물론입니다 – API는 모든 Java 기반 서버 환경에서 작동합니다.

## What is “add text to PSD”?
PSD에 텍스트를 추가한다는 것은 프로그래밍 방식으로 Photoshop 문서 안에 새로운 텍스트 레이어를 만드는 것을 의미합니다. 이 레이어는 일반 Photoshop 텍스트 레이어와 동일하게 동작하며, Photoshop을 열지 않고도 이동, 내용 편집 및 스타일 적용이 가능합니다.

## Why create a text layer in a PSD with Java?
- **Automation** – 마케팅 자산, 워터마크 또는 제품 라벨을 대량으로 생성합니다.  
- **Consistency** – 수천 개 파일에 걸쳐 동일한 폰트, 크기 및 위치를 보장합니다.  
- **Integration** – 다른 Java 서비스(e‑commerce, 보고, CI 파이프라인)와 결합해 실시간으로 그래픽을 제공합니다.

## Prerequisites
코드를 작성하기 전에 다음을 준비하세요:

1. **Java Development Kit (JDK)** – JDK 8 이상 설치. [download it here](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드할 수 있습니다.  
2. **Aspose.PSD for Java** – 최신 JAR 파일을 [Aspose releases page](https://releases.aspose.com/psd/java/)에서 받으세요.  
3. **IDE (optional but helpful)** – IntelliJ IDEA, Eclipse 또는 선호하는 편집기.  
4. **Basic Java knowledge** – 클래스, 객체 및 파일 I/O에 익숙해야 합니다.  
5. **A sample PSD** – 이 가이드에서는 `OneLayer.psd`를 사용하며, 원하는 폴더에 배치합니다.

## Import Packages
먼저 PSD 파일과 텍스트 레이어 작업에 필요한 클래스를 가져옵니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

이 임포트는 Aspose.PSD 핵심 기능에 접근할 수 있게 해줍니다.

## Step‑by‑Step Guide

### Step 1: Set Up Your Document Directory
소스 PSD가 위치한 폴더와 출력이 저장될 폴더를 정의합니다.

```java
String dataDir = "Your Document Directory"; 
```

`"Your Document Directory"`를 파일이 있는 절대 경로나 상대 경로로 교체하세요.

### Step 2: Load Your Source PSD File
`Image.load()`를 사용해 기존 PSD를 메모리로 불러옵니다.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

경로가 올바르면 `img`가 로드된 Photoshop 문서를 나타냅니다.

### Step 3: Cast to `PsdImage`
Photoshop 전용 기능을 사용하기 위해 일반 `Image`를 `PsdImage`로 캐스팅합니다.

```java
PsdImage im = (PsdImage)img;
```

캐스팅을 통해 `addTextLayer()`와 같은 메서드를 사용할 수 있습니다.

### Step 4: Define the Rectangle for the Text Layer
새 텍스트가 표시될 위치를 지정합니다. 사각형은 위치(x, y)와 크기(width, height)를 정의합니다.

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

레이아웃에 맞게 계산식을 자유롭게 조정하세요.

### Step 5: Add the Text Layer
정의한 사각형 안에 실제 텍스트 레이어를 생성합니다.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

`"Added text"`를 PSD에 표시하고 싶은 문자열로 교체합니다. 여기서 **create text layer PSD**를 프로그래밍 방식으로 수행합니다.

### Step 6: Save Your Updated PSD File
원본을 덮어쓰지 않도록 수정된 문서를 새 파일에 저장합니다.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

실행 후 대상 폴더에서 `ImageWithTextLayer.psd`를 찾을 수 있으며, 이제 새 텍스트 레이어가 포함되어 있습니다.

## Common Issues & Solutions
| Issue | Reason | Fix |
|-------|--------|-----|
| **`NullPointerException` on `im.addTextLayer`** | PSD가 올바르게 로드되지 않음(경로 오류). | `sourceFileName`이 존재하는 PSD를 가리키는지 확인하세요. |
| **Text not visible** | 사각형이 캔버스 밖에 있거나 레이어가 숨김 상태. | 사각형 좌표를 조정하거나 `layer.setVisible(true)`로 레이어 가시성을 확인하세요. |
| **LicenseException** | 프로덕션 환경에서 유효한 라이선스 없이 사용. | 상업용 라이선스를 구매하고 `License license = new License(); license.setLicense("Aspose.PSD.lic");`로 설정하세요. |

## Frequently Asked Questions

**Q: 여러 개의 텍스트 레이어를 추가할 수 있나요?**  
A: 예 – 삽입하고 싶은 텍스트마다 Steps 4와 5를 반복하면 됩니다.

**Q: 텍스트 스타일(폰트, 크기, 색상)은 어떻게 지정하나요?**  
A: `TextLayer` 클래스의 `getTextData()` 메서드를 통해 `Font`, `FontSize`, `Color` 등 스타일 속성을 수정할 수 있습니다. 자세한 내용은 Aspose.PSD API 문서를 참고하세요.

**Q: PSD에 이미 많은 레이어가 있는 경우는 어떻게 하나요?**  
A: Aspose.PSD는 복잡한 레이어 구조를 지원합니다. 특정 그룹을 대상으로 하거나 `addTextLayer`의 오버로드를 사용해 원하는 인덱스에 새 텍스트 레이어를 삽입할 수 있습니다.

**Q: 이 방법을 웹 애플리케이션에 적용할 수 있나요?**  
A: 물론입니다. 서버가 Java를 실행할 수 있다면 실시간으로 PSD를 생성·수정하고 클라이언트에 제공할 수 있습니다.

**Q: 문제가 발생하면 어디서 도움을 받을 수 있나요?**  
A: [Aspose support forums](https://forum.aspose.com/c/psd/34)에서 커뮤니티와 Aspose 엔지니어가 지원을 제공합니다.

## Conclusion
이제 Java와 Aspose.PSD를 사용해 런타임에 **PSD에 텍스트를 추가**하는 방법이 얼마나 쉬운지 확인했습니다. 이 기술을 활용하면 그래픽 생성 자동화, 자산 개인화 및 Photoshop 수준의 편집을 모든 Java 기반 솔루션에 통합할 수 있습니다. 나머지 Aspose.PSD API를 탐색해 도형, 래스터 레이어 추가 또는 필터 적용 등 더욱 풍부한 자동화를 구현해 보세요.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose
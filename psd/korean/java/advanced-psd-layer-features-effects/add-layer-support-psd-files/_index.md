---
date: 2025-12-10
description: Aspose.PSD for Java를 사용하여 PSD 레이어를 추출하고 PSD 레이어를 PNG로 변환하는 방법을 배워보세요.
  강력한 그래픽 조작이 필요한 개발자에게 이상적입니다.
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: Aspose.PSD Java를 사용하여 PSD 레이어 추출 및 PSD 파일에 레이어 지원 추가
url: /ko/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java를 사용하여 PSD 레이어 추출 및 PSD 파일에 레이어 지원 추가

## Introduction
Photoshop Document(PSD) 파일 작업은 그래픽 디자이너와 개발자 모두에게 일상적인 현실입니다. 가장 일반적인 작업 중 하나는 **PSD 레이어를 추출**하여 편집, 재사용 또는 PNG와 같은 다른 형식으로 변환하는 것입니다. Java 애플리케이션에서는 Aspose.PSD가 이 과정을 직관적이고 코드 친화적으로 만들어 줍니다. 이 튜토리얼에서는 PSD 레이어를 추출하고 레이어 지원을 활성화하며 **PSD 레이어를 PNG로 변환**하는 정확한 단계와 명확한 설명, 실용적인 팁을 제공합니다.

## Quick Answers
- **“extract PSD layers”는 무엇을 의미하나요?** PSD 파일을 로드하고 각 개별 레이어에 접근하여작하거나 내보내는 것을 의미합니다.  
- **Java에서 이를 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java는 Photoshop 없이도 완전한 PSD 처리 기능을 제공합니다.  
- **한 번에 PSD 레이어를 PNG로 변환할 수 있나요?** 네—적절한 옵션으로 파일을 로드하고 투명성을 보존하는 PNG 옵션으로 저장하면 됩니다.  
- **프로덕션 사용에 라이선스가 필요한가요?** 프로덕션에서는 상용 라이선스가 필요하며, 평가용 무료 체험판을 사용할 수 있습니다.  
- **필요한 Java 버전은 무엇인가요?** JDK 8 이상(예제에서는 JDK 11 사용)입니다.

## What is “extract PSD layers”?
PSD 레이어 추출이란 PSD 파일의 내부 구조를 읽어 각 레이어를 독립적인 이미지 객체로 가져오는 것을 말합니다. 이를 통해 레이어를 개별적으로 편집, 숨김, 순서 변경 또는 내보낼 수 있으며, 디자이너가 Photoshop에서 하는 작업을 프로그래밍 방식으로 수행할 수 있습니다.

## Why extract PSD layers and convert them to PNG?
- **자산 재사용:** 마스터 PSD에서 아이콘, 버튼, UI 요소 등을 수동으로 내보내지 않고 바로 추출합니다.  
- **자동화:** 썸네일이나 웹용 이미지를 실시간으로 생성합니다.  
- **투명성 보존:** PNG는 알파 채널을 유지하므로 웹 그래픽에 최적입니다.  

## Prerequisites
본격적으로 진행하기 전에 다음 항목을 준비하세요.

1. **Java Development Environment** – JDK가 설치되어 있어야 합니다. [Oracle 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드할 수 있습니다.  
2. **Aspose.PSD for Java** – 공식 다운로드 페이지에서 최신 라이브러리를 받으세요. [여기](https://releases.aspose.com/psd/java/)에서 확인합니다.  
3. **Basic Java knowledge** – Java 프로그램을 컴파일하고 실행하는 기본 지식.  
4. **IDE** – IntelliJ IDEA, Eclipse 또는 선호하는 편집기.  
5. **A PSD file** – 보유하고 있는 PSD 파일을 사용하거나 테스트용 샘플 PSD를 다운로드합니다.

이 항목들을 준비하면 PSD 레이어 추출을 시작할 준비가 된 것입니다.

## Import Packages
먼저 Aspose.PSD 라이브러리에서 필요한 클래스를 가져옵니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Define Your Directories
소스 PSD와 출력 PNG의 경로를 설정합니다. `dataDir`을 파일이 위치한 폴더로 지정하세요.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"Your Document Directory"`를 실제 폴더 경로로 교체합니다.  
- `sourceFileName` – 처리하려는 PSD 파일의 전체 경로.  
- `output` – 추출된 레이어가 포함될 PNG 파일의 대상 경로.

## Step 2: Set Up the Load Options
`PsdLoadOptions`를 구성하면 모든 레이어 효과와 리소스가 올바르게 로드되어 **PSD 레이어를 추출**할 때 필수적입니다.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – 레이어에 연결된 추가 **효과**(예: 그림자)를 로드합니다.  
- `setUseDiskForLoadEffectsResource(true)` – 무거운 리소스를 **디스크**에 오프로드하여 **메모리** 부담을 줄입니다.

## Step 3: Load the PSD File
위에서 정의한 옵션을 사용해 PSD를 `PsdImage` 객체로 로드합니다.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

이 시점에서 `image`는 모든 레이어, 마스크 및 효과를 포함하고 있어 추출 준비가 완료되었습니다.

## Step 4: Set Up the Save Options
PNG 저장 방식을 구성합니다. `TruecolorWithAlpha`를 사용하면 원본 레이어의 투명성을 보존할 수 있습니다.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Step 5: Save the Image (Convert PSD Layers to PNG)
로드한 PSD(전체 레이어 포함)를 단일 PNG 파일로 내보냅니다. 이 단계는 **convert psd layers png**를 한 번에 수행합니다.

```java
image.save(output, saveOptions);
```

각 **레이어**를 별도의 PNG로 저장하려면 `image.getLayers()`를 순회하면 되지만, 많은 경우 병합된 PNG만으로 충분합니다.

## Step 6: Wrap It Up
프로세스가 성공했음을 알리는 친절한 콘솔 메시지를 추가합니다.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Common Issues & Tips
- **Out‑of‑Memory Errors:** 매우 큰 PSD를 처리할 경우 `setUseDiskForLoadEffectsResource(true)`를 유지해 임시 데이터를 디스크에 오프로드합니다.  
- **Missing Effects:** `setLoadEffectsResource(true)`가 설정되어 있는지 확인하세요. 그렇지 않으면 일부 **레이어 효과**가 무시될 수 있습니다.  
- **Path Problems:** 플랫폼에 독립적인 경로 처리를 위해 `java.nio.file`의 `Paths.get(...)`를 사용합니다.

## Frequently Asked Questions

**Q: Aspose.PSD for Java란 무엇인가요?**  
A: Aspose.PSD for Java는 Photoshop이 설치되지 않아도 PSD 파일을 조작할 수 있게 해 주는 라이브러리입니다.

**Q: Aspose.PSD를 다른 파일 형식에도 사용할 수 있나요?**  
A: 네! 주로 PSD 파일용이지만, Aspose는 다양한 다른 형식용 **라이브러리**도 제공합니다.

**Q: 체험판 버전을 사용할 수 있나요?**  
A: 물론입니다! 무료 체험판을 [여기](https://releases.aspose.com/)에서 다운로드할 수 있습니다.

**Q: 도움이 필요하면 어디서 지원을 받을 수 있나요?**  
A: Aspose 포럼에서 지원을 받을 수 있습니다. [여기](https://forum.aspose.com/c/psd/34)에서 확인하세요.

**Q: PNG를 PSD로 다시 변환할 수 있나요?**  
A: Aspose.PSD 라이브러리는 PSD 파일을 읽고 조작하는 데 중점을 두며, 다른 형식을 PSD로 변환하는 기능은 제한적입니다.

**Q: 각 **레이어**를 별도의 PNG로 추출하려면 어떻게 해야 하나요?**  
A: `image.getLayers()`를 순회하면서 각 레이어마다 새로운 `Bitmap`을 생성하고, 해당 `PngOptions`를 사용해 저장하면 레이어당 개별 PNG 파일을 얻을 수 있습니다.

## Conclusion
이제 Aspose.PSD for Java를 사용해 **PSD 레이어를 추출**, 전체 레이어 지원을 활성화하고 **PSD 레이어를 PNG로 변환**하는 방법을 배웠습니다. 자동화된 자산 파이프라인을 구축하거나 데스크톱 애플리케이션에 그래픽 기능을 추가하든, 이 접근 방식은 Photoshop을 직접 사용하지 않고도 Photoshop 파일을 세밀하게 제어할 수 있게 해 줍니다. 필터 적용, 레이어 병합 프로그래밍, 개별 레이어 별도 내보내기 등 다양한 확장도 자유롭게 시도해 보세요.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
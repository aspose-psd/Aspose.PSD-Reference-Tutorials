---
date: 2025-12-15
description: Aspose.PSD를 사용하여 Java에서 PSD를 PNG로 변환하고 PSD 레이어를 회전하는 방법을 배웁니다. 코드 샘플이
  포함된 단계별 가이드.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Java를 사용하여 PSD를 PNG로 변환하고 PSD 파일의 레이어 회전
url: /ko/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 PSD를 PNG로 변환하고 PSD 파일의 레이어 회전하기

## Introduction
**PSD를 PNG로 변환**하면서 레이어를 회전해야 한다면 이 가이드를 확인하세요. 배치 처리 도구를 만들거나 이미지 조작을 웹 서비스에 통합하려는 경우, 프로그래밍 방식으로 수행하면 시간을 절약하고 Adobe Photoshop에 대한 의존성을 없앨 수 있습니다. 이 튜토리얼에서는 Aspose.PSD for Java 라이브러리를 사용해 **PSD 레이어를 회전**하고 결과를 PNG로 내보내는 방법을 보여드립니다. 이제 팔을 걷어붙이고 디자인 워크플로를 원활하게 진행해 보세요!

## Quick Answers
- **어떤 라이브러리를 사용할 수 있나요?** Aspose.PSD for Java  
- **한 번에 회전과 변환을 모두 할 수 있나요?** 예 – PSD를 회전한 뒤 PNG로 저장  
- **라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있으며, 프로덕션에서는 유료 라이선스가 필요합니다  
- **지원되는 Java 버전은?** Java 8 이상  
- **PNG 출력이 투명합니까?** 예, `PngColorType.TruecolorWithAlpha`를 설정하면 투명도가 유지됩니다  

## What is “convert PSD to PNG”?
Photoshop 문서(PSD)를 PNG 이미지로 변환한다는 것은 모든 레이어, 마스크 및 투명성을 포함한 시각적 콘텐츠를 널리 지원되는 래스터 형식으로 추출하는 것을 의미합니다. PNG는 알파 채널을 보존하므로 웹 그래픽, 썸네일 및 추가 이미지 처리에 이상적입니다.

## Why use Aspose.PSD for Java to convert PSD to PNG and rotate PSD layers?
- **Photoshop이 필요 없음** – 모든 서버 또는 CI 환경에서 동작  
- **전체 레이어 지원** – 투명도와 레이어 효과를 그대로 유지  
- **간단한 API** – 몇 줄의 메서드 호출만으로 회전, 뒤집기 및 저장 가능  
- **크로스‑플랫폼** – Windows, Linux, macOS에서 실행  

## Prerequisites
코드를 작성하기 전에 다음 항목을 준비하세요:

- **Java Development Kit (JDK)** – [Oracle 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html)에서 다운로드.  
- **통합 개발 환경 (IDE)** – IntelliJ IDEA, Eclipse, NetBeans 중 선택.  
- **Aspose.PSD for Java 라이브러리** – [릴리스 페이지](https://releases.aspose.com/psd/java/)에서 최신 JAR 파일 획득.  
- **기본 Java 지식** – 클래스, 객체 및 예외 처리에 익숙해야 합니다.

## Step-by-Step Guide

### Step 1: Set Up Your Java Project
IDE에서 새 Java 프로젝트를 만들고 Aspose.PSD JAR 파일을 프로젝트 빌드 경로에 추가합니다.

### Step 2: Import Required Classes
Java 소스 파일 상단에 다음 import 구문을 추가하세요:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

이 클래스들을 통해 이미지 로드, 회전 및 PNG 전용 옵션을 사용할 수 있습니다.

### Step 3: Define File Paths
소스 PSD 파일이 위치한 경로와 출력 파일을 저장할 경로를 지정합니다.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** 테스트 단계에서는 절대 경로를 사용해 “파일을 찾을 수 없음” 오류를 방지하세요.

### Step 4: Load the PSD File
PSD 파일을 조작 가능한 객체로 로드합니다.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

이제 `im`은 모든 레이어를 포함한 전체 Photoshop 문서를 나타냅니다.

### Step 5: Rotate the Image (How to rotate PSD)
`RotateFlipType`에서 회전 유형을 선택합니다. 이 예제에서는 270° 회전 후 두 축을 모두 뒤집습니다.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

`Rotate90FlipNone`이나 `Rotate180FlipX`와 같은 다른 값도 자유롭게 실험해 보세요.

### Step 6: Save the Rotated Image as PNG (convert PSD to PNG)
투명도를 유지하도록 PNG 옵션을 설정한 뒤 저장합니다.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

이렇게 생성된 PNG는 레이어 투명도를 유지하므로 웹에서 바로 사용할 수 있습니다.

### Step 7: Save the Modified PSD (optional)
회전이 적용된 새로운 PSD 파일이 필요하다면, 다시 저장합니다.

```java
im.save(psdPath);
```

이제 PNG 미리보기와 업데이트된 PSD 파일을 모두 확보했습니다.

## Common Issues and Solutions
- **File not found:** `dataDir`이 경로 구분자(`/` 또는 `\`)로 끝나는지 확인하세요.  
- **OutOfMemoryError on large PSDs:** JVM 힙 크기를 늘리세요 (`-Xmx2g`).  
- **Transparency lost:** `PngColorType.TruecolorWithAlpha`가 설정되어 있는지 확인하세요; 설정되지 않으면 PNG가 알파 없이 저장됩니다.

## FAQs
### Can I rotate a specific layer in a PSD file?
예, `im.getLayers()`를 순회한 뒤 개별 레이어에 `Layer.rotateFlip()`을 호출하면 됩니다.

### Is there any performance limitation with Aspose.PSD for Java?
대부분의 파일을 효율적으로 처리하지만, 500 MB를 초과하는 매우 큰 PSD는 추가 메모리가 필요할 수 있습니다.

### Is Aspose.PSD free to use?
Aspose는 무료 체험판을 제공하지만, 프로덕션에서는 유료 라이선스가 필요합니다. 테스트용 [temporary license](https://purchase.aspose.com/temporary-license/)를 확인하세요.

### Where can I find detailed documentation?
자세한 문서는 [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

### What if I encounter issues while using Aspose.PSD?
문제가 발생하면 [Aspose Support Forum](https://forum.aspose.com/c/psd/34)에서 도움을 받을 수 있습니다.

## Additional Frequently Asked Questions

**Q: Does converting PSD to PNG preserve layer effects?**  
A: 예, `PngColorType.TruecolorWithAlpha`로 저장하면 대부분의 시각 효과가 PNG에 래스터화됩니다.

**Q: Can I batch‑process multiple PSD files?**  
A: 물론입니다. 디렉터리의 PSD 파일들을 순회하는 루프에 코드를 넣으면 됩니다.

**Q: Is it possible to set PNG compression level?**  
A: `PngOptions` 클래스의 `setCompressionLevel(int)` 메서드를 사용해 압축 수준을 조정할 수 있습니다.

**Q: Do I need to close the image object?**  
A: `PsdImage`는 `Closeable`을 구현하므로 `finally` 블록에서 `im.close()`를 호출하거나 try‑with‑resources를 사용하세요.

**Q: Will the rotated PNG have the same dimensions as the original?**  
A: 90° 또는 270° 회전 시 너비와 높이가 서로 바뀝니다. PNG는 새로운 방향을 반영합니다.

## Conclusion
Aspose.PSD for Java를 활용하면 **PSD를 PNG로 변환**하고 **PSD 레이어를 회전**하는 작업을 몇 줄의 코드만으로 수행할 수 있습니다. 이 방법은 Photoshop이 필요 없게 해 주며 자동화된 워크플로를 가속화하고 이미지 출력에 대한 완전한 제어권을 제공합니다. 직접 프로젝트에 적용해 보고 얼마나 많은 시간을 절약할 수 있는지 확인해 보세요!

---

**Last Updated:** 2025-12-15  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
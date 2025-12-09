---
date: 2025-12-06
description: Aspose.PSD for Java를 사용하여 이미지를 270도 회전하는 방법을 배워보세요. 이 가이드는 PSD 파일을 회전하고,
  이미지를 뒤집으며, PSD를 JPEG로 변환하는 방법을 보여줍니다.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 이미지를 270도 회전하는 방법
url: /ko/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotate Image 270 Degrees with Aspose.PSD for Java

## Introduction

이 **java 이미지 처리 튜토리얼**에서는 Aspose.PSD for Java를 사용하여 **이미지를 270도 회전**하는 방법을 빠르고 안정적으로 알아봅니다. 사진 편집 도구를 만들든, 배치 변환을 자동화하든, PSD 레이어의 방향을 바꾸든, 이 라이브러리를 사용하면 작업이 손쉽습니다. 또한 이미지 플립과 회전된 PSD를 JPEG로 변환하는 과정도 다루어 전체적인 엔드‑투‑엔드 워크플로우를 제공합니다.

## Quick Answers
- **What library handles the rotation?** Aspose.PSD for Java  
- **Which rotation angle does the example use?** 270 degrees  
- **Can I also flip the image?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **How do I save the result?** In the example we save as JPEG using `JpegOptions`  
- **Do I need a license for production?** A valid Aspose.PSD license is required for commercial use  

## What is “rotate image 270 degrees”?
이미지를 270도 회전한다는 것은 시계 방향으로 전체 원의 3/4(또는 반시계 방향으로 90도)만큼 회전하는 것을 의미합니다. 많은 그래픽 편집 상황에서 이 회전은 일련의 변환 후 원래 세로형 레이아웃과 일치합니다.

## Why use Aspose.PSD for this task?
- **Full PSD support** – works with layers, masks, and adjustment objects.  
- **No native Photoshop required** – run on any Java runtime.  
- **Simple API** – a single method call (`rotateFlip`) handles rotation and flipping.  
- **Easy format conversion** – export directly to JPEG, PNG, or other common formats.

## Prerequisites

시작하기 전에 다음이 준비되어 있는지 확인하세요:

- **Aspose.PSD for Java** 라이브러리가 설치되어 있어야 합니다. 전체 API 레퍼런스는 [여기](https://reference.aspose.com/psd/java/)에서 다운로드하고 확인할 수 있습니다.  
- Java 개발 환경(JDK 8 이상)  
- 회전하려는 샘플 PSD 파일. 코드의 `sourceFile` 변수에 파일 경로를 올바르게 지정하세요.

## Import Packages

Aspose.PSD 패키지에서 필요한 클래스를 가져옵니다:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## How to Rotate PSD – Step 1: Load the Image

소스 PSD 파일을 가리키는 `Image` 인스턴스를 생성합니다:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## How to Rotate PSD – Step 2: Rotate the Image 270 Degrees

`RotateFlipType.Rotate270FlipNone`을 사용하여 플립 없이 270도 회전을 수행합니다:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** 이미지 를 수평 또는 수직으로도 플립해야 한다면 `Rotate90FlipX` 또는 `Rotate180FlipY`와 같은 다른 `RotateFlipType`을 선택하면 됩니다.

## How to Rotate PSD – Step 3: Convert PSD to JPEG and Save

회전이 끝난 후 적절한 옵션 클래스를 사용해 **PSD를 JPEG**(또는 다른 지원 형식)로 변환하고 저장합니다:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

`RotatedImage_out.jpg` 파일에는 원본 PSD 내용이 270도 회전된 상태로 JPEG 형식으로 저장됩니다.

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Image appears upside‑down** | Verify you used `Rotate270FlipNone`. For a 90‑degree clockwise rotation use `Rotate90FlipNone`. |
| **Output file is corrupted** | Ensure the destination folder exists and you have write permissions. |
| **License exception** | Install a temporary or permanent Aspose.PSD license before loading the image in production. |

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with different image formats?**  
A: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, and many other raster formats.

**Q: Can I apply custom rotations, not just predefined flips?**  
A: Absolutely! While `RotateFlipType` provides common angles, you can combine multiple calls or use transformation matrices for arbitrary angles.

**Q: How do I convert the rotated PSD to another format, such as PNG?**  
A: Replace `JpegOptions` with `PngOptions` (or the appropriate options class) in the `save` method.

**Q: Where can I find additional support or assistance?**  
A: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Is there a free trial available?**  
A: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).

**Q: How do I obtain a temporary license?**  
A: If you need a temporary license, you can obtain one [here](https://purchase.aspose.com/temporary-license/).

## Conclusion

이제 Aspose.PSD for Java를 사용해 **이미지를 270도 회전**하고, 필요 시 이미지를 플립하며, 결과를 JPEG로 내보내는 방법을 배웠습니다. 이 간단한 워크플로우는 더 큰 Java 기반 이미지 처리 파이프라인에 쉽게 통합될 수 있어, Photoshop에 의존하지 않고도 PSD 조작을 완벽히 제어할 수 있습니다.

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
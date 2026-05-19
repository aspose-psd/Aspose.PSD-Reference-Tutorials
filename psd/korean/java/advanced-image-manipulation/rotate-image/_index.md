---
date: 2026-05-19
description: Aspose.PSD for Java를 사용하여 PSD를 JPEG로 변환하고 이미지를 270도 회전하는 방법을 배웁니다. 이
  가이드는 PSD 파일을 회전하고, 이미지를 뒤집으며, PSD를 JPEG로 변환하는 방법을 보여줍니다.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: 이미지 270도 회전
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD를 JPEG로 변환하고 270° 회전
url: /ko/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD를 JPEG로 변환하고 이미지 270도 회전

## 소개

이 **Java 이미지 처리 튜토리얼**에서는 Aspose.PSD for Java를 사용하여 이미지를 270도 회전하면서 **PSD를 JPEG로 변환**하는 방법을 배웁니다. 배치 처리 파이프라인, 웹 기반 편집기 또는 데스크톱 유틸리티를 구축하든, 이 라이브러리를 사용하면 Photoshop 없이도 PSD 레이어를 조작할 수 있습니다. 또한 선택적인 플리핑에 대해서도 다루고, PSD 파일을 로드하여 JPEG로 저장하는 전체 엔드‑투‑엔드 흐름을 보여드립니다.

## 빠른 답변
- **회전을 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java  
- **예제에서 사용하는 회전 각도는 무엇인가요?** 270 degrees  
- **이미지를 플립할 수도 있나요?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **결과를 어떻게 저장하나요?** In the example we save as JPEG using `JpegOptions`  
- **프로덕션에 라이선스가 필요합니까?** A valid Aspose.PSD license is required for commercial use  

## “이미지 270도 회전”이란 무엇인가요?
이미지를 270도 회전한다는 것은 그림을 시계 방향으로 전체 원의 3/4(또는 반시계 방향으로 90도)만큼 돌리는 것을 의미합니다. 이 방향은 이전 변환 후 원래의 세로 레이아웃을 복원하는 경우가 많으며, 풍경 모드로 촬영된 이미지를 세로로 표시해야 할 때 일반적으로 사용됩니다. 결과는 품질 손실 없이 올바르게 방향이 맞춰진 시각적 이미지입니다.

## 이 작업에 Aspose.PSD를 사용하는 이유는 무엇인가요?
Aspose.PSD는 **50개 이상의 입력 및 출력 포맷**을 지원합니다—PSD, JPEG, PNG, BMP, GIF, TIFF 등을 포함하며, **2 GB**까지의 파일을 전체 문서를 메모리에 로드하지 않고 처리할 수 있습니다. API는 모든 Java 런타임(JDK 8+)에서 작동하며, 별도의 Photoshop 설치가 필요 없고, 회전과 플리핑을 한 번에 처리하는 단일 `rotateFlip` 호출을 제공합니다.

## 전제 조건

시작하기 전에 다음이 설치되어 있는지 확인하십시오:

- **Aspose.PSD for Java** 라이브러리가 설치되어 있어야 합니다. 전체 API 레퍼런스는 [here](https://reference.aspose.com/psd/java/)에서 다운로드하고 확인할 수 있습니다.  
- Java 개발 환경(JDK 8 이상).  
- 회전하려는 샘플 PSD 파일. 코드의 `sourceFile` 변수를 파일의 올바른 경로로 업데이트하십시오.

## 패키지 가져오기

`Image`, `RotateFlipType`, `JpegOptions` 클래스는 파일을 로드하고 변환하며 저장하는 데 필요합니다.  
`Image`는 메모리 내에서 PSD 문서를 나타내는 핵심 클래스입니다.  
`RotateFlipType`은 지원되는 회전 및 플립 작업을 열거합니다.  
`JpegOptions`는 품질과 같은 JPEG 출력 설정을 구성합니다.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 회전 후 PSD를 JPEG로 변환하는 방법은?

소스 PSD를 로드하고 270도 회전을 적용한 뒤 즉시 JPEG로 저장합니다. 이 3단계 흐름은 최신 CPU에서 일반적인 10MP 이미지의 경우 1초 미만에 실행되어 고처리량 배치 작업에 이상적입니다. 필요한 이미지 데이터만 처리함으로써 메모리 사용량이 낮게 유지되고, 결과 JPEG는 파일 크기를 줄이면서 시각적 품질을 유지합니다.

### 단계 1: PSD 파일 로드

`Image`는 메모리 내에서 단일 PSD 문서를 나타내는 Aspose.PSD의 핵심 클래스입니다. 인스턴스를 생성하면 헤더 정보만 읽어 메모리 사용량을 낮게 유지합니다.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### 단계 2: 이미지 270도 회전

`rotateFlip`은 지정된 회전 및 선택적인 플립을 이미지에 적용합니다. `RotateFlipType.Rotate270FlipNone`은 캔버스를 시계 방향으로 270도 회전시키며 이미지 방향은 변경하지 않습니다.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** 이미지 를 가로 또는 세로로 플립해야 하는 경우 `Rotate90FlipX` 또는 `Rotate180FlipY`와 같은 다른 `RotateFlipType`을 선택하십시오.

### 단계 3: PSD를 JPEG로 변환하고 저장

`JpegOptions`는 압축 품질과 같은 JPEG 전용 매개변수를 정의합니다. `save` 메서드는 변환된 이미지를 원하는 형식으로 디스크에 기록합니다.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

`RotatedImage_out.jpg` 파일에는 원본 PSD 내용이 270도 회전된 후 JPEG로 저장된 이미지가 들어 있습니다.

## 일반적인 문제와 해결책

| 문제 | 해결책 |
|-------|----------|
| **이미지가 뒤집혀 보임** | `Rotate270FlipNone`를 사용했는지 확인하십시오. 시계 방향 90도 회전은 `Rotate90FlipNone`을 사용합니다. |
| **출력 파일이 손상됨** | 대상 폴더가 존재하고 쓰기 권한이 있는지 확인하십시오. |
| **라이선스 예외** | 프로덕션에서 이미지를 로드하기 전에 임시 또는 영구 Aspose.PSD 라이선스를 설치하십시오. |

## 자주 묻는 질문

**Q: Aspose.PSD가 다양한 이미지 포맷과 호환되나요?**  
A: 예, Aspose.PSD는 PSD, JPEG, PNG, BMP, GIF, TIFF 및 기타 많은 래스터 포맷을 지원합니다.

**Q: 미리 정의된 플립이 아니라 사용자 지정 회전을 적용할 수 있나요?**  
A: 물론 가능합니다! `RotateFlipType`이 일반적인 각도를 제공하지만, 여러 호출을 연결하거나 변환 행렬을 사용하여 임의의 각도를 적용할 수 있습니다.

**Q: 회전된 PSD를 PNG와 같은 다른 포맷으로 변환하려면 어떻게 해야 하나요?**  
A: `save` 메서드에서 `JpegOptions`를 `PngOptions`(또는 해당 옵션 클래스)로 교체하십시오.

**Q: 추가 지원이나 도움을 어디서 찾을 수 있나요?**  
A: 커뮤니티 도움을 위해 [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) 을 방문하십시오.

**Q: 무료 체험판이 있나요?**  
A: 예, [free trial](https://releases.aspose.com/)을 통해 Aspose.PSD를 체험할 수 있습니다.

**Q: 임시 라이선스를 어떻게 얻을 수 있나요?**  
A: 임시 라이선스가 필요하면 [here](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

---

**마지막 업데이트:** 2026-05-19  
**테스트 환경:** Aspose.PSD for Java 24.12  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.PSD for Java를 사용하여 PSD를 래스터 이미지 포맷으로 변환](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Java를 사용하여 PSD를 PNG로 변환하고 PSD 파일의 레이어를 회전](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Aspose.PSD를 사용하여 Java에서 이미지 회전하는 방법](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
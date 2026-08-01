---
date: 2026-08-01
description: Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 압축되지 않은 이미지 스트림을 처리하는 방법을 배웁니다.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: PSD에서 압축되지 않은 이미지 스트림 객체 처리 - Java
og_description: Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보냅니다. 압축되지 않은 이미지 스트림을 처리하고,
  그래픽 객체를 생성하며, 고품질 PNG를 저장하는 방법을 배웁니다.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: PSD를 PNG로 내보내기 – 압축되지 않은 PSD 스트림을 위한 Java 가이드
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: PSD를 PNG로 내보내기 – PSD 그래픽 객체 생성 – Java에서 압축되지 않은 스트림
url: /ko/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 PNG로 내보내기 – PSD 그래픽스 객체 생성 – Java에서 비압축 스트림

## 소개
이 단계별 가이드에서는 Aspose.PSD for Java를 사용하여 비압축 이미지 스트림으로 작업하면서 **PSD를 PNG로 내보내기**를 수행합니다. 디자인 파이프라인을 자동화하거나 맞춤형 편집기를 구축하든, 품질 손실 없이 Photoshop 파일을 렌더링할 수 있는 능력은 필수적입니다. 필요한 설정부터 시작하여 `Graphics` 객체 생성 과정을 살펴보고 무손실 PNG 내보내기로 마무리합니다. 끝까지 읽으면 Aspose.PSD가 원시 스트림을 효율적으로 처리하는 이유와 이를 모든 Java 프로젝트에 통합하는 방법을 이해하게 됩니다.

## 빠른 답변
- **“create PSD graphics object”가 무엇을 의미하나요?** 이는 프로그래밍 방식으로 PSD 이미지를 그리거나 수정할 수 있는 `Graphics` 컨텍스트를 인스턴스화하는 것을 의미합니다.  
- **어떤 라이브러리가 비압축 스트림을 처리하나요?** Aspose.PSD for Java는 원시(비압축) 이미지 데이터를 완벽히 지원합니다.  
- **편집 후 PSD를 PNG로 내보낼 수 있나요?** 예—`Graphics` 객체가 있으면 PSD를 렌더링하고 한 번의 호출로 PNG로 저장할 수 있습니다.  
- **개발에 라이선스가 필요합니까?** 무료 체험판으로 테스트가 가능하지만, 실제 배포에는 상업용 라이선스가 필요합니다.  
- **내보내기가 무손실인가요?** PNG로 내보내면 원본 픽셀 데이터를 보존하여 원시 PSD보다 파일 크기는 작지만 무손실 품질을 제공합니다.

## PSD를 PNG로 내보내는 것이란?
PSD를 PNG로 내보내면 레이어가 있는 Photoshop 문서를 단일 레이어의 무손실 래스터 이미지로 변환하여 모든 웹 브라우저나 이미지 뷰어에서 표시할 수 있습니다. 이 과정은 투명도, 색 깊이 및 레이어 효과를 유지하면서 Photoshop 전용 메타데이터는 제외합니다. 또한 정확한 색 재현을 위해 원본 색 프로필을 보존합니다.

## 이미지 조작을 위해 Aspose.PSD for Java를 사용하는 이유는?
Aspose.PSD는 **50개 이상의** 입력 및 출력 포맷을 지원합니다—PSD, PNG, JPEG, BMP, TIFF 등을 포함하며, 전체 문서를 메모리에 로드하지 않고도 **200개 이상의 레이어**가 있는 파일을 처리할 수 있습니다. `Raw` 압축 옵션은 픽셀 데이터를 비압축으로 저장하여 후속 편집이나 보관 시 픽셀 완전성을 보장합니다.

## 사전 요구 사항
- **Java Development Kit (JDK)** – JDK 8 이상이 설치되어 있어야 합니다.  
- **Aspose.PSD for Java** – 공식 릴리스 페이지에서 최신 JAR를 다운로드하세요: [Aspose.PSD Java 다운로드](https://releases.aspose.com/psd/java/). 또한 [이 링크](https://releases.aspose.com/psd/java/) 또는 [릴리스 페이지](https://releases.aspose.com/psd/java/)에서도 접근할 수 있습니다. 다른 Aspose 제품은 [여기](https://releases.aspose.com/)를 클릭하세요.  
- **IDE** – IntelliJ IDEA, Eclipse 또는 Java와 호환되는 편집기.  
- **기본 Java 지식** – 클래스, 메서드 및 예외 처리에 익숙함.

위 사항이 준비되면 코딩을 시작할 준비가 된 것입니다.

## 패키지 가져오기
`Graphics` 클래스는 Aspose.PSD의 그리기 표면으로, 픽셀 데이터를 직접 렌더링하거나 편집할 수 있게 해줍니다. `PsdImage` 클래스는 메모리 내 PSD 파일을 나타내며, `PsdOptions`는 이미지 저장 방식을 제어합니다.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

이제 코드를 이해하기 쉬운 단계로 나누어 보겠습니다. 환경을 설정하고, PSD 파일을 로드하고, 조작한 뒤 최종적으로 출력을 저장합니다.

## 단계 1: 문서 디렉터리 정의
파일 작업을 수행하기 전에 프로그램에 PSD 자산이 위치한 디렉터리를 알려야 합니다. 이 디렉터리 경로는 튜토리얼 전반에 걸쳐 사용됩니다.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"`를 `layers.psd`가 포함된 절대 경로로 교체하세요. 경로를 구성 가능하게 유지하면 프로젝트 간에 코드를 재사용할 수 있습니다.

## 단계 2: ByteArrayOutputStream 생성
`ByteArrayOutputStream`은 데이터를 바이트 배열 형태로 메모리에 보관하는 Java 스트림입니다. 수정된 이미지를 메모리 버퍼로 사용하여 디스크에 쓰거나 네트워크로 전송하기 전에 원시 바이트를 캡처할 수 있게 합니다.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

`ms` 변수는 `save` 작업 후 비압축 이미지 데이터를 보관하게 됩니다.

## 단계 3: PSD 파일 로드
`PsdImage` 클래스는 PSD 파일을 메모리로 로드하여 조작할 수 있게 합니다. 파일을 로드하면 디스크에 있는 PSD가 `PsdImage` 객체로 변환되어 조작이 가능해집니다. 이 단계에서 Aspose.PSD는 파일 헤더, 레이어 및 리소스를 읽습니다.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

경로가 올바르지 않으면 Aspose.PSD가 `FileNotFoundException`을 발생시키며, 이는 실제 코드에서 예외 처리해야 합니다.

## 단계 4: 저장을 위한 PsdOptions 설정
`PsdOptions`는 PSD 파일 저장 매개변수를 지정합니다. 압축 방식을 `Raw`로 설정하면 픽셀 데이터를 압축 없이 저장하여 메모리에 나타나는 그대로 모든 픽셀을 보존합니다.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

`CompressionMethod.Raw` 옵션은 픽셀 데이터를 전혀 압축하지 않고 저장하므로, 이후에 추가 편집을 할 계획이 있을 때 이상적입니다.

## 단계 5: 이미지를 출력 스트림에 저장
이제 앞서 만든 `ByteArrayOutputStream`에 PSD(수정 사항 포함)를 저장합니다. `save` 메서드는 설정한 `PsdOptions`를 준수합니다.

```java
psdImage.save(ms, saveOptions);
```

이 시점에서 `ms`는 비압축 PSD의 전체 바이너리 표현을 포함합니다.

## 단계 6: 출력 스트림 재설정
쓰기 후 스트림 내부 포인터가 끝에 위치합니다. 이를 재설정하면 스트림을 처음부터 읽을 수 있도록 되감습니다.

```java
ms.reset();
```

재생 전에 테이프 헤드를 시작 위치로 되돌리는 것과 같습니다.

## 단계 7: 새로 만든 이미지 로드
이제 바이트 배열에서 새로운 `PsdImage` 인스턴스를 직접 생성할 수 있습니다. 이 단계는 저장된 데이터가 손상 없이 다시 로드될 수 있음을 확인합니다.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

이미지가 성공적으로 로드되면 비압축 스트림이 올바르게 기록된 것을 알 수 있습니다.

## 단계 8: Graphics 객체 생성
`Graphics` 클래스는 Aspose.PSD의 그리기 캔버스입니다. `PsdImage`의 픽셀 매트릭스에 직접 도형, 텍스트 및 필터를 적용하는 메서드를 제공합니다.

```java
Graphics graphics = new Graphics(psdImage);
```

이 `Graphics` 인스턴스를 사용하면 새 콘텐츠를 그리거나, 일부를 지우거나, 추가 레이어를 합성할 수 있습니다.

## Aspose.PSD for Java를 사용해 PSD를 PNG로 내보내는 방법은?
`new PsdImage(dataDir + "layers.psd")`로 PSD를 로드하고, `Graphics` 객체를 생성한 뒤 필요한 그리기를 수행합니다. 그런 다음 `psdImage.save("output.png", new PngOptions())`를 호출합니다. 이 순서는 편집된 PSD를 렌더링하고 단일 단계로 무손실 PNG를 작성하며, Aspose.PSD의 내장 변환 엔진을 활용합니다.

## Graphics 객체로 PSD 레이어 조작하기
`Graphics` 인스턴스를 사용하면 각 레이어에 대해 픽셀 수준의 제어가 가능합니다. 기하학적 도형을 그리거나, 텍스트를 렌더링하거나, 사용자 정의 필터를 적용할 수 있습니다. 그래픽 컨텍스트가 레이어의 래스터화된 뷰에서 작동하기 때문에, 이미지를 저장하면 변경 사항이 즉시 반영됩니다.

## 일반적인 문제와 해결책
- **파일 로드 시 NullPointerException** – `dataDir` 경로를 다시 확인하고 파일 이름이 대소문자를 포함해 정확히 일치하는지 확인하세요.  
- **Raw 사용에도 불구하고 압축된 출력** – `saveOptions.setCompressionMethod(CompressionMethod.Raw);`가 `save` 호출 **이전에** 호출되었는지 확인하세요.  
- **Graphics 객체가 빈 화면** – 올바른 `PsdImage` 인스턴스(로드한 이미지)에서 그리고 있는지, 새로 만든 빈 이미지가 아닌지 확인하세요.  
- **대용량 파일에서 OutOfMemoryError** – `PsdImage.load(dataDir, LoadOptions)`와 `loadOptions.setLoadMode(LoadMode.Memory)`를 사용하여 전체 문서를 RAM에 로드하지 않고 스트리밍하도록 하세요.

## FAQ

### Aspose.PSD란?
Aspose.PSD는 개발자가 Adobe Photoshop 없이도 프로그래밍 방식으로 Photoshop PSD 파일을 생성, 편집 및 변환할 수 있게 해주는 Java 라이브러리입니다. PSD 파일의 읽기·쓰기, 레이어·마스크·채널·다양한 이미지 리소스 처리를 지원하며, 래스터 및 벡터 작업을 위한 API를 제공해 서버‑사이드 이미지 처리 및 자동화 작업에 적합합니다.

### Aspose.PSD for Java를 어떻게 다운로드하나요?
공식 릴리스 페이지에서 다운로드할 수 있습니다: [Aspose.PSD Java 다운로드](https://releases.aspose.com/psd/java/).

### Aspose.PSD의 무료 체험판이 있나요?
예, 동일한 다운로드 페이지에서 완전 기능을 갖춘 체험판을 제공하며, 개발 및 평가 목적으로 사용할 수 있습니다.

### Aspose.PSD에 대한 지원을 받을 수 있나요?
물론입니다! Aspose 지원 포럼에서는 제품 팀과 커뮤니티가 답변을 제공합니다: [Aspose 지원 포럼](https://forum.aspose.com/c/psd/34).

### Aspose.PSD의 임시 라이선스를 어떻게 얻나요?
임시 라이선스는 Aspose 라이선스 포털에서 직접 요청할 수 있으며, 30일 유효한 제한된 키를 제공합니다. 이를 통해 상용 라이선스를 구매하지 않고도 Aspose.PSD의 전체 기능을 평가할 수 있습니다. 체험 기간이 끝난 후에는 임시 키를 영구 라이선스로 교체해야 프로덕션에서 라이브러리를 계속 사용할 수 있습니다. 제한된 키를 생성하려면 임시 라이선스 페이지를 방문하세요: [임시 라이선스 페이지](https://purchase.aspose.com/temporary-license/).

## 자주 묻는 질문

- **그래픽스 객체를 사용해 특정 레이어만 편집할 수 있나요?**  
  예. PSD를 로드한 후 `psdImage.getLayers().get_Item(index)`를 사용해 원하는 레이어를 가져와 `Graphics` 생성자에 전달하면 해당 레이어만 편집할 수 있습니다.

- **Raw 압축 방식은 파일 크기에 영향을 미치나요?**  
  `Raw` 압축 방식은 픽셀 데이터를 전혀 압축하지 않으므로, 결과 파일은 압축된 PSD보다 크지만 100 % 픽셀 정확성을 보장합니다.

- **편집된 PSD를 다른 포맷(e.g., PNG)으로 내보낼 수 있나요?**  
  물론입니다. 편집 후 `psdImage.save("output.png", new PngOptions())`를 호출하면 무손실 품질로 **PSD를 PNG로 내보내기**하는 표준 방법이 됩니다.

- **어떤 Java 버전이 필요합니까?**  
  Aspose.PSD for Java는 JDK 8 이상을 지원하며, JDK 21까지 모든 LTS 릴리스를 포함합니다.

- **처리 후 리소스를 해제하려면 어떻게 해야 하나요?**  
  `psdImage.dispose()`를 호출하고 모든 스트림(e.g., `ms.close()`)을 닫아 네이티브 메모리를 해제하고 누수를 방지하세요.

**마지막 업데이트:** 2026-08-01  
**테스트 환경:** Aspose.PSD for Java (최신 릴리스)  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.PSD for Java로 이미지 스트림에 저장하기](/psd/java/advanced-techniques/save-images-to-stream/)
- [Java를 사용해 PSD 레이어 그룹을 이미지로 내보내기](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Aspose.PSD for Java에서 스트림을 사용해 이미지 만들기](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
---
date: 2026-02-17
description: Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 압축되지 않은 이미지 스트림을 처리하는 방법을 배우세요.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: PSD를 PNG로 내보내기 – PSD 그래픽 객체 생성 – Java에서 비압축 스트림
url: /ko/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 PNG로 내보내기 – PSD 그래픽 객체 생성 – Java에서 압축되지 않은 스트림

## 소개
Java에서 이미지 조작의 세계에 오신 것을 환영합니다! 이 튜토리얼에서는 **PSD 그래픽 객체를 생성**하고, 압축되지 않은 이미지 스트림 객체를 처리하며, Aspose.PSD for Java를 사용하여 **PSD를 PNG로 내보내는 방법**을 배웁니다. 워크플로를 자동화하려는 그래픽 디자이너이든, 강력한 이미지‑처리 기능을 애플리케이션에 통합하려는 소프트웨어 개발자이든, 이 가이드는 여러분을 위해 맞춤 제작되었습니다. 전제 조건부터 최종 내보내기까지 모든 과정을 단계별로 안내하여 전체 프로세스를 확실히 이해할 수 있도록 도와드립니다.

## 빠른 답변
- **“PSD 그래픽 객체를 생성”한다는 의미는 무엇인가요?** PSD 파일에 대한 그래픽 컨텍스트를 인스턴스화하여 내용에 그리기 또는 편집을 할 수 있게 하는 것을 의미합니다.  
- **어떤 라이브러리가 압축되지 않은 스트림을 처리하나요?** Aspose.PSD for Java는 원시(압축되지 않은) 이미지 데이터에 대한 완전한 지원을 제공합니다.  
- **편집 후 PSD를 PNG로 내보낼 수 있나요?** 네—`Graphics` 객체가 있으면 PSD를 렌더링하고 PNG로 저장할 수 있습니다.  
- **개발에 라이선스가 필요합니까?** 무료 체험판으로 테스트가 가능하며, 상용 환경에서는 상업용 라이선스가 필요합니다.  
- **내보내기가 무손실인가요?** PNG로 내보내면 이미지 품질이 유지되며, 파일 크기는 JPEG보다 크지만 압축되지 않은 PSD보다는 작습니다.  

## Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내는 방법
**PSD를 PNG로 내보내야** 할 때 일반적인 워크플로는 다음과 같습니다:

1. PSD 파일을 로드하거나 새로 생성합니다.  
2. `Graphics` 객체를 사용해 원하는 그리기 또는 레이어 조작을 수행합니다.  
3. `PngOptions`를 사용해 결과 이미지를 저장합니다 (`Graphics` 인스턴스를 재사용할 수 있습니다).  

이 튜토리얼은 압축되지 않은 스트림 처리에 중점을 두지만, 생성한 동일한 `Graphics` 객체를 나중에 파이프라인에서 PSD를 PNG 파일로 렌더링하는 데 재사용할 수 있습니다.

## 전제 조건
코드 작성을 시작하기 전에 이 여정을 시작하는 데 필요한 모든 것이 준비되어 있는지 확인해 보세요. 전제 조건은 다음과 같습니다:

### Java Development Kit (JDK)
머신에 JDK가 설치되어 있는지 확인하세요. Oracle 웹사이트에서 다운로드하거나 OpenJDK를 사용할 수 있습니다.

### Aspose.PSD for Java
Aspose.PSD 라이브러리를 다운로드하고 설치해야 합니다. 이 강력한 라이브러리를 통해 PSD 파일을 손쉽게 조작할 수 있습니다. 최신 버전은 [this link](https://releases.aspose.com/psd/java/)에서 받을 수 있습니다.

### Integrated Development Environment (IDE)
Java 코드를 작성하고 테스트하려면 IDE를 사용하는 것이 좋습니다. IntelliJ IDEA, Eclipse 또는 선호하는 다른 IDE를 사용할 수 있습니다.

### Basic Understanding of Java
Java 프로그래밍에 대한 기본 지식이 있으면 과정이 더 원활합니다. 클래스, 메서드, 예외 처리와 같은 기본 개념을 숙지하고 있어야 합니다.

모든 준비가 끝났다면, 소매를 걷어붙이고 흥미진진한 코딩 파트로 들어갑시다!

## 패키지 가져오기
Aspose.PSD와 함께 작업하기 위해 필요한 패키지를 가져와야 합니다. 아래는 일반적으로 PSD 파일을 처리할 때 사용되는 import 구문입니다.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

이제 코드를 소화하기 쉬운 단계로 나누어 따라가기 쉽도록 하겠습니다. 설정, PSD 파일 로드, 조작, 출력 저장 순으로 진행합니다.

## 단계 1: 문서 디렉터리 정의
코딩을 시작하기 전에 PSD 파일이 위치한 디렉터리를 정의해야 합니다. 이는 프로젝트의 기본 설정과 같습니다.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"`를 실제 PSD 파일(예: layers.psd)이 있는 경로로 교체하세요. 이렇게 하면 파일을 손쉽게 찾을 수 있습니다.

## 단계 2: ByteArrayOutputStream 생성
수정된 이미지를 저장할 장소가 필요합니다. `ByteArrayOutputStream`을 사용하면 이미지 데이터를 쉽게 캡처할 수 있습니다.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

이 코드는 `ms`라는 이름의 새로운 `ByteArrayOutputStream` 객체를 초기화합니다. 이 객체를 사용해 압축되지 않은 이미지를 저장하게 됩니다.

## 단계 3: PSD 파일 로드
이제 실제 PSD 파일을 로드할 차례입니다. 여기서 마법이 시작됩니다!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

이 코드는 PSD 파일을 `PsdImage` 객체에 로드합니다. 경로가 올바른지 확인하지 않으면 오류가 발생합니다.

## 단계 4: 저장을 위한 PsdOptions 설정
이미지를 어떻게 저장할지 지정해야 합니다—당연히 압축되지 않은 형태로!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

여기서 `PsdOptions` 객체를 생성하고 압축 방식을 `Raw`로 설정합니다. 이 방식은 이미지가 완전한 품질을 유지하면서 압축 없이 저장되도록 합니다.

## 단계 5: 이미지를 출력 스트림에 저장
```java
psdImage.save(ms, saveOptions);
```

이 코드는 2단계에서 만든 `ByteArrayOutputStream`에 수정된 이미지를 저장합니다. `save` 메서드는 설정에 따라 이미지를 올바르게 인코딩합니다.

## 단계 6: 출력 스트림 재설정
저장 후 출력 스트림은 끝에 위치합니다. 처음부터 읽을 수 있도록 재설정해야 합니다.

```java
ms.reset();
```

`reset` 메서드는 `ByteArrayOutputStream`을 처음부터 다시 읽을 수 있게 준비합니다. 마치 테이프를 되감아 좋아하는 노래를 듣는 것과 같습니다!

## 단계 7: 새로 만든 이미지 로드
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

여기서는 `ByteArrayOutputStream`에서 이미지를 다시 읽어 새로운 `PsdImage` 객체에 로드합니다. 이전 작업 결과를 확인할 수 있는 단계입니다.

## 단계 8: Graphics 객체 생성
이미지를 추가로 수정하거나 렌더링하려면 graphics 객체가 필요합니다.

```java
Graphics graphics = new Graphics(psdImage);
```

이 코드는 `psdImage`를 사용해 `Graphics` 객체를 초기화합니다. 이제 이 graphics 객체를 이용해 그림을 그리거나 이미지를 조작할 수 있습니다. 마치 손에 붓을 든 것과 같습니다!

## Graphics 객체로 PSD 레이어 조작
`Graphics` 인스턴스를 확보했으니 **PSD 레이어를 조작**할 수 있습니다—예를 들어 도형을 그리거나 텍스트를 추가하거나 특정 레이어에 필터를 적용하는 식입니다. graphics 컨텍스트는 기본 픽셀 데이터에 직접 작용하므로 각 레이어의 외관을 세밀하게 제어할 수 있습니다.

## 일반적인 문제 및 해결책
- **파일 로드 시 NullPointerException** – `dataDir` 경로와 파일 이름이 정확한지 다시 확인하세요.  
- **Raw 사용에도 압축된 출력이 나옴** – `save` 메서드 호출 전에 `saveOptions.setCompressionMethod(CompressionMethod.Raw);`가 실행됐는지 확인하세요.  
- **Graphics 객체가 빈 화면을 표시** – 올바른 `PsdImage` 인스턴스(로드한 이미지)를 사용했는지 확인하고, 새로 만든 이미지가 아니라면 해당 인스턴스를 사용하세요.

## FAQ
### Aspose.PSD란?
Aspose.PSD는 개발자가 프로그래밍 방식으로 Photoshop PSD 파일 및 관련 이미지 형식을 생성, 편집 및 조작할 수 있게 해 주는 .NET 라이브러리입니다.

### Aspose.PSD for Java를 어떻게 다운로드하나요?
[release page](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

### Aspose.PSD의 무료 체험판이 있나요?
네, [here](https://releases.aspose.com/)에서 무료 체험 버전을 받을 수 있습니다.

### Aspose.PSD에 대한 지원을 받을 수 있나요?
물론입니다! [Aspose support forum](https://forum.aspose.com/c/psd/34)에서 도움을 받을 수 있습니다.

### Aspose.PSD의 임시 라이선스를 어떻게 얻나요?
시작하려면 [temporary license page](https://purchase.aspose.com/temporary-license/)를 방문하세요.

## 자주 묻는 질문

**Q: Graphics 객체를 사용해 특정 레이어 하나만 편집할 수 있나요?**  
A: 네. PSD를 로드한 후 `psdImage.getLayers().get_Item(index)` 로 원하는 레이어를 선택하고 해당 레이어를 `Graphics` 생성자에 전달하면 됩니다.

**Q: Raw 압축 방식이 파일 크기에 영향을 미치나요?**  
A: Raw는 픽셀 데이터를 압축 없이 저장하므로 파일 크기가 압축된 PSD보다 크게 되지만, 이미지 품질은 전혀 손상되지 않습니다.

**Q: 편집된 PSD를 다른 형식(예: PNG)으로 내보낼 수 있나요?**  
A: 물론 가능합니다. 편집 후 `Image.save` 메서드에 `PngOptions`를 지정하면 **PSD를 PNG로 내보내기**가 표준 방식으로 수행됩니다.

**Q: 필요한 Java 버전은 무엇인가요?**  
A: Aspose.PSD for Java는 JDK 8 이상을 지원합니다.

**Q: 처리 후 리소스를 어떻게 해제하나요?**  
A: `psdImage.dispose()` 를 호출하고 모든 스트림을 닫아 네이티브 리소스를 해제합니다.

**마지막 업데이트:** 2026-02-17  
**테스트 대상:** Aspose.PSD for Java (latest release)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
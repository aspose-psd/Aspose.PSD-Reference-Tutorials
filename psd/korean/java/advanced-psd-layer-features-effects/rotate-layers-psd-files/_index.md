---
date: 2026-02-17
description: Aspose.PSD를 사용하여 Java에서 PSD를 PNG로 변환하고 PNG 투명성을 유지하며 PSD 레이어를 회전하는 방법을
  배웁니다. 코드 샘플이 포함된 단계별 가이드.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Java를 사용하여 PSD를 PNG로 변환하고 PSD 파일의 레이어 회전
url: /ko/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

codes unchanged.

Now produce final content.

Be careful with markdown formatting.

Let's craft final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 PNG로 변환하고 PSD 파일의 레이어 회전하기 (Java 사용)

## 소개
레이어를 회전하면서 **PSD를 PNG로 변환**해야 한다면 이 가이드가 적합합니다. 배치 처리 도구를 만들거나, 실시간 이미지 조작이 필요한 웹 서비스를 구축하거나, 디자인 워크플로우를 자동화하려는 경우, 프로그래밍 방식으로 수행하면 시간을 절약하고 Adobe Photoshop에 대한 의존성을 없앨 수 있습니다. 이 튜토리얼에서는 Aspose.PSD for Java 라이브러리를 사용하여 **PSD 레이어를 회전**하고 결과를 PNG로 내보내는 방법을 단계별로 살펴보겠습니다. 이제 팔을 걷어붙이고 디자인 워크플로우를 원활하게 실행해 보세요!

## 빠른 답변
- **어떤 라이브러리를 사용할 수 있나요?** Aspose.PSD for Java  
- **한 번에 회전과 변환을 모두 할 수 있나요?** 예 – PSD를 회전한 뒤 PNG로 저장  
- **라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있으며, 프로덕션에서는 유료 라이선스가 필요합니다  
- **지원되는 Java 버전은?** Java 8 이상  
- **PNG 출력이 투명합니까?** `PngColorType.TruecolorWithAlpha`를 설정하면 투명합니다  

## “PSD를 PNG로 변환”이란 무엇인가요?
Photoshop 문서(PSD)를 PNG 이미지로 변환한다는 것은 시각적 콘텐츠—모든 레이어, 마스크, 투명도—를 널리 지원되는 래스터 형식으로 추출하는 것을 의미합니다. PNG는 알파 채널을 보존하므로 웹 그래픽, 썸네일 및 추가 이미지 처리에 이상적입니다.

## 왜 Aspose.PSD for Java를 사용해 PSD를 PNG로 변환하고 PSD 레이어를 회전하나요?
- **Photoshop 불필요** – 모든 서버 또는 CI 환경에서 작동  
- **전체 레이어 지원** – 투명도와 레이어 효과를 그대로 유지  
- **간단한 API** – 몇 번의 메서드 호출만으로 회전, 뒤집기 및 저장  
- **크로스 플랫폼** – Windows, Linux, macOS에서 실행  
- **Java 이미지 변환**을 단일 라이브러리로 손쉽게  

## 사전 요구 사항
- **Java Development Kit (JDK)** – [Oracle 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html)에서 다운로드하십시오.  
- **통합 개발 환경 (IDE)** – IntelliJ IDEA, Eclipse, NetBeans 모두 사용 가능합니다.  
- **Aspose.PSD for Java 라이브러리** – 최신 JAR 파일은 [릴리스 페이지](https://releases.aspose.com/psd/java/)에서 받으세요.  
- **기본 Java 지식** – 클래스, 객체, 예외 처리에 익숙해야 합니다.

## 단계별 가이드

### 단계 1: Java 프로젝트 설정
IDE에서 새 Java 프로젝트를 만들고 Aspose.PSD JAR를 프로젝트의 빌드 경로에 추가합니다.

### 단계 2: 필요한 클래스 가져오기
Java 소스 파일 상단에 다음 import 문을 추가합니다:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

이 클래스들을 통해 이미지 로드, 회전 및 PNG 전용 옵션에 접근할 수 있습니다.

### 단계 3: 파일 경로 정의
소스 PSD 파일이 위치한 경로와 출력 파일을 저장할 위치를 지정합니다.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** 테스트 중에는 절대 경로를 사용하여 “file not found” 오류를 방지하세요.

### 단계 4: PSD 파일 로드
PSD를 조작 가능한 객체로 로드합니다.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

이제 `im`은 모든 레이어를 포함한 전체 Photoshop 문서를 나타냅니다.

### 단계 5: 이미지 회전 (PSD 회전 방법)
`RotateFlipType`에서 회전 유형을 선택합니다. 이 예제에서는 270° 회전하고 두 축을 모두 뒤집습니다.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

`Rotate90FlipNone`이나 `Rotate180FlipX`와 같은 다른 값을 자유롭게 실험해 보세요. 이것이 튜토리얼의 **PSD 회전 방법** 부분입니다.

### 단계 6: 회전된 이미지를 PNG로 저장 (PSD를 PNG로 변환)
투명도를 유지하도록 PNG 옵션을 설정한 뒤 저장합니다.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

결과 PNG는 레이어 투명도를 유지하여 **PNG 투명성 보존**을 보장합니다.

### 단계 7: 수정된 PSD 저장 (선택 사항)
회전이 적용된 새로운 PSD가 필요하다면 다시 저장합니다.

```java
im.save(psdPath);
```

이제 PNG 미리보기와 업데이트된 PSD 파일을 모두 보유하게 됩니다.

## 일반적인 문제 및 해결책
- **File not found:** `dataDir`이 경로 구분자(`/` 또는 `\`)로 끝나는지 확인하세요.  
- **OutOfMemoryError on large PSDs:** JVM 힙 크기(`-Xmx2g`)를 늘리세요.  
- **Transparency lost:** `PngColorType.TruecolorWithAlpha`가 설정되어 있는지 확인하세요; 그렇지 않으면 PNG가 알파 없이 저장됩니다.  
- **Flip PSD image not behaving as expected:** 선택한 `RotateFlipType` 상수를 다시 확인하세요; 일부 상수는 회전과 뒤집기를 한 단계로 결합합니다.

## 자주 묻는 질문

**Q: PSD 파일의 특정 레이어를 회전할 수 있나요?**  
A: 예, `im.getLayers()`를 순회한 후 개별 레이어에 `Layer.rotateFlip()`을 사용할 수 있습니다.

**Q: Aspose.PSD for Java에 성능 제한이 있나요?**  
A: 대부분의 파일을 효율적으로 처리하지만, 500 MB 이상의 매우 큰 PSD는 추가 메모리가 필요할 수 있습니다.

**Q: Aspose.PSD는 무료로 사용할 수 있나요?**  
A: 무료 체험판을 제공하지만, 프로덕션에서는 유료 라이선스가 필요합니다. 테스트용 [임시 라이선스](https://purchase.aspose.com/temporary-license/)를 확인하세요.

**Q: 자세한 문서는 어디에서 찾을 수 있나요?**  
A: [Aspose.PSD 문서](https://reference.aspose.com/psd/java/)에서 포괄적인 문서를 확인할 수 있습니다.

**Q: Aspose.PSD 사용 중 문제가 발생하면 어떻게 하나요?**  
A: [Aspose 지원 포럼](https://forum.aspose.com/c/psd/34)에서 도움을 요청하세요.

**Q: PSD를 PNG로 변환하면 레이어 효과가 보존되나요?**  
A: 예, `PngColorType.TruecolorWithAlpha`로 저장하면 대부분의 시각 효과가 PNG에 래스터화됩니다.

**Q: 여러 PSD 파일을 배치 처리할 수 있나요?**  
A: 물론입니다. PSD 파일이 들어 있는 디렉터리를 순회하는 루프에 코드를 넣으면 됩니다.

**Q: PNG 압축 수준을 설정할 수 있나요?**  
A: `PngOptions` 클래스의 `setCompressionLevel(int)` 메서드를 사용해 미세 조정할 수 있습니다.

**Q: 이미지 객체를 닫아야 하나요?**  
A: `PsdImage`는 `Closeable`을 구현하므로 `finally` 블록에서 `im.close()`를 호출하거나 try‑with‑resources를 사용하세요.

**Q: 회전된 PNG의 크기가 원본과 동일합니까?**  
A: 90° 또는 270° 회전 시 가로와 세로가 교환됩니다. PNG는 새로운 방향을 반영합니다.

## 결론
Aspose.PSD for Java를 활용하면 **PSD를 PNG로 변환**, **PNG 투명성 보존**, 그리고 **PSD 레이어 회전**을 몇 줄의 코드만으로 수행할 수 있습니다. 이 접근 방식은 Photoshop이 필요 없게 만들고 자동화된 워크플로우를 가속화하며 이미지 출력에 대한 완전한 제어권을 제공합니다. 직접 프로젝트에 적용해 보고 얼마나 시간을 절약할 수 있는지 확인해 보세요!

---

**마지막 업데이트:** 2026-02-17  
**테스트 환경:** Aspose.PSD for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
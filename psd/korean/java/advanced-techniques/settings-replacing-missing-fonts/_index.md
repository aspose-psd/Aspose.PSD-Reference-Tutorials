---
date: 2025-12-25
description: Aspose.PSD for Java를 사용하여 PSD 파일의 글꼴을 교체하는 방법을 배우세요 – 단계별 가이드로 PSD를 PNG로
  저장하고 누락된 글꼴을 처리하는 방법도 보여줍니다.
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java에서 글꼴을 교체하는 방법
url: /ko/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java에서 글꼴 교체하는 방법

## 소개

Java 애플리케이션에서 Photoshop(PSD) 파일을 다룰 때, 누락된 글꼴은 시각 레이아웃을 깨뜨리고 렌더링 오류를 일으킬 수 있습니다. **글꼴 교체 방법**을 빠르고 신뢰성 있게 수행하는 것은 디자인 충실도를 유지하는 데 필수적입니다. 이 튜토리얼에서는 Aspose.PSD for Java를 사용하여 누락된 글꼴을 교체하고, 결과를 PNG로 변환하며, 이미지 변환 워크플로우를 원활하게 유지하는 방법을 배웁니다. 최종적으로 이미지에서 글꼴을 교체하고, PSD를 PNG로 저장하며, 개발자가 흔히 겪는 문제들을 피할 수 있게 됩니다.

## 빠른 답변
- **“글꼴 교체”가 PSD 처리에서 의미하는 것은?** 누락되었거나 사용할 수 없는 글꼴을 지정한 대체 글꼴로 교체합니다.  
- **어떤 라이브러리가 이를 자동으로 처리하나요?** Aspose.PSD for Java는 `PsdLoadOptions.setDefaultReplacementFont`를 제공합니다.  
- **교체 후 PSD를 PNG로 변환할 수도 있나요?** 예 – `PngOptions`를 사용하고 `psdImage.save`를 호출합니다.  
- **프로덕션 사용에 라이선스가 필요합니까?** 비평가용 빌드가 아닌 경우 유효한 Aspose.PSD 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** 현재 Aspose.PSD 릴리스는 Java 8 이상 런타임에서 작동합니다.

## PSD 파일에서 글꼴 교체란?

PSD가 호스트 머신에 설치되지 않은 글꼴을 참조하면, 렌더링 엔진은 일반적인 기본 글꼴로 대체하게 되며, 이는 종종 텍스트 정렬이 어긋나는 결과를 초래합니다. 글꼴 교체를 사용하면 누락된 글꼴을 만날 때마다 라이브러리가 사용할 기본 글꼴(예: Arial)을 정의할 수 있어 일관된 시각 출력을 보장합니다.

## Aspose.PSD로 누락된 글꼴을 교체해야 하는 이유

- **Zero‑dependency solution** – 네이티브 Photoshop이나 외부 도구가 필요 없습니다.  
- **Batch‑ready** – 동일한 설정으로 여러 파일을 루프에서 처리할 수 있습니다.  
- **Image conversion ready** – 교체 후 바로 **PSD를 PNG로 저장**하거나 **PSD를 PNG로 변환**할 수 있어 추가 단계가 없습니다.  
- **Cross‑platform** – Windows, Linux, macOS Java 런타임에서 모두 작동합니다.

## 전제 조건

1. **Aspose.PSD Library** – [releases page](https://releases.aspose.com/psd/java/)에서 Aspose.PSD for Java 라이브러리를 다운로드하고 설치합니다.  
2. **Java Development Environment** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.  

필수 사항을 준비했으니, 이제 코드로 들어가 보겠습니다.

## 패키지 가져오기

필요한 Aspose.PSD 클래스를 가져옵니다. 이를 통해 이미지 로드, 글꼴 교체 옵션, PNG 내보내기 기능에 접근할 수 있습니다.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 단계 1: 문서 디렉터리 설정

소스 PSD가 들어 있는 폴더와 결과 PNG가 저장될 폴더를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

## 단계 2: 원본 및 대상 파일 지정

입력 PSD와 출력 PNG의 전체 경로를 제공합니다. 이렇게 하면 워크플로우가 명확해지고 코드를 유지 관리하기 쉬워집니다.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## 단계 3: 글꼴 교체 설정 구성

`PsdLoadOptions` 인스턴스를 생성하고 누락된 글꼴을 만났을 때 사용할 글꼴을 Aspose.PSD에 알려줍니다. 이 예제에서는 **Arial**을 사용하지만, 시스템에 설치된 다른 글꼴로 교체할 수 있습니다.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## 단계 4: PSD 이미지 로드 및 글꼴 교체

위에서 정의한 옵션을 사용해 PSD를 로드합니다. 라이브러리는 자동으로 누락된 글꼴을 지정한 기본 글꼴로 교체합니다.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## 단계 5: 수정된 이미지 저장

투명도를 보존하기 위해 알파 채널이 포함된 true color PNG 내보내기 옵션을 설정합니다. 이 단계는 글꼴 교체 후 **PSD를 PNG로 변환**을 보여줍니다.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### 방금 무슨 일이 일어났나요?

- PSD가 대체 글꼴(Arial)로 열렸습니다.  
- 원래 누락된 글꼴을 참조하던 모든 텍스트 레이어가 이제 Arial로 렌더링됩니다.  
- 최종 이미지는 PNG로 저장되어, 시각적 충실도를 유지하면서 **PSD를 PNG로 저장**한 효과를 얻습니다.

## 일반적인 문제 및 해결 방법

| 문제 | 원인 | 해결책 |
|------|------|--------|
| 텍스트가 여전히 잘못 표시됨 | 글꼴 메트릭이 다름(크기, 굵기) | 프로그램matically 교체 글꼴 크기를 조정하거나 메트릭이 유사한 글꼴을 선택합니다. |
| PNG 파일이 예상보다 큼 | 기본 PNG 옵션이 32‑bit 색상을 사용함 | `PngColorType`을 `Truecolor`로 전환하여 알파가 필요 없을 경우 사용합니다. |
| 라이선스 예외 발생 | 유효한 라이선스 없이 실행 | 이미지를 로드하기 전에 임시 또는 영구 Aspose.PSD 라이선스를 적용합니다. |

## 자주 묻는 질문

**Q: Aspose.PSD가 모든 PSD 파일 버전과 호환되나요?**  
A: Aspose.PSD는 초기 Photoshop 릴리스부터 최신 기능까지 다양한 PSD 버전을 지원합니다.

**Q: Aspose.PSD에서 교체용 커스텀 글꼴을 사용할 수 있나요?**  
A: 예, `setDefaultReplacementFont`에 커스텀 글꼴 이름을 전달하면 됩니다. 해당 글꼴이 JVM에서 접근 가능해야 합니다.

**Q: Aspose.PSD에 대한 라이선스 옵션이 있나요?**  
A: 라이선스 옵션은 [here](https://purchase.aspose.com/buy)에서 확인하여 필요에 맞는 플랜을 선택하세요.

**Q: Aspose.PSD 지원을 위한 커뮤니티 포럼이 있나요?**  
A: 예, 커뮤니티 지원 및 토론을 위해 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)을 방문하세요.

**Q: Aspose.PSD 임시 라이선스를 어떻게 얻을 수 있나요?**  
A: 테스트 및 평가용 임시 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

---

**마지막 업데이트:** 2025-12-25  
**테스트 대상:** Aspose.PSD 24.11 for Java (latest at time of writing)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
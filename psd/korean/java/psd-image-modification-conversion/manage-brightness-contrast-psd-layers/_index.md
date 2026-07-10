---
date: 2026-03-28
description: Aspose.PSD for Java를 사용하여 PSD의 밝기를 조정하는 방법을 배우고, PSD 레이어의 밝기와 대비를 변경하는
  방법도 포함됩니다. 개발자와 그래픽 디자이너에게 이상적입니다.
linktitle: Adjust Brightness PSD Java – Manage Brightness & Contrast
second_title: Aspose.PSD Java API
title: 밝기 조정 PSD Java – 밝기 및 대비 관리
url: /ko/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 밝기 조정 PSD Java – 밝기 및 대비 관리

## 소개

PSD(Photoshop Document) 파일을 자주 다루는 그래픽 디자이너이거나 개발자이신가요? Java 환경을 떠나지 않고 **adjust brightness psd java** 를 빠르고 신뢰성 있게 수행해야 하나요? 이 튜토리얼에서는 Aspose.PSD 라이브러리를 사용하여 PSD 레이어의 밝기와 대비를 변경하는 방법을 정확히 보여드립니다. 자동화된 이미지 처리 파이프라인에 통합할 수 있는 재사용 가능한 코드 스니펫을 얻을 수 있습니다. 이제 팔을 걷어붙이고 시작해 봅시다!

## 빠른 답변
- **필요한 라이브러리는 무엇인가요?** Aspose.PSD for Java  
- **여러 레이어를 한 번에 변경할 수 있나요?** 예 – 모든 `BrightnessContrastLayer` 객체를 반복합니다.  
- **필요한 Java 버전은?** JDK 8 이상.  
- **프로덕션에 라이선스가 필요합니까?** 예, 비평가용이 아닌 사용을 위해 상업용 라이선스가 필요합니다.  
- **코드가 Maven/Gradle 프로젝트와 호환되나요?** 물론입니다 – Aspose.PSD 의존성을 추가하기만 하면 됩니다.

## “adjust brightness psd java”란 무엇인가요?

Java를 통해 PSD 파일의 밝기를 조정한다는 것은 `BrightnessContrastLayer` 값을 프로그래밍 방식으로 수정하는 것을 의미하며, 포토샵에서 수동으로 해야 할 시각적 조정을 자동화할 수 있게 합니다.

## 왜 PSD 레이어에서 밝기와 대비를 조정해야 할까요?

- **배치 처리 속도 향상** – 대규모 디자인 라이브러리에 적합합니다.  
- **레이어 구조 유지** – 대상 조정 레이어만 변경되어 마스크와 효과가 보존됩니다.  
- **CI/CD 파이프라인에 통합** – 미리보기 이미지나 썸네일을 자동으로 생성합니다.

## 전제 조건

Java로 PSD 파일을 조작하는 흥미로운 여정을 시작하기 전에, 필요한 모든 것이 올바르게 설정되어 있는지 확인하는 것이 중요합니다. 이 튜토리얼을 성공적으로 완료하기 위해 필요한 사항은 다음과 같습니다:

1. **Java Development Kit (JDK)** – 머신에 JDK 8 이상이 설치되어 있는지 확인하세요. [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html)에서 다운로드할 수 있습니다.
2. **Aspose.PSD for Java Library** – PSD 파일을 다루려면 Aspose.PSD 라이브러리가 필요합니다. 최신 버전은 [release page](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.
3. **IDE of Your Choice** – IntelliJ IDEA, Eclipse, NetBeans와 같은 통합 개발 환경(IDE)을 사용하면 Java 코드를 작성하고 실행하기에 좋습니다.
4. **Basic Knowledge of Java** – Java 프로그래밍에 익숙하면 우리가 다룰 코드 스니펫을 이해하는 데 도움이 됩니다.

이 전제 조건들을 갖추면 이제 진행할 준비가 된 것입니다. 이제 좋아하는 코드 편집기를 열고 코딩을 시작해 봅시다!

## 패키지 가져오기

코딩 여정의 첫 단계는 필요한 패키지를 가져오는 것입니다. Aspose.PSD가 제공하는 기능을 사용하려면 라이브러리가 클래스패스에 포함되어 있어야 합니다. 다음은 그 방법입니다:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

이 단계들을 완료하면 PSD 파일을 효과적으로 다룰 준비가 된 것입니다!

이제 모든 준비가 끝났으니 튜토리얼의 핵심인 PSD 레이어의 밝기와 대비 조정으로 들어갑시다. 이 과정을 명확한 단계로 나누어 쉽게 따라올 수 있도록 하겠습니다.

## 단계 1: 문서 디렉터리 정의

먼저 PSD 파일이 위치한 디렉터리를 정의합니다. 이 단계는 파일을 효율적으로 정리하는 데 도움이 됩니다.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"`를 PSD 파일 디렉터리의 실제 경로로 교체하세요.

## 단계 2: 소스 및 대상 파일 이름 지정

다음으로 PSD의 소스 파일 이름과 편집된 PSD가 저장될 대상 파일을 지정해야 합니다.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

이 예에서는 디렉터리에 `BrightnessContrastModern.psd`라는 PSD 파일이 있다고 가정합니다.

## 단계 3: PSD 파일 로드

이제 PSD 파일을 애플리케이션에 로드하여 조작할 차례입니다.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

이 코드 라인은 PSD 파일을 나타내는 `PsdImage` 인스턴스를 생성합니다. 이제 PSD의 모든 레이어에 접근할 수 있습니다.

## 단계 4: 레이어 반복

다음 단계는 PSD 파일의 각 레이어를 반복하여 밝기와 대비 설정을 찾고 조작하는 것입니다.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

`for` 루프는 PSD의 각 레이어를 순회합니다. 레이어가 `BrightnessContrastLayer` 인스턴스인지 확인하고 있습니다. 이는 올바른 레이어에서만 PSD 레이어 밝기 변경을 시도하도록 보장하는 데 필수적입니다.

## 단계 5: 밝기 및 대비 조정

루프 안에서 이제 각 `BrightnessContrastLayer`에 대해 밝기와 대비를 설정할 수 있습니다. 

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

이 예에서는 밝기와 대비를 `50`으로 설정했습니다. 필요에 따라 이 값을 조정할 수 있습니다. 숫자가 높을수록 밝기/대비가 증가하고, 낮을수록 감소합니다.

## 단계 6: 변경 사항 저장

마지막 단계는 변경 사항을 PSD 파일에 저장하는 것입니다. 수정된 이미지를 지정된 대상에 다시 기록해야 합니다.

```java
im.save(psdPathAfterChange);
```

이 코드 라인은 새로운 밝기와 대비 설정이 적용된 편집된 PSD 파일을 저장합니다.

## 일반적인 문제 및 해결책

| Issue | Why It Happens | Fix |
|-------|----------------|-----|
| **`BrightnessContrastLayer` 없음** | PSD가 다른 조정 유형(예: Levels)을 사용할 수 있습니다. | `BrightnessContrastLayer` 로 변환하거나 레이어 유형을 확인하세요. |
| **저장된 파일이 손상된 것처럼 보임** | 라이선스가 없거나 오래된 Aspose.PSD 버전을 사용하고 있습니다. | 유효한 라이선스를 적용하고 최신 라이브러리 릴리스를 사용하고 있는지 확인하세요. |
| **값이 범위를 벗어남** | 밝기/대비 값은 -100에서 100 사이여야 합니다. | `setBrightness`/`setContrast` 호출 전에 값을 제한하세요. |

## 자주 묻는 질문

**Q: Aspose.PSD for Java란 무엇인가요?**  
A: Aspose.PSD for Java는 개발자가 PSD 파일을 프로그래밍 방식으로 조작할 수 있게 해 주는 라이브러리로, Photoshop 관련 작업을 자동화할 수 있습니다.

**Q: 여러 레이어의 밝기와 대비를 한 번에 조정할 수 있나요?**  
A: 예, 이 튜토리얼에서 사용한 방법은 PSD의 모든 레이어를 반복하므로 여러 `BrightnessContrastLayer` 인스턴스를 조정할 수 있습니다.

**Q: Aspose.PSD 임시 라이선스를 어떻게 얻나요?**  
A: [temporary license page](https://purchase.aspose.com/temporary-license/)를 방문하면 임시 라이선스를 얻을 수 있습니다.

**Q: Aspose.PSD 무료 체험판이 있나요?**  
A: 예, [release page](https://releases.aspose.com/)에서 Aspose.PSD 무료 체험판을 다운로드할 수 있습니다.

**Q: Aspose.PSD에 대한 추가 지원은 어디서 받을 수 있나요?**  
A: 그들의 [support forum](https://forum.aspose.com/c/psd/34)에서 Aspose.PSD 지원을 받을 수 있습니다.

---

**마지막 업데이트:** 2026-03-28  
**테스트 대상:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
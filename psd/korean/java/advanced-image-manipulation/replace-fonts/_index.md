---
date: 2026-02-09
description: Java에서 Aspose PSD 글꼴 대체 기능을 사용하여 누락된 글꼴이 있는 PSD 파일을 처리하고, 누락된 글꼴을 빠르게
  교체하며, 이미지를 내보내는 방법을 배웁니다.
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Java에서 Aspose PSD 글꼴 대체 – 누락된 글꼴 교체
url: /ko/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 Aspose PSD 교체

## 소개

Photoshop(PSD) 파일 내부에 반대하는 경우에는 교체할 수 없습니다. **PSD 파일 교체**를 사용하면 처리할 수 없습니다. Java에서 PSD를 로드하고, Aspose에 제외하고, 원하는 형식으로 저장하면 됩니다. 이 튜토리얼에서는 프로젝트 설정부터 업데이트된 이미지를 처리할 수 있는 전체 **aspose psd 글꼴 대체** 워크플로우를 섹션으로 안내합니다. 따라서 Photoshop을 열지 이벤트에 참여시킨 PSD를 처리할 수 있습니다.

## 빠른 답변
- **글꼴 대체를 처리하는 라이브러리는 무엇입니까?** Java용 Aspose.PSD
- **구현하는 데 시간이 얼마나 걸리나요?** 기본 시나리오의 경우 약 5~10분 정도 소요됩니다.
- **기본 대체 글꼴로 사용되는 글꼴은 무엇입니까?** "Arial"과 같은 트루타입 글꼴을 설정할 수 있습니다.
- **PNG 이외의 형식으로 저장할 수 있나요?** 예 – PSD, JPEG, BMP 등이 지원됩니다.
- **프로덕션을 위해 라이선스가 필요합니까?** 평가판이 아닌 사용을 위해서는 유효한 Aspose.PSD 라이선스가 필요합니다.

## Aspose PSD 글꼴 대체란 무엇입니까?

Aspose PSD 전투기는 교체용 PSD 파일에서 운동 지원을 하지 않고 반대 방향으로 전투를 벌이는 것을 사용하도록 유도하는 과정입니다. 이를 통해 텍스트 레이어는 Photoshop에서 수동으로 편집하지 않고 보관할 수 있으며 **누락된 글꼴 PSD를 처리**을 자동으로 파일로 처리할 수 있습니다.

## Java용 Aspose.PSD를 사용하는 이유는 무엇입니까?

- **완벽한 PSD 처리 기능** – 레이어, 마스크, 효과 및 텍스트 모두 API를 통해 접근 가능합니다.

- **크로스 플랫폼** – Java를 지원하는 모든 운영 체제에서 작동합니다.

- **외부 종속성 없음** – 라이브러리가 글꼴 대체를 내부적으로 처리하므로 앱에 추가 글꼴을 포함할 필요가 없습니다.

## Aspose PSD를 사용하여 PSD 파일에서 누락된 글꼴을 바꾸는 방법

아래는 **누락된 글꼴이 있는 PSD 파일**을 사용자 지정 대체 글꼴로 바꾸는 방법을 단계별로 안내합니다.

## 필수 조건

시작하기 전에 다음 사항을 확인하십시오.

- **Java Development Kit(JDK)** – 버전 8 이상이 설치되어 있어야 합니다.

- **Aspose.PSD for Java** – [릴리스 페이지](https://releases.aspose.com/psd/java/)에서 최신 JAR 파일을 다운로드하십시오.

- **IDE** – IntelliJ IDEA, Eclipse 또는 원하는 편집기

## 패키지 가져오기

먼저 필요한 클래스를 가져옵니다. 이를 통해 이미지 로딩, 로딩 옵션 및 저장 기능을 사용할 수 있습니다.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 1단계: 문서 디렉터리 설정

원본 PSD 파일이 있는 폴더를 지정합니다. 자리 표시자를 컴퓨터의 실제 경로로 바꾸세요.

```java
String dataDir = "Your Document Directory";
```

## 2단계: 대체 글꼴로 이미지 로드

`PsdLoadOptions` 인스턴스를 생성하고 기본 대체 글꼴(예: **Arial**)을 지정한 다음 PSD 파일을 로드합니다. Aspose는 누락된 글꼴을 발견하면 자동으로 대체 글꼴을 적용합니다.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## 3단계: 대체된 이미지 저장

글꼴 대체 후 지원되는 형식으로 이미지를 내보낼 수 있습니다. 여기서는 PNG로 저장하지만 JPEG, BMP를 선택하거나 PSD 파일로 다시 저장할 수도 있습니다.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## 일반적인 문제 및 해결 방법

| 이슈 | 원인 | 수정 |
|-------|-------|------|
| 텍스트가 교체되는 깨져보임 | 대체할 필요가 없습니다. | 필요한 유니코드 범위를 지원하는 데(예: “Arial Unicode MS”)를 선택 |
| 큰 PSD 파일에서 `OutOfMemoryError` 발생 | 힙 메모리 없이 고해상도 파일을 로드 | JVM 힙 크기(`-Xmx2g`)를 사용하거나 스트리밍 모드가 있으면 사용 가능 |
| 라이선스 발생 | 서비스얼 버전을 사용하는 방법 | 로드하기 전에 이미지를 영구히 또는 임시 전원을 적용 |

## 자주 묻는 질문

**Q: PSD 외에 다른 이미지 형식의 글꼴을 교체할 수 있나요?**
답: 그렇습니다. 주요 사용 사례는 PSD이지만 Aspose.PSD는 PNG, JPEG, BMP 및 TIFF도 지원하므로 텍스트 레이어가 있는 경우 글꼴 교체가 가능합니다.

**질문: 기본 대체 글꼴 설정이 필수인가요?**
답변: 아니요. 원하는 TrueType 글꼴을 설정하거나, 설정을 생략하여 Aspose에서 제공하는 기본 글꼴을 사용할 수 있습니다.

**질문: Aspose.PSD 사용에 필요한 라이선스가 있나요?**
답변: 프로덕션 환경에 배포하려면 상용 라이선스가 필요합니다. 자세한 내용은 [구매 페이지](https://purchase.aspose.com/buy)를 참조하세요.

**질문: 테스트용 임시 라이선스를 받을 수 있나요?**
답변: 네, 가능합니다. Aspose는 평가용 임시 라이선스를 무료로 제공합니다. [임시 라이선스 페이지](https://purchase.aspose.com/temporary-license/)를 방문하세요.

**질문: Aspose.PSD 관련 추가 지원을 받거나 문제를 논의할 수 있는 곳은 어디인가요?**
답변: 커뮤니티 포럼에서 질문하실 수 있습니다. [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)을 참조하세요.


**질문: 여러 개의 글꼴이 누락된 PSD 파일은 어떻게 처리해야 하나요?**
답변: 기본 대체 글꼴을 한 번만 설정하면(아래 그림 참조) 로드 작업 중에 누락된 모든 글꼴에 적용됩니다.

**질문: 이미지를 저장한 후 글꼴을 바꿀 수 있나요?**
답변: 글꼴 대체는 로드 단계에서 이루어져야 합니다. 나중에 글꼴을 변경하려면 다른 대체 글꼴을 사용하여 PSD 파일을 다시 로드하고 저장해야 합니다.

## 결론

이제 올바른 클래스를 가져오고, 대체 글꼴을 구성하고, PSD 파일을 로드하고, 수정된 이미지를 내보내기까지 **Aspose PSD 글꼴 대체** 워크플로 전체를 Java에서 살펴보았습니다. 이 패턴을 이미지 처리 파이프라인에 통합하여 모든 PSD 에셋에서 일관된 타이포그래피를 유지하고 **PSD 파일에서 글꼴이 누락된 경우**를 자동으로 처리하세요.


---

**최종 업데이트:** 2026년 2월 9일
**테스트 환경:** Aspose.PSD for Java 24.12 (작성 시점 기준 최신 버전)
**제작자:** Aspose 

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

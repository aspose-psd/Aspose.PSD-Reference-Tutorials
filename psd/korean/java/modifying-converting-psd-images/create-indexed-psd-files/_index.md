---
date: 2026-03-15
description: Aspose.PSD for Java를 사용하여 PSD 파일을 만들고, PSD 색상 팔레트를 생성하며, PSD 색상 모드를 설정하는
  방법을 단계별 가이드에서 배워보세요.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD 파일 만드는 방법
url: /ko/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD 파일 만드는 방법

## 소개
프로그래밍으로 **PSD 파일을 만드는 방법**이 궁금하시다면 이곳이 정답입니다. Aspose.PSD for Java는 Photoshop 문서를 완전히 제어할 수 있게 해 주어, Photoshop을 열지 않고도 PSD 파일을 생성·편집·저장할 수 있습니다. 이번 튜토리얼에서는 **인덱스 PSD** 파일을 만들고, PSD 색상 모드를 설정하며, 사용자 정의 색상 팔레트를 생성하는 과정을 명확한 단계별 Java 코드와 함께 살펴봅니다. 그래픽 파이프라인을 구축하거나, 에셋 자동화를 진행하거나, 단순히 실험해 보려는 경우에도 여기서 다루는 개념이 시각적 아이디어를 구현하는 데 도움이 될 것입니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.PSD for Java  
- **인덱스 PSD를 만들 수 있나요?** 예, 색상 모드를 `Indexed`로 설정하면 됩니다.  
- **Photoshop이 설치돼 있어야 하나요?** 아니요, Aspose.PSD는 독립적으로 동작합니다.  
- **필요한 Java 버전은?** JDK 8 이상  
- **캔버스 크기 제한은?** 제한 없음; 이 예제에서는 500 × 500 px를 사용합니다.

## 인덱스 PSD 파일이란?
인덱스 PSD는 각 픽셀마다 전체 색상 값을 저장하는 대신 색상 팔레트에 색상을 저장합니다. 이를 통해 파일 크기를 줄일 수 있으며, 아이콘이나 UI 에셋처럼 제한된 색상을 사용하는 그래픽에 적합합니다. 사용자 정의 팔레트를 생성하면 최종 이미지에 어떤 색상이 사용될지 정확히 제어할 수 있습니다.

## PSD 색상 팔레트를 생성하는 이유
**PSD 색상 팔레트**를 만들면 다음과 같은 이점이 있습니다.
- 웹·모바일용 파일 크기를 작게 유지  
- 기업 브랜드 색상 팔레트로 색상을 제한해 일관성 확보  
- 인덱스 이미지를 지원하는 애플리케이션에서 렌더링 속도 향상  

## 사전 준비
코드를 진행하기 전에 다음 항목을 준비하세요.

1. **Java 기본 지식** – 클래스, 메서드, 객체 생성에 익숙해야 합니다.  
2. **Java Development Kit (JDK) 8+** – IDE에 설치·설정되어 있어야 합니다.  
3. **IDE (IntelliJ IDEA, Eclipse 등)** – 선택 사항이지만 디버깅에 크게 도움이 됩니다.  
4. **Aspose.PSD for Java 라이브러리** – **[여기](https://releases.aspose.com/psd/java/)**에서 다운로드하고 JAR 파일을 프로젝트 클래스패스에 추가합니다.  
5. **기본 그래픽 디자인 개념** – 색상 모드, 팔레트, 기본 도형에 대한 이해가 있으면 따라하기 쉽습니다.

## 패키지 가져오기
코드를 작성하기 전에 Java 애플리케이션에 필요한 패키지를 모두 가져와야 합니다. 아래가 필요한 import 구문입니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

이 import 구문을 통해 Aspose.PSD를 이용한 PSD 옵션, 색상, 그래픽 조작 기능을 사용할 수 있습니다.

이제 **인덱스 색상 모드**로 **PSD 파일을 만드는 방법**을 단계별로 살펴보겠습니다.

## 1단계: 문서 디렉터리 설정
먼저 생성된 PSD 파일이 저장될 위치를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"`를 절대 경로나 상대 경로로 교체하세요. 예: `"/Users/YourName/Documents/"`.

## 2단계: PsdOptions 인스턴스 생성
`PsdOptions`는 생성하려는 파일의 모든 설정을 담고 있습니다.

```java
PsdOptions createOptions = new PsdOptions();
```

## 3단계: PsdOptions 핵심 속성 설정
출력 위치, **PSD 색상 모드**를 `Indexed`로 지정, 그리고 PSD 버전을 설정합니다.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – 새 파일의 전체 경로.  
- **Color Mode** – `Indexed`는 Aspose.PSD가 팔레트 기반 이미지를 사용하도록 지정합니다.  
- **Version** – PSD 포맷 버전 (대부분 최신 Photoshop에서 5 버전이면 충분합니다).

## 4단계: 색상 팔레트 생성 (Generate PSD Color Palette)
인덱스 이미지에서 사용할 색상을 정의합니다.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- `palette` 배열은 최대 256개의 `Color` 객체를 담을 수 있습니다.  
- `CompressionMethod.RLE`는 인덱스 이미지에 효율적인 무손실 압축을 제공합니다.

## 5단계: PSD 이미지 캔버스 만들기
이제 원하는 크기의 빈 PSD를 생성합니다.

```java
Image psd = Image.create(createOptions, 500, 500);
```

위 코드는 앞서 정의한 팔레트를 사용해 500 × 500 픽셀 캔버스를 만들게 됩니다.

## 6단계: PSD에 그래픽 그리기
시각적 내용을 추가합니다—예제에서는 흰 배경에 빨간 타원을 그립니다.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())`는 배경을 흰색으로 채웁니다.  
- `drawEllipse`은 6픽셀 두께의 빨간 타원을 그립니다.

## 7단계: PSD 파일 저장
마지막으로 이미지를 디스크에 저장합니다.

```java
psd.save();
```

`Newsample_out.psd` 파일이 앞서 지정한 디렉터리에 생성됩니다.

## 흔히 발생하는 문제 및 팁
- **팔레트 크기** – 4가지 색 이상이 필요하면 `palette` 배열에 색을 추가하면 됩니다(최대 256개).  
- **파일 권한** – Java 프로세스가 `dataDir`에 쓸 수 있는 권한이 있는지 확인하세요.  
- **잘못된 색상 모드** – `createOptions.setColorMode(ColorModes.Indexed)`를 빼먹으면 RGB PSD가 생성됩니다.  

## 자주 묻는 질문

**Q: Aspose.PSD for Java가 무엇인가요?**  
A: Aspose.PSD for Java는 Java를 사용해 프로그래밍 방식으로 PSD(Photoshop) 파일을 조작할 수 있게 해 주는 라이브러리입니다.

**Q: Aspose.PSD를 무료로 사용할 수 있나요?**  
A: 예, **[여기](https://releases.aspose.com/)**에서 무료 체험 버전을 이용할 수 있습니다.

**Q: Aspose.PSD를 사용하려면 Photoshop이 설치돼 있어야 하나요?**  
A: 아니요, Aspose.PSD는 모든 작업을 독립적으로 수행하므로 Photoshop이 없어도 PSD 파일을 만들고 편집할 수 있습니다.

**Q: Aspose.PSD 임시 라이선스는 어떻게 얻나요?**  
A: **[여기](https://purchase.aspose.com/temporary-license/)**에서 임시 라이선스를 요청할 수 있습니다.

**Q: Aspose.PSD 지원을 어디서 받을 수 있나요?**  
A: **[여기](https://forum.aspose.com/c/psd/34)**의 Aspose 포럼에서 지원을 받을 수 있습니다.

## 결론
인덱스 색상 모드로 **PSD 파일을 만드는 방법**, 사용자 정의 팔레트 생성, 간단한 그래픽 추가까지 Aspose.PSD for Java를 활용해 모두 배웠습니다. 이제 이 기본 블록을 바탕으로 더 복잡한 드로잉, 레이어 관리, 배치 처리 등을 확장해 보세요. 자세한 API 참고는 **[여기](https://reference.aspose.com/psd/java/)**에서 확인하고, 다양한 팔레트와 그리기 원시 요소를 실험해 보시기 바랍니다.

---

**마지막 업데이트:** 2026-03-15  
**테스트 환경:** Aspose.PSD for Java 24.12 (최신)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
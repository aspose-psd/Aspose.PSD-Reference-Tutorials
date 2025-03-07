---
title: .NET용 Aspose.PSD를 사용하여 타원형 모양 만들기
linktitle: .NET용 Aspose.PSD를 사용하여 타원형 모양 만들기
second_title: Aspose.PSD .NET API
description: Aspose.PSD를 사용하여 .NET에서 타원형 모양을 그리는 방법을 알아보세요. 코드 예제가 포함된 단계별 가이드입니다. 손쉽게 멋진 그래픽을 만들어 보세요.
weight: 13
url: /ko/net/psd-drawing-techniques/creating-elliptical-shapes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.PSD를 사용하여 타원형 모양 만들기

## 소개

.NET용 Aspose.PSD를 사용하여 타원형 모양을 만드는 방법에 대한 포괄적인 가이드에 오신 것을 환영합니다. Aspose.PSD는 개발자가 Adobe Photoshop 없이도 Photoshop 파일을 조작하고 변환할 수 있는 강력한 .NET 라이브러리입니다. 이 튜토리얼에서는 라이브러리를 사용하여 타원형 모양을 그리는 과정을 안내합니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- .NET 라이브러리용 Aspose.PSD: .NET 프로젝트에 Aspose.PSD 라이브러리가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[.NET 문서용 Aspose.PSD](https://reference.aspose.com/psd/net/).

- .NET 환경: 이 튜토리얼에서는 사용자가 .NET 프레임워크에 대한 실무 지식을 가지고 있다고 가정합니다.

## 네임스페이스 가져오기

시작하려면 필요한 네임스페이스를 프로젝트로 가져옵니다. 이렇게 하면 타원형 모양을 그리는 데 필요한 클래스와 메서드에 액세스할 수 있습니다. 예는 다음과 같습니다.

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

이제 타원형 모양을 만드는 과정을 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 설정

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";
```

## 2단계: BmpOptions 인스턴스 생성

```csharp
// BmpOptions 인스턴스를 생성하고 다양한 속성을 설정합니다.
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## 3단계: 이미지 인스턴스 생성

```csharp
// 이미지 인스턴스 생성
using (Image image = new PsdImage(100, 100))
{
    // Graphics 클래스 및 Clear Graphics 표면의 인스턴스 생성 및 초기화
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## 4단계: 점선 타원 모양 그리기

```csharp
    // 빨간색의 Pen 객체와 주변의 Rectangle을 지정하여 점선으로 된 타원 모양을 그린다.
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## 5단계: 연속적인 타원 모양 그리기

```csharp
    //파란색의 단색 브러시와 주변의 Rectangle을 포함하는 Pen 객체를 지정하여 연속적인 타원 모양을 그립니다.
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // 이미지를 bmp 파일 형식으로 내보냅니다.
    image.Save(outpath, saveOptions);
}
```

## 결론

축하해요! .NET용 Aspose.PSD를 사용하여 타원형 모양을 성공적으로 만들었습니다. 이 튜토리얼에서는 환경 설정부터 점선 및 연속 타원 모양 그리기까지 필수 단계를 다루었습니다.

## FAQ

### Q1: .NET용 Aspose.PSD에 대한 설명서는 어디에서 찾을 수 있습니까?

 A1: 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/psd/net/).

### Q2: .NET용 Aspose.PSD를 어떻게 다운로드합니까?

 A2: 릴리스 페이지에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/psd/net/).

### Q3: 무료 평가판이 제공됩니까?

 A3: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: .NET용 Aspose.PSD에 대한 지원을 어떻게 받을 수 있나요?

 A4: 지원 포럼을 방문하세요.[여기](https://forum.aspose.com/c/psd/34).

### Q5: 테스트하려면 임시 라이센스가 필요합니까?

 A5: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

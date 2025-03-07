---
title: .NET용 Aspose.PSD에서 외부 광선 효과 지원
linktitle: 외부 광선 효과 지원
second_title: Aspose.PSD .NET API
description: .NET용 Aspose.PSD에서 외부 광선 효과의 강력한 기능을 살펴보세요. 이 단계별 튜토리얼을 통해 이미지 디자인을 향상시키세요.
weight: 16
url: /ko/net/image-manipulation/supporting-outer-glow-effect/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.PSD에서 외부 광선 효과 지원

## 소개

.NET용 Aspose.PSD의 외부 광선 효과 지원에 대한 단계별 가이드에 오신 것을 환영합니다. Aspose.PSD는 .NET 애플리케이션에서 PSD 파일을 원활하게 조작할 수 있는 강력한 라이브러리입니다. 이 튜토리얼에서는 외부 광선 효과의 구현을 살펴보고 이를 프로젝트에 통합하기 위한 자세한 연습을 제공합니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET 라이브러리용 Aspose.PSD: 다음에서 라이브러리를 다운로드하세요.[Aspose.PSD .NET 문서](https://reference.aspose.com/psd/net/).

- 개발 환경: 선호하는 .NET 개발 환경을 설정합니다.

- 문서 및 출력 디렉터리: 제공된 코드에서 문서 및 출력 디렉터리를 정의합니다.

## 네임스페이스 가져오기

이 섹션에서는 Outer Glow Effect 구현을 시작하는 데 필요한 네임스페이스를 가져옵니다. 다음 단계를 따르세요.

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

이제 제공된 예제를 여러 단계로 나누어 외부 광선 효과를 달성해 보겠습니다.

## 1단계: 문서 및 출력 경로 설정

```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```

## 2단계: PSD 이미지 로드

```csharp
string src = Path.Combine(baseDir, "GreenLayer.psd");
using (var image = (PsdImage)Image.Load(src))
{
    // 구현 단계가 아래에 추가됩니다.
}
```

## 3단계: 외부 광선 효과 추가

```csharp
OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
```

## 4단계: 외부 광선 매개변수 구성

```csharp
effect.Range = 10;
effect.Spread = 10;
((IColorFillSettings)effect.FillColor).Color = Color.Red;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

## 5단계: 이미지 저장

```csharp
string outputPng = Path.Combine(outputDir, "output261.png");
image.Save(outputPng, new PngOptions());
```

## 6단계: 정리

```csharp
File.Delete(outputPng);
```

## 7단계: 성공 메시지 표시

```csharp
Console.WriteLine("SupportOfOuterGlowEffect executed successfully");
```

## 결론

축하해요! .NET용 Aspose.PSD를 사용하여 외부 광선 효과를 성공적으로 구현했습니다. 이 강력한 기능은 이미지의 시각적 매력을 향상시켜 디자인에 독특한 느낌을 더해줍니다.

## FAQ

### Q1: Aspose.PSD는 모든 .NET 프레임워크와 호환됩니까?

A1: 예, Aspose.PSD는 광범위한 .NET 프레임워크를 지원하여 다양한 개발 환경과의 호환성을 보장합니다.

### Q2: Aspose.PSD에 대한 추가 문서는 어디서 찾을 수 있나요?

 A2: 다음을 참조하세요.[Aspose.PSD .NET 문서](https://reference.aspose.com/psd/net/) 포괄적인 정보와 예시를 보려면

### Q3: Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?

 A3: 방문[Aspose.PSD 임시 라이센스](https://purchase.aspose.com/temporary-license/) 임시 라이센스 옵션의 경우.

### Q4: Aspose.PSD 사용자는 어떤 지원을 받을 수 있나요?

 A4: 가입하세요[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 커뮤니티 지원 및 토론을 위해.

### Q5: .NET용 Aspose.PSD를 구입할 수 있나요?

 A5: 예, 라이선스 옵션을 살펴보고 구매하세요.[여기](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

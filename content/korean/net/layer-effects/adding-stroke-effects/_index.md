---
title: .NET용 Aspose.PSD의 레이어에 획 효과 추가
linktitle: 레이어에 획 효과 추가
second_title: Aspose.PSD .NET API
description: .NET용 Aspose.PSD를 사용하여 이미지 미학을 향상하세요. 획 효과를 단계별로 추가하는 방법을 알아보세요. 지금 무료 평가판을 다운로드, 구매 또는 사용해 보세요.
type: docs
weight: 10
url: /ko/net/layer-effects/adding-stroke-effects/
---
## 소개

.NET용 Aspose.PSD의 레이어에 스트로크 효과를 추가하는 방법에 대한 단계별 튜토리얼에 오신 것을 환영합니다. 획 효과를 사용하면 이미지의 시각적 매력을 쉽게 향상할 수 있으며 Aspose.PSD를 사용하면 .NET 개발자가 원활하게 작업할 수 있습니다. 이 가이드에서는 이 강력한 기능을 익히는 데 도움이 되는 명확한 단계와 예를 제공하면서 프로세스를 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- .NET용 Aspose.PSD: 다음에서 Aspose.PSD 라이브러리를 다운로드하고 설치하세요.[웹사이트](https://releases.aspose.com/psd/net/).

- 문서 디렉토리: 획 효과를 적용할 PSD 문서가 포함된 디렉토리를 준비합니다.

- 출력 디렉터리: 획 효과가 포함된 출력 이미지를 저장하기 위한 별도의 디렉터리가 있습니다.

- Visual Studio: Visual Studio 또는 기타 선호하는 .NET 개발 환경이 설정되어 있는지 확인하세요.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.PSD 기능을 활용하는 데 필요한 네임스페이스를 포함합니다.

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## 1단계: PSD 문서 로드

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // PSD 문서를 로드하기 위한 코드는 여기에 있습니다.
}
```

## 2단계: 색상 획 효과 추가

```csharp
// 내부 위치에 색상 채우기를 추가합니다.
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## 3단계: 아웃사이드 포지션

```csharp
// 외부 위치에 색상 채우기를 추가합니다.
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## 4단계: 중앙 위치

```csharp
// 중앙 위치에 색상 채우기를 추가합니다.
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

그라데이션 및 패턴 채우기에 대해 유사한 단계를 반복하고 그에 따라 설정을 조정합니다.

## 결론

축하해요! .NET용 Aspose.PSD를 사용하여 레이어에 획 효과를 추가하는 방법을 성공적으로 배웠습니다. 이미지에 원하는 시각적 효과를 얻으려면 다양한 설정을 실험해 보세요.

## FAQ

### Q1: 특정 레이어에만 획 효과를 적용할 수 있나요?

A1: 예, 코드에서 레이어 인덱스를 조정하여 특정 레이어를 대상으로 지정할 수 있습니다.

### Q2: Aspose.PSD는 최신 .NET 프레임워크와 호환됩니까?

A2: 물론이죠! Aspose.PSD는 최신 .NET 프레임워크와 원활하게 통합되도록 설계되었습니다.

### Q3: 획 색상을 어떻게 사용자 정의할 수 있나요?

 A3: 간단히 수정하세요.`Color` 원하는 획 색상을 얻으려면 코드의 속성을 사용하세요.

### Q4: Aspose.PSD는 여러 PSD 파일에 대한 일괄 처리를 지원합니까?

A4: 예, 여러 PSD 파일을 반복하고 유사한 접근 방식을 사용하여 획 효과를 적용할 수 있습니다.

### Q5: Aspose.PSD를 구매하기 전에 평가판을 사용할 수 있나요?

 A5: 물론이죠! 잡아[무료 시험판](https://releases.aspose.com/) 구매하기 전에 Aspose.PSD의 기능을 살펴보세요.
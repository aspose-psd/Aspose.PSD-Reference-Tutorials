---
title: .NET용 Aspose.PSD에서 단색으로 획 레이어 추가
linktitle: 단색으로 획 레이어 추가
second_title: Aspose.PSD .NET API
description: Aspose.PSD를 사용하여 .NET 이미지 조작 기술을 향상하세요. 단색으로 획 레이어를 추가하는 방법을 단계별로 알아보세요.
type: docs
weight: 11
url: /ko/net/layer-effects/adding-stroke-layer-solid-color/
---
## 소개

.NET 개발 영역에서는 시각적으로 매력적인 이미지를 만드는 것이 일반적인 요구 사항입니다. .NET용 Aspose.PSD는 이미지를 원활하게 조작하고 향상시킬 수 있는 강력한 도구 세트를 제공합니다. 필수 기능 중 하나는 단색의 획 레이어를 추가하여 이미지에 생동감과 깊이를 더하는 것입니다. 이 튜토리얼에서는 .NET용 Aspose.PSD를 사용하여 프로세스를 단계별로 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- .NET 개발에 대한 기본 지식.
- 컴퓨터에 Visual Studio가 설치되어 있습니다.
- .NET 라이브러리용 Aspose.PSD. 다음에서 다운로드할 수 있습니다.[웹사이트](https://releases.aspose.com/psd/net/).

## 네임스페이스 가져오기

.NET용 Aspose.PSD의 기능을 활용하려면 필요한 네임스페이스를 가져오는 것부터 시작하세요.

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## 1단계: PSD 파일 로드

스트로크 레이어로 향상시키려는 PSD 파일을 로드하는 것부터 시작하세요. 파일 경로가 올바른지 확인하세요.

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // 추가 단계에 대한 코드가 여기에 추가됩니다.
}
```

## 2단계: 획 효과 속성에 액세스

PSD 파일에서 획 효과의 속성을 검색합니다.

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## 3단계: 스트로크 설정 조정

원하는 대로 스트로크 설정을 수정합니다. 이 예에서는 색상을 노란색으로 변경하고 불투명도를 127로 설정한 다음 색상 혼합 모드를 사용합니다.

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## 4단계: 편집된 이미지 저장

획 레이어 변경 사항을 적용한 후 이미지를 저장합니다.

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## 5단계: 변경 사항 확인

편집된 이미지를 로드하고 검사하여 변경 사항이 올바르게 적용되었는지 확인하세요.

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // 변경사항을 확인하는 코드가 여기에 추가됩니다.
}
```

추가 조정을 위해 이 단계를 반복하거나 다양한 획 효과를 실험하여 원하는 시각적 효과를 얻으세요.

## 결론

축하해요! .NET용 Aspose.PSD를 사용하여 단색으로 획 레이어를 추가하는 방법을 성공적으로 배웠습니다. 이 강력한 기능은 .NET 환경에서 이미지를 향상시킬 수 있는 가능성의 세계를 열어줍니다.

## 자주 묻는 질문

### Q1: .NET용 Aspose.PSD는 최신 .NET 프레임워크 버전과 호환됩니까?

A1: 예, .NET용 Aspose.PSD는 최신 .NET 프레임워크 버전과의 호환성을 보장하기 위해 정기적으로 업데이트됩니다.

### Q2: 상업용 프로젝트에 Aspose.PSD for .NET을 사용할 수 있습니까?

A2: 물론이죠! Aspose.PSD for .NET은 상용 제품이므로 라이선스를 구매하여 프로젝트에 사용할 수 있습니다.

### Q3: .NET용 Aspose.PSD에 대한 추가 예제와 문서는 어디에서 찾을 수 있습니까?

 A3: 탐색해 보세요.[선적 서류 비치](https://reference.aspose.com/psd/net/) 포괄적인 예시와 지침을 확인하세요.

### Q4: .NET용 Aspose.PSD에 대한 무료 평가판이 있습니까?

 A4: 예, 다음 사이트에서 무료 평가판을 받을 수 있습니다.[릴리스 페이지](https://releases.aspose.com/).

### Q5: .NET용 Aspose.PSD에 대한 지원을 어떻게 받을 수 있나요?

 A5: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 도움을 구하고 지역 사회와 연결됩니다.
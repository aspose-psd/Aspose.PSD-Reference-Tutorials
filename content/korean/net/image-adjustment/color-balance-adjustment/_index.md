---
title: .NET용 Aspose.PSD에서 색상 균형 조정 적용
linktitle: 색상 균형 조정 적용
second_title: Aspose.PSD .NET API
description: .NET용 Aspose.PSD의 색상 균형 조정 기능을 사용하여 PSD 이미지 색상을 손쉽게 향상하세요. 놀라운 결과를 얻으려면 단계별 가이드를 따르십시오.
type: docs
weight: 14
url: /ko/net/image-adjustment/color-balance-adjustment/
---
## 소개

.NET용 Aspose.PSD에서 색상 균형 조정을 적용하는 방법에 대한 포괄적인 가이드에 오신 것을 환영합니다! Aspose.PSD는 개발자가 PSD 파일을 효율적으로 사용할 수 있게 해주는 강력한 .NET 라이브러리입니다. 이 튜토리얼에서는 PSD 이미지의 색상 균형을 쉽게 향상시킬 수 있는 색상 균형 조정 기능에 중점을 둘 것입니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET 라이브러리용 Aspose.PSD: 다음에서 라이브러리를 다운로드하고 설치합니다.[Aspose.PSD 웹사이트](https://releases.aspose.com/psd/net/).
- 개발 환경: 컴퓨터에 작동하는 .NET 개발 환경이 설정되어 있는지 확인하세요.
- PSD 파일: 색상 균형 조정을 적용할 PSD 파일을 준비합니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.PSD 기능을 사용하는 데 필요한 네임스페이스를 포함합니다. 코드에 다음 줄을 추가합니다.

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

이제 색상 균형 조정 프로세스를 여러 단계로 나누어 보겠습니다.

## 1단계: PSD 파일 로드

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // 색상 균형 조정을 위한 코드는 다음 단계에서 추가됩니다.
}
```

## 2단계: 색상 균형 액세스 및 조정

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## 3단계: 조정된 이미지 저장

```csharp
im.Save(outputPath);
```

이제 .NET용 Aspose.PSD를 사용하여 PSD 파일에 색상 균형 조정을 성공적으로 적용했습니다!

## 결론

축하해요! .NET용 Aspose.PSD를 사용하여 PSD 이미지의 색상 균형을 향상시키는 방법을 배웠습니다. 원하는 시각 효과를 얻으려면 다양한 균형 값을 실험해 보세요.

## FAQ

### Q1: 색상 균형 조정을 여러 레이어에 적용할 수 있습니까?

A1: 예, PSD 파일의 모든 레이어를 반복하고 필요에 따라 색상 균형을 조정할 수 있습니다.

### Q2: Aspose.PSD for .NET은 PSD 파일의 일괄 처리에 적합합니까?

A2: 물론이죠! Aspose.PSD는 PSD 파일에 대한 효율적인 일괄 처리 기능을 제공합니다.

### Q3: .NET용 Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?

 A3: 방문[Aspose.PSD 임시 라이센스](https://purchase.aspose.com/temporary-license/) 임시 라이센스를 위해.

### Q4: 더 많은 예제와 문서는 어디에서 찾을 수 있습니까?

 A4: 탐색해 보세요.[Aspose.PSD 문서](https://reference.aspose.com/psd/net/) 자세한 예시와 가이드를 확인하세요.

### Q5: .NET용 Aspose.PSD에 어떤 지원 옵션을 사용할 수 있나요?

 A5: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 커뮤니티 지원 및 토론을 위해.

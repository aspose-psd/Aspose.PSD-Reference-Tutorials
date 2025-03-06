---
title: .NET용 Aspose.PSD에 패턴이 있는 획 레이어 추가
linktitle: 패턴으로 획 레이어 추가
second_title: Aspose.PSD .NET API
description: .NET용 Aspose.PSD를 사용하여 스트로크 레이어와 패턴으로 PSD 파일을 향상하세요. 원활한 통합을 위한 단계별 가이드를 따르세요.
weight: 13
url: /ko/net/layer-effects/adding-stroke-layer-pattern/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.PSD에 패턴이 있는 획 레이어 추가

## 소개

스트로크 레이어와 패턴을 사용하여 PSD(Photoshop 문서) 파일을 향상하면 디자인에 역동적인 느낌을 더할 수 있습니다. 이 튜토리얼에서는 .NET용 Aspose.PSD를 활용하여 패턴이 있는 스트로크 레이어를 PSD 파일에 쉽게 추가하는 방법을 살펴보겠습니다. Aspose.PSD는 PSD 파일 조작에 대한 포괄적인 지원을 제공하는 강력한 .NET 라이브러리로, 개발자와 디자이너 모두에게 귀중한 도구입니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- C# 프로그래밍 언어에 대한 기본 지식.
- 컴퓨터에 Visual Studio가 설치되어 있습니다.
-  다운로드할 수 있는 .NET 라이브러리용 Aspose.PSD[여기](https://releases.aspose.com/psd/net/).

## 네임스페이스 가져오기

C# 코드에서 필요한 네임스페이스를 가져왔는지 확인하세요.

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## 1단계: 환경 설정

C# 코드에서 소스 및 출력 디렉터리를 정의하는 것부터 시작하세요.

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## 2단계: PSD 파일 로드

Aspose.PSD의 PsdImage 클래스를 사용하여 PSD 파일을 로드합니다.

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // PSD 파일을 처리하기 위한 코드는 여기에 있습니다.
}
```

## 3단계: 새 패턴 데이터 준비

새 패턴과 그 경계를 정의합니다.

```csharp
var newPattern = new int[]
{
    // 패턴 색상이 여기에 표시됩니다.
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## 4단계: 획 레이어 수정

스트로크 레이어에 액세스하고 해당 속성을 업데이트합니다.

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

// 획 속성 확인 및 업데이트
// ...

// 불투명도 및 혼합 모드 업데이트
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## 5단계: 패턴 정보 업데이트

PSD 파일의 패턴 정보를 업데이트합니다.

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        // 패턴 정보 업데이트를 위한 코드는 여기에 있습니다.
    }
}

// 수정된 PSD 파일을 저장합니다.
im.Save(exportPath);
```

## 6단계: 변경 사항 확인

수정된 PSD 파일을 로드하고 변경 사항을 확인합니다.

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    // 변경 사항을 확인하기 위한 코드가 여기에 있습니다.
}
```

## 결론

축하해요! .NET용 Aspose.PSD에서 패턴이 있는 획 레이어를 추가하는 방법을 성공적으로 배웠습니다. 이 다용도 라이브러리를 통해 개발자는 시각적으로 매력적인 디자인을 만들고 PSD 파일의 유연성을 향상시킬 수 있습니다.

## FAQ

### Q1: 모든 버전의 Visual Studio에서 .NET용 Aspose.PSD를 사용할 수 있습니까?

A1: 예, .NET용 Aspose.PSD는 다양한 버전의 Visual Studio와 호환됩니다.

### Q2: Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?

 A2: 방문[여기](https://purchase.aspose.com/temporary-license/) 임시면허를 취득하기 위해

### Q3: 테스트에 사용할 수 있는 샘플 PSD 파일이 있습니까?

 A3: 설명서에서 샘플 PSD 파일을 찾을 수 있습니다.[여기](https://reference.aspose.com/psd/net/).

### Q4: Aspose.PSD는 PSD 파일의 일괄 처리에 적합합니까?

A4: 물론 .NET용 Aspose.PSD는 일괄 처리에 대한 강력한 지원을 제공합니다.

### Q5: 어디에서 도움을 구하거나 커뮤니티 토론에 참여할 수 있습니까?

 A5: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 지원 및 지역 사회 상호 작용을 위해.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

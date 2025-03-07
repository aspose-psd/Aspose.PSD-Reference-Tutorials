---
title: .NET용 Aspose.PSD에서 타임라인 작업
linktitle: 타임라인 작업
second_title: Aspose.PSD .NET API
description: .NET Timeline 클래스용 Aspose.PSD를 사용하여 PSD 이미지 조작을 향상시킵니다. 프레임 속성, 레이어 상태를 제어하고 창의적인 가능성을 손쉽게 활용하세요.
weight: 16
url: /ko/net/psd-file-manipulation/timeline/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.PSD에서 타임라인 작업

## 소개
그래픽 디자인과 이미지 조작의 역동적인 세계에서는 이미지의 타임라인을 제어하고 조작하는 능력이 매우 중요합니다. .NET용 Aspose.PSD는 Timeline 클래스를 통해 강력한 솔루션을 제공합니다. 이 고급 기능을 통해 사용자는 프레임 지연 변경, 특정 프레임의 레이어 상태 편집 등과 같은 PsdImage의 타임라인을 변경할 수 있습니다.
## 전제조건
Timeline 클래스가 제공하는 흥미로운 가능성을 살펴보기 전에 다음 전제 조건이 갖추어져 있는지 확인하십시오.
-  .NET 라이브러리용 Aspose.PSD: .NET 라이브러리용 Aspose.PSD가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[.NET 문서용 Aspose.PSD](https://reference.aspose.com/psd/net/).
-  문서 및 출력 디렉터리: 코드에서 문서 및 출력 디렉터리의 경로를 정의합니다. 조정하다`baseDir` 그리고`outputDir` 프로젝트 구조에 따른 변수.
이제 Timeline 클래스를 활용하는 방법을 단계별로 살펴보겠습니다.
## 네임스페이스 가져오기
Timeline 클래스 작업을 시작하려면 코드에서 필요한 네임스페이스를 가져옵니다.
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## 1단계: PSD 이미지 로드
지정된 소스 파일에서 PSD 이미지를 로드하는 것으로 시작합니다. 소스 파일 경로가 올바르게 설정되었는지 확인하세요.
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //추가 작업을 위한 코드는 여기에 있습니다.
}
```
## 2단계: 타임라인에 액세스
PSD 이미지가 로드되면 다음 코드를 사용하여 타임라인에 액세스합니다.
```csharp
Timeline timeline = psdImage.Timeline;
```
## 3단계: 폐기 방법 변경
특정 프레임의 처리 방법을 조작합니다. 이 예에서는 프레임 1의 삭제 방법을 변경합니다.
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## 4단계: 프레임 지연 조정
특정 프레임의 지연을 수정합니다. 여기서는 프레임 2의 지연을 15로 변경합니다.
```csharp
timeline.Frames[1].Delay = 15;
```
## 5단계: 레이어 상태 편집
특정 프레임에서 '레이어 1'의 불투명도를 변경합니다. 이 예에서는 프레임 2의 불투명도를 50으로 설정했습니다.
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## 6단계: 레이어 이동
'레이어 1'을 특정 프레임(이 예에서는 프레임 3)의 왼쪽 하단 모서리로 이동합니다.
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## 7단계: 새 프레임 추가
타임라인에 새 프레임을 추가합니다.
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## 8단계: 블렌드 모드 변경
특정 프레임(이 경우 프레임 4)에서 '레이어 1'의 혼합 모드를 변경합니다.
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## 9단계: 변경 사항 저장
PsdImage 인스턴스에 변경 사항을 다시 적용하고 수정된 PSD 이미지를 저장합니다.
```csharp
psdImage.Save(outputPsd);
```
## 10단계: 정리
마지막으로 임시 출력 파일을 삭제하여 정리합니다.
```csharp
File.Delete(outputPsd);
```
## 결론

결론적으로, .NET용 Aspose.PSD의 Timeline 클래스를 사용하면 개발자가 PSD 이미지의 타임라인을 세부적으로 제어할 수 있습니다. 일련의 간단한 단계를 통해 프레임 속성, 레이어 상태 등을 조작하여 창의적인 가능성의 영역을 열어줄 수 있습니다.

## FAQ

### Q1: Aspose.PSD for .NET은 초보자에게 적합합니까?

A1: 물론이죠! .NET용 Aspose.PSD는 사용자 친화적인 인터페이스와 포괄적인 문서를 제공하므로 초보자와 노련한 개발자 모두가 액세스할 수 있습니다.

### Q2: 타임라인 변경 사항을 GIF 이미지에 적용할 수 있나요?

A2: Timeline 클래스는 PSD 이미지용으로 특별히 설계되었습니다. GIF 조작에 대해서는 .NET용 Aspose.GIF를 참조하세요.

### Q3: 추가 지원을 찾거나 문제를 논의할 수 있는 곳은 어디입니까?

 A3: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 커뮤니티 지원 및 문제 토론을 위해.

### Q4: .NET용 Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?

 A4: 임시 라이센스 취득[여기](https://purchase.aspose.com/temporary-license/).

### Q5: .NET용 Aspose.PSD를 사용하면 어떤 주요 이점이 있습니까?

A5: .NET용 Aspose.PSD는 고급 이미지 처리 기능, PSD 파일 조작 및 고성능 렌더링을 제공합니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

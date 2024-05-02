---
title: .NET용 Aspose.PSD에서 이미지 흐리게 하기
linktitle: 이미지 흐리게 하기
second_title: Aspose.PSD .NET API
description: .NET용 Aspose.PSD를 사용하여 손쉽게 이미지를 흐리게 하는 방법을 알아보세요. C# 프로젝트에서 원활한 이미지 조작을 위한 단계별 가이드입니다.
type: docs
weight: 13
url: /ko/net/image-adjustment/blur-image/
---
## 소개

.NET 개발 영역에서 Aspose.PSD는 이미지 조작을 위한 강력한 동맹임이 입증되었습니다. 이 튜토리얼은 .NET용 Aspose.PSD를 사용하여 이미지를 흐리게 하는 특정 작업에 중점을 둡니다. 이미지 처리 기술을 강화하고 싶거나 프로그래밍 방식으로 이미지를 흐리게 하는 효율적인 방법을 찾고 있다면 잘 찾아오셨습니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.PSD: Aspose.PSD 라이브러리가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/psd/net/).

- 개발 환경: .NET 개발 환경을 설정하고 C#에 대한 기본적인 이해가 있어야 합니다.

- 샘플 이미지: PSD 형식의 샘플 이미지를 준비합니다. 직접 사용하거나 테스트용으로 다운로드할 수 있습니다.

## 네임스페이스 가져오기

C# 코드에서 필요한 네임스페이스를 가져오는 것부터 시작하세요.

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## 1단계: 문서 디렉터리 정의

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";
```

## 2단계: 이미지 로드

```csharp
//ExStart:Bluran이미지

string sourceFile = dataDir + @"sample.psd";

// RasterImage 클래스의 인스턴스에 기존 이미지 로드
using (var image = Image.Load(sourceFile))
{
    // 이 using 블록 내에서 다음 단계를 계속 진행하세요.
}
```

## 3단계: 이미지를 RasterImage로 변환

```csharp
RasterImage rasterImage = (RasterImage)image;
```

## 4단계: 가우시안 흐림 필터 적용

```csharp
rasterImage.Filter(rasterImage.Bounds, new GaussianBlurFilterOptions(15, 15));
```

 여기서는`GaussianBlurFilterOptions` 클래스는 수평 및 수직 흐림 모두에 대해 지정된 반경 15로 활용됩니다.

## 5단계: 흐린 이미지 저장

```csharp
string destName = dataDir + @"BlurAnImage_out.gif";
rasterImage.Save(destName, new GifOptions());
```

## 결론

축하해요! .NET용 Aspose.PSD를 사용하여 이미지를 성공적으로 흐리게 했습니다. 이 튜토리얼은 Aspose.PSD의 기능을 간략하게 소개하고 .NET 애플리케이션에서 이미지 조작을 위한 수많은 가능성을 열어줍니다.

## FAQ

### Q1: 이미지의 각 부분에 서로 다른 흐림 강도를 적용할 수 있습니까?

A1: 예, Aspose.PSD를 사용하면 이미지의 특정 영역에 다양한 매개변수가 포함된 필터를 적용하여 흐림 프로세스를 세부적으로 제어할 수 있습니다.

### Q2: Aspose.PSD는 모든 이미지 형식과 호환됩니까?

A2: Aspose.PSD는 광범위한 이미지 형식을 지원하지만 전체 목록과 형식별 고려 사항은 설명서를 확인하는 것이 좋습니다.

### Q3: Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?

 A3: 다음에서 임시 라이센스를 취득할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/) 테스트 및 평가 목적으로.

### Q4: Aspose.PSD에는 다른 이미지 조작 기능이 있습니까?

A4: 물론이죠! Aspose.PSD는 크기 조정, 자르기, 색상 조정을 포함한 포괄적인 기능 세트를 제공합니다. 전체 목록을 보려면 설명서를 살펴보세요.

### Q5: 어디서 도움을 구하거나 Aspose.PSD 커뮤니티에 연결할 수 있나요?

 A5: 질문이나 토론이 있는 경우[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34).
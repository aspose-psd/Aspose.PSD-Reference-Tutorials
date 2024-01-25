---
title: .NET용 Aspose.PSD에서 감마 조정 구현
linktitle: 감마 조정 구현
second_title: Aspose.PSD .NET API
description: 감마 조정 구현에 대한 단계별 가이드를 통해 .NET용 Aspose.PSD의 강력한 기능을 살펴보세요. 이미지 밝기와 대비를 손쉽게 미세 조정하세요.
type: docs
weight: 12
url: /ko/net/image-adjustment/gamma-adjustment/
---
## 소개

.NET용 Aspose.PSD에서 감마 조정 구현에 대한 포괄적인 가이드에 오신 것을 환영합니다! 감마 조정은 이미지의 밝기와 대비를 미세 조정할 수 있는 중요한 이미지 처리 기술입니다. 이 튜토리얼에서는 .NET용 강력한 Aspose.PSD 라이브러리를 사용하는 프로세스를 안내합니다.

## 전제 조건

구현을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET 라이브러리용 Aspose.PSD: .NET용 Aspose.PSD 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/psd/net/).

- .NET Framework: 이 자습서에서는 사용자가 .NET 개발에 대한 기본 지식을 갖고 있고 .NET Framework가 설치되어 있다고 가정합니다.

- IDE(통합 개발 환경): Visual Studio 등 .NET 개발을 위해 선호하는 IDE를 선택합니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.PSD 작업에 필요한 네임스페이스를 가져오는 것부터 시작하세요.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## 1단계: 프로젝트 설정

선택한 IDE에서 새 .NET 프로젝트를 만듭니다. Aspose.PSD 라이브러리에 대한 참조를 추가했는지 확인하세요.

## 2단계: 문서 디렉터리 정의

```csharp
string dataDir = "Your Document Directory";
```

## 3단계: 이미지 로드

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // 이 using 블록 내에서 추가 단계가 수행됩니다.
}
```

## 4단계: RasterImage 및 캐시 데이터로 캐스팅

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## 5단계: 감마 조정

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## 6단계: TiffOptions 생성 및 저장

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## 결론

축하해요! .NET용 Aspose.PSD를 사용하여 감마 조정을 성공적으로 구현했습니다. 이 강력한 라이브러리는 이미지 처리를 위한 강력한 기능을 제공하므로 .NET 개발자에게 유용한 도구입니다.

## FAQ

### Q1: Aspose.PSD 설명서는 어디서 찾을 수 있나요?

 A1: 문서를 참조할 수 있습니다.[여기](https://reference.aspose.com/psd/net/).

### Q2: .NET용 Aspose.PSD를 어떻게 다운로드합니까?

 A2: 라이브러리를 다운로드할 수 있습니다.[여기](https://releases.aspose.com/psd/net/).

### Q3: 무료 평가판이 제공됩니까?

 A3: 예, 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.PSD에 대한 지원은 어디서 받을 수 있나요?

 A4: 지원 포럼을 방문할 수 있습니다.[여기](https://forum.aspose.com/c/psd/34).

### Q5: 임시 라이센스가 필요합니까?

 A5: 필요한 경우 임시 라이센스를 취득할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).
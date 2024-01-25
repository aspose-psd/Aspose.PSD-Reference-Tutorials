---
title: .NET용 Aspose.PSD에서 직사각형으로 이미지 자르기
linktitle: 직사각형으로 이미지 자르기
second_title: Aspose.PSD .NET API
description: Aspose.PSD를 사용하여 .NET 이미지 조작 기술을 향상하세요. 정확성을 위해 직사각형을 사용하여 이미지 자르기를 단계별로 알아보세요.
type: docs
weight: 11
url: /ko/net/image-manipulation/crop-image-rectangle/
---
## 소개

.NET 프로그래밍 영역에서는 이미지를 조작하고 향상시키는 것이 일반적인 작업이며 .NET용 Aspose.PSD는 이 프로세스를 단순화하는 강력한 라이브러리입니다. 이 튜토리얼은 기본적이면서도 중요한 이미지 조작 기술, 즉 이미지를 직사각형으로 자르는 기술에 중점을 둡니다. 이 가이드를 마치면 .NET용 Aspose.PSD를 사용하여 이미지를 정밀하게 자르는 방법을 확실하게 이해하게 될 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.PSD: 라이브러리가 설치되어 있는지 확인하세요. 그렇지 않은 경우 다운로드할 수 있습니다.[여기](https://releases.aspose.com/psd/net/).

- 문서 디렉터리: 이미지 파일이 저장되는 디렉터리를 설정합니다.

- 통합 개발 환경(IDE): 원활한 코딩을 위해 Visual Studio와 같은 .NET 호환 IDE를 활용합니다.

## 네임스페이스 가져오기

시작하려면 프로젝트에 필요한 네임스페이스를 포함하세요.

```csharp
using Aspose.PSD.ImageOptions;
```

## 1단계: 문서 디렉터리 설정

문서 디렉토리의 경로를 지정하여 시작하십시오.

```csharp
string dataDir = "Your Document Directory";
```

## 2단계: 이미지 로드 및 캐시

소스 파일에서 이미지를 로드하고 해당 데이터를 캐시합니다.

```csharp
//ExStart:직사각형으로 자르기
string sourceFile = dataDir + @"sample.psd";

// RasterImage 클래스의 인스턴스에 기존 이미지 로드
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // 후속 단계에 대한 코드가 여기에 표시됩니다.
}
//ExEnd:직사각형으로 자르기
```

## 3단계: 자르기 직사각형 정의

 인스턴스를 생성합니다.`Rectangle` 자르기에 원하는 크기를 가진 클래스:

```csharp
// 원하는 크기로 Rectangle 클래스의 인스턴스를 만듭니다.
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

## 4단계: 자르기 작업 수행

 자르기 작업을 수행합니다.`RasterImage` 정의된 직사각형을 사용하는 객체:

```csharp
rasterImage.Crop(rectangle);
```

## 5단계: 결과 저장

자른 이미지를 지정된 형식(이 경우 JPEG)으로 디스크에 저장합니다.

```csharp
string destName = dataDir + @"CroppingByRectangle_out.jpg";
rasterImage.Save(destName, new JpegOptions());
```

필요에 따라 이 단계를 반복하여 다양한 자르기 시나리오에 맞게 직사각형 매개변수를 조정합니다.

## 결론

결론적으로, .NET용 Aspose.PSD를 사용하여 직사각형으로 이미지를 자르는 기술을 익히면 이미지 조작에 대한 가능성의 세계가 열립니다. 이 자습서에서는 이 기능을 .NET 애플리케이션에 원활하게 통합하기 위한 필수 단계를 제공합니다.

## FAQ

### Q1: .NET용 Aspose.PSD는 모든 이미지 형식과 호환됩니까?

A1: 예, .NET용 Aspose.PSD는 JPEG, PNG, SVG, TIFF, BMP, GIF, PSD 및 Jpeg2000을 포함한 광범위한 형식을 지원합니다.

### Q2: 동일한 이미지에 여러 자르기 작업을 적용할 수 있습니까?

A2: 물론이죠! 여러 자르기 작업을 순차적으로 수행하여 원하는 결과를 얻을 수 있습니다.

### Q3: .NET용 Aspose.PSD로 처리된 이미지에 크기 제한이 있습니까?

A3: .NET용 Aspose.PSD는 다양한 크기의 이미지를 처리하도록 설계되었습니다. 그러나 매우 큰 이미지로 작업할 때는 시스템 리소스와 메모리를 고려하십시오.

### Q4: .NET용 Aspose.PSD에 사용할 수 있는 평가판이 있습니까?

 A4: 예, 무료 평가판을 통해 도서관의 기능을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q5: 추가 지원은 어디서 찾을 수 있나요?

 A5: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)지역 사회와 연결하고 지원을 구합니다.
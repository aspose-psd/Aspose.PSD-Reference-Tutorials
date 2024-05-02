---
title: .NET용 Aspose.PSD에서 이미지 확장 및 자르기
linktitle: 이미지 확장 및 자르기
second_title: Aspose.PSD .NET API
description: .NET용 Aspose.PSD를 사용하여 이미지를 동적으로 확장하고 자르는 방법을 알아보세요. 원활한 이미지 조작을 위한 단계별 가이드를 따르세요.
type: docs
weight: 13
url: /ko/net/image-manipulation/expand-crop-images/
---
## 소개

.NET용 Aspose.PSD는 개발자가 .NET 애플리케이션에서 다양한 이미지 형식으로 작업할 수 있는 포괄적인 이미징 라이브러리입니다. 뛰어난 기능 중 하나는 이미지를 쉽게 조작할 수 있다는 것입니다. 이 튜토리얼에서는 이미지 확장 및 자르기에 중점을 두고 Aspose.PSD를 사용하여 이러한 작업을 수행하기 위한 실습 가이드를 제공합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET 라이브러리용 Aspose.PSD: .NET 라이브러리용 Aspose.PSD가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[.NET 문서용 Aspose.PSD](https://reference.aspose.com/psd/net/).

- 샘플 이미지: 튜토리얼에 사용할 샘플 이미지 파일(예: "example1.psd")을 준비합니다.

이제 단계별 가이드를 시작해 보겠습니다.

## 네임스페이스 가져오기

.NET용 Aspose.PSD에서 제공하는 기능을 활용하려면 필요한 네임스페이스를 가져오는 것부터 시작하세요. 코드에 다음 네임스페이스를 추가합니다.

```csharp
using Aspose.PSD.ImageOptions;
```

## 1단계: 프로젝트 설정

 .NET용 Aspose.PSD가 통합된 프로젝트가 설정되어 있는지 확인하세요. 그렇지 않은 경우 다음을 따르십시오.[선적 서류 비치](https://reference.aspose.com/psd/net/) 안내를 위해.

## 2단계: 이미지 로드

다음 코드를 사용하여 샘플 이미지를 로드합니다.

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// 이미지 로드
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // 이미지 처리를 위한 추가 코드가 여기에 표시됩니다.
}
```

## 3단계: 이미지 데이터 캐시

성능을 최적화하기 위해 이미지 데이터를 캐시합니다.

```csharp
rasterImage.CacheData();
```

## 4단계: 대상 직사각형 정의

Rectangle 클래스의 인스턴스를 만들고 직사각형의 X, Y, 너비 및 높이를 정의합니다. 이는 이미지가 확장되거나 잘리는 영역이 됩니다.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## 5단계: 출력 이미지 저장

지정된 옵션과 대상 직사각형을 사용하여 출력 이미지를 저장합니다.

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## 결론

축하해요! .NET용 Aspose.PSD를 사용하여 이미지를 확장하고 자르는 방법을 성공적으로 배웠습니다. 이 강력한 라이브러리는 .NET 애플리케이션 내에서 이미지 조작에 대한 가능성의 세계를 열어줍니다.

## FAQ

### Q1: Aspose.PSD는 PSD 외에 다른 이미지 형식도 처리할 수 있나요?

A1: 예, Aspose.PSD는 JPEG, PNG, GIF 등을 포함한 광범위한 이미지 형식을 지원합니다.

### Q2: Aspose.PSD에 대한 지원은 어디서 찾을 수 있나요?

 답변 2: 다음에서 지원을 찾고 커뮤니티에 참여할 수 있습니다.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34).

### Q3 .NET용 Aspose.PSD에 대한 무료 평가판이 있습니까?

 A3: 예, 다음에서 제공되는 무료 평가판을 통해 기능을 탐색할 수 있습니다.[Aspose.PSD 무료 평가판](https://releases.aspose.com/).

### Q4: Aspose.PSD에 대한 임시 라이선스를 어떻게 얻나요?

 A4: 다음에서 임시 라이센스를 받을 수 있습니다.[Aspose.PSD 임시 라이센스](https://purchase.aspose.com/temporary-license/).

### Q5: .NET용 Aspose.PSD를 어디서 구입할 수 있나요?

 A5: 도서관은 다음에서 구입할 수 있습니다.[Aspose.PSD 구매 페이지](https://purchase.aspose.com/buy).
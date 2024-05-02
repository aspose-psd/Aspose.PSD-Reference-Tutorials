---
title: .NET용 Aspose.PSD에서 특정 각도로 이미지 회전
linktitle: 특정 각도로 이미지 회전하기
second_title: Aspose.PSD .NET API
description: .NET용 Aspose.PSD의 강력한 기능을 살펴보세요. 특정 각도로 이미지를 쉽게 회전할 수 있습니다. 라이브러리를 다운로드하고 이미지를 원활하게 조작해 보세요.
type: docs
weight: 16
url: /ko/net/image-manipulation/rotate-image-specific-angle/
---
.NET을 사용하여 이미지 조작의 세계를 탐구하고 있다면 Aspose.PSD가 강력한 솔루션을 제공합니다. 이 튜토리얼에서는 Aspose.PSD를 사용하여 이미지를 특정 각도로 회전하는 과정을 안내합니다. 단계를 시작하기 전에 소개를 통해 기본을 설정해 보겠습니다.

## 소개

.NET용 Aspose.PSD는 개발자가 PSD 및 래스터 이미지 형식을 원활하게 사용할 수 있도록 지원하는 다목적 라이브러리입니다. 주요 기능 중 하나는 이미지를 정확한 각도로 회전시켜 이미지 조작에 유연성을 제공하는 기능입니다. 이 튜토리얼은 .NET용 Aspose.PSD를 사용하여 특정 각도로 이미지를 회전하는 단계를 안내합니다.

## 전제 조건

이 여정을 시작하기 전에 다음과 같은 전제 조건이 갖추어져 있는지 확인하세요.

-  .NET 라이브러리용 Aspose.PSD: 다음에서 라이브러리를 다운로드하고 설치합니다.[다운로드 페이지](https://releases.aspose.com/psd/net/).
- 문서 디렉터리: 소스 및 출력 파일을 저장할 디렉터리를 설정합니다.

## 네임스페이스 가져오기

시작하려면 .NET 프로젝트에서 필요한 네임스페이스를 가져옵니다.

```csharp
using Aspose.PSD.ImageOptions;
```

이제 단계별 가이드 형식으로 예제를 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 설정

```csharp
string dataDir = "Your Document Directory";
```

 바꾸다`"Your Document Directory"` 소스 및 출력 파일을 저장하는 디렉터리 경로를 사용합니다.

## 2단계: 이미지 로드

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // 여기에 추가 단계가 삽입됩니다.
}
```

 회전하려는 이미지를 인스턴스로 로드합니다.`RasterImage`.

## 3단계: 이미지 데이터 캐시

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

회전 중 성능 향상을 위해 이미지 데이터를 캐시합니다.

## 4단계: 이미지 회전

```csharp
image.Rotate(20f, true, Color.Red);
```

비례적인 크기를 유지하고 빨간색 배경을 사용하여 이미지를 20도 회전합니다.

## 5단계: 결과 저장

```csharp
image.Save(destName, new JpegOptions());
```

지정된 옵션으로 회전된 이미지를 저장합니다(이 경우 JPEG로).

## 결론

 축하해요! .NET용 Aspose.PSD를 사용하여 이미지를 특정 각도로 성공적으로 회전했습니다. 이 라이브러리는 이미지 조작을 위한 강력한 도구 세트를 제공하며 이 튜토리얼은 빙산의 일각에 불과합니다. 탐색[선적 서류 비치](https://reference.aspose.com/psd/net/) 더 많은 기능과 옵션을 확인하세요.

## FAQ

### Q1: 이미지를 20도 이외의 각도로 회전할 수 있나요?

 A1: 예, 각도 매개변수를 사용자 정의할 수 있습니다.`image.Rotate` 방법을 원하는 값으로 설정합니다.

### Q2: Aspose.PSD는 JPEG 외에 다른 이미지 형식을 지원합니까?

A2: 물론이죠! Aspose.PSD는 PNG, GIF, BMP 및 TIFF를 포함한 광범위한 형식을 지원합니다.

### Q3: 회전 전에 이미지 데이터를 캐싱해야 합니까?

A3: 필수는 아니지만 데이터 캐싱은 특히 큰 이미지의 경우 성능을 크게 향상시킬 수 있습니다.

### Q4: Aspose.PSD 관련 쿼리에 대한 지원은 어디서 받을 수 있나요?

 A4: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 커뮤니티 지원 및 토론을 위해.

### Q5: 구매하기 전에 Aspose.PSD를 사용해 볼 수 있나요?

 A5: 물론이죠! 당신의[무료 시험판](https://releases.aspose.com/) 도서관의 기능을 탐색합니다.
---
title: .NET용 Aspose.PSD에서 이미지 크기를 비례적으로 조정하기
linktitle: 이미지 크기를 비례적으로 조정
second_title: Aspose.PSD .NET API
description: .NET용 Aspose.PSD를 사용하여 원활한 이미지 크기 조정을 살펴보세요. 라이브러리를 다운로드하고 튜토리얼을 따라 이미지 처리 기능을 향상시켜 보세요.
type: docs
weight: 14
url: /ko/net/image-manipulation/resize-images-proportionally/
---
이미지 조작 영역에서 .NET용 Aspose.PSD는 개발자에게 이미지 크기를 비례적으로 쉽게 조정할 수 있는 기능을 제공하는 강력한 툴킷으로 돋보입니다. 이 단계별 가이드에서는 .NET용 Aspose.PSD를 사용하여 이미지 크기를 조정하여 이미지의 비율이 완벽하게 유지되도록 하는 과정을 안내합니다.

## 소개

이미지 크기를 비례적으로 조정하는 것은 많은 응용 프로그램에서 일반적인 작업이며 .NET용 Aspose.PSD는 개발자를 위해 이 프로세스를 단순화합니다. 웹 애플리케이션, 데스크탑 소프트웨어, 모바일 앱 등 어떤 작업을 하든 시각적 매력과 일관성을 유지하려면 이미지의 종횡비를 유지하면서 이미지 크기를 조정하는 방법을 이해하는 것이 중요합니다.

## 전제조건

.NET용 Aspose.PSD를 사용하여 크기 조정 마법을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1.  .NET 라이브러리용 Aspose.PSD: .NET 라이브러리용 Aspose.PSD가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[.NET 릴리스용 Aspose.PSD](https://releases.aspose.com/psd/net/) 페이지.

2. 문서 디렉터리: 문서를 저장할 디렉터리를 만들고 제공된 코드의 "문서 디렉터리"를 이 디렉터리의 실제 경로로 바꿉니다.

이제 전제 조건이 설정되었으므로 단계별 가이드로 넘어가겠습니다.

## 네임스페이스 가져오기

```csharp
using Aspose.PSD.ImageOptions;
```

필요한 클래스와 메서드에 액세스하려면 필요한 네임스페이스를 가져옵니다.

## 1단계: 이미지 로드

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// RasterImage 클래스의 인스턴스에 기존 이미지 로드
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// 나머지 단계는 여기로 이동합니다.
}
```

 다음을 사용하여 소스 이미지를 로드합니다.`Image.Load` 방법.

## 2단계: 너비와 높이 지정

```csharp
// 너비와 높이 지정
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

크기가 조정된 이미지의 새로운 너비와 높이를 결정합니다. 이 예에서는 너비와 높이가 절반으로 줄어들었지만 요구 사항에 따라 이러한 값을 조정할 수 있습니다.

## 3단계: 크기가 조정된 이미지 저장

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 다음을 사용하여 크기가 조정된 이미지를 저장합니다.`Save` 지정된 옵션을 사용하는 방법입니다. 이 경우에는 PNG 파일로 저장하겠습니다.

## 결론

.NET용 Aspose.PSD에서 이미지 크기를 비례적으로 조정하는 것은 이미지 처리 워크플로우에 가치를 추가하는 간단한 프로세스입니다. 이 가이드는 이 기능을 애플리케이션에 원활하게 통합하는 데 필요한 지식을 제공합니다.

## FAQ

### Q1: 이미지 크기를 특정 크기로 조정할 수 있나요?

A1: 예, 코드 요구 사항에 따라 새로운 너비와 높이를 사용자 정의할 수 있습니다.

### Q2: .NET용 Aspose.PSD는 일괄 이미지 크기 조정에 적합합니까?

A2: 물론이죠! 여러 이미지를 일괄 처리하기 위해 이러한 단계를 루프에 통합할 수 있습니다.

### Q3: .NET용 Aspose.PSD에는 다른 이미지 조작 기능이 있습니까?

A3: 예, .NET용 Aspose.PSD는 자르기, 회전, 이미지에 필터 적용 등 다양한 기능을 제공합니다.

### Q4: .NET용 Aspose.PSD에 대한 무료 평가판이 있습니까?

 A4: 예, 무료 평가판을 통해 .NET용 Aspose.PSD의 기능을 탐색할 수 있습니다. 방문하다[여기](https://releases.aspose.com/) 시작하려면.

### Q5: .NET용 Aspose.PSD에 대한 지원은 어디서 찾을 수 있습니까?

 A5: 다음을 방문하세요.[.NET 포럼용 Aspose.PSD](https://forum.aspose.com/c/psd/34) 커뮤니티 지원 및 토론을 위해.
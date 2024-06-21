---
title: .NET용 Aspose.PSD에서 이미지 회전
linktitle: 이미지 회전
second_title: Aspose.PSD .NET API
description: Aspose.PSD를 사용하여 .NET에서 이미지를 쉽게 회전하는 방법을 알아보세요. 단계별 튜토리얼을 따라해보세요.
type: docs
weight: 15
url: /ko/net/image-manipulation/rotate-image/
---
## 소개

.NET을 사용하여 이미지 조작의 세계에 뛰어들고 있다면 Aspose.PSD는 원활하고 효율적인 이미지 처리를 위한 최고의 도구입니다. 이 튜토리얼에서는 .NET용 Aspose.PSD를 사용하여 이미지를 회전하는 기본적인 작업에 중점을 둘 것입니다. 프로세스를 간단하고 실행 가능한 단계로 나누는 과정을 따라해보세요.

## 전제조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET 라이브러리용 Aspose.PSD: 다음에서 라이브러리를 다운로드하고 설치합니다.[Aspose.PSD .NET 문서](https://reference.aspose.com/psd/net/).

- 문서 디렉터리: 이미지가 저장되는 디렉터리를 설정합니다. 코드 조각의 "문서 디렉터리"를 이 디렉터리의 경로로 바꿉니다.

## 네임스페이스 가져오기

Aspose.PSD 기능에 액세스하려면 필요한 네임스페이스를 포함해야 합니다. .NET 프로젝트 시작 부분에 다음 줄을 추가합니다.

```csharp
using Aspose.PSD.ImageOptions;
```

## 1단계: 이미지 로드

```csharp
string sourceFile = dataDir + @"sample.psd";

// RasterImage 클래스의 인스턴스에 기존 이미지 로드
using (Image image = Image.Load(sourceFile))
{
```

## 2단계: 이미지 회전

```csharp
    // 이미지를 시계 방향으로 270도 회전합니다.
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## 3단계: 회전된 이미지 저장

```csharp
    // 회전된 이미지를 JPEG 파일로 저장
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

그게 다야! 단 몇 줄의 코드만으로 .NET용 Aspose.PSD를 사용하여 이미지를 성공적으로 회전했습니다.

## 결론

이 튜토리얼에서는 .NET용 Aspose.PSD를 사용하여 이미지 회전의 기본 사항을 살펴보았습니다. Aspose.PSD는 이미지 조작을 위한 강력한 도구 세트를 제공하므로 .NET 개발자에게 필수적인 라이브러리입니다. 다양한 회전을 실험하고 추가 기능을 탐색하여 이미지 처리 워크플로우를 향상하십시오.

## FAQ

### Q1: Aspose.PSD를 사용하여 사용자 정의 각도로 이미지를 회전할 수 있나요?

 예, Aspose.PSD를 사용하면 사용자 정의 회전 각도를 지정할 수 있습니다. 간단히 교체하십시오.`RotateFlipType.Rotate270FlipNone` 원하는 회전 각도로 선을 그으세요.

### Q2: Aspose.PSD는 다양한 이미지 형식과 호환됩니까?

 전적으로. Aspose.PSD는 PSD, JPEG, PNG 등을 포함한 광범위한 이미지 형식을 지원합니다. 을 체크 해봐[선적 서류 비치](https://reference.aspose.com/psd/net/) 전체 목록을 보려면.

### Q3: Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?

 방문하다[임시 라이센스 페이지](https://purchase.aspose.com/temporary-license/) Aspose 웹사이트에서 평가 목적으로 임시 라이선스를 얻으세요.

### Q4: Aspose.PSD에 대한 지원은 어디서 찾을 수 있나요?

 질문이나 도움이 필요하면 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 그리고 커뮤니티와 연결하세요.

### Q5: Aspose.PSD를 상업용으로 구입할 수 있나요?

 틀림없이. 탐색[구매 페이지](https://purchase.aspose.com/buy) 귀하의 필요에 맞는 라이센스를 취득하십시오.
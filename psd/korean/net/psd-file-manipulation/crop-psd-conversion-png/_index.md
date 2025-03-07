---
title: .NET용 Aspose.PSD에서 PNG로 변환할 때 PSD 파일 자르기
linktitle: PNG로 변환할 때 PSD 파일 자르기
second_title: Aspose.PSD .NET API
description: .NET용 Aspose.PSD를 사용하여 PSD 파일을 쉽게 자르는 방법을 알아보세요. PNG로 원활하게 변환하려면 단계별 가이드를 따르세요.
weight: 18
url: /ko/net/psd-file-manipulation/crop-psd-conversion-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.PSD에서 PNG로 변환할 때 PSD 파일 자르기

## 소개
.NET 개발 영역에서는 이미지를 조작하고 변환하는 것이 일반적인 작업입니다. .NET용 Aspose.PSD는 이 프로세스를 간소화하는 강력한 도구 세트를 제공합니다. 자주 발생하는 요구 사항 중 하나는 PSD 파일을 PNG로 변환하기 전에 자르는 것입니다. 이 단계별 튜토리얼에서는 .NET용 Aspose.PSD를 사용하는 프로세스를 자세히 살펴보겠습니다.
## 전제조건
이 여정을 시작하기 전에 다음 사항을 확인하세요.
-  .NET 라이브러리용 Aspose.PSD: 다음에서 라이브러리를 다운로드하고 설치합니다.[.NET 문서용 Aspose.PSD](https://reference.aspose.com/psd/net/).
- 샘플 PSD 파일: 실험용 PSD 파일을 준비합니다. 샘플이 없으면 자습서에 제공된 샘플을 사용할 수 있습니다.
- .NET 환경: 작동하는 .NET 개발 환경이 설정되어 있는지 확인하세요.
- 문서 디렉터리: 코드에 문서 디렉터리 경로를 지정합니다.
## 네임스페이스 가져오기
.NET 프로젝트에서 .NET용 Aspose.PSD에 필요한 네임스페이스를 포함합니다.
```csharp
using Aspose.PSD.ImageOptions;
```
## 1단계: PSD 이미지 로드
```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// 기존 PSD 이미지 로드
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // 추가 단계를 위한 코드가 여기에 표시됩니다.
}
```
## 2단계: 자르기 직사각형 정의
```csharp
// x, y, 너비 및 높이를 전달하여 Rectangle 클래스의 인스턴스를 만듭니다.
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## 3단계: 이미지 자르기
```csharp
// Image 클래스의 자르기 메소드를 호출하고 직사각형 클래스 인스턴스를 전달합니다.
image.Crop(cropRectangle);
```
## 4단계: PNG 옵션 지정
```csharp
// PngOptions 클래스의 인스턴스 만들기
PngOptions pngOptions = new PngOptions();
```
## 5단계: 자른 이미지를 PNG로 저장
```csharp
// 저장 메서드를 호출하고, 출력 경로를 제공하고, PngOptions를 제공하여 PSD 파일을 PNG로 변환하고 출력을 저장합니다.
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## 결론

축하해요! .NET용 Aspose.PSD를 사용하여 PSD 파일을 PNG로 변환할 때 자르는 방법을 성공적으로 배웠습니다. 이 기능은 다양한 이미지 처리 시나리오에서 매우 중요할 수 있습니다.

## FAQ

### Q1: 이 라이브러리를 상업용 프로젝트에 사용할 수 있나요?

 A1: 예, .NET용 Aspose.PSD는 상업용으로 사용할 수 있습니다. 참조[Aspose.PSD 라이센스](https://purchase.aspose.com/buy) 자세한 내용은.

### Q2: 무료 평가판을 이용할 수 있나요?

A2: 물론이죠! 무료 평가판을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: .NET용 Aspose.PSD에 대한 지원은 어디서 찾을 수 있습니까?

 A3: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 도움이나 문의사항이 있으면

### Q4: 임시 라이센스는 어떻게 얻나요?

 A4: 임시 라이센스가 필요한 경우 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 설명서에 사용 가능한 예제나 튜토리얼이 있습니까?

 A5: 예, 포괄적인 문서와 예제를 찾을 수 있습니다.[여기](https://reference.aspose.com/psd/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

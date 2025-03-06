---
title: PSD 파일의 렌더 곡선 조정 레이어 - Java
linktitle: PSD 파일의 렌더 곡선 조정 레이어 - Java
second_title: Aspose.PSD 자바 API
description: 이 상세한 단계별 가이드를 통해 Java용 Aspose.PSD를 사용하여 PSD 파일에서 곡선 조정 레이어를 렌더링하고 조정하는 방법을 알아보세요.
weight: 16
url: /ko/java/psd-layer-management-effects/render-curves-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD 파일의 렌더 곡선 조정 레이어 - Java

## 소개

Photoshop의 곡선 조정 레이어는 이미지를 향상시키는 마술 지팡이와 같습니다. 당신이 걸작의 색상과 톤을 조정하는 예술가라고 상상해 보십시오. 각 곡선 조정을 통해 빛과 색상 균형을 놀라울 정도로 정밀하게 제어할 수 있습니다. PSD 파일로 작업하고 이러한 곡선을 프로그래밍 방식으로 조작해야 하는 경우 Java용 Aspose.PSD가 가장 적합한 도구입니다. 이 가이드에서는 Java용 Aspose.PSD를 사용하여 PSD 파일에서 곡선 조정 레이어를 렌더링하고 조정하는 방법을 안내합니다. 이미지 톤을 업데이트하든 결과를 내보내든 이 튜토리얼에서는 시작하는 데 필요한 모든 것을 다룹니다.

## 전제조건

코딩 세부 사항을 살펴보기 전에 모든 설정이 완료되었는지 확인하겠습니다. 필요한 것은 다음과 같습니다.

1. JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요. Java용 Aspose.PSD에는 Java 8 이상이 필요합니다.
   
2.  Java 라이브러리용 Aspose.PSD: 다음에서 Java 라이브러리용 Aspose.PSD를 다운로드하세요.[Aspose 릴리스 페이지](https://releases.aspose.com/psd/java/). 

3. IDE(통합 개발 환경): IntelliJ IDEA 또는 Eclipse와 같은 모든 Java 호환 IDE가 작동합니다.

4. Java 프로그래밍의 기본 지식: Java 구문과 기본 프로그래밍 개념을 이해하면 튜토리얼을 따라가는 데 도움이 됩니다.

5. PSD 파일: 편집하려는 곡선 조정 레이어가 포함된 PSD 파일입니다. 

이러한 전제 조건을 갖추고 나면 PSD 파일 조작을 시작할 준비가 된 것입니다.

## 패키지 가져오기

우선 Aspose.PSD에서 필요한 패키지를 가져와야 합니다. 이러한 라이브러리는 곡선 레이어 읽기 및 수정을 포함하여 PSD 파일 작업을 처리합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
import com.aspose.psd.imageoptions.PngOptions;
```

## 1단계: PSD 파일 로드

 먼저 PSD 파일을 애플리케이션에 로드해야 합니다. 그만큼`PsdImage` Aspose.PSD의 클래스를 사용하면 PSD 파일을 열고 조작할 수 있습니다.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
PsdImage im = (PsdImage)Image.load(sourceFileName + ".psd");
```

 여기서 교체하세요`"Your Document Directory/CurvesAdjustmentLayer"` PSD 파일의 경로를 사용하세요. 이 코드 조각은 PSD 파일을`PsdImage` 물체.

## 2단계: 레이어를 통해 반복

PSD 파일에는 여러 레이어가 포함될 수 있습니다. 곡선 조정 레이어를 찾고 조작하려면 PSD 파일의 레이어를 반복해야 합니다.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof CurvesLayer) {
        CurvesLayer curvesLayer = (CurvesLayer)im.getLayers()[i];
        // 추가 작업은 여기에서 처리됩니다.
    }
}
```

이 루프는 각 레이어를 검사하여 해당 레이어가 인스턴스인지 확인합니다.`CurvesLayer`. 그렇다면 곡선 조정을 진행할 수 있습니다.

## 3단계: 곡선 레이어 수정

곡선 조정 레이어를 식별한 후에는 해당 설정을 수정할 수 있습니다. 레이어가 이산 관리자를 사용하는지, 연속 관리자를 사용하는지에 따라 접근 방식이 달라집니다.

### 이산 곡선 관리자 수정

 만약`CurvesLayer` 사용하다`CurvesDiscreteManager`, 곡선 점을 직접 조정할 수 있습니다.

```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();
    
    for (int k = 10; k < 50; k++) {
        manager.setValueInPosition(0, (byte)k, (byte)(15 + (k * 2)));
    }
}
```

이 스니펫에서는 개별적인 방식으로 곡선 값을 조정합니다. 여기에는 다양한 위치에 값을 설정하여 곡선 모양을 효과적으로 수정하는 작업이 포함됩니다.

### 연속 곡선 관리자 수정

 레이어를 사용하는 경우`CurvesContinuousManager`, 곡선 점을 추가합니다.

```java
else {
    CurvesContinuousManager manager = (CurvesContinuousManager)curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte)0, (byte)50, (byte)100);
    manager.addCurvePoint((byte)0, (byte)150, (byte)130);
}
```

이 코드는 두 개의 곡선 점을 추가하여 연속 값으로 곡선의 모양을 조정합니다. 

## 4단계: PSD 파일 저장

조정을 마친 후 수정된 PSD 파일을 저장합니다. 이 단계를 수행하면 모든 변경 사항이 저장됩니다.

```java
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
im.save(psdPathAfterChange + ".psd");
```

여기에서는 수정된 PSD 파일이 저장될 경로를 지정합니다. 

## 5단계: PNG로 내보내기

 조정된 PSD 파일을 PNG로 내보내려면`PngOptions` 그리고 파일을 저장하세요.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
String pngExportPath = dataDir + "CurvesAdjustmentLayerChanged";
im.save(pngExportPath + ".png", saveOptions);
```

이 조각은 알파 투명도가 포함된 색상 유형을 포함한 PNG 내보내기 옵션을 설정하고 파일을 PNG로 저장합니다.

## 결론

Java용 Aspose.PSD를 사용하여 PSD 파일에서 곡선 조정 레이어를 조작하는 것은 처음에는 복잡해 보일 수 있지만 이러한 단계별 지침을 사용하면 관리하기 쉽고 직관적이라는 것을 알게 될 것입니다. 이 가이드를 따르면 이미지 톤을 손쉽게 조정하고 결과를 다양한 형식으로 내보낼 수 있습니다. 프로젝트의 이미지를 향상시키거나 배치 프로세스를 자동화하든 Aspose.PSD는 전문적인 결과를 쉽게 달성하는 데 필요한 도구를 제공합니다.

## FAQ

### 곡선 조정 레이어란 무엇입니까?
Photoshop의 곡선 조정 레이어를 사용하면 RGB 곡선을 수정하여 이미지의 밝기와 대비를 조정할 수 있습니다. 톤 조정을 정밀하게 제어할 수 있습니다.

### 다른 이미지 형식과 함께 Java용 Aspose.PSD를 사용할 수 있나요?
예, Java용 Aspose.PSD는 주로 PSD 파일용이지만 편집한 이미지를 PNG, TIFF 및 JPEG와 같은 형식으로 내보낼 수 있습니다.

### Java용 Aspose.PSD를 사용하려면 Photoshop을 설치해야 합니까?
아니요, Java용 Aspose.PSD는 Photoshop과 독립적으로 작동하므로 프로그래밍 방식으로 PSD 파일을 조작할 수 있습니다.

### Java용 Aspose.PSD 무료 평가판을 어떻게 받을 수 있나요?
 다음 사이트에서 Java용 Aspose.PSD 무료 평가판을 다운로드할 수 있습니다.[Aspose 릴리스 페이지](https://releases.aspose.com/psd/java/).

### Java용 Aspose.PSD에 대한 지원은 어디서 찾을 수 있나요?
 지원을 받으려면 다음을 방문하세요.[Aspose 지원 포럼](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

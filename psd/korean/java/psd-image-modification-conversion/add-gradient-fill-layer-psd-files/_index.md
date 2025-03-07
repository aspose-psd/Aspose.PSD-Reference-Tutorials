---
title: Java를 사용하여 PSD 파일에 그라디언트 채우기 레이어 추가
linktitle: Java를 사용하여 PSD 파일에 그라디언트 채우기 레이어 추가
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일의 그라데이션 채우기 레이어를 수정합니다. 프로그래밍 방식으로 색상, 투명도 및 기타 그라데이션 속성을 변경하는 방법을 알아보세요.
weight: 15
url: /ko/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 PSD 파일에 그라디언트 채우기 레이어 추가

## 소개

PSD 파일에 시각적 마법을 더하고 싶었던 적이 있습니까? 그라디언트는 디자인에 깊이와 입체감을 더할 수 있는 놀라운 방법을 제공합니다. 하지만 Java를 사용하여 이러한 그라데이션을 프로그래밍 방식으로 조작하려면 어떻게 해야 할까요? Aspose.PSD가 구출해 드립니다! 이 포괄적인 가이드는 Aspose.PSD를 사용하여 PSD 파일 내에서 그라데이션 채우기 레이어를 수정할 수 있도록 지원하여 흥미로운 프로세스를 단계별로 안내합니다.

## 전제조건

다이빙을 시작하기 전에 다음 사항을 확인하세요.

-  JDK(Java Development Kit): Java 코드를 실행하려면 안정적인 버전의 JDK가 필요합니다. Oracle 웹사이트에서 다운로드할 수 있습니다.[Oracle JDK 다운로드 페이지 링크]
-  Aspose.PSD for Java: 이 강력한 라이브러리를 사용하면 Java 애플리케이션에서 PSD 파일로 작업할 수 있습니다. Aspose 웹사이트에서 다운로드하세요:[Java 다운로드를 위한 Aspose.PSD 링크] (무료 평가판 이용 가능)

## 패키지 가져오기

PSD 파일 작업에 필요한 필수 Aspose.PSD 패키지를 가져오는 것부터 시작해 보겠습니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

이러한 가져오기를 통해 PSD 파일을 로드, 조작 및 저장하기 위한 클래스 및 메서드에 액세스할 수 있습니다.

이제 그라디언트 채우기 레이어를 수정하는 흥미진진한 여정을 시작하세요!

## 1단계: PSD 파일 로드

 먼저 수정하려는 그래디언트 채우기 레이어가 포함된 PSD 파일을 로드해야 합니다. 사용`Image.load` 메서드, 파일 경로 지정:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

 이 코드 조각은 지정된 디렉터리에서 PSD 파일을 로드하고 이를`image` 변하기 쉬운.

## 2단계: 그라디언트 채우기 레이어 식별

 PSD 파일에는 수많은 레이어가 포함될 수 있습니다. 편집하려는 그라데이션 채우기가 포함된 특정 레이어를 분리해야 합니다. 다음을 통해 반복`image.getLayers()` 원하는 레이어를 찾기 위한 배열:

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // 여기에서 추가 확인 및 수정이 이루어집니다.
   break;
}
}
```

 이 루프는 각 레이어를 확인합니다. 레이어가`FillLayer` , 에 캐스팅되었습니다.`FillLayer` 입력하고 저장합니다.`fillLayer`추가 처리를 위한 변수입니다. 대상 레이어를 식별하기 위한 특정 기준(예: 레이어 이름)이 있는 경우 루프 내에 추가 검사를 추가할 수 있습니다.

## 3단계: 그라데이션 채우기 유형 확인

모든 채우기 레이어가 그라디언트를 활용하는 것은 아닙니다. 이 코드 조각은 식별된 레이어에 실제로 그라데이션 채우기가 포함되어 있는지 확인합니다.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

 만약`getFillType` 메소드가 반환되지 않습니다`FillType.Gradient`, 잘못된 레이어로 작업하고 있음을 나타내는 예외가 발생합니다.

## 4단계: 그라데이션 속성 액세스 및 수정

 여기서 마법이 일어납니다! Aspose.PSD는 다음을 통해 다양한 그라데이션 채우기 속성에 대한 액세스를 제공합니다.`IGradientFillSettings` 인터페이스. 필요에 따라 검색하고 수정할 수 있습니다.

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// 속성 수정(원하는 값으로 대체)
settings.setAngle(0.0);  // 각도를 0도로 설정
settings.setDither(false);  // 디더링 비활성화
settings.setAlignWithLayer(true); // 레이어에 그라디언트 정렬
settings.setReverse(true);  // 역방향 그라데이션 방향
settings.setHorizontalOffset(25);  // 수평 오프셋 설정
settings.setVerticalOffset(-15);  // 수직 오프셋 설정
```

 이 코드는`IGradientFillSettings`개체를 선택한 다음 각도, 디더링, 정렬 및 오프셋과 같은 속성을 수정합니다. 제공된 값을 원하는 설정으로 바꾸면 원하는 그라데이션 효과를 얻을 수 있습니다.

## 5단계: 색상 및 투명도 포인트 조작

그라데이션은 스펙트럼을 따라 색상 및 투명도 점으로 정의됩니다. Aspose.PSD를 사용하면 정확한 제어를 위해 다음 포인트를 수정할 수 있습니다.

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// 새로운 컬러 포인트 추가
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// 기존 색상 포인트 수정
colorPoints.get(1).setLocation(3000);

// 새로운 투명도 포인트 추가
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// 기존 투명점 수정
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

## 6단계: PSD 파일 업데이트 및 저장

필요한 수정을 완료한 후 채우기 레이어를 업데이트하고 PSD 파일을 저장합니다.

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

 그만큼`fillLayer.update()` 방법은 그라디언트 채우기 레이어에 변경 사항을 적용하고`image.save` 수정된 PSD 파일을 지정된 출력 경로에 저장합니다.

## 결론

Java용 Aspose.PSD를 사용하여 PSD 파일의 그라데이션 채우기 레이어를 수정하는 기술을 성공적으로 마스터했습니다! 다음 단계를 따르면 창의성을 발휘하고 프로그래밍 방식의 정확성으로 놀라운 시각 효과를 만들 수 있습니다.

## FAQ

### 그라디언트에 여러 색상 및 투명도 포인트를 추가할 수 있나요?
전적으로! 원하는 그라데이션 효과를 얻기 위해 필요한 만큼 색상 및 투명도 포인트를 추가할 수 있습니다. 새로운 포인트를 생성하고 해당 목록에 추가하기만 하면 됩니다.

### 그라디언트에서 색상이나 투명도 점을 어떻게 제거합니까?
 점을 제거하려면 해당 목록의`remove` 방법. 예를 들어,`colorPoints.remove(index)` 지정된 인덱스에서 색상 포인트를 제거합니다.

### 그라데이션 유형(선형, 방사형 등)을 변경할 수 있나요?
Aspose.PSD는 현재 선형 그래디언트를 지원합니다. 향후 버전에서는 다른 그라데이션 유형이 지원될 수도 있지만 색상 및 투명도 포인트를 창의적으로 조작하여 유사한 효과를 얻을 수 있습니다.

### 그라디언트를 수정하면 성능에 영향이 있나요?
성능에 미치는 영향은 그라데이션의 복잡성과 수정 횟수에 따라 달라집니다. 대부분의 실제 사용 사례에서는 성능이 허용 가능해야 합니다. 그러나 대규모 이미지 처리의 경우 효율성을 위해 코드를 최적화하는 것이 좋습니다.

### PSD 파일의 여러 그래디언트 채우기 레이어에 이 기술을 적용할 수 있습니까?
예, 레이어를 반복하고 기준에 맞는 각 그라디언트 채우기 레이어에 수정 사항을 적용할 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

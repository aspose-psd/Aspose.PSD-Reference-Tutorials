---
date: 2026-02-01
description: Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 새로운 PSD 레이어를 만드는 방법을 배웁니다. 이
  단계별 튜토리얼은 PSD 이미지 조작 및 PSD를 PNG로 변환하는 내용을 다룹니다.
linktitle: Add a New Regular Layer to PSD
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 새 일반 레이어 추가
url: /ko/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 새 일반 레이어 추가

## Introduction

이 **aspose psd tutorial**에서는 **export PSD to PNG**와 동시에 **creating a new regular layer**하는 방법을 알아봅니다. 웹용 썸네일을 생성하거나, 디자인 파이프라인을 위한 자산을 준비하거나, 단순히 실험하고 싶을 때, Aspose.PSD for Java는 완전한 프로그래밍 제어를 제공합니다. 소스 파일을 로드하는 것부터 업데이트된 PSD와 PNG 사본을 저장하는 단계까지 모두 안내하므로 바로 PSD 레이어를 조작할 수 있습니다.

## How to export PSD to PNG using Aspose.PSD

PSD를 PNG로 내보내는 것은 두 단계 과정입니다: 먼저 필요한 레이어를 추가Options`합니다 as PNG**를 한 번의 연속적인 작업으로 수행할 수 있습니다.

## What is a regular layer and why add a new PSD layer?

**regular layer**는 픽셀 데이터, 투명도 및 위치 정보를 보유할 수 있는 기본 래스터 레이어입니다. 새로운 PSD 레이어를 추가하면 기존 아트워크를 변경하지 않고 그래픽, 워터마크 또는 플레이스홀더를 삽입할 수 있습니다. 이는 자동 배치 처리용으로 프로그래용합니다 I `save`를 `PngOptions`와 함께 호출하면 됩니다.
- **Do I need a license for development?** 테스트용 임시 라이선스로 동작하며, 프로덕션에서는 정식 라이선스가 필요합니다.
- **Which Java version is supported?** Aspose.PSD는 Java 8 및 이후 버전을 지원합니다.
- **Is layer positioning pixel‑based?** 예, 왼쪽, 위, 오른쪽, 아래 좌표를 픽셀 단위로 설정합니다.
- **Will the PNG retain layer transparency?** PNG는 모든 보이는 레이어를 병합한 결과를 포함합니다.

## Prerequisites

- **Java Development Environment** – JDK 8 이상 및 빌드 도구(Maven/Gradle)가 설치되어 있어야 합니다.
- **Aspose.PSD for Java** – 공식 사이트에서 최신 JAR을 다운로드하십시오 [here](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – 예제에서는 `OneLayer.psd`를 사용합니다.

## Import Packages

Java 클래스에 필요한 import를 추가합니다. 이러한 클래스들은 **psd image manipulation** 및 레이어 처리를 위한 핵심 기능을 제공합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Step 1: Load the PSD File

먼저, 수정하려는 기존 PSD를 로드합니다. 이렇게 하면 작업할 수 있는 `PsdImage` 객체가 제공됩니다.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Step 2: Prepare Pixel Data and Rectangles

두 개의 픽셀 버퍼(`int[]`)를 만들고 새 레이어가 그려질 사각형의 기반이 됩니다.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Step 3: Initialize Layer Data

픽셀 버퍼를 기본 ARGB 값으로 채웁니다. 값 `-10000000`은 반투명 어두운 색조에 해당합니다.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Step 4: Add Regular Layers (Manipulate PSD Layers)

이제 PSD 이미지에 **add regular layers**를 추가하고 경계를 설정합니다. 이는 프로그래밍 방식으로 **manipulate PSD layers**하고 효과적으로 **add layer to PSD**하는 방법을 보여줍니다.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Step 5: Export PSD to PNG and Save the Updated PSD

레이d to png** 단계), 그 다음 새 레이어가 포함된 PSD를 저장합니다.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** PNG만 필요하면 PSD `save` 호출을 건너뛰고 `PngOptions`와 함께 `save`를 직접 호출하면 됩니다.

## Common Issues & Troubleshooting

| 증상 | 가능한 원인 | 해결 방법 |
|---------|--------------|-----|
| PNG가 빈 화면으로 표시됨 | 레이어가 보이지 않거나 완전히 투명함 | 비투명 픽셀 값을 설정하거나 `layer.setVisible(true)`를 호출했는지 확인하십시오. |
| `ArrayIndexOutOfBoundsException` | 사각형 크기와 픽셀 배열 길이가 일치하지 않음 | `rect.width * rect.height == dataArray.length`인지 확인하십시오. |
| 런타임 시 LicenseException | 유효한 라이선스가 로드되지 않음 | API 메서드를 호출하기 전에 임시 또는 영구 라이선스를 로드하십시오. |

## Frequently Asked Questions

**Q: Aspose.PSD가 Java 8과 호환되나요?**  
A: 예, Aspose.PSD는 Java 8 및 이후 버전을 지원합니다.

**Q: 추가된 레이어에 변환(회전, 스케일)을 적용할 수 있나요?**  
A: 물론입니다! `Layer` 클래스는 `rotate`, `scale`, `translate`와 같은 메서드를 제공하여 전체 변환을 제어할 수 있습니다.

**Q: 추가 Aspose.PSD 문서는 어디에서 찾을 수 있나요?**  
A: 자세한 API 문서는 [here](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

**Q: Aspose.PSD의 임시 라이선스는 어떻게 얻나요?**  
A: 임시 라이선스 페이지를 [here](https://purchase.aspose.com/temporary-license/)에서 방문하십시오.

**Q: Aspose.PSD 지원을 위한 커뮤니티 포럼이 있나요?**  
A: 예, Aspose 포럼에서 토론에 참여하십시오 [here](https://forum.aspose.com/c/psd/34).

## Conclusion

이제 Aspose.PSD for Java를 사용하여 **export PSD to PNG**와 동시에 **adding new regular layers**를 수행하는 방법을 배웠습니다. 이 워크플로는 핵심 **psd image manipulation** 기능을 보여줍니다: 파일 로드, 레이어 생성, 픽셀 데이터 채우기, 최종 구성보내기. 다양한 사험하여 프로젝트 요구에 맞게 출력물을 조정해 보세요.

**마지막 업데이트:** 2026-02-01  
 Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
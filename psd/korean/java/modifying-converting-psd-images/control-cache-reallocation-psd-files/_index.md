---
title: PSD 파일의 캐시 재할당 제어
linktitle: PSD 파일의 캐시 재할당 제어
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일의 캐시 재할당을 관리합니다. 개발자에게 이상적인 메모리 및 파일 처리를 효율적으로 최적화하는 방법을 알아보세요.
weight: 22
url: /ko/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD 파일의 캐시 재할당 제어

## 소개
이미지와 Photoshop 파일을 프로그래밍 방식으로 작업할 때 효율성이 핵심 요소입니다. Aspose.PSD for Java는 PSD 파일을 원활하게 관리하고 조작할 수 있는 강력한 기능을 제공합니다. 성능 최적화의 기본 측면 중 하나는 캐시 재할당을 제어하는 것입니다. 캐시 관리는 메모리와 디스크 사용량 사이의 균형을 유지하여 예상치 못한 충돌이나 속도 저하 없이 애플리케이션이 원활하게 실행되도록 보장합니다. 
## 전제조건
코딩 부분으로 넘어가기 전에 모든 것이 원활하게 실행되도록 확인해야 할 몇 가지 사항이 있습니다.
1. JDK(Java Development Kit): 컴퓨터에 JDK가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[오라클의 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Java용 Aspose.PSD: Aspose.PSD 라이브러리를 다운로드해야 합니다. 최신 릴리스를 찾을 수 있습니다[여기](https://releases.aspose.com/psd/java/).
3. IDE 설정: IntelliJ IDEA 또는 Eclipse와 같은 IDE(통합 개발 환경)를 사용하면 코드를 더 쉽게 관리할 수 있습니다.
4. Java의 기본 이해: Java 프로그래밍에 익숙하면 개념과 코드 조각을 더 잘 이해하는 데 도움이 됩니다.
5.  Aspose 라이선스(선택 사항): 워터마크를 제거하고 전체 기능을 얻으려면 라이선스 구매를 고려하세요.[여기](https://purchase.aspose.com/buy) 또는 무료 평가판을 사용해 보세요.[여기](https://releases.aspose.com/).
## 패키지 가져오기
코드 작성을 시작하기 전에 필요한 패키지를 가져왔는지 확인하겠습니다. 다음은 Java 파일 시작 부분에 포함할 항목에 대한 간략한 목록입니다.
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```
## 1단계: 데이터 디렉터리 설정
먼저, 캐시 파일을 저장할 디렉터리를 설정해야 합니다. 이는 캐시를 효과적으로 관리하는 데 필수적입니다.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: 문서 캐시의 디렉터리를 정의합니다.
- Cache.setCacheFolder(dataDir): 이 메소드는 캐시 폴더를 지정된 디렉토리로 설정합니다. Aspose로 생성된 모든 캐시는 이제 기본 임시 디렉터리 대신 여기에 저장됩니다.
## 2단계: 캐시-디스크 구성
다음으로 캐시를 디스크에만 저장하도록 지정하겠습니다. 이는 애플리케이션이 대용량 파일을 사용하고 메모리를 계속 사용 가능한 상태로 유지하려는 경우 특히 유용합니다.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): 이 옵션은 캐시가 메모리에 유지되지 않도록 보장하므로 너무 많은 RAM을 소비하지 않고 대용량 PSD 파일을 처리하는 데 유용합니다.
## 3단계: 최대 디스크 및 메모리 캐시 크기 설정
이제 캐시 크기를 제한해 보겠습니다. 무제한 캐시로 인해 성능 문제가 발생할 수 있으므로 이는 매우 중요합니다.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1기가바이트
Cache.setMaxMemoryForCache(1073741824); // 1기가바이트
```

- Cache.setMaxDiskSpaceForCache(1073741824): 디스크의 캐시 제한을 1GB로 설정합니다. 필요에 따라 이 크기를 조정할 수 있습니다.
- Cache.setMaxMemoryForCache(1073741824): 마찬가지로 이는 메모리 내 캐시를 제한하여 애플리케이션이 과도한 메모리를 사용하지 않도록 합니다.
## 4단계: 캐시 재할당 전략 관리
성능을 유지하려면 캐시가 재할당되는 방식을 관리하는 것이 필수적입니다. 설정 방법은 다음과 같습니다.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): false로 설정하면 Aspose가 캐시 재할당을 보다 유연하게 관리할 수 있어 성능이 향상될 수 있습니다.
## 5단계: 할당된 캐시 크기 확인
이 단계에서는 메모리나 디스크의 캐시에 현재 할당된 바이트 수를 모니터링하는 단계입니다. 이를 구현해 보겠습니다.
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: 디스크에 할당된 바이트 수를 저장합니다.
- long l2: 메모리에 할당된 바이트 수를 저장합니다. 
언제든지 이러한 값을 확인하여 애플리케이션이 예상대로 메모리 및 디스크 사용량을 관리하고 있는지 확인할 수 있습니다.
## 6단계: PSD 이미지 만들기
이제 캐시 구성이 설정되었으므로 간단한 PSD 이미지를 만들어 보겠습니다.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- PsdOptions 옵션: 이 개체를 사용하면 Photoshop 이미지를 만들 때 옵션을 지정할 수 있습니다.
- 색상[] 색상: 이미지 팔레트에 사용될 색상이 포함된 배열입니다.
## 7단계: 이미지에 픽셀 데이터 저장
이제 이미지를 픽셀 데이터로 채우고 저장해 보겠습니다.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- 색상[] 픽셀: 색상 객체의 배열입니다. 여기서는 흰색 픽셀로 채워보겠습니다.
- image.savePixels(image.getBounds(), 픽셀): 이 메소드는 픽셀 데이터를 이미지에 저장합니다. 우리가 정의한 색상으로 이미지를 업데이트합니다.
## 8단계: 이미지 생성 후 할당된 캐시 모니터링
이미지를 생성한 후에는 캐시에 할당된 바이트 수를 다시 확인하는 것이 좋습니다.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: 이미지 생성 후 디스크의 현재 할당을 캡처합니다.
- long memoryBytes: 메모리의 현재 할당을 캡처합니다. 
이 단계는 작업 후 소비되는 캐시의 양을 결정하는 데 도움이 됩니다.
## 9단계: 적절한 폐기 여부 확인
마지막으로 메모리 누수를 방지하려면 모든 Aspose.PSD 개체가 올바르게 삭제되었는지 확인하는 것이 중요합니다.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 및 l2: 이 변수는 최종 할당을 확인하는 데 도움이 됩니다. 0이 아닌 경우 일부 개체가 제대로 삭제되지 않았음을 나타냅니다.
## 결론
Java용 Aspose.PSD에서 캐시 재할당을 제어하면 애플리케이션 성능에 상당한 차이를 만들 수 있습니다. 위에 설명된 단계를 따르면 캐시를 효과적으로 관리하고, 메모리 사용량을 최소화하며, 아름다운 PSD 파일을 효율적으로 만들 수 있습니다. 이러한 기술을 수용하고 최적의 성능으로 애플리케이션이 번성하는 것을 지켜보십시오!
## FAQ
### Aspose.PSD란 무엇인가요?
Aspose.PSD는 .NET 및 Java 개발자가 Photoshop(PSD) 파일을 프로그래밍 방식으로 생성, 조작 및 변환할 수 있는 라이브러리입니다.
### 할당된 캐시 크기를 어떻게 확인하나요?
 다음과 같은 방법을 사용하십시오.`Cache.getAllocatedDiskBytesCount()` 그리고`Cache.getAllocatedMemoryBytesCount()` 현재 캐시 사용량을 모니터링합니다.
### 캐시에 대한 사용자 정의 디렉터리를 설정할 수 있나요?
 예, 다음을 사용하여 다른 디렉터리를 지정할 수 있습니다.`Cache.setCacheFolder("Your Directory Path")`.
### Aspose.PSD는 무료로 사용할 수 있나요?
Aspose.PSD는 유료 라이브러리이지만 다음에서 제공되는 무료 평가판으로 시작할 수 있습니다.[웹사이트](https://releases.aspose.com/).
### 물건을 처리하지 않으면 어떻게 되나요?
객체를 삭제하지 않으면 메모리 누수가 발생하여 애플리케이션이 필요 이상으로 더 많은 리소스를 사용하게 될 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

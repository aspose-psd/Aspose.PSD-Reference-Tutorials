---
date: 2026-01-01
description: XMP 메타데이터를 생성하고, PSD 파일에 XMP를 추가하며, Aspose.PSD for Java를 사용하여 이미지 메타데이터를
  업데이트하는 방법을 배워보세요. 지금 바로 이 단계별 가이드를 따라하세요.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 XMP 메타데이터 만들기
url: /ko/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 XMP 메타데이터 만들기

## Introduction

Photoshop (PSD) 파일을 다루는 Java 개발자에게 이미지 메타데이터 관리는 일반적인 요구 사항입니다. 이 튜토리얼에서는 Aspose.PSD 라이브러리를 사용하여 **XMP 메타데이터를 만드는 방법**을 배우고, PSD 이미지에 XMP를 추가하며, 프로그래밍 방식으로 이미지 메타데이터를 업데이트하는 방법을 다룹니다. 각 단계를 차근차근 살펴보고, 각 요소가 왜 중요한지 설명하며, 실제 프로젝트에 적용할 수 있는 실용적인 팁을 제공하겠습니다.

## Quick Answers
- **What is XMP metadata?** 이미지 파일 내부에 설명 정보를 삽입하기 위한 표준화된 형식(작성자, 키워드 등)입니다.  
- **Why use Aspose.PSD?** Photoshop 없이도 PSD 파일을 생성, 읽기, 편집할 수 있는 순수 Java API를 제공합니다.  
- **Can I add XMP to an existing PSD?** 예 — `setXmpData`를 사용해 실시간으로 이미지 메타데이터를 업데이트할 수 있습니다.  
- **What are the main steps?** 이미지 크기 설정, 헤더/트레일러 생성, XMP 패키지 구축, 패키지 첨부, 저장 순서입니다.  
- **Do I need a license?** 개발 단계에서는 무료 체험판으로 충분하지만, 상용 환경에서는 상업용 라이선스가 필요합니다.

## What is “create XMP metadata” in Java?

XMP 메타데이터를 만든다는 것은 이미지에 대한 설명을 담은 XMP 패킷(헤더, 본문, 트레일러)을 구성한 뒤, 해당 패킷을 PSD 파일에 삽입하는 것을 의미합니다. Aspose.PSD 라이브러리는 저수준 세부 사항을 추상화하여 저장하고자 하는 내용에 집중할 수 있게 해줍니다.

## Why add XMP to PSD files?

- **Searchability:** 작성자, 제목, 사용자 정의 태그 등을 기반으로 강력한 자산 관리 검색이 가능합니다.  
- **Interoperability:** XMP는 Adobe 제품, Lightroom 및 다수의 DAM 시스템에서 인식됩니다.  
- **Version control:** 처리 이력(예: 도시, 색상 모드)을 파일 내부에 직접 저장할 수 있습니다.

## Prerequisites

- **Java Development Environment:** JDK 8 이상 설치 및 Java에 대한 기본 이해가 필요합니다.  
- **Aspose.PSD Library:** Aspose.PSD for Java 라이브러리를 다운로드하고 설정합니다. 라이브러리와 자세한 문서는 [here](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.  
- **Your Document Directory:** 시스템에서 PSD 파일을 읽고 쓸 위치를 결정합니다.

## Import Packages

Java 프로젝트에서 Aspose.PSD 기능을 활용하기 위해 필요한 패키지를 가져옵니다:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Step 1: Specify Image Size

새 PSD 이미지의 캔버스 크기를 정의합니다.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Step 2: Create a New Image

이후 XMP 메타데이터를 추가할 빈 PSD 이미지를 생성합니다.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Step 3: Create XMP Header

헤더에는 XML 처리 지시문과 문서를 식별하는 GUID가 포함됩니다.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Step 4: Create XMP Trailer

트레일러는 XMP 패킷의 끝을 표시합니다. `true` 플래그를 설정하면 닫는 처리 지시문이 기록됩니다.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Step 5: Create XMP Metadata

핵심 XMP 메타데이터 객체에 작성자 및 설명과 같은 일반 속성을 추가합니다.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Step 6: Create XMP Packet Wrapper

헤더, 트레일러 및 핵심 메타데이터를 하나의 패킷으로 감싸 이미지에 첨부할 수 있게 합니다.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Step 7: Set Photoshop Attributes

많은 Adobe 도구가 기대하는 Photoshop 전용 필드(도시, 국가, 색상 모드 등)를 채웁니다.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Step 8: Add Photoshop Package to XMP Metadata

Photoshop 패키지를 XMP 패킷에 첨부합니다.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Step 9: Set DublinCore Attributes

작성자, 제목 및 사용자 정의 영화 태그와 같은 Dublin Core 메타데이터를 추가합니다.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Step 10: Add DublinCore Package to XMP Metadata

기존 XMP 패킷에 Dublin Core 패키지를 결합합니다.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Step 11: Update XMP Metadata into Image

완성된 XMP 패킷을 PSD 이미지에 삽입합니다.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Step 12: Save Image

메타데이터가 포함된 PSD 파일을 디스크(또는 메모리 스트림)로 저장합니다.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Common Issues and Solutions

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **`NullPointerException` on `setXmpData`** | XMP 패킷이 완전히 구성되지 않아(헤더/트레일러 누락) 발생합니다. | `XmpHeaderPi`, `XmpTrailerPi`를 생성하고 모든 패키지를 추가한 뒤 `setXmpData`를 호출하십시오. |
| **Metadata not visible in Photoshop** | Photoshop이 XMP 패킷이 올바르게 래핑되기를 기대합니다. | `XmpTrailerPi(true)`가 사용되었는지 확인하고, 패킷이 이미지와 함께 저장되었는지 검증하십시오. |
| **File path errors** | 상대 경로 사용 시 권한이 부족할 수 있습니다. | 절대 경로를 사용하거나 대상 폴더에 대한 쓰기 권한을 확보하십시오. |

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with different image formats?**  
A: Yes, Aspose.PSD supports PSD, PSB, BMP, GIF, JPEG, PNG, TIFF, and more, giving you flexibility across formats.

**Q: Can I manipulate existing metadata using Aspose.PSD?**  
A: Absolutely. You can load an existing PSD, retrieve its XMP data with `getXmpData()`, modify the packet, and save it back.

**Q: Are there any limitations on the image size Aspose.PSD can handle?**  
A: Aspose.PSD is designed to work with large images (up to several gigapixels) limited only by available memory.

**Q: Is there a trial version available for Aspose.PSD?**  
A: Yes, you can explore the capabilities of Aspose.PSD by obtaining a free trial [here](https://releases.aspose.com/).

**Q: Where can I seek support for Aspose.PSD-related queries?**  
A: For any assistance or queries, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

## Conclusion

이제 **XMP 메타데이터를 만드는 방법**, PSD에 XMP를 추가하는 방법, 그리고 Aspose.PSD for Java를 사용해 이미지 메타데이터를 업데이트하는 방법을 마스터했습니다. 이러한 단계들을 통해 이미지에 삽입되는 설명 정보를 완전히 제어할 수 있어 검색 가능하고, 워크플로우에 바로 활용할 수 있습니다. 추가적인 XMP 스키마를 실험하거나 이 코드를 더 큰 이미지 처리 파이프라인에 통합해 보세요.

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
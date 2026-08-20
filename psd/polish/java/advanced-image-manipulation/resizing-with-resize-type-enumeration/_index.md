---
date: 2026-06-03
description: Dowiedz się, jak zmienić rozmiar obrazu przy użyciu Aspose.PSD dla Javy.
  Ten przewodnik krok po kroku omawia enumerację Resize Type, wysokiej jakości zmianę
  rozmiaru obrazu oraz konwersję PSD do JPEG.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Zmiana rozmiaru przy użyciu enumeracji Resize Type
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Jak zmienić rozmiar obrazu w Javie przy użyciu enumeracji Resize Type
url: /pl/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zmienić rozmiar obrazu w Javie przy użyciu wyliczenia typu zmiany rozmiaru

## Wprowadzenie

If you’re looking for **jak zmienić rozmiar obrazu** files efficiently in a Java project, Aspose.PSD for Java provides a clean, high‑performance API. In this tutorial we’ll walk through loading a PSD, applying the **Resize Type Enumeration** for high‑quality image resize, and finally **konwertować PSD do JPEG**. Whether you’re building a desktop editor or an automated server‑side pipeline, these steps let you control dimensions, quality, and format with just a few lines of code.

## Szybkie odpowiedzi
- **Jaka biblioteka obsługuje zmianę rozmiaru obrazu w Javie?** Aspose.PSD for Java.
- **Jaki typ zmiany rozmiaru daje najlepszą jakość?** `ResizeType.LanczosResample`.
- **Czy mogę konwertować PSD do JPEG po zmianie rozmiaru?** Yes – simply save with `JpegOptions`.
- **Czy potrzebuję licencji do produkcji?** A valid Aspose.PSD license is required for production use.
- **Czy to podejście jest odpowiednie dla dużych partii?** Absolutely; the API processes multi‑hundred‑page files without loading the whole document into memory.

## Co to jest „jak zmienić rozmiar obrazu” w Javie?

**Jak zmienić rozmiar obrazu** odnosi się do programowego zmieniania wymiarów pikselowych obrazu przy zachowaniu wizualnej wierności. Aspose.PSD’s `Resize` method combined with the `ResizeType` enumeration delivers precise control over scaling algorithms, allowing developers to maintain quality across a wide range of source files and target sizes.

## Dlaczego używać wyliczenia Resize Type?

`ResizeType` pozwala wybrać algorytm resamplingu, który najlepiej równoważy szybkość i jakość wizualną. W większości scenariuszy **LanczosResample** zapewnia ostre wyniki przy umiarkowanym koszcie wydajności, przetwarzając obraz 2000 × 1500 w mniej niż 120 ms na typowym procesorze klasy serwerowej, zachowując szczegóły krawędzi.

## Prerequisites

Before you start, make sure you have:

1. **Środowisko programistyczne Java** – JDK 8 or newer installed and configured.  
2. **Biblioteka Aspose.PSD** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).  
3. **Przykładowy plik PSD** – Use the [sample.psd](Your Document Directory/sample.psd) file included with the SDK for hands‑on testing.

## Importowanie pakietów

`Image` is the base class for all image types in Aspose.PSD. Add the required imports to your Java source file:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 1: Załaduj obraz

### Definicja kotwicy
The `RasterImage` class is Aspose.PSD’s core object that represents a raster‑based image loaded from a PSD file.

Load your PSD into a `RasterImage` instance so you can manipulate its pixels:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Krok 2: Zmień rozmiar obrazu

`image.resize(width, height, resizeType)` zmienia rozmiar obrazu do określonych wymiarów przy użyciu wybranego algorytmu.

Now resize the loaded image using the **Resize Type Enumeration**. In this example we use the Lanczos Resample method, which is ideal when you **jak zmienić rozmiar obrazu** with high quality:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Krok 3: Zapisz zmieniony rozmiar obrazu

`image.save(path, options)` writes the image to disk in the format defined by the provided options.

After resizing, save the image with the specified dimensions and the chosen resize type. Here, we also demonstrate **konwersję psd do jpeg** by saving the result as a JPEG file:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Dlaczego używać wyliczenia Resize Type?

`ResizeType` daje precyzyjną kontrolę nad algorytmem resamplingu, pozwalając na zrównoważenie szybkości i jakości. Dla większości aplikacji `LanczosResample` oferuje doskonały kompromis, dostarczając ostre wyniki bez dużego obciążenia wydajności, i działa dobrze w różnych treściach obrazu.

## Typowe problemy i rozwiązania

- **Obraz jest rozmyty po zmianie rozmiaru** – Spróbuj innego `ResizeType`, takiego jak `Bicubic` lub `NearestNeighbour`, aby zobaczyć, który daje najlepszy rezultat wizualny dla konkretnego obrazu.  
- **OutOfMemoryError przy dużych plikach PSD** – Przetwarzaj obraz w mniejszych fragmentach lub zwiększ rozmiar sterty JVM (flaga `-Xmx`). Aspose.PSD może obsługiwać pliki do **2 GB** bez ładowania całego dokumentu do pamięci.

## FAQ

### P1: Czy Aspose.PSD for Java jest odpowiedni zarówno dla małych, jak i dużych projektów?

O1: Zdecydowanie! Aspose.PSD for Java jest zaprojektowany tak, aby obsługiwać projekty każdej wielkości, zapewniając skalowalność i wydajność.

### P2: Czy mogę użyć innego typu zmiany rozmiaru niż Lanczos Resample?

O2: Tak, Aspose.PSD for Java oferuje różne typy zmiany rozmiaru, takie jak **NearestNeighbour**, **Bicubic**, i inne. Consult the API docs for the full list.

### P3: Gdzie mogę znaleźć dodatkowe wsparcie dla Aspose.PSD for Java?

O3: For any queries or assistance, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### P4: Czy dostępna jest darmowa wersja próbna Aspose.PSD for Java?

O4: Yes, you can access a free trial version [here](https://releases.aspose.com/).

### P5: Jak mogę uzyskać tymczasową licencję dla Aspose.PSD for Java?

O5: To obtain a temporary license, visit [this link](https://purchase.aspose.com/temporary-license/).

## Najczęściej zadawane pytania

**P: Jak programowo konwertować plik PSD na JPEG bez zmiany rozmiaru?**  
O: Load the PSD with `Image.load`, then call `image.save("output.jpg", new JpegOptions());`.

**P: Czy można zachować oryginalne DPI przy zmianie rozmiaru?**  
O: Yes, you can set the `Resolution` property on the `Image` object before saving.

**P: Czy mogę łączyć wiele operacji zmiany rozmiaru?**  
O: While you can call `resize` multiple times, it’s more efficient to calculate the final dimensions and resize once.

---

**Ostatnia aktualizacja:** 2026-06-03  
**Testowano z:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane tutoriale

- [Proste zmienianie rozmiaru z Aspose.PSD – Biblioteka manipulacji obrazami Java](/psd/java/basic-image-operations/simple-resizing/)
- [Skalowanie obrazu wysokiej jakości z Bicubic Resampler w Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Jak konwertować PSD do PNG i zmieniać rozmiar proporcjonalnie z Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
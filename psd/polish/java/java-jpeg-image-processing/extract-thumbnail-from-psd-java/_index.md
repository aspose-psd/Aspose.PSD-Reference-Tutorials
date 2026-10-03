---
date: 2026-10-03
description: Dowiedz się, jak wyodrębnić miniaturę z pliku PSD w Javie przy użyciu
  Aspose.PSD. Ten przewodnik krok po kroku obejmuje konfigurację, fragmenty kodu oraz
  zapisywanie miniatury jako obrazu JPEG.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Wyodrębnij miniaturę z pliku PSD w Javie
og_description: Dowiedz się, jak wyodrębnić miniaturę z pliku PSD w Javie przy pomocy
  Aspose.PSD. Ten przewodnik prowadzi Cię przez konfigurację, wczytywanie pliku, wyodrębnianie
  miniatury i zapisywanie jej jako obrazu JPEG.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Wyodrębnij miniaturę z pliku PSD w Javie przy użyciu Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Wyodrębnij miniaturę z pliku PSD w Javie
url: /pl/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wyodrębnianie miniatury z PSD w Javie

## Wprowadzenie
Wyodrębnianie miniatury z pliku PSD pozwala generować szybkie podglądy bez ładowania obrazu w pełnej rozdzielczości. W Javie Aspose.PSD upraszcza ten proces, zapewniając wydajność. W tym samouczku dowiesz się, jak skonfigurować bibliotekę, zlokalizować zasób miniatury i zapisać go jako plik JPEG — wszystko w kilku linijkach kodu.

## Szybkie odpowiedzi
- **Która biblioteka obsługuje miniatury PSD?** Aspose.PSD for Java.  
- **Ile linii kodu jest wymaganych?** Około pięciu linii, aby załadować, wyodrębnić i zapisać.  
- **Czy mogę wyodrębniać miniatury z dużych plików PSD?** Tak, Aspose.PSD przetwarza pliki do 500 MB bez pełnego ładowania do pamięci.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna wystarcza do oceny; licencja jest wymagana w produkcji.  
- **Jakie formaty wyjściowe są obsługiwane?** Wyodrębnioną miniaturę można zapisać jako JPEG, PNG lub BMP.

## Czym jest wyodrębnianie miniatury z PSD?
Wyodrębnianie miniatury z PSD to proces odczytywania małego obrazu podglądowego osadzonego wewnątrz dokumentu Photoshop (PSD). Ten podgląd jest przechowywany jako zasób i może być zapisany niezależnie w celu katalogowania lub wyświetlania. Miniatura jest zazwyczaj niskiej rozdzielczości i służy aplikacjom do szybkiego przedstawienia wizualnego bez ładowania pełnowymiarowego obrazu.

## Dlaczego używać Aspose.PSD do tego zadania?
Aspose.PSD obsługuje **ponad 30 formatów obrazów** i może radzić sobie z plikami PSD do **500 MB**, jednocześnie utrzymując niskie zużycie pamięci, ponieważ odczytuje zasoby na żądanie. API zapewnia także solidną obsługę błędów, dzięki czemu możesz niezawodnie wyodrębniać miniatury nawet z uszkodzonych plików.

## Wymagania wstępne
Przed rozpoczęciem upewnij się, że masz:
- Zainstalowany Java Development Kit (JDK).  
- Bibliotekę Aspose.PSD for Java pobraną z [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).  
- Podstawową znajomość składni Java oraz konfiguracji projektu.

## Jak wyodrębnić miniaturę z pliku PSD w Javie?
Załaduj plik PSD przy użyciu `PsdImage`, zlokalizuj `ThumbnailResource` i zapisz jego dane obrazu jako JPEG. Aspose.PSD abstrahuje niskopoziomowe parsowanie, więc wystarczy wywołać `getResources()` i następnie `save()` na wyodrębnionym obrazie. To podejście działa dla każdego PSD zawierającego miniaturę, niezależnie od rozmiaru pliku.

## Importowanie pakietów
`Image` jest klasą bazową do ładowania obrazów. `PsdImage` reprezentuje dokument PSD. `ThumbnailResource` i `Thumbnail4Resource` reprezentują zasoby miniatur. `JpegOptions` określa opcje zapisu JPEG.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Krok 1: załaduj plik PSD
Najpierw utwórz instancję `PsdImage`, wskazującą na Twój plik PSD. Konstruktor odczytuje tylko nagłówek i niezbędne zasoby, co minimalizuje zużycie pamięci.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Zastąp `"Your_Document_Directory/"` ścieżką do katalogu, w którym znajduje się Twój plik PSD, oraz `"your_file.psd"` nazwą tego pliku.

## Krok 2: iteruj zasoby obrazu
Aspose.PSD przechowuje miniatury jako obiekty `ThumbnailResource` w kolekcji zasobów obrazu. Przejdź pętlą po kolekcji, sprawdź typ zasobu i przechwyć pierwszą napotkaną miniaturę.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Krok 3: zapisz wyodrębnioną miniaturę
Gdy masz już obraz miniatury, wywołaj jego metodę `save`, aby zapisać go na dysku. Możesz wybrać JPEG, PNG lub BMP; JPEG jest najczęściej używany do podglądów w sieci.

## Krok 4: obsługa różnych typów miniatur
Jeśli PSD zawiera wiele wariantów miniatur, np. `Thumbnail4Resource`, rozszerz logikę iteracji, aby sprawdzać każdy typ. API udostępnia osobne klasy dla każdego zasobu, co pozwala wybrać pożądaną rozdzielczość.

## Typowe problemy i rozwiązania
- **Nie znaleziono miniatury:** Nie wszystkie pliki PSD zawierają podgląd. Zweryfikuj plik w panelu „Plik → Informacje o pliku” w Photoshopie.  
- **Błąd nieobsługiwanego formatu:** Upewnij się, że używasz najnowszej wersji Aspose.PSD; starsze wydania mogą nie obsługiwać nowszych typów zasobów miniatur.  
- **Brak pamięci przy dużych plikach:** Użyj `PsdImage.load(..., LoadOptions)` z `LoadOptions.setLoadResourcesOnly(true)`, aby uniknąć ładowania pełnych danych obrazu, gdy potrzebna jest tylko miniatura.

## Najczęściej zadawane pytania

**Q: What is Aspose.PSD?**  
A: Aspose.PSD is a Java library that enables programmatic creation, manipulation, and conversion of PSD and other raster image formats without requiring Adobe Photoshop.

**Q: Where can I find more documentation on Aspose.PSD for Java?**  
A: You can refer to the [documentation](https://reference.aspose.com/psd/java/) for detailed API references and examples.

**Q: Can I try Aspose.PSD for free before purchasing?**  
A: Yes, you can download a [free trial](https://releases.aspose.com/) to evaluate the library’s capabilities.

**Q: How can I obtain a temporary license for Aspose.PSD?**  
A: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/) page.

**Q: Is Aspose.PSD suitable for commercial use?**  
A: Yes, Aspose.PSD can be used in both personal and commercial projects under its licensing terms.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## Powiązane samouczki

- [How to Convert PSD to Raster Image Formats with Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)
- [Save PSD as JPEG and Support RGB Color with Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
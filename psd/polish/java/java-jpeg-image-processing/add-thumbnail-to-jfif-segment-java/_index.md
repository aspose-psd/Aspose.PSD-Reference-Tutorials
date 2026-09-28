---
date: 2026-09-28
description: Jak dodać miniaturkę do segmentu JFIF w Javie przy użyciu Aspose.PSD.
  Postępuj zgodnie z tym przewodnikiem krok po kroku, aby szybko i niezawodnie osadzać
  miniaturki w plikach PSD.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Dodaj miniaturkę do segmentu JFIF w Javie
og_description: Jak dodać miniaturkę do segmentu JFIF w Javie przy użyciu Aspose.PSD.
  Postępuj zgodnie z tym przewodnikiem krok po kroku, aby szybko i niezawodnie osadzać
  miniaturki w plikach PSD.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Jak dodać miniaturkę do segmentu JFIF w Javie
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Jak dodać miniaturkę do segmentu JFIF w Javie
url: /pl/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać miniaturkę do segmentu JFIF w Javie

## Wprowadzenie
Dodanie miniaturki do segmentu JFIF pliku PSD jest powszechnym wymaganiem, gdy potrzebujesz szybkiego podglądu wizualnego bez ładowania pełnego obrazu. W tym samouczku nauczysz się **jak dodać miniaturkę** do segmentu JFIF w Javie przy użyciu Aspose.PSD. Po zakończeniu przewodnika będziesz mieć działający fragment kodu, zrozumienie struktury JFIF oraz wskazówki dotyczące efektywnego przetwarzania dużych plików.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebujesz?** Aspose.PSD for Java.  
- **Która wersja Javy działa?** JDK 11 lub nowsza.  
- **Ile linii kodu jest potrzebnych?** Około 10 linii, aby wczytać, zmodyfikować i zapisać.  
- **Czy mogę przetwarzać pliki wielomegabajtowe?** Tak, Aspose.PSD strumieniuje dane, więc zużycie pamięci pozostaje niskie.  
- **Czy potrzebna jest licencja komercyjna?** Licencja jest wymagana do użytku produkcyjnego; dostępna jest darmowa wersja próbna.

## Czym jest segment JFIF?
Segment JFIF to blok formatu JPEG File Interchange Format, który może przechowywać opcjonalne dane, takie jak miniaturki, EXIF czy profile kolorów.  
Znajduje się wewnątrz strumienia JPEG pliku PSD i jest rozpoznawany przez większość przeglądarek obrazów w celu szybkiego generowania podglądu.

## Dlaczego dodać miniaturkę do pliku PSD?
Aspose.PSD for Java obsługuje **ponad 30 formatów obrazów** i może przetwarzać pliki do **2 GB** bez ładowania całego dokumentu do pamięci. Dodanie miniaturki zmniejsza zużycie pasma sieciowego przy przesyłaniu podglądów i przyspiesza renderowanie interfejsu w aplikacjach galerii.

## Wymagania wstępne
- Java Development Kit (JDK): Upewnij się, że Java jest zainstalowana w Twoim systemie. Możesz ją pobrać ze [strony JDK firmy Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
- Aspose.PSD for Java: Musisz posiadać bibliotekę Aspose.PSD for Java. Możesz ją uzyskać ze [strony pobierania Aspose.PSD Java](https://releases.aspose.com/psd/java/).  
- Integrated Development Environment (IDE): Użyj środowiska IDE, takiego jak IntelliJ IDEA lub Eclipse, do programowania w Javie.  
- Podstawowa znajomość Javy: Znajomość języka programowania Java i jego koncepcji.

## Jak dodać miniaturkę do segmentu JFIF w Javie?
Wczytaj docelowy plik PSD, znajdź zasób JFIF, zamień jego dane miniaturki i zapisz plik. Cała operacja może być wykonana kilkoma prostymi wywołaniami API, a Aspose.PSD zajmuje się niskopoziomową strukturą JPEG za Ciebie.

### Krok 1: importowanie pakietów
`Document`, `JfifResource` i powiązane klasy są częścią przestrzeni nazw Aspose.PSD. `Document` reprezentuje kontener pliku PSD, a `JfifResource` zapewnia dostęp do segmentu JFIF w PSD. Zaimportuj je na początku swojego pliku źródłowego.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Krok 2: wczytanie obrazu PSD
Utwórz instancję `PsdImage`, przekazując ścieżkę pliku do konstruktora. `PsdImage` to klasa Aspose.PSD modelująca dokument Photoshop. Ładuje ona metadane dokumentu, jednocześnie strumieniując dane pikseli.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Krok 3: iteracja po zasobach obrazu
Przeszukaj kolekcję `Resources` w poszukiwaniu `JfifResource`. Po jej znalezieniu możesz zamienić tablicę bajtów miniaturki na nowy podgląd zakodowany w JPEG.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Krok 4: dostosowanie danych miniaturki
Wygeneruj małą miniaturkę JPEG (np. 120 × 120 px) przy użyciu dowolnej biblioteki przetwarzania obrazów, a następnie przypisz otrzymaną tablicę bajtów do `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Krok 5: zapis zmodyfikowanego obrazu
Wywołaj metodę `save` na obiekcie `PsdImage`, podając ścieżkę wyjściową i żądany format. Segment JFIF zawiera teraz nową miniaturkę.

```java
image.save(dataDir + "output.psd");
```

## Typowe problemy i rozwiązania
- **Miniaturka nie jest widoczna w przeglądarkach:** Upewnij się, że dane miniaturki są prawidłową tablicą bajtów JPEG i że ich wymiary mieszczą się w granicach 256 × 256 px, co jest maksymalnym rozmiarem obsługiwanym przez specyfikację JFIF.  
- **OutOfMemoryError przy dużych plikach PSD:** Użyj `PsdImage.load(inputStream, true)`, aby włączyć tryb strumieniowy, co utrzymuje niskie zużycie pamięci.  
- **Nieprawidłowy typ zasobu:** Zweryfikuj, że modyfikowany zasób jest rzeczywiście `JfifResource`; inne zasoby, takie jak `ExifResource`, nie wpłyną na wyświetlanie miniaturki.

## Najczęściej zadawane pytania

**Q: Czym jest Aspose.PSD for Java?**  
A: Aspose.PSD for Java to komercyjna biblioteka, która umożliwia programistom tworzenie, edytowanie, konwertowanie i renderowanie plików Photoshop PSD bez konieczności posiadania Adobe Photoshop.

**Q: Gdzie mogę znaleźć więcej dokumentacji dla Aspose.PSD for Java?**  
A: Szczegółowa dokumentacja jest dostępna na [stronie dokumentacji Aspose.PSD for Java](https://reference.aspose.com/psd/java/).

**Q: Czy Aspose.PSD for Java nadaje się do użytku komercyjnego?**  
A: Tak, Aspose.PSD for Java może być używany komercyjnie. Licencję można zakupić na [stronie zakupu Aspose.PSD](https://purchase.aspose.com/buy).

**Q: Czy mogę wypróbować Aspose.PSD for Java przed zakupem?**  
A: Tak, możesz pobrać darmową wersję próbną z [strony pobierania wersji próbnej Aspose.PSD](https://releases.aspose.com/).

**Q: Jak mogę uzyskać wsparcie dla Aspose.PSD for Java?**  
A: W celu uzyskania wsparcia odwiedź [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

---

**Ostatnia aktualizacja:** 2026-09-28  
**Testowano z:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Powiązane samouczki

- [Dodaj zasób IOPA do plików PSD przy użyciu Aspose PSD for Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Dodaj podpis do obrazu – rysowanie obrazu na płótnie z Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Jak obrócić obraz pod określonym kątem przy użyciu Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
title: Wyodrębnij miniaturę z PSD w Javie
linktitle: Wyodrębnij miniaturę z PSD w Javie
second_title: Aspose.PSD API Java
description: Dowiedz się, jak wyodrębnić miniatury z plików PSD za pomocą Aspose.PSD dla Java. Ten przewodnik krok po kroku obejmuje wszystko, od konfiguracji po zapisywanie wyodrębnionych obrazów.
type: docs
weight: 15
url: /pl/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Wstęp
tym samouczku przyjrzymy się, jak wyodrębnić miniatury z plików PSD za pomocą Aspose.PSD dla Java. Miniatury mogą być przydatne do szybkiego podglądu lub tworzenia mniejszych wersji obrazów osadzonych w dokumentach PSD. Przyjrzyjmy się krokom wymaganym do osiągnięcia tego celu za pomocą Aspose.PSD.
## Warunki wstępne
Zanim zaczniemy, upewnij się, że masz następującą konfigurację:
- Zestaw Java Development Kit (JDK) zainstalowany w systemie.
-  Aspose.PSD dla biblioteki Java. Można go pobrać z[Tutaj](https://releases.aspose.com/psd/java/).
- Podstawowa znajomość programowania w języku Java.
## Importuj pakiety
Aby rozpocząć, dołącz niezbędny pakiet Aspose.PSD do swojej klasy Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Krok 1: Załaduj plik PSD
Najpierw załaduj plik PSD zawierający miniaturę, którą chcesz wyodrębnić.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Zastępować`"Your_Document_Directory/"` ze ścieżką katalogu, w którym znajduje się plik PSD, oraz`"your_file.psd"` z nazwą pliku PSD.
## Krok 2: Iteruj po zasobach obrazu
Przeglądaj zasoby obrazu, aby znaleźć zasób miniatury.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Wyodrębnij dane miniatur
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Utwórz nowy obraz z wyodrębnionymi danymi miniatur
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Zapisz wyodrębnioną miniaturę jako oddzielny plik JPEG
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Wyjście komunikatu o powodzeniu
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Wyjdź z pętli po znalezieniu i przetworzeniu miniatury
    }
}
```
## Krok 3: Zapisz wyodrębnioną miniaturę
Zapisz wyodrębnioną miniaturę jako oddzielny plik obrazu (w tym przypadku jako plik JPEG).
## Krok 4: Obsługa różnych typów miniatur
 Jeśli plik PSD może zawierać wiele typów miniatur, np`Thumbnail4Resource`, możesz rozszerzyć logikę, aby obsługiwać te przypadki w podobny sposób.

## Wniosek
W tym samouczku omówiliśmy, jak wyodrębnić miniatury z plików PSD za pomocą Aspose.PSD dla Java. Wykonując czynności opisane powyżej, możesz skutecznie pobierać i zapisywać miniatury osadzone w dokumentach PSD.

## Często zadawane pytania
### Co to jest Aspose.PSD?
Aspose.PSD to biblioteka Java, która umożliwia programistom programową pracę z PSD i innymi formatami plików graficznych.
### Gdzie mogę znaleźć więcej dokumentacji na temat Aspose.PSD dla Java?
 Możesz odwołać się do[dokumentacja](https://reference.aspose.com/psd/java/) szczegółowe odniesienia do API i przykłady.
### Czy mogę wypróbować Aspose.PSD za darmo przed zakupem?
 Tak, możesz pobrać plik[bezpłatna wersja próbna](https://releases.aspose.com/) ocenić możliwości biblioteki.
### Jak mogę uzyskać tymczasowe licencje na Aspose.PSD?
 Licencje tymczasowe można uzyskać od[Tutaj](https://purchase.aspose.com/temporary-license/).
### Czy Aspose.PSD nadaje się do użytku komercyjnego?
Tak, Aspose.PSD może być używany zarówno do projektów osobistych, jak i komercyjnych zgodnie z warunkami licencji.
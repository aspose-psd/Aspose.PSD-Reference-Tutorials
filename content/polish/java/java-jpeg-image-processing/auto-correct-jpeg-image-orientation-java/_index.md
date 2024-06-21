---
title: Automatyczna korekta orientacji obrazu JPEG w Javie
linktitle: Automatyczna korekta orientacji obrazu JPEG w Javie
second_title: Aspose.PSD API Java
description: Dowiedz się, jak automatycznie korygować orientację obrazu JPEG w Javie przy użyciu Aspose.PSD. Zwiększ swoje umiejętności przetwarzania obrazu bez wysiłku.
type: docs
weight: 12
url: /pl/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## Wstęp
W dzisiejszej erze cyfrowej programowe manipulowanie i optymalizowanie obrazów stało się kluczowym zadaniem dla programistów z różnych dziedzin. Aspose.PSD dla Java zapewnia programistom solidne narzędzia do wydajnej obsługi PSD, JPEG i innych formatów obrazów. Ten samouczek omawia konkretne zadanie: automatyczne korygowanie orientacji obrazu JPEG przy użyciu Aspose.PSD dla Java. Niezależnie od tego, czy tworzysz aplikację do edycji zdjęć, zarządzasz zasobami obrazów w systemie zarządzania treścią, czy automatyzujesz przepływy pracy związane z przetwarzaniem obrazów, ten przewodnik zapewni Ci niezbędną wiedzę, aby bezproblemowo zintegrować tę funkcjonalność z aplikacjami Java.
## Warunki wstępne
Zanim zagłębisz się w ten samouczek, upewnij się, że masz skonfigurowane następujące wymagania wstępne:
- Środowisko programistyczne Java: Upewnij się, że w systemie jest zainstalowany zestaw Java Development Kit (JDK).
-  Aspose.PSD dla Java JAR: Pobierz bibliotekę Aspose.PSD dla Java z[Tutaj](https://releases.aspose.com/psd/java/).
- Zintegrowane środowisko programistyczne (IDE): Użyj IntelliJ IDEA, Eclipse lub dowolnego wybranego IDE do programowania w języku Java.
- Podstawowa znajomość języka Java i przetwarzania obrazu: Znajomość programowania w języku Java i podstawowych koncepcji przetwarzania obrazu będzie korzystna.

## Importuj pakiety
Zanim zaczniesz od przykładu, pamiętaj o zaimportowaniu niezbędnych pakietów z Aspose.PSD dla Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Krok 1: Załaduj obraz PSD
Najpierw załaduj obraz PSD zawierający miniaturę JPEG, której orientacja wymaga korekty:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 Zastępować`"Your Document Directory"` z rzeczywistą ścieżką katalogu, w którym znajduje się plik PSD.
## Krok 2: Iteruj po zasobach obrazu
Następnie przejrzyj zasoby obrazu, aby znaleźć zasób miniatury JPEG:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Znajdź zasób miniatur. Zazwyczaj są one w formacie pliku JPEG.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Dostosuj dane miniatury.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // Jeśli zapisano miniaturę, obróć ją automatycznie.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## Krok 3: Zapisz obraz
Na koniec zapisz poprawiony obraz po zastosowaniu automatycznego obrotu:
```java
image.save();
```
Ten krok zapewnia utrwalenie zmian wprowadzonych w obrazie.

## Wniosek
Podsumowując, użycie Aspose.PSD dla Java zapewnia potężne rozwiązanie do automatycznego korygowania orientacji obrazów JPEG w plikach PSD. Wykonując kroki opisane w tym samouczku, programiści mogą ulepszyć przepływy pracy przetwarzania obrazów, zapewniając prawidłowe wyświetlanie obrazów na różnych platformach i urządzeniach.
## Często zadawane pytania
### Co to jest Aspose.PSD dla Java?
Aspose.PSD for Java to potężna biblioteka, która umożliwia programistom Java programową pracę z PSD, JPEG i innymi formatami obrazów.
### Jak mogę pobrać Aspose.PSD dla Java?
 Bibliotekę możesz pobrać ze strony[Tutaj](https://releases.aspose.com/psd/java/).
### Czy Aspose.PSD dla Java obsługuje manipulację obrazami?
Tak, obsługuje różne zadania manipulacji obrazem, takie jak zmiana rozmiaru, przycinanie i dostosowywanie orientacji.
### Gdzie mogę znaleźć dokumentację Aspose.PSD dla Java?
 Dostępna jest obszerna dokumentacja[Tutaj](https://reference.aspose.com/psd/java/).
### Czy mogę wypróbować Aspose.PSD dla Java za darmo?
 Tak, możesz uzyskać bezpłatną wersję próbną od[Tutaj](https://releases.aspose.com/).
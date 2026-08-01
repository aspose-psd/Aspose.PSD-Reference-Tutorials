---
date: 2026-08-01
description: Dowiedz się, jak eksportować PSD do PNG i obsługiwać uncompressed image
  streams przy użyciu Aspose.PSD for Java.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: Obsługa Uncompressed Image Stream Object w PSD – Java
og_description: eksport psd do png przy użyciu Aspose.PSD for Java. Dowiedz się, jak
  obsługiwać uncompressed image streams, tworzyć obiekty graficzne i zapisywać wysokiej
  jakości PNG.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: eksport psd do png – przewodnik Java po uncompressed PSD streams
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: Eksportuj PSD do PNG – Utwórz obiekt graficzny PSD – Uncompressed Stream w
  Javie
url: /pl/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj PSD do PNG – Utwórz obiekt graficzny PSD – Niekompresowany strumień w Javie

## Wprowadzenie
W tym przewodniku krok po kroku **wyeksportujesz PSD do PNG**, pracując z niekompresowanym strumieniem obrazu przy użyciu Aspose.PSD for Java. Niezależnie od tego, czy automatyzujesz pipeline projektowy, czy tworzysz własny edytor, możliwość renderowania pliku Photoshop bez utraty jakości jest niezbędna. Rozpoczniemy od wymaganego przygotowania, przejdziemy przez tworzenie obiektu `Graphics`, a zakończymy bezstratnym eksportem do PNG. Po zakończeniu zrozumiesz, dlaczego Aspose.PSD efektywnie obsługuje surowe strumienie i jak zintegrować go z dowolnym projektem Java.

## Szybkie odpowiedzi
- **Co oznacza „utwórz obiekt graficzny PSD”?** Oznacza to zainicjowanie kontekstu `Graphics`, który pozwala programowo rysować lub modyfikować obraz PSD.  
- **Która biblioteka obsługuje niekompresowane strumienie?** Aspose.PSD for Java zapewnia pełne wsparcie dla surowych (niekompresowanych) danych obrazu.  
- **Czy mogę wyeksportować PSD do PNG po edycji?** Tak — po uzyskaniu obiektu `Graphics` możesz renderować PSD i zapisać go jako PNG w jednym wywołaniu.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna wystarcza do testów; licencja komercyjna jest wymagana w środowiskach produkcyjnych.  
- **Czy eksport jest bezstratny?** Eksport do PNG zachowuje oryginalne dane pikseli, oferując jakość bezstratną przy mniejszym rozmiarze pliku niż surowy PSD.

## Co to jest eksport PSD do PNG?
Eksportowanie PSD do PNG konwertuje warstwowy dokument Photoshop na jednowarstwowy, bezstratny obraz rastrowy, który może być wyświetlany w dowolnej przeglądarce internetowej lub przeglądarce obrazów. Proces zachowuje przezroczystość, głębię kolorów i efekty warstw, jednocześnie odrzucając metadane specyficzne dla Photoshopa. Zachowuje także oryginalny profil kolorów dla dokładnego odwzorowania barw.

## Dlaczego warto używać Aspose.PSD for Java do manipulacji obrazami?
Aspose.PSD obsługuje **ponad 50** formatów wejścia i wyjścia — w tym PSD, PNG, JPEG, BMP i TIFF — oraz może przetwarzać pliki z **ponad 200** warstwami bez ładowania całego dokumentu do pamięci. Opcja kompresji `Raw` przechowuje dane pikseli niekompresowane, gwarantując perfekcyjną wierność pikseli przy dalszej edycji lub archiwizacji.

## Wymagania wstępne
Zanim przejdziesz do kodu, upewnij się, że masz następujące elementy:

- **Java Development Kit (JDK)** – zainstalowany JDK 8 lub nowszy.  
- **Aspose.PSD for Java** – pobierz najnowszy plik JAR z oficjalnej strony wydania: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/). Możesz również uzyskać dostęp poprzez [ten link](https://releases.aspose.com/psd/java/) lub [stronę wydania](https://releases.aspose.com/psd/java/). Dla innych produktów Aspose kliknij [tutaj](https://releases.aspose.com/).  
- **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor kompatybilny z Javą.  
- **Podstawowa znajomość Javy** – znajomość klas, metod i obsługi wyjątków.

Mając to wszystko, możesz przystąpić do kodowania.

## Importowanie pakietów
Klasa `Graphics` jest powierzchnią rysunkową Aspose.PSD, która pozwala renderować lub edytować dane pikseli bezpośrednio. Klasa `PsdImage` reprezentuje plik PSD w pamięci, natomiast `PsdOptions` kontroluje sposób zapisu obrazu.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Teraz rozbijemy kod na przystępne kroki, abyś mógł łatwo podążać za instrukcją. Skonfigurujemy środowisko, wczytamy plik PSD, zmodyfikujemy go i w końcu zapiszemy wynik.

## Krok 1: Zdefiniuj katalog dokumentu
Przed jakimikolwiek operacjami na plikach musisz poinformować program, gdzie szukać zasobów PSD. Ścieżka katalogu jest używana w całym samouczku.

```java
String dataDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` pełną ścieżką, w której znajduje się `layers.psd`. Utrzymanie ścieżki konfigurowalnej sprawia, że kod jest wielokrotnego użytku w różnych projektach.

## Krok 2: Utwórz strumień wyjściowy ByteArrayOutputStream
`ByteArrayOutputStream` to strumień Javy, który przechowuje dane w pamięci jako tablicę bajtów. Działa jako bufor w pamięci dla zmodyfikowanego obrazu, umożliwiając przechwycenie surowych bajtów przed zapisaniem ich na dysk lub wysłaniem przez sieć.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Zmienna `ms` będzie zawierała niekompresowane dane obrazu po operacji `save`.

## Krok 3: Wczytaj plik PSD
Klasa `PsdImage` wczytuje plik PSD do pamięci w celu dalszej manipulacji. Ładowanie pliku konwertuje PSD z dysku na obiekt `PsdImage`, który możesz modyfikować. W tym kroku Aspose.PSD odczytuje nagłówek pliku, warstwy i zasoby.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Jeśli ścieżka jest nieprawidłowa, Aspose.PSD zgłosi `FileNotFoundException`, który powinieneś obsłużyć w kodzie produkcyjnym.

## Krok 4: Skonfiguruj PsdOptions do zapisu
`PsdOptions` określa parametry zapisu dla plików PSD. Ustawienie metody kompresji na `Raw` wskazuje, że dane pikseli mają być przechowywane bez kompresji, zachowując każdy piksel dokładnie tak, jak wygląda w pamięci.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Opcja `CompressionMethod.Raw` przechowuje dane pikseli bez żadnej kompresji, co jest idealne, gdy planujesz dalsze edycje.

## Krok 5: Zapisz obraz do strumienia wyjściowego
Teraz zapisujesz PSD (z ewentualnymi modyfikacjami) do wcześniej utworzonego `ByteArrayOutputStream`. Metoda `save` respektuje skonfigurowane `PsdOptions`.

```java
psdImage.save(ms, saveOptions);
```

W tym momencie `ms` zawiera pełną binarną reprezentację niekompresowanego PSD.

## Krok 6: Zresetuj strumień wyjściowy
Po zapisie wewnętrzny wskaźnik strumienia znajduje się na końcu. Resetowanie go przewija strumień z powrotem na początek, aby można było odczytać dane od początku.

```java
ms.reset();
```

Można to porównać do przewinięcia taśmy magnetofonowej do początku przed odtworzeniem.

## Krok 7: Wczytaj nowo utworzony obraz
Możesz teraz utworzyć nową instancję `PsdImage` bezpośrednio z tablicy bajtów. Ten krok weryfikuje, że zapisane dane mogą być ponownie wczytane bez uszkodzeń.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Jeśli obraz wczyta się pomyślnie, wiesz, że niekompresowany strumień został zapisany prawidłowo.

## Krok 8: Utwórz obiekt Graphics
Klasa `Graphics` jest płótnem rysunkowym Aspose.PSD. Udostępnia metody do rysowania kształtów, tekstu i stosowania filtrów bezpośrednio na macierzy pikseli `PsdImage`.

```java
Graphics graphics = new Graphics(psdImage);
```

Dzięki temu obiektowi `Graphics` możesz malować nową zawartość, wycierać fragmenty lub łączyć dodatkowe warstwy.

## Jak wyeksportować PSD do PNG przy użyciu Aspose.PSD for Java?
Wczytaj PSD za pomocą `new PsdImage(dataDir + "layers.psd")`, utwórz obiekt `Graphics`, wykonaj potrzebne rysowanie, a następnie wywołaj `psdImage.save("output.png", new PngOptions())`. Ta sekwencja renderuje edytowany PSD i zapisuje bezstratny PNG w jednym kroku, wykorzystując wbudowany silnik konwersji Aspose.PSD.

## Manipulacja warstwami PSD przy użyciu obiektu Graphics
Posiadanie instancji `Graphics` daje kontrolę na poziomie pikseli nad każdą warstwą. Możesz rysować kształty geometryczne, renderować tekst lub stosować własne filtry. Ponieważ kontekst graficzny działa na zrasowanym widoku warstwy, zmiany są widoczne od razu po zapisaniu obrazu.

## Typowe problemy i rozwiązania
- **NullPointerException przy wczytywaniu pliku** – sprawdź dokładnie ścieżkę `dataDir` i upewnij się, że nazwa pliku jest identyczna, łącznie z wielkością liter.  
- **Skompresowany wynik pomimo użycia Raw** – upewnij się, że wywołanie `saveOptions.setCompressionMethod(CompressionMethod.Raw);` znajduje się **przed** wywołaniem `save`.  
- **Obiekt Graphics jest pusty** – sprawdź, czy rysujesz na właściwej instancji `PsdImage` (tej, którą wczytałeś, a nie na nowo utworzonym pustym obrazie).  
- **OutOfMemoryError przy dużych plikach** – użyj `PsdImage.load(dataDir, LoadOptions)` z `loadOptions.setLoadMode(LoadMode.Memory)`, aby strumieniowo przetwarzać duże pliki bez ładowania całego dokumentu do RAM.

## FAQ
### Co to jest Aspose.PSD?
Aspose.PSD to biblioteka Java, która umożliwia programistom tworzenie, edytowanie i konwertowanie plików Photoshop PSD bez konieczności posiadania Adobe Photoshop. Obsługuje odczyt i zapis plików PSD, zarządzanie warstwami, maskami, kanałami i różnymi zasobami obrazu oraz oferuje API do operacji rastrowych i wektorowych, co czyni ją przydatną w przetwarzaniu obrazów po stronie serwera i automatyzacji.

### Jak mogę pobrać Aspose.PSD for Java?
Możesz pobrać go ze strony wydania: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

### Czy istnieje darmowa wersja próbna Aspose.PSD?
Tak, w pełni funkcjonalna wersja próbna jest dostępna na tej samej stronie pobierania. Działa do celów rozwojowych i ewaluacyjnych.

### Czy mogę uzyskać wsparcie dla Aspose.PSD?
Oczywiście! Forum wsparcia Aspose zapewnia odpowiedzi od zespołu produktu i społeczności: [Aspose support forum](https://forum.aspose.com/c/psd/34).

### Jak mogę uzyskać tymczasową licencję dla Aspose.PSD?
Możesz poprosić o tymczasową licencję bezpośrednio w portalu licencjonowania Aspose, który generuje klucz ważny przez 30 dni. Umożliwia to ocenę pełnej funkcjonalności Aspose.PSD bez zakupu licencji komercyjnej. Po okresie próbnym należy wymienić klucz tymczasowy na stałą licencję, aby kontynuować używanie biblioteki w produkcji. Odwiedź stronę tymczasowej licencji, aby wygenerować klucz ograniczony czasowo: [temporary license page](https://purchase.aspose.com/temporary-license/).

## Najczęściej zadawane pytania

**P: Czy mogę używać obiektu graficznego do edycji tylko jednej konkretnej warstwy?**  
O: Tak. Po wczytaniu PSD pobierz żądaną warstwę za pomocą `psdImage.getLayers().get_Item(index)` i przekaż tę warstwę do konstruktora `Graphics`.

**P: Czy metoda kompresji Raw wpływa na rozmiar pliku?**  
O: Raw przechowuje dane pikseli bez żadnej kompresji, więc wynikowy plik jest większy niż skompresowany PSD, ale zapewnia 100 % wierność pikseli.

**P: Czy można wyeksportować edytowany PSD do innego formatu (np. PNG)?**  
O: Absolutnie. Po edycji wywołaj `psdImage.save("output.png", new PngOptions())` — to standardowy sposób **eksportu PSD do PNG** z jakością bezstratną.

**P: Jaka wersja Javy jest wymagana?**  
O: Aspose.PSD for Java obsługuje JDK 8 i nowsze, w tym wszystkie wersje LTS aż do JDK 21.

**P: Jak zwolnić zasoby po przetworzeniu?**  
O: Wywołaj `psdImage.dispose()` oraz zamknij wszystkie strumienie (np. `ms.close()`), aby zwolnić pamięć natywną i uniknąć wycieków.

---

**Ostatnia aktualizacja:** 2026-08-01  
**Testowano z:** Aspose.PSD for Java (najnowsze wydanie)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Save Images to Stream with Aspose.PSD for Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Export PSD Layer Group to Image using Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Create Image using Stream in Aspose.PSD for Java](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
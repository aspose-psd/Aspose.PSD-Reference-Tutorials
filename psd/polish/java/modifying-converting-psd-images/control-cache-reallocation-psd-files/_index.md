---
title: Kontroluj realokację pamięci podręcznej w plikach PSD
linktitle: Kontroluj realokację pamięci podręcznej w plikach PSD
second_title: Aspose.PSD API Java
description: Zarządzaj realokacją pamięci podręcznej w plikach PSD za pomocą Aspose.PSD dla Java. Dowiedz się, jak efektywnie optymalizować pamięć i obsługę plików — idealne rozwiązanie dla programistów.
weight: 22
url: /pl/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kontroluj realokację pamięci podręcznej w plikach PSD

## Wstęp
Podczas programowej pracy z obrazami i plikami programu Photoshop wydajność jest kluczowym czynnikiem. Aspose.PSD dla Java oferuje solidne funkcje do płynnego zarządzania plikami PSD i manipulowania nimi. Jednym z podstawowych aspektów optymalizacji wydajności jest kontrolowanie realokacji pamięci podręcznej. Zarządzanie pamięcią podręczną pomaga w utrzymaniu równowagi pomiędzy wykorzystaniem pamięci i dysku, zapewniając płynne działanie aplikacji, bez nieoczekiwanych awarii i spowolnień. 
## Warunki wstępne
Zanim przejdziemy do części dotyczącej kodowania, musisz zadbać o kilka rzeczy, aby wszystko działało sprawnie:
1. Zestaw Java Development Kit (JDK): Upewnij się, że na komputerze jest zainstalowany pakiet JDK. Można go pobrać z[stronie internetowej Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD dla Java: Musisz pobrać bibliotekę Aspose.PSD. Możesz znaleźć najnowszą wersję[Tutaj](https://releases.aspose.com/psd/java/).
3. Konfiguracja IDE: Zintegrowane środowisko programistyczne (IDE), takie jak IntelliJ IDEA lub Eclipse, ułatwi zarządzanie kodem.
4. Podstawowa znajomość języka Java: Znajomość programowania w języku Java pomoże Ci lepiej zrozumieć pojęcia i fragmenty kodu.
5.  Licencja Aspose (opcjonalnie): Jeśli chcesz usunąć znaki wodne i uzyskać pełną funkcjonalność, rozważ zakup licencji[Tutaj](https://purchase.aspose.com/buy) lub wypróbuj bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).
## Importuj pakiety
Zanim zaczniemy pisać kod, upewnijmy się, że mamy zaimportowane niezbędne pakiety. Poniżej znajduje się krótka lista elementów, które należy umieścić na początku pliku Java:
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
## Krok 1: Konfigurowanie katalogu danych
Po pierwsze, musisz skonfigurować katalog, w którym chcesz przechowywać pliki pamięci podręcznej. Jest to niezbędne do skutecznego zarządzania pamięcią podręczną.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Zdefiniuj katalog pamięci podręcznej dokumentów.
- Cache.setCacheFolder(dataDir): Ta metoda ustawia folder pamięci podręcznej w określonym katalogu. Każda pamięć podręczna utworzona przez Aspose będzie teraz przechowywana tutaj zamiast domyślnego katalogu tymczasowego.
## Krok 2: Konfiguracja pamięci podręcznej na dysku
Następnie określimy, że chcemy, aby nasza pamięć podręczna była przechowywana wyłącznie na dysku. Jest to szczególnie przydatne, jeśli aplikacja korzysta z dużych plików i chcesz mieć pewność, że pamięć pozostanie wolna.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Ta opcja gwarantuje, że pamięć podręczna nie będzie przechowywana w pamięci, co jest korzystne w przypadku obsługi dużych plików PSD bez zużywania zbyt dużej ilości pamięci RAM.
## Krok 3: Ustawianie maksymalnego rozmiaru dysku i pamięci podręcznej
Teraz ograniczmy rozmiary naszych pamięci podręcznych. Ma to kluczowe znaczenie, ponieważ nieograniczona pamięć podręczna może prowadzić do problemów z wydajnością.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabajt
Cache.setMaxMemoryForCache(1073741824); // 1 gigabajt
```

- Cache.setMaxDiskSpaceForCache(1073741824): ustawia limit 1 GB pamięci podręcznej na dysku. Możesz dostosować ten rozmiar w zależności od potrzeb.
- Cache.setMaxMemoryForCache(1073741824): w podobny sposób ogranicza to pamięć podręczną w pamięci, zapewniając, że aplikacja nie zużywa nadmiernej ilości pamięci.
## Krok 4: Zarządzaj strategią realokacji pamięci podręcznej
Zarządzanie sposobem realokacji pamięci podręcznej jest niezbędne do utrzymania wydajności. Oto jak możesz to skonfigurować.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): Kiedy jest ustawione na false, pozwala Aspose na bardziej elastyczne zarządzanie realokacją pamięci podręcznej, co może prowadzić do lepszej wydajności.
## Krok 5: Sprawdź przydzielony rozmiar pamięci podręcznej
Ten krok polega na monitorowaniu liczby bajtów aktualnie przydzielonych do pamięci podręcznej w pamięci lub na dysku. Zaimplementujmy to:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Przechowuje liczbę bajtów przydzielonych na dysku.
- long l2: Przechowuje liczbę bajtów przydzielonych w pamięci. 
Możesz sprawdzić te wartości w dowolnym momencie, aby upewnić się, że aplikacja zarządza wykorzystaniem pamięci i dysku zgodnie z oczekiwaniami.
## Krok 6: Tworzenie obrazu PSD
Teraz, gdy mamy już skonfigurowane konfiguracje pamięci podręcznej, utwórzmy prosty obraz PSD.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- Opcje PsdOptions: ten obiekt umożliwia określenie opcji podczas tworzenia obrazu Photoshop.
- Kolor[] kolor: Tablica zawierająca kolory, które będą używane w palecie obrazu.
## Krok 7: Zapisywanie danych pikseli na obrazie
Teraz wypełnijmy nasz obraz danymi pikselowymi i zapiszmy go.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Kolor[] pikseli: To jest tablica kolorowych obiektów. Tutaj wypełniamy go białymi pikselami.
- image.savePixels(image.getBounds(), piksele): Ta metoda zapisuje dane pikseli w obrazie. Aktualizuje obraz przy użyciu zdefiniowanych przez nas kolorów.
## Krok 8: Monitorowanie przydzielonej pamięci podręcznej po utworzeniu obrazu
Po utworzeniu obrazu dobrą praktyką jest ponowne sprawdzenie, ile bajtów jest przydzielonych na pamięć podręczną.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long discBytes: Przechwytuje bieżącą alokację na dysku po utworzeniu obrazu.
- long memoryBytes: Przechwytuje bieżącą alokację w pamięci. 
Ten krok pomoże Ci określić, ile pamięci podręcznej jest zużywane po wykonaniu operacji.
## Krok 9: Sprawdź, czy utylizacja jest prawidłowa
Na koniec ważne jest, aby upewnić się, że wszystkie obiekty Aspose.PSD zostały prawidłowo usunięte, aby uniknąć wycieków pamięci.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 i l2: Te zmienne pomogą Ci sprawdzić ostateczną alokację. Jeśli nie są równe zero, oznacza to, że niektóre przedmioty nie zostały prawidłowo usunięte.
## Wniosek
Kontrolowanie realokacji pamięci podręcznej w Aspose.PSD dla Java może znacząco wpłynąć na wydajność aplikacji. Wykonując czynności opisane powyżej, możesz skutecznie zarządzać pamięcią podręczną, minimalizować zużycie pamięci i efektywnie tworzyć piękne pliki PSD. Wykorzystaj te techniki i obserwuj, jak Twoje aplikacje rozwijają się z optymalną wydajnością!
## Często zadawane pytania
### Co to jest Aspose.PSD?
Aspose.PSD to biblioteka dla programistów .NET i Java służąca do programowego tworzenia, manipulowania i konwertowania plików Photoshop (PSD).
### Jak sprawdzić przydzielony rozmiar pamięci podręcznej?
 Użyj metod takich jak`Cache.getAllocatedDiskBytesCount()` I`Cache.getAllocatedMemoryBytesCount()` do monitorowania bieżącego wykorzystania pamięci podręcznej.
### Czy mogę ustawić niestandardowy katalog dla pamięci podręcznej?
 Tak, możesz określić inny katalog za pomocą`Cache.setCacheFolder("Your Directory Path")`.
### Czy korzystanie z Aspose.PSD jest bezpłatne?
Aspose.PSD jest biblioteką płatną, ale możesz zacząć od bezpłatnej wersji próbnej dostępnej na ich stronie[strona internetowa](https://releases.aspose.com/).
### Co się stanie, jeśli nie wyrzucę przedmiotów?
Niepozbywanie się obiektów może prowadzić do wycieków pamięci, co powoduje, że aplikacja zużywa więcej zasobów, niż to konieczne.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
date: 2026-03-13
description: Dowiedz się, jak tworzyć projekty Java z obrazami PSD, zarządzając realokacją
  pamięci podręcznej przy użyciu Aspose.PSD for Java. Optymalizuj efektywnie zużycie
  pamięci i dysku.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Tworzenie obrazu PSD w Javie – kontrola ponownego przydzielania pamięci podręcznej
url: /pl/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

 sure to keep markdown formatting.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kontrola ponownego przydzielania pamięci podręcznej w plikach PSD

## Wstęp
Jeśli potrzebujesz **create PSD image java** projektów efektywnie, kontrola ponownego przydzielania pamięci podręcznej jest niezbędna. Pracując programowo z obrazami i plikami Photoshop, wydajność jest kluczowym czynnikiem. Aspose.PSD for Java oferuje solidne funkcje umożliwiające zarządzanie i manipulację plikami PSD bezproblemowo. Jednym z podstawowych aspektów optymalizacji wydajności jest kontrola ponownego przydzielania pamięci podręcznej. Zarządzanie pamięcią podręczną pomaga utrzymać równowagę między użyciem pamięci a dysku, zapewniając płynne działanie aplikacji, bez nieoczekiwanych awarii czy spowolnień. 

## Szybkie odpowiedzi
- **Co robi ponowne przydzielanie pamięci podręcznej?** Balansuje użycie pamięci i dysku podczas przetwarzania dużych plików PSD.  
- **Jaki typ pamięci podręcznej jest najlepszy dla dużych obrazów?** `CacheOnDiskOnly` utrzymuje wolną pamięć, przechowując pamięć podręczną na dysku.  
- **Ile miejsca na dysku mogę przydzielić?** Do 1 GB (lub dowolny rozmiar, który ustawisz za pomocą `setMaxDiskSpaceForCache`).  
- **Czy potrzebuję licencji, aby korzystać z tych funkcji?** Licencja usuwa ograniczenia wersji próbnej; zobacz stronę zakupu Aspose.  
- **Czy mogę monitorować użycie pamięci podręcznej w czasie działania?** Tak, użyj `Cache.getAllocatedDiskBytesCount()` i `Cache.getAllocatedMemoryBytesCount()`.

## Dlaczego kontrolować ponowne przydzielanie pamięci podręcznej?
Zarządzanie pamięcią podręczną jest kluczowe, gdy **create PSD image java** aplikacje obsługują obrazy wysokiej rozdzielczości lub pliki wielowarstwowe. Odpowiednie ustawienia pamięci podręcznej zapobiegają błędom braku pamięci, redukują przerwy GC i zapewniają przewidywalną wydajność na serwerach lub aplikacjach desktopowych.

## Wymagania wstępne
Zanim przejdziemy do części kodowej, jest kilka rzeczy, które musisz zapewnić, aby wszystko działało płynnie:
1. Java Development Kit (JDK): Upewnij się, że masz zainstalowany JDK na swoim komputerze. Możesz go pobrać ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Musisz pobrać bibliotekę Aspose.PSD. Najnowsze wydanie znajdziesz [tutaj](https://releases.aspose.com/psd/java/).
3. Konfiguracja IDE: Zintegrowane środowisko programistyczne (IDE) takie jak IntelliJ IDEA lub Eclipse ułatwi zarządzanie kodem.
4. Podstawowa znajomość Javy: Znajomość programowania w Javie pomoże lepiej zrozumieć koncepcje i fragmenty kodu.
5. Licencja Aspose (opcjonalnie): Jeśli chcesz usunąć znaki wodne i uzyskać pełną funkcjonalność, rozważ zakup licencji [tutaj](https://purchase.aspose.com/buy) lub wypróbowanie darmowej wersji próbnej [tutaj](https://releases.aspose.com/).

## Importowanie pakietów
Zanim zaczniemy pisać kod, upewnijmy się, że mamy zaimportowane niezbędne pakiety. Poniżej znajduje się krótka lista tego, co należy umieścić na początku pliku Java:
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

## Jak utworzyć PSD Image Java z kontrolą pamięci podręcznej
Poniżej znajduje się krok po kroku przewodnik, który łączy konfigurację pamięci podręcznej bezpośrednio z procesem tworzenia obrazu PSD w Javie.

### Krok 1: Konfiguracja katalogu danych
Na początek musisz skonfigurować katalog, w którym będą przechowywane pliki pamięci podręcznej. Jest to niezbędne do efektywnego zarządzania pamięcią podręczną.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Definiuje katalog dla pamięci podręcznej dokumentu.  
- `Cache.setCacheFolder(dataDir)`: Ta metoda ustawia folder pamięci podręcznej na określony katalog. Wszystka pamięć podręczna tworzona przez Aspose będzie teraz przechowywana tutaj zamiast w domyślnym katalogu tymczasowym.

### Krok 2: Konfiguracja pamięci podręcznej na dysk
Następnie określimy, że pamięć podręczna ma być przechowywana wyłącznie na dysku. Jest to szczególnie przydatne, jeśli aplikacja używa dużych plików i chcesz zapewnić wolną pamięć.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Ta opcja zapewnia, że pamięć podręczna nie jest przechowywana w pamięci, co jest korzystne przy obsłudze dużych plików PSD bez zużywania zbyt dużej ilości RAM.

### Krok 3: Ustawienie maksymalnego rozmiaru pamięci podręcznej na dysku i w pamięci
Teraz ograniczmy rozmiary pamięci podręcznej. Jest to kluczowe, ponieważ nieograniczona pamięć podręczna może prowadzić do problemów z wydajnością.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Ustawia limit 1 GB dla pamięci podręcznej na dysku. Możesz dostosować ten rozmiar w zależności od potrzeb.  
- `Cache.setMaxMemoryForCache(1073741824)`: Podobnie, ogranicza pamięć podręczną w pamięci, zapewniając, że aplikacja nie zużywa nadmiernej ilości pamięci.

### Krok 4: Zarządzanie strategią ponownego przydzielania pamięci podręcznej
Zarządzanie sposobem ponownego przydzielania pamięci podręcznej jest niezbędne do utrzymania wydajności. Oto jak możesz to skonfigurować.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Gdy ustawione na `false`, pozwala Aspose na bardziej elastyczne zarządzanie ponownym przydzielaniem pamięci podręcznej, co może prowadzić do lepszej wydajności.

### Krok 5: Sprawdzenie przydzielonego rozmiaru pamięci podręcznej
Ten krok dotyczy monitorowania, ile bajtów jest obecnie przydzielonych dla pamięci podręcznej w pamięci lub na dysku. Zaimplementujmy to:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Przechowuje liczbę bajtów przydzielonych na dysku.  
- `long l2`: Przechowuje liczbę bajtów przydzielonych w pamięci.  
Możesz sprawdzić te wartości w dowolnym momencie, aby upewnić się, że aplikacja zarządza pamięcią i użyciem dysku zgodnie z oczekiwaniami.

### Krok 6: Tworzenie obrazu PSD
Teraz, gdy mamy skonfigurowane ustawienia pamięci podręcznej, utwórzmy prosty obraz PSD.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Ten obiekt pozwala określić opcje przy tworzeniu obrazu Photoshop.  
- `Color[] color`: Tablica zawierająca kolory, które będą użyte w palecie obrazu.

### Krok 7: Zapisywanie danych pikseli do obrazu
Teraz wypełnijmy nasz obraz danymi pikseli i zapiszmy go.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: To tablica obiektów koloru. Tutaj wypełniamy ją białymi pikselami.  
- `image.savePixels(image.getBounds(), pixels)`: Ta metoda zapisuje dane pikseli do obrazu. Aktualizuje obraz kolorami, które zdefiniowaliśmy.

### Krok 8: Monitorowanie przydzielonej pamięci podręcznej po utworzeniu obrazu
Po utworzeniu obrazu warto sprawdzić ponownie, ile bajtów jest przydzielonych dla pamięci podręcznej.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Rejestruje bieżące przydzielenie na dysku po utworzeniu obrazu.  
- `long memoryBytes`: Rejestruje bieżące przydzielenie w pamięci.  
Ten krok pomoże określić, ile pamięci podręcznej jest zużywane po wykonaniu operacji.

### Krok 9: Sprawdzenie prawidłowego zwalniania zasobów
Na koniec, kluczowe jest zapewnienie, że wszystkie obiekty Aspose.PSD zostały prawidłowo zwolnione, aby uniknąć wycieków pamięci.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` i `l2`: Te zmienne pomogą sprawdzić końcowe przydzielenie. Jeśli nie są zerowe, wskazuje to, że niektóre obiekty nie zostały prawidłowo zwolnione.

## Typowe problemy i rozwiązania
- **Folder pamięci podręcznej nie został utworzony** – Sprawdź, czy aplikacja ma uprawnienia do zapisu w ścieżce przekazanej do `Cache.setCacheFolder`.  
- **Błędy braku pamięci** – Upewnij się, że `Cache.setCacheType(CacheType.CacheOnDiskOnly)` jest zastosowane przed wczytaniem dużych plików PSD.  
- **Nieoczekiwany rozmiar pamięci podręcznej** – Użyj metod `Cache.getAllocated*BytesCount()` po każdej większej operacji, aby śledzić wzrost.

## Najczęściej zadawane pytania

**P: Co to jest Aspose.PSD?**  
O: Aspose.PSD to biblioteka dla programistów .NET i Java umożliwiająca programowe tworzenie, manipulację i konwersję plików Photoshop (PSD).

**P: Jak sprawdzić przydzielony rozmiar pamięci podręcznej?**  
O: Użyj metod takich jak `Cache.getAllocatedDiskBytesCount()` i `Cache.getAllocatedMemoryBytesCount()`, aby monitorować bieżące użycie pamięci podręcznej.

**P: Czy mogę ustawić własny katalog dla pamięci podręcznej?**  
O: Tak, możesz określić inny katalog, używając `Cache.setCacheFolder("Your Directory Path")`.

**P: Czy Aspose.PSD jest darmowy?**  
O: Aspose.PSD jest płatną biblioteką, ale możesz rozpocząć od darmowej wersji próbnej dostępnej na ich [stronie internetowej](https://releases.aspose.com/).

**P: Co się stanie, jeśli nie zwolnię obiektów?**  
O: Niezwolnienie obiektów może prowadzić do wycieków pamięci, powodując, że aplikacja będzie zużywać więcej zasobów niż konieczne.

## Podsumowanie
Kontrola ponownego przydzielania pamięci podręcznej podczas tworzenia aplikacji **create PSD image java** może znacząco wpłynąć na wydajność. Postępując zgodnie z powyższymi krokami, efektywnie zarządzisz pamięcią podręczną, zminimalizujesz zużycie pamięci i wygenerujesz wysokiej jakości pliki PSD przy użyciu Aspose.PSD for Java. Zastosuj te techniki, a Twoje projekty będą działały płynniej i lepiej skalowały się.

---

**Ostatnia aktualizacja:** 2026-03-13  
**Testowano z:** Aspose.PSD for Java (latest release)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-03-13
description: Dowiedz się, jak dodać warstwę odcienia i nasycenia do plików PSD przy
  użyciu Aspose.PSD for Java. Ten przewodnik pokazuje również, jak przetwarzać pliki
  PSD wsadowo i programowo tworzyć warstwę korekcji odcienia.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Dodaj warstwę odcienia i nasycenia do PSD przy użyciu Aspose.PSD dla Javy
url: /pl/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj warstwę nasycenia barwy do PSD

## Wprowadzenie
W projektowaniu graficznym manipulacja kolorami odgrywa kluczową rolę — szczególnie regulacja odcienia, nasycenia i jasności może diametralnie zmienić nastrój i jakość dowolnego obrazu. Jednym ze skutecznych sposobów osiągnięcia tego jest użycie warstw dopasowania w Photoshopie (pliki PSD). Jeśli chcesz **add hue saturation layer** programowo przy użyciu Javy, biblioteka Aspose.PSD jest tutaj, aby pomóc! Ten samouczek przeprowadzi Cię krok po kroku przez dodanie warstwy dopasowania Hue Saturation do Twoich plików PSD, zwiększając produktywność i efektywność pracy.

## Szybkie odpowiedzi
- **Jaką bibliotekę użyć, aby dodać warstwę nasycenia barwy w Javie?** Aspose.PSD for Java.  
- **Czy potrzebny jest zainstalowany Photoshop?** Nie, biblioteka działa niezależnie od Photoshopa.  
- **Czy mogę przetwarzać pliki PSD wsadowo przy użyciu tego podejścia?** Tak — po automatyzacji kroków możesz zastosować je do wielu plików.  
- **Jaka wersja Javy jest wymagana?** JDK 8 lub nowsza.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Tak, po okresie próbnym wymagana jest licencja komercyjna.

## Co to jest operacja „add hue saturation layer”?
Operacja **add hue saturation layer** tworzy warstwę dopasowania, która nie jest destrukcyjna i pozwala modyfikować wartości odcienia, nasycenia i jasności bez zmiany oryginalnych danych pikseli. Jest to idealne rozwiązanie do precyzyjnego dostrajania kolorów w całej kompozycji lub w określonych zakresach kolorów.

## Dlaczego warto używać Aspose.PSD dla Javy?
- **Brak zależności od Photoshopa** – działa na każdej platformie obsługującej Javę.  
- **Pełna wierność PSD** – zachowuje wszystkie informacje o warstwach, maskach i efektach.  
- **Gotowość do przetwarzania wsadowego** – możesz przechodzić przez foldery i stosować te same korekty do dziesiątek plików.  
- **Skoncentrowanie na wydajności** – zoptymalizowane pod kątem dużych dokumentów i automatyzacji po stronie serwera.

## Wymagania wstępne
Zanim przejdziemy do kodu, upewnij się, że masz przygotowane następujące elementy:

1. **Java Development Kit (JDK):** Upewnij się, że masz zainstalowany JDK 8 lub nowszy. Możesz go pobrać z [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java Library:** Potrzebujesz biblioteki Aspose.PSD, którą możesz [pobrać tutaj](https://releases.aspose.com/psd/java/).  
3. **IDE:** Odpowiednie zintegrowane środowisko programistyczne (IDE), takie jak IntelliJ IDEA lub Eclipse, do programowania w Javie.  
4. **Podstawowa znajomość Javy:** Znajomość programowania w Javie jest dodatkowym atutem, ale nie martw się — przeprowadzimy Cię przez każdy wiersz kodu.

Teraz, gdy mamy już spełnione wymagania wstępne, przejdźmy do najciekawszej części — kodowania!

## Importowanie pakietów
Aby rozpocząć pracę z biblioteką Aspose.PSD, pierwszym krokiem jest zaimportowanie niezbędnych klas. Oto jak zrobić to w pliku Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

Upewnij się, że odpowiednie biblioteki zostały dodane do projektu, aby te importy działały bezproblemowo.

## Krok 1: Ustaw katalog dokumentów
Każdy projekt potrzebuje punktu wyjścia i nasz nie jest wyjątkiem. Musisz określić katalog, w którym przechowywane są pliki PSD. Jest to kluczowe dla prawidłowego ładowania i zapisywania obrazów.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Krok 2: Załaduj istniejący plik PSD
Aby manipulować istniejącym plikiem PSD, najpierw musimy go wczytać do programu. Oto jak to zrobić:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

W tym kodzie zaktualizuj `"HueSaturationAdjustmentLayer.psd"` na nazwę swojego istniejącego pliku PSD, który chcesz edytować.

## Krok 3: Edytuj warstwę Hue/Saturation
Następnie przeiterujemy warstwy załadowanego obrazu PSD, aby znaleźć i edytować istniejące warstwy Hue/Saturation. Ten krok obejmuje modyfikację wartości odcienia, nasycenia i jasności.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

W tym przykładzie:  
- Ustawiamy odcień na **-25**, nasycenie na **-12**, a jasność na **+67**.  
- Metoda `getRange(2)` pozwala dostosować konkretne zakresy kolorów według potrzeb.

## Krok 4: Zapisz zmodyfikowany plik PSD
Po wprowadzeniu korekt następnym krokiem jest zapisanie pliku. To ważny element procesu, zapewniający, że wprowadzone zmiany nie zostaną utracone.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Krok 5: Dodaj nową warstwę Hue/Saturation
Jeśli potrzebujesz **create hue adjustment layer** od podstaw, możesz dodać zupełnie nową warstwę dopasowania Hue/Saturation do innego pliku PSD. Skorzystaj z tego samego schematu ładowania, ale użyj metody `addHueSaturationAdjustmentLayer()`.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Krok 6: Ustaw nowe wartości Hue/Saturation dla nowej warstwy
Teraz, gdy utworzyłeś nową warstwę, zastosuj pożądane ustawienia odcienia, nasycenia i jasności tak jak wcześniej.

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## Krok 7: Zapisz zaktualizowany plik PSD
Na koniec zapisz plik PSD z dodaną warstwą Hue/Saturation, aby zobaczyć wprowadzone zmiany.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

Gratulacje! Pomyślnie manipulowałeś plikami PSD przy użyciu Aspose.PSD for Java. Teraz możesz eksperymentować z różnymi obrazami i głębszymi modyfikacjami, ożywiając swoje projekty graficzne.

## Jak przetwarzać pliki PSD wsadowo z korektami barwy
Ponieważ powyższy kod jest w pełni skryptowalny, możesz owinąć całą sekwencję w pętlę iterującą po każdym pliku `.psd` w folderze. Dzięki temu możesz **batch process psd files** i zastosować te same korekty odcienia, nasycenia i jasności w jednym uruchomieniu — idealne rozwiązanie dla masowych aktualizacji brandingu.

## Typowe problemy i rozwiązania
- **NullPointerException przy ładowaniu pliku:** Sprawdź, czy `dataDir` kończy się odpowiednim separatorem plików (`/` lub `\`) oraz czy nazwa pliku jest poprawna.  
- **Wartości korekty poza zakresem:** Odcień, nasycenie i jasność przyjmują wartości od -255 do 255. Trzymaj się tego zakresu.  
- **Warstwa nie znaleziona:** Jeśli PSD nie zawiera warstwy Hue/Saturation, sprawdzenie `instanceof` pominie blok. Użyj `addHueSaturationAdjustmentLayer()`, aby najpierw ją utworzyć.

## Najczęściej zadawane pytania

**Q: Czym jest warstwa dopasowania Hue Saturation?**  
A: Pozwala modyfikować właściwości kolorystyczne obrazu bez trwałej zmiany oryginalnych pikseli.

**Q: Czy muszę mieć zainstalowany Photoshop, aby używać Aspose.PSD?**  
A: Nie, Aspose.PSD to samodzielna biblioteka działająca niezależnie od Photoshopa.

**Q: Czy mogę używać Aspose.PSD do przetwarzania wsadowego?**  
A: Tak, możesz automatyzować i przetwarzać wsadowo wiele plików PSD przy użyciu Aspose.PSD.

**Q: Czy Aspose.PSD jest darmowy?**  
A: Aspose.PSD oferuje bezpłatną wersję próbną, ale do długoterminowego użytkowania wymagana jest licencja. Cennik możesz zobaczyć [tutaj](https://purchase.aspose.com/buy).

## Zakończenie
Praca z grafiką programowo otwiera świat możliwości. Korzystanie z Aspose.PSD for Java do **add hue saturation layer** oraz **create hue adjustment layer** zapewnia elastyczność i wydajność, które mogą usprawnić Twój przepływ pracy projektowej. Niezależnie od tego, czy ulepszasz zdjęcia do projektu, czy tworzysz zachwycające treści wizualne, opanowanie tych narzędzi znacząco podniesie jakość Twoich rezultatów.

Śmiało eksploruj kolejne funkcje Aspose.PSD, zagłębiając się w [documentation](https://reference.aspose.com/psd/java/) lub rozważ uzyskanie [temporary license](https://purchase.aspose.com/temporary-license/), aby przetestować pełną moc biblioteki.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---
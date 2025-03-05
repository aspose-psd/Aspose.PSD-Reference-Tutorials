---
title: Dodaj warstwę dopasowania nasycenia odcienia do PSD
linktitle: Dodaj warstwę dopasowania nasycenia odcienia do PSD
second_title: Aspose.PSD API Java
description: Dowiedz się, jak dodać warstwy dopasowania nasycenia odcienia do PSD przy użyciu Aspose.PSD dla Java, w tym kompleksowym samouczku krok po kroku. Ulepsz swój proces projektowania graficznego.
type: docs
weight: 14
url: /pl/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## Wstęp
Jeśli chodzi o projektowanie graficzne, manipulacja kolorami odgrywa kluczową rolę — w szczególności poprawianie odcienia, nasycenia i jasności może radykalnie zmienić nastrój i jakość każdego obrazu. Jednym ze skutecznych sposobów osiągnięcia tego jest użycie warstw dopasowania w programie Photoshop (pliki PSD). Jeśli chcesz programowo ulepszyć swoje pliki PSD przy użyciu języka Java, biblioteka Aspose.PSD jest tutaj, aby Ci pomóc! Ten samouczek przeprowadzi Cię przez kolejne etapy dodawania warstwy dopasowania nasycenia odcienia do plików PSD, dzięki czemu Twoja praca stanie się bardziej produktywna i wydajna.
tym przewodniku omówimy wszystko, od importowania niezbędnych pakietów po najdrobniejsze szczegóły przykładów kodu.
## Warunki wstępne
Zanim przejdziemy do kodu, upewnij się, że masz następujące elementy:
1.  Zestaw Java Development Kit (JDK): Upewnij się, że na komputerze jest zainstalowany pakiet JDK 8 lub nowszy. Można go pobrać z[Pobieranie zestawu deweloperskiego Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD dla biblioteki Java: Będziesz potrzebować biblioteki Aspose.PSD, co możesz zrobić[pobierz tutaj](https://releases.aspose.com/psd/java/). 
3. IDE: odpowiednie zintegrowane środowisko programistyczne (IDE), takie jak IntelliJ IDEA lub Eclipse do programowania w języku Java.
4. Podstawowa znajomość języka Java: Znajomość programowania w języku Java będzie dodatkowym atutem, ale nie martw się; przeprowadzimy Cię przez kod krok po kroku.
Teraz, gdy mamy już ustalone wymagania wstępne, przejdźmy do przyjemniejszej części — kodowania!
## Importuj pakiety
Aby rozpocząć pracę z biblioteką Aspose.PSD, pierwszym krokiem jest zaimportowanie niezbędnych klas. Oto jak możesz to zrobić w pliku Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Upewnij się, że do projektu dodano odpowiednie biblioteki, aby importy przebiegały bezproblemowo.
## Krok 1: Skonfiguruj katalog dokumentów
Każdy projekt potrzebuje punktu wyjścia i nasz nie jest wyjątkiem. Musisz określić katalog, w którym przechowywane są pliki PSD. Ma to kluczowe znaczenie dla prawidłowego ładowania i zapisywania obrazów.
```java
String dataDir = "Your Document Directory"; // Zaktualizuj tę ścieżkę do rzeczywistego katalogu
```
## Krok 2: Załaduj istniejący plik PSD
Aby manipulować istniejącym plikiem PSD, musimy najpierw załadować go do naszego programu. Oto jak możesz to zrobić:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 W tym kodzie zaktualizuj`"HueSaturationAdjustmentLayer.psd"` do nazwy istniejącego pliku PSD, który chcesz edytować.
## Krok 3: Edytuj warstwę Barwa/Nasycenie
Następnie będziemy przeglądać warstwy załadowanego obrazu PSD, aby znaleźć i edytować istniejące warstwy Barwa/Nasycenie. Ten krok obejmuje modyfikację wartości odcienia, nasycenia i jasności.
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
- Dostosowujemy odcień do -25, nasycenie do -12 i jasność do +67.
-  The`getRange(2)` Metoda pozwala nam dostosować określone zakresy kolorów według potrzeb.
## Krok 4: Zapisz zmodyfikowany plik PSD
Po dokonaniu poprawek kolejnym krokiem jest zapisanie pliku. Jest to istotna część naszego procesu, zapewniająca, że wprowadzone przez nas zmiany nie zostaną utracone.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Krok 5: Dodaj nową warstwę odcienia/nasycenia
Następnie możesz dodać nową warstwę dopasowania Barwa/Nasycenie do innego pliku PSD. Po prostu zastosuj to samo podejście, które zastosowałeś wcześniej, ale z innymi plikami PSD.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Krok 6: Ustaw nowe wartości odcienia/nasycenia dla nowej warstwy
Po utworzeniu nowej warstwy zastosuj żądane ustawienia odcienia, nasycenia i jasności, tak jak poprzednio.
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
Na koniec zapisz plik PSD z dodaną warstwą Barwa/Nasycenie, aby móc zobaczyć wprowadzone zmiany.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Gratulacje! Udało Ci się manipulować plikami PSD przy użyciu Aspose.PSD dla Java. Teraz możesz eksperymentować z różnymi obrazami i głębszymi zmianami, ożywiając swoje projekty graficzne.
## Wniosek
Programowa praca z grafiką otwiera świat możliwości. Korzystanie z Aspose.PSD dla Java w celu dodawania i modyfikowania warstw dopasowania nasycenia odcienia zapewnia elastyczność i wydajność, które mogą usprawnić przepływ prac projektowych. Niezależnie od tego, czy ulepszasz zdjęcia do projektu, czy tworzysz oszałamiającą treść wizualną, opanowanie tych narzędzi może znacznie poprawić wydajność.
 Zachęcamy do odkrywania większej liczby funkcjonalności Aspose.PSD, zagłębiając się w nie[dokumentacja](https://reference.aspose.com/psd/java/) lub rozważ złapanie a[licencja tymczasowa](https://purchase.aspose.com/temporary-license/) aby przetestować pełną moc biblioteki.
## Często zadawane pytania
### Co to jest warstwa dopasowania nasycenia odcienia?
Warstwa dopasowania nasycenia odcienia umożliwia modyfikowanie właściwości kolorów obrazu bez trwałej zmiany oryginalnych pikseli.
### Czy muszę mieć zainstalowany program Photoshop, aby móc korzystać z Aspose.PSD?
Nie, Aspose.PSD to samodzielna biblioteka działająca niezależnie od programu Photoshop.
### Czy mogę używać Aspose.PSD do przetwarzania wsadowego?
Tak, możesz zautomatyzować i przetwarzać wsadowo wiele plików PSD za pomocą Aspose.PSD.
### Czy Aspose.PSD jest darmowy?
Aspose.PSD oferuje bezpłatną wersję próbną, ale do długotrwałego użytkowania wymagana jest licencja. Możesz zobaczyć ceny[Tutaj](https://purchase.aspose.com/buy).
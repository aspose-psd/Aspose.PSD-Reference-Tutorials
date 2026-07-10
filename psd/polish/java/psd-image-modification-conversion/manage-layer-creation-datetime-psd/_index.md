---
date: 2026-03-28
description: Dowiedz się, jak utworzyć nową warstwę PSD i zarządzać jej datą i godziną
  utworzenia przy użyciu Aspose.PSD for Java. Ten przewodnik krok po kroku obejmuje
  ładowanie, odczytywanie, weryfikację i dodawanie warstw.
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: Utwórz nową warstwę PSD i zarządzaj datą oraz godziną jej utworzenia w Javie
url: /pl/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz nową warstwę PSD i zarządzaj datą i godziną utworzenia w Javie

## Wprowadzenie
Kiedy programowo pracujesz z plikami Photoshop (PSD), możliwość **tworzenia nowych obiektów warstwy PSD** i śledzenia ich znaczników czasu utworzenia jest prawdziwym przełomem. Niezależnie od tego, czy budujesz system kontroli wersji zasobów graficznych, automatyzujesz masowe edycje, czy po prostu potrzebujesz ścieżki audytu dla projektów zespołowych, znajomość sposobu odczytywania i ustawiania daty utworzenia warstwy pozwala zachować pełną historię każdego zmian. W tym samouczku przejdziemy krok po kroku przez cały proces przy użyciu Aspose.PSD dla Javy — od załadowania PSD, pobrania daty utworzenia warstwy, jej weryfikacji, po dodanie zupełnie nowej warstwy dopasowania.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje pliki PSD w Javie?** Aspose.PSD dla Javy  
- **Czy mogę odczytać datę utworzenia warstwy?** Tak, używając `layer.getLayerCreationDateTime()`  
- **Czy można dodać nową warstwę dopasowania?** Oczywiście – `im.addLevelsAdjustmentLayer()` tworzy taką warstwę  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Licencja komercyjna jest wymagana dla wdrożeń nie‑testowych  
- **Jaką wersję Javy obsługuje?** JDK 8 lub nowsza  

## Co oznacza „create new PSD layer”?
Tworzenie nowej warstwy PSD oznacza programowe wstawienie świeżego obiektu warstwy — takiego jak warstwa dopasowania, tekstowa lub pikselowa — do istniejącego dokumentu PSD. Ta operacja pozwala rozszerzyć lub zmodyfikować obraz bez ręcznego otwierania Photoshopa.

## Dlaczego zarządzać DateTime utworzenia warstwy?
Śledzenie daty i godziny utworzenia każdej warstwy pomaga:
- **Audytować wersje** – dokładnie wiedzieć, kiedy warstwa została dodana.  
- **Synchronizować zasoby** między zespołami, porównując znaczniki czasu.  
- **Automatyzować przepływy pracy**, które zależą od reguł czasowych (np. ukrywać warstwy starsze niż miesiąc).  

## Wymagania wstępne
Zanim przejdziesz dalej, upewnij się, że masz przygotowane:

1. **Java Development Kit (JDK)** – wersja 8 lub nowsza.  
2. **IDE** – IntelliJ IDEA, Eclipse, NetBeans lub dowolny edytor, którego używasz.  
3. **Aspose.PSD dla Javy** – możesz [pobrać go tutaj](https://releases.aspose.com/psd/java/) w celu instalacji.  
4. **Podstawową znajomość Javy** – jeśli dopiero zaczynasz, nie martw się; kod jest w pełni skomentowany.

Masz wszystko? Świetnie! Przejdźmy do najciekawszej części kodowania.

## Importowanie pakietów
Najpierw zaimportuj klasy Aspose.PSD oraz potrzebne utilsy Javy. Te importy dają dostęp do obsługi obrazu, manipulacji warstwami i formatowania dat.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## Krok 1: Ustaw katalog dokumentu
Określ folder zawierający PSD, z którym chcesz pracować. Zamień placeholder na absolutną ścieżkę na swoim komputerze.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Załaduj plik PSD
Utwórz instancję `PsdImage`, ładując docelowy plik. Ten obiekt jest punktem wejścia dla wszystkich operacji na warstwach.

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## Krok 3: Uzyskaj dostęp do warstwy i jej daty utworzenia
Pobierz pierwszą warstwę (indeks 0) i odczytaj jej znacznik czasu utworzenia. To data, którą później porównasz lub zalogujesz.

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## Krok 4: Sformatuj datę utworzenia
Przekształć surowy obiekt `Date` w czytelny dla człowieka ciąg znaków. Dostosuj wzorzec, jeśli wolisz inny format.

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## Krok 5: Zweryfikuj datę utworzenia
Dla demonstracji porównujemy pobraną datę z oczekiwaną wartością. W rzeczywistych projektach możesz porównywać ją z rekordem w bazie danych lub plikiem konfiguracyjnym.

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## Krok 6: Utwórz nową warstwę
Teraz faktycznie **tworzymy nowe obiekty warstwy PSD**. Dodajemy warstwę dopasowania Levels, która pozwala regulować zakresy tonalne bez modyfikacji oryginalnych pikseli.

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **Pro tip:** Zmienna `now` przechowuje moment, w którym warstwa została dodana; możesz ją później zapisać jako metadane, jeśli potrzebujesz własnego znacznika czasu.

## Typowe problemy i rozwiązania
| Problem | Dlaczego się pojawia | Rozwiązanie |
|-------|----------------|-----|
| `NullPointerException` przy `layer.getLayerCreationDateTime()` | PSD nie ma warstw lub indeks warstwy jest poza zakresem. | Sprawdź, czy `im.getLayers().length > 0` przed dostępem. |
| Niepasująca data w weryfikacji | Konstruktor `Date` parsuje ciągi zależnie od lokalizacji. | Użyj `SimpleDateFormat.parse("2018/07/17 08:57:24")` dla pewnego parsowania. |
| Nowa warstwa niewidoczna w Photoshopie | Warstwa dopasowania może być domyślnie ukryta. | Wywołaj `createdLayer.setVisible(true);` po jej utworzeniu. |

## Zakończenie
Teraz wiesz, jak **tworzyć nowe obiekty warstwy PSD**, odczytywać ich znaczniki czasu utworzenia, weryfikować te znaczniki oraz dodawać warstwy dopasowania — wszystko przy użyciu Aspose.PSD dla Javy. Ta możliwość otwiera drzwi do zaawansowanej automatyzacji, ścieżek audytu i współpracy w dowolnym pipeline przetwarzania obrazów opartym na Javie.

Jeśli podobał Ci się ten samouczek, odkryj inne funkcje Aspose.PSD, takie jak scalanie warstw, stosowanie filtrów czy eksport do różnych formatów. Możliwości są nieograniczone!

## FAQ's
### Co to jest Aspose.PSD?  
Aspose.PSD to potężna biblioteka do programowego pracy z plikami Photoshop (PSD).
### Czy mogę używać Aspose.PSD za darmo?  
Tak! Możesz rozpocząć od darmowej wersji próbnej dostępnej [tutaj](https://releases.aspose.com/).
### Czy muszę kupić licencję na długoterminowe użycie?  
Tak, licencję możesz nabyć [tutaj](https://purchase.aspose.com/buy), gdy będziesz gotowy.
### Gdzie znajdę więcej informacji o Aspose.PSD?  
Szczegółowe przewodniki i referencje API znajdziesz w [dokumentacji](https://reference.aspose.com/psd/java/).
### Jak mogę uzyskać wsparcie, jeśli napotkam problemy z Aspose.PSD?  
Odwiedź [forum wsparcia](https://forum.aspose.com/c/psd/34) dla pomocy społeczności.

---

**Ostatnia aktualizacja:** 2026-03-28  
**Testowane z:** Aspose.PSD dla Javy 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
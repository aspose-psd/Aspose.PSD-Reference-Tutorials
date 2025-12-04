---
date: 2025-12-04
description: Dowiedz się, jak zapisać plik PSD jako PNG i zastosować renderowany cień
  padający przy użyciu Aspose.PSD dla Javy. Ten przewodnik opisuje, jak dodać cień,
  przekonwertować PSD na PNG oraz zastosować cień padający w Javie.
language: pl
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Zapisz PSD jako PNG i dodaj cień przy użyciu Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz PSD jako PNG i dodaj cień rzutu z Aspose.PSD Java

## Wstęp

Jeśli pracujesz z plikami Photoshop w Javie, **zapisanie PSD jako PNG** z jednoczesnym dodaniem profesjonalnie wyglądającego cienia rzutu jest częstym wymaganiem. Aspose.PSD upraszcza to zadanie, umożliwiając **konwersję PSD do PNG** oraz **zastosowanie cienia rzutu w Javie** w kilku linijkach kodu. W tym samouczku przeprowadzimy Cię przez cały proces, od załadowania pliku PSD po wyeksportowanie finalnego PNG z wyrenderowanym efektem cienia.

## Szybkie odpowiedzi
- **Co oznacza „zapisz PSD jako PNG”?** Konwertuje warstwowy plik Photoshop na płaski obraz PNG, zachowując przezroczystość.  
- **Czy mogę dodać cień rzutu podczas konwersji?** Tak — Aspose.PSD pozwala modyfikować efekty warstw przed eksportem.  
- **Czy potrzebna jest licencja do uruchomienia kodu?** Darmowa wersja próbna wystarczy do oceny; licencja jest wymagana w środowisku produkcyjnym.  
- **Jaką wersję Javy obsługuje?** Java 8 lub nowsza.  
- **Czy efekt cienia rzutu jest konfigurowalny?** Oczywiście — możesz dostosować kolor, krycie, odległość, rozmiar, kąt i wiele innych parametrów.

## Wymagania wstępne

Zanim przejdziemy dalej, upewnij się, że masz:

- **Środowisko programistyczne Java** – zainstalowany JDK 8 lub nowszy.  
- **Bibliotekę Aspose.PSD** – pobierz najnowszy plik JAR z oficjalnej strony [here](https://releases.aspose.com/psd/java/).  
- **Plik PSD** – plik zawierający przynajmniej jedną warstwę, którą chcesz wzbogacić o cień.  

## Jak zapisać PSD jako PNG z cieniem rzutu w Javie?

Poniżej znajdziesz przewodnik krok po kroku. Każdy krok zawiera krótkie wyjaśnienie oraz dokładny kod, który należy skopiować.

### Krok 1: Importuj wymagane pakiety

Zaczynamy od zaimportowania klas, które umożliwiają ładowanie obrazu, obsługę efektów i eksport do PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Krok 2: Zdefiniuj katalog dokumentu

Ustaw folder, w którym będą znajdować się źródłowy PSD oraz wynikowy PNG.

```java
String dataDir = "Your Document Directory";
```

### Krok 3: Ustaw ścieżki plików PSD i PNG

Określ pełne ścieżki do wejściowego pliku PSD oraz wyjściowego pliku PNG.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Krok 4: Załaduj plik PSD z włączonymi efektami

Włączenie **loadEffectsResource** zapewnia dostęp do efektów warstw (takich jak cienie) w celu ich modyfikacji.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Krok 5: Uzyskaj dostęp do efektu Drop Shadow

Tutaj pobieramy pierwszy efekt zastosowany do drugiej warstwy (indeks 1). To miejsce, w którym odczytujemy lub modyfikujemy parametry cienia.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Krok 6: Zweryfikuj właściwości efektu cienia (opcjonalnie, ale przydatne)

Sprawdzenie istniejących właściwości pomaga zdecydować, czy trzeba coś zmienić. Poniższe asercje potwierdzają wartości domyślne.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Pro tip:** Jeśli chcesz **jak dodać cień** z własnymi ustawieniami, zmodyfikuj właściwości obiektu `shadowEffect` przed zapisem (np. `shadowEffect.setColor(Color.getRed());`).

### Krok 7: Zapisz zmodyfikowany obraz jako PNG

Na koniec eksportujemy PSD (z wyrenderowanym cieniem) do pliku PNG. Opcja `TruecolorWithAlpha` zachowuje przezroczystość.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

I gotowe — kompletny **workflow konwersji PSD do PNG**, który jednocześnie **zastosuje cień rzutu w Javie** w jednym przebiegu.

## Dlaczego warto używać Aspose.PSD do tego zadania?

- **Brak wymogu posiadania Photoshopa** – Działa na każdej platformie obsługującej Javę.  
- **Pełna wierność PSD** – Wszystkie informacje o warstwach, maskach i efektach są zachowane.  
- **Precyzyjna kontrola** – Możesz dostosować każdy parametr cienia rzutu przed eksportem.  
- **Wysoka wydajność** – Optymalizowane pod kątem dużych plików i przetwarzania wsadowego.

## Typowe problemy i rozwiązywanie

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|-------|--------------------------|-------------|
| `NullPointerException` on `shadowEffect` | Docelowa warstwa nie ma efektów lub indeks jest nieprawidłowy. | Zweryfikuj indeks warstwy (`im.getLayers()[i]`) i upewnij się, że efekt istnieje. |
| Wyeksportowany PNG jest pusty | Opcje PNG nie zostały ustawione poprawnie lub obraz nie został zapisany. | Użyj `PngColorType.TruecolorWithAlpha` i potwierdź, że ścieżka w `im.save()` jest zapisywalna. |
| Kolor cienia nie jest widoczny | Krycie cienia ustawione na 0 lub kolor jest taki sam jak tło. | Ustaw `shadowEffect.setOpacity(255);` i wybierz kontrastowy kolor. |

## Najczęściej zadawane pytania

**P: Czy mogę zastosować cienie rzutu do wielu warstw jednocześnie?**  
O: Tak. Przejdź pętlą przez `im.getLayers()` i zmodyfikuj każdy `DropShadowEffect` według potrzeb.

**P: Co robi parametr „Spread”?**  
O: Kontroluje, jak gwałtownie cień przechodzi od pełnej nieprzezroczystości do przezroczystości. Wyższy spread tworzy twardszą krawędź.

**P: Czy Aspose.PSD jest kompatybilny ze wszystkimi wersjami Photoshopa?**  
O: Obsługuje szeroki zakres wersji PSD, od wczesnych wydań po najnowsze pliki Photoshop CC.

**P: Jak mogę uzyskać pomoc, jeśli napotkam problemy?**  
O: Odwiedź [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) dla wsparcia społeczności i oficjalnej pomocy.

**P: Czy mogę wypróbować Aspose.PSD przed zakupem?**  
O: Oczywiście. Pobierz darmową wersję próbną z [strony Aspose](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Ostatnia aktualizacja:** 2025-12-04  
**Testowano z:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  

---
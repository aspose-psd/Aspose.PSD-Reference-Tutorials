---
date: 2025-11-30
description: Dowiedz się, jak dodać obrys i zmienić kolor obrysu w pliku PSD przy
  użyciu Aspose.PSD dla Javy. Postępuj zgodnie z tym przewodnikiem krok po kroku,
  aby zmodyfikować kolor i krycie warstwy obrysu.
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Jak dodać kolor obrysu warstwy w Aspose.PSD dla Javy
url: /pl/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać kolor warstwy obramowania w Aspose.PSD dla Javy

## Wprowadzenie

Jeśli potrzebujesz **jak dodać obramowanie** do dokumentu Photoshop programowo, Aspose.PSD dla Javy umożliwia to w prosty sposób. W tym samouczku przejdziemy przez dodawanie koloru warstwy obramowania, regulację jego krycia oraz zapisanie wyniku. Na koniec zobaczysz także, **jak zmienić kolor obramowania** (lub *change PSD stroke color*) dla dowolnej istniejącej warstwy, dając pełną kontrolę kreatywną z poziomu kodu Java.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.PSD dla Javy (najnowsza wersja).  
- **Czy mogę zmienić kolor obramowania?** Tak – użyj `ColorFillSettings`, aby ustawić dowolny `Color`.  
- **Czy potrzebna jest licencja?** Tymczasowa licencja działa w trybie ewaluacyjnym; pełna licencja jest wymagana w produkcji.  
- **Jaką wersję Javy obsługuje?** Java 8 lub wyższą.  
- **Jak długo trwa implementacja?** Zazwyczaj poniżej 10 minut dla podstawowej zmiany obramowania.

## Co to jest warstwa obramowania w PSD?
Warstwa obramowania to efekt wektorowy, który rysuje kontur wokół zawartości warstwy. Można go dostosować pod względem koloru, grubości, krycia i trybu mieszania. Modyfikowanie tego efektu programowo umożliwia automatyzację brandingu, przetwarzanie wsadowe lub dynamiczne generowanie grafiki.

## Dlaczego warto używać Aspose.PSD do zmiany koloru obramowania?
- **Brak wymogu Photoshopa** – pracuj w pełni w Javie.  
- **Pełna zgodność ze specyfikacją PSD** – wszystkie nowoczesne funkcje PSD są obsługiwane.  
- **Wysoka wydajność** – szybkie przetwarzanie dużych plików.  
- **Cross‑platform** – działa na każdym systemie operacyjnym z JVM.

## Wymagania wstępne

- **Biblioteka Aspose.PSD** – pobierz z [oficjalnej dokumentacji](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – wersja 8 lub nowsza.  
- **IDE** – Eclipse, IntelliJ IDEA lub dowolny edytor kompatybilny z Javą.

## Importowanie pakietów

Najpierw zaimportuj klasy, które będą potrzebne. Dzięki temu projekt uzyska dostęp do API obsługi PSD oraz efektów obramowania.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Krok 1: Konfiguracja projektu

Utwórz nowy projekt Java, dodaj plik JAR Aspose.PSD do ścieżki kompilacji i sprawdź, czy biblioteka ładuje się bez błędów.

## Krok 2: Załaduj plik PSD

Włącz ładowanie zasobów efektów, aby informacje o obramowaniu były dostępne.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Krok 3: Uzyskaj dostęp do warstwy efektu obramowania

Pobierz pierwszy efekt obramowania z drugiej warstwy (indeks 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Krok 4: Zweryfikuj właściwości obramowania

Potwierdź istniejące właściwości przed wprowadzeniem zmian. To pomaga uniknąć nieoczekiwanych rezultatów.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Krok 5: Ustaw kolor i krycie (Jak zmienić kolor obramowania)

Tutaj **zmieniamy kolor obramowania PSD** na żółty i redukujemy krycie do 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Krok 6: Zapisz zmodyfikowany plik PSD

Zapisz zaktualizowany obraz z powrotem na dysk. Nowy plik zawiera zmodyfikowane obramowanie.

```java
im.save(exportPath);
```

## Częste pułapki i wskazówki

- **Sprawdzanie null** – zawsze weryfikuj, czy `getEffects()` zwraca nie‑nullową tablicę przed rzutowaniem.  
- **Indeks warstwy** – warstwy PSD są numerowane od zera; upewnij się, że celujesz w właściwą warstwę.  
- **Format koloru** – `Color.getYellow()` to tylko przykład; możesz tworzyć własne kolory przy pomocy `new Color(r, g, b)`.  
- **Zakres krycia** – krycie jest bajtem (0–255); wartości powyżej 255 zostaną przycięte.

## Zakończenie

Teraz wiesz, **jak dodać obramowanie** do pliku PSD oraz **jak zmienić kolor obramowania** przy użyciu Aspose.PSD dla Javy. Eksperymentuj z różnymi kolorami, trybami mieszania i kryciami, aby uzyskać dokładnie taki styl wizualny, jaki potrzebuje Twój projekt.

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.PSD z innymi bibliotekami graficznymi Javy?**  
O: Tak, Aspose.PSD może być łączony z takimi bibliotekami jak Apache Commons Imaging czy Java2D w celu rozszerzenia funkcjonalności.

**P: Czy Aspose.PSD jest kompatybilny z najnowszym formatem plików PSD?**  
O: Zdecydowanie. Biblioteka jest regularnie aktualizowana, aby obsługiwać najnowsze specyfikacje Photoshopa.

**P: Jak obsługiwać wyjątki podczas korzystania z Aspose.PSD?**  
O: Zapoznaj się z [forum wsparcia](https://forum.aspose.com/c/psd/34), gdzie znajdziesz szczegółowe porady dotyczące rozwiązywania problemów i przykładowy kod obsługi błędów.

**P: Czy mogę wypróbować Aspose.PSD przed zakupem?**  
O: Oczywiście! Pobierz [bezpłatną wersję próbną](https://releases.aspose.com/), aby przetestować wszystkie funkcje.

**P: Gdzie mogę uzyskać tymczasową licencję dla Aspose.PSD?**  
O: Uzyskaj [tymczasową licencję](https://purchase.aspose.com/temporary-license/), aby ocenić bibliotekę w swoim środowisku deweloperskim.

---

**Ostatnia aktualizacja:** 2025-11-30  
**Testowano z:** Aspose.PSD 24.11 dla Javy  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
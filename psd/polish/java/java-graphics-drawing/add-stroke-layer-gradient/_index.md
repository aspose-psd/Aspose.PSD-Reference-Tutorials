---
date: 2026-01-14
description: Dowiedz się, jak utworzyć warstwę obrysu gradientowego i dostosować gradienty
  obrysu w plikach PSD przy użyciu Aspose.PSD for Java w tym samouczku krok po kroku.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Jak utworzyć warstwę gradientowego obrysu w Javie
url: /pl/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak utworzyć warstwę obrysu gradientowego w Javie

## Wprowadzenie
Zastanawiałeś się kiedyś, jak **create gradient stroke layer** w swoich plikach PSD przy użyciu Javy? Jesteś we właściwym miejscu! Dziś zagłębimy się w Aspose.PSD for Java — potężną bibliotekę, która umożliwia łatwą manipulację plikami PSD. Niezależnie od tego, czy dopiero zaczynasz przygodę z programowaniem grafiki, czy chcesz dopracować istniejące projekty, ten przewodnik poprowadzi Cię krok po kroku przez dodawanie i dostosowywanie gradientów obrysu.

## Szybkie odpowiedzi
- **Jaki jest główny cel?** Utworzyć warstwę obrysu gradientowego w pliku PSD.  
- **Jakiej biblioteki potrzebujesz?** Aspose.PSD for Java.  
- **Czy potrzebna jest licencja?** Tak, wymagana jest ważna (lub tymczasowa) licencja do produkcji.  
- **Jaką wersję Javy obsługuje?** Java 8 lub wyższą.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego obrysu gradientowego.

## Czym jest warstwa obrysu gradientowego?
Warstwa obrysu gradientowego to wektorowy kontur wokół kształtu lub tekstu, który płynnie przechodzi pomiędzy kolorami. Korzystając z Aspose.PSD możesz programowo określić kolory, krycie, kąt i typ (liniowy, radialny itp.) obrysu.

## Dlaczego używać Aspose.PSD for Java?
- **Pełne wsparcie PSD** – odczyt, edycja i zapis plików PSD bez Photoshopa.  
- **Bogate API efektów** – dostęp do obrysu, cienia, poświaty i wielu innych efektów warstwy.  
- **Cross‑platform** – działa na każdym systemie operacyjnym obsługującym Javę.  
- **Brak natywnych zależności** – czysta Java, łatwa integracja z pipeline'ami CI.

## Wymagania wstępne
1. **Java Development Kit (JDK)** – Zainstaluj najnowszy JDK ze [strony Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – Pobierz bibliotekę ze [strony pobierania Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub NetBeans.  
4. **Licencja** – Uzyskaj [tymczasową licencję](https://purchase.aspose.com/temporary-license/), jeśli nie masz pełnej.

## Importowanie pakietów
Najpierw zaimportuj klasy, które będą potrzebne do ładowania PSD, dostępu do efektów i konfigurowania wypełnień gradientowych.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

Teraz podzielmy proces na przejrzyste kroki.

## Krok 1: Załaduj plik PSD
Ładujemy źródłowy plik PSD i włączamy zasoby efektów, aby efekt obrysu był dostępny.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Krok 2: Uzyskaj dostęp do efektu obrysu
Zakładając, że obrys, który chcemy zmodyfikować, należy do trzeciej warstwy (indeks 2), pobieramy jego `StrokeEffect`.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Krok 3: Zweryfikuj właściwości efektu obrysu
Przed wprowadzeniem zmian potwierdzamy istniejące ustawienia, aby dokładnie wiedzieć, co aktualizujemy.

```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```

## Krok 4: Zmodyfikuj ustawienia wypełnienia gradientowego
Tutaj zmieniamy kolor, krycie, tryb mieszania i inne właściwości, aby uzyskać pożądany wygląd.

```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```

## Krok 5: Dodaj i zmodyfikuj punkty koloru i przejrzystości
Dodajemy nowe punkty koloru i przejrzystości, a następnie dostosowujemy istniejące, aby ukształtować gradient.

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## Krok 6: Zapisz zmodyfikowany plik PSD
Po wszystkich korektach zapisujemy zaktualizowany plik na dysku.

```java
im.save(exportPath);
```

## Krok 7: Zweryfikuj modyfikacje
Ładujemy zapisany plik i sprawdzamy, czy każda właściwość odzwierciedla wprowadzone zmiany.

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## Podsumowanie
Teraz wiesz, jak **create gradient stroke layer** w plikach PSD przy użyciu Aspose.PSD for Java. Ładując PSD, uzyskując dostęp do efektu obrysu, dostosowując ustawienia wypełnienia gradientowego i zapisując wynik, możesz programowo tworzyć grafiki o profesjonalnym wyglądzie bez konieczności otwierania Photoshopa.

## FAQ
### Czym jest Aspose.PSD for Java?
Aspose.PSD for Java to biblioteka, która umożliwia programistom pracę z plikami PSD w aplikacjach Java, oferując funkcje tworzenia, manipulacji i konwersji plików PSD.

### Czy potrzebuję licencji, aby używać Aspose.PSD for Java?
Tak, potrzebna jest ważna licencja do używania Aspose.PSD for Java. Możesz uzyskać [tymczasową licencję](https://purchase.aspose.com/temporary-license/) do celów ewaluacyjnych.

### Czy mogę używać Aspose.PSD for Java do tworzenia plików PSD od podstaw?
Oczywiście! Aspose.PSD for Java zapewnia kompleksowe API do programowego tworzenia i manipulacji plikami PSD.

### Czy można zastosować inne efekty przy użyciu Aspose.PSD for Java?
Tak, możesz zastosować różne efekty, takie jak cień, poświata i wiele innych, korzystając z Aspose.PSD for Java.

### Gdzie mogę znaleźć dokumentację Aspose.PSD for Java?
Dokumentację znajdziesz [tutaj](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-01-14  
**Testowano z:** Aspose.PSD for Java 24.11  
**Autor:** Aspose
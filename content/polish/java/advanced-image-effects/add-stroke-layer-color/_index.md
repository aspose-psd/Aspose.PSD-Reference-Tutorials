---
title: Dodaj kolor warstwy obrysu w Aspose.PSD dla Java
linktitle: Dodaj kolor warstwy obrysu
second_title: Aspose.PSD API Java
description: Odkryj moc Aspose.PSD dla Java, korzystając z naszego przewodnika krok po kroku na temat dodawania koloru warstwy obrysu. Podnieś poziom swoich projektów graficznych bez wysiłku.
type: docs
weight: 14
url: /pl/java/advanced-image-effects/add-stroke-layer-color/
---
## Wstęp

Odblokuj potencjał projektu graficznego swojej aplikacji Java za pomocą Aspose.PSD. W tym samouczku zagłębimy się w fascynujący świat dodawania koloru warstwy obrysu za pomocą Aspose.PSD dla Java. Ulepsz swoją grafikę za pomocą efektownych pociągnięć, tworząc atrakcyjne wizualnie projekty bez wysiłku.

## Warunki wstępne

Przed wyruszeniem w tę twórczą podróż upewnij się, że spełniasz następujące warunki wstępne:

-  Biblioteka Aspose.PSD: Pobierz i skonfiguruj bibliotekę Aspose.PSD, postępując zgodnie z instrukcją[dokumentacja](https://reference.aspose.com/psd/java/).

- Zestaw Java Development Kit (JDK): Upewnij się, że w systemie jest zainstalowana Java.

- Zintegrowane środowisko programistyczne (IDE): Wybierz preferowane IDE; Popularnymi opcjami są Eclipse lub IntelliJ.

## Importuj pakiety

Zacznijmy od zaimportowania niezbędnych pakietów, aby zadziałała magia Aspose.PSD.

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

## Krok 1: Skonfiguruj swój projekt

Rozpocznij od utworzenia nowego projektu Java w preferowanym środowisku IDE. Upewnij się, że biblioteka Aspose.PSD została dodana do Twojego projektu.

## Krok 2: Załaduj plik PSD

Załaduj plik PSD za pomocą Aspose.PSD, umożliwiając ładowanie zasobów efektów.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Krok 3: Uzyskaj dostęp do warstwy obrysów

Uzyskaj dostęp do warstwy efektu obrysu w pliku PSD.

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Krok 4: Sprawdź właściwości obrysu

Upewnij się, że właściwości obrysu są zgodne z oczekiwaniami.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Krok 5: Ustaw kolor i krycie

Zmodyfikuj kolor i krycie warstwy obrysu.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Krok 6: Zapisz zmodyfikowany plik PSD

Zapisz zmodyfikowany plik PSD z nowo dodanym kolorem warstwy obrysu.

```java
im.save(exportPath);
```

## Wniosek

Gratulacje! Pomyślnie dodałeś kolor warstwy obrysu do swojego pliku PSD przy użyciu Aspose.PSD dla Java. Eksperymentuj z różnymi kolorami i ustawieniami, aby ożywić swoje projekty graficzne.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.PSD z innymi bibliotekami graficznymi Java?

O1: Tak, Aspose.PSD można zintegrować z innymi bibliotekami graficznymi Java w celu zwiększenia funkcjonalności.

### P2: Czy Aspose.PSD jest kompatybilny z najnowszym formatem pliku PSD?

A2: Absolutnie! Aspose.PSD dotrzymuje kroku najnowszym specyfikacjom formatu plików PSD, zapewniając kompatybilność.

### P3: Jak obsługiwać wyjątki podczas korzystania z Aspose.PSD?

 A3: Patrz[forum wsparcia](https://forum.aspose.com/c/psd/34) w celu uzyskania pomocy w obsłudze wyjątków i rozwiązywaniu problemów.

### P4: Czy mogę wypróbować Aspose.PSD przed zakupem?

 A4: Oczywiście! Chwyć a[bezpłatna wersja próbna](https://releases.aspose.com/) aby poznać funkcje Aspose.PSD przed podjęciem zobowiązania.

### P5: Gdzie mogę uzyskać tymczasową licencję na Aspose.PSD?

 A5: Uzyskaj[licencja tymczasowa](https://purchase.aspose.com/temporary-license/) dla Aspose.PSD w celu oceny jego możliwości w Twoich projektach.
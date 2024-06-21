---
title: Dodaj efekty wzorców w Aspose.PSD dla Java
linktitle: Dodaj efekty wzoru
second_title: Aspose.PSD API Java
description: Ulepsz swoje wzorce obrazów Java bez wysiłku dzięki Aspose.PSD dla Java. Postępuj zgodnie z naszym samouczkiem krok po kroku, aby dodać urzekające efekty wzorów.
type: docs
weight: 12
url: /pl/java/advanced-image-effects/add-pattern-effects/
---
## Wstęp

W świecie programowania w języku Java ulepszanie wzorców obrazów jest częstym zadaniem, a Aspose.PSD dla Java zapewnia solidne rozwiązanie tego problemu. Ten samouczek poprowadzi Cię przez proces dodawania efektów wzorów przy użyciu Aspose.PSD, upewniając się, że Twoje obrazy wyróżniają się dzięki unikalnym nakładkom i ulepszeniom.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Zestaw Java Development Kit (JDK) zainstalowany w systemie.
-  Biblioteka Aspose.PSD for Java pobrana i dodana do Twojego projektu. Można go pobrać z[Witryna Aspose.PSD](https://releases.aspose.com/psd/java/).

## Importuj pakiety

W swoim projekcie Java zaimportuj pakiety niezbędne do pracy z Aspose.PSD. Dołącz następujący kod na początku klasy Java:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## Krok 1: Załaduj obraz

```java
// Załaduj obraz PSD
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

Pamiętaj, aby zastąpić „YourImagePath” i „YourExportPath” rzeczywistymi ścieżkami w projekcie.

## Krok 2: Wyodrębnij informacje o nakładce wzorca

```java
// Wyodrębnij informacje o nakładce wzoru
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Krok 3: Zmodyfikuj ustawienia nakładki wzoru

```java
// Zmodyfikuj ustawienia nakładki wzoru
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## Krok 4: Edytuj dane wzoru

```java
// Edytuj dane wzoru
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## Krok 5: Zapisz edytowany obraz

```java
// Zapisz edytowany obraz
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Krok 6: Sprawdź zmiany

```java
// Sprawdź zmiany w edytowanym pliku
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// Dodaj potwierdzenia, aby upewnić się, że zmiany zostały pomyślnie zastosowane
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się dodawać efekty wzorców przy użyciu Aspose.PSD dla Java. Ta potężna biblioteka umożliwia tworzenie atrakcyjnych wizualnie obrazów z niestandardowymi wzorami, zapewniając nieograniczone możliwości dla projektów opartych na Javie.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.PSD for Java z innymi bibliotekami do przetwarzania obrazów Java?

O1: Aspose.PSD dla Java został zaprojektowany do pracy niezależnej, ale w razie potrzeby można go zintegrować z innymi bibliotekami Java.

### P2: Gdzie mogę znaleźć szczegółową dokumentację Aspose.PSD dla Java?

 Odpowiedź 2: Patrz[Aspose.PSD dla dokumentacji Java](https://reference.aspose.com/psd/java/) w celu uzyskania wyczerpujących informacji.

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla Java?

 Odpowiedź 3: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego.[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać wsparcie dla Aspose.PSD dla Java?

 A4: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) o wsparcie społeczne lub rozważ zakup planu wsparcia.

### P5: Czy mogę uzyskać tymczasową licencję na Aspose.PSD dla Java?

Odpowiedź 5: Tak, możesz uzyskać licencję tymczasową.[Tutaj](https://purchase.aspose.com/temporary-license/).
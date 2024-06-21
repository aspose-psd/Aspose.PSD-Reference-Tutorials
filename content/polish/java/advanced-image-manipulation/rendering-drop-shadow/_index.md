---
title: Zastosuj renderowanie cienia w Aspose.PSD dla Java
linktitle: Zastosuj cień renderowania
second_title: Aspose.PSD API Java
description: Zapoznaj się z przewodnikiem krok po kroku dotyczącym stosowania cieni renderujących w Aspose.PSD dla Java, bez wysiłku poprawiając umiejętności przetwarzania obrazu.
type: docs
weight: 16
url: /pl/java/advanced-image-manipulation/rendering-drop-shadow/
---
## Wstęp

Jeśli zaczynasz przygodę z przetwarzaniem obrazów w Javie, Aspose.PSD to idealne narzędzie do płynnej i wydajnej manipulacji plikami PSD. W tym samouczku omówimy proces stosowania cienia renderującego przy użyciu Aspose.PSD dla Java. Zapnij pasy, my rozkładamy dla Ciebie stopnie.

## Warunki wstępne

Zanim wyruszymy w tę podróż, upewnijmy się, że spełniliśmy następujące wymagania wstępne:

- Środowisko programistyczne Java: Upewnij się, że na komputerze jest zainstalowana Java.
- Biblioteka Aspose.PSD: Pobierz i skonfiguruj bibliotekę Aspose.PSD. Możesz znaleźć drogę do biblioteki[Tutaj](https://releases.aspose.com/psd/java/).
- Plik PSD: Przygotuj plik PSD zawierający warstwę, na którą chcesz zastosować cień.

## Importuj pakiety

Zacznijmy od zaimportowania niezbędnych pakietów. Ten krok zapewnia, że masz do dyspozycji niezbędne narzędzia do płynnego wykonania kodu.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

Teraz rozłóżmy każdy krok.

## Krok 1: Zdefiniuj katalog dokumentów

Rozpocznij od określenia katalogu, w którym znajduje się plik PSD.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Ustaw ścieżki plików PSD i PNG

Zdefiniuj ścieżki źródłowego pliku PSD i docelowego pliku PNG.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

## Krok 3: Załaduj plik PSD z efektami

Załaduj plik PSD, umożliwiając załadowanie zasobów efektów.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Krok 4: Uzyskaj dostęp do efektu cienia

Pobierz efekt cienia z określonej warstwy.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Krok 5: Sprawdź właściwości efektu cienia

Upewnij się, że właściwości efektu cienia spełniają Twoje oczekiwania.

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

## Krok 6: Zapisz jako PNG

Zapisz zmodyfikowany obraz jako plik PNG.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

I gotowe — przewodnik krok po kroku dotyczący stosowania renderowanych cieni w Aspose.PSD dla Java.

## Wniosek

Opanowanie manipulacji obrazami w Javie staje się proste dzięki Aspose.PSD. Właśnie odkryłeś sekrety renderowania cieni, otwierając świat kreatywnych możliwości.

## Często zadawane pytania

### P1: Czy mogę zastosować cienie na wielu warstwach jednocześnie?

Odpowiedź 1: Tak, możesz przeglądać warstwy i w razie potrzeby zastosować cienie.

### P2: Jakie jest znaczenie parametru „Rozprzestrzenianie” w cieniach?

A2: Parametr „Rozprzestrzenianie” kontroluje przejście pomiędzy obszarami cienia i obszarów niezacienionych.

### P3: Czy Aspose.PSD jest kompatybilny ze wszystkimi wersjami plików Photoshopa?

O3: Aspose.PSD zapewnia kompatybilność z szeroką gamą wersji plików PSD, zapewniając wszechstronność.

### P4: Jak mogę zgłosić problemy lub poprosić o pomoc w Aspose.PSD?

 A4: Udaj się do[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za kompleksowe wsparcie.

### P5: Czy mogę przetestować Aspose.PSD przed dokonaniem zakupu?

 Odpowiedź 5: Oczywiście, użyj[bezpłatna wersja próbna](https://releases.aspose.com/) aby poznać możliwości przed podjęciem decyzji o zakupie.
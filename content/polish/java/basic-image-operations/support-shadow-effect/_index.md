---
title: Obsługa efektu cienia w Aspose.PSD dla Java
linktitle: Wsparcie efektu cienia
second_title: Aspose.PSD API Java
description: Dowiedz się, jak dodawać urzekające efekty cieni do obrazów przy użyciu Aspose.PSD dla Java. Ulepsz swój projekt graficzny dzięki temu samouczkowi krok po kroku.
type: docs
weight: 13
url: /pl/java/basic-image-operations/support-shadow-effect/
---
## Wstęp

Uwydatnianie obrazów efektami cienia jest powszechną praktyką w projektowaniu graficznym, dodającą głębi i realizmu. Aspose.PSD dla Java zapewnia solidną obsługę efektów cienia, umożliwiając programistom bezproblemową integrację tych efektów z aplikacjami Java. W tym samouczku odkryjemy krok po kroku, jak wspierać efekty cieni przy użyciu Aspose.PSD.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Podstawowa znajomość programowania w języku Java.
-  Zainstalowano Aspose.PSD dla Java. Możesz go pobrać[Tutaj](https://releases.aspose.com/psd/java/).

## Importuj pakiety

Upewnij się, że zaimportowałeś niezbędne pakiety, aby wykorzystać funkcje Aspose.PSD w swojej aplikacji Java. Użyj poniższego fragmentu kodu jako przewodnika:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Krok 1: Załaduj obraz PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Krok 2: Odzyskaj efekt cienia

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Krok 3: Sprawdź ustawienia domyślne

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

## Krok 4: Dostosuj efekt cienia

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## Krok 5: Zapisz zmodyfikowany obraz

```java
im.save(psdPathAfterChange);
```

## Wniosek

Dzięki tym prostym krokom możesz bez wysiłku obsługiwać efekty cieni w Aspose.PSD dla Java, poprawiając atrakcyjność wizualną swoich obrazów.

## Często zadawane pytania

### P1: Czy Aspose.PSD dla Java nadaje się do profesjonalnych projektów graficznych?

A1: Absolutnie! Aspose.PSD dla Java to potężna biblioteka przeznaczona do profesjonalnych zadań związanych z projektowaniem graficznym.

### P2: Czy mogę używać Aspose.PSD dla Java w aplikacjach komercyjnych?

 O2: Tak, Aspose.PSD dla Java jest produktem komercyjnym. Możesz go kupić[Tutaj](https://purchase.aspose.com/buy).

### P3: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 3: Tak, możesz skorzystać z bezpłatnej wersji próbnej.[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę znaleźć szczegółową dokumentację?

 A4: Zapoznaj się z obszerną dokumentacją[Tutaj](https://reference.aspose.com/psd/java/).

### P5: Jak mogę uzyskać wsparcie dla Aspose.PSD dla Java?

 Odpowiedź 5: Dołącz do forum społeczności.[Tutaj](https://forum.aspose.com/c/psd/34) w przypadku jakichkolwiek pytań dotyczących wsparcia.
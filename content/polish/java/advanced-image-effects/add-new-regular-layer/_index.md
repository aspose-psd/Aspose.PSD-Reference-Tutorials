---
title: Dodaj nową zwykłą warstwę do PSD za pomocą Aspose.PSD dla Java
linktitle: Dodaj nową zwykłą warstwę do PSD
second_title: Aspose.PSD API Java
description: Dowiedz się, jak dodać nową zwykłą warstwę do plików PSD przy użyciu Aspose.PSD dla Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby bezproblemowo manipulować plikami PSD.
type: docs
weight: 11
url: /pl/java/advanced-image-effects/add-new-regular-layer/
---
## Wstęp

Witamy w tym kompleksowym samouczku dotyczącym używania Aspose.PSD dla Java w celu dodania nowej zwykłej warstwy do pliku PSD. Aspose.PSD to potężna biblioteka Java, która pozwala programistom efektywnie manipulować plikami PSD i pracować z nimi. W tym samouczku przeprowadzimy Cię przez proces dodawania nowej zwykłej warstwy do pliku PSD, podając szczegółowe kroki i przykłady kodu.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Środowisko programistyczne Java: Upewnij się, że w systemie skonfigurowano środowisko programistyczne Java.
-  Biblioteka Aspose.PSD: Pobierz i zainstaluj bibliotekę Aspose.PSD dla Java. Możesz znaleźć drogę do biblioteki[Tutaj](https://releases.aspose.com/psd/java/).

## Importuj pakiety

Aby rozpocząć, zaimportuj niezbędne pakiety do swojego projektu Java. Pakiety te są niezbędne do pracy z funkcjonalnościami Aspose.PSD. Umieść następujące wiersze na początku pliku Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Krok 1: Załaduj plik PSD

Załaduj plik PSD, który chcesz edytować, używając następującego kodu:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Krok 2: Przygotuj tablice danych i prostokąty

Przygotuj dwie tablice int i dwa obiekty Rectangle w następujący sposób:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Krok 3: Zainicjuj dane warstwy

Zainicjuj tablice danych wartością domyślną:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Krok 4: Dodaj regularne warstwy

Dodaj dwie zwykłe warstwy do obrazu PSD:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Krok 5: Zapisz PSD i PNG

Zapisz zmodyfikowany plik PSD i dodatkowy plik PNG:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Gratulacje! Pomyślnie dodałeś nową zwykłą warstwę do pliku PSD przy użyciu Aspose.PSD dla Java.

## Wniosek

W tym samouczku omówiliśmy proces dodawania nowej zwykłej warstwy do pliku PSD przy użyciu Aspose.PSD dla Java. Ta potężna biblioteka upraszcza manipulację plikami PSD, udostępniając ją programistom Java. Eksperymentuj z różnymi parametrami i funkcjonalnościami, aby odkryć pełny potencjał Aspose.PSD.

## Często zadawane pytania

### P1: Czy Aspose.PSD jest kompatybilny z Java 8?

O1: Tak, Aspose.PSD obsługuje Java 8 i nowsze wersje.

### P2: Czy mogę zastosować transformacje do dodanych warstw?

A2: Absolutnie! Aspose.PSD zapewnia szereg opcji transformacji warstw.

### P3: Gdzie mogę znaleźć dodatkową dokumentację Aspose.PSD?

 Odpowiedź 3: Możesz zapoznać się z dokumentacją.[Tutaj](https://reference.aspose.com/psd/java/).

### P4: Jak mogę uzyskać tymczasową licencję na Aspose.PSD?

 A4: Odwiedź[ten link](https://purchase.aspose.com/temporary-license/) dla opcji licencji tymczasowej.

### P5: Czy istnieją fora społeczności dotyczące wsparcia Aspose.PSD?

 Odpowiedź 5: Tak, możesz znaleźć wsparcie i dyskusje.[Tutaj](https://forum.aspose.com/c/psd/34).
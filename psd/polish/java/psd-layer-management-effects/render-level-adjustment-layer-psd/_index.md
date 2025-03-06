---
title: Warstwa dopasowania poziomu renderowania w plikach PSD — Java
linktitle: Warstwa dopasowania poziomu renderowania w plikach PSD — Java
second_title: Aspose.PSD API Java
description: Dowiedz się, jak bez wysiłku poprawić kontrast i intensywność obrazu za pomocą Aspose.PSD dla Java. Opanuj warstwy dopasowywania poziomów dzięki temu przewodnikowi krok po kroku.
weight: 17
url: /pl/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Warstwa dopasowania poziomu renderowania w plikach PSD — Java

## Wstęp

Czy kiedykolwiek otworzyłeś plik PSD i stwierdziłeś, że obrazowi brakuje kontrastu lub żywości? Nie bójcie się, wojownicy edycji obrazów! Aspose.PSD dla Java przychodzi na ratunek dzięki potężnym możliwościom manipulacji warstwami dopasowywania poziomów. Ten przewodnik wyposaży Cię w wiedzę niezbędną do doprecyzowania obrazów za pomocą Poziomów w mgnieniu oka. 

## Warunki wstępne

- Zestaw Java Development Kit (JDK): Upewnij się, że masz zainstalowaną najnowszą wersję pakietu JDK w swoim systemie. Można go pobrać ze strony internetowej Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD for Java Library: Pobierz bibliotekę Aspose.PSD for Java ze strony pobierania ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Aby korzystać z pełnych funkcji, potrzebujesz ważnej licencji, ale na początek dostępna jest bezpłatna wersja próbna ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Importuj pakiety

Zanim zagłębimy się w kod, musimy zaimportować niezbędne klasy Aspose.PSD, aby móc współdziałać z plikami PSD. Oto, czego będziesz potrzebować:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 The`com.aspose.psd` pakiet zapewnia dostęp do funkcjonalności manipulacji PSD, natomiast`com.aspose.psd.imaging.PngOptions` pozwala nam zdefiniować opcje podczas zapisywania obrazu jako PNG.

A teraz rozpocznijmy naszą przygodę z dostosowywaniem poziomów:

## Krok 1: Konfigurowanie ścieżek plików:

- Zdefiniuj zmienne dla katalogu dokumentów (`dataDir`), nazwa źródłowego pliku PSD (`sourceFileName`), docelowa nazwa pliku PSD po modyfikacji (`psdPathAfterChange`) i końcową ścieżkę eksportu PNG (`pngExportPath`). Rozważ użycie nazw opisowych, aby poprawić czytelność kodu.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Krok 2: Ładowanie obrazu PSD:

-  Skorzystaj z`Image.load` metoda otwierania źródłowego pliku PSD i przechowywania go w formacie`PsdImage`obiekt (`im`). Aspose.PSD automatycznie wykrywa format pliku.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Krok 3: Iteracja po warstwach:

- Musimy znaleźć warstwę regulacji poziomów w twoim PSD. Aspose zapewnia wygodny sposób iteracji po wszystkich warstwach za pomocą pętli.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (tu zostanie dodany kod sprawdzający warstwę poziomów)
}
```

## Krok 4: Identyfikacja warstwy poziomów:

- Wewnątrz pętli sprawdź, czy bieżąca warstwa (`im.getLayers()[i]` ) jest przykładem`LevelsLayer` klasa za pomocą`instanceof` operator. 
-  Jeśli tak, rzuć warstwę na a`LevelsLayer` obiekt do dalszej manipulacji.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (kod do dostosowania poziomów zostanie dodany tutaj)
   }
}
```
## Krok 5: Poziomy dostrajania (ciąg dalszy):

-  Dostosuj poziomy wyjściowe za pomocą`setOutputShadowLevel` I`setOutputHighlightLevel` kontrolować ciemność i jasność powstałego obrazu. Wartości te określają zakres poziomów wejściowych, które zostaną odwzorowane na zakres wyjściowy.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Dostosuj poziomy wejściowe (0-255):
	   channel.setInputShadowLevel((short) 10); // Przyciemnij lekko cienie
	   channel.setInputMidtoneLevel(2.0f);     // Zwiększ półcienie
	   channel.setInputHighlightLevel((short) 230); // Zmniejsz rozjaśnienia

	   // Dostosuj poziomy wyjściowe (0-255):
	   channel.setOutputShadowLevel((short) 20); // Przyciemnij cienie jeszcze bardziej
	   channel.setOutputHighlightLevel((short) 200); //Rozjaśnij pasemka
   }
}
```

## Krok 6: Zapisywanie zmodyfikowanego pliku PSD:

-  Skorzystaj z`save` metoda`PsdImage` obiekt, aby zapisać zmodyfikowany obraz w określonej ścieżce (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Krok 7: Eksportowanie jako PNG (opcjonalnie):

-  Jeśli potrzebujesz dostosowanego obrazu w formacie PNG, utwórz plik`PngOptions` obiekt i ustaw typ koloru na`TruecolorWithAlpha` . Następnie skorzystaj z`save` ponownie, podając ścieżkę eksportu PNG i opcje.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

I masz to! Pomyślnie dostosowałeś warstwę dopasowania poziomów w pliku PSD przy użyciu Aspose.PSD dla Java. Rozumiejąc te kroki i eksperymentując z różnymi wartościami, możesz poprawić kontrast i ogólny wygląd swoich obrazów.

## Wniosek

Aspose.PSD dla Java umożliwia przejęcie kontroli nad procesem edycji obrazu. Opanowując warstwę dopasowania poziomów, możesz tchnąć nowe życie w swoje zdjęcia i projekty. Pamiętaj, praktyka czyni mistrza, więc nie wahaj się eksperymentować i odkrywać pełny potencjał tego potężnego narzędzia.
 
## Często zadawane pytania

### Czy mogę oddzielnie regulować poszczególne kanały kolorów (RGB)? 
Tak, dostęp do każdego kanału koloru można uzyskać za pomocą przycisku`getChannel` metoda`LevelsLayer` obiektu i niezależnie modyfikować jego poziomy.

### Jak obsługiwać wiele warstw dopasowania poziomów w pliku PSD?
Kod iteruje po wszystkich warstwach, więc automatycznie przetworzy wszelkie dodatkowe warstwy Levels znalezione na obrazie.

### Czy istnieją inne sposoby regulacji kontrastu obrazu oprócz poziomów?
Absolutnie! Aspose.PSD oferuje różne narzędzia do regulacji obrazu, takie jak Krzywe, Jasność/Kontrast i inne.

### Czy mogę zautomatyzować ten proces dla wielu obrazów? 
Tak, możesz włączyć ten kod do skryptu przetwarzania w pętli lub wsadowego, aby efektywnie przetwarzać wiele plików PSD.

### Gdzie mogę znaleźć więcej informacji i wsparcia?
Aspose zapewnia obszerną dokumentację ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) i forum wsparcia ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) w przypadku jakichkolwiek pytań lub problemów, które możesz napotkać.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

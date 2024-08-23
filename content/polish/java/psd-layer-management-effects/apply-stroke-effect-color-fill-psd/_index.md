---
title: Zastosuj efekt obrysu z wypełnieniem kolorem w PSD - Java
linktitle: Zastosuj efekt obrysu z wypełnieniem kolorem w PSD - Java
second_title: Aspose.PSD API Java
description: Dowiedz się, jak zastosować efekt obrysu z wypełnieniem kolorem do plików PSD za pomocą Aspose.PSD dla Java. Postępuj zgodnie z tym przewodnikiem krok po kroku, aby z łatwością ulepszać swoje obrazy.
type: docs
weight: 21
url: /pl/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---
## Wstęp

tym przewodniku przeprowadzimy Cię przez proces stosowania efektu obrysu z wypełnieniem kolorem do plików PSD przy użyciu Aspose.PSD dla Java. Niezależnie od tego, czy jesteś doświadczonym programistą, czy dopiero zaczynasz, ten samouczek krok po kroku ułatwi Ci wykonanie pracy. Omówimy wszystko, od skonfigurowania środowiska po zapisanie końcowego obrazu z zastosowanymi efektami.

## Warunki wstępne

Zanim zaczniemy, upewnijmy się, że masz wszystko, czego potrzebujesz, wraz z tym samouczkiem:

1. Zainstalowany zestaw Java Development Kit (JDK): Upewnij się, że w systemie jest zainstalowany pakiet JDK 8 lub nowszy.
2.  Biblioteka Aspose.PSD dla Java: Będziesz potrzebować biblioteki Aspose.PSD dla Java. Można go pobrać z[strona internetowa](https://releases.aspose.com/psd/java/).
3. Zintegrowane środowisko programistyczne (IDE): IDE, takie jak IntelliJ IDEA, Eclipse lub dowolne inne według własnego wyboru.
4. Przykładowy plik PSD: Przykładowy plik PSD, do którego można zastosować efekt obrysu. Jeśli go nie masz, możesz utworzyć prosty plik PSD w Photoshopie lub pobrać go z Internetu.
5. Podstawowa znajomość języka Java: Chociaż ten samouczek jest przyjazny dla początkujących, przydatna będzie podstawowa znajomość języka Java.

Po spełnieniu tych wymagań wstępnych można przystąpić do stosowania efektu obrysu z wypełnieniem kolorem w plikach PSD.

## Importuj pakiety

Aby rozpocząć pracę z Aspose.PSD dla Java, musisz zaimportować niezbędne pakiety do swojego projektu Java. Oto jak możesz to zrobić:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Importy te obejmują wszystkie niezbędne klasy potrzebne do pracy z plikami PSD, stosowania efektów i zapisywania obrazów w żądanym formacie.

## Krok 1: Załaduj plik PSD

 Pierwszym krokiem naszego procesu jest załadowanie pliku PSD, który chcesz zmodyfikować. Aspose.PSD dla Java sprawia, że jest to niezwykle proste dzięki swoim`PsdImage` klasa. Oto jak możesz to zrobić:

### 1.1 Ustaw ścieżkę katalogu

Najpierw zdefiniuj ścieżkę katalogu, w którym przechowywane są pliki PSD:

```java
String dataDir = "Your Document Directory";
```

 Zastępować`"Your Document Directory"` z rzeczywistą ścieżką, w której znajduje się plik PSD.

### 1.2 Załaduj obraz PSD

 Teraz załaduj plik PSD za pomocą`PsdLoadOptions` I`PsdImage` zajęcia:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

 Tutaj,`PsdLoadOptions`jest skonfigurowany tak, aby ładować zasoby efektów, zapewniając dostępność wszelkich istniejących efektów w PSD.

## Krok 2: Zastosuj efekt obrysu za pomocą wypełnienia kolorem

Następnym krokiem po załadowaniu pliku PSD jest zastosowanie efektu obrysu na warstwach obrazu. To tutaj dzieje się prawdziwa magia.

Każdy plik PSD może zawierać wiele warstw i do każdej z nich konieczne będzie zastosowanie efektu. Oto jak to zrobić:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

W tej pętli:

- `im.getLayers()`: pobiera wszystkie warstwy z pliku PSD.
- `StrokeEffect effect`: wyodrębnia efekt obrysu zastosowany do warstwy.
- `ColorFillSettings settings`: modyfikuje ustawienia wypełnienia efektu obrysu.
- `settings.setColor(Color.getDeepPink())`: Ustawia kolor obrysu na głęboki róż. Możesz to zmienić na dowolny preferowany kolor.

## Krok 3: Zapisz zmodyfikowany plik PSD i eksportuj jako PNG

Po zastosowaniu efektu obrysu czas zapisać zmiany i wyeksportować obraz.

### 3.1 Zapisz plik PSD

Aby zapisać zmodyfikowany plik PSD, użyj następującego kodu:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

Spowoduje to zapisanie pliku z zastosowanym efektem obrysu w określonej ścieżce.

### 3.2 Eksportuj jako PNG

Aby obraz był bardziej dostępny, możesz wyeksportować go jako plik PNG. Oto jak:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

Ten fragment kodu zapisuje obraz jako plik PNG z prawdziwymi kolorami i przezroczystością alfa, dzięki czemu jest gotowy do użycia w aplikacjach internetowych i innych platformach.

## Wniosek

Stosowanie efektu obrysu z wypełnieniem kolorem do plików PSD za pomocą Aspose.PSD dla Java jest nie tylko proste, ale także niezwykle wydajne. Za pomocą zaledwie kilku linii kodu możesz zautomatyzować złożone zadania przetwarzania obrazu, oszczędzając czas i wysiłek.

Niezależnie od tego, czy pracujesz nad dużą partią obrazów, czy po prostu chcesz zmodyfikować kilka plików, ta metoda zapewnia elastyczne i wydajne rozwiązanie. Teraz, gdy znasz już podstawy, możesz zacząć eksperymentować z różnymi efektami i dostosowaniami, aby Twoje obrazy naprawdę się wyróżniały.

Gotowy, aby to wypróbować? Pobierz swój przykładowy plik PSD i zacznij dodawać te wspaniałe efekty już dziś!

## Często zadawane pytania

### Czy mogę zastosować wiele efektów do pojedynczej warstwy przy użyciu Aspose.PSD dla Java?
Tak, możesz zastosować wiele efektów do pojedynczej warstwy, uzyskując dostęp do opcji mieszania warstwy i dodając żądane efekty.

### Czy można zautomatyzować proces w przypadku partii plików PSD?
Absolutnie! Możesz przeglądać katalog plików PSD, zastosować efekt obrysu i automatycznie zapisać wyniki.

### Jak mogę cofnąć zmiany wprowadzone w pliku PSD przy użyciu Aspose.PSD dla Java?
Aby cofnąć zmiany, przed zapisaniem jakichkolwiek modyfikacji należy ponownie załadować oryginalny plik PSD. W Aspose.PSD nie ma funkcji bezpośredniego cofania.

### Czy mogę dostosować szerokość i położenie obrysu?
 Tak, Aspose.PSD dla Java umożliwia dostosowanie szerokości, położenia i innych właściwości obrysu poprzez`StrokeEffect` klasa.

### Czy korzystanie z biblioteki Aspose.PSD for Java jest bezpłatne?
 Aspose.PSD dla Java oferuje bezpłatną wersję próbną, ale aby uzyskać pełny dostęp do wszystkich funkcji, należy zakupić licencję. Możesz zwiedzać[kup opcje](https://purchase.aspose.com/buy)na ich stronie internetowej.
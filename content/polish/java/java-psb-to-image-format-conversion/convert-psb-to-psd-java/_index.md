---
title: Konwertuj PSB na PSD w Javie
linktitle: Konwertuj PSB na PSD w Javie
second_title: Aspose.PSD API Java
description: Dowiedz się, jak bezproblemowo przekonwertować PSB na PSD w Javie za pomocą Aspose.PSD, usprawniając zarządzanie plikami graficznymi w swoich aplikacjach.
type: docs
weight: 12
url: /pl/java/java-psb-to-image-format-conversion/convert-psb-to-psd-java/
---
## Wstęp
W środowisku programowania w języku Java efektywne manipulowanie plikami graficznymi ma kluczowe znaczenie. Ten samouczek koncentruje się na wykorzystaniu Aspose.PSD dla Java do płynnej konwersji plików PSB (Photoshop Big) do formatu PSD (Dokument Photoshop). Wykonując poniższe kroki, możesz bez wysiłku zintegrować tę funkcję z aplikacjami Java.
## Warunki wstępne
Zanim przystąpisz do procesu konwersji, upewnij się, że masz skonfigurowane następujące wymagania wstępne:
- Zestaw Java Development Kit (JDK): Upewnij się, że w systemie jest zainstalowany pakiet JDK 8 lub nowszy.
-  Biblioteka Aspose.PSD dla Java: Pobierz i skonfiguruj bibliotekę Aspose.PSD dla Java. Można go uzyskać od[Tutaj](https://releases.aspose.com/psd/java/).
- Zintegrowane środowisko programistyczne (IDE): Użyj IntelliJ IDEA, Eclipse lub innego wybranego środowiska Java IDE.
- Podstawowa znajomość języka Java: Zrozumienie podstaw programowania w języku Java będzie korzystne.
## Importuj pakiety
Najpierw zaimportuj niezbędne klasy Aspose.PSD do pliku Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.FileFormatVersion;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
## Krok 1: Zainicjuj zmienne i załaduj plik PSB
Zacznij od zdefiniowania zmiennych i załadowania pliku PSB:
```java
String dataDir = "Your_Document_Directory/";
String sourceFileName = dataDir + "2layers.psb";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```
 Pamiętaj o wymianie`"Your_Document_Directory/"` ze ścieżką do aktualnego katalogu dokumentów zawierającego plik PSB.
## Krok 2: Skonfiguruj opcje konwersji PSD
Następnie skonfiguruj opcje konwersji PSD:
```java
PsdOptions options = new PsdOptions();
options.setFileFormatVersion(FileFormatVersion.Psd);
```
 Tutaj,`FileFormatVersion.Psd` gwarantuje, że plik wyjściowy będzie w formacie PSD.
## Krok 3: Zapisz przekonwertowany plik PSD
Zapisz przekonwertowany plik PSD, korzystając z załadowanego obrazu PSB i opcji:
```java
image.save(dataDir + "ConvertFromPsb_out.psd", options);
```
 Zastępować`"ConvertFromPsb_out.psd"` z żądaną nazwą pliku wyjściowego i ścieżką.

## Wniosek
Wykonując poniższe kroki, pomyślnie przekonwertowałeś plik PSB do formatu PSD przy użyciu Aspose.PSD dla Java. Ta funkcja usprawnia działanie aplikacji Java, zapewniając bezproblemową integrację z formatami plików programu Photoshop.
## Często zadawane pytania
### Czy Aspose.PSD dla Java może obsługiwać złożone pliki PSB z wieloma warstwami?
Tak, Aspose.PSD for Java obsługuje pliki PSB z wieloma warstwami, zachowując ich strukturę podczas konwersji.
### Czy Aspose.PSD dla Java nadaje się do przetwarzania wsadowego konwersji PSB na PSD?
Absolutnie możesz efektywnie przetwarzać wsadowo konwersje PSB na PSD za pomocą Aspose.PSD dla Java.
### Czy Aspose.PSD dla Java zachowuje jakość obrazu podczas konwersji?
Tak, biblioteka zapewnia konwersję o wysokiej wierności, zachowując jakość i szczegóły obrazu.
### Czy mogę zintegrować Aspose.PSD for Java z aplikacją internetową?
Tak, Aspose.PSD for Java można bezproblemowo zintegrować z aplikacjami Java zarówno stacjonarnymi, jak i internetowymi.
### Gdzie mogę znaleźć dalsze wsparcie lub pomoc dotyczącą Aspose.PSD dla Java?
 Aby uzyskać dalszą pomoc, odwiedź stronę[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).
---
title: Dodaj warstwę regulacji poziomu w PSD
linktitle: Dodaj warstwę regulacji poziomu w PSD
second_title: Aspose.PSD API Java
description: Dowiedz się, jak skutecznie dodawać warstwę dostosowania poziomu do plików PSD przy użyciu Aspose.PSD dla Java. Podnieś swoje umiejętności edycji obrazu.
type: docs
weight: 16
url: /pl/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## Wstęp
Jeśli chodzi o edycję obrazu, zarządzanie poziomami może znacząco wpłynąć na intensywność i wyrazistość zdjęć. Przydatnym narzędziem w arsenale Photoshopa jest „Warstwa regulacji poziomu”, która umożliwia dostosowanie zakresu tonalnego i balansu kolorów obrazów. W tym przewodniku przeprowadzimy Cię przez proces implementowania warstwy dostosowania poziomu w pliku PSD przy użyciu Aspose.PSD dla Java. Więc chwyć swoje Java IDE.
## Warunki wstępne
Zanim wkroczysz w świat dostosowywania poziomów, musisz skonfigurować kilka rzeczy, aby zapewnić płynną jazdę:
1.  Zestaw Java Development Kit (JDK): Upewnij się, że masz zainstalowany pakiet JDK na swoim komputerze. Jeśli go nie masz, możesz go pobrać z[stronie internetowej Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) lub użyj OpenJDK.
2.  Aspose.PSD dla biblioteki Java: Aby manipulować plikami PSD, musisz pobrać bibliotekę Aspose.PSD. Możesz pobrać najnowszą wersję z tego[link do pobrania](https://releases.aspose.com/psd/java/) i upewnij się, że umieściłeś plik JAR w bibliotece projektu.
3. Podstawowa znajomość języka Java: Pomocna będzie podstawowa znajomość programowania w języku Java, ponieważ w tym samouczku będziemy zagłębiać się w fragmenty kodu.
4. Konfiguracja IDE: Do pisania i uruchamiania kodu możesz używać dowolnego preferowanego środowiska Java IDE — na przykład IntelliJ IDEA, Eclipse lub NetBeans. Upewnij się tylko, że skonfigurowałeś projekt Java i dodałeś bibliotekę Aspose.PSD.

## Importuj pakiety
Zanim zaczniemy pisać nasz kod, musimy zaimportować niezbędne pakiety z biblioteki Aspose.PSD. Oto jak możesz to zrobić:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Importując te pakiety, będziemy mieli dostęp do klas niezbędnych do ładowania, modyfikowania i zapisywania naszych plików PSD.

Podzielmy teraz proces na zrozumiałe etapy. Postępuj zgodnie z instrukcjami ładowania pliku PSD, dostosowywania poziomów i zapisywania zmian. 
## Krok 1: Skonfiguruj ścieżki plików
Pierwszym krokiem jest określenie, gdzie znajduje się nasz plik PSD i gdzie chcemy zapisać zmodyfikowane dane wyjściowe. Możesz dostosować ścieżkę katalogu do swoich potrzeb.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Tutaj, wymień`"Your Document Directory"` rzeczywistą ścieżką w systemie, w którym przechowywany jest plik PSD. To przygotowuje grunt pod wszystko, co będziemy robić dalej.
## Krok 2: Załaduj plik PSD
 Teraz załadujmy plik PSD za pomocą`PsdImage` klasa. Ten krok jest niezbędny, ponieważ pozwala nam uzyskać dostęp do warstw i manipulować nimi.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Kiedy zadzwonisz`Image.load()` , odczyta plik PSD i utworzy instancję`PsdImage` z którym możesz pracować.
## Krok 3: Iteruj po warstwach
Ponieważ chcemy dostosować warstwę dopasowania poziomu, będziemy musieli przejść przez każdą warstwę w naszym pliku PSD. Pomaga nam to znaleźć konkretną warstwę, którą chcemy zmodyfikować.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Dalsza manipulacja będzie tutaj...
    }
}
```
 W tej pętli`instanceof LevelsLayer` sprawdza, czy bieżąca warstwa jest warstwą dopasowania poziomów. Jeśli tak, możemy przystąpić do dostosowywania jego właściwości.
## Krok 4: Dostosuj ustawienia kanału poziomu
Kiedy już zidentyfikujemy właściwą warstwę, możemy zmodyfikować jej poziomy wejściowe i wyjściowe. To tutaj dzieje się magia! Dostosuj różne parametry, aby zobaczyć, jak wpływają one na obraz.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Oto działanie każdego parametru:
- Poziom półtonów wejściowych: reguluje tony średnie.
- Poziom wejściowego cienia: poprawia ciemniejsze obszary obrazu.
- Poziom podświetlenia sygnału wejściowego: Zmienia jasne obszary obrazu.
- Poziom wyjściowego cienia: Ustawia sposób wyświetlania ciemnych cieni.
- Poziom podświetlenia wyjściowego: Ustawia sposób wyświetlania jasnych świateł.
Zachęcamy do eksperymentowania z różnymi wartościami!
## Krok 5: Zapisz zmodyfikowany plik PSD
Teraz, gdy dokonaliśmy już poprawek, czas zapisać zmodyfikowany plik PSD. Ten krok jest kluczowy, aby mieć pewność, że zmiany zostaną zastosowane i zapisane.
```java
im.save(psdPathAfterChange);
```
 Możesz teraz znaleźć dostosowany plik PSD w określonym miejscu`psdPathAfterChange`. 
## Wniosek
Właśnie nauczyłeś się, jak dodać warstwę dopasowania poziomu do pliku PSD przy użyciu Aspose.PSD dla Java! Postępując zgodnie z tym przewodnikiem, możesz bez wysiłku dostosować jakość tonalną obrazów, torując drogę do bardziej żywych i atrakcyjnych wizualnie wydruków. Pamiętaj, że praktyka czyni mistrza, więc możesz dowolnie modyfikować ustawienia i przeglądać różne pliki PSD, aby zobaczyć efekty swoich zmian.
## Często zadawane pytania
### Co to jest warstwa dopasowania poziomu?
Warstwa regulacji poziomu umożliwia korygowanie zakresu tonalnego obrazów, równoważąc cienie, półcienie i światła.
### Czy mogę używać Aspose.PSD bez zakupu?
Tak! Aspose oferuje bezpłatną wersję próbną w celu przetestowania biblioteki przed zakupem.
### Gdzie mogę znaleźć dokumentację dla Aspose.PSD?
 Można znaleźć dokumentację[Tutaj](https://reference.aspose.com/psd/java/).
### Czy istnieje jakieś wsparcie społeczności dla produktów Aspose?
 Absolutnie! Możesz zadawać pytania i uzyskać wsparcie w[forum dyskusyjne](https://forum.aspose.com/c/psd/34).
### Jak mogę uzyskać tymczasową licencję na Aspose.PSD?
 Możesz ubiegać się o licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).
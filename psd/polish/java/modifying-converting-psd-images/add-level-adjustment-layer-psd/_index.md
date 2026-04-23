---
date: 2026-03-07
description: Naucz się regulować poziomy, dodając warstwę korekty poziomów w plikach
  PSD przy użyciu Aspose.PSD dla Javy. Szybko opanuj korekty tonalne.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Jak dostosować poziomy – Dodaj warstwę dopasowania poziomu w PSD
url: /pl/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj warstwę dopasowania poziomów w PSD

## Wprowadzenie
Jeśli chcesz **dowiedzieć się, jak regulować poziomy** w swoich dokumentach Photoshop, warstwa dopasowania poziomów jest idealnym narzędziem. Pozwala ona precyzyjnie dostroić cienie, półtony i podświetlenia bez trwałej zmiany oryginalnych pikseli. W tym samouczku przeprowadzimy Cię przez dodanie warstwy dopasowania poziomów do pliku PSD przy użyciu Aspose.PSD for Java, abyś mógł uzyskać profesjonalną kontrolę tonalną w kilku prostych krokach.

## Szybkie odpowiedzi
- **Co robi warstwa dopasowania poziomów?** Modyfikuje zakres tonalny obrazu w sposób niedestrukcyjny.  
- **Jakiej biblioteki użyto?** Aspose.PSD for Java.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja jest wymagana w produkcji.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego dopasowania.  
- **Czy mogę regulować wiele kanałów?** Tak, możesz ustawić poziomy wejściowe/wyjściowe dla każdego kanału kolorowego osobno.

## Co to jest warstwa dopasowania poziomów?
Warstwa dopasowania poziomów pozwala skorygować balans tonalny obrazu, regulując wejściowe cienie, półtony i podświetlenia oraz poziomy wyjściowe. Ponieważ istnieje jako oddzielna warstwa, możesz przełączać jej widoczność lub usuwać ją bez wpływu na leżącą pod nią grafikę.

## Dlaczego dodać warstwę dopasowania poziomów przy użyciu Aspose.PSD?
- **Automatyzacja:** Zintegruj korekty poziomów w potokach przetwarzania wsadowego.  
- **Wieloplatformowość:** Działa na każdym systemie operacyjnym obsługującym Javę.  
- **Precyzja:** Uzyskaj programowy dostęp do ustawień każdego kanału dla dokładnych rezultatów.  

## Wymagania wstępne
1. Java Development Kit (JDK). Jeśli go nie masz, pobierz go ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) lub użyj OpenJDK.  
2. Biblioteka Aspose.PSD for Java – pobierz najnowszy plik JAR z tego [linku do pobrania](https://releases.aspose.com/psd/java/).  
3. Podstawowa znajomość programowania w Javie.  
4. IDE, takie jak IntelliJ IDEA, Eclipse lub NetBeans, z dodanym do classpath projektu plikiem JAR Aspose.PSD.

## Importowanie pakietów
Zanim zaczniemy pisać kod, musimy zaimportować niezbędne pakiety z biblioteki Aspose.PSD. Oto jak to zrobić:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Te importy dają dostęp do klas służących do ładowania plików PSD, pracy z warstwami dopasowania poziomów oraz manipulacji ustawieniami poszczególnych kanałów.

## Jak dostosować poziomy w pliku PSD
Poniżej znajduje się przewodnik krok po kroku, który pokazuje dokładnie **jak regulować poziomy** programowo.

### Krok 1: Ustaw ścieżki plików
Zdefiniuj, gdzie znajduje się źródłowy plik PSD i gdzie zostanie zapisany zmodyfikowany plik.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Zastąp `"Your Document Directory"` rzeczywistym folderem na swoim komputerze.

### Krok 2: Załaduj plik PSD
Utwórz instancję `PsdImage` z pliku źródłowego.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Teraz masz pełny dostęp do wszystkich warstw wewnątrz pliku PSD.

### Krok 3: Przejdź przez warstwy
Znajdź warstwę dopasowania poziomów, którą chcesz zmodyfikować.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
Sprawdzenie `instanceof LevelsLayer` zapewnia, że pracujemy wyłącznie z warstwami dopasowania poziomów.

### Krok 4: Dostosuj ustawienia kanału poziomu
Dostosuj wartości wejściowe i wyjściowe dla wybranego kanału.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Poziom środkowy (Input Midtone Level):** Przesuwa zakres tonów środkowych.  
- **Poziom cieni (Input Shadow Level):** Przyciemnia lub rozjaśnia cienie.  
- **Poziom podświetleń (Input Highlight Level):** Kontroluje najjaśniejsze partie.  
- **Poziomy wyjściowe cieni/podświetleń:** Definiują ostateczny zakres wyjściowy.

Śmiało eksperymentuj z różnymi wartościami, aby zobaczyć, jak wpływają na obraz.

### Krok 5: Zapisz zmodyfikowany plik PSD
Zachowaj wprowadzone zmiany w nowym pliku.
```java
im.save(psdPathAfterChange);
```
Zaktualizowany plik PSD znajdziesz w lokalizacji określonej w `psdPathAfterChange`.

## Typowe problemy i rozwiązania
- **Plik nie znaleziony:** Sprawdź, czy `dataDir` wskazuje na właściwy folder i czy źródłowy plik PSD istnieje.  
- **ClassCastException:** Upewnij się, że ładowany plik jest rzeczywiście PSD; inne formaty wymagają innych klas.  
- **Błędy licencji:** Użyj ważnej licencji Aspose.PSD w wersjach produkcyjnych; wersja próbna działa w środowisku deweloperskim.

## Zakończenie
Teraz wiesz **jak regulować poziomy** poprzez dodanie i skonfigurowanie warstwy dopasowania poziomów w pliku PSD przy użyciu Aspose.PSD for Java. Ta technika zapewnia precyzyjną kontrolę nad balansem tonalnym, jednocześnie utrzymując pełną automatyzację przepływu pracy. Eksperymentuj z różnymi wartościami kanałów i odkrywaj przetwarzanie wsadowe, aby zastosować te same korekty do wielu obrazów.

## Najczęściej zadawane pytania

**P: Co to jest warstwa dopasowania poziomów?**  
O: To warstwa niedestrukcyjna, która pozwala modyfikować zakres tonalny (cienie, półtony, podświetlenia) obrazu.

**P: Czy mogę używać Aspose.PSD bez zakupu licencji?**  
O: Tak, możesz ocenić bibliotekę w wersji próbnej, ale licencja jest wymagana przy wdrożeniach komercyjnych.

**P: Gdzie mogę znaleźć dokumentację Aspose.PSD?**  
O: Dokumentację znajdziesz [tutaj](https://reference.aspose.com/psd/java/).

**P: Czy istnieje wsparcie społeczności dla produktów Aspose?**  
O: Oczywiście! Możesz zadawać pytania i uzyskać pomoc na [forum Aspose](https://forum.aspose.com/c/psd/34).

**P: Jak mogę uzyskać tymczasową licencję dla Aspose.PSD?**  
O: Tymczasową licencję możesz zamówić [tutaj](https://purchase.aspose.com/temporary-license/).

**Ostatnia aktualizacja:** 2026-03-07  
**Testowano z:** najnowsza wersja Aspose.PSD (Java)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2025-12-17
description: Dowiedz się, jak modyfikować wektorowe kształty PSD, obsługując właściwości
  danych rekordów długości przy użyciu Aspose.PSD dla Javy. Przewodnik krok po kroku
  z przykładami kodu.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Jak modyfikować wektorowe kształty PSD – Obsługa właściwości danych rekordów
  długości w Javie
url: /pl/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obsługa właściwości danych rekordów długości w PSD - Java

## Wprowadzenie
Jeśli potrzebujesz **modyfikować wektory kształtów PSD** programowo, biblioteka Aspose.PSD for Java daje pełną kontrolę nad plikami Photoshop bezpośrednio z kodu Java. W tym samouczku przeprowadzimy Cię przez wszystko, co musisz wiedzieć, aby obsługiwać właściwości danych rekordów długości — kluczowy krok, gdy chcesz edytować warstwy wektorowych kształtów. Po zakończeniu będziesz w stanie otworzyć plik PSD, dostosować jego właściwości wektorowych kształtów i zapisać zaktualizowany plik, nie opuszczając IDE. Zanurzmy się!

## Szybkie odpowiedzi
- **Co oznacza „modify PSD vector shapes”?** Dostosowywanie geometrii, operacji ścieżek lub innych właściwości warstw opartych na wektorach w pliku PSD.  
- **Która biblioteka to obsługuje?** Aspose.PSD for Java.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do oceny; licencja komercyjna jest wymagana w produkcji.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego skryptu modyfikującego kształty.  
- **Jakie są główne wymagania wstępne?** Java , Aspose.PSD for Java oraz przykładowy plik PSD.

## Co to jest „modify PSD vector shapes”?
Modyfikowanie wektorowych kształtów PSD polega na zmianie podstawowych danych ścieżki wektorowej — takich jak rekordy długości i operacje ścieżek — tak aby wygląd wizualny kształtów został odpowiednio zaktualizowany. Jest to szczególnie przydatne w zautomatyzowanych pipeline'ach graficznych, przetwarzaniu wsadowym lub niestandardowych narzędziach projektowych.

## Dlaczego używać Aspose.PSD for Java do modyfikacji wektorowych kształtów PSD?
- **Brak wymogu posiadania Photoshopa** – pracuj bezpośrednio z plikami PSD na dowolnym serwerze.  
- **Bogate API** – dostęp do warstw, zasobów i danych wektorowych przy użyciu silnie typowanych klas.  
- **Wieloplatformowość** – uruchamiaj na Windows, Linux lub macOS z dowolnym JDK.  
- **Skupienie na wydajności** – efektywne zarządzanie pamięcią i szybkie operacje zapisu.

## Wymagania wstępne
1. **Java Development Kit (JDK)** – pobierz ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) lub użyj preferowanego menedżera pakietów.  
2. **Aspose.PSD for Java** – pobierz najnowszy plik JAR ze [strony wydań Aspose](https://releases.aspose.com/psd/java/3. **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor kompatybilny z Javą.  
4. **Plik PSD** – utwórz go w Photoshopie lub pobierz przykładowy plik PSD do eksperymentów.  
5. **Podstawowa znajomość Javy** – znajomość klas, obiektów i obsługi wyjątków.

## Importowanie pakietów
Najpierw zaimportuj klasy, których będziesz potrzebować do pracy z plikami PSD i zasobami wektorowych kształtów.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Krok 1: Skonfiguruj katalogi źródłowy i wyjściowy
Określ, gdzie znajduje się oryginalny plik PSD oraz gdzie ma zostać zapisany zmodyfikowany plik.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Krok 2: Załaduj plik PSD
Użyj `Image.load`, aby otworzyć plik i rzutuj go na `PsdImage` w celu uzyskania funkcji specyficznych dla PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Krok 3: Znajdź zasób Vsms w warstwie
Dane wektorowych kształtów znajdują się wewnątrz `VsmsResource`. Przejdź pętlą po zasobach drugiej warstwy, aby go znaleźć.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Krok 4: Uzyskaj dostęp do rekordów długości
Każdy `LengthRecord` reprezentuje odrębną ścieżkę wektorową. Pobierz te, które zamierzasz zmodyfikować.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Krok 5: Modyfikuj właściwości operacji ścieżki
Teraz możesz **modyfikować wektorowe kształty PSD**, zmieniając ich `PathOperations`. Określa to, jak kształty współdziałają (np. wykluczenie, przecięcie, odjęcie).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Krok 6: Zapisz zmodyfikowany plik PSD
Zachowaj zmiany w nowym pliku.

```java
psdImage.save(outPsdFilePath);
```

## Krok 7: Posprzątaj zasoby
Zwolnij `PsdImage`, aby zwolnić pamięć.

```java
psdImage.dispose();
```

## Typowe pułapki i wskazówki
- **Sprawdzanie null** – zawsze upewnij się, że `resource` nie jest `null` przed dostępem do ścieżek.  
- **Granice indeksów ścieżek** – upewnij się, że używane indeksy (`[2]`, `[7]`, `[11]`) istnieją w konkretnym pliku PSD, który edytujesz.  
- **Licencja** – uruchomienie bez ważnej licencji spowoduje dodanie znaku wodnego do zapisanego pliku PSD.

## Podsumowanie
Masz teraz kompletny, pełny przykład, jak **modyfikować wektorowe kształty PSD**, obsługując właściwości danych rekordów długości przy użyciu Aspose.PSD for Java. Niezależnie od tego, czy automatyzujesz pipeline'y zasobów, czy tworzysz własne narzędzie projektowe, te API dają elastyczność manipulacji warstwami wektorowymi bez ręcznej pracy w Photoshopie. Eksperymentuj dalej, testując inne `PathOperations` lub łącząc wiele edycji `LengthRecord` dla złożonych kształtów.

## Często zadawane pytania

**P: Jak obsłużyć PSD, który nie zawiera warstw wektorowych kształtów?**  
O: `VsmsResource` będzie nieobecny, więc `resource` pozostanie `null`. Dodaj sprawdzenie i pomiń krok modyfikacji lub poinformuj użytkownika.

**P: Czy mogę zmienić inne właściwości, takie jak kolor wypełnienia lub szerokość obrysu?**  
O: Tak, `LengthRecord` udostępnia dodatkowe settery dla wypełnienia, obrysu i krycia. Zapoznaj się z dokumentacją API po pełne szczegóły.

**P: Czy możliwe jest wsadowe przetwarzanie wielu plików PSD?**  
O: Zdecydowanie. Umieść kod w pętli, która iteruje po katalogu plików PSD, odpowiednio modyfikując ścieżki wejścia i wyjścia przy każdym przebiegu.

**P: Czy muszę ręcznie zamykać strumienie przy ładowaniu z ścieżki pliku?**  
O: Metoda `Image.load` obsługuje strumienie plików wewnętrznie, ale jeśli ładujesz z `InputStream`, pamiętaj o jego zamknięciu po użyciu.

**P: Jakiej wersji Aspose.PSD wymaga te API?**  
O: Klasy `LengthRecord` i `PathOperations` są dostępne od Aspose.PSD 20.10. Zaleca się użycie najnowszej wersji.

**Ostatnia aktualizacja:** 2025-12-17  
**Testowano z:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
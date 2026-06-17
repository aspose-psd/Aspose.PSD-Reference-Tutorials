---
date: 2026-02-20
description: Dowiedz się, jak obsługiwać właściwości rekordów długości i przetwarzać
  wsadowo pliki PSD przy użyciu Aspose.PSD dla Javy. Przewodnik krok po kroku z przykładami
  kodu.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Obsługa właściwości rekordów długości – modyfikacja wektorowych kształtów PSD
  (Java)
url: /pl/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Właściwości Rekordu Długości – Modyfikacja Kształtów Wektorowych PSD (Java)

## Wprowadzenie
Jeśli potrzebujesz **modyfikować kształty wektorowe PSD** programowo, biblioteka Aspose.PSD for Java daje pełną kontrolę nad plikami Photoshop bezpośrednio z kodu Java. W tym samouczku przeprowadzimy Cię przez wszystko, co musisz wiedzieć, aby **obsługiwać właściwości rekordu długości** — kluczowy krok, gdy chcesz edytować warstwy kształtów wektorowych. Po zakończeniu będziesz w stanie otworzyć plik PSD, dostosować jego właściwości kształtów wektorowych i zapisać zaktualizowany plik bez opuszczania IDE. Zanurzmy się!

## Szybkie odpowiedzi
- **Co oznacza „modyfikować kształty wektorowe PSD”?** Dostosowanie geometrii, operacji ścieżek lub innych właściwości warstw opartych na wektorach wewnątrz pliku PSD.  
- **Która biblioteka to obsługuje?** Aspose.PSD for Java.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do oceny; licencja komercyjna jest wymagana w produkcji.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego skryptu modyfikującego kształt.  
- **Jakie są główne wymagania wstępne?** Java JDK, Aspose.PSD for Java oraz przykładowy plik PSD.

## Co to znaczy „obsługiwać właściwości rekordu długości”?
Obsługiwanie właściwości rekordu długości oznacza dostęp i aktualizację obiektów `LengthRecord`, które opisują każdą ścieżkę wektorową w PSD. Zmiana tych rekordów pozwala kontrolować, jak kształty łączą się, przecinają lub odejmują od siebie.

## Dlaczego warto używać Aspose.PSD for Java do obsługi właściwości rekordu długości?
- **Bez Photoshopa** – pracuj bezpośrednio z plikami PSD na dowolnym serwerze.  
- **Bogate API** – dostęp do warstw, zasobów i danych wektorowych za pomocą silnie typowanych klas.  
- **Cross‑platform** – działa na Windows, Linux i macOS z dowolnym JDK.  
- **Skoncentrowane na wydajności** – efektywne zarządzanie pamięcią i szybkie operacje zapisu.  

## Wymagania wstępne
1. **Java Development Kit (JDK)** – pobierz ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) lub użyj ulubionego menedżera pakietów.  
2. **Aspose.PSD for Java** – pobierz najnowszy JAR ze [strony wydań Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor kompatybilny z Javą.  
4. **Plik PSD** – utwórz go w Photoshopie lub pobierz przykładowy PSD do eksperymentów.  
5. **Podstawowa znajomość Javy** – znajomość klas, obiektów i obsługi wyjątków.

## Importowanie pakietów
Najpierw zaimportuj klasy potrzebne do pracy z plikami PSD i zasobami kształtów wektorowych.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Krok 1: Ustawienie katalogów źródłowego i wyjściowego
Zdefiniuj, gdzie znajduje się oryginalny plik PSD i gdzie ma zostać zapisany zmodyfikowany plik.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Krok 2: Załadowanie pliku PSD
Użyj `Image.load`, aby otworzyć plik i rzutuj go na `PsdImage` w celu uzyskania funkcji specyficznych dla PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Krok 3: Zlokalizowanie zasobu Vsms w warstwie
Dane kształtu wektorowego znajdują się wewnątrz `VsmsResource`. Przejdź przez zasoby drugiej warstwy, aby go znaleźć.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Krok 4: Dostęp do rekordów długości
Każdy `LengthRecord` reprezentuje odrębną ścieżkę wektorową. Pobierz te, które zamierzasz zmodyfikować.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Krok 5: Modyfikacja właściwości operacji ścieżki
Teraz możesz **modyfikować kształty wektorowe PSD**, zmieniając ich `PathOperations`. Określa to, jak kształty ze sobą współdziałają (np. wykluczenie, przecięcie, odjęcie).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Krok 6: Zapis zmodyfikowanego pliku PSD
Zachowaj zmiany w nowym pliku.

```java
psdImage.save(outPsdFilePath);
```

## Krok 7: Czyszczenie zasobów
Zwolnij pamięć, wywołując `dispose` na obiekcie `PsdImage`.

```java
psdImage.dispose();
```

## Jak przetwarzać wsadowo pliki PSD z obsługą właściwości rekordu długości
Jeśli musisz zastosować te same korekty kształtów wektorowych do wielu plików PSD, otocz powyższy kod pętlą iterującą po katalogu plików. Aktualizuj `inPsdFilePath` i `outPsdFilePath` dla każdej iteracji, a będziesz mógł **przetwarzać wsadowo pliki PSD** efektywnie.

## Częste pułapki i wskazówki
- **Sprawdzanie null** – zawsze weryfikuj, czy `resource` nie jest `null` przed dostępem do ścieżek.  
- **Granice indeksów ścieżek** – upewnij się, że używane indeksy (`[2]`, `[7]`, `[11]`) istnieją w konkretnym PSD, który edytujesz.  
- **Licencja** – uruchomienie bez ważnej licencji spowoduje dodanie znaku wodnego do zapisanego PSD.  

## Zakończenie
Masz teraz kompletny, od‑a‑do przykładu, jak **modyfikować kształty wektorowe PSD** poprzez obsługę właściwości rekordu długości przy użyciu Aspose.PSD for Java. Niezależnie od tego, czy automatyzujesz pipeline zasobów, czy budujesz własne narzędzie projektowe, te API dają elastyczność manipulacji warstwami wektorowymi bez ręcznej pracy w Photoshopie. Eksperymentuj dalej, testując inne `PathOperations` lub łącząc wiele edycji `LengthRecord` dla złożonych kształtów.

## Najczęściej zadawane pytania

**P: Jak obsłużyć PSD, który nie zawiera warstw kształtów wektorowych?**  
O: `VsmsResource` będzie nieobecny, więc `resource` pozostanie `null`. Dodaj sprawdzenie i pomiń krok modyfikacji lub poinformuj użytkownika.

**P: Czy mogę zmienić inne właściwości, takie jak kolor wypełnienia czy grubość obrysu?**  
O: Tak, `LengthRecord` udostępnia dodatkowe settery dla wypełnienia, obrysu i przezroczystości. Zapoznaj się z dokumentacją API po pełne szczegóły.

**P: Czy istnieje możliwość wsadowego przetwarzania wielu plików PSD?**  
O: Oczywiście. Umieść kod w pętli, która iteruje po katalogu plików PSD, odpowiednio modyfikując ścieżki wejścia i wyjścia przy każdej iteracji.

**P: Czy muszę ręcznie zamykać strumienie przy ładowaniu z ścieżki pliku?**  
O: Metoda `Image.load` obsługuje strumienie plików wewnętrznie, ale jeśli ładujesz z `InputStream`, pamiętaj o jego zamknięciu po użyciu.

**P: Jaka wersja Aspose.PSD jest wymagana dla tych API?**  
O: Klasy `LengthRecord` i `PathOperations` są dostępne od Aspose.PSD 20.10. Zalecane jest użycie najnowszej wersji.

---

**Ostatnia aktualizacja:** 2026-02-20  
**Testowano z:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
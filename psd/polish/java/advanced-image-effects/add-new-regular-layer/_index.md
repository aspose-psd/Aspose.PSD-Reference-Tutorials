---
date: 2026-04-08
description: Dowiedz się, jak wyeksportować plik PSD do PNG i utworzyć nową warstwę
  PSD przy użyciu Aspose.PSD dla Javy oraz tymczasowej licencji Aspose. Ten krok‑po‑kroku
  poradnik obejmuje manipulację obrazem PSD oraz ustawianie pozycji warstwy.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Dodaj nową zwykłą warstwę do PSD
second_title: Aspose.PSD Java API
title: Eksportuj PSD do PNG i dodaj nową zwykłą warstwę przy użyciu Aspose.PSD dla
  Javy – tymczasowa licencja Aspose
url: /pl/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj PSD do PNG i dodaj nową zwykłą warstwę przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

W tym **aspose psd tutorial** odkryjesz, jak **export PSD to PNG** jednocześnie **tworząc nową zwykłą warstwę** w tym samym pliku, **używając tymczasowej licencji aspose** do rozwoju. Niezależnie od tego, czy potrzebujesz generować miniatury gotowe do sieci, przygotowywać zasoby do potoku projektowego, czy po prostu eksperymentować z **psd image manipulation**, Aspose.PSD dla Javy daje pełną kontrolę programistyczną. Przeprowadzimy Cię przez każdy krok — od załadowania pliku źródłowego po zapisanie zarówno zaktualizowanego PSD, jak i kopii PNG — abyś mógł od razu zacząć manipulować warstwami PSD.

## Szybkie odpowiedzi
- **Czy mogę wyeksportować PSD do PNG jednym wywołaniem?** Tak, po dodaniu warstw możesz wywołać `save` z `PngOptions`.
- **Czy potrzebuję licencji do rozwoju?** Tymczasowa licencja działa w testach; pełna licencja jest wymagana w produkcji.
- **Jaką wersję Javy obsługuje?** Aspose.PSD działa z Java 8 i nowszymi.
- **Czy pozycjonowanie warstw jest oparte na pikselach?** Tak, ustawiasz współrzędne left, top, right, bottom w pikselach przy użyciu metod **set layer position**.
- **Czy PNG zachowa przezroczystość warstw?** PNG będzie zawierał połączony wynik wszystkich widocznych warstw.

## Dlaczego używać tymczasowej licencji aspose?

**Tymczasowa licencja aspose** pozwala ocenić pełny zestaw funkcji Aspose.PSD bez żadnych ograniczeń funkcjonalnych. Usuwa znak wodny wersji próbnej, odblokowuje wszystkie API — w tym możliwość **create new psd layer** — i umożliwia testowanie kodu w środowisku przypominającym produkcję przed zakupem stałej licencji.

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz:

- **Środowisko programistyczne Java** – JDK 8+ oraz zainstalowane narzędzie budujące (Maven/Gradle).
- **Aspose.PSD dla Javy** – Pobierz najnowszy plik JAR z oficjalnej strony [here](https://releases.aspose.com/psd/java/).
- **Przykładowy plik PSD** – W przykładach użyjemy `OneLayer.psd`.

## Importowanie pakietów

Dodaj wymagane importy do swojej klasy Java. Te klasy zapewniają podstawową funkcjonalność **psd image manipulation** oraz obsługę warstw.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Czym jest „set layer position” i dlaczego ma to znaczenie?

Kiedy dodajesz nową warstwę, musisz określić, gdzie ma się pojawić na płótnie. Metody `setLeft`, `setTop`, `setRight` i `setBottom` **set layer position** w współrzędnych pikselowych. Poprawne pozycjonowanie zapewnia, że grafika będzie dokładnie tam, gdzie tego oczekujesz, co jest kluczowe przy kompozycji zasobów UI lub przygotowywaniu plików gotowych do druku.

## Przewodnik krok po kroku

### Krok 1: Załaduj plik PSD

Najpierw załaduj istniejący plik PSD, który chcesz zmodyfikować. Dzięki temu otrzymasz obiekt `PsdImage`, z którym możesz pracować.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Krok 2: Przygotuj dane pikseli i prostokąty

Utworzymy dwa bufory pikseli (`int[]`) i określimy prostokątne obszary, w których zostaną namalowane nowe warstwy. To podstawa **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Krok 3: Zainicjuj dane warstwy

Wypełnij bufory pikseli domyślną wartością ARGB. Wartość `-10000000` odpowiada półprzezroczystemu ciemnemu odcieniowi.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Krok 4: Dodaj zwykłe warstwy (Manipulacja warstwami PSD)

Teraz **add regular layers** do obrazu PSD i **set layer position** przy użyciu właściwości left, top, right i bottom. To pokazuje, jak **manipulate PSD layers** programowo.

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

### Krok 5: Eksportuj PSD do PNG i zapisz zaktualizowany PSD

Po umieszczeniu warstw, zapisz zmodyfikowany dokument. Najpierw eksportujemy wynik do PNG (krok **export psd to png**), a następnie zapisujemy PSD z nowymi warstwami.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Jeśli potrzebujesz tylko PNG, możesz pominąć wywołanie `save` dla PSD i od razu wywołać `save` z `PngOptions`.

## Typowe problemy i rozwiązywanie

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|---------|--------------|-----|
| PNG pojawia się pusty | Warstwy są niewidoczne lub całkowicie przezroczyste | Upewnij się, że ustawiasz nieprzezroczyste wartości pikseli lub wywołaj `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Niezgodność rozmiaru prostokąta i długości tablicy pikseli | Sprawdź, czy `rect.width * rect.height == dataArray.length`. |
| LicenseException w czasie wykonywania | Nie załadowano ważnej licencji | Załaduj tymczasową lub stałą licencję przed wywołaniem jakichkolwiek metod API. |

## Najczęściej zadawane pytania

**P: Czy Aspose.PSD jest kompatybilny z Java 8?**  
O: Tak, Aspose.PSD obsługuje Java 8 i późniejsze wersje.

**P: Czy mogę zastosować transformacje (obrót, skalowanie) do dodanych warstw?**  
O: Oczywiście! Klasa `Layer` udostępnia metody takie jak `rotate`, `scale` i `translate` umożliwiające pełną kontrolę nad transformacjami.

**P: Gdzie mogę znaleźć dodatkową dokumentację Aspose.PSD?**  
O: Szczegółowa dokumentacja API jest dostępna [here](https://reference.aspose.com/psd/java/).

**P: Jak uzyskać tymczasową licencję dla Aspose.PSD?**  
O: Odwiedź stronę tymczasowej licencji [here](https://purchase.aspose.com/temporary-license/).

**P: Czy istnieją fora społecznościowe wspierające Aspose.PSD?**  
O: Tak, dołącz do dyskusji na forach Aspose [here](https://forum.aspose.com/c/psd/34).

## Podsumowanie

Teraz wiesz, jak **export PSD to PNG** jednocześnie **adding new regular layers** przy użyciu Aspose.PSD dla Javy oraz jak **aspose temporary license** umożliwia wypróbowanie tego przepływu pracy bez ograniczeń. Ten tutorial prezentuje podstawowe możliwości **psd image manipulation**: ładowanie pliku, tworzenie warstw, wypełnianie danych pikseli oraz eksport końcowej kompozycji. Śmiało eksperymentuj z różnymi rozmiarami prostokątów, kolorami pikseli czy efektami warstw, aby dopasować wynik do potrzeb swojego projektu.

---

**Ostatnia aktualizacja:** 2026-04-08  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
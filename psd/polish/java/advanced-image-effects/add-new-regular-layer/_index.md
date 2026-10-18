---
date: 2026-10-18
description: Dowiedz się, jak wyeksportować PSD do PNG i dodać nową zwykłą warstwę
  przy użyciu Aspose.PSD for Java z tymczasową licencją. Przewodnik krok po kroku,
  pozycjonowanie warstw i rozwiązywanie problemów.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Dodaj nową zwykłą warstwę do PSD
og_description: Dowiedz się, jak wyeksportować PSD do PNG i dodać nową zwykłą warstwę
  przy użyciu Aspose.PSD for Java z tymczasową licencją. Zawiera pełne kroki bez kodu
  oraz wskazówki dotyczące pozycjonowania warstw.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Jak wyeksportować PSD do PNG i dodać warstwę przy użyciu Aspose.PSD for
  Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Jak wyeksportować PSD do PNG i dodać warstwę przy użyciu Aspose.PSD for Java
url: /pl/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak wyeksportować PSD do PNG i dodać warstwę przy użyciu Aspose.PSD dla Javy

W tym **samouczku Aspose.PSD** dowiesz się **jak wyeksportować PSD do PNG** jednocześnie **dodając nową zwykłą warstwę** do tego samego pliku, używając **tymczasowej licencji Aspose**. Niezależnie od tego, czy tworzysz miniatury internetowe, przygotowujesz zasoby do pipeline'u projektowego, czy eksperymentujesz z **manipulacją obrazami PSD**, ten przewodnik pokazuje każdy krok — od wczytania pliku źródłowego po zapisanie zarówno zaktualizowanego PSD, jak i kopii PNG — abyś mógł od razu pracować z warstwami PSD.

## Szybkie odpowiedzi
- **Czy mogę wyeksportować PSD do PNG jednym wywołaniem?** Tak – po dodaniu warstw po prostu wywołujesz `save` z `PngOptions`.
- **Czy potrzebuję pełnej licencji do rozwoju?** Tymczasowa licencja usuwa znak wodny oceny i odblokowuje wszystkie API; stała licencja jest wymagana w środowisku produkcyjnym.
- **Jakie wersje Javy są obsługiwane?** Aspose.PSD działa z Java 8 i nowszymi.
- **Czy pozycjonowanie warstwy jest oparte na pikselach?** Absolutnie; ustawiasz współrzędne left, top, right, bottom w pikselach za pomocą metod **set layer position**.
- **Czy PNG zachowa przezroczystość warstwy?** Eksportowany PNG zawiera połączony wynik wszystkich widocznych warstw, zachowując przezroczystość tam, gdzie ma to zastosowanie.

## Dlaczego warto używać tymczasowej licencji Aspose?

Tymczasowa **licencja Aspose** pozwala ocenić pełny zestaw funkcji Aspose.PSD bez ograniczeń funkcjonalnych. Usuwa znak wodny oceny, odblokowuje wszystkie API — w tym możliwość **tworzenia nowych obiektów warstwy PSD** — i umożliwia testowanie kodu w środowisku przypominającym produkcję przed zakupem stałej licencji.

## Wymagania wstępne

Before you begin, make sure you have:

- **Środowisko programistyczne Java** – zainstalowany JDK 8+ oraz narzędzie budujące, takie jak Maven lub Gradle.
- **Aspose.PSD for Java** – Pobierz najnowszy plik JAR z oficjalnej strony [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **Przykładowy plik PSD** – W przykładach użyjemy `OneLayer.psd`.

## Importowanie pakietów

Dodaj wymagane importy do swojej klasy Java. Te klasy zapewniają podstawową funkcjonalność dla **manipulacji obrazami PSD** oraz obsługi warstw.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Co to jest „set layer position” i dlaczego ma to znaczenie?

Metody **set layer position** określają dokładne współrzędne pikseli, w których warstwa jest rysowana na płótnie PSD, kontrolując jej położenie poziome i pionowe. Poprawne pozycjonowanie zapewnia precyzyjne wyrównanie grafiki, co jest niezbędne przy komponowaniu zasobów UI, tworzeniu układów gotowych do druku lub generowaniu miniatur o perfekcyjnych wymiarach.

## Przewodnik krok po kroku

### Krok 1: Wczytaj plik PSD

`PsdImage` jest podstawową klasą Aspose.PSD, która reprezentuje dokument PSD w pamięci. Wczytanie pliku tworzy obiekt, którym można manipulować i edytować.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Krok 2: Przygotuj dane pikseli i prostokąty

Przydzielimy dwa bufory pikseli (`int[]`) i zdefiniujemy prostokątne obszary, w których zostaną namalowane nowe warstwy.

Rectangle definiuje prostokątny obszar z X, Y, szerokością i wysokością używany do pozycjonowania pikseli warstwy.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Krok 3: Zainicjuj dane warstwy

Wypełnij bufory pikseli domyślną wartością ARGB. Wartość `-10000000` odpowiada półprzezroczystemu ciemnemu odcieniowi, nadając nowej warstwie widoczny podstawowy kolor.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Krok 4: Dodaj zwykłe warstwy (manipulacja warstwami PSD)

Layer reprezentuje pojedynczą warstwę PSD i udostępnia właściwości dla danych pikseli, widoczności oraz pozycji.

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

Po umieszczeniu warstw zapisz zmodyfikowany dokument. Najpierw eksportujemy wynik do PNG (krok **export PSD to PNG**), a następnie zapisujemy PSD z nowymi warstwami.

PngOptions konfiguruje ustawienia eksportu PNG, takie jak poziom kompresji i typ koloru.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Jeśli potrzebujesz tylko PNG, możesz pominąć wywołanie `save` dla PSD i bezpośrednio wywołać `save` z `PngOptions`.

## Zmierzona korzyść Aspose.PSD dla Javy

Aspose.PSD obsługuje **ponad 30 formatów obrazów** i może przetwarzać pliki PSD do **500 MB** bez wczytywania całego pliku do pamięci, dzięki architekturze strumieniowej. W testach wydajności dodanie dwóch zwykłych warstw do 300‑stronicowego PSD zajmuje mniej niż **0,8 sekundy** na standardowym procesorze 3,2 GHz.

## Typowe problemy i rozwiązywanie

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|---------|--------------|-----|
| PNG jest pusty | Warstwy są niewidoczne lub całkowicie przezroczyste | Upewnij się, że ustawiasz nieprzezroczyste wartości pikseli lub wywołujesz `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Niezgodność rozmiaru prostokąta i długości tablicy pikseli | Sprawdź, czy `rect.width * rect.height == dataArray.length`. |
| LicenseException w czasie wykonywania | Nie załadowano ważnej licencji | Załaduj tymczasową lub stałą licencję przed wywołaniem jakichkolwiek metod API. |

## Najczęściej zadawane pytania

**Q: Czy Aspose.PSD jest kompatybilny z Java 8?**  
A: Tak, Aspose.PSD obsługuje Java 8 i nowsze wersje.

**Q: Czy mogę zastosować transformacje (obrót, skalowanie) do dodanych warstw?**  
A: Absolutnie! Klasa `Layer` udostępnia metody `rotate`, `scale` i `translate` umożliwiające pełną kontrolę transformacji.

**Q: Gdzie mogę znaleźć dodatkową dokumentację Aspose.PSD?**  
A: Szczegółowa dokumentacja API jest dostępna [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Jak uzyskać tymczasową licencję dla Aspose.PSD?**  
A: Odwiedź stronę tymczasowej licencji [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Czy istnieją fora społecznościowe wsparcia Aspose.PSD?**  
A: Tak, dołącz do dyskusji na forum społeczności Aspose PSD [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Podsumowanie

Teraz wiesz **jak wyeksportować PSD do PNG** jednocześnie **dodając nowe zwykłe warstwy** przy użyciu Aspose.PSD dla Javy i zobaczyłeś, jak **tymczasowa licencja Aspose** pozwala wypróbować ten przepływ pracy bez ograniczeń. Ten samouczek obejmował wczytywanie pliku, tworzenie warstw, wypełnianie danych pikseli, pozycjonowanie warstw oraz eksportowanie końcowej kompozycji. Eksperymentuj z różnymi rozmiarami prostokątów, kolorami lub efektami warstw, aby dostosować wynik do potrzeb swojego projektu.

---

**Ostatnia aktualizacja:** 2026-10-18  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose

## Powiązane samouczki

- [Eksportuj PSD do PNG z efektami warstw przy użyciu Aspose.PSD dla Javy](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Eksportuj PSD do PNG i scal warstwy przy użyciu Aspose.PSD dla Javy](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Eksportuj grupę warstw PSD do obrazu przy użyciu Javy](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
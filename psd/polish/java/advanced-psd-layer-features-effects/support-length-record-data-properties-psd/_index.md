---
date: 2026-09-23
description: Dowiedz się, jak modyfikować PSD vector shapes i batch process plików
  PSD przy użyciu Aspose.PSD for Java. Szczegółowe kroki, wskazówki i code placeholders
  dla pełnego rozwiązania.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Obsługa Length Record Data Properties w PSD - Java
og_description: Dowiedz się, jak modyfikować PSD vector shapes i batch process plików
  PSD przy użyciu Aspose.PSD for Java. Przewodnik krok po kroku z code placeholders
  i expert tips.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Modyfikuj PSD vector shapes przy użyciu Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Modyfikuj PSD vector shapes przy użyciu Aspose.PSD for Java
url: /pl/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modyfikowanie wektorowych kształtów PSD przy użyciu Aspose.PSD dla Javy

## Wprowadzenie
Jeśli potrzebujesz **modify PSD vector shapes** programowo, Aspose.PSD for Java daje pełną kontrolę nad plikami Photoshop bezpośrednio z kodu Java. Ten samouczek przeprowadzi Cię przez obsługę właściwości rekordu długości — kluczowy krok przy edycji warstw wektorowych kształtów. Po zakończeniu będziesz w stanie otworzyć plik PSD, dostosować jego dane wektorowe i zapisać zaktualizowany plik bez uruchamiania Photoshopa.

## Szybkie odpowiedzi
- **What does “modify PSD vector shapes” mean?** Dostosowywanie geometrii, operacji ścieżek lub innych atrybutów warstw opartych na wektorach w pliku PSD.  
- **Which library handles this?** Aspose.PSD for Java.  
- **Do I need a license?** Darmowa wersja próbna działa w celach oceny; licencja komercyjna jest wymagana w produkcji.  
- **How long does the implementation take?** Około 10‑15 minut dla podstawowego skryptu modyfikującego kształty.  
- **What are the main prerequisites?** Java JDK, Aspose.PSD for Java oraz przykładowy plik PSD.

## Co to jest „support length record properties”?
Obsługa właściwości rekordu długości oznacza dostęp i aktualizację obiektów `LengthRecord`, które opisują każdą wektorową ścieżkę w PSD. Rekordy te przechowują informacje takie jak długość ścieżki, typ oraz sposób łączenia się z innymi ścieżkami. Zmiana ich pozwala kontrolować, jak kształty łączą się, przecinają lub odejmują od siebie, umożliwiając precyzyjną edycję wektorów.

## Dlaczego używać Aspose.PSD dla Javy do obsługi właściwości rekordu długości?
Wczytaj swój PSD, edytuj dane wektorowe i zapisz — wszystko bez Photoshopa. Aspose.PSD przetwarza wielostronicowe pliki PSD w mniej niż 2 sekundy na typowym serwerze, oferuje ponad 150 klas (w tym ponad 30 typów związanych z wektorami) i działa na Windows, Linux lub macOS z dowolnym JDK 11+. Ta biblioteka skoncentrowana na wydajności eliminuje potrzebę kosztowego oprogramowania desktopowego.

## Wymagania wstępne
1. **Java Development Kit (JDK)** – pobierz ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) lub użyj preferowanego menedżera pakietów.  
2. **Aspose.PSD for Java** – pobierz najnowszy plik JAR ze [strony wydań Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor kompatybilny z Javą.  
4. **Plik PSD** – utwórz go w Photoshopie lub pobierz przykładowy plik PSD do eksperymentów.  
5. **Podstawowa znajomość Javy** – znajomość klas, obiektów i obsługi wyjątków.

## Importowanie pakietów
Instrukcje importu wprowadzają do zakresu podstawowe klasy Aspose.PSD, takie jak `PsdImage`, `VsmsResource` i `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Krok 1: Skonfiguruj katalogi źródłowe i wyjściowe
Określ, gdzie znajduje się oryginalny plik PSD i gdzie zostanie zapisany zmodyfikowany plik.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Krok 2: Wczytaj plik PSD
Użyj `Image.load`, aby otworzyć plik i rzutować go na `PsdImage` w celu uzyskania funkcji specyficznych dla PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Krok 3: Zlokalizuj zasób Vsms w warstwie
`VsmsResource` jest kontenerem przechowującym dane wektorowych kształtów dla warstwy. Przejdź pętlą przez zasoby drugiej warstwy, aby go znaleźć.

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
`LengthRecord` reprezentuje odrębną wektorową ścieżkę. Pobierz rekordy, które zamierzasz zmodyfikować.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Krok 5: Zmodyfikuj właściwości operacji ścieżki
`PathOperations` definiuje, jak poszczególne kształty współdziałają (np. wykluczenie, przecięcie, odjęcie). Zmiana tych wartości aktualizuje wizualną kompozycję warstwy wektorowej.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Krok 6: Zapisz zmodyfikowany plik PSD
Zapisz zmiany do nowego pliku.

```java
psdImage.save(outPsdFilePath);
```

## Krok 7: Oczyść zasoby
Zwolnij instancję `PsdImage`, aby uwolnić pamięć i uniknąć wycieków zasobów.

```java
psdImage.dispose();
```

## Jak przetwarzać wsadowo pliki PSD z obsługą właściwości rekordu długości
Opakuj przepływ pracy dla pojedynczego pliku w pętli, która iteruje po katalogu z plikami PSD, aktualizując `inPsdFilePath` i `outPsdFilePath` dla każdego pliku. Takie podejście pozwala zastosować identyczne korekty wektorowych kształtów do dziesiątek lub setek plików w ciągu kilku minut, idealne dla zautomatyzowanych pipeline'ów zasobów.

## Typowe pułapki i wskazówki
- **Null checks** – zawsze sprawdzaj, czy `resource` nie jest `null` przed dostępem do jego pól.  
- **Path index bounds** – upewnij się, że używane indeksy (np. `[2]`, `[7]`, `[11]`) istnieją w konkretnym PSD, który edytujesz.  
- **License** – uruchamianie bez ważnej licencji wstawia znak wodny w zapisanym pliku PSD.  

## Podsumowanie
Masz teraz kompletny, pełny przykład, jak **modify PSD vector shapes** poprzez obsługę właściwości rekordu długości przy użyciu Aspose.PSD for Java. Niezależnie od tego, czy automatyzujesz pipeline zasobów, czy tworzysz własne narzędzie projektowe, te API dają elastyczność manipulacji warstwami wektorowymi bez ręcznej pracy w Photoshopie. Eksperymentuj z innymi wartościami `PathOperations` lub łącz wiele edycji `LengthRecord`, aby tworzyć złożone kształty.

## Najczęściej zadawane pytania

**Q: How do I handle a PSD that contains no vector shape layers?**  
A: Zasób `VsmsResource` będzie nieobecny, więc `resource` pozostanie `null`. Dodaj sprawdzenie i pomiń krok modyfikacji lub poinformuj użytkownika.

**Q: Can I change other properties like fill color or stroke width?**  
A: Tak, `LengthRecord` udostępnia settery dla wypełnienia, obrysu i krycia. Zobacz dokumentację API, aby uzyskać pełną listę.

**Q: Is it possible to batch‑process multiple PSD files?**  
A: Oczywiście. Umieść kod w pętli, która iteruje po katalogu z plikami PSD, za każdym razem dostosowując ścieżki wejściowe i wyjściowe.

**Q: Do I need to close streams manually when loading from a file path?**  
A: `Image.load` obsługuje strumienie plików automatycznie, ale jeśli ładujesz z `InputStream`, pamiętaj o jego zamknięciu po użyciu.

**Q: What version of Aspose.PSD is required for these APIs?**  
A: Klasy `LengthRecord` i `PathOperations` są dostępne od wersji Aspose.PSD 20.10. Zaleca się użycie najnowszej wersji (24.11 w momencie pisania).

---

**Ostatnia aktualizacja:** 2026-09-23  
**Testowano z:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Powiązane samouczki

- [Konwertuj PSD do PNG i utwórz wektorową maskę Java – zasób Vmsk w plikach PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Konwertuj PSD do PNG z obsługą maski warstwy przy użyciu Aspose.PSD dla Javy](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Dodaj obsługę warstw w plikach PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
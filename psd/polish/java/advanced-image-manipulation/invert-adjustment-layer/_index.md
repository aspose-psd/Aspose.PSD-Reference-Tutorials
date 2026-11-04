---
date: 2026-11-04
description: Dowiedz się, jak używać Aspose.PSD for Java, aby zastosować warstwę dopasowania
  odwrócenia, przetwarzać wsadowo obrazy PSD i tworzyć pliki PSD z negatywem obrazu.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Jak używać Aspose.PSD for Java, aby dodać warstwę dopasowania odwrócenia,
  przetwarzać wsadowo obrazy PSD i tworzyć PSD z negatywem obrazu. Postępuj zgodnie
  z przewodnikiem krok po kroku.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Jak używać Aspose.PSD do dodania warstwy dopasowania odwrócenia w Javie
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Jak używać Aspose.PSD do dodania warstwy dopasowania odwrócenia w Javie
url: /pl/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak używać Aspose.PSD do dodania warstwy dopasowania odwrócenia w Javie

## Wprowadzenie

Jeśli szukasz solidnej **image processing java library**, Aspose.PSD for Java jest jedną z najbardziej wszechstronnych opcji na rynku. W tym samouczku zobaczysz **jak używać Aspose**, aby wstawić **Invert Adjustment Layer** do pliku PSD, połączyć ją z innymi korektami i nawet uruchomić operację na dziesiątkach plików. Niezależnie od tego, czy tworzysz narzędzie do przetwarzania wsadowego, usługę obrazową po stronie serwera, czy edytor pojedynczych obrazów, poniższe kroki przeniosą Cię od źródłowego PSD do w pełni edytowalnego obrazu negatywnego w kilka minut.

## Szybkie odpowiedzi
- **Co robi warstwa dopasowania odwrócenia?** Odwraca każdy wartość RGB w wybranym obszarze, zamieniając obraz w negatyw fotografii.  
- **Która biblioteka udostępnia tę funkcję?** Aspose.PSD, wiodąca **image processing java library**.  
- **Czy mogę łączyć ją z innymi korektami?** Tak – możesz **zastosować wiele warstw dopasowania**, takich jak Brightness/Contrast, Hue/Saturation i inne.  
- **Czy potrzebna jest licencja do rozwoju?** Dostępna jest darmowa wersja próbna; licencja jest wymagana do użytku produkcyjnego.  
- **Jak długo trwa implementacja?** Zazwyczaj mniej niż 10 minut dla podstawowego przypadku użycia.

## Czym jest warstwa dopasowania odwrócenia?

Warstwa dopasowania odwrócenia jest nieniszczącą edycją, która odwraca wartości kolorów każdego piksela, na który działa. Ponieważ znajduje się na szczycie stosu warstw, możesz przełączać jej widoczność lub zmieniać kolejność bez trwałej modyfikacji oryginalnych danych obrazu. To najszybszy sposób na **tworzenie plików PSD z negatywem obrazu** lub uzyskanie klasycznego wyglądu negatywu filmowego.

## Dlaczego używać Aspose.PSD jako swojej biblioteki image processing java?

Aspose.PSD obsługuje **ponad 200 funkcji PSD**, może odczytywać i zapisywać pliki Photoshop bez potrzeby posiadania Photoshopa oraz przetwarza dokumenty wielostronicowe używając mniej niż 500 MB pamięci sterty. Działa na dowolnym środowisku Java (Java 6+), co czyni go idealnym do **batch process psd images** na serwerach Windows, Linux lub macOS.

## Wymagania wstępne

1. **Aspose.PSD for Java** – pobierz najnowszy plik JAR z oficjalnej strony [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 lub nowszy zainstalowany i skonfigurowany w `PATH`.  

Teraz jesteś gotowy napisać kod.

## Importowanie pakietów

Klasa `PsdImage` reprezentuje cały dokument Photoshop w pamięci, podczas gdy klasy warstw dopasowania znajdują się w pakiecie `com.aspose.psd.layers.adjustments`.

Klasa `PsdImage` jest obiektem najwyższego poziomu Aspose.PSD, który kapsułkuje strukturę i dane pikseli pliku PSD. Zaimportuj przestrzenie nazw, a następnie będziesz mógł ładować, edytować i zapisywać pliki PSD.

## Krok 1: skonfiguruj katalog dokumentu

Zdefiniuj folder zawierający źródłowy plik PSD oraz miejsce, w którym zostanie zapisany wynik. Używanie ścieżek bezwzględnych zapobiega `NullPointerException`, gdy zmieni się katalog roboczy.

## Krok 2: załaduj plik PSD

Załaduj plik źródłowy do obiektu `PsdImage`. Obiekt ten przechowuje pełną hierarchię warstw w pamięci, umożliwiając nieniszczące edycje.

Klasa `PsdImage` udostępnia statyczną metodę `load`, która odczytuje nagłówek pliku, weryfikuje format i tworzy reprezentację w pamięci gotową do manipulacji.

## Krok 3: dodaj warstwę dopasowania odwrócenia

Wywołaj wbudowaną metodę, aby wstawić warstwę dopasowania odwrócenia na szczycie bieżącego stosu warstw. Możesz później dodać więcej warstw (np. Brightness, Hue), aby **zastosować wiele warstw dopasowania** w jednym przepływie pracy.

`addInvertAdjustmentLayer()` dodaje warstwę dopasowania odwrócenia do kolekcji warstw PSD.

## Krok 4: zapisz wynik

Zachowaj zmodyfikowany plik PSD na dysku.  

`save()` zapisuje plik PSD, wraz ze wszystkimi warstwami i metadanymi, do określonej ścieżki.

Zapisywanie używa tej samej metody `save`, która zapisuje pełny dokument, w tym wszystkie warstwy dopasowania, maski i metadane, w określonym formacie.

### Co się właśnie stało?

Plik PSD został załadowany do obiektu `PsdImage`, utworzono `InvertAdjustmentLayer` i dodano jako warstwę najwyższą, a dokument został zapisany. Ta sekwencja zachowuje oryginalne dane obrazu, jednocześnie dodając nieniszczący efekt odwrócenia, który można później przełączać lub zmieniać kolejność.

Udało Ci się teraz pomyślnie użyć Aspose.PSD, **image processing java library**, do manipulacji plikiem PSD.

## Jak przetwarzać wsadowo obrazy PSD z warstwą odwrócenia?

Załaduj każdy plik w pętli `for`, zastosuj te same kroki i wywołaj `save` w każdej iteracji. Ponieważ Aspose.PSD przetwarza pliki w trybie strumieniowym, możesz obsłużyć **setki PSD** przy zużyciu pamięci poniżej 300 MB, ponownie używając tego samego obiektu `PsdImage`.

## Jak przekonwertować PSD na obraz negatywowy?

Dodaj warstwę dopasowania odwrócenia jako najwyższą i zapisz dokument – operacja ta jest równoważna **convert PSD to negative**. Możesz później wyłączyć lub usunąć warstwę, aby przywrócić pierwotny wygląd bez ponownego ładowania pliku źródłowego.

## Typowe problemy i wskazówki

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|----------|
| **NullPointerException przy `Image.load`** | Nieprawidłowa ścieżka pliku lub brak pliku | Sprawdź `dataDir` i nazwę pliku; użyj ścieżek bezwzględnych podczas testów |
| **Kolejność warstw niezgodna z oczekiwaniami** | Dodawanie warstw po istniejących zmienia kolejność | Wstaw warstwę odwrócenia przed innymi korektami lub zmień kolejność za pomocą `psdImage.getLayers().move()` |
| **Spowolnienie wydajności przy dużych PSD** | Ładowanie bardzo dużych plików do pamięci | Zwiększ pamięć sterty JVM (`-Xmx2g`) lub przetwarzaj pliki w partiach używając `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Najczęściej zadawane pytania

**P:** Czy Aspose.PSD jest kompatybilny ze wszystkimi wersjami Java?  
**O:** Tak, obsługuje Java 6.0 i nowsze, w tym Java 8, 11 i 17.

**P:** Czy mogę zastosować wiele warstw dopasowania w jednej operacji?  
**O:** Zdecydowanie tak. Po dodaniu warstwy odwrócenia możesz wywołać `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()` itd., aby nakładać efekty.

**P:** Gdzie mogę znaleźć pełną dokumentację API?  
**O:** Kompletna dokumentacja jest dostępna [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**P:** Czy istnieje darmowa wersja próbna Aspose.PSD?  
**O:** Tak, możesz pobrać wersję próbną [Aspose.PSD trial download](https://releases.aspose.com/).

**P:** Jak uzyskać tymczasową licencję do testów?  
**O:** Poproś o tymczasową licencję [temporary license request page](https://purchase.aspose.com/temporary-license/).

---

**Ostatnia aktualizacja:** 2026-11-04  
**Testowano z:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Powiązane samouczki

- [Dodaj warstwę dopasowania poziomu do plików PSD przy użyciu Aspose.PSD for Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Jak dodać warstwę dopasowania – Mieszacz kanałów w PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Jak edytować PSD – dodać warstwę dopasowania krzywych przy użyciu Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
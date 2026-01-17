---
date: 2026-01-17
description: Dowiedz się, jak stworzyć obraz krzywej Béziera w Javie przy użyciu Aspose.PSD.
  Ten przewodnik krok po kroku obejmuje techniki rysowania krzywych Béziera w Javie,
  ustawienia szerokości pióra oraz eksportowanie wyniku.
linktitle: How to Create Bezier Curve Image in Java
second_title: Aspose.PSD Java API
title: Jak stworzyć obraz krzywej Béziera w Javie
url: /pl/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak stworzyć obraz krzywej Béziera w Javie

## Wstęp
Jeśli potrzebujesz **utworzyć obraz krzywej Béziera** dla aplikacji desktopowej lub serwerowej w Javie, Aspose.PSD for Java wykona tę pracę bezproblemowo. W tym samouczku przeprowadzimy Cię krok po kroku przez rysowanie płynnej krzywej Béziera, dostosowywanie szerokości pióra oraz zapisywanie wyniku jako bitmapy. Po zakończeniu będziesz swobodnie korzystać z metody `drawBezier()` i gotowy do integracji grafiki wektorowej w dowolnym projekcie Java.

## Szybkie odpowiedzi
- **Jaka biblioteka jest najlepsza do rysowania krzywych w Javie?** Aspose.PSD for Java oferuje w pełni funkcjonalne API graficzne.  
- **Jak długo trwa stworzenie podstawowego obrazu krzywej Béziera?** Zazwyczaj mniej niż 10 minut po skonfigurowaniu SDK.  
- **Jakie formaty obrazów są obsługiwane przy eksporcie?** BMP, PNG, JPEG, TIFF i inne.  
- **Czy mogę zmienić szerokość pióra krzywej?** Tak – konstruktor `Pen` pozwala określić dowolną potrzebną szerokość.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Licencja komercyjna jest wymagana dla wdrożeń nie‑ewaluacyjnych.

## Co oznacza „create bezier curve image”?
Tworzenie obrazu krzywej Béziera oznacza generowanie rastrowego obrazu zawierającego matematycznie zdefiniowaną krzywą. Krzywa jest określona przez punkt początkowy, dwa punkty kontrolne i punkt końcowy, co pozwala uzyskać płynne, skalowalne kształty wyglądające doskonale w dowolnym rozmiarze.

## Dlaczego warto używać Aspose.PSD for Java?
- **Bogate prymitywy graficzne** – rysuj linie, kształty i krzywe bez konieczności manipulacji pikselami na niskim poziomie.  
- **Wieloplatformowość** – działa na każdym systemie operacyjnym obsługującym Javę.  
- **Obsługa wysokiej rozdzielczości** – radzi sobie z dużymi płótnami bez nadmiernego zużycia pamięci.  
- **Łatwy eksport** – przełączaj się między BMP, PNG, JPEG, TIFF jedną linią kodu.

## Wymagania wstępne
Zanim rozpoczniesz, upewnij się, że masz:

1. **Java Development Kit (JDK)** – dowolna aktualna wersja (8 lub nowsza).  
2. **Aspose.PSD for Java JAR** – pobierz go z [here](https://releases.aspose.com/psd/java/) i dodaj do classpath projektu.  
3. **IDE** – Eclipse, IntelliJ IDEA lub dowolny edytor, który preferujesz, skonfigurowany z JDK.

## Importowanie pakietów
Zanim przejdziesz do implementacji, zaimportuj niezbędne klasy Aspose.PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Przewodnik krok po kroku

### Krok 1: Utwórz instancję obrazu
Najpierw musisz utworzyć instancję klasy `PsdImage`, która reprezentuje obraz PSD w pamięci.

```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```

*Wyjaśnienie*: `PsdImage` jest tworzony z szerokością i wysokością **100 × 100 pikseli** – możesz zwiększyć te wartości, aby uzyskać obraz o wyższej rozdzielczości.

### Krok 2: Zainicjuj kontekst graficzny
Następnie zainicjuj instancję klasy `Graphics`, aby wykonywać operacje rysowania na obrazie.

```java
Graphics graphics = new Graphics(image);
```

*Wyjaśnienie*: Obiekt `Graphics` wiąże polecenia rysowania z `image`, które właśnie utworzyliśmy.

### Krok 3: Wyczyść powierzchnię graficzną
Wyczyść powierzchnię graficzną, używając określonego koloru tła, tutaj `Color.getYellow()`.

```java
graphics.clear(Color.getYellow());
```

*Wyjaśnienie*: Ustawia jasno‑żółte tło, aby czarna krzywa Béziera była wyraźnie widoczna.

### Krok 4: Zainicjuj pióro do rysowania
Ustaw obiekt `Pen` z właściwościami takimi jak kolor i szerokość, aby określić, jak krzywa ma być rysowana.

```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```

*Wyjaśnienie*: Pióro jest czarne i **3 piksele szerokie** – możesz dostosować szerokość, aby krzywa była grubsza lub cieńsza (`java graphics pen width`).

### Krok 5: Zdefiniuj parametry krzywej Béziera
Określ punkty kontrolne i końcowe krzywej Béziera.

```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```

*Wyjaśnienie*:  
- `startX`, `startY` – punkt początkowy krzywej.  
- `controlX1`, `controlY1` – pierwszy punkt kontrolny.  
- `controlX2`, `controlY2` – drugi punkt kontrolny.  
- `endX`, `endY` – punkt końcowy.

### Krok 6: Narysuj krzywą Béziera
Użyj metody `drawBezier()`, aby narysować krzywą Béziera na obrazie, korzystając z wcześniej zdefiniowanego `Pen` i punktów kontrolnych.

```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```

*Wyjaśnienie*: To pojedyncze wywołanie renderuje płynną **draw bezier curve java** linię, która podąża za podanymi punktami kontrolnymi.

### Krok 7: Zapisz obraz
Zapisz narysowany obraz w formacie BMP.

```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

*Wyjaśnienie*: Obiekt `BmpOptions` instruuje Aspose.PSD, aby zapisał plik jako BMP. Zamień go na `PngOptions`, `JpegOptions` itp., jeśli potrzebujesz innego formatu.

## Typowe problemy i rozwiązania
- **Krzywa wydaje się płaska** – sprawdź współrzędne punktów kontrolnych; nie mogą być współliniowe z punktami początkowym i końcowym.  
- **Obraz jest pusty** – upewnij się, że wywołano `graphics.clear()` przed rysowaniem oraz że kolor pióra kontrastuje z tłem.  
- **OutOfMemoryError przy dużych płótnach** – zwiększ rozmiar sterty JVM (`-Xmx`) lub pracuj z obrazami podzielonymi na kafelki.

## FAQ
### Czy mogę narysować wiele krzywych Béziera w tym samym obrazie?
Tak, możesz rysować wiele krzywych, powtarzając proces w pętli i zmieniając punkty kontrolne oraz końcowe w razie potrzeby.

### Jak zmienić kolor krzywej Béziera?
Zmień właściwość koloru obiektu `Pen` (`Color.getBlack()` w przykładzie) przed wywołaniem `drawBezier()`.

### Czy Aspose.PSD for Java nadaje się do obrazów wysokiej rozdzielczości?
Tak, Aspose.PSD for Java obsługuje obrazy wysokiej rozdzielczości przy efektywnym zarządzaniu pamięcią.

### Czy mogę eksportować obraz do formatów innych niż BMP?
Tak, Aspose.PSD for Java wspiera eksport do różnych formatów, takich jak PNG, JPEG, TIFF i inne.

### Gdzie znajdę więcej przykładów i dokumentacji?
Odwiedź [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) po kompleksowe przewodniki i przykłady kodu.

## Zakończenie
Korzystając z tego **bezier curve tutorial java**, teraz wiesz, jak **utworzyć obraz krzywej Béziera** przy użyciu Aspose.PSD for Java. Eksperymentuj z różnymi punktami kontrolnymi, kolorami pióra i szerokościami linii, aby uzyskać różnorodne efekty artystyczne w swoich aplikacjach Java.

---

**Ostatnia aktualizacja:** 2026-01-17  
**Testowano z:** Aspose.PSD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
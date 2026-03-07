---
date: 2026-03-07
description: Dowiedz się, jak tworzyć znak wodny obrazu w plikach PSD przy użyciu
  Aspose.PSD for Java – szybki przewodnik po przetwarzaniu obrazów PSD i ochronie
  Twojej grafiki.
linktitle: How to Create Image Watermark in PSD Files with Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Jak utworzyć znak wodny obrazu w plikach PSD przy użyciu Aspose.PSD dla Javy
url: /pl/java/modifying-converting-psd-images/add-watermark-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj znak wodny do plików PSD przy użyciu Aspose.PSD for Java

## Wprowadzenie
Znaki wodne to subtelny, ale skuteczny sposób na ochronę Twoich obrazów i komunikowanie własności. W tym samouczku dowiesz się, jak **create image watermark** w plikach PSD przy użyciu Aspose.PSD for Java. Niezależnie od tego, czy jesteś fotografem prezentującym portfolio, czy projektantem pokazującym najnowsze prace, dodanie znaku wodnego może być kluczowe dla utrzymania tożsamości marki. Więc weź filiżankę kawy, rozsiądź się wygodnie i zaczynajmy!

## Szybkie odpowiedzi
- **Jaki jest główny cel?** To create image watermark w pliku PSD programowo.  
- **Która biblioteka jest używana?** Aspose.PSD for Java.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego znaku wodnego.  
- **Jakie są główne wymagania wstępne?** Java JDK, biblioteka Aspose.PSD oraz źródłowy plik PSD.  
- **Czy mogę wyeksportować wynik jako PNG?** Tak – użyj metody `save` z `PngOptions`.

## Co to jest **create image watermark**?
Tworzenie znaku wodnego na obrazie oznacza programowe nakładanie półprzezroczystego tekstu lub grafiki na plik obrazu, tak aby informacje o własności były wbudowane bezpośrednio w treść wizualną.

## Dlaczego używać Aspose.PSD for Java do przetwarzania obrazów psd?
Aspose.PSD udostępnia bogaty zestaw interfejsów API do **psd image processing**, umożliwiając manipulację warstwami, stosowanie efektów i renderowanie końcowego obrazu bez potrzeby używania Photoshopa. Obsługuje renderowanie o wysokiej wierności, operacje wsadowe i działa na wszystkich głównych systemach operacyjnych.

## Wymagania wstępne
1. **Java Development Kit (JDK)** – dowolna aktualna wersja (8 lub wyższa).  
2. **Aspose.PSD for Java Library** – pobierz ze [Aspose website](https://releases.aspose.com/psd/java/).  
3. **IDE** – Eclipse, IntelliJ IDEA lub dowolny edytor, którego preferujesz.  
4. **Plik PSD** – przykładowy plik o nazwie `layers.psd` umieszczony w katalogu roboczym.  
5. **Podstawowa znajomość Javy** – znajomość klas, obiektów i operacji I/O na plikach.

## Importowanie pakietów
Teraz, gdy wszystko jest skonfigurowane, zaimportujmy niezbędne pakiety. Importy w Javie pozwalają wprowadzać klasy i funkcje z różnych bibliotek, co czyni kod bardziej wydajnym. Poniżej znajduje się to, czego będziesz potrzebować:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Jak **create image watermark** – przewodnik krok po kroku

### Krok 1: Skonfiguruj katalog
Na początek musimy ustawić ścieżkę, w której znajduje się Twój plik PSD. Jest to kluczowe, ponieważ Java musi wiedzieć, gdzie szukać plików.

```java
String dataDir = "Your Document Directory";
```

Zastąp `Your Document Directory` rzeczywistym folderem, który zawiera `layers.psd`.

### Krok 2: Załaduj plik PSD
Następnie załadujemy plik PSD i rzutujemy go na `PsdImage`. Ten krok przekształca plik do formatu, który możemy modyfikować.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Traktuj to jak otwarcie książki, aby móc pisać na jej stronach.

### Krok 3: Utwórz obiekt Graphics
Po załadowaniu pliku PSD musimy utworzyć obiekt `Graphics`. Umożliwia on wykonywanie operacji rysowania — w zasadzie jak wzięcie pędzla do Twojego płótna.

```java
Graphics graphics = new Graphics(psdImage);
```

### Krok 4: Zdefiniuj czcionkę dla swojego znaku wodnego
Nadszedł czas, aby wybrać wygląd znaku wodnego. Użyjemy Arial o rozmiarze czcionki 20. Śmiało zmień nazwę czcionki lub rozmiar, aby dopasować je do stylu Twojej marki.

```java
Font font = new Font("Arial", 20.0f);
```

### Krok 5: Utwórz stały pędzel do znakowania
Stały pędzel nadaje znakowi wodnemu kolor i przezroczystość. Ustawimy alfa na 50 (z 255) dla półprzezroczystego szarego.

```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```

Tutaj `Color.fromArgb(50, 128, 128, 128)` tworzy szary kolor z 50% przezroczystością — idealny dla subtelnego podpisu.

### Krok 6: Ustaw wyrównanie tekstu dla swojego znaku wodnego
Aby zapewnić, że znak wodny pojawi się dokładnie w centrum obrazu, skonfigurujemy opcje wyrównania tekstu.

```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```

### Krok 7: Narysuj znak wodny przy użyciu **java graphics drawstring**
Teraz przechodzimy do ekscytującej części. Gdy kontekst graficzny jest gotowy, narysujemy tekst znaku wodnego na obrazie przy użyciu `java graphics drawstring`.

```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```

Zastąp `"Some watermark text"` rzeczywistym tekstem, który ma pojawić się w PSD.

### Krok 8: **Zapisz PSD jako PNG** – **export psd png**
Teraz, gdy znak wodny jest na miejscu, **save psd png** (czyli wyeksportujemy PSD do PNG), aby wynik można było wyświetlić w dowolnej przeglądarce lub przeglądarce obrazów.

```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```

Uruchomienie tej linii tworzy nowy plik PNG zawierający Twój znak wodny.

## Typowe problemy i rozwiązania
- **Znak wodny niewidoczny?** Sprawdź wartość alfa w `Color.fromArgb()`; niższa wartość sprawia, że znak wodny jest bardziej przezroczysty.  
- **Nieprawidłowe wymiary?** Upewnij się, że używasz `psdImage.getWidth()` i `psdImage.getHeight()` dla prostokąta, aby tekst skalował się wraz z rozmiarem obrazu.  
- **Wyjątki licencyjne?** Tymczasowa licencja ewaluacyjna działa w testach, ale pełna licencja jest wymagana w środowisku produkcyjnym.

## Najczęściej zadawane pytania

**Q: Czy mogę dostosować tekst znaku wodnego?**  
A: Oczywiście! Po prostu zamień ciąg znaków w metodzie `drawString` na pożądany tekst.

**Q: Co zrobić, jeśli chcę inną czcionkę?**  
A: Zmień inicjalizację `Font` na dowolną zainstalowaną czcionkę, np. `new Font("Times New Roman", 24.0f)`.

**Q: Czy istnieje sposób na regulację przezroczystości?**  
A: Tak — zmodyfikuj pierwszy parametr w `Color.fromArgb(alpha, r, g, b)`. Niższe wartości `alpha` zwiększają przezroczystość.

**Q: Czy mogę używać innych formatów obrazów poza PNG?**  
A: Oczywiście. Zastąp `new PngOptions()` przez `new JpegOptions()` lub `new BmpOptions()`, aby **save psd png** w innym formacie.

**Q: Gdzie mogę znaleźć więcej pomocy?**  
A: W przypadku szczegółowych pytań odwiedź [Aspose forums](https://forum.aspose.com/c/psd/34) lub sprawdź ich [documentation](https://reference.aspose.com/psd/java/).

## Podsumowanie
Nauczyłeś się teraz, jak **create image watermark** w pliku PSD przy użyciu Aspose.PSD for Java. Ta technika nie tylko zabezpiecza Twoje treści, ale także wzmacnia obecność marki we wszystkich zasobach wizualnych. Eksperymentuj z różnymi czcionkami, kolorami i poziomami przezroczystości, aby dopasować je do swojego stylu, i pamiętaj, że możesz **save psd png** lub **export psd png** do dowolnego potrzebnego formatu.

---

**Ostatnia aktualizacja:** 2026-03-07  
**Testowano z:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
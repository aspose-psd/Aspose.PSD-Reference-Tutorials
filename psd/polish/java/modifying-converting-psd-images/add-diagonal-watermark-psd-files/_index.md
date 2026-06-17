---
date: 2026-03-04
description: Dowiedz się, jak utworzyć obiekt graficzny w Javie i dodać przekątny
  znak wodny do plików PSD przy użyciu Aspose.PSD. Ten przewodnik krok po kroku opisuje
  użycie biblioteki znaków wodnych dla obrazów w Javie.
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: Tworzenie obiektu graficznego w Javie – Przekątny znak wodny dla PSD
url: /pl/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj przekątną znak wodny do plików PSD w Javie

## Wstęp
W tym samouczku **utworzysz obiekt graficzny w Javie** i użyjesz go do dodania przekątnego znaku wodnego do plików PSD. Niezależnie od tego, czy jesteś projektantem chroniącym swoją pracę, czy marketerem oznaczającym obrazy, czysty znak wodny może sprawić, że Twoje dzieło będzie wyglądało profesjonalnie i bezpiecznie. Przeprowadzimy Cię przez każdy krok z jasnymi wyjaśnieniami, abyś mógł szybko zastosować tę technikę w własnych projektach.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.PSD for Java (solidna biblioteka java do znakowania obrazów).  
- **Jakie główne słowo kluczowe obejmuje ten samouczek?** create graphics object java.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę zmienić tekst i styl znaku wodnego?** Tak – możesz dostosować czcionkę, kolor, krycie i obrót.  
- **Jakie formaty wyjściowe są obsługiwane?** Przykład zapisuje jako PNG, ale Aspose.PSD może eksportować do PSD, JPEG, BMP i innych.

## Co to jest obiekt Graphics w Javie?
Obiekt **Graphics** reprezentuje powierzchnię rysowania dla obrazu. Tworząc obiekt graficzny, zyskujesz dostęp do metod umożliwiających renderowanie tekstu, kształtów i innych elementów wizualnych bezpośrednio na bitmapie lub płótnie PSD. To podstawowa koncepcja stojąca za głównym słowem kluczowym **create graphics object java**.

## Dlaczego warto używać Aspose.PSD do znakowania?
Aspose.PSD to dedykowana **java image watermark library**, działająca bez Adobe Photoshop. Daje pełną kontrolę nad warstwami, renderowaniem tekstu i przekształceniami obrazu, co czyni ją idealną do przetwarzania po stronie serwera lub operacji wsadowych.

## Wymagania wstępne
Zanim przejdziemy do kodu, upewnij się, że masz następujące elementy:

### 1. Środowisko programistyczne Java
Zainstaluj najnowszy JDK ze [strony Java](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### 2. Biblioteka Aspose.PSD
Pobierz bibliotekę ze [strony pobierania Aspose](https://releases.aspose.com/psd/java/). Dodaj plik JAR do projektu za pomocą Maven, Gradle lub ręcznego dołączenia do classpath.

### 3. Podstawowa znajomość Javy
Znajomość klas, obiektów i operacji I/O ułatwi Ci śledzenie instrukcji.

### 4. Konfiguracja IDE
Użyj IntelliJ IDEA, Eclipse lub NetBeans, aby wygodnie pisać kod.

## Importowanie pakietów
Aby manipulować plikami PSD, zaimportuj wymagane klasy Aspose.PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Teraz, gdy mamy spełnione wymagania wstępne i zaimportowane niezbędne pakiety, przejdźmy przez kroki dodawania przekątnego znaku wodnego do pliku PSD.

## Krok 1: Przygotuj katalog
```java
String dataDir = "Your Document Directory";
```
Zastąp `"Your Document Directory"` ścieżką do folderu zawierającego źródłowy plik PSD.

## Krok 2: Załaduj plik PSD
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
Metoda `Image.load` odczytuje plik i rzutuje go na `PsdImage`, abyśmy mogli korzystać z funkcji specyficznych dla PSD.

## Krok 3: Utwórz obiekt Graphics
```java
Graphics graphics = new Graphics(psdImage);
```
Tutaj **create graphics object java** – płótno, na którym narysujemy znak wodny.

## Krok 4: Utwórz czcionkę dla znaku wodnego
```java
Font font = new Font("Arial", 20.0f);
```
Wybierz dowolną zainstalowaną czcionkę; rozmiar kontroluje widoczność znaku wodnego.

## Krok 5: Utwórz pędzel dla znaku wodnego
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
Wartość `alpha` (pierwszy parametr) określa przezroczystość. Alfa = 50 daje subtelny, półprzezroczysty efekt.

## Krok 6: Skonfiguruj macierz transformacji
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
Obracamy powierzchnię rysowania o 45° wokół środka obrazu, uzyskując efekt przekątnego znaku.

## Krok 7: Zdefiniuj wyrównanie tekstu
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
Wyrównanie centralne zapewnia, że znak wodny znajduje się ładnie w środku obróconego prostokąta.

## Krok 8: Narysuj znak wodny
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
Zastąp `"Some watermark text"` nazwą swojej marki lub informacją o prawach autorskich. Prostokąt określa, gdzie tekst zostanie wyrenderowany.

## Krok 9: Zapisz obraz
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
Wynik zostaje zapisany jako PNG, ale możesz wybrać dowolny format obsługiwany przez Aspose.PSD.

## Typowe przypadki użycia
- **Ochrona marki:** Dodaj półprzezroczyste logo, aby zapobiec nieautoryzowanemu wykorzystaniu.  
- **Przetwarzanie wsadowe:** Automatyzuj znakowanie dużych bibliotek obrazów na serwerze.  
- **Podglądy kreatywne:** Prezentuj klientom wersje z znakiem wodnym, pozostawiając oryginalne pliki nienaruszone.

## Rozwiązywanie problemów i wskazówki
- **Przezroczystość niewidoczna?** Zwiększ wartość alfa (np. `100`), aby znak był wyraźniejszy.  
- **Znak wodny jest przesunięty?** Upewnij się, że punkt obrotu używa dokładnego podziału szerokości/wysokości obrazu.  
- **Obawy o wydajność:** Ponownie używaj tego samego obiektu `Graphics` przy przetwarzaniu wielu obrazów w pętli.

## FAQ
### Co to jest Aspose.PSD?
Aspose.PSD to biblioteka Java służąca do pracy i manipulacji plikami PSD bez konieczności posiadania Adobe Photoshop.

### Czy mogę używać innych czcionek do znakowania?
Tak, możesz wybrać dowolną czcionkę zainstalowaną w systemie.

### Czy da się dostosować przezroczystość znaku wodnego?
Oczywiście! Możesz zmienić wartość alfa w obiekcie `SolidBrush`, aby regulować przezroczystość.

### Czy mogę dodać wiele znaków wodnych?
Tak, możesz wywołać metodę `drawString` wielokrotnie z różnymi parametrami, aby dodać kolejne znaki.

### Gdzie znajdę więcej informacji o Aspose.PSD?
Sprawdź dokumentację [tutaj](https://reference.aspose.com/psd/java/).

---

**Ostatnia aktualizacja:** 2026-03-04  
**Testowano z:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
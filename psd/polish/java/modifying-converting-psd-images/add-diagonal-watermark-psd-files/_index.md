---
title: Dodaj ukośny znak wodny do plików PSD za pomocą Java
linktitle: Dodaj ukośny znak wodny do plików PSD za pomocą Java
second_title: Aspose.PSD API Java
description: Dowiedz się, jak łatwo dodać ukośny znak wodny do plików PSD przy użyciu Java z Aspose.PSD. Przewodnik krok po kroku, jak pewnie poprawić swoje zdjęcia.
type: docs
weight: 12
url: /pl/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
---
## Wstęp
W dzisiejszym cyfrowym świecie posiadanie uderzającego obrazu może mieć ogromne znaczenie. Niezależnie od tego, czy jesteś projektantem chcącym chronić swoją pracę, czy marketerem chcącym dodać branding do obrazów, zastosowanie znaku wodnego jest niezbędne. W tym samouczku omówimy, jak dodać ukośny znak wodny do plików PSD przy użyciu Java i Aspose.PSD, potężnej biblioteki do manipulowania plikami PSD.
## Warunki wstępne
Zanim przejdziemy do ciekawej części kodowania, musisz upewnić się, że masz skonfigurowanych kilka rzeczy:
### 1. Środowisko programistyczne Java
 Upewnij się, że masz zainstalowaną Javę na swoim komputerze. Najnowszą wersję można pobrać ze strony[witryna internetowa Java](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
### 2. Biblioteka Aspose.PSD
 Do pracy z plikami PSD potrzebna jest biblioteka Aspose.PSD. Można go pobrać z[Strona z plikami do pobrania Aspose](https://releases.aspose.com/psd/java/)W zależności od struktury projektu możesz używać Mavena lub innego narzędzia do zarządzania zależnościami, więc możesz włączyć je zgodnie ze swoimi potrzebami.
### 3. Podstawowa znajomość języka Java
Solidna znajomość języka Java pomoże Ci bezproblemowo przejść przez ten samouczek. Upewnij się, że znasz klasy, obiekty i podstawową obsługę plików w Javie.
### 4. Konfiguracja IDE
Do kodowania używaj dowolnego zintegrowanego środowiska programistycznego (IDE), takiego jak IntelliJ IDEA, Eclipse lub NetBeans. To znacznie ułatwia kodowanie, nie sądzisz?
## Importuj pakiety
Aby manipulować plikami PSD, musisz zaimportować określone pakiety z Aspose.PSD. Oto pakiety, które musisz umieścić na górze pliku Java:
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
Teraz, gdy mamy już posortowane wymagania wstępne i zaimportowane niezbędne pakiety, przejdźmy przez kolejne kroki, aby dodać ukośny znak wodny do pliku PSD.
## Krok 1: Skonfiguruj swój katalog
```java
String dataDir = "Your Document Directory";
```
Najpierw musisz określić katalog, w którym znajdują się Twoje pliki PSD. Katalog ten będzie punktem wyjścia do ładowania obrazu. Więc wymień`"Your Document Directory"` z rzeczywistą ścieżką, w której znajduje się plik PSD.
## Krok 2: Załaduj plik PSD
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
 Teraz załadujemy plik PSD, z którym chcesz pracować. The`Image.load` Metoda odczytuje plik i rzutuje go do pliku`PsdImage` obiekt. Pamiętaj, aby podać dokładną nazwę pliku PSD, czyli w tym przypadku`"layers.psd"`.
## Krok 3: Utwórz obiekt graficzny
```java
Graphics graphics = new Graphics(psdImage);
```
 Na tym etapie tworzymy plik`Graphics` obiekt pozwalający na wykonanie operacji rysunkowych na wczytanym obrazie. Pomyśl o tym jak o przygotowaniu płótna, na którym możemy namalować nasz znak wodny.
## Krok 4: Utwórz czcionkę dla znaku wodnego
```java
Font font = new Font("Arial", 20.0f);
```
Tutaj definiujemy styl i rozmiar czcionki dla naszego tekstu znaku wodnego. W tym przypadku wybraliśmy Arial w rozmiarze 20. Możesz wybrać dowolną czcionkę zainstalowaną w Twoim systemie — dodaj trochę pikanterii!
## Krok 5: Utwórz pędzel dla znaku wodnego
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
 Następnie tworzymy`SolidBrush` obiekt, który pokoloruje nasz znak wodny. The`Color.fromArgb`metoda przyjmuje cztery parametry: alfa, czerwony, zielony i niebieski. Wartość alfa kontroluje przezroczystość (0 oznacza całkowicie przezroczyste, a 255 jest całkowicie nieprzezroczyste). Ustawiliśmy go na 50, aby uzyskać ładny efekt półprzezroczystości.
## Krok 6: Skonfiguruj macierz transformacji
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
 To tutaj dzieje się magia! Tworzymy macierz transformacji, aby obrócić znak wodny. The`rotateAt` funkcja przyjmuje dwa parametry: kąt (45 stopni dla wyglądu po przekątnej) i punkt, wokół którego należy obrócić (w naszym przypadku jest to środek obrazu).
## Krok 7: Zdefiniuj wyrównanie ciągu
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
 Musimy upewnić się, że nasz znak wodny jest wyśrodkowany. The`StringFormat` class nam w tym pomaga, wyrównując tekst idealnie na środku obrazu. W końcu kto lubi niechlujne miejsca docelowe?
## Krok 8: Narysuj znak wodny
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
 Teraz nadszedł czas, aby narysować znak wodny! Korzystanie z`drawString`metody, określamy zawartość naszego znaku wodnego (możesz dostosować tekst), czcionkę, pędzel, obszar, w którym chcemy go narysować, oraz ustawienie wyrównania. Twój znak wodny zostanie zastosowany przy użyciu parametrów, które ustawiliśmy w prostokącie!
## Krok 9: Zapisz obraz
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
 Na koniec zapisujemy nasz zmodyfikowany obraz. Tutaj eksportujemy go jako plik PNG. Pamiętaj, aby nadać plikowi wyjściowemu unikalną nazwę, aby nie nadpisał żadnych istniejących plików. The`PngOptions` class pomaga określić format obrazu.
## Wniosek
I tak właśnie udało Ci się dodać ukośny znak wodny do pliku PSD przy użyciu języka Java! Jest to prosty proces, ale może znacząco podnieść profesjonalizm Twoich zdjęć. Niezależnie od tego, czy chronisz swoją grafikę, czy promujesz swoją markę, znak wodny to proste, ale skuteczne rozwiązanie.

## Często zadawane pytania
### Co to jest Aspose.PSD?
Aspose.PSD to biblioteka Java używana do pracy z plikami PSD i manipulowania nimi bez konieczności stosowania programu Adobe Photoshop.
### Czy mogę używać innych czcionek do znakowania wodnego?
Tak, możesz wybrać dowolną czcionkę zainstalowaną w systemie do znakowania wodnego.
### Czy istnieje sposób na dostosowanie przezroczystości znaku wodnego?
Absolutnie! Można dostosować wartość alfa w SolidBrush, aby zmienić przezroczystość.
### Czy mogę dodać wiele znaków wodnych?
 Tak, możesz zadzwonić do`drawString` metodę wielokrotnie z różnymi parametrami, aby dodać więcej znaków wodnych.
### Gdzie mogę znaleźć więcej informacji na temat Aspose.PSD?
 Możesz sprawdzić dokumentację[Tutaj](https://reference.aspose.com/psd/java/).
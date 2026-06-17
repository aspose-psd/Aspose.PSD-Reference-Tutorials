---
date: 2026-03-21
description: Dowiedz się, jak konwertować pliki PSD na PNG i przycinać pliki PSD przy
  użyciu Aspose.PSD dla Javy. Ten przewodnik pokazuje krok po kroku przetwarzanie
  obrazów w aplikacjach Java.
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: Jak przekonwertować plik PSD na PNG przy jednoczesnym przycinaniu za pomocą
  Aspose.PSD dla Javy
url: /pl/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak konwertować psd na png przy jednoczesnym przycinaniu za pomocą Aspose.PSD dla Javy

## Wprowadzenie
W dynamicznym świecie programowania w Javie opanowanie efektywnego przetwarzania obrazów jest kluczowe. W tym samouczku dowiesz się **jak konwertować psd na png** i przyciąć obraz w jednym przepływie pracy, korzystając z potężnej biblioteki Aspose.PSD dla Javy. Po zakończeniu tego przewodnika krok po kroku będziesz w stanie dodać precyzyjne przycinanie do eksportów PNG i sprawić, że Twoje aplikacje Java będą pewnie obsługiwać zasoby PSD.

## Szybkie odpowiedzi
- **Co robi kod?** Ładuje plik PSD, przycina prostokąt i zapisuje go jako PNG.  
- **Jakiej biblioteki potrzebujesz?** Aspose.PSD dla Javy (najnowsza wersja).  
- **Czy potrzebna jest licencja?** Tak, wymagana jest licencja komercyjna do użytku produkcyjnego.  
- **Czy mogę zdefiniować dowolny obszar przycięcia?** Oczywiście – ustawiasz wartości X, Y, szerokość i wysokość, które są Ci potrzebne.  
- **Czy to podejście jest szybkie dla dużych plików?** Tak, Aspose.PSD jest zoptymalizowane pod kątem wysokowydajnego przetwarzania.

## Co to jest konwersja psd na png?
Konwersja PSD na PNG oznacza wzięcie warstwowego dokumentu Photoshop i spłaszczenie go do bezstratnego obrazu PNG. Ten format jest idealny do dostarczania w sieci, miniatur lub wszelkich scenariuszy, w których potrzebny jest obraz rastrowy bez oryginalnych warstw.

## Dlaczego przycinać PSD przed konwersją na PNG?
Przycinanie pozwala wyodrębnić tylko tę część projektu, której potrzebujesz, zmniejszając rozmiar pliku i koncentrując się na istotnej treści wizualnej. Jest to szczególnie przydatne przy generowaniu miniatur, zasobów UI lub przygotowywaniu obrazów do responsywnych układów.

## Wymagania wstępne
Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania:
- Podstawowa znajomość programowania w Javie.  
- Zainstalowany Java Development Kit (JDK).  
- Biblioteka Aspose.PSD dla Javy pobrana i dodana do projektu.  
- Przykładowy plik PSD do eksperymentów.

## Importowanie pakietów
W swoim projekcie Java upewnij się, że importujesz niezbędne pakiety do korzystania z funkcjonalności Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Konfiguracja projektu
Rozpocznij od utworzenia projektu Java i dodania biblioteki Aspose.PSD dla Javy do ścieżki klas projektu. Dzięki temu uzyskasz dostęp do wszystkich klas przetwarzania obrazu, których będziesz potrzebować.

## Krok 2: Ładowanie obrazu PSD
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*Tutaj ładujemy źródłowy plik PSD do obiektu `RasterImage`, który zapewnia operacje oparte na rastrze, takie jak przycinanie.*

## Krok 3: Definiowanie obszaru przycięcia
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*Obiekt `Rectangle` definiuje obszar, który chcesz zachować. Dostosuj wartości `x`, `y`, `width` i `height` do swojego projektu. Ten krok bezpośrednio odpowiada na frazę „define crop region”.*

## Krok 4: Przycinanie obrazu PSD
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*Wywołanie `crop` modyfikuje obraz w pamięci, usuwając wszystko poza określonym prostokątem.*

## Krok 5: Ustawienie opcji eksportu PNG
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` pozwala kontrolować ustawienia specyficzne dla PNG, takie jak poziom kompresji, typ koloru i inne.*

## Krok 6: Zapis przyciętego obrazu jako PNG
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*Metoda `save` wykonuje operację **convert psd to png** jednocześnie zachowując zdefiniowane przycięcie.*

## Typowe pułapki i wskazówki
- **Nieprawidłowe wymiary prostokąta:** Upewnij się, że szerokość i wysokość nie przekraczają rozmiaru oryginalnego obrazu, w przeciwnym razie zostanie zgłoszony wyjątek.  
- **Zużycie pamięci przy dużych PSD:** Po zapisaniu zwolnij zasoby natywne, wywołując `image.dispose()` na obiekcie `RasterImage`.  
- **Brak ustawionej licencji:** Jeśli uruchomisz kod bez ważnej licencji, na wyjściowym PNG pojawi się znak wodny.

## Najczęściej zadawane pytania
### Czy mogę przycinać pliki PSD o nieregularnych kształtach za pomocą Aspose.PSD dla Javy?
Tak, Aspose.PSD dla Javy pozwala zdefiniować własny obszar przycięcia, umożliwiając przycinanie obrazów do różnych kształtów.

### Czy Aspose.PSD dla Javy nadaje się do przetwarzania obrazów w dużej skali?
Zdecydowanie! Aspose.PSD jest zaprojektowane tak, aby efektywnie obsługiwać duże obrazy, co czyni je idealnym rozwiązaniem dla projektów wymagających intensywnego przetwarzania obrazów.

### Czy potrzebuję licencji na Aspose.PSD dla Javy?
Tak, wymagana jest ważna licencja do użytku komercyjnego. Możesz ją uzyskać na stronie [Aspose Purchase](https://purchase.aspose.com/buy).

### Jak mogę uzyskać pomoc lub zgłosić problemy z Aspose.PSD dla Javy?
Odwiedź [forum Aspose.PSD](https://forum.aspose.com/c/psd/34), aby uzyskać pomoc, podzielić się doświadczeniami i zgłosić napotkane problemy.

### Czy mogę wypróbować Aspose.PSD dla Javy przed zakupem?
Oczywiście! Zapoznaj się z funkcjami biblioteki, korzystając z darmowej wersji próbnej dostępnej [tutaj](https://releases.aspose.com/).

---

**Ostatnia aktualizacja:** 2026-03-21  
**Testowano z:** Aspose.PSD dla Javy 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
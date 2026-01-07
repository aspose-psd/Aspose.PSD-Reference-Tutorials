---
date: 2026-01-07
description: Dowiedz się, jak przycinać obrazy w Javie przy użyciu Aspose.PSD for
  Java. Przewodnik krok po kroku dotyczący przycinania obrazów, zmiany rozmiaru i
  konwersji z PSD do JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Przycinanie obrazu w Javie: Rozszerzanie i przycinanie obrazów przy użyciu
  Aspose.PSD dla Javy'
url: /pl/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Przycinanie obrazu Java: Rozszerzanie i przycinanie obrazów przy użyciu Aspose.PSD dla Java

## Wprowadzenie

W tym samouczku dowiesz się, jak **przycinać obraz java** przy użyciu biblioteki Aspose.PSD. Niezależnie od tego, czy potrzebujesz rozszerzyć płótno, odciąć niechciane krawędzie, czy przekonwertować plik PSD na JPEG, poniższe kroki poprowadzą Cię przez czysty, powtarzalny proces. Omówimy wymagania wstępne, instrukcje importu oraz każdy krok kodowania z jasnymi wyjaśnieniami, abyś mógł zastosować tę technikę w rzeczywistych projektach.

## Szybkie odpowiedzi
- **Jakiej biblioteki używać do przycinania obrazu java?** Aspose.PSD for Java.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna wystarczy do testów; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę konwertować PSD na JPEG jednocześnie przycinając?** Tak, używając `JpegOptions` razem z prostokątem przycinania.  
- **Czy Java 8 jest obsługiwana?** Aspose.PSD obsługuje Java 8 i nowsze wersje.  
- **Jak długo trwa implementacja?** Zazwyczaj mniej niż 10 minut dla podstawowego przycięcia.

## Co to jest „crop image java”?

Przycinanie obrazu w Javie oznacza wybranie prostokątnego obszaru źródłowego obrazu i odrzucenie pozostałej części. Dzięki Aspose.PSD możesz zdefiniować ten obszar przy pomocy obiektu `Rectangle`, a następnie zapisać wynik w innym formacie, np. JPEG.

## Dlaczego warto używać Aspose.PSD dla przycinania obrazów w Javie?

- **Pełne wsparcie PSD** – pracuj bezpośrednio z warstwowymi plikami PSD, bez konieczności ich konwersji.  
- **Wysokowydajne przetwarzanie rastra** – efektywne wykorzystanie pamięci przy dużych obrazach.  
- **Wbudowana konwersja** – łatwo eksportuj do JPEG, PNG, BMP itp., jednocześnie stosując przycinanie lub rozszerzanie płótna.  
- **Wieloplatformowość** – działa na każdym systemie, na którym uruchomiona jest Java.

## Wymagania wstępne

Zanim przejdziesz do kodu, upewnij się, że masz:

1. **Java Development Kit (JDK)** – zainstalowaną Javę 8 lub nowszą.  
2. **Aspose.PSD for Java** – pobierz bibliotekę ze strony **[tutaj](https://releases.aspose.com/psd/java/)**.  

> **Wskazówka:** Dodaj plik JAR Aspose.PSD do classpath projektu lub jako zależność Maven/Gradle, aby uniknąć `ClassNotFoundException`.

## Importowanie pakietów

Dodaj wymagane importy do swojego pliku źródłowego Java. Te klasy dają dostęp do ładowania obrazu, manipulacji rastrem, definiowania prostokąta oraz opcji eksportu JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 1: Ustaw katalog dokumentu

Określ folder zawierający źródłowy plik PSD. Zamień symboliczny placeholder na rzeczywistą ścieżkę w swoim systemie.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Określ ścieżki źródłowe i docelowe

Zdefiniuj, skąd odczytać plik PSD i gdzie zapisać przycięty JPEG.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Krok 3: Załaduj i zbuforuj obraz

Wczytaj PSD do obiektu `RasterImage`. Buforowanie poprawia wydajność przy kolejnych operacjach, takich jak przycinanie.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Krok 4: Utwórz prostokąt przycinania

Utwórz `Rectangle`, który opisuje region, który chcesz zachować. Współrzędne mogą być ujemne, aby **rozszerzyć** płótno przed przycięciem – przydatne przy dodawaniu obramowania wokół oryginalnego obrazu.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Dlaczego używać ujemnych współrzędnych?**  
> Ujemne wartości X/Y przesuwają obszar przycinania w lewo/górę, skutecznie dodając pustą przestrzeń (rozszerzając) wokół oryginalnej zawartości przed ostatecznym przycięciem.

## Krok 5: Zapisz przycięty obraz

Na koniec zapisz wynikowy obraz przy użyciu `JpegOptions`. Ten krok jednocześnie demonstruje **convert psd jpeg** przy zastosowaniu prostokąta przycinania.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Rezultat:** `jpeg_out.jpg` zawiera teraz obraz 300 × 300 px, który został rozszerzony o 200 px po każdej stronie, a następnie przycięty do zdefiniowanego prostokąta.

Gratulacje! Pomyślnie wykonałeś **java image cropping**, rozszerzyłeś płótno i przekonwertowałeś plik PSD na JPEG – wszystko w kilku zwięzłych linijkach kodu.

## Typowe scenariusze użycia

- **Przygotowywanie zasobów dla sieci** – przycinaj i zmieniaj rozmiar zrzutów ekranu lub projektów przed ich publikacją.  
- **Generowanie miniatur** – wyodrębnij określony fragment dużego PSD w celu podglądu.  
- **Automatyczne przetwarzanie wsadowe** – iteruj po folderze plików PSD, stosując ten sam prostokąt przycinania do każdego z nich.

## Rozwiązywanie problemów i wskazówki

| Problem | Sugerowane rozwiązanie |
|-------|----------------|
| `OutOfMemoryError` przy ładowaniu dużych PSD | Wywołaj `rasterImage.cacheData()` wcześnie i rozważ zwiększenie rozmiaru sterty JVM (`-Xmx`). |
| Przycięty obszar jest przesunięty | Sprawdź offsety X/Y prostokąta; pamiętaj, że ujemne wartości rozszerzają płótno. |
| Wyjściowy JPEG jest rozmyty | Dostosuj ustawienie jakości w `JpegOptions` (np. `new JpegOptions { Quality = 90 }`). |

## Najczęściej zadawane pytania

### Q1: Czy Aspose.PSD jest kompatybilny z różnymi wersjami Java?

A1: Tak, Aspose.PSD obsługuje różne wersje Java, zapewniając zgodność z szerokim zakresem środowisk programistycznych.

### Q2: Czy mogę używać Aspose.PSD w projektach komercyjnych?

A2: Oczywiście, Aspose.PSD oferuje licencje komercyjne dla deweloperów, umożliwiając jego użycie zarówno w projektach prywatnych, jak i komercyjnych.

### Q3: Czy istnieją ograniczenia dotyczące obsługiwanych formatów plików obrazów?

A3: Aspose.PSD obsługuje wiele formatów plików graficznych, w tym PSD, JPEG, PNG i inne. Pełną listę znajdziesz w [dokumentacji](https://reference.aspose.com/psd/java/).

### Q4: Jak mogę uzyskać wsparcie w sprawach związanych z Aspose.PSD?

A4: Odwiedź [forum Aspose.PSD](https://forum.aspose.com/c/psd/34), aby uzyskać pomoc od społeczności lub zespołu wsparcia Aspose.

### Q5: Czy dostępna jest darmowa wersja próbna?

A5: Tak, możesz wypróbować Aspose.PSD w wersji trial. Pobierz ją [tutaj](https://releases.aspose.com/).

---

**Ostatnia aktualizacja:** 2026-01-07  
**Testowano z:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
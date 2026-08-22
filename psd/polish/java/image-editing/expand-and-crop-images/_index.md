---
date: 2026-07-08
description: 'Poradnik Java Image Editing Library: dowiedz się, jak crop image java
  przy użyciu Aspose.PSD for Java, resize, expand canvas i convert PSD to JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Expand i Crop Images
og_description: Poradnik Java Image Editing Library pokazuje, jak crop, expand canvas
  i convert PSD to JPEG przy użyciu Aspose.PSD for Java w kilka minut.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java Image Editing Library – Crop Image with Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java Image Editing Library – Crop Image with Aspose.PSD
url: /pl/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Biblioteka do edycji obrazów Java: przycinanie obrazu w Javie z Aspose.PSD

## Wprowadzenie

W tym samouczku dowiesz się, jak używać **java image editing library** — konkretnie Aspose.PSD dla Javy — do przycinania, rozszerzania i konwertowania plików PSD na JPEG. Niezależnie od tego, czy przygotowujesz zasoby dla portalu internetowego, czy automatyzujesz generowanie miniatur, poniższe kroki zapewniają powtarzalny, gotowy do produkcji przepływ pracy, który możesz zintegrować z dowolnym projektem Java 8+.

## Szybkie odpowiedzi
- **Jaka biblioteka obsługuje przycinanie obrazu w Javie?** Aspose.PSD for Java.  
- **Czy potrzebuję licencji do rozwoju?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę konwertować PSD na JPEG podczas przycinania?** Tak, używając `JpegOptions` razem z prostokątem przycinania.  
- **Czy Java 8 jest obsługiwana?** Aspose.PSD obsługuje Javę 8 i nowsze wersje.  
- **Jak długo trwa implementacja?** Zazwyczaj mniej niż 10 minut dla podstawowej operacji przycinania.

## Co to jest „crop image java”?

Crop image java oznacza wybranie prostokątnego obszaru źródłowego obrazu i odrzucenie wszystkiego poza tym obszarem. Z Aspose.PSD tworzysz `Rectangle`, który definiuje obszar, stosujesz go do `RasterImage`, a następnie zapisujesz wynik w dowolnym obsługiwanym formacie, takim jak JPEG.

## Dlaczego warto używać Aspose.PSD do przycinania obrazów w Javie?

Aspose.PSD zapewnia **java image editing library**, które obsługuje pliki PSD natywnie, wspiera ponad 100 funkcji warstw i może przetwarzać obrazy do 10 000 × 10 000 pikseli, utrzymując zużycie pamięci poniżej 500 MB. Oferuje także wbudowaną konwersję do JPEG, PNG, BMP i innych, bez potrzeby używania zewnętrznych narzędzi. Dzięki temu potoki przetwarzania wsadowego są szybkie, niezawodne i łatwe w utrzymaniu.

## Wymagania wstępne

1. **Java Development Kit (JDK)** – Zainstalowany Java 8 lub nowszy.  
2. **Aspose.PSD for Java** – pobierz bibliotekę z oficjalnej strony **[here](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** Dodaj plik JAR Aspose.PSD do classpath projektu lub zależności Maven/Gradle, aby uniknąć `ClassNotFoundException`.

## Importowanie pakietów

Dodaj wymagane importy do swojego pliku źródłowego Java. Te klasy zapewniają dostęp do ładowania obrazów, manipulacji rastrami, definiowania prostokątów oraz opcji eksportu JPEG.

## Jak przycinać obraz w Javie przy użyciu Aspose.PSD?

Wczytaj źródłowy plik PSD za pomocą `RasterImage`, zdefiniuj `Rectangle` opisujący obszar przycięcia (ujemne współrzędne mogą rozszerzyć płótno), a na końcu zapisz wynik przy użyciu `JpegOptions`. Ten trzyetapowy przepływ obsługuje zarówno przycinanie, jak i konwersję formatu w jednym przebiegu, eliminując potrzebę plików pośrednich.

## Krok 1: Ustaw katalog dokumentu

Określ folder zawierający źródłowy plik PSD. Zastąp placeholder rzeczywistą ścieżką na swoim komputerze.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 2: Określ ścieżki źródłową i docelową

Określ, skąd odczytać plik PSD i gdzie zapisać przycięty JPEG.

```java
String dataDir = "Your Document Directory";
```

## Krok 3: Wczytaj i buforuj obraz

`RasterImage` reprezentuje rasteryzowaną wersję pliku PSD w pamięci.  
Wczytaj PSD do obiektu `RasterImage`. Buforowanie poprawia wydajność kolejnych operacji, takich jak przycinanie.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Krok 4: Utwórz prostokąt do przycinania

`Rectangle` definiuje współrzędne X, Y oraz szerokość/wysokość obszaru przycinania.  
Utwórz `Rectangle`, który opisuje region, który chcesz zachować. Współrzędne mogą być ujemne, aby **rozszerzyć** płótno przed przycięciem, co jest przydatne przy dodawaniu obramowania wokół oryginalnego obrazu.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Dlaczego używać ujemnych współrzędnych?**  
> Ujemne wartości X/Y przesuwają obszar przycinania w lewo/górę, skutecznie dodając pustą przestrzeń (rozszerzając) wokół oryginalnej zawartości przed ostatecznym przycięciem.

## Krok 5: Zapisz przycięty obraz

`JpegOptions` określa ustawienia wyjścia JPEG, takie jak jakość i kompresja.  
Na koniec zapisz powstały obraz przy użyciu `JpegOptions`. Ten krok również demonstruje **convert psd jpeg** podczas stosowania prostokąta przycinania.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Wynik:** `jpeg_out.jpg` teraz zawiera obraz o wymiarach 300 × 300 pikseli, który został rozszerzony o 200 px po każdej stronie, a następnie przycięty do zdefiniowanego prostokąta.

Gratulacje! Pomyślnie wykonałeś **java image cropping**, rozszerzyłeś płótno i skonwertowałeś plik PSD na JPEG — wszystko w kilku zwięzłych linijkach kodu.

## Typowe przypadki użycia

- **Preparing assets for web** – przycinaj i zmieniaj rozmiar zrzutów ekranu lub projektów przed ich przesłaniem.  
- **Generating thumbnails** – wyodrębnij konkretny region z dużego pliku PSD w celu podglądu.  
- **Automated batch processing** – przetwarzaj folder z plikami PSD, stosując ten sam prostokąt przycinania do każdego.

## Rozwiązywanie problemów i wskazówki

| Problem | Sugerowane rozwiązanie |
|-------|----------------|
| `OutOfMemoryError` podczas ładowania dużych plików PSD | Wywołaj `rasterImage.cacheData()` wcześnie i rozważ zwiększenie rozmiaru sterty JVM (`-Xmx`). |
| Obszar przycięcia jest niecentralny | Sprawdź przesunięcia X/Y prostokąta; pamiętaj, że ujemne wartości rozszerzają płótno. |
| Wyjściowy JPEG jest rozmyty | Dostosuj ustawienie jakości w `JpegOptions` (np. `new JpegOptions { Quality = 90 }`). |

## Najczęściej zadawane pytania

### Q1: Czy Aspose.PSD jest kompatybilny z różnymi wersjami Java?
A1: Tak, Aspose.PSD obsługuje Javę 8, 11, 17 i nowsze wydania, zapewniając szeroką kompatybilność w różnych środowiskach programistycznych.

### Q2: Czy mogę używać Aspose.PSD w projektach komercyjnych?
A2: Oczywiście, Aspose.PSD oferuje licencje komercyjne dla programistów, umożliwiając jego użycie zarówno w aplikacjach prywatnych, jak i komercyjnych.

### Q3: Czy istnieją ograniczenia dotyczące obsługiwanych formatów plików graficznych?
A3: Aspose.PSD obsługuje ponad 30 formatów graficznych, w tym PSD, JPEG, PNG, BMP, TIFF i inne. Zobacz [documentation](https://reference.aspose.com/psd/java/) po pełną listę.

### Q4: Jak mogę uzyskać wsparcie w kwestiach związanych z Aspose.PSD?
A4: Odwiedź [Aspose.PSD forum](https://forum.aspose.com/c/psd/34), aby uzyskać pomoc od społeczności lub zespołu wsparcia Aspose.

### Q5: Czy dostępna jest darmowa wersja próbna?
A5: Tak, możesz wypróbować Aspose.PSD w wersji próbnej. Pobierz ją [here](https://releases.aspose.com/).

**Ostatnia aktualizacja:** 2026-07-08  
**Testowano z:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Powiązane samouczki

- [Proste skalowanie z Aspose.PSD – Biblioteka do manipulacji obrazami w Javie](/psd/java/basic-image-operations/simple-resizing/)
- [Jak obrócić obraz o 270 stopni przy użyciu Aspose.PSD dla Javy](/psd/java/advanced-image-manipulation/rotate-image/)
- [Jak dostosować gamma w przetwarzaniu obrazów w Javie z Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
---
date: 2026-03-13
description: Dowiedz się, jak tworzyć miniatury PSD w Javie przy użyciu Aspose.PSD.
  Skorzystaj z naszego krok po kroku przewodnika, aby szybko generować miniatury z
  plików PSD.
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: Tworzenie miniatur PSD w Javie – Generowanie miniatur z plików PSD
url: /pl/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

 all text content. So translate "Last Updated:" to "Ostatnia aktualizacja:", "Tested With:" to "Testowano z:", "Author:" to "Autor:". Keep dates and names.

Now produce final content with same markdown.

We must ensure we keep all shortcodes and code blocks placeholders unchanged.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz miniaturkę PSD w Javie – Generuj miniaturki z plików PSD

## Wprowadzenie
Jeśli potrzebujesz **kod Java do tworzenia miniaturki PSD**, który wyodrębnia obrazy podglądu z plików Photoshop, trafiłeś we właściwe miejsce. Niezależnie od tego, czy tworzysz menedżer zasobów cyfrowych, galerię internetową, czy zautomatyzowany potok przetwarzania wsadowego, generowanie miniatur z plików PSD może znacząco poprawić wydajność i doświadczenie użytkownika. W tym samouczku przeprowadzimy Cię przez cały proces przy użyciu Aspose.PSD for Java, pokazując, jak załadować PSD, zlokalizować wbudowane zasoby miniatur i zapisać je jako oddzielne pliki graficzne.

## Szybkie odpowiedzi
- **Jaka biblioteka jest najlepsza do wyodrębniania miniatur PSD?** Aspose.PSD for Java.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowej konfiguracji.  
- **Czy potrzebny jest zainstalowany Photoshop?** Nie, Aspose.PSD działa niezależnie.  
- **Do jakich formatów obrazów mogę wyeksportować miniaturkę?** Każdy format obsługiwany przez Aspose.PSD (np. BMP, PNG, JPEG).  
- **Czy wymagana jest licencja do produkcji?** Tak, do użytku produkcyjnego potrzebna jest licencja komercyjna.

## Co to jest „create PSD thumbnail Java”?
Tworzenie miniaturki PSD w Javie oznacza programowe odczytanie podglądu miniatury przechowywanego wewnątrz dokumentu Photoshop (PSD) i zapisanie go jako oddzielny plik graficzny. Jest to przydatne do generowania szybkich podglądów bez ładowania pełnej, często dużej, zawartości PSD.

## Dlaczego używać Aspose.PSD do tego zadania?
- **Brak zależności od Photoshopa:** Działa na każdej platformie z JDK.  
- **Pełne wsparcie PSD:** Obsługuje wszystkie wersje i zasoby PSD, w tym miniatury.  
- **Proste API:** Kilka linii kodu wystarczy, aby wyodrębnić i zapisać miniatury.  
- **Optymalizacja wydajności:** Efektywne zarządzanie pamięcią przy dużych plikach.

## Wymagania wstępne
Zanim przejdziemy do szczegółów tworzenia miniatur, omówmy, co będzie potrzebne.

### Środowisko programistyczne Java
- **Java JDK:** Upewnij się, że masz zainstalowany Java Development Kit (JDK). Możesz go pobrać [tutaj](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
- **IDE:** Zintegrowane środowisko programistyczne (IDE) takie jak IntelliJ IDEA, Eclipse lub NetBeans ułatwi kodowanie.

### Biblioteka Aspose.PSD
- Musisz dołączyć bibliotekę Aspose.PSD do swojego projektu. Możesz [pobrać najnowszą wersję tutaj](https://releases.aspose.com/psd/java/).

### Podstawowa znajomość Javy
- Znajomość podstaw Javy pomoże Ci lepiej zrozumieć przykładowy kod. Koncepcje takie jak klasy, obiekty i pętle będą używane często.

## Importowanie pakietów
Rozpocznij od zaimportowania niezbędnych klas z biblioteki Aspose.PSD. Ten krok jest kluczowy, ponieważ umożliwia korzystanie z funkcjonalności biblioteki w Twoim kodzie.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

Po spełnieniu wymagań możemy przejść do głównego tematu! Tworzenie miniatur z plików PSD obejmuje kilka prostych kroków, które teraz szczegółowo opiszę.

## Jak utworzyć miniaturkę PSD w Javie – przewodnik krok po kroku

### Krok 1: Przygotuj środowisko
Oto jak zainicjować projekt i przygotować się do generowania miniatur.

1. **Utwórz projekt Java**  
   - Otwórz swoje IDE i utwórz nowy projekt Java.  
   - Nazwij go np. `"PsdThumbnailGenerator"`.

2. **Dołącz bibliotekę Aspose.PSD**  
   - Dodaj plik JAR Aspose.PSD do ścieżki kompilacji projektu.  
   - Jeśli używasz Maven, umieść go w pliku `pom.xml`:

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### Krok 2: Załaduj plik PSD
Następnie musimy załadować plik PSD, z którego chcemy utworzyć miniatury.

1. **Określ katalog dokumentu**  
   Zdefiniuj katalog, w którym znajduje się Twój plik PSD.

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **Załaduj plik PSD**  
   Użyj klasy `PsdImage`, aby wczytać plik PSD.

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **Pro tip:** Przechowuj pliki PSD w dedykowanym folderze (np. `src/main/resources`), aby uniknąć problemów ze ścieżkami.

### Krok 3: Iteruj po zasobach PSD
Teraz, gdy nasz obraz PSD jest załadowany, kolejnym krokiem jest przejrzenie jego zasobów.

1. **Pobierz liczbę zasobów**  
   Przejdziemy pętlą po wszystkich zasobach w pliku PSD.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **Zidentyfikuj zasoby miniatur**  
   Wewnątrz pętli sprawdź, czy zasób jest miniaturą.

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### Krok 4: Przetwórz miniaturkę
Gdy zidentyfikujemy zasób miniatury, musimy go odpowiednio obsłużyć.

1. **Pobierz i sprawdź format miniaturki**  
   Jeśli zasób jest rzeczywiście miniaturą, pobierz go i sprawdź jego format.

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### Krok 5: Utwórz i zapisz miniaturkę
Tutaj dzieje się magia! Utworzymy nowy obraz z danych miniatury i zapiszemy go.

1. **Utwórz nowy obraz**  
   Użyjemy szerokości i wysokości zasobu miniatury, aby stworzyć nowy obraz bitmapowy.

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **Zapisz piksele w nowym obrazie**  
   Przenieś dane miniatury do nowo utworzonego obrazu.

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **Zapisz obraz miniaturki**  
   Na koniec zapisz obraz miniaturki w katalogu dokumentu pod unikalną nazwą.

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **Common pitfall:** Zapominanie o zamknięciu obiektów `PsdImage` może prowadzić do wycieków pamięci. Owiń kod obsługujący obrazy w blok `try‑with‑resources`, jeśli używasz Java 7+.

## Podsumowanie
Postępując zgodnie z tymi krokami, masz teraz solidny, wielokrotnego użytku sposób na **implementację tworzenia miniatur PSD w Javie**, który wyodrębnia obrazy podglądu z dowolnego pliku Photoshop. Technika ta może być zintegrowana z procesorami wsadowymi, usługami internetowymi lub aplikacjami desktopowymi, aby przyspieszyć katalogowanie obrazów i poprawić responsywność interfejsu użytkownika. Wypróbuj ją na własnej kolekcji PSD i zobacz, jak szybko możesz generować lekkie podglądy!

## FAQ's
### Co to jest Aspose.PSD?
Aspose.PSD to biblioteka Java, która umożliwia programistom pracę z plikami Photoshop, ułatwiając programowe manipulowanie i zarządzanie plikami PSD.

### Czy mogę używać Aspose.PSD za darmo?
Tak, Aspose oferuje bezpłatną wersję próbną, którą możesz wykorzystać do przetestowania biblioteki przed zakupem licencji.

### W jakich formatach mogę zapisać miniaturki?
W tym przykładzie zapisaliśmy miniaturki w formacie BMP, ale Aspose.PSD obsługuje także wiele innych formatów.

### Czy potrzebny jest Photoshop, aby używać Aspose.PSD?
Nie, Aspose.PSD działa niezależnie od Photoshopa.

### Gdzie mogę znaleźć więcej informacji o Aspose.PSD?
Możesz zajrzeć do [dokumentacji Aspose.PSD](https://reference.aspose.com/psd/java/), aby uzyskać więcej szczegółów, samouczków i zasobów.

## Często zadawane pytania

**Q: Jak wyodrębnić miniatury z PSD chronionego hasłem?**  
A: Załaduj PSD przy użyciu odpowiedniej przeciążonej metody `Image.load`, która przyjmuje parametr hasła.

**Q: Czy mogę generować miniaturki w PNG zamiast BMP?**  
A: Oczywiście. Zmień rozszerzenie pliku w metodzie `save`, a Aspose.PSD zajmie się konwersją.

**Q: Czy istnieje sposób na przetwarzanie wsadowe wielu plików PSD?**  
A: Umieść kod w pętli, która iteruje po katalogu z plikami PSD, ponownie wykorzystując tę samą logikę wyodrębniania dla każdego pliku.

**Q: Jakiej wersji Javy wymaga biblioteka?**  
A: Aspose.PSD obsługuje Java 8 i nowsze. Zaleca się użycie najnowszego JDK pod kątem wydajności i bezpieczeństwa.

**Q: Czy biblioteka radzi sobie efektywnie z dużymi plikami PSD?**  
A: Tak, Aspose.PSD wykorzystuje leniwe ładowanie i zoptymalizowane zarządzanie pamięcią, aby pracować z dużymi plikami bez wyczerpywania pamięci heap.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-03-13  
**Testowano z:** Aspose.PSD 24.11 for Java (najnowsza w momencie pisania)  
**Autor:** Aspose  

---
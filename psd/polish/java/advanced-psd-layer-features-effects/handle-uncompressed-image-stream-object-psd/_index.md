---
date: 2026-02-17
description: Dowiedz się, jak eksportować PSD do PNG i obsługiwać nieskompresowane
  strumienie obrazu przy użyciu Aspose.PSD dla Javy.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Eksportuj PSD do PNG – Utwórz obiekt graficzny PSD – Nieskompresowany strumień
  w Javie
url: /pl/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj PSD do PNG – Utwórz obiekt graficzny PSD – Niekompresowany strumień w Javie

## Wprowadzenie
Witamy w świecie manipulacji obrazami w Javie! W tym samouczku **utworzysz obiekt graficzny PSD**, obsłużysz niekompresowane strumienie obrazu i nauczysz się **eksportować PSD do PNG** przy użyciu Aspose.PSD for Java. Niezależnie od tego, czy jesteś projektantem graficznym chcącym zautomatyzować swoje procesy, czy programistą, który chce zintegrować potężne możliwości przetwarzania obrazów w swoich aplikacjach, ten przewodnik jest właśnie dla Ciebie. Przejdziemy przez wszystko, od wymagań wstępnych po ostateczny eksport, zapewniając solidne zrozumienie całego procesu.

## Szybkie odpowiedzi
- **Co oznacza „utwórz obiekt graficzny PSD”?** Odnosi się to do zainicjowania kontekstu graficznego dla pliku PSD, aby można było rysować lub edytować jego zawartość.  
- **Która biblioteka obsługuje niekompresowane strumienie?** Aspose.PSD for Java zapewnia pełne wsparcie dla surowych (niekompresowanych) danych obrazu.  
- **Czy mogę wyeksportować PSD do PNG po edycji?** Tak — po uzyskaniu obiektu `Graphics` możesz renderować PSD i zapisać go jako PNG.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna wystarczy do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy eksport jest bezstratny?** Eksport do PNG zachowuje jakość obrazu, przy czym rozmiar pliku jest większy niż w przypadku JPEG, ale mniejszy niż w niekompresowanym PSD.  

## Jak wyeksportować PSD do PNG przy użyciu Aspose.PSD for Java
Gdy potrzebujesz **wyeksportować PSD do PNG**, typowy przepływ pracy wygląda następująco:

1. Załaduj plik PSD (lub utwórz nowy).  
2. Wykonaj dowolne rysowanie lub manipulację warstwami przy użyciu obiektu `Graphics`.  
3. Zapisz wynikowy obraz przy użyciu `PngOptions` (ten sam obiekt `Graphics` może być ponownie użyty).  

Choć ten samouczek koncentruje się na obsłudze niekompresowanych strumieni, ten sam obiekt `Graphics`, który utworzysz, może być później użyty do renderowania PSD do pliku PNG w Twoim potoku.

## Wymagania wstępne
Zanim przejdziemy do kodu, upewnijmy się, że masz wszystko, co potrzebne, aby rozpocząć tę podróż. Oto wymagania wstępne:

### Java Development Kit (JDK)
Upewnij się, że masz zainstalowany JDK na swoim komputerze. Możesz go pobrać ze strony Oracle lub użyć OpenJDK.

### Aspose.PSD for Java
Musisz pobrać i zainstalować bibliotekę Aspose.PSD. Ta potężna biblioteka umożliwia łatwą manipulację plikami PSD. Najnowszą wersję możesz uzyskać z [tego linku](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Warto używać IDE do pisania i testowania kodu Java. Możesz wybrać IntelliJ IDEA, Eclipse lub dowolne inne, które odpowiada Twoim preferencjom.

### Podstawowa znajomość Javy
Znajomość programowania w Javie ułatwi ten proces. Upewnij się, że rozumiesz podstawy, takie jak klasy, metody i obsługa wyjątków.

Mając wszystko gotowe, zakasaj rękawy i przejdźmy do ekscytującej części — kodowania!

## Importowanie pakietów
Aby rozpocząć, musimy zaimportować niezbędne pakiety do pracy z Aspose.PSD. Poniżej znajdziesz typowe importy potrzebne do obsługi plików PSD.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Teraz rozbijmy kod na przystępne kroki, abyś mógł łatwo podążać za instrukcjami. Skonfigurujemy, załadujemy plik PSD, zmodyfikujemy go i zapisujemy wynik.

## Krok 1: Zdefiniuj katalog dokumentów
Zanim zaczniesz pisać kod, określ, gdzie znajduje się Twój plik PSD. To właściwie przygotowanie sceny dla Twojego projektu.

```java
String dataDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` rzeczywistą ścieżką, w której znajduje się Twój plik PSD (np. layers.psd). Dzięki temu unikniesz problemów ze znajdowaniem plików.

## Krok 2: Utwórz strumień wyjściowy ByteArrayOutputStream
Potrzebujesz miejsca, w którym przechowasz zmodyfikowany obraz przed dalszą obróbką. `ByteArrayOutputStream` pomoże Ci łatwo przechwycić dane obrazu.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Ta linia inicjalizuje nowy obiekt `ByteArrayOutputStream` o nazwie `ms`. Będziesz używać tego obiektu do zapisu niekompresowanego obrazu.

## Krok 3: Załaduj plik PSD
Teraz czas załadować rzeczywisty plik PSD. Tu zaczyna się magia!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Ta linia ładuje Twój plik PSD do obiektu `PsdImage`. Upewnij się, że podajesz prawidłową ścieżkę; w przeciwnym razie pojawi się błąd, jak nieoczekiwany quiz.

## Krok 4: Skonfiguruj PsdOptions do zapisu
Musisz określić, jak chcesz zapisać obraz — oczywiście bez kompresji!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Tutaj tworzysz obiekt `PsdOptions` i ustawiasz metodę kompresji na `Raw`. Ta metoda zapewnia, że obraz zachowuje pełną jakość i jest zapisywany bez żadnej kompresji.

## Krok 5: Zapisz obraz do strumienia wyjściowego
```java
psdImage.save(ms, saveOptions);
```

Ta linia zapisuje zmodyfikowany obraz do `ByteArrayOutputStream`, który utworzyłeś w Kroku 2, używając opcji zdefiniowanych w Kroku 4. Metoda `save` zajmuje się prawidłowym kodowaniem obrazu zgodnie z Twoimi ustawieniami.

## Krok 6: Zresetuj strumień wyjściowy
Po zapisie Twój strumień wyjściowy znajduje się na końcu. Musisz go zresetować, aby odczytać dane od początku.

```java
ms.reset();
```

Metoda `reset` przygotowuje Twój `ByteArrayOutputStream` do ponownego odczytu od początku. To jak przewinięcie taśmy przed odsłuchaniem ulubionej piosenki!

## Krok 7: Załaduj nowo utworzony obraz
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Tutaj ładujemy obraz z powrotem z `ByteArrayOutputStream` do nowego obiektu `PsdImage`. To moment, w którym możesz sprawdzić wyniki swojej wcześniejszej pracy.

## Krok 8: Utwórz obiekt Graphics
Aby dalej modyfikować lub renderować obraz, musisz utworzyć obiekt graficzny.

```java
Graphics graphics = new Graphics(psdImage);
```

Ta linia inicjalizuje obiekt `Graphics` przy użyciu Twojego `psdImage`. Teraz możesz używać tego obiektu graficznego do rysowania lub manipulacji obrazem według potrzeb. To jak posiadanie pędzla w ręku!

## Manipulacja warstwami PSD przy użyciu obiektu Graphics
Mając już instancję **Graphics**, możesz **manipulować warstwami PSD** — na przykład rysować kształty, dodawać tekst lub stosować filtry na konkretnej warstwie. Kontekst graficzny działa bezpośrednio na danych pikselowych, dając precyzyjną kontrolę nad wyglądem każdej warstwy.

## Typowe problemy i rozwiązania
- **NullPointerException podczas ładowania pliku** — sprawdź dokładnie ścieżkę `dataDir` i upewnij się, że nazwa pliku jest poprawna.  
- **Wyjście skompresowane pomimo użycia Raw** — zweryfikuj, czy przed wywołaniem `save` metoda `saveOptions.setCompressionMethod(CompressionMethod.Raw);` została wywołana.  
- **Obiekt Graphics jest pusty** — upewnij się, że rysujesz na właściwym obiekcie `PsdImage` (użyj tego, który załadowałeś, a nie nowo utworzonego, chyba że tak zamierzasz).

## FAQ's
### Co to jest Aspose.PSD?
Aspose.PSD to biblioteka .NET umożliwiająca programistom tworzenie, edytowanie i manipulowanie plikami Photoshop PSD oraz powiązanymi formatami obrazów w sposób programistyczny.

### Jak mogę pobrać Aspose.PSD for Java?
Możesz pobrać ją ze [strony wydania](https://releases.aspose.com/psd/java/).

### Czy istnieje darmowa wersja próbna Aspose.PSD?
Tak, darmową wersję próbną możesz uzyskać [tutaj](https://releases.aspose.com/).

### Czy mogę uzyskać wsparcie dla Aspose.PSD?
Oczywiście! Pomoc znajdziesz na [forum wsparcia Aspose](https://forum.aspose.com/c/psd/34).

### Jak mogę uzyskać tymczasową licencję dla Aspose.PSD?
Wystarczy odwiedzić [stronę tymczasowej licencji](https://purchase.aspose.com/temporary-license/), aby rozpocząć.

## Frequently Asked Questions

**Q: Czy mogę używać obiektu graphics do edycji tylko jednej konkretnej warstwy?**  
A: Tak. Po załadowaniu PSD wybierz żądaną warstwę poprzez `psdImage.getLayers().get_Item(index)` i przekaż ją do konstruktora `Graphics`.

**Q: Czy metoda kompresji Raw wpływa na rozmiar pliku?**  
A: Raw przechowuje dane pikselowe bez kompresji, więc rozmiar pliku będzie większy niż w skompresowanych PSD, ale jakość obrazu pozostaje niezmieniona.

**Q: Czy można wyeksportować edytowany PSD do innego formatu (np. PNG)?**  
A: Zdecydowanie. Użyj odpowiedniego przeciążenia `Image.save` z `PngOptions` po edycji — to standardowy sposób **eksportowania PSD do PNG**.

**Q: Jakiej wersji Javy wymaga Aspose.PSD?**  
A: Aspose.PSD for Java obsługuje JDK 8 i nowsze.

**Q: Jak zwolnić zasoby po przetworzeniu?**  
A: Wywołaj `psdImage.dispose()` i zamknij wszystkie strumienie, aby zwolnić zasoby natywne.

---

**Ostatnia aktualizacja:** 2026-02-17  
**Testowano z:** Aspose.PSD for Java (najnowsze wydanie)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
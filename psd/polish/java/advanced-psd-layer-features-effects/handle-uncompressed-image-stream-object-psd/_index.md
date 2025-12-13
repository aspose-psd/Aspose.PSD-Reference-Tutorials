---
date: 2025-12-13
description: Dowiedz się, jak tworzyć obiekt graficzny PSD i manipulować warstwami
  PSD, obsługując nieskompresowane strumienie obrazów przy użyciu Aspose.PSD dla Javy.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Utwórz obiekt graficzny PSD – niekompresowany strumień w Javie
url: /pl/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz obiekt graficzny PSD – Niekompresowany strumień w Javie

## Wprowadzenie
Witamy w świecie manipulacji obrazami w Javie! W tym samouczku **utworzysz obiekt graficzny PSD** i obsłużysz niekompresowane strumienie obrazu przy użyciu Aspose.PSD for Java. Niezależnie od tego, czy jesteś projektantem graficznym, który chce zautomatyzować swoje procesy, czy programistą, który chce zintegrować potężne możliwości przetwarzania obrazów w swoich aplikacjach, ten przewodnik jest stworzony właśnie dla Ciebie. Przejdziemy przez wszystko, od wymagań wstępnych po podsumowanie, zapewniając solidne zrozumienie, jak rozpocząć pracę z Aspose.PSD.

## Szybkie odpowiedzi
- **Co oznacza „utwórz obiekt graficzny PSD”?** Odnosi się to do utworzenia kontekstu graficznego dla pliku PSD, aby móc rysować lub edytować jego zawartość.  
- **Która biblioteka obsługuje niekompresowane strumienie?** Aspose.PSD for Java zapewnia pełne wsparcie dla surowych (niekompresowanych) danych obrazu.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna wystarczy do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę manipulować warstwami PSD po utworzeniu obiektu graficznego?** Tak – instancja Graphics pozwala rysować na dowolnej warstwie.  

## Wymagania wstępne
Zanim przejdziemy do kodu, upewnijmy się, że masz wszystko, co potrzebne, aby rozpocząć tę podróż. Oto wymagania wstępne:

### Java Development Kit (JDK)
Upewnij się, że masz zainstalowany JDK na swoim komputerze. Możesz go pobrać ze strony Oracle lub użyć OpenJDK.

### Aspose.PSD for Java
Musisz pobrać i zainstalować bibliotekę Aspose.PSD. Ta potężna biblioteka umożliwia łatwą manipulację plikami PSD. Najnowszą wersję możesz uzyskać z [tego linku](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Warto używać IDE do pisania i testowania kodu Java. Możesz wybrać IntelliJ IDEA, Eclipse lub dowolne inne, które odpowiada Twoim preferencjom.

### Podstawowa znajomość Javy
Znajomość programowania w Javie ułatwi ten proces. Upewnij się, że znasz podstawy, takie jak klasy, metody i obsługa wyjątków.

Mając wszystko gotowe, zakasaj rękawy i przejdźmy do ekscytującej części – kodowania!

## Importowanie pakietów
Aby rozpocząć, musimy zaimportować niezbędne pakiety do pracy z Aspose.PSD. Poniżej znajdziesz importy, które zazwyczaj będą potrzebne do obsługi plików PSD.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Teraz rozbijmy kod na przystępne kroki, abyś mógł łatwo podążać za instrukcją. Skonfigurujemy, załadujemy plik PSD, zmodyfikujemy go i zapisujemy wynik.

## Krok 1: Zdefiniuj katalog dokumentów
Zanim zaczniesz pisać kod, określ, gdzie znajduje się Twój plik PSD. To właściwie przygotowanie sceny dla Twojego projektu.

```java
String dataDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` rzeczywistą ścieżką, w której znajduje się plik PSD (np. layers.psd). Dzięki temu łatwiej będzie odnaleźć pliki bez problemów.

## Krok 2: Utwórz strumień wyjściowy ByteArrayOutputStream
Potrzebujesz miejsca, w którym przechowasz zmodyfikowany obraz przed dalszą obróbką. `ByteArrayOutputStream` pomoże Ci łatwo przechwycić dane obrazu.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Ta linia inicjalizuje nowy obiekt `ByteArrayOutputStream` o nazwie `ms`. Będziesz używać tego obiektu do zapisu niekompresowanego obrazu.

## Krok 3: Załaduj plik PSD
Nadszedł czas, aby wczytać rzeczywisty plik PSD. Tu zaczyna się magia!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Ta linia ładuje Twój plik PSD do obiektu `PsdImage`. Upewnij się, że podajesz prawidłową ścieżkę; w przeciwnym razie pojawi się błąd, jak nieoczekiwany quiz.

## Krok 4: Skonfiguruj PsdOptions do zapisu
Musisz określić, w jaki sposób chcesz zapisać obraz — oczywiście niekompresowany!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Tutaj tworzysz obiekt `PsdOptions` i ustawiasz metodę kompresji na `Raw`. Ta metoda zapewnia, że obraz zachowuje pełną jakość i jest zapisywany bez kompresji.

## Krok 5: Zapisz obraz do strumienia wyjściowego
```java
psdImage.save(ms, saveOptions);
```

Ta linia zapisuje zmodyfikowany obraz do `ByteArrayOutputStream`, który utworzyłeś w Kroku 2, używając opcji zdefiniowanych w Kroku 4. Metoda `save` zajmuje się prawidłowym kodowaniem obrazu zgodnie z Twoimi ustawieniami.

## Krok 6: Zresetuj strumień wyjściowy
Po zapisie Twój strumień wyjściowy znajduje się na końcu. Musisz go zresetować, aby móc odczytać dane od początku.

```java
ms.reset();
```

Metoda `reset` przygotowuje Twój `ByteArrayOutputStream` do odczytu od początku. To jak przewinięcie taśmy przed odtworzeniem ulubionej piosenki!

## Krok 7: Załaduj nowo utworzony obraz
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Tutaj wczytujemy obraz z powrotem z `ByteArrayOutputStream` do nowego obiektu `PsdImage`. Dzięki temu możesz sprawdzić wyniki swojej wcześniejszej pracy.

## Krok 8: Utwórz obiekt Graphics
Aby dalej modyfikować lub renderować obraz, musisz utworzyć obiekt graficzny.

```java
Graphics graphics = new Graphics(psdImage);
```

Ta linia inicjalizuje obiekt `Graphics` przy użyciu Twojego `psdImage`. Teraz możesz używać tego obiektu graficznego do rysowania lub manipulacji obrazem według potrzeb. To jak posiadanie pędzla w ręku!

## Manipulacja warstwami PSD za pomocą obiektu Graphics
Mając już instancję **Graphics**, możesz **manipulować warstwami PSD** — na przykład rysować kształty, dodawać tekst lub stosować filtry na konkretnej warstwie. Kontekst graficzny działa bezpośrednio na danych pikseli, dając precyzyjną kontrolę nad wyglądem każdej warstwy.

## Typowe problemy i rozwiązania
- **NullPointerException przy ładowaniu pliku** – sprawdź dwukrotnie ścieżkę `dataDir` i upewnij się, że nazwa pliku jest poprawna.  
- **Wyjście skompresowane pomimo użycia Raw** – zweryfikuj, czy przed wywołaniem metody `save` wywołano `saveOptions.setCompressionMethod(CompressionMethod.Raw);`.  
- **Obiekt Graphics jest pusty** – upewnij się, że rysujesz na właściwej instancji `PsdImage` (użyj tej, którą załadowałeś, a nie nowo utworzonej, chyba że tak zamierzasz).

## FAQ's
### Co to jest Aspose.PSD?
Aspose.PSD to biblioteka .NET, która umożliwia programistom tworzenie, edytowanie i manipulowanie plikami Photoshop PSD oraz powiązanymi formatami obrazów w sposób programowy.

### Jak mogę pobrać Aspose.PSD for Java?
Możesz pobrać ją ze [strony wydania](https://releases.aspose.com/psd/java/).

### Czy istnieje darmowa wersja próbna Aspose.PSD?
Tak, darmową wersję próbną możesz uzyskać [tutaj](https://releases.aspose.com/).

### Czy mogę uzyskać wsparcie dla Aspose.PSD?
Oczywiście! Pomoc znajdziesz na [forum wsparcia Aspose](https://forum.aspose.com/c/psd/34).

### Jak mogę uzyskać tymczasową licencję dla Aspose.PSD?
Wystarczy odwiedzić [stronę tymczasowej licencji](https://purchase.aspose.com/temporary-license/), aby rozpocząć.

## Frequently Asked Questions

**Q: Czy mogę używać obiektu Graphics do edycji tylko jednej, konkretnej warstwy?**  
A: Tak. Po załadowaniu PSD wybierz żądaną warstwę za pomocą `psdImage.getLayers().get_Item(index)` i przekaż ją do konstruktora `Graphics`.

**Q: Czy metoda kompresji Raw wpływa na rozmiar pliku?**  
A: Raw przechowuje dane pikseli bez kompresji, więc rozmiar pliku będzie większy niż w przypadku skompresowanych PSD, ale jakość obrazu pozostaje niezmieniona.

**Q: Czy można wyeksportować edytowany PSD do innego formatu (np. PNG)?**  
A: Zdecydowanie. Użyj odpowiedniego przeciążenia `Image.save` z `PngOptions` po zakończeniu edycji.

**Q: Jaka wersja Javy jest wymagana?**  
A: Aspose.PSD for Java obsługuje JDK 8 i nowsze.

**Q: Jak zwolnić zasoby po przetworzeniu?**  
A: Wywołaj `psdImage.dispose()` i zamknij wszystkie strumienie, aby zwolnić zasoby natywne.

---  

**Ostatnia aktualizacja:** 2025-12-13  
**Testowano z:** Aspose.PSD for Java (najnowsze wydanie)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
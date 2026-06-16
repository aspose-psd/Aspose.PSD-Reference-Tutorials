---
date: 2026-03-02
description: Naucz się, jak dodać wypełnienie, tworząc warstwę wypełnienia kolorem
  w plikach PSD przy użyciu Javy i Aspose.PSD. Skorzystaj z naszego przewodnika krok
  po kroku, aby szybko ustawić kolor warstwy wypełnienia.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'Jak dodać wypełnienie: Dodaj warstwę wypełnienia kolorem do plików PSD przy
  użyciu Javy'
url: /pl/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj warstwę wypełnienia kolorem do plików PSD przy użyciu Javy

## Wprowadzenie
Czy kiedykolwiek musiałeś programowo manipulować plikami Photoshop, na przykład dodać odrobinę koloru do projektu? Jeśli zastanawiasz się **jak dodać wypełnienie** do PSD, jesteś we właściwym miejscu. W tym samouczku pokażemy, jak dodać warstwę wypełnienia kolorem do plików PSD (Photoshop Document) przy użyciu Javy i biblioteki Aspose.PSD. Wyobraź sobie swój PSD jako cyfrowe płótno — po zakończeniu będziesz wiedział, jak utworzyć warstwę wypełnienia kolorem, ustawić kolor warstwy wypełnienia i zapisać zaktualizowany plik w kilku linijkach kodu.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebujesz?** Aspose.PSD for Java  
- **Podstawowy przypadek użycia?** Programowe dodawanie lub zmiana kolorów wypełnienia w PSD  
- **Ile czasu zajmuje implementacja?** Około 10‑15 minut dla podstawowego scenariusza  
- **Czy potrzebna jest licencja?** Bezpłatna wersja próbna wystarczy do oceny; licencja komercyjna jest wymagana w produkcji  
- **Obsługiwana wersja Javy?** Java 8 i wyższe  

## Co to jest warstwa wypełnienia kolorem?
Warstwa wypełnienia kolorem to jednokolorowa nakładka, która znajduje się nad innymi warstwami w dokumencie Photoshop. Często używana jest do dodania koloru tła, tworzenia masek lub szybkiej zmiany tematu wizualnego projektu bez edytowania poszczególnych pikseli.

## Dlaczego dodawać warstwę wypełnienia kolorem przy pomocy kodu?
- **Automatyzacja:** Generowanie spójnych zasobów brandingowych w wielu plikach.  
- **Przetwarzanie wsadowe:** Aktualizacja dziesiątek PSD w kilka sekund zamiast ręcznie.  
- **Dynamiczne projekty:** Zmiana kolorów w locie w zależności od danych wejściowych lub źródeł danych.

## Wymagania wstępne
Zanim przejdziemy do kodu, upewnijmy się, że masz wszystko, co potrzebne:

1. **Java Development Kit (JDK)** – zainstalowany JDK 8 lub nowszy.  
2. **Biblioteka Aspose.PSD** – pobierz najnowszy plik JAR ze [strony Aspose Releases](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans lub dowolny edytor, którego używasz.  
4. **Podstawowa znajomość Javy** – znajomość obiektów, pętli i obsługi wyjątków.

## Importowanie pakietów
Teraz, gdy podstawy są już znane, zaimportujmy niezbędne klasy. Te importy dają dostęp do obsługi PSD oraz manipulacji warstwą wypełnienia.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## Jak dodać wypełnienie – przewodnik krok po kroku

### Krok 1: Konfiguracja środowiska
Zdefiniuj, gdzie znajduje się źródłowy plik PSD i gdzie zostanie zapisany zmodyfikowany plik, a następnie załaduj dokument.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` wskazuje folder zawierający Twój PSD.  
- `sourceFileName` to oryginalny plik, który będziesz modyfikować.  
- `exportPath` to miejsce, w którym zostanie zapisany nowy plik z **dodanym warstwą wypełnienia kolorem**.

### Krok 2: Przeglądanie warstw
Musimy znaleźć istniejące warstwy wypełnienia, aby móc je zmodyfikować lub utworzyć nową.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- Pętla `for` iteruje po każdej warstwie w PSD.  
- Sprawdzenie `instanceof FillLayer` zapewnia, że pracujemy wyłącznie z warstwami wypełnienia.

### Krok 3: Weryfikacja typu wypełnienia
Upewnij się, że znaleziona warstwa jest **warstwą wypełnienia kolorem**, zanim spróbujesz zmienić jej kolor.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

Jeśli typ wypełnienia nie jest `FillType.Color`, przerywamy działanie, aby nie zmienić przypadkowo wypełnień gradientowych lub wzorcowych.

### Krok 4: Ustawienie koloru wypełnienia
Tutaj **ustawiamy kolor warstwy wypełnienia**. Przykład zmienia warstwę na czerwony, ale możesz zamienić `Color.getRed()` na dowolny inny `Color`, którego potrzebujesz (np. `Color.getBlue()`, `new Color(255, 165, 0)` dla pomarańczowego).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` zmienia rzeczywisty kolor wypełnienia.  
- `fillLayer.update()` odświeża warstwę, aby nowy kolor został zastosowany.

### Krok 5: Zapisanie zmian
Na koniec zapisz zmodyfikowany PSD z powrotem na dysk.

```java
im.save(exportPath);
break;
```

- `break` przerywa pętlę po zaktualizowaniu pierwszej pasującej warstwy wypełnienia, co zazwyczaj jest pożądane, gdy chcesz **zmienić kolor wypełnienia PSD** tylko raz.

## Typowe problemy i wskazówki
- **Nie znaleziono FillLayer:** Jeśli Twój PSD nie zawiera warstwy wypełnienia, musisz ją utworzyć przy pomocy `new FillLayer(im)` i dodać do `im.getLayers()`.  
- **Kolor się nie aktualizuje:** Upewnij się, że wywołujesz `fillLayer.update()` po ustawieniu koloru.  
- **Plik nie został zapisany:** Sprawdź, czy `exportPath` wskazuje na katalog, do którego masz prawo zapisu.

## Najczęściej zadawane pytania

**P: Czym jest Aspose.PSD?**  
O: Aspose.PSD to solidna biblioteka Java, która umożliwia tworzenie, edytowanie i konwertowanie plików Photoshop PSD bez potrzeby posiadania Adobe Photoshop.

**P: Czy mogę używać Aspose.PSD za darmo?**  
O: Tak, dostępna jest bezpłatna wersja próbna na [stronie Aspose Releases](https://releases.aspose.com/).

**P: Z jakimi formatami plików mogę pracować oprócz PSD?**  
O: Aspose.PSD obsługuje PSD, PSB, BMP, JPEG, PNG, GIF, TIFF i inne.

**P: Jak uzyskać wsparcie, jeśli napotkam problemy?**  
O: Możesz zadawać pytania na [forum Aspose Support](https://forum.aspose.com/c/psd/34).

**P: Gdzie mogę kupić pełną licencję?**  
O: Licencje są sprzedawane poprzez [stronę zakupu Aspose](https://purchase.aspose.com/buy).

## Zakończenie
Teraz wiesz **jak dodać wypełnienie** do dokumentu Photoshop programowo przy użyciu Javy. Tworząc lub znajdując warstwę wypełnienia kolorem, ustawiając jej kolor i zapisując wynik, możesz automatyzować powtarzalne zadania projektowe, generować dynamiczne zasoby lub integrować manipulację PSD z większymi aplikacjami Java. Spróbuj — eksperymentuj z różnymi kolorami, dodawaj wiele warstw wypełnienia lub łącz tę technikę z innymi funkcjami Aspose.PSD, aby uzyskać potężne potoki przetwarzania obrazów.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-03-02  
**Testowano z:** Aspose.PSD for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

---
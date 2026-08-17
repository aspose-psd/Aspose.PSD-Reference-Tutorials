---
date: 2026-03-07
description: Dowiedz się, jak dodawać tekst do plików PSD w czasie wykonywania przy
  użyciu Javy i Aspose.PSD. Skorzystaj z tego przewodnika krok po kroku, aby szybko
  utworzyć warstwę tekstową w pliku PSD.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Dodaj tekst do plików PSD w czasie wykonywania przy użyciu Javy
url: /pl/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodawanie tekstu do plików PSD w czasie wykonywania przy użyciu Javy

## Wprowadzenie
Jeśli kiedykolwiek ręcznie edytowałeś dokument Photoshop, wiesz, jak potężne mogą być warstwy. Co by było, gdybyś mógł **dodawać tekst do PSD** automatycznie z poziomu aplikacji Java? Dzięki bibliotece Aspose.PSD for Java możesz w czasie wykonywania utworzyć warstwę tekstową w pliku PSD, otwierając drzwi do przetwarzania wsadowego, dynamicznego generowania grafiki i zautomatyzowanych procesów brandingu. W tym samouczku przeprowadzimy Cię przez cały proces, od konfiguracji projektu po zapis zaktualizowanego pliku.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.PSD for Java.  
- **Czy mogę dodać tekst do istniejącego PSD?** Tak – po prostu wczytaj plik, dodaj `TextLayer` i zapisz.  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest licencja komercyjna do użytku nie‑ewaluacyjnego.  
- **Jaką wersję Javy obsługuje?** JDK 8 lub wyższą (rekomendujemy najnowszą wersję LTS).  
- **Czy to nadaje się do backendów webowych?** Absolutnie – API działa w każdym środowisku serwerowym opartym na Javie.

## Co to jest „dodawanie tekstu do PSD”?
Dodawanie tekstu do PSD oznacza programowe tworzenie nowej warstwy tekstowej wewnątrz dokumentu Photoshop. Warstwa zachowuje się jak każda inna warstwa tekstowa w Photoshopie: możesz ją przesuwać, edytować jej zawartość i stosować stylizacje – wszystko bez otwierania Photoshopa.

## Dlaczego tworzyć warstwę tekstową w PSD przy użyciu Javy?
- **Automatyzacja** – generowanie zasobów marketingowych, znaków wodnych lub etykiet produktów masowo.  
- **Spójność** – zapewnienie tego samego fontu, rozmiaru i położenia w tysiącach plików.  
- **Integracja** – połączenie z innymi usługami Java (e‑commerce, raportowanie, pipeline CI), aby dostarczać grafiki w locie.

## Wymagania wstępne
Przed napisaniem kodu upewnij się, że masz:

1. **Java Development Kit (JDK)** – Zainstaluj JDK 8 lub nowszy. Możesz [pobrać go tutaj](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – Pobierz najnowszy plik JAR ze [strony wydań Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE (opcjonalnie, ale przydatne)** – IntelliJ IDEA, Eclipse lub dowolny edytor, którego używasz.  
4. **Podstawową znajomość Javy** – Powinieneś być pewny w pracy z klasami, obiektami i operacjami I/O.  
5. **Przykładowy plik PSD** – W tym przewodniku użyjemy `OneLayer.psd` umieszczonego w wybranym przez Ciebie folderze.

## Importowanie pakietów
Najpierw zaimportuj klasy, których będziesz potrzebował do pracy z plikami PSD i warstwami tekstowymi.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Te importy dają dostęp do podstawowej funkcjonalności Aspose.PSD.

## Przewodnik krok po kroku

### Krok 1: Ustaw katalog dokumentów
Zdefiniuj folder, w którym znajduje się źródłowy plik PSD oraz miejsce, w którym zostanie zapisany wynik.

```java
String dataDir = "Your Document Directory"; 
```

Zastąp `"Your Document Directory"` absolutną lub względną ścieżką do swoich plików.

### Krok 2: Wczytaj źródłowy plik PSD
Wczytaj istniejący plik PSD do pamięci przy użyciu `Image.load()`.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

Jeśli ścieżka jest prawidłowa, `img` reprezentuje teraz wczytany dokument Photoshop.

### Krok 3: Rzutuj na `PsdImage`
Ponieważ korzystamy z funkcji specyficznych dla Photoshopa, rzutujemy ogólny obiekt `Image` na `PsdImage`.

```java
PsdImage im = (PsdImage)img;
```

Rzutowanie odblokowuje metody takie jak `addTextLayer()`.

### Krok 4: Zdefiniuj prostokąt dla warstwy tekstowej
Określ, gdzie ma się pojawić nowy tekst. Prostokąt definiuje pozycję (x, y) oraz rozmiar (szerokość, wysokość).

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

Śmiało dostosuj obliczenia do własnych potrzeb projektowych.

### Krok 5: Dodaj warstwę tekstową
Utwórz rzeczywistą warstwę tekstową wewnątrz zdefiniowanego prostokąta.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

Zastąp `"Added text"` dowolnym ciągiem znaków, który ma się pojawić w PSD. To miejsce, w którym **tworzymy warstwę tekstową PSD** programowo.

### Krok 6: Zapisz zaktualizowany plik PSD
Zapisz zmodyfikowany dokument do nowego pliku, aby nie nadpisać oryginału.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

Po wykonaniu znajdziesz `ImageWithTextLayer.psd` w docelowym folderze, teraz zawierający nową warstwę tekstową.

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|-------|--------|-----|
| **`NullPointerException` on `im.addTextLayer`** | PSD nie został poprawnie wczytany (zła ścieżka). | Sprawdź, czy `sourceFileName` wskazuje istniejący plik PSD. |
| **Text not visible** | Prostokąt znajduje się poza obszarem płótna lub warstwa jest ukryta. | Dostosuj współrzędne prostokąta lub sprawdź widoczność warstwy przy użyciu `layer.setVisible(true)`. |
| **LicenseException** | Używanie biblioteki bez ważnej licencji w środowisku produkcyjnym. | Uzyskaj licencję komercyjną i ustaw ją za pomocą `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |

## Najczęściej zadawane pytania

**Q: Czy mogę dodać wiele warstw tekstowych?**  
**A:** Tak – po prostu powtórz Kroki 4 i 5 dla każdego fragmentu tekstu, który chcesz wstawić.

**Q: Jak stylizować tekst (czcionka, rozmiar, kolor)?**  
**A:** Klasa `TextLayer` udostępnia metodę `getTextData()`, w której możesz modyfikować `Font`, `FontSize`, `Color` oraz inne właściwości stylu. Zapoznaj się z dokumentacją API Aspose.PSD, aby poznać wszystkie szczegóły.

**Q: Co zrobić, jeśli mój PSD już zawiera wiele warstw?**  
**A:** Aspose.PSD radzi sobie ze złożonymi strukturami warstw. Możesz celować w konkretne grupy lub wstawić nową warstwę tekstową pod określonym indeksem, używając przeciążeń `addTextLayer`.

**Q: Czy to podejście nadaje się do aplikacji webowych?**  
**A:** Absolutnie. O ile Twój serwer uruchamia Javę, możesz generować lub modyfikować pliki PSD w locie i udostępniać je klientom.

**Q: Gdzie mogę uzyskać pomoc, jeśli napotkam problemy?**  
**A:** Odwiedź [forum wsparcia Aspose](https://forum.aspose.com/c/psd/34), gdzie społeczność oraz inżynierowie Aspose chętnie pomogą.

## Podsumowanie
Teraz wiesz, jak łatwo **dodawać tekst do PSD** w czasie wykonywania przy użyciu Javy i Aspose.PSD. Ta technika umożliwia automatyzację tworzenia grafiki, personalizację zasobów oraz integrację edycji na poziomie Photoshopa w dowolnym rozwiązaniu opartym na Javie. Przeglądaj dalsze możliwości API Aspose.PSD, aby dodawać kształty, warstwy rastrowe czy nawet stosować filtry dla jeszcze bogatszej automatyzacji.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-03-07  
**Testowano z:** Aspose.PSD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose
---
date: 2026-03-18
description: Dowiedz się, jak zmienić rozdzielczość PNG w Javie i ustawić rozdzielczość
  obrazu w Javie przy użyciu Aspose.PSD for Java. Skorzystaj z tego przewodnika krok
  po kroku, aby szybko zoptymalizować swoje obrazy.
linktitle: Change PNG resolution java using Aspose.PSD
second_title: Aspose.PSD Java API
title: Zmień rozdzielczość PNG w Javie przy użyciu Aspose.PSD
url: /pl/java/optimizing-png-files/set-png-file-resolution/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zmienianie rozdzielczości PNG w Javie przy użyciu Aspose.PSD

## Wstęp
Jeśli potrzebujesz **zmienić rozdzielczość PNG w Javie** szybko i niezawodnie, jesteś we właściwym miejscu. W tym samouczku przeprowadzimy Cię krok po kroku przez wszystkie niezbędne czynności, aby dostosować rozdzielczość pliku PNG przy użyciu Aspose.PSD for Java. Niezależnie od tego, czy tworzysz narzędzie do przetwarzania wsadowego, usługę internetową, czy po prostu dopracowujesz kilka zasobów, to samo podejście działa wszędzie. Otwórz ulubione IDE i zaczynamy!

## Szybkie odpowiedzi
- **Jaką bibliotekę używać do rozdzielczości PNG?** Aspose.PSD for Java  
- **Główna metoda?** `PngOptions.setResolutionSettings`  
- **Typowe wartości DPI?** 72 × 96 dla obrazów przeznaczonych do sieci  
- **Czy potrzebna jest licencja?** Wersja próbna wystarczy do testów; licencja jest wymagana w środowisku produkcyjnym  
- **Obsługiwany JDK?** Java 8 lub wyższa  

## Co oznacza „change PNG resolution java”?
Zmiana rozdzielczości PNG w Javie polega na modyfikacji metadanych DPI (dots per inch), które informują przeglądarki i drukarki, jak duży ma być wyświetlany obraz. Dane pikseli pozostają niezmienione, ale znacznik rozdzielczości jest aktualizowany, co może wpływać na rozmiar i jakość wydruku.

## Dlaczego warto używać Aspose.PSD do tego zadania?
Aspose.PSD oferuje wysokopoziomowe API, które ukrywa szczegóły niskopoziomowej obsługi PNG, pozwalając skupić się na logice biznesowej zamiast na niuansach formatu pliku. Biblioteka obsługuje setki funkcji PSD, działa na każdej platformie uruchamiającej Javę i nie wymaga natywnych bibliotek.

## Wymagania wstępne
Zanim rozpoczniesz, upewnij się, że masz:

1. **Java Development Kit (JDK) 8+** – kod działa na każdym współczesnym JDK.  
2. **Aspose.PSD for Java** – pobierz ją z [linku do pobrania](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub VS Code z obsługą Javy.  
4. **Przykładowy plik PSD** – przekonwertujemy go na PNG i zmienimy rozdzielczość.  
5. **Podstawową znajomość Javy** – fragmenty kodu będą zrozumiałe bez dodatkowych wyjaśnień.

## Importowanie pakietów
Teraz, gdy wszystko jest gotowe, zaimportuj klasy, które będą Ci potrzebne. Te importy dają dostęp do ładowania obrazu, ustawień rozdzielczości i opcji eksportu PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResolutionSetting;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Konfiguracja projektu Java
Utwórz nowy projekt Java (lub moduł Maven/Gradle) i dodaj plik JAR Aspose.PSD do ścieżki kompilacji. Jeśli używasz Maven, dodaj odpowiednią zależność z repozytorium Aspose.

## Krok 2: Definiowanie katalogu dokumentów
Określ programowi, gdzie znajduje się źródłowy plik PSD oraz gdzie zapisać wynikowy PNG.

```java
String dataDir = "Your Document Directory"; // Update with your folder path
```

Zastąp `"Your Document Directory"` absolutną lub względną ścieżką zawierającą `sample.psd`.

## Krok 3: Ładowanie obrazu PSD
Użyj klasy `PsdImage`, aby odczytać plik PSD z dysku.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Upewnij się, że nazwa pliku odpowiada rzeczywistemu PSD, który chcesz przetworzyć.

## Krok 4: Tworzenie i konfigurowanie opcji PNG
Tutaj faktycznie **zmieniamy rozdzielczość PNG w Javie**. Tworzymy obiekt `PngOptions` i ustawiamy poziomy DPI w poziomie i pionie za pomocą `ResolutionSetting`.

```java
PngOptions options = new PngOptions();
options.setResolutionSettings(new ResolutionSetting(72, 96)); // 72 DPI horizontal, 96 DPI vertical
```

Śmiało zamień `72` i `96` na dowolne wartości pasujące do docelowego urządzenia. To jest sedno operacji **ustawiania rozdzielczości obrazu w Javie**.

## Krok 5: Zapisanie wynikowego PNG
Na koniec wyeksportuj PSD jako PNG z nowymi metadanymi rozdzielczości.

```java
psdImage.save(dataDir + "SettingResolution_output.png", options);
```

Plik `SettingResolution_output.png` pojawi się w tym samym folderze, zawierając teraz DPI, które określiłeś.

## Typowe pułapki i wskazówki
- **Nieprawidłowa ścieżka** – sprawdź, czy `dataDir` kończy się separatorem plików (`/` lub `\`).  
- **Nieobsługiwane DPI** – większość przeglądarek ignoruje wartości DPI powyżej 300; zachowaj rozsądne liczby.  
- **Zużycie pamięci** – duże pliki PSD mogą pochłaniać dużo RAM; rozważ zwolnienie `psdImage` po zapisaniu (`psdImage.dispose()`).  

## Zakończenie
Właśnie nauczyłeś się, jak **zmienić rozdzielczość PNG w Javie** przy użyciu Aspose.PSD. Modyfikując `ResolutionSetting`, możesz kontrolować, jak Twoje PNG są interpretowane przez drukarki i narzędzia projektowe, nie zmieniając danych pikselowych. Eksperymentuj z innymi opcjami, takimi jak poziom kompresji, głębia kolorów czy przetwarzanie wsadowe, aby jeszcze bardziej zautomatyzować swój przepływ pracy.

Po więcej informacji zajrzyj do oficjalnej [dokumentacji Aspose.PSD](https://reference.aspose.com/psd/java/).

## FAQ
### Jakie formaty mogę konwertować z plików PSD przy użyciu Aspose.PSD for Java?
Możesz konwertować pliki PSD do formatów takich jak PNG, JPEG, BMP i TIFF.  
### Czy potrzebna jest licencja do korzystania z Aspose.PSD for Java?
Tak, wersja próbna jest dostępna, ale po ocenie wymagana jest ważna licencja.  
### Czy mogę zmienić rozdzielczość więcej niż raz w jednym programie?
Oczywiście! Możesz tworzyć różne instancje `PngOptions` dla różnych ustawień eksportu w tej samej aplikacji.  
### Co zrobić, jeśli mój plik PSD jest uszkodzony?
Aspose.PSD radzi sobie z wieloma typowymi problemami, ale w przypadku poważnego uszkodzenia pliku może nie udać się jego załadowanie. Zawsze trzymaj kopię zapasową.  
### Czy Aspose.PSD nadaje się do aplikacji o wysokiej wydajności?
Tak, biblioteka została zaprojektowana do efektywnego obsługiwania dużych plików i jest odpowiednia dla zadań wymagających intensywnego przetwarzania obrazów.

## Frequently Asked Questions
**Q: Jak programowo ustawić różne DPI dla osi poziomej i pionowej?**  
A: Użyj `new ResolutionSetting(horizontalDpi, verticalDpi)` tak, jak pokazano w przykładzie opcji PNG.  

**Q: Czy mogę przetwarzać wsadowo wiele plików PSD w jednym uruchomieniu?**  
A: Tak — umieść kroki ładowania, konfiguracji opcji i zapisu w pętli iterującej po kolekcji plików.  

**Q: Czy zmiana DPI wpływa na rozmiar pliku?**  
A: Zazwyczaj nie; DPI to metadane. Rozmiar pliku zmienia się tylko przy modyfikacji kompresji lub wymiarów pikseli.  

**Q: Czy istnieje sposób, aby odczytać aktualne DPI istniejącego PNG?**  
A: Załaduj PNG przy pomocy `Image.load()` i sprawdź `image.getResolutionSettings()` (dostępne dla plików PNG).  

**Q: Jakie wersje JDK są oficjalnie wspierane?**  
A: Aspose.PSD for Java obsługuje JDK 8 do JDK 21.

---

**Ostatnia aktualizacja:** 2026-03-18  
**Testowano z:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-04-05
description: Dowiedz się, jak eksportować pliki PSD do PNG i łączyć warstwy PSD przy
  użyciu Aspose.PSD dla Javy. Zawiera informacje o konwersji PSD do JPEG, ustawianiu
  jakości JPEG oraz wskazówki dotyczące konwersji PSD do TIFF.
keywords:
- export psd to png
- convert psd to jpeg
- how to merge psd
- set jpeg quality
- psd to tiff conversion
linktitle: Eksportuj PSD do PNG i scal warstwy przy użyciu Aspose.PSD dla Javy
second_title: Aspose.PSD Java API
title: Eksportuj PSD do PNG i scal warstwy przy użyciu Aspose.PSD dla Javy
url: /pl/java/psd-layer-management-effects/merge-psd-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj PSD do PNG i scal warstwy przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

Zastanawiałeś się kiedyś, jak graficy osiągają te skomplikowane, warstwowe obrazy w Photoshopie? Sekret często tkwi w **eksportowaniu PSD do PNG** i inteligentnym scalaniu warstw. Jeśli pracujesz z plikami PSD w Javie, opanowanie tych technik może pomóc Ci tworzyć obrazy kompozytowe, zmniejszyć rozmiar pliku i przygotować zasoby do wdrożenia w sieci lub na urządzenia mobilne. W tym samouczku przeprowadzimy Cię przez **sposób scalania warstw PSD** przy użyciu Aspose.PSD dla Javy, a także pokażemy, jak wyeksportować wynik do PNG (lub JPEG/TIFF w razie potrzeby). Po zakończeniu będziesz mógł automatyzować zarządzanie warstwami i procesy eksportu bezpośrednio z aplikacji Java.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje pliki PSD w Javie?** Aspose.PSD for Java.  
- **Czy mogę wyeksportować PSD do PNG?** Tak – wystarczy ustawić odpowiednie opcje obrazu.  
- **Jak scalić wiele warstw?** Załaduj PSD, manipuluj kolekcją `Layer`, a następnie zapisz.  
- **Co zrobić, jeśli potrzebuję kontroli jakości JPEG?** Użyj `JpegOptions` i ustaw jakość (0‑100).  
- **Czy Photoshop jest wymagany?** Nie, Aspose.PSD działa niezależnie od oprogramowania Adobe.

## Co to jest eksport PSD do PNG?
Eksportowanie PSD do PNG oznacza konwersję dokumentu Photoshop (PSD) na plik Portable Network Graphics (PNG) przy jednoczesnym opcjonalnym spłaszczaniu lub scalaniu warstw. PNG zachowuje przezroczystość i jest szeroko wspierany w sieci, co czyni go popularnym formatem dla zasobów interfejsu użytkownika.

## Dlaczego programowo scalać warstwy PSD?
- **Automatyzacja:** Przetwarzaj setki plików wsadowo, bez ręcznych kliknięć.  
- **Wydajność:** Scalane warstwy skracają czas renderowania w aplikacjach downstream.  
- **Rozmiar pliku:** Spłaszczanie niepotrzebnych warstw może zmniejszyć ostateczny rozmiar obrazu.  
- **Spójność:** Gwarantuje taką samą kolejność warstw i tryby mieszania w różnych kompilacjach.

## Wymagania wstępne

1. **Biblioteka Aspose.PSD dla Javy** – pobierz z [linku do pobrania Aspose.PSD dla Javy](https://releases.aspose.com/psd/java/).  
2. **Środowisko programistyczne Java** – IntelliJ IDEA, Eclipse lub dowolne IDE, które preferujesz.  
3. **Przykładowy plik PSD** – plik z wieloma warstwami (np. `layers.psd`).  
4. **Podstawowa znajomość Javy** – powinieneś czuć się komfortowo z klasami i metodami.  
5. **Tymczasowa licencja Aspose (Opcjonalnie)** – dla większych plików lub aby usunąć ograniczenia wersji próbnej, uzyskaj [tymczasową licencję](https://purchase.aspose.com/temporary-license/).

## Importowanie pakietów

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Przewodnik krok po kroku

### Krok 1: Załaduj plik PSD

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```

> To ładuje `layers.psd` do obiektu `PsdImage`, dając pełny dostęp do jego warstw.

### Krok 2: Przeglądaj warstwy (jak scalić psd)

```java
Layer[] layers = psdImage.getLayers();
System.out.println("Total layers: " + layers.length);

for (Layer layer : layers) {
    System.out.println("Layer name: " + layer.getName());
}
```

> Przeglądanie nazw warstw pomaga zdecydować, które z nich spłaszczyć, a które pozostawić osobno.

### Krok 3: Ustaw opcje obrazu (ustaw jakość jpeg)

```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(80); // Set the quality of the JPEG image (0-100)
```

> Jeśli wolisz PNG lub TIFF, możesz zamienić `JpegOptions` na `PngOptions` lub `TiffOptions` – to miejsce, w którym konfiguruje się **konwersję psd do tiff**.

### Krok 4: Zapisz scalony obraz (eksport psd do png)

```java
psdImage.save(dataDir + "MergePSDlayers_output.png", jpgOptions);
```

> Metoda `save` zapisuje scalony wynik do `MergePSDlayers_output.png`.  
> *Wskazówka:* Aby wyeksportować do PNG, zamień `jpgOptions` na instancję `PngOptions`; reszta kodu pozostaje bez zmian.

## Typowe problemy i rozwiązania

- **Wyjątek plik‑nie‑znaleziony:** Sprawdź, czy `dataDir` kończy się separatorem ścieżki (`/` lub `\\`) i czy plik `layers.psd` istnieje.  
- **Nieoczekiwane kolory po scaleniu:** Upewnij się, że tryby mieszania warstw są kompatybilne; możesz je dostosować za pomocą `layer.setBlendMode(...)`.  
- **Duży plik wyjściowy:** Obniż jakość JPEG lub użyj poziomów kompresji PNG, aby zmniejszyć rozmiar.

## Najczęściej zadawane pytania

**P:** Czy można zapisać scalony obraz w formatach innych niż JPEG?  
**O:** Oczywiście! Aspose.PSD obsługuje PNG, BMP, TIFF i inne. Wystarczy użyć odpowiedniej klasy opcji (`PngOptions`, `BmpOptions`, `TiffOptions`).

**P:** Jak mogę dostosować jakość obrazu dla różnych formatów wyjściowych?  
**O:** Każda klasa opcji udostępnia własne ustawienia jakości/kompresji. Dla JPEG użyj `setQuality(int)`. Dla PNG możesz kontrolować `CompressionLevel`.

**P:** Czy potrzebny jest zainstalowany Photoshop, aby używać Aspose.PSD dla Javy?  
**O:** Nie. Aspose.PSD działa niezależnie od Adobe Photoshop, więc możesz go uruchomić na dowolnym serwerze lub w środowisku CI.

**P:** Co się stanie, jeśli nie ustawimy opcji obrazu przed zapisem?  
**O:** Biblioteka zastosuje domyślne ustawienia (np. jakość JPEG 75). Określenie opcji daje kontrolę nad ostatecznym wynikiem.

**P:** Czy mogę przekonwertować PSD bezpośrednio do TIFF w jednym kroku?  
**O:** Tak – utwórz instancję `TiffOptions` i wywołaj `psdImage.save("output.tiff", tiffOptions);`.

---

**Ostatnia aktualizacja:** 2026-04-05  
**Testowano z:** Aspose.PSD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
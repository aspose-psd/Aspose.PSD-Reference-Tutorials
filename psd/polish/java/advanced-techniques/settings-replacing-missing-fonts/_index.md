---
date: 2025-12-25
description: Dowiedz się, jak zamienić czcionki w plikach PSD przy użyciu Aspose.PSD
  dla Javy – krok po kroku przewodnik, który także pokazuje, jak zapisać PSD jako
  PNG i obsłużyć brakujące czcionki.
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: Jak wymienić czcionki w Aspose.PSD dla Javy
url: /pl/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak wymienić czcionki w Aspose.PSD dla Javy

## Wprowadzenie

Jeśli pracujesz z plikami Photoshop (PSD) w aplikacji Java, brakujące czcionki mogą zepsuć układ wizualny i powodować błędy renderowania. **Jak wymienić czcionki** szybko i niezawodnie jest niezbędne dla zachowania wierności projektu. W tym samouczku nauczysz się, jak używać Aspose.PSD dla Javy do zamiany brakujących czcionek, konwersji wyniku do PNG oraz utrzymania płynnego przepływu pracy przy konwersji obrazów. Po zakończeniu będziesz w stanie wymienić czcionki w obrazach, zapisać PSD jako PNG i unikać typowych pułapek, na które napotykają programiści.

## Szybkie odpowiedzi
- **Co oznacza „replace fonts” w przetwarzaniu PSD?** Zastępuje brakujące lub niedostępne czcionki czcionką zapasową, którą określasz.  
- **Która biblioteka obsługuje to automatycznie?** Aspose.PSD for Java udostępnia `PsdLoadOptions.setDefaultReplacementFont`.  
- **Czy mogę również przekonwertować PSD na PNG po zamianie?** Tak – użyj `PngOptions` i wywołaj `psdImage.save`.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Wymagana jest ważna licencja Aspose.PSD dla wersji nie‑ewaluacyjnych.  
- **Jaką wersję Javy obsługuje?** Każde środowisko uruchomieniowe Java 8+ działa z bieżącą wersją Aspose.PSD.

## Czym jest zamiana czcionek w plikach PSD?

Gdy PSD odwołuje się do czcionki, która nie jest zainstalowana na komputerze hosta, silnik renderujący przechodzi na czcionkę ogólną, co często skutkuje nieprawidłowo wyrównanym tekstem. Zamiana czcionek pozwala zdefiniować domyślną czcionkę (np. Arial), której biblioteka użyje, gdy napotka brakującą czcionkę, zapewniając spójny wygląd wizualny.

## Dlaczego wymieniać brakujące czcionki przy użyciu Aspose.PSD?

- **Rozwiązanie bez zależności** – Nie wymaga natywnego Photoshopa ani zewnętrznych narzędzi.  
- **Gotowe do przetwarzania wsadowego** – Przetwarzaj dziesiątki plików w pętli przy użyciu tych samych ustawień.  
- **Gotowe do konwersji obrazów** – Po zamianie możesz od razu **zapisać PSD jako PNG** lub **przekonwertować PSD na PNG** bez dodatkowych kroków.  
- **Wieloplatformowe** – Działa w środowiskach Java na Windows, Linux i macOS.

## Wymagania wstępne

1. **Biblioteka Aspose.PSD** – Pobierz i zainstaluj bibliotekę Aspose.PSD for Java ze [strony wydań](https://releases.aspose.com/psd/java/).  
2. **Środowisko programistyczne Java** – Zainstalowany i skonfigurowany JDK 8 lub nowszy.

Teraz, gdy mamy niezbędne elementy, przejdźmy do kodu.

## Importowanie pakietów

Zacznij od zaimportowania niezbędnych klas Aspose.PSD. Dzięki temu uzyskasz dostęp do ładowania obrazów, opcji zamiany czcionek oraz możliwości eksportu do PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Skonfiguruj katalog dokumentów

Określ folder zawierający źródłowy plik PSD oraz miejsce, w którym zostanie zapisany wynikowy plik PNG.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Określ pliki źródłowy i docelowy

Podaj pełne ścieżki do pliku PSD wejściowego oraz pliku PNG wyjściowego. Dzięki temu przepływ pracy jest przejrzysty, a kod łatwy w utrzymaniu.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Krok 3: Skonfiguruj ustawienia zamiany czcionek

Utwórz instancję `PsdLoadOptions` i określ Aspose.PSD, której czcionki użyć, gdy napotka brakującą. W tym przykładzie używamy **Arial**, ale możesz zamienić ją na dowolną czcionkę zainstalowaną w systemie.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Krok 4: Załaduj obraz PSD i zamień czcionki

Załaduj plik PSD przy użyciu wcześniej zdefiniowanych opcji. Biblioteka automatycznie zamienia wszystkie brakujące czcionki na domyślną, którą określiłeś.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Krok 5: Zapisz zmodyfikowany obraz

Skonfiguruj opcje eksportu PNG — true color z kanałem alfa — aby zachować przezroczystość. Ten krok również demonstruje **konwersję obrazu PSD do PNG** po zamianie czcionek.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### Co się właśnie wydarzyło?

- Plik PSD został otwarty z czcionką zapasową (Arial).  
- Wszystkie warstwy tekstowe, które pierwotnie odwoływały się do brakujących czcionek, są teraz renderowane przy użyciu Arial.  
- Końcowy obraz został zapisany jako PNG, efektywnie **zapisując PSD jako PNG**, zachowując wierność wizualną.

## Typowe problemy i rozwiązywanie

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|----------|
| Tekst nadal wygląda niepoprawnie | Metryki czcionki różnią się (rozmiar, waga) | Dostosuj rozmiar czcionki zamiennika programowo lub wybierz czcionkę o podobnych metrykach. |
| PNG jest większy niż oczekiwano | Domyślne opcje PNG używają 32‑bitowego koloru | Przełącz `PngColorType` na `Truecolor`, jeśli kanał alfa nie jest potrzebny. |
| Wyjątek licencyjny | Uruchamianie bez ważnej licencji | Zastosuj tymczasową lub stałą licencję Aspose.PSD przed załadowaniem obrazu. |

## Najczęściej zadawane pytania

**P: Czy Aspose.PSD jest kompatybilny ze wszystkimi wersjami plików PSD?**  
O: Aspose.PSD obsługuje szeroki zakres wersji PSD, od wczesnych wydań Photoshopa po najnowsze funkcje.

**P: Czy mogę używać własnych czcionek do zamiany w Aspose.PSD?**  
O: Tak, po prostu przekaż nazwę własnej czcionki do `setDefaultReplacementFont`. Upewnij się, że czcionka jest dostępna dla JVM.

**P: Czy dostępne są opcje licencjonowania Aspose.PSD?**  
O: Zapoznaj się z opcjami licencjonowania [tutaj](https://purchase.aspose.com/buy), aby wybrać najlepszy plan dla swoich potrzeb.

**P: Czy istnieje forum społecznościowe wsparcia Aspose.PSD?**  
O: Tak, odwiedź [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) w celu uzyskania wsparcia i dyskusji.

**P: Jak mogę uzyskać tymczasową licencję dla Aspose.PSD?**  
O: Uzyskaj tymczasową licencję [tutaj](https://purchase.aspose.com/temporary-license/) do celów testowych i ewaluacyjnych.

---

**Ostatnia aktualizacja:** 2025-12-25  
**Testowano z:** Aspose.PSD 24.11 for Java (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-03-15
description: Dowiedz się, jak tworzyć pliki PSD, generować paletę kolorów PSD i ustawiać
  tryb kolorów PSD przy użyciu Aspose.PSD for Java w tym przewodniku krok po kroku.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Jak tworzyć pliki PSD przy użyciu Aspose.PSD dla Javy
url: /pl/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

}}

All shortcodes unchanged.

Now ensure we didn't miss any text.

Check the initial lines: after shortcodes there is blank line then title. Keep same.

Now produce final content with all translations. Ensure we keep code block placeholders exactly as they appear.

Also ensure we keep markdown formatting.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak tworzyć pliki PSD przy użyciu Aspose.PSD w Javie

## Wstęp
Jeśli kiedykolwiek zastanawiałeś się **how to create PSD** plików programowo, jesteś we właściwym miejscu. Aspose.PSD for Java daje pełną kontrolę nad dokumentami Photoshop, umożliwiając generowanie, edytowanie i zapisywanie plików PSD bez otwierania Photoshopa. W tym samouczku przeprowadzimy Cię przez tworzenie **indexed PSD** pliku, ustawianie trybu kolorów PSD oraz generowanie własnej palety kolorów — wszystko przy użyciu przejrzystego, krok po kroku kodu Java. Niezależnie od tego, czy budujesz pipeline graficzny, automatyzujesz tworzenie zasobów, czy po prostu eksperymentujesz, przedstawione koncepcje pomogą Ci ożywić Twoje wizualne pomysły.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.PSD for Java
- **Czy mogę utworzyć indexed PSD?** Yes, by setting the color mode to `Indexed`
- **Czy muszę mieć zainstalowany Photoshop?** No, Aspose.PSD works independently
- **Jakiej wersji Java wymaga się?** JDK 8 or later
- **Jak duży może być płótno?** Any size; this example uses 500 × 500 px

## Czym jest plik Indexed PSD?
Plik Indexed PSD przechowuje kolory w palecie zamiast pełnych wartości kolorów dla każdego piksela. To zmniejsza rozmiar pliku i jest idealne dla grafiki o ograniczonej liczbie kolorów, takiej jak ikony lub zasoby UI. Generując własną paletę, kontrolujesz dokładnie, które kolory pojawią się w końcowym obrazie.

## Dlaczego generować paletę kolorów PSD?
Tworzenie **PSD color palette** pozwala:
- Utrzymać mały rozmiar plików dla zastosowań webowych lub mobilnych  
- Zapewnić spójność marki poprzez ograniczenie kolorów do palety firmowej  
- Przyspieszyć renderowanie w aplikacjach obsługujących obrazy indeksowane  

## Wymagania wstępne
Zanim przejdziemy do kodu, upewnij się, że masz następujące:

1. **Basic Knowledge of Java** – powinieneś być zaznajomiony z klasami, metodami i tworzeniem obiektów.  
2. **Java Development Kit (JDK) 8+** – zainstalowany i skonfigurowany w Twoim IDE.  
3. **IDE (IntelliJ IDEA, Eclipse, itp.)** – opcjonalne, ale bardzo zalecane dla łatwiejszego debugowania.  
4. **Aspose.PSD for Java Library** – pobierz ją **[here](https://releases.aspose.com/psd/java/)** i dodaj plik JAR do classpathu projektu.  
5. **Fundamental Graphic Design Concepts** – zrozumienie trybów kolorów, palet i podstawowych kształtów pomoże Ci podążać za instrukcją.

## Importowanie pakietów
Zanim przejdziemy do kodu, upewnijmy się, że wszystkie niezbędne pakiety zostały zaimportowane do Twojej aplikacji Java. Oto, czego będziesz potrzebować:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Te importy pozwolą Ci pracować z opcjami PSD, kolorami i manipulacją grafiką przy użyciu Aspose.PSD.

Teraz rozłożymy kod krok po kroku, aby **how to create PSD** pliki w trybie kolorów indeksowanych.

## Krok 1: Ustaw katalog dokumentu
Najpierw określ, gdzie zostanie zapisany wygenerowany plik PSD.

```java
String dataDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` ścieżką absolutną lub względną, np. `"/Users/YourName/Documents/"`.

## Krok 2: Utwórz instancję PsdOptions
`PsdOptions` przechowuje wszystkie ustawienia pliku, który zamierzasz wygenerować.

```java
PsdOptions createOptions = new PsdOptions();
```

## Krok 3: Ustaw podstawowe właściwości PsdOptions
Tutaj określamy lokalizację wyjściową, **set psd color mode** na `Indexed` oraz wersję PSD.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – pełna ścieżka nowego pliku.  
- **Color Mode** – `Indexed` informuje Aspose.PSD, że ma używać obrazu opartego na palecie.  
- **Version** – wersja formatu PSD (5 działa w większości nowoczesnych wersji Photoshopa).

## Krok 4: Utwórz paletę kolorów (Generate PSD Color Palette)
Zdefiniuj kolory, które będą dostępne w obrazie indeksowanym.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- Tablica `palette` może zawierać do 256 obiektów `Color`.  
- `CompressionMethod.RLE` zapewnia efektywną bezstratną kompresję dla obrazów indeksowanych.

## Krok 5: Utwórz płótno obrazu PSD
Teraz tworzymy pusty plik PSD o żądanych wymiarach.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Tworzy to płótno o wymiarach 500 × 500 pikseli, które używa wcześniej zdefiniowanej palety.

## Krok 6: Rysowanie grafiki na PSD
Dodaj zawartość wizualną — tutaj rysujemy prostą czerwoną elipsę na białym tle.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` wypełnia tło białym kolorem.  
- `drawEllipse` rysuje czerwoną elipsę o grubości 6 pikseli.

## Krok 7: Zapisz plik PSD
Na koniec zapisz obraz na dysku.

```java
psd.save();
```

Plik `Newsample_out.psd` pojawi się w katalogu, który określiłeś wcześniej.

## Typowe problemy i wskazówki
- **Palette Size** – Jeśli potrzebujesz więcej niż 4 kolory, po prostu dodaj je do tablicy `palette` (do 256).  
- **File Permissions** – Upewnij się, że proces Java ma dostęp do zapisu w `dataDir`.  
- **Incorrect Color Mode** – Zapomnienie o `createOptions.setColorMode(ColorModes.Indexed)` spowoduje utworzenie PSD w trybie RGB zamiast indeksowanego.  

## Najczęściej zadawane pytania

**Q: Czym jest Aspose.PSD for Java?**  
A: Aspose.PSD for Java to biblioteka umożliwiająca programowe manipulowanie plikami PSD (Photoshop) przy użyciu Javy.

**Q: Czy mogę używać Aspose.PSD za darmo?**  
A: Tak, możesz uzyskać dostęp do wersji próbnej Aspose.PSD **[here](https://releases.aspose.com/)**.

**Q: Czy muszę mieć zainstalowany Photoshop, aby pracować z Aspose.PSD?**  
A: Nie, możesz tworzyć i manipulować plikami PSD bez Photoshopa, ponieważ Aspose.PSD obsługuje wszystkie operacje samodzielnie.

**Q: Jak uzyskać tymczasową licencję na Aspose.PSD?**  
A: Możesz poprosić o tymczasową licencję **[here](https://purchase.aspose.com/temporary-license/)**.

**Q: Gdzie mogę uzyskać wsparcie dla Aspose.PSD?**  
A: Wsparcie możesz uzyskać na forum Aspose **[here](https://forum.aspose.com/c/psd/34)**.

## Zakończenie
Właśnie nauczyłeś się **how to create PSD** plików w trybie kolorów indeksowanych, wygenerowałeś własną paletę i dodałeś proste grafiki — wszystko przy użyciu Aspose.PSD for Java. Dzięki tym elementom możesz rozbudować projekt o bardziej złożone rysunki, zarządzanie warstwami i przetwarzanie wsadowe. Aby zgłębić temat, zapoznaj się z oficjalną dokumentacją API **[here](https://reference.aspose.com/psd/java/)** i dalej eksperymentuj z różnymi paletami oraz prymitywami rysunkowymi.

---

**Ostatnia aktualizacja:** 2026-03-15  
**Testowano z:** Aspose.PSD for Java 24.12 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
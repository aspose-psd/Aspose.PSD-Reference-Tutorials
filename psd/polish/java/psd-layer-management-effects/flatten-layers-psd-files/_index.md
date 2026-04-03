---
date: 2026-04-03
description: Dowiedz się, jak zmniejszyć rozmiar pliku PSD, spłaszczając warstwy przy
  użyciu Aspose.PSD for Java. Ten przewodnik krok po kroku pokazuje, jak szybko spłaszczyć
  pliki PSD.
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: Zmniejsz rozmiar pliku PSD poprzez spłaszczenie warstw – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: Zmniejsz rozmiar pliku PSD poprzez spłaszczenie warstw – Aspose.PSD Java
url: /pl/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zmniejsz rozmiar pliku PSD poprzez spłaszczenie warstw – Aspose.PSD Java

## Wprowadzenie

Jeśli kiedykolwiek otworzyłeś dokument Photoshop i zastanawiałeś się, jak **zmniejszyć rozmiar pliku PSD**, spłaszczenie warstw jest jednym z najskuteczniejszych trików. Dzięki Aspose.PSD for Java możesz programowo spłaszczyć cały plik PSD lub scalić tylko wybrane warstwy, dając Ci precyzyjną kontrolę nad wagą pliku bez utraty jakości wizualnej. W tym samouczku przeprowadzimy Cię przez oba podejścia — spłaszczenie całego obrazu oraz scalanie wybranych warstw — abyś mógł szybko zmniejszyć rozmiar swoich plików PSD i utrzymać płynny przepływ pracy.

## Szybkie odpowiedzi
- **Co robi spłaszczenie?** Łączy widoczne warstwy w jedną warstwę tła, usuwając informacje o warstwach i często zmniejszając rozmiar pliku.  
- **Czy mogę spłaszczyć tylko wybrane warstwy?** Tak, możesz scalić konkretne warstwy, pozostawiając inne nietknięte.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w celach deweloperskich; licencja komercyjna jest wymagana w produkcji.  
- **Jakiej wersji Javy wymaga?** JDK 8 lub wyższej.  
- **Czy spłaszczenie wpłynie na jakość obrazu?** Nie, wygląd wizualny pozostaje taki sam; zmienia się tylko struktura warstw.

## Co to jest „zmniejszenie rozmiaru pliku PSD”?

Zmniejszenie rozmiaru pliku PSD oznacza usunięcie niepotrzebnych danych — takich jak dodatkowe warstwy, ukryte kanały czy nadmiarowe metadane — aby plik stał się lżejszy i szybciej się ładował, udostępniał lub przetwarzał. Spłaszczenie warstw jest powszechną techniką, ponieważ usuwa oddzielne obiekty warstw, zachowując jednocześnie ostateczny obraz kompozycyjny.

## Dlaczego spłaszczyć warstwy przy użyciu Aspose.PSD for Java?

- **Automatyzacja:** Nie ma potrzeby ręcznego otwierania Photoshopa; integruj bezpośrednio w aplikacjach Java.  
- **Precyzja:** Wybierz spłaszczenie całego dokumentu lub tylko widocznych warstw (`flattenImage`) lub scalanie wybranych warstw (`mergeLayers`).  
- **Wydajność:** Mniejsze pliki ładują się szybciej i zużywają mniej pamięci w kolejnych procesach.  
- **Cross‑platform:** Działa na każdym systemie operacyjnym obsługującym Javę.

## Prerequisites

1. **Java Development Kit (JDK):** Zainstalowany JDK 8 lub nowszy.  
2. **Aspose.PSD for Java:** Pobierz bibliotekę z [here](https://releases.aspose.com/psd/java/).  
3. **IDE:** IntelliJ IDEA, Eclipse lub dowolne IDE kompatybilne z Javą.  
4. **Podstawowa znajomość Javy:** Przydatna, ale nieobowiązkowa do wykonania kroków.  
5. **Przykładowy PSD:** Plik z wieloma warstwami (użyjemy `ThreeRegularLayersSemiTransparent.psd`).

Teraz, gdy wszystko jest gotowe, zanurzmy się w kod.

## Importowanie pakietów

Aby rozpocząć, zaimportuj niezbędne klasy Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Te importy pozwalają nam ładować pliki PSD, pracować z ich warstwami i zapisywać wyniki.

## Krok 1: Spłaszczenie całego obrazu PSD

Spłaszczenie całego obrazu to najszybszy sposób na **zmniejszyć rozmiar pliku PSD**, ponieważ usuwa wszystkie indywidualne dane warstw.

### 1.1 Załaduj plik PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 Spłaszcz obraz

```java
im.flattenImage();
```

### 1.3 Zapisz spłaszczony obraz

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

Nowy plik zawiera jedną warstwę tła, co zazwyczaj skutkuje mniejszym rozmiarem PSD.

## Krok 2: Scalanie wybranych warstw (Jak spłaszczyć PSD selektywnie)

Czasami chcesz **spłaszczyć widoczne warstwy** lub połączyć podzbiór warstw, pozostawiając inne edytowalne.

### 2.1 Ponownie załaduj plik PSD

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 Zidentyfikuj i wybierz warstwy

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 Scal warstwy

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 Zastąp istniejące warstwy scaloną warstwą

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 Zapisz zaktualizowany plik PSD

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Teraz PSD zawiera tylko scaloną warstwę, osiągając zmniejszony rozmiar pliku przy zachowaniu warstw, które chciałeś zachować.

## Częste problemy i wskazówki

- **Kopia zapasowa przed spłaszczeniem:** Po spłaszczeniu warstw operacji nie można cofnąć. Zachowaj kopię oryginalnego PSD.  
- **Widoczność ma znaczenie:** `flattenImage()` scala tylko *widoczne* warstwy. Ukryj warstwy, które nie mają być uwzględnione.  
- **Zużycie pamięci:** Duże pliki PSD mogą zużywać znaczną ilość RAM; rozważ przetwarzanie ich na maszynie z wystarczającą ilością pamięci.  
- **Tryby mieszania:** Scalanie respektuje tryb mieszania każdej warstwy, więc wynik wizualny odpowiada temu, co widziałbyś w Photoshopie.

## Najczęściej zadawane pytania

**P: Czy mogę cofnąć spłaszczenie warstw w Aspose.PSD?**  
O: Nie, spłaszczenie jest nieodwracalne. Zawsze zachowuj kopię oryginalnego pliku.

**P: Czy można spłaszczyć tylko widoczne warstwy?**  
O: Tak. `flattenImage()` respektuje widoczność warstw, więc ukryj warstwy, które nie mają być spłaszczone przed wywołaniem metody.

**P: Czy spłaszczenie warstw zmniejsza rozmiar pliku?**  
O: Zazwyczaj tak. Usunięcie danych warstw i metadanych często prowadzi do mniejszego PSD, choć dokładne zmniejszenie zależy od zawartości.

**P: Czy mogę scalać warstwy o różnych trybach mieszania?**  
O: Absolutnie. Aspose.PSD scala warstwy, zachowując wygląd wizualny utworzony przez ich tryby mieszania.

**P: Co się stanie, jeśli spróbuję scalić nie‑sąsiadujące warstwy?**  
O: Aspose.PSD pozwala scalać dowolne warstwy niezależnie od ich kolejności w stosie; wynik odzwierciedla połączony wygląd.

---

**Ostatnia aktualizacja:** 2026-04-03  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}
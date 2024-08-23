---
title: Jak dodać gradient warstwy obrysu w Javie
linktitle: Jak dodać gradient warstwy obrysu w Javie
second_title: Aspose.PSD API Java
description: Dowiedz się, jak dodawać i dostosowywać gradienty warstw obrysów w plikach PSD za pomocą Aspose.PSD dla Java, korzystając z tego wszechstronnego samouczka krok po kroku.
type: docs
weight: 10
url: /pl/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## Wstęp
Czy zastanawiałeś się kiedyś, jak dodać gradient warstwy obrysu do swoich obrazów za pomocą Java? Cóż, jesteś we właściwym miejscu! Dzisiaj zanurzamy się w świat Aspose.PSD dla Java, potężnej biblioteki, która pomaga z łatwością manipulować plikami PSD. Niezależnie od tego, czy jesteś początkującym, czy doświadczonym programistą, ten przewodnik krok po kroku przeprowadzi Cię przez proces dodawania gradientu warstwy obrysu do plików PSD. Zatem zapnij pasy i przygotuj się na doskonalenie swoich umiejętności edycji grafiki!
## Warunki wstępne
Zanim zaczniemy, jest kilka rzeczy, które musisz mieć na miejscu. Upewnij się, że masz następujące elementy:
1.  Zestaw Java Development Kit (JDK): Upewnij się, że w systemie jest zainstalowany pakiet JDK. Można go pobrać z[stronie internetowej Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD dla biblioteki Java: Możesz pobrać ją z[Strona pobierania Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Zintegrowane środowisko programistyczne (IDE): dowolne IDE, takie jak IntelliJ IDEA, Eclipse lub NetBeans, będzie działać.
4.  Ważna licencja: Możesz uzyskać[licencja tymczasowa](https://purchase.aspose.com/temporary-license/) jeśli nie masz pełnego.
## Importuj pakiety
Na początek zaimportujmy niezbędne pakiety. Umożliwią nam one użycie klas i metod wymaganych do manipulowania plikiem PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
Podzielmy teraz przykład na wiele kroków, aby lepiej zrozumieć.
## Krok 1: Załaduj plik PSD
 Najpierw musimy załadować plik PSD, który chcemy zmodyfikować. Skorzystamy z`PsdLoadOptions` aby określić, że chcemy załadować zasoby efektów.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Krok 2: Uzyskaj dostęp do efektu obrysu
Następnie musimy uzyskać dostęp do efektu obrysu warstwy, która nas interesuje. Tutaj zakładamy, że jest to trzecia warstwa (indeks 2) w pliku PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Krok 3: Sprawdź właściwości efektu obrysu
Przed wprowadzeniem jakichkolwiek zmian sprawdźmy właściwości efektu obrysu, aby mieć pewność, że modyfikujemy prawidłowe ustawienia.
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
## Krok 4: Zmodyfikuj ustawienia wypełnienia gradientowego
Teraz czas zmodyfikować ustawienia wypełnienia gradientowego zgodnie z naszymi wymaganiami. Zmienimy kolor, krycie, tryb mieszania i inne właściwości.
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
## Krok 5: Dodaj i zmodyfikuj punkty koloru i przezroczystości
Dodajmy nowe punkty koloru i przezroczystości oraz zmodyfikujmy istniejące, aby uzyskać pożądany efekt gradientu.
```java
// Dodaj nowy punkt koloru
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Zmień lokalizację poprzedniego punktu
fillSettings.getColorPoints()[1].setLocation(1899);
// Dodaj nowy punkt przezroczystości
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Zmień lokalizację poprzedniego punktu przezroczystości
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Krok 6: Zapisz zmodyfikowany plik PSD
Po dokonaniu wszystkich niezbędnych modyfikacji musimy zapisać plik PSD.
```java
im.save(exportPath);
```
## Krok 7: Sprawdź modyfikacje
Na koniec załadujmy zapisany plik PSD i sprawdźmy, czy nasze zmiany zostały zastosowane poprawnie.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Sprawdź punkty koloru
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Sprawdź punkty przezroczystości
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```
## Wniosek
I masz to! Teraz wiesz, jak dodawać i manipulować gradientami warstw obrysów w plikach PSD przy użyciu Aspose.PSD dla Java. W tym samouczku omówiono ładowanie pliku PSD, uzyskiwanie dostępu i modyfikowanie efektów obrysu oraz zapisywanie zmian. Dzięki tym umiejętnościom możesz tworzyć atrakcyjne wizualnie gradienty i dostosowywać pliki PSD do swoich potrzeb.
## Często zadawane pytania
### Co to jest Aspose.PSD dla Java?
Aspose.PSD dla Java to biblioteka, która umożliwia programistom pracę z plikami PSD w aplikacjach Java, zapewniając funkcje tworzenia, manipulowania i konwertowania plików PSD.
### Czy potrzebuję licencji, aby używać Aspose.PSD dla Java?
 Tak, potrzebujesz ważnej licencji, aby używać Aspose.PSD dla Java. Możesz dostać[licencja tymczasowa](https://purchase.aspose.com/temporary-license/) w celach ewaluacyjnych.
### Czy mogę używać Aspose.PSD dla Java do tworzenia plików PSD od podstaw?
Absolutnie! Aspose.PSD dla Java zapewnia kompleksowe interfejsy API do programowego tworzenia i manipulowania plikami PSD.
### Czy możliwe jest zastosowanie innych efektów przy użyciu Aspose.PSD dla Java?
Tak, możesz zastosować różne efekty, takie jak cień, poświata i inne, używając Aspose.PSD dla Java.
### Gdzie mogę znaleźć dokumentację Aspose.PSD dla Java?
 Można znaleźć dokumentację[Tutaj](https://reference.aspose.com/psd/java/).
---
title: Praca z osią czasu w Aspose.PSD dla .NET
linktitle: Praca z osią czasu
second_title: Aspose.PSD API .NET
description: Ulepsz manipulację obrazami PSD za pomocą klasy Aspose.PSD for .NET Timeline. Kontroluj właściwości ramki, stany warstw i bez wysiłku uwalniaj możliwości twórcze.
type: docs
weight: 16
url: /pl/net/psd-file-manipulation/timeline/
---
## Wstęp
dynamicznym świecie projektowania graficznego i manipulacji obrazami umiejętność kontrolowania i manipulowania osią czasu obrazów jest kluczowa. Aspose.PSD dla .NET zapewnia potężne rozwiązanie dzięki klasie Timeline. Ta zaawansowana funkcja umożliwia użytkownikom wprowadzanie zmian na osi czasu PsdImage, takich jak zmiana opóźnienia klatek, edytowanie stanów warstw w określonych klatkach i nie tylko.
## Warunki wstępne
Zanim zagłębisz się w ekscytujące możliwości, jakie oferuje klasa Oś czasu, upewnij się, że spełniasz następujące wymagania wstępne:
-  Biblioteka Aspose.PSD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.PSD dla .NET. Można go pobrać z[Dokumentacja Aspose.PSD dla .NET](https://reference.aspose.com/psd/net/).
-  Katalogi dokumentów i wyników: Zdefiniuj ścieżki do katalogów dokumentów i wyników w kodzie. Dostosuj`baseDir` I`outputDir` zmienne zgodnie ze strukturą projektu.
Przyjrzyjmy się teraz, jak krok po kroku wykorzystać klasę Timeline.
## Importuj przestrzenie nazw
Aby rozpocząć pracę z klasą Timeline, zaimportuj niezbędne przestrzenie nazw do swojego kodu:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Krok 1: Załaduj obraz PSD
Rozpocznij od załadowania obrazu PSD z określonego pliku źródłowego. Upewnij się, że ścieżka pliku źródłowego jest poprawnie ustawiona:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Twój kod do dalszych operacji znajduje się tutaj
}
```
## Krok 2: Uzyskaj dostęp do osi czasu
Po załadowaniu obrazu PSD uzyskaj dostęp do osi czasu, używając następującego kodu:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Krok 3: Zmień metodę usuwania
Manipuluj metodą usuwania określonej ramki. W tym przykładzie zmieniamy metodę usuwania ramki 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Krok 4: Dostosuj opóźnienie ramki
Zmodyfikuj opóźnienie określonej klatki. Tutaj zmieniamy opóźnienie klatki 2 na 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Krok 5: Edytuj stan warstwy
Zmień krycie „warstwy 1” w określonej klatce. W tym przypadku ustawiliśmy krycie na 50 w klatce 2:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Krok 6: Przesuń warstwę
Przesuń „Warstwa 1” do lewego dolnego rogu określonej klatki (w tym przykładzie klatka 3):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Krok 7: Dodaj nową ramkę
Dodaj nową klatkę do osi czasu:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Krok 8: Zmień tryb mieszania
Zmień tryb mieszania „Warstwa 1” w określonej klatce (w tym przypadku klatka 4):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Krok 9: Zapisz zmiany
Zastosuj zmiany z powrotem do instancji PsdImage i zapisz zmodyfikowany obraz PSD:
```csharp
psdImage.Save(outputPsd);
```
## Krok 10: Oczyść
Na koniec wyczyść, usuwając tymczasowy plik wyjściowy:
```csharp
File.Delete(outputPsd);
```
## Wniosek

Podsumowując, klasa Timeline w Aspose.PSD dla .NET umożliwia programistom uzyskanie szczegółowej kontroli nad osią czasu obrazów PSD. Wykonując serię prostych kroków, możesz manipulować właściwościami ramki, stanami warstw i nie tylko, otwierając obszar kreatywnych możliwości.

## Często zadawane pytania

### P1: Czy Aspose.PSD dla .NET jest odpowiedni dla początkujących?

A1: Absolutnie! Aspose.PSD dla .NET zapewnia przyjazny dla użytkownika interfejs i obszerną dokumentację, dzięki czemu jest dostępny zarówno dla początkujących, jak i doświadczonych programistów.

### P2: Czy mogę zastosować zmiany na osi czasu do obrazów GIF?

Odpowiedź 2: Klasa Timeline została zaprojektowana specjalnie dla obrazów PSD. Informacje na temat manipulacji GIF można znaleźć w Aspose.GIF dla .NET.

### P3: Gdzie mogę znaleźć dodatkowe wsparcie lub omówić problemy?

 A3: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie społeczności i dyskusje na temat problemów.

### P4: Jak mogę uzyskać tymczasową licencję na Aspose.PSD dla .NET?

 A4: Zdobądź licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Jakie są kluczowe korzyści z używania Aspose.PSD dla .NET?

O5: Aspose.PSD dla .NET oferuje zaawansowane możliwości przetwarzania obrazu, manipulację plikami PSD i renderowanie o wysokiej wydajności.
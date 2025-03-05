---
title: Dodawanie warstwy obrysu ze wzorem w Aspose.PSD dla .NET
linktitle: Dodawanie warstwy obrysu ze wzorem
second_title: Aspose.PSD API .NET
description: Wzbogacaj swoje pliki PSD warstwami obrysów i wzorami za pomocą Aspose.PSD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zapewnić bezproblemową integrację.
type: docs
weight: 13
url: /pl/net/layer-effects/adding-stroke-layer-pattern/
---
## Wstęp

Ulepszanie plików PSD (dokument programu Photoshop) warstwami obrysów i wzorami może dodać dynamiczny akcent do Twoich projektów. W tym samouczku odkryjemy, jak wykorzystać Aspose.PSD dla .NET, aby bez wysiłku dodać warstwę obrysu ze wzorem do plików PSD. Aspose.PSD to potężna biblioteka .NET, która zapewnia kompleksową obsługę manipulowania plikami PSD, co czyni ją nieocenionym narzędziem zarówno dla programistów, jak i projektantów.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Podstawowa znajomość języka programowania C#.
- Program Visual Studio zainstalowany na Twoim komputerze.
-  Biblioteka Aspose.PSD dla .NET, którą możesz pobrać[Tutaj](https://releases.aspose.com/psd/net/).

## Importuj przestrzenie nazw

Upewnij się, że zaimportowałeś niezbędne przestrzenie nazw w kodzie C#:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## Krok 1: Skonfiguruj swoje środowisko

Zacznij od zdefiniowania katalogów źródłowych i wyjściowych w kodzie C#:

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## Krok 2: Załaduj plik PSD

Załaduj plik PSD przy użyciu klasy PsdImage Aspose.PSD:

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Twój kod do przetwarzania pliku PSD znajduje się tutaj
}
```

## Krok 3: Przygotuj nowe dane wzorca

Zdefiniuj nowy wzór i jego granice:

```csharp
var newPattern = new int[]
{
    // Tutaj znajdują się kolory Twojego wzoru
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## Krok 4: Zmodyfikuj warstwę obrysu

Uzyskaj dostęp do warstwy obrysu i zaktualizuj jej właściwości:

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

// Sprawdź i zaktualizuj właściwości obrysu
// ...

// Zaktualizuj krycie i tryb mieszania
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## Krok 5: Zaktualizuj informacje o wzorcu

Zaktualizuj informacje o wzorze w pliku PSD:

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        // Twój kod do aktualizacji informacji o wzorcu znajduje się tutaj
    }
}

// Zapisz zmodyfikowany plik PSD
im.Save(exportPath);
```

## Krok 6: Sprawdź zmiany

Załaduj zmodyfikowany plik PSD i zweryfikuj zmiany:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    // Twój kod do weryfikacji zmian znajduje się tutaj
}
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak dodać warstwę obrysu ze wzorem w Aspose.PSD dla .NET. Ta wszechstronna biblioteka umożliwia programistom tworzenie atrakcyjnych wizualnie projektów i zwiększanie elastyczności plików PSD.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.PSD dla .NET z dowolną wersją Visual Studio?

O1: Tak, Aspose.PSD dla .NET jest kompatybilny z różnymi wersjami Visual Studio.

### P2: Jak mogę uzyskać tymczasową licencję na Aspose.PSD?

 A2: Odwiedź[Tutaj](https://purchase.aspose.com/temporary-license/) w celu uzyskania licencji tymczasowej.

### P3: Czy dostępne są przykładowe pliki PSD do testowania?

 O3: Przykładowe pliki PSD można znaleźć w dokumentacji[Tutaj](https://reference.aspose.com/psd/net/).

### P4: Czy Aspose.PSD nadaje się do przetwarzania wsadowego plików PSD?

Odpowiedź 4: Oczywiście, Aspose.PSD dla .NET zapewnia solidną obsługę przetwarzania wsadowego.

### P5: Gdzie mogę szukać pomocy lub wziąć udział w dyskusjach społeczności?

 A5: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie i interakcje społeczne.
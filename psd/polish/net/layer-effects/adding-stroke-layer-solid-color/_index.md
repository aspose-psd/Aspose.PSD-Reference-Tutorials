---
title: Dodawanie warstwy obrysu z jednolitym kolorem w Aspose.PSD dla .NET
linktitle: Dodawanie warstwy obrysu z jednolitym kolorem
second_title: Aspose.PSD API .NET
description: Zwiększ swoje umiejętności manipulacji obrazami .NET dzięki Aspose.PSD. Naucz się krok po kroku dodawać warstwy obrysów w jednolitych kolorach.
weight: 11
url: /pl/net/layer-effects/adding-stroke-layer-solid-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodawanie warstwy obrysu z jednolitym kolorem w Aspose.PSD dla .NET

## Wstęp

W dziedzinie programowania .NET powszechnym wymogiem jest tworzenie atrakcyjnych wizualnie obrazów. Aspose.PSD dla .NET zapewnia potężny zestaw narzędzi do płynnego manipulowania i ulepszania obrazów. Jedną z podstawowych funkcji jest dodanie warstwy obrysu o jednolitym kolorze, która nadaje obrazom żywotność i głębię. W tym samouczku przeprowadzimy Cię krok po kroku przez proces korzystania z Aspose.PSD dla .NET.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Podstawowa wiedza z zakresu programowania .NET.
- Program Visual Studio zainstalowany na Twoim komputerze.
- Biblioteka Aspose.PSD dla .NET. Można go pobrać z[strona internetowa](https://releases.aspose.com/psd/net/).

## Importuj przestrzenie nazw

Zacznij od zaimportowania niezbędnych przestrzeni nazw, aby wykorzystać funkcjonalność Aspose.PSD dla .NET:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## Krok 1: Załaduj plik PSD

Rozpocznij od załadowania pliku PSD, który chcesz ulepszyć warstwą obrysu. Upewnij się, że masz poprawną ścieżkę pliku:

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Kod dalszych kroków zostanie dodany tutaj
}
```

## Krok 2: Uzyskaj dostęp do właściwości efektu obrysu

Pobierz właściwości efektu obrysu z pliku PSD:

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## Krok 3: Dostosuj ustawienia obrysu

Zmodyfikuj ustawienia obrysu zgodnie ze swoimi preferencjami. W tym przykładzie zmieniamy kolor na żółty, ustawiamy krycie na 127 i używamy trybu mieszania kolorów:

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## Krok 4: Zapisz edytowany obraz

Zapisz obraz po zastosowaniu zmian warstwy obrysu:

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## Krok 5: Sprawdź zmiany

Upewnij się, że zmiany zostały prawidłowo zastosowane, ładując i sprawdzając edytowany obraz:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // Tutaj zostanie dodany kod umożliwiający weryfikację zmian
}
```

Powtórz te kroki, aby uzyskać dodatkowe korekty lub poeksperymentuj z różnymi efektami obrysu, aby uzyskać pożądany efekt wizualny.

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak dodać warstwę obrysu o jednolitym kolorze przy użyciu Aspose.PSD dla .NET. Ta potężna funkcja otwiera świat możliwości ulepszania obrazów w środowisku .NET.

## Często zadawane pytania

### P1: Czy Aspose.PSD dla .NET jest kompatybilny z najnowszymi wersjami platformy .NET?

O1: Tak, Aspose.PSD dla .NET jest regularnie aktualizowany, aby zapewnić kompatybilność z najnowszymi wersjami platformy .NET.

### P2: Czy mogę używać Aspose.PSD for .NET w projektach komercyjnych?

A2: Absolutnie! Aspose.PSD dla .NET jest produktem komercyjnym i możesz go używać w swoich projektach, kupując licencję.

### P3: Gdzie mogę znaleźć więcej przykładów i dokumentacji dla Aspose.PSD dla .NET?

 A3: Poznaj[dokumentacja](https://reference.aspose.com/psd/net/) w celu uzyskania wyczerpujących przykładów i wskazówek.

### P4: Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla .NET?

 A4: Tak, możesz uzyskać bezpłatną wersję próbną od[strona z wydaniami](https://releases.aspose.com/).

### P5: Jak mogę uzyskać wsparcie dla Aspose.PSD dla .NET?

 A5: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) szukać pomocy i nawiązywać kontakt ze społecznością.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

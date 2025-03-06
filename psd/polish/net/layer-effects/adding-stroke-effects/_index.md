---
title: Dodawanie efektów obrysu do warstw w Aspose.PSD dla .NET
linktitle: Dodawanie efektów obrysu do warstw
second_title: Aspose.PSD API .NET
description: Popraw estetykę obrazu dzięki Aspose.PSD dla .NET. Naucz się dodawać efekty obrysów krok po kroku. Pobierz, kup lub wypróbuj bezpłatną wersję próbną już teraz.
weight: 10
url: /pl/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodawanie efektów obrysu do warstw w Aspose.PSD dla .NET

## Wstęp

Witamy w tym samouczku krok po kroku dotyczącym dodawania efektów obrysu do warstw w Aspose.PSD dla .NET. Zwiększenie atrakcyjności wizualnej obrazów jest proste dzięki efektowi obrysu, a Aspose.PSD sprawia, że jest to płynne dla programistów .NET. W tym przewodniku przeprowadzimy Cię przez cały proces, podając jasne kroki i przykłady, które pomogą Ci opanować tę zaawansowaną funkcję.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Aspose.PSD dla .NET: Pobierz i zainstaluj bibliotekę Aspose.PSD z[strona internetowa](https://releases.aspose.com/psd/net/).

- Katalog dokumentów: Przygotuj katalog zawierający dokument PSD, do którego chcesz zastosować efekty obrysu.

- Katalog wyjściowy: posiada oddzielny katalog do przechowywania obrazów wyjściowych z efektami obrysu.

- Visual Studio: Upewnij się, że masz skonfigurowane Visual Studio lub inne preferowane środowisko programistyczne .NET.

## Importuj przestrzenie nazw

W swoim projekcie .NET uwzględnij niezbędne przestrzenie nazw, aby wykorzystać funkcjonalność Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Załaduj dokument PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Twój kod do ładowania dokumentu PSD znajduje się tutaj
}
```

## Krok 2: Dodaj efekt obrysu koloru

```csharp
// Dodaje wypełnienie kolorem w pozycji Wewnątrz
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Krok 3: Pozycja zewnętrzna

```csharp
// Dodaje wypełnienie kolorem w pozycji Na zewnątrz
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Krok 4: Pozycja środkowa

```csharp
// Dodaje wypełnienie kolorem w pozycji Środek
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Powtórz podobne kroki dla wypełnień gradientowych i wzorków, odpowiednio dostosowując ustawienia.

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się dodawać efekty obrysu do warstw przy użyciu Aspose.PSD dla .NET. Eksperymentuj z różnymi ustawieniami, aby uzyskać pożądany efekt wizualny na swoich obrazach.

## Często zadawane pytania

### P1: Czy mogę zastosować efekty obrysu tylko do określonych warstw?

Odpowiedź 1: Tak, możesz kierować reklamy na określone warstwy, dostosowując indeks warstw w kodzie.

### P2: Czy Aspose.PSD jest kompatybilny z najnowszym frameworkiem .NET?

A2: Absolutnie! Aspose.PSD został zaprojektowany tak, aby bezproblemowo integrować się z najnowszymi frameworkami .NET.

### P3: Jak mogę dostosować kolor obrysu?

 A3: Po prostu zmodyfikuj plik`Color` właściwość w kodzie, aby uzyskać pożądany kolor obrysu.

### P4: Czy Aspose.PSD obsługuje przetwarzanie wsadowe wielu plików PSD?

Odpowiedź 4: Tak, możesz przeglądać wiele plików PSD w pętli i stosować efekt obrysu, stosując podobne podejście.

### P5: Czy mogę skorzystać z wersji próbnej przed zakupem Aspose.PSD?

 A5: Oczywiście! Chwyć[bezpłatna wersja próbna](https://releases.aspose.com/) aby poznać możliwości Aspose.PSD przed dokonaniem zakupu.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
title: Dodawanie efektów w czasie wykonywania w Aspose.PSD dla .NET
linktitle: Dodawanie efektów w czasie wykonywania
second_title: Aspose.PSD API .NET
description: Poznaj dynamiczne ulepszenia obrazu za pomocą Aspose.PSD dla .NET. Z łatwością dodawaj efekty w czasie wykonywania.
type: docs
weight: 10
url: /pl/net/image-effects/add-effect-runtime/
---
## Wstęp

Poprawa atrakcyjności wizualnej obrazów jest powszechnym wymaganiem w aplikacjach do projektowania graficznego i przetwarzania obrazów. W tym samouczku omówimy, jak dodawać efekty w czasie wykonywania przy użyciu Aspose.PSD dla .NET. Aspose.PSD to potężny interfejs API, który umożliwia programistom bezproblemową pracę z plikami Adobe Photoshop. 

## Warunki wstępne

Zanim przejdziemy do przewodnika krok po kroku, upewnij się, że posiadasz następujące elementy:

- Podstawowa znajomość C# i frameworku .NET.
-  Zainstalowano Aspose.PSD dla .NET. Można go pobrać z[Tutaj](https://releases.aspose.com/psd/net/).

## Importuj przestrzenie nazw

Aby rozpocząć, upewnij się, że w projekcie C# zostały uwzględnione niezbędne przestrzenie nazw. Te przestrzenie nazw są niezbędne do wykorzystania funkcjonalności zapewnianej przez Aspose.PSD.

```csharp
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageLoadOptions;
```

## Krok 1: Skonfiguruj katalog dokumentów

```csharp
string dataDir = "Your Document Directory";
```

Zastąp „Twój katalog dokumentów” rzeczywistą ścieżką, w której znajdują się pliki PSD.

## Krok 2: Załaduj obraz PSD z zasobami efektów

```csharp
string sourceFileName = dataDir + "ThreeRegularLayers.psd";
string exportPath = dataDir + "ThreeRegularLayersChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

Ten krok ładuje obraz PSD, umożliwiając załadowanie zasobów efektów.

## Krok 3: Dodaj efekt warstwy nakładki koloru

```csharp
var effect = im.Layers[1].BlendingOptions.AddColorOverlay();
effect.Color = Color.Green;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

Tutaj dodajemy efekt nakładki kolorów na drugą warstwę obrazu PSD. Możesz dostosować kolor, krycie i tryb mieszania zgodnie ze swoimi preferencjami.

## Krok 4: Zapisz zmodyfikowany obraz

```csharp
im.Save(exportPath);
```

Na koniec zapisz obraz z zastosowanym efektem w określonej ścieżce eksportu.

## Wniosek

Dodawanie efektów w czasie wykonywania w Aspose.PSD dla .NET jest prostym procesem. Za pomocą zaledwie kilku linii kodu możesz dynamicznie poprawić atrakcyjność wizualną swoich obrazów. Eksperymentuj z różnymi efektami i parametrami, aby osiągnąć pożądane rezultaty.

## Często zadawane pytania

### P1: Czy Aspose.PSD jest kompatybilny z najnowszym frameworkiem .NET?

O1: Tak, Aspose.PSD jest regularnie aktualizowany, aby zapewnić kompatybilność z najnowszymi wersjami platformy .NET.

### P2: Czy mogę zastosować wiele efektów na jednej warstwie?

A2: Absolutnie! Można łączyć wiele efektów na warstwie, aby tworzyć złożone ulepszenia wizualne.

### P3: Czy są jakieś ograniczenia dotyczące typów efektów, które mogę dodać?

O3: Aspose.PSD oferuje szeroką gamę efektów, ale zaleca się sprawdzenie dokumentacji w celu uzyskania szczegółowych informacji na temat obsługiwanych efektów.

### P4: Jak mogę uzyskać tymczasową licencję do celów testowych?

 A4: Możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/) do testowania i oceny.

### P5: Gdzie mogę znaleźć dodatkowe wsparcie i dyskusje społeczności?

 A5: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie i dyskusję.
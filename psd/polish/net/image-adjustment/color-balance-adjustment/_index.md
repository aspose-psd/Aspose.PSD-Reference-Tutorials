---
title: Stosowanie regulacji balansu kolorów w Aspose.PSD dla .NET
linktitle: Stosowanie regulacji balansu kolorów
second_title: Aspose.PSD API .NET
description: Popraw kolory obrazu PSD bez wysiłku dzięki funkcji regulacji balansu kolorów Aspose.PSD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać oszałamiające rezultaty.
weight: 14
url: /pl/net/image-adjustment/color-balance-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stosowanie regulacji balansu kolorów w Aspose.PSD dla .NET

## Wstęp

Witamy w tym kompleksowym przewodniku na temat stosowania regulacji balansu kolorów w Aspose.PSD dla .NET! Aspose.PSD to potężna biblioteka .NET, która umożliwia programistom wydajną pracę z plikami PSD. W tym samouczku skupimy się na funkcji regulacji balansu kolorów, która umożliwia łatwą poprawę balansu kolorów obrazów PSD.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Biblioteka Aspose.PSD dla .NET: Pobierz i zainstaluj bibliotekę z[Witryna Aspose.PSD](https://releases.aspose.com/psd/net/).
- Środowisko programistyczne: Upewnij się, że na komputerze skonfigurowano działające środowisko programistyczne .NET.
- Plik PSD: Przygotuj plik PSD, do którego chcesz zastosować korekcję balansu kolorów.

## Importuj przestrzenie nazw

W swoim projekcie .NET uwzględnij niezbędne przestrzenie nazw, aby móc korzystać z funkcji Aspose.PSD. Dodaj następujące linie do swojego kodu:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Podzielmy teraz proces regulacji balansu kolorów na kilka etapów:

## Krok 1: Załaduj plik PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Kod regulacji balansu kolorów zostanie dodany w poniższych krokach.
}
```

## Krok 2: Uzyskaj dostęp i dostosuj balans kolorów

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Krok 3: Zapisz dostosowany obraz

```csharp
im.Save(outputPath);
```

Teraz pomyślnie zastosowałeś regulację balansu kolorów do swojego pliku PSD przy użyciu Aspose.PSD dla .NET!

## Wniosek

Gratulacje! Nauczyłeś się, jak poprawić balans kolorów obrazów PSD za pomocą Aspose.PSD dla .NET. Eksperymentuj z różnymi wartościami balansu, aby uzyskać pożądane efekty wizualne.

## Często zadawane pytania

### P1: Czy mogę zastosować regulację balansu kolorów do wielu warstw?

O1: Tak, możesz przeglądać wszystkie warstwy w pliku PSD i w razie potrzeby dostosowywać balans kolorów.

### P2: Czy Aspose.PSD dla .NET nadaje się do przetwarzania wsadowego plików PSD?

A2: Absolutnie! Aspose.PSD zapewnia wydajne możliwości przetwarzania wsadowego plików PSD.

### P3: Jak mogę uzyskać tymczasową licencję na Aspose.PSD dla .NET?

 A3: Odwiedź[Licencja tymczasowa Aspose.PSD](https://purchase.aspose.com/temporary-license/) o licencję tymczasową.

### P4: Gdzie mogę znaleźć więcej przykładów i dokumentacji?

 A4: Poznaj[Dokumentacja Aspose.PSD](https://reference.aspose.com/psd/net/) szczegółowe przykłady i przewodniki.

### P5: Jakie opcje wsparcia są dostępne dla Aspose.PSD dla .NET?

 A5: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie społeczności i dyskusje.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

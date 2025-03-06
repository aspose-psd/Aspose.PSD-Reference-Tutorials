---
title: Tworzenie kształtów eliptycznych za pomocą Aspose.PSD dla .NET
linktitle: Tworzenie kształtów eliptycznych za pomocą Aspose.PSD dla .NET
second_title: Aspose.PSD API .NET
description: Dowiedz się, jak rysować kształty eliptyczne w .NET przy użyciu Aspose.PSD. Przewodnik krok po kroku z przykładami kodu. Twórz oszałamiającą grafikę bez wysiłku.
weight: 13
url: /pl/net/psd-drawing-techniques/creating-elliptical-shapes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie kształtów eliptycznych za pomocą Aspose.PSD dla .NET

## Wstęp

Witamy w naszym obszernym przewodniku na temat tworzenia kształtów eliptycznych przy użyciu Aspose.PSD dla .NET. Aspose.PSD to potężna biblioteka .NET, która umożliwia programistom manipulowanie i konwertowanie plików programu Photoshop bez konieczności stosowania programu Adobe Photoshop. W tym samouczku przeprowadzimy Cię przez proces rysowania kształtów eliptycznych przy użyciu biblioteki.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Biblioteka Aspose.PSD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.PSD w projekcie .NET. Można go pobrać z[Aspose.PSD dla dokumentacji .NET](https://reference.aspose.com/psd/net/).

- Środowisko .NET: W tym samouczku założono, że posiadasz praktyczną wiedzę na temat środowiska .NET.

## Importuj przestrzenie nazw

Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw do swojego projektu. Dzięki temu masz dostęp do klas i metod wymaganych do rysowania kształtów eliptycznych. Oto przykład:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Podzielmy teraz proces tworzenia kształtów eliptycznych na kilka etapów:

## Krok 1: Skonfiguruj katalog dokumentów

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";
```

## Krok 2: Utwórz instancję BmpOptions

```csharp
// Utwórz instancję BmpOptions i ustaw jej różne właściwości
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## Krok 3: Utwórz instancję obrazu

```csharp
// Utwórz instancję Image
using (Image image = new PsdImage(100, 100))
{
    // Utwórz i zainicjuj instancję klasy Graphics i powierzchni Clear Graphics
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Krok 4: Narysuj kropkowany kształt elipsy

```csharp
    // Narysuj kształt kropkowanej elipsy, określając obiekt Pióro o kolorze czerwonym i otaczający go prostokąt
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Krok 5: Narysuj ciągły kształt elipsy

```csharp
    //Narysuj ciągły kształt elipsy, określając obiekt Pióro z solidnym pędzlem w kolorze niebieskim i otaczającym go prostokątem
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Eksportuj obraz do formatu pliku bmp.
    image.Save(outpath, saveOptions);
}
```

## Wniosek

Gratulacje! Pomyślnie utworzyłeś kształty eliptyczne przy użyciu Aspose.PSD dla .NET. W tym samouczku omówiono podstawowe kroki, od skonfigurowania środowiska po rysowanie zarówno kropkowanych, jak i ciągłych kształtów elips.

## Często zadawane pytania

### P1: Gdzie mogę znaleźć dokumentację Aspose.PSD dla .NET?

 Odpowiedź 1: Dokumentacja jest dostępna[Tutaj](https://reference.aspose.com/psd/net/).

### P2: Jak pobrać Aspose.PSD dla .NET?

 Odpowiedź 2: Możesz pobrać go ze strony wydania[Tutaj](https://releases.aspose.com/psd/net/).

### P3: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 3: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać wsparcie dla Aspose.PSD dla .NET?

 Odpowiedź 4: Odwiedź forum pomocy technicznej[Tutaj](https://forum.aspose.com/c/psd/34).

### P5: Czy potrzebuję tymczasowej licencji do testowania?

 Odpowiedź 5: Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

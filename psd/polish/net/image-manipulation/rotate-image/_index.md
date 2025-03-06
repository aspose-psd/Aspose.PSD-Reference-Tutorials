---
title: Obracanie obrazu w Aspose.PSD dla .NET
linktitle: Obracanie obrazu
second_title: Aspose.PSD API .NET
description: Naucz się bez wysiłku obracać obrazy w .NET za pomocą Aspose.PSD. Postępuj zgodnie z naszym samouczkiem krok po kroku.
weight: 15
url: /pl/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obracanie obrazu w Aspose.PSD dla .NET

## Wstęp

Jeśli zagłębiasz się w świat manipulacji obrazami za pomocą .NET, Aspose.PSD jest Twoim narzędziem do płynnego i wydajnego przetwarzania obrazów. W tym samouczku skupimy się na podstawowym zadaniu – obracaniu obrazu za pomocą Aspose.PSD dla .NET. Postępuj zgodnie z instrukcjami, dzieląc proces na proste, wykonalne kroki.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że spełnione są następujące wymagania wstępne:

-  Biblioteka Aspose.PSD dla .NET: Pobierz i zainstaluj bibliotekę z[Dokumentacja Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Twój katalog dokumentów: skonfiguruj katalog, w którym przechowywane są Twoje obrazy. Zastąp „Twój katalog dokumentów” we fragmencie kodu ścieżką do tego katalogu.

## Importuj przestrzenie nazw

Upewnij się, że uwzględniłeś niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności Aspose.PSD. Dodaj następujące wiersze na początku projektu .NET:

```csharp
using Aspose.PSD.ImageOptions;
```

## Krok 1: Załaduj obraz

```csharp
string sourceFile = dataDir + @"sample.psd";

// Załaduj istniejący obraz do instancji klasy RasterImage
using (Image image = Image.Load(sourceFile))
{
```

## Krok 2: Obróć obraz

```csharp
    // Obróć obraz o 270 stopni w prawo
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Krok 3: Zapisz obrócony obraz

```csharp
    // Zapisz obrócony obraz jako plik JPEG
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

To wszystko! Za pomocą zaledwie kilku linii kodu udało Ci się obrócić obraz za pomocą Aspose.PSD dla .NET.

## Wniosek

tym samouczku omówiliśmy podstawy obracania obrazów przy użyciu Aspose.PSD dla .NET. Aspose.PSD zapewnia solidny zestaw narzędzi do manipulacji obrazami, co czyni go niezbędną biblioteką dla programistów .NET. Eksperymentuj z różnymi obrotami i odkrywaj dalsze możliwości usprawniające procesy przetwarzania obrazu.

## Często zadawane pytania

### P1: Czy mogę obracać obrazy o niestandardowy kąt przy użyciu Aspose.PSD?

 Tak, Aspose.PSD pozwala określić niestandardowy kąt obrotu. Po prostu wymień`RotateFlipType.Rotate270FlipNone` zgodnie z żądanym kątem obrotu.

### P2: Czy Aspose.PSD jest kompatybilny z różnymi formatami obrazów?

 Absolutnie. Aspose.PSD obsługuje szeroką gamę formatów obrazów, w tym PSD, JPEG, PNG i inne. Sprawdź[dokumentacja](https://reference.aspose.com/psd/net/) dla pełnej listy.

### P3: Jak mogę uzyskać tymczasową licencję na Aspose.PSD?

 Odwiedź[strona licencji tymczasowej](https://purchase.aspose.com/temporary-license/) na stronie internetowej Aspose w celu uzyskania tymczasowej licencji do celów ewaluacyjnych.

### P4: Gdzie mogę znaleźć wsparcie dla Aspose.PSD?

 W razie jakichkolwiek pytań lub pomocy odwiedź stronę[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) i łącz się ze społecznością.

### P5: Czy mogę kupić Aspose.PSD do użytku komercyjnego?

 Z pewnością. Poznaj[strona zakupu](https://purchase.aspose.com/buy) aby nabyć licencję dostosowaną do Twoich potrzeb.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

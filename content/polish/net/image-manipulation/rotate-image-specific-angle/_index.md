---
title: Obracanie obrazu pod określonym kątem w Aspose.PSD dla .NET
linktitle: Obracanie obrazu pod określonym kątem
second_title: Aspose.PSD API .NET
description: Poznaj moc Aspose.PSD dla .NET. Obracaj obrazy bez wysiłku pod określonym kątem. Pobierz bibliotekę i zacznij płynnie manipulować obrazami.
type: docs
weight: 16
url: /pl/net/image-manipulation/rotate-image-specific-angle/
---
Jeśli zagłębiasz się w świat manipulacji obrazami za pomocą .NET, Aspose.PSD zapewnia potężne rozwiązanie. W tym samouczku przeprowadzimy Cię przez proces obracania obrazu pod określonym kątem za pomocą Aspose.PSD. Zanim przejdziemy do kolejnych kroków, przygotujmy scenę wprowadzeniem.

## Wstęp

Aspose.PSD dla .NET to wszechstronna biblioteka, która umożliwia programistom płynną pracę z formatami PSD i obrazami rastrowymi. Jedną z jego kluczowych funkcji jest możliwość obracania obrazów pod precyzyjnym kątem, zapewniając elastyczność w manipulacji obrazami. Ten samouczek przeprowadzi Cię przez kolejne kroki obracania obrazu pod określonym kątem przy użyciu Aspose.PSD dla .NET.

## Warunki wstępne

Zanim wyruszymy w tę podróż, upewnijmy się, że spełniliśmy następujące wymagania wstępne:

-  Biblioteka Aspose.PSD dla .NET: Pobierz i zainstaluj bibliotekę z[strona pobierania](https://releases.aspose.com/psd/net/).
- Katalog dokumentów: skonfiguruj katalog do przechowywania plików źródłowych i wyjściowych.

## Importuj przestrzenie nazw

Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw do swojego projektu .NET:

```csharp
using Aspose.PSD.ImageOptions;
```

Podzielmy teraz przykład na wiele kroków w formie przewodnika krok po kroku.

## Krok 1: Ustaw katalog dokumentów

```csharp
string dataDir = "Your Document Directory";
```

 Zastępować`"Your Document Directory"` ze ścieżką do katalogu, w którym przechowujesz pliki źródłowe i wyjściowe.

## Krok 2: Załaduj obraz

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // W tym miejscu zostaną wstawione dodatkowe kroki
}
```

 Załaduj obraz, który chcesz obrócić, do instancji`RasterImage`.

## Krok 3: Buforuj dane obrazu

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Buforuj dane obrazu, aby uzyskać lepszą wydajność podczas obracania.

## Krok 4: Obróć obraz

```csharp
image.Rotate(20f, true, Color.Red);
```

Obróć obraz o 20 stopni, zachowując proporcjonalne rozmiary i używając czerwonego tła.

## Krok 5: Zapisz wynik

```csharp
image.Save(destName, new JpegOptions());
```

Zapisz obrócony obraz z określonymi opcjami (w tym przypadku jako plik JPEG).

## Wniosek

 Gratulacje! Pomyślnie obróciłeś obraz pod określonym kątem za pomocą Aspose.PSD dla .NET. Ta biblioteka zapewnia solidny zestaw narzędzi do manipulacji obrazami, a ten samouczek to tylko wierzchołek góry lodowej. Poznaj[dokumentacja](https://reference.aspose.com/psd/net/) aby uzyskać więcej funkcji i opcji.

## Często zadawane pytania

### P1: Czy mogę obracać obrazy o kąt inny niż 20 stopni?

 A1: Tak, możesz dostosować parametr kąta w`image.Rotate` metodę na dowolną żądaną wartość.

### P2: Czy Aspose.PSD obsługuje inne formaty obrazów oprócz JPEG?

A2: Absolutnie! Aspose.PSD obsługuje szeroką gamę formatów, w tym PNG, GIF, BMP i TIFF.

### P3: Czy konieczne jest buforowanie danych obrazu przed rotacją?

Odpowiedź 3: Chociaż nie jest to obowiązkowe, buforowanie danych może znacznie zwiększyć wydajność, szczególnie w przypadku większych obrazów.

### P4: Gdzie mogę uzyskać pomoc dotyczącą zapytań związanych z Aspose.PSD?

 A4: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie społeczności i dyskusje.

### P5: Czy mogę wypróbować Aspose.PSD przed zakupem?

 A5: Oczywiście! Chwyć swoje[bezpłatna wersja próbna](https://releases.aspose.com/) poznać możliwości biblioteki.
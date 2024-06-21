---
title: Przycinanie obrazów przez przesunięcia w Aspose.PSD dla .NET
linktitle: Przycinanie obrazów metodą Shift
second_title: Aspose.PSD API .NET
description: Naucz się bez wysiłku przycinać obrazy za pomocą Aspose.PSD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać precyzyjną regulację obrazu.
type: docs
weight: 12
url: /pl/net/image-manipulation/crop-image-shifts/
---
## Wstęp

W dziedzinie programowania .NET Aspose.PSD wyróżnia się jako potężny zestaw narzędzi do zadań przetwarzania obrazu. Jedną z jego godnych uwagi funkcji jest możliwość precyzyjnego przycinania obrazów dzięki funkcji „Kadrowanie przez przesunięcie”. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces płynnego przycinania obrazów przy użyciu Aspose.PSD dla .NET.

## Warunki wstępne

Przed przystąpieniem do samouczka upewnij się, że spełnione są następujące wymagania wstępne:

-  Biblioteka Aspose.PSD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę. Jeśli nie, możesz pobrać go ze strony[strona wydania](https://releases.aspose.com/psd/net/).

- Środowisko .NET: Upewnij się, że na komputerze jest skonfigurowane środowisko programistyczne .NET.

- Przykładowy obraz: Przygotuj przykładowy obraz w formacie PSD, z którym chcesz pracować.

## Importuj przestrzenie nazw

Rozpocznij od zaimportowania niezbędnych przestrzeni nazw do projektu .NET. Te przestrzenie nazw zapewniają dostęp do klas i metod Aspose.PSD wymaganych do przycinania obrazu.

```csharp
using Aspose.PSD.ImageOptions;
```

## Krok 1: Zdefiniuj katalog dokumentów

Ustaw ścieżkę do katalogu dokumentów, w którym będą znajdować się pliki źródłowe i docelowe.

```csharp
string dataDir = "Your Document Directory";
```

## Krok 2: Załaduj obraz źródłowy

Załaduj obraz PSD, który chcesz przyciąć. Pamiętaj, aby zastąpić „sample.psd” nazwą pliku źródłowego.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Krok 3: Buforuj dane obrazu w celu uzyskania lepszej wydajności

Przed przycięciem zaleca się buforowanie danych obrazu w celu poprawy wydajności.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Krok 4: Zdefiniuj wartości przesunięcia dla przycinania

Określ wartości przesunięcia lewej, prawej, górnej i dolnej strony obrazu. Dostosuj te wartości w oparciu o wymagania dotyczące przycinania.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Krok 5: Zastosuj kadrowanie i zapisz wyniki

 Skorzystaj z`Crop` metodę zastosowania określonych przesunięć i zapisania przyciętego obrazu w pliku docelowym.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się przycinać obrazy poprzez przesunięcia przy użyciu Aspose.PSD dla .NET. Ta potężna funkcjonalność zapewnia precyzję i kontrolę niezbędną do wykonywania różnych zadań przetwarzania obrazu.

## Często zadawane pytania

### P1: Czy mogę przycinać obrazy w różnych formatach, nie tylko PSD?

O1: Tak, Aspose.PSD obsługuje różne formaty obrazów, umożliwiając przycinanie obrazów w formatach takich jak JPEG, PNG i innych.

### P2: Czy przed zakupem Aspose.PSD dla .NET dostępna jest wersja próbna?

 A2: Oczywiście! Możesz zapoznać się z zestawem narzędzi w ramach bezpłatnej wersji próbnej[Tutaj](https://releases.aspose.com/).

### P3: Jak uzyskać tymczasową licencję na Aspose.PSD dla .NET?

 Odpowiedź 3: Możesz nabyć tymczasową licencję do celów testowych.[Tutaj](https://purchase.aspose.com/temporary-license/).

### P4: Gdzie mogę znaleźć dodatkowe wsparcie i dyskusje związane z Aspose.PSD?

 A4: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie i ciekawe dyskusje.

### P5: Czy mogę kupić Aspose.PSD dla .NET bezpośrednio ze strony internetowej?

 Odpowiedź 5: Tak, możesz bezpiecznie kupić bibliotekę w witrynie[strona zakupu](https://purchase.aspose.com/buy).

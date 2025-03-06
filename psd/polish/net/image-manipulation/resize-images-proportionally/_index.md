---
title: Proporcjonalna zmiana rozmiaru obrazów w Aspose.PSD dla .NET
linktitle: Proporcjonalna zmiana rozmiaru obrazów
second_title: Aspose.PSD API .NET
description: Poznaj płynną zmianę rozmiaru obrazu za pomocą Aspose.PSD dla .NET. Pobierz bibliotekę, postępuj zgodnie z naszym samouczkiem i zwiększ swoje możliwości przetwarzania obrazów.
weight: 14
url: /pl/net/image-manipulation/resize-images-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Proporcjonalna zmiana rozmiaru obrazów w Aspose.PSD dla .NET

dziedzinie manipulacji obrazami Aspose.PSD dla .NET wyróżnia się jako potężny zestaw narzędzi, zapewniający programistom możliwość łatwego proporcjonalnego zmieniania rozmiaru obrazów. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces zmiany rozmiaru obrazów przy użyciu Aspose.PSD dla .NET, upewniając się, że Twoje obrazy zachowują swoje proporcje bezbłędnie.

## Wstęp

Proporcjonalna zmiana rozmiaru obrazów jest częstym zadaniem w wielu aplikacjach, a Aspose.PSD dla .NET upraszcza ten proces dla programistów. Niezależnie od tego, czy pracujesz nad aplikacją internetową, oprogramowaniem komputerowym czy aplikacją mobilną, zrozumienie, jak zmieniać rozmiar obrazów przy jednoczesnym zachowaniu ich proporcji, ma kluczowe znaczenie dla utrzymania atrakcyjności wizualnej i spójności.

## Warunki wstępne

Zanim zagłębisz się w magię zmiany rozmiaru w Aspose.PSD dla .NET, upewnij się, że spełniasz następujące wymagania wstępne:

1.  Biblioteka Aspose.PSD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.PSD dla .NET. Można go pobrać z[Aspose.PSD dla wydań .NET](https://releases.aspose.com/psd/net/) strona.

2. Katalog dokumentów: Utwórz katalog do przechowywania dokumentów i zastąp „Twój katalog dokumentów” w dostarczonym kodzie rzeczywistą ścieżką do tego katalogu.

Po skonfigurowaniu wymagań wstępnych przejdźmy do przewodnika krok po kroku.

## Importuj przestrzenie nazw

```csharp
using Aspose.PSD.ImageOptions;
```

Zaimportuj niezbędne przestrzenie nazw, aby uzyskać dostęp do wymaganych klas i metod.

## Krok 1: Załaduj obraz

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Załaduj istniejący obraz do instancji klasy RasterImage
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Pozostałe kroki należy wykonać tutaj
}
```

 Załaduj obraz źródłowy za pomocą`Image.Load` metoda.

## Krok 2: Określ szerokość i wysokość

```csharp
// Określanie szerokości i wysokości
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Określ nową szerokość i wysokość obrazu o zmienionym rozmiarze. W tym przykładzie szerokość i wysokość są zmniejszone o połowę, ale możesz dostosować te wartości w zależności od wymagań.

## Krok 3: Zapisz obraz o zmienionym rozmiarze

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Zapisz obraz o zmienionym rozmiarze za pomocą`Save` metoda z określonymi opcjami. W tym przypadku zapisujemy go jako plik PNG.

## Wniosek

Proporcjonalna zmiana rozmiaru obrazów w Aspose.PSD dla .NET to prosty proces, który dodaje wartości do przepływu pracy przetwarzania obrazu. Ten przewodnik wyposażył Cię w wiedzę niezbędną do bezproblemowej integracji tej funkcjonalności z Twoimi aplikacjami.

## Często zadawane pytania

### P1: Czy mogę zmienić rozmiar obrazów do określonych wymiarów?

Odpowiedź 1: Tak, możesz dostosować nową szerokość i wysokość zgodnie z wymaganiami zawartymi w kodzie.

### P2: Czy Aspose.PSD dla .NET nadaje się do wsadowej zmiany rozmiaru obrazu?

A2: Absolutnie! Możesz włączyć te kroki w pętlę do przetwarzania wsadowego wielu obrazów.

### P3: Czy w Aspose.PSD dla .NET dostępne są inne funkcje manipulacji obrazami?

O3: Tak, Aspose.PSD dla .NET oferuje szeroką gamę funkcji, w tym przycinanie, obracanie i stosowanie filtrów do obrazów.

### P4: Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla .NET?

 O4: Tak, możesz poznać możliwości Aspose.PSD dla .NET w ramach bezpłatnej wersji próbnej. Odwiedzać[Tutaj](https://releases.aspose.com/) zacząć.

### P5: Gdzie mogę znaleźć wsparcie dla Aspose.PSD dla .NET?

 A5: Odwiedź[Aspose.PSD dla forum .NET](https://forum.aspose.com/c/psd/34) za wsparcie społeczności i dyskusje.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

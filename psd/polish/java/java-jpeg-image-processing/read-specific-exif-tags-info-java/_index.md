---
date: 2026-10-08
description: Dowiedz się, jak odczytać znaczniki EXIF w Javie przy użyciu Aspose.PSD
  for Java (asp) dzięki naszemu samouczkowi krok po kroku i zwiększ swoje możliwości
  przetwarzania obrazów.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Odczytaj informacje o konkretnych znacznikach EXIF w Javie
og_description: Odczytaj znaczniki EXIF – programiści Java mogą szybko wyodrębnić
  metadane obrazu przy użyciu Aspose.PSD. Ten przewodnik prowadzi Cię przez ładowanie
  pliku PSD, znajdowanie zasobów miniatur oraz wyświetlanie kluczowych pól EXIF, takich
  jak WhiteBalance i ISO speed.
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Jak odczytać znaczniki EXIF w Javie przy użyciu Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Jak odczytać znaczniki EXIF w Javie przy użyciu Aspose.PSD
url: /pl/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Odczyt informacji o konkretnych tagach EXIF w Javie przy użyciu Aspose (asp)

## Wprowadzenie
Jeśli potrzebujesz **odczytać tagi EXIF w Javie**, Aspose.PSD (asp) oferuje czyste, czysto‑Java API, które działa bez Photoshopa. W tym samouczku nauczysz się, jak wyodrębnić dane EXIF z obrazu PSD, wybrać tylko interesujące Cię tagi i wydrukować je w konsoli. Omówimy wszystko, od konfiguracji środowiska programistycznego po pobieranie metadanych, takich jak WhiteBalance, prędkość ISO i ogniskowa. Zaczynajmy!

## Szybkie odpowiedzi
- **Jaka biblioteka odczytuje dane EXIF z PSD w Javie?** Aspose.PSD (asp)  
- **Jakie tagi można wyodrębnić?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength i inne.  
- **Czy potrzebna jest licencja do produkcji?** Tak, wymagana jest licencja komercyjna; dostępna jest darmowa wersja próbna.  
- **Czy mogę używać tego z innymi formatami obrazów?** To samo API obsługuje PNG, JPEG, TIFF poprzez wyodrębnianie metadanych obrazu w Javie.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego scenariusza tylko do odczytu.

## Czym jest asp (Aspose.PSD dla Javy)?
Aspose.PSD for Java to czysto‑Java biblioteka, która umożliwia programistom pracę z plikami Adobe Photoshop (PSD, PSB) bez instalacji Photoshopa. Zapewnia programowy dostęp do warstw, zasobów i metadanych — w tym tagów EXIF — co czyni ją idealną do zadań **java image metadata extraction**.

## Dlaczego używać Aspose.PSD (asp) do wyodrębniania EXIF?
Możesz wyodrębnić tagi EXIF w Javie za pomocą zaledwie dwóch wywołań metod, a biblioteka przetwarza pliki do 2 GB bez ładowania całego dokumentu do pamięci. Obsługuje **ponad 30 formatów obrazu** i zachowuje dokładne ustawienia aparatu, zapewniając deterministyczne wyniki w środowiskach Windows, Linux i macOS.

## Wymagania wstępne
Zanim przejdziemy do kodu, musisz mieć przygotowane kilka rzeczy:

1. Java Development Kit (JDK): Upewnij się, że masz zainstalowany JDK na swoim komputerze. Możesz go pobrać ze [strony Oracle JDK](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. Aspose.PSD for Java: Pobierz bibliotekę ze [strony pobierania Aspose.PSD for Java](https://releases.aspose.com/psd/java/).  
3. Zintegrowane środowisko programistyczne (IDE): IDE takie jak IntelliJ IDEA, Eclipse lub NetBeans ułatwi programowanie.  
4. Plik PSD: Plik PSD zawierający dane EXIF. Możesz użyć przykładu podanego w tym samouczku lub dowolnego innego pliku PSD z tagami EXIF.

## Importowanie pakietów
Importuj wymagane klasy Aspose.PSD, takie jak Image, PsdImage, ThumbnailResource i JpegExifData, aby pracować z plikami PSD.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Krok 1: załaduj obraz PSD
`Image.load()` ładuje plik i zwraca obiekt Image reprezentujący dane obrazu.  
`PsdImage` jest klasą Aspose.PSD, która zapewnia funkcjonalność specyficzną dla PSD.  
Metoda `Image.load()` ładuje dowolny obsługiwany plik obrazu do pamięci, zwracając ogólny obiekt `Image`, który możesz rzutować na typ specyficzny dla PSD.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

W tym kroku ładujemy plik PSD za pomocą metody `Image.load()`. Klasa `PsdImage` jest używana do reprezentacji obrazu PSD, a załadowany obraz rzutujemy na tę klasę, aby uzyskać dostęp do funkcji specyficznych dla PSD.

## Krok 2: iteracja po zasobach obrazu
`PsdImage.getResources()` zwraca kolekcję osadzonych zasobów, takich jak miniatury i dane EXIF.  
Wywołanie `PsdImage.getResources()` zwraca kolekcję wszystkich osadzonych zasobów. Iterując po tej kolekcji, możesz znaleźć zasoby miniatur, które zawierają metadane EXIF.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Iterujemy zasoby obrazu przy użyciu pętli `for`. Celem jest zidentyfikowanie zasobów będących instancjami `ThumbnailResource` lub `Thumbnail4Resource`, ponieważ to właśnie te typy przechowują dane EXIF.

## Krok 3: wyodrębnianie danych EXIF
`ThumbnailResource.getJpegOptions()` zapewnia dostęp do opcji JPEG, w tym metadanych EXIF.  
`JpegExifData` przechowuje pojedyncze wartości tagów EXIF.  
Metoda `ThumbnailResource.getJpegOptions()` zapewnia dostęp do obiektu `JpegExifData`, który przechowuje poszczególne tagi EXIF, takie jak WhiteBalance, ISOSpeed i FocalLength.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

Używamy instrukcji `if`, aby sprawdzić, czy zasób jest instancją `ThumbnailResource`. Jeśli tak, rzutujemy go i pobieramy jego `JpegOptions`, aby uzyskać dostęp do `ExifData`. Na końcu wypisujemy różne tagi EXIF, takie jak WhiteBalance, wymiary pikseli, ISOSpeed i FocalLength.

## Typowe problemy i wskazówki
- **Null EXIF data:** Niektóre pliki PSD mogą nie zawierać zasobu miniatury z informacjami EXIF. Zawsze sprawdzaj `null` przed dostępem do wartości tagów.  
- **File path errors:** Używaj ścieżek bezwzględnych lub upewnij się, że katalog roboczy wskazuje na folder zawierający Twój plik PSD.  
- **License restrictions:** Darmowa wersja próbna ogranicza liczbę stron, które możesz przetworzyć; przejdź na pełną licencję, aby uzyskać nieograniczone użycie.

## Najczęściej zadawane pytania
### Co to są dane EXIF?
Dane EXIF (Exchangeable Image File Format) to metadane osadzone w plikach obrazów, zawierające informacje takie jak ustawienia aparatu, data i godzina oraz wymiary obrazu.

### Czy mogę edytować dane EXIF przy użyciu Aspose.PSD?
Tak, Aspose.PSD umożliwia odczyt i modyfikację danych EXIF. Możesz aktualizować tagi i zapisywać zmiany z powrotem do pliku obrazu.

### Czy Aspose.PSD dla Javy jest darmowy?
Aspose.PSD oferuje darmową wersję próbną, którą możesz pobrać ze [strony oficjalnych wydań Aspose.PSD](https://releases.aspose.com/). Aby uzyskać pełną funkcjonalność, musisz zakupić licencję.

### Jakie inne formaty obsługuje Aspose.PSD?
Aspose.PSD obsługuje różne formaty Adobe Photoshop, w tym PSD, PSB i inne. Zapewnia także możliwość konwersji tych formatów do PNG, JPEG, TIFF itp.

### Jak uzyskać wsparcie dla Aspose.PSD?
Wsparcie możesz uzyskać poprzez [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Jak to pomaga w **java image metadata extraction**?
Korzystając z obiektu `JpegExifData`, możesz programowo wyciągnąć dowolny potrzebny tag EXIF, co stanowi solidną podstawę do szerszych zadań wyodrębniania metadanych w różnych formatach obrazów.

---

**Ostatnia aktualizacja:** 2026-10-08  
**Testowano z:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Autor:** Aspose

## Powiązane samouczki

- [Odczyt i modyfikacja tagów JPEG Exif w Javie](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Przetwarzanie obrazów JPEG w Javie](/psd/java/java-jpeg-image-processing/)
- [Jak obrócić obraz pod określonym kątem przy użyciu Aspose.PSD dla Javy](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
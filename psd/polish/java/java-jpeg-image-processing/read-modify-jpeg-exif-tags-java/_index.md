---
date: 2026-10-03
description: Dowiedz się, jak w języku Java odczytać metadane obrazu i modyfikować
  tagi JPEG EXIF przy użyciu Aspose.PSD for Java w tym przewodniku step‑by‑step, idealnym
  dla programistów efektywnie pracujących z metadanymi obrazu.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Odczyt i modyfikacja tagów JPEG EXIF w języku Java
og_description: Dowiedz się, jak w języku Java odczytać metadane obrazu i modyfikować
  tagi JPEG EXIF przy użyciu Aspose.PSD for Java. Ten przewodnik pokazuje kod step‑by‑step
  do wyodrębniania i aktualizacji informacji EXIF.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Jak w języku Java odczytać metadane obrazu i modyfikować tagi JPEG EXIF
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Jak w języku Java odczytać metadane obrazu i modyfikować tagi JPEG EXIF
url: /pl/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Odczyt i modyfikacja znaczników EXIF JPEG w Javie

## Wprowadzenie
Jeśli potrzebujesz **java read image metadata** z plików JPEG i chcesz je zmienić programowo, trafiłeś we właściwe miejsce. W tym samouczku przeprowadzimy Cię przez wyodrębnianie i aktualizację znaczników EXIF przy użyciu Aspose.PSD for Java. Po zakończeniu będziesz mógł pobrać szczegóły aparatu, orientację i pola niestandardowe, a następnie zapisać je z powrotem do pliku — wszystko bez edytora graficznego.

## Szybkie odpowiedzi
- **Która biblioteka obsługuje JPEG EXIF w Javie?** Aspose.PSD for Java.
- **Ile linii kodu potrzebnych jest do odczytu EXIF?** Około trzy linie po załadowaniu obrazu.
- **Czy możesz modyfikować znaczniki EXIF?** Tak, możesz zmienić dowolny standardowy lub niestandardowy znacznik i zapisać wynik.
- **Obsługiwane formaty obrazów?** Ponad 150 formatów, w tym PSD, JPEG, PNG, TIFF i BMP.
- **Minimalna wersja Java?** Java 7 lub wyższa.

## Dlaczego warto używać Aspose.PSD for Java?
Aspose.PSD obsługuje **ponad 150 formatów obrazów** i może przetwarzać pliki do **2 GB** bez ładowania całego dokumentu do pamięci, co zapewnia szybkie operacje metadanych przy niskim zużyciu pamięci na dużych kolekcjach zdjęć. Dostarcza także prostego API do odczytu i zapisu danych EXIF, IPTC i XMP, co sprawia, że przetwarzanie wsadowe tysięcy obrazów jest wydajne i niezawodne.

## Wymagania wstępne
1. **Java Development Kit (JDK)** – upewnij się, że masz JDK 11 lub nowszy. Możesz go pobrać ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – pobierz najnowszy JAR ze [strony wydań Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor, który preferujesz.  
4. **Basic Java knowledge** – powinieneś być zaznajomiony z tworzeniem projektów i dodawaniem zewnętrznych plików JAR.

## Co to jest Java read image metadata?
Java read image metadata odnosi się do procesu programowego uzyskiwania dostępu do osadzonych informacji, takich jak EXIF, IPTC i XMP, przechowywanych w plikach obrazów przy użyciu kodu Java. Metadane te mogą zawierać ustawienia aparatu, znaczniki czasu, współrzędne GPS, informacje o prawach autorskich oraz komentarze użytkowników, umożliwiając aplikacjom organizowanie, wyszukiwanie i manipulowanie obrazami na podstawie ich danych opisowych.

## Importowanie pakietów
Najpierw dodaj plik JAR Aspose.PSD do ścieżki klas swojego projektu i zaimportuj wymagane klasy.

Pakiet `com.aspose.psd` zapewnia podstawowe API do ładowania obrazów i uzyskiwania dostępu do ich zasobów.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Jak odczytać metadane obrazu z plików JPEG w Javie?
Załaduj plik JPEG za pomocą `PsdImage.load("image.jpg")`, znajdź zasób miniatury zawierający dane EXIF, a następnie wywołaj `ExifData.read()`, aby uzyskać wypełniony obiekt `ExifData`. To jednoczesne podejście daje pełny dostęp do wszystkich standardowych pól EXIF oraz dowolnych niestandardowych znaczników, które mogłeś dodać.

## Krok 1: Załaduj obraz PSD
PsdImage jest klasą Aspose.PSD reprezentującą plik PSD i udostępnia metody do dostępu do jego zasobów i metadanych.  
W tym kroku załadujemy obraz PSD, z którego chcemy odczytać dane EXIF. Upewnij się, że Twój obraz znajduje się w odpowiednim katalogu.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Krok 2: Iteracja po zasobach obrazu
ThumbnailResource reprezentuje miniaturę przechowywaną w pliku PSD, często zawierającą osadzone dane EXIF.  
Po załadowaniu obrazu następnym krokiem jest iteracja po jego zasobach w celu znalezienia zasobu miniatury, który zazwyczaj zawiera dane EXIF.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Krok 3: Wyodrębnij dane EXIF
JpegExifData jest klasą przechowującą informacje EXIF wyodrębnione z obrazu JPEG, umożliwiającą odczyt i modyfikację poszczególnych znaczników.  
Teraz, gdy mamy zasób miniatury, możemy wyodrębnić z niego dane EXIF. Dane EXIF zawierają cenne informacje, takie jak nazwa właściciela aparatu, wartość przysłony, orientacja i inne.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Krok 4: Modyfikacja danych EXIF
Po odczytaniu danych EXIF możesz chcieć zmodyfikować niektóre z ich pól. Oto jak możesz to zrobić:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Krok 5: Zapisz zmiany
Na koniec, po zmodyfikowaniu danych EXIF, zapisz zmiany do nowego pliku PSD.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Typowe problemy i rozwiązania
- **Brak zasobu miniatury** – Niektóre pliki JPEG przechowują EXIF bezpośrednio w nagłówku głównego obrazu. Jeśli zasób miniatury jest nieobecny, użyj `image.getExifData()`.
- **Duże pliki powodują OutOfMemoryError** – Upewnij się, że uruchamiasz JVM z wystarczającą ilością pamięci (`-Xmx2g`) lub przetwarzaj obraz w trybie strumieniowym używając `PsdImage.load(inputStream, loadOptions)`.
- **Nieobsługiwane typy znaczników** – Aspose.PSD obsługuje wszystkie standardowe znaczniki EXIF; znaczniki niestandardowe mogą wymagać ręcznej obsługi na poziomie bajtów.

## Najczęściej zadawane pytania

**Q: Czym są dane EXIF?**  
A: Metadane EXIF (Exchangeable Image File Format) przechowują ustawienia aparatu, znaczniki czasu, współrzędne GPS oraz inne informacje osadzone w plikach JPEG i innych plikach obrazów.

**Q: Czy mogę używać Aspose.PSD for Java za darmo?**  
A: Możesz uzyskać bezpłatną wersję próbną ze [strony wydań Aspose](https://releases.aspose.com/).

**Q: Czy Aspose.PSD for Java jest kompatybilny ze wszystkimi wersjami Java?**  
A: Aspose.PSD for Java obsługuje Java SE 7 i wyższe.

**Q: Gdzie mogę znaleźć więcej dokumentacji na temat Aspose.PSD for Java?**  
A: Sprawdź [dokumentację](https://reference.aspose.com/psd/java/) po więcej szczegółów.

**Q: Jak mogę uzyskać wsparcie dla Aspose.PSD for Java?**  
A: Możesz uzyskać wsparcie na [forum wsparcia Aspose PSD](https://forum.aspose.com/c/psd/34/).

## Zakończenie
Postępując zgodnie z tymi krokami, możesz **java read image metadata** z dowolnego pliku JPEG, dostosować potrzebne pola EXIF i zapisać zaktualizowane dane z powrotem do pliku — wszystko przy użyciu kilku linii czystego kodu Java. Bogate API Aspose.PSD zapewnia niezawodne i wydajne operacje na metadanych, dzięki czemu możesz zintegrować je z potokami przetwarzania wsadowego, narzędziami do zarządzania zdjęciami lub dowolną aplikacją, która musi pracować z informacjami o obrazach.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.5  
**Author:** Aspose

## Powiązane samouczki

- [Odczytaj informacje o konkretnych znacznikach EXIF w Javie przy użyciu Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Utwórz metadane XMP w plikach PSD przy użyciu Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [Zmień rozmiar obrazu przy użyciu Aspose.PSD for Java – Rysowanie kształtów i podstawowe operacje na obrazach](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
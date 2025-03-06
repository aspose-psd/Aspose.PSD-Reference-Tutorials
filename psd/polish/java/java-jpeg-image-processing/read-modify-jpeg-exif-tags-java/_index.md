---
title: Odczytuj i modyfikuj tagi JPEG EXIF w Javie
linktitle: Odczytuj i modyfikuj tagi JPEG EXIF w Javie
second_title: Aspose.PSD API Java
description: W tym przewodniku krok po kroku dowiesz się, jak czytać i modyfikować tagi JPEG EXIF przy użyciu Aspose.PSD dla Java. Idealny dla programistów, którzy chcą bez wysiłku obsługiwać metadane obrazu.
weight: 18
url: /pl/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Odczytuj i modyfikuj tagi JPEG EXIF w Javie

## Wstęp
Hej tam! Czy zastanawiałeś się kiedyś, jak czytać i modyfikować tagi JPEG EXIF przy użyciu Java? Jeśli tak, jesteś we właściwym miejscu! Ten samouczek poprowadzi Cię krok po kroku przez proces korzystania z Aspose.PSD dla Java. Niezależnie od tego, czy jesteś doświadczonym programistą, czy nowicjuszem, po przeczytaniu tego przewodnika będziesz w stanie obsługiwać tagi JPEG EXIF jak profesjonalista. Zatem zanurzmy się!
## Warunki wstępne
Zanim zaczniemy, upewnij się, że masz następujące elementy:
1.  Zestaw Java Development Kit (JDK): Upewnij się, że w systemie jest zainstalowany pakiet JDK. Można go pobrać z[stronie internetowej Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Biblioteka Aspose.PSD dla Java: Musisz pobrać bibliotekę Aspose.PSD dla Java. Zdobądź to z[Strona z wydaniami Aspose](https://releases.aspose.com/psd/java/).
3. Zintegrowane środowisko programistyczne (IDE): IDE, takie jak IntelliJ IDEA lub Eclipse, sprawi, że kodowanie stanie się płynniejsze.
4. Podstawowa znajomość języka Java: Aby skorzystać z tego samouczka, wymagana jest podstawowa znajomość języka Java.
## Importuj pakiety
Na początek zaimportujmy niezbędne pakiety. Otwórz swoje środowisko Java IDE i utwórz nowy projekt Java. Następnie dołącz bibliotekę Aspose.PSD for Java do zależności projektu.
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Krok 1: Załaduj obraz PSD
tym kroku załadujemy obraz PSD, z którego chcemy odczytać dane EXIF. Upewnij się, że obraz znajduje się we właściwym katalogu.
```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```
## Krok 2: Iteruj po zasobach obrazu
Następnym krokiem po załadowaniu obrazu jest iteracja jego zasobów w celu znalezienia zasobu miniatury, który zazwyczaj zawiera dane EXIF.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Przejdź do następnego kroku
    }
}
```
## Krok 3: Wyodrębnij dane EXIF
Teraz, gdy mamy zasób miniatur, możemy wyodrębnić z niego dane EXIF. Dane EXIF zawierają cenne informacje, takie jak imię i nazwisko właściciela aparatu, wartość przysłony, orientacja i inne.
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
## Krok 4: Zmodyfikuj dane EXIF
Po przeczytaniu danych EXIF możesz chcieć zmodyfikować niektóre z ich pól. Oto jak możesz to zrobić:
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
Na koniec, po modyfikacji danych EXIF, zapisz zmiany w nowym pliku PSD.
```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Wniosek
masz to! Wykonując poniższe kroki, możesz łatwo czytać i modyfikować tagi JPEG EXIF przy użyciu Aspose.PSD dla Java. Ta potężna biblioteka sprawia, że obsługa metadanych obrazów jest dziecinnie prosta. Zatem śmiało wypróbuj go we własnych projektach. Miłego kodowania!
## Często zadawane pytania
### Co to są dane EXIF?
Dane EXIF (Exchangeable Image File Format) zawierają metadane dotyczące obrazu, takie jak ustawienia aparatu i orientacja.
### Czy mogę używać Aspose.PSD dla Java za darmo?
 Możesz uzyskać bezpłatną wersję próbną od[Strona z wydaniami Aspose](https://releases.aspose.com/).
### Czy Aspose.PSD for Java jest kompatybilny ze wszystkimi wersjami Java?
Aspose.PSD dla Java obsługuje Java SE 7 i nowsze wersje.
### Gdzie mogę znaleźć więcej dokumentacji na temat Aspose.PSD dla Java?
 Sprawdź[dokumentacja](https://reference.aspose.com/psd/java/) aby uzyskać więcej szczegółów.
### Jak uzyskać wsparcie dla Aspose.PSD dla Java?
 Możesz uzyskać wsparcie od[Forum wsparcia Aspose PSD](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

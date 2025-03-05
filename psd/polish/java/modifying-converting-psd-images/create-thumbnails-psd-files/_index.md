---
title: Twórz miniatury z plików PSD przy użyciu języka Java
linktitle: Twórz miniatury z plików PSD przy użyciu języka Java
second_title: Aspose.PSD API Java
description: Dowiedz się, jak bez wysiłku tworzyć miniatury z plików PSD przy użyciu Java i Aspose.PSD. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać płynne przetwarzanie obrazu.
type: docs
weight: 24
url: /pl/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---
## Wstęp
świecie projektowania graficznego praca z plikami PSD (dokument Photoshop) jest na porządku dziennym. Niezależnie od tego, czy jesteś doświadczonym programistą, grafikiem, czy po prostu osobą, która chce zagłębić się w przetwarzanie obrazów, tworzenie miniatur z plików PSD może zaoszczędzić czas i usprawnić przepływ pracy. Ten samouczek poprowadzi Cię przez cały proces korzystania z Aspose.PSD dla Java. Aspose.PSD to nie tylko solidna biblioteka do zarządzania plikami Photoshopa, ale także sprawia, że wykonywane zadanie jest intuicyjne i łatwe w zarządzaniu. Czy jesteś gotowy, aby dowiedzieć się, jak efektywnie tworzyć miniatury z plików PSD?
## Warunki wstępne
Zanim zagłębimy się w szczegóły tworzenia miniatur, omówmy, co będzie potrzebne na początek.
### Środowisko programistyczne Java
-  Java JDK: Upewnij się, że na komputerze jest zainstalowany zestaw Java Development Kit (JDK). Możesz go pobrać[Tutaj](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: Zintegrowane środowisko programistyczne (IDE), takie jak IntelliJ IDEA, Eclipse lub NetBeans, ułatwi kodowanie.
### Biblioteka Aspose.PSD
- Musisz dołączyć bibliotekę Aspose.PSD do swojego projektu. Możesz[pobierz najnowszą wersję tutaj](https://releases.aspose.com/psd/java/).
### Podstawowa znajomość Javy
- Znajomość podstaw języka Java pomoże Ci efektywniej poruszać się po przykładowym kodzie. Pojęcia takie jak klasy, obiekty i pętle będą często stosowane.
## Importuj pakiety
Zacznij od zaimportowania niezbędnych klas z biblioteki Aspose.PSD. Ten krok jest kluczowy, ponieważ umożliwia wykorzystanie funkcjonalności biblioteki w kodzie.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Po spełnieniu wymagań wstępnych przejdźmy do głównego wydarzenia! Tworzenie miniatur z plików PSD obejmuje kilka prostych kroków, które wyjaśnię.
## Krok 1: Skonfiguruj swoje środowisko
Oto jak rozpocząć projekt i przygotować się do generowania miniatur.
1. Utwórz projekt Java:
   - Otwórz swoje IDE i utwórz nowy projekt Java.
   - Nadaj mu nazwę „PsdThumbnailGenerator”.
2. Dołącz bibliotekę Aspose.PSD:
   -  Dodaj plik JAR Aspose.PSD do ścieżki kompilacji projektu. Jeśli używasz Mavena, dołącz go do swojego`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## Krok 2: Załaduj plik PSD
Następnie musimy załadować plik PSD, z którego chcemy stworzyć miniaturki. 
1. Określ katalog dokumentów:
   Zdefiniuj katalog, w którym znajduje się plik PSD.
   ```java
   String dataDir = "Your Document Directory"; // Zamień na swoją ścieżkę
   ```
2. Załaduj plik PSD:
    Skorzystaj z`PsdImage` class, aby załadować plik PSD.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 Tutaj,`sample.psd` to nazwa Twojego pliku PSD. Dostosuj to zgodnie z nazwą pliku.
## Krok 3: Iteruj po zasobach PSD
Teraz, gdy mamy załadowany obraz PSD, następnym krokiem jest sprawdzenie jego zasobów.
1. Uzyskaj liczbę zasobów:
   Przejdziemy przez wszystkie zasoby w pliku PSD.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // Przetwarzanie zasobów
   }
   ```
   
2. Zidentyfikuj zasoby miniatur:
   Wewnątrz pętli sprawdź, czy zasób jest miniaturą.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // Przetwórz miniaturę
   }
   ```
## Krok 4: Przetwórz miniaturę
Gdy zidentyfikujemy zasób miniatury, będziemy musieli odpowiednio się nim zająć.
1. Pobierz i sprawdź format miniatury:
   Jeśli zasób rzeczywiście jest miniaturą, pobierz go i sprawdź jego format.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // Utwórz i zapisz miniaturę
   }
   ```
## Krok 5: Utwórz i zapisz miniaturę
To tutaj dzieje się magia! Utworzymy nowy obraz z danych miniatur i zapiszemy go.
1. Utwórz nowy obraz:
   Do utworzenia nowego obrazu bitmapowego użyjemy szerokości i wysokości zasobu miniatury.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. Przechowuj piksele w nowym obrazie:
   Przenieś dane miniatury do nowo utworzonego obrazu.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. Zapisz obraz miniatury:
   Na koniec zapisz obraz miniatury w katalogu dokumentów pod unikalną nazwą.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## Wniosek
Tworzenie miniatur z plików PSD przy użyciu Java i Aspose.PSD może być prostym zadaniem, jeśli podzielisz je na łatwe do wykonania kroki. Dzięki temu samouczkowi możesz teraz z łatwością wyodrębniać miniatury z plików PSD, co daje Ci sprytne narzędzie usprawniające pracę. Więc co Cię powstrzymuje? Zdobądź kilka plików PSD i spróbuj!
## Często zadawane pytania
### Co to jest Aspose.PSD?
Aspose.PSD to biblioteka Java, która umożliwia programistom pracę z plikami Photoshopa, ułatwiając programowe manipulowanie plikami PSD i zarządzanie nimi.
### Czy mogę używać Aspose.PSD za darmo?
Tak, Aspose oferuje bezpłatną wersję próbną, której możesz użyć do przetestowania biblioteki przed zakupem licencji.
### W jakich formatach mogę zapisać miniatury?
W tym przykładzie zapisaliśmy miniatury w formacie BMP, ale Aspose.PSD obsługuje również różne inne formaty.
### Czy muszę mieć zainstalowany program Photoshop, aby móc korzystać z Aspose.PSD?
Nie, Aspose.PSD działa niezależnie od Photoshopa.
### Gdzie mogę znaleźć więcej informacji na temat Aspose.PSD?
 Możesz sprawdzić[Dokumentacja Aspose.PSD](https://reference.aspose.com/psd/java/) aby uzyskać więcej informacji, samouczków i zasobów.
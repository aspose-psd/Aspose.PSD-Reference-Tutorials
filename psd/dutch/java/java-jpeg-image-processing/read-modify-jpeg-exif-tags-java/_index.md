---
title: Lees en wijzig JPEG EXIF-tags in Java
linktitle: Lees en wijzig JPEG EXIF-tags in Java
second_title: Aspose.PSD Java-API
description: Leer in deze stapsgewijze handleiding hoe u JPEG EXIF-tags leest en wijzigt met Aspose.PSD voor Java. Perfect voor ontwikkelaars die moeiteloos metagegevens van afbeeldingen willen verwerken.
weight: 18
url: /nl/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lees en wijzig JPEG EXIF-tags in Java

## Invoering
Hé daar! Heeft u zich ooit afgevraagd hoe u JPEG EXIF-tags kunt lezen en wijzigen met Java? Dan ben je hier aan het juiste adres! Deze tutorial leidt u stap voor stap door het proces met Aspose.PSD voor Java. Of u nu een doorgewinterde ontwikkelaar of een nieuweling bent, aan het einde van deze handleiding kunt u als een professional met JPEG EXIF-tags omgaan. Dus laten we erin duiken!
## Vereisten
Voordat we beginnen, zorg ervoor dat je het volgende hebt:
1.  Java Development Kit (JDK): Zorg ervoor dat JDK op uw systeem is geïnstalleerd. Je kunt het downloaden van de[Oracle-website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD voor Java-bibliotheek: u moet de Aspose.PSD voor Java-bibliotheek downloaden. Haal het van de[Aspose-releasespagina](https://releases.aspose.com/psd/java/).
3. Integrated Development Environment (IDE): Een IDE zoals IntelliJ IDEA of Eclipse zal uw codeerervaring soepeler maken.
4. Basiskennis van Java: Een fundamenteel begrip van Java is vereist om deze tutorial te volgen.
## Pakketten importeren
Laten we eerst de benodigde pakketten importeren. Open uw Java IDE en maak een nieuw Java-project. Neem vervolgens de Aspose.PSD voor Java-bibliotheek op in uw projectafhankelijkheden.
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Stap 1: Laad de PSD-afbeelding
In deze stap laden we de PSD-afbeelding waarvan we de EXIF-gegevens willen lezen. Zorg ervoor dat uw afbeelding in de juiste map staat.
```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```
## Stap 2: Herhaal de afbeeldingsbronnen
Zodra de afbeelding is geladen, is de volgende stap het herhalen van de bronnen om de miniatuurbron te vinden, die doorgaans de EXIF-gegevens bevat.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Ga door naar de volgende stap
    }
}
```
## Stap 3: EXIF-gegevens extraheren
Nu we de thumbnail-bron hebben, kunnen we de EXIF-gegevens eruit extraheren. EXIF-gegevens bevatten waardevolle informatie zoals de naam van de camera-eigenaar, diafragmawaarde, oriëntatie en meer.
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
## Stap 4: Wijzig EXIF-gegevens
Nadat u de EXIF-gegevens heeft gelezen, wilt u wellicht enkele velden wijzigen. Hier ziet u hoe u het kunt doen:
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
## Stap 5: Sla de wijzigingen op
Sla ten slotte, na het wijzigen van de EXIF-gegevens, de wijzigingen op in een nieuw PSD-bestand.
```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Conclusie
En daar heb je het! Door deze stappen te volgen, kunt u eenvoudig JPEG EXIF-tags lezen en wijzigen met Aspose.PSD voor Java. Deze krachtige bibliotheek maakt het verwerken van metagegevens van afbeeldingen een fluitje van een cent. Dus ga je gang en probeer het uit op je eigen projecten. Veel codeerplezier!
## Veelgestelde vragen
### Wat zijn EXIF-gegevens?
EXIF-gegevens (Exchangeable Image File Format) bevatten metagegevens over een afbeelding, zoals camera-instellingen en oriëntatie.
### Kan ik Aspose.PSD voor Java gratis gebruiken?
 U kunt een gratis proefversie krijgen van de[Aspose-releasespagina](https://releases.aspose.com/).
### Is Aspose.PSD voor Java compatibel met alle versies van Java?
Aspose.PSD voor Java ondersteunt Java SE 7 en hoger.
### Waar kan ik meer documentatie vinden over Aspose.PSD voor Java?
 Bekijk de[documentatie](https://reference.aspose.com/psd/java/) voor meer informatie.
### Hoe krijg ik ondersteuning voor Aspose.PSD voor Java?
 U kunt ondersteuning krijgen van de[Aspose PSD-ondersteuningsforum](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

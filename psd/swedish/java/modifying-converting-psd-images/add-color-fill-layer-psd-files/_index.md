---
date: 2026-03-02
description: Lär dig hur du lägger till fyllning genom att skapa ett färgfyllnadslager
  i PSD‑filer med Java och Aspose.PSD. Följ vår steg‑för‑steg‑guide för att snabbt
  ställa in färgen på fyllnadslagret.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'Hur man lägger till fyllning: Lägg till färgfyllningslager i PSD-filer med
  Java'
url: /sv/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till färgfyllnadslager i PSD-filer med Java

## Introduktion
Har du någonsin behövt manipulera Photoshop‑filer programatiskt, kanske för att lägga till en färgklick i en design? Om du undrar **how to add fill** till en PSD, är du på rätt plats. I den här handledningen går vi igenom hur du lägger till ett färgfyllnadslager i PSD (Photoshop Document)‑filer med Java och Aspose.PSD‑biblioteket. Tänk på din PSD som en digital duk – i slutet kommer du att veta hur du skapar ett färgfyllnadslager, sätter färg på lagret och sparar den uppdaterade filen med bara några rader kod.

## Snabba svar
- **Vilket bibliotek behövs?** Aspose.PSD for Java  
- **Primärt användningsfall?** Programatiskt lägga till eller ändra PSD‑fyllnadsfärger  
- **Hur lång tid tar implementeringen?** Omkring 10‑15 minuter för ett grundscenario  
- **Behöver jag en licens?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktion  
- **Stödd Java‑version?** Java 8 och senare  

## Vad är ett färgfyllnadslager?
Ett färgfyllnadslager är ett solid‑färgsöverlägg som ligger ovanpå andra lager i ett Photoshop‑dokument. Det används ofta för att lägga till bakgrundsfärg, skapa masker eller snabbt ändra den visuella temat för en design utan att redigera enskilda pixlar.

## Varför lägga till ett färgfyllnadslager med kod?
- **Automatisering:** Generera konsekventa varumärkesresurser över många filer.  
- **Batchbearbetning:** Uppdatera dussintals PSD‑filer på sekunder istället för manuellt.  
- **Dynamiska designer:** Ändra färger i farten baserat på användarinmatning eller datakällor.

## Förutsättningar
Innan vi dyker ner i koden, låt oss försäkra oss om att du har allt du behöver:

1. **Java Development Kit (JDK)** – JDK 8 eller nyare installerat.  
2. **Aspose.PSD Library** – Ladda ner den senaste JAR‑filen från [Aspose Releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans, eller någon editor du föredrar.  
4. **Basic Java knowledge** – Bekantskap med objekt, loopar och undantagshantering.

## Importera paket
Nu när grunderna är täckta, låt oss importera de nödvändiga klasserna. Dessa imports ger oss åtkomst till PSD‑hantering och manipulation av fyllnadslager.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## Hur man lägger till fyllning – steg‑för‑steg‑guide

### Steg 1: Ställ in din miljö
Definiera var din käll‑PSD finns och var den redigerade filen ska sparas, och ladda sedan dokumentet.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` pekar på mappen som innehåller din PSD.  
- `sourceFileName` är den ursprungliga filen du kommer att modifiera.  
- `exportPath` är där den nya filen med **add color fill layer** kommer att skrivas.  

### Steg 2: Loopa igenom lagren
Vi behöver hitta eventuella befintliga fyllnadslager så att vi kan antingen modifiera dem eller skapa ett nytt.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- `for`‑loopen itererar över varje lager i PSD‑filen.  
- `instanceof FillLayer`‑kontrollen säkerställer att vi endast arbetar med fyllnadslager.  

### Steg 3: Verifiera fyllnadstypen
Se till att lagret vi hittade är ett **color fill layer** innan vi försöker ändra dess färg.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

Om fyllnadstypen inte är `FillType.Color` avbryter vi för att undvika oavsiktlig ändring av gradient‑ eller mönsterfyllnader.

### Steg 4: Ställ in fyllnadsfärgen
Här är vi **set fill layer color**. Exemplet ändrar lagret till rött, men du kan ersätta `Color.getRed()` med någon annan `Color` du behöver (t.ex. `Color.getBlue()`, `new Color(255, 165, 0)` för orange).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` ändrar den faktiska fyllnadsfärgen.  
- `fillLayer.update()` uppdaterar lagret så den nya färgen tillämpas.  

### Steg 5: Spara ändringarna
Skriv slutligen den modifierade PSD‑filen tillbaka till disk.

```java
im.save(exportPath);
break;
```

- `break` stoppar loopen efter att det första matchande fyllnadslagret har uppdaterats, vilket vanligtvis är vad du vill när du bara behöver **change PSD fill color** en gång.  

## Vanliga problem & tips
- **No FillLayer found:** Om din PSD inte innehåller ett fyllnadslager måste du skapa ett med `new FillLayer(im)` och lägga till det i `im.getLayers()`.  
- **Color not updating:** Se till att du anropar `fillLayer.update()` efter att du har satt färgen.  
- **File not saved:** Verifiera att `exportPath` pekar på en skrivbar katalog och att du har behörighet att skriva filer där.  

## Vanliga frågor

**Q: What is Aspose.PSD?**  
A: Aspose.PSD är ett robust Java‑bibliotek som låter dig skapa, redigera och konvertera Photoshop‑PSD‑filer utan att behöva Adobe Photoshop.

**Q: Can I use Aspose.PSD for free?**  
A: Ja, en gratis provversion finns tillgänglig på [Aspose Releases page](https://releases.aspose.com/).  

**Q: Which file formats can I work with besides PSD?**  
A: Aspose.PSD stödjer PSD, PSB, BMP, JPEG, PNG, GIF, TIFF och fler.

**Q: How do I get support if I run into problems?**  
A: Du kan ställa frågor på [Aspose Support Forum](https://forum.aspose.com/c/psd/34).  

**Q: Where can I purchase a full license?**  
A: Licenser säljs via [Aspose Purchase page](https://purchase.aspose.com/buy).

## Slutsats
Du vet nu **how to add fill** till ett Photoshop‑dokument programatiskt med Java. Genom att skapa eller hitta ett färgfyllnadslager, sätta dess färg och spara resultatet kan du automatisera repetitiva designuppgifter, generera dynamiska resurser eller integrera PSD‑manipulation i större Java‑applikationer. Prova det – experimentera med olika färger, lägg till flera fyllnadslager, eller kombinera denna teknik med andra Aspose.PSD‑funktioner för kraftfulla bildbehandlingspipelines.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose
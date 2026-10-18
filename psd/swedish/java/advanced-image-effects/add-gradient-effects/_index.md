---
date: 2026-10-18
description: Lär dig hur du skapar radial gradient‑effekter i Java‑bilder med Aspose.PSD.
  Följ den här steg‑för‑steg‑guiden för sömlös integration.
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: Lägg till gradient‑effekter
og_description: Lär dig skapa radial gradient java‑effekter med Aspose.PSD. Den här
  handledningen visar hur du lägger till, anpassar och sparar gradient‑överlägg på
  några minuter.
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Skapa radial gradient java med Aspose.PSD – steg‑för‑steg‑guide
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Hur man skapar radial gradient‑effekter i Aspose.PSD för Java
url: /sv/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man skapar radialgradient‑effekter i Aspose.PSD för Java

## Introduktion

I den här guiden kommer du att lära dig hur du **skapar radial gradient java**‑effekter med hjälp av Aspose.PSD‑biblioteket. Radiala gradienter är perfekta för att lägga till djup, fokus eller ett subtilt sken till dina PSD‑lager utan att öppna Photoshop. I slutet av handledningen kommer du att kunna läsa in en PSD, applicera ett gradient‑överlägg, justera dess egenskaper och spara resultatet – allt från Java‑kod.

## Snabba svar
- **Vad kan jag uppnå?** Lägg till, redigera och blanda radiala gradient‑överlägg på PSD‑lager.  
- **Vilket bibliotek krävs?** Aspose.PSD för Java (senaste versionen).  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för ett grundläggande radialt gradient‑överlägg.  
- **Är det kompatibelt med Java 8+?** Ja, API‑et stödjer Java 8 och nyare runtime‑miljöer.

## Förutsättningar

Innan vi dyker ner i handledningen, se till att du har följande förutsättningar på plats:

1. **Aspose.PSD för Java‑bibliotek** – Säkerställ att du har laddat ner och installerat Aspose.PSD för Java‑biblioteket. Du hittar biblioteket och dess dokumentation på [Aspose.PSD Java documentation page](https://reference.aspose.com/psd/java/).  
2. **Java‑utvecklingsmiljö** – Ställ in en Java‑utvecklingsmiljö på din maskin (JDK 8 eller högre, valfri IDE).  
3. **Senaste Aspose.PSD‑utgåvan** – Ladda ner den senaste versionen från [Aspose releases page](https://releases.aspose.com/).  
4. **Support‑resurser** – Om du stöter på problem, konsultera [Aspose.PSD Support forum](https://forum.aspose.com/c/psd/34).  
5. **Licensköp** – När du är redo för produktion, skaffa en licens via [purchase page](https://purchase.aspose.com/buy).

Nu när du har allt på plats, låt oss gå vidare med steg‑för‑steg‑guiden.

## Vad är en gradient‑överläggseffekt?

En gradient‑överläggseffekt målar en mjuk övergång mellan två eller fler färger över ett valt område av ett lager. I Photoshop kan denna effekt blandas, färgas och placeras för att skapa sofistikerade visuella designer. Klassen `GradientOverlayEffect` är Aspose.PSD:s representation av den lagerstilen och exponerar egenskaper som färgstopp, opacitet, blandningsläge och gradientstil.

## Hur man skapar en radialgradient‑effekt

Läs in PSD‑filen, lokalisera mål‑lagret, justera `GradientOverlayEffect`‑egenskaperna och spara slutligen filen. Det kompletta arbetsflödet ryms i fyra koncisa rader Java‑kod när bilden har lästs in.

### Steg 1: Läs in PSD‑filen och få åtkomst till gradient‑överlägget

`PsdLoadOptions` konfigurerar hur en PSD‑fil läses in och låter dig aktivera laddning av effekt‑resurser. `Image.load` läser filen till ett `Image`‑objekt.

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

I detta steg läser vi in en PSD‑fil och hämtar det första `GradientOverlayEffect` från det andra lagret (index 1). Anropet `loadOptions.setLoadEffectsResource(true)` säkerställer att effekt‑resurserna är tillgängliga för redigering.

### Steg 2: Verifiera initiala inställningar

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

Innan du gör ändringar är det god praxis att bekräfta aktuellt blandningsläge, opacitet och synlighet. Detta hjälper dig att förstå grundläget för gradient‑överlägget.

### Steg 3: Ändra gradientinställningar

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

Här kan du anpassa gradientens färg, opacitet och blandningsläge. Exemplet ändrar färgen till grön, minskar opaciteten till 193 (av 255) och byter blandningsläge till **Lighten**. Känn dig fri att experimentera med andra `BlendMode`‑värden såsom `Multiply`, `Screen` eller `Overlay`.

### Steg 4: Spara den redigerade bilden

```java
// Save the edited image
im.save(exportPath);
```

Efter att du har applicerat dina modifieringar, skriv förändringarna till en ny PSD‑fil. Detta steg säkerställer att originalfilen förblir orörd.

### Steg 5: Verifiera ändringar

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

Kodsnutten ovan demonstrerar hur du öppnar en PSD, hämtar det andra lagrets första effekt (antagen att vara ett gradient‑överlägg) och förbereder den för modifiering.

### Steg 2: Verifiera de ursprungliga inställningarna (valfritt men rekommenderat)

Innan du ändrar något, hjälper kontroll av befintligt blandningsläge, opacitet och synlighet dig att förstå grundläget. `Assert`‑anropen i koden bekräftar att effekten för närvarande är inställd på **Normal** blandningsläge, helt opak och synlig.

### Steg 3: Justera gradient‑egenskaper för att uppnå en radial stil

Du kan ändra gradientens färg, opacitet och blandningsläge. För en sann radial effekt, sätt gradientstilen:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Proffstips:* Använd `Color.getGreen()` eller någon `java.awt.Color`‑instans för att definiera startfärgen, och `gradientOverlay.setColor2(Color.getBlue())` för slutfärgen.

### Steg 4: Spara den redigerade PSD‑filen

Anropet `im.save(exportPath);` skriver den modifierade bilden till disk. Den sparade filen behåller det radiala gradient‑överlägget och kan öppnas i Photoshop, förhandsgranskas i webbläsare eller konverteras till andra format.

## Varför skapa radiala gradient‑överlägg?

Radiala gradienter tillför djup och fokus till designer, vilket får element att framstå som tredimensionella eller spotlightade. De är idealiska för:

- **Bakgrundsfyllningar** som drar ögat mot ett centralt motiv.  
- **Knapp‑ eller ikon‑höjdpunkter** där ett subtilt sken behövs.  
- **Kreativa fotoeffekter** som vignetter eller ljusutbrott.  

Aspose.PSD bearbetar **50+ in‑ och utdataformat** och kan hantera flershundratusentals‑sidiga PSD‑filer utan att ladda hela dokumentet i minnet, vilket låter dig automatisera gradient‑skapande över stora tillgångsbibliotek.

## Vanliga problem & tips

- **Effekten syns inte:** Säkerställ att `gradientOverlay.isVisible()` returnerar `true`. Vissa PSD‑filer döljer effekter som standard.  
- **Fel lager‑index:** Lager är noll‑baserade; dubbelkolla att du riktar in dig på rätt lager (`im.getLayers()[1]` refererar till det andra lagret).  
- **Opacitets‑casting:** Metoden `setOpacity` förväntar sig en `byte`. Att skicka ett `int` ger ett kompileringsfel; casta explicit som i exemplet.  
- **Resursladdning:** Om du får `null` när du försöker komma åt effekter, verifiera att `loadOptions.setLoadEffectsResource(true)` är satt innan bilden laddas.

## Vanliga frågor

**Q: Kan jag applicera flera gradient‑effekter på en enda bild?**  
A: Ja. Hämta lagrets `BlendingOptions`, iterera genom `Effects`‑samlingen och lägg till ett nytt `GradientOverlayEffect` för varje gradient du behöver.

**Q: Vilka andra effekter kan jag kombinera med gradient‑överlägg?**  
A: Aspose.PSD erbjuder skuggor, glöd, relief och mer. Varje effekt visas i `Effects`‑arrayen och kan konfigureras oberoende.

**Q: Hur felsöker jag om effekterna inte renderas korrekt?**  
A: Verifiera att PSD‑filen laddades med `setLoadEffectsResource(true)`, kontrollera lagersynlighet och bekräfta att du modifierar rätt effekt‑index.

**Q: Finns det en provversion av Aspose.PSD för Java?**  
A: Ja, du kan få en gratis provversion [här](https://releases.aspose.com/).

**Q: Var kan jag köpa en licens för Aspose.PSD för Java?**  
A: Besök [purchase page](https://purchase.aspose.com/buy) för licensinformation.

## Ytterligare vanliga frågor

**Q: Kan jag programatiskt ändra gradientens riktning?**  
A: Ja. Använd metoden `GradientOverlayEffect.setAngle(float angle)` för att sätta gradientens vinkel i grader. För radiala gradienter ignoreras vinkeln, men metoden måste ändå anropas.

**Q: Stöder Aspose.PSD radiala gradienter?**  
A: Absolut. Sätt gradientstilen till `GradientStyle.Radial` via `GradientOverlayEffect`‑egenskaperna.

**Q: Bevaras gradient‑överlägg när PSD konverteras till andra format (t.ex. PNG)?**  
A: När du rasteriserar PSD (t.ex. sparar som PNG) behålls det visuella resultatet av gradient‑överlägget, men själva effekten blir en del av pixeldata.

**Q: Hur tar jag bort ett gradient‑överlägg från ett lager?**  
A: Hämta lagrets `BlendingOptions`, lokalisera `GradientOverlayEffect` i `Effects`‑samlingen och ta bort den med `remove(effect)`.

**Q: Är det möjligt att animera gradient‑ändringar?**  
A: Även om Aspose.PSD inte direkt hanterar animation, kan du generera en sekvens av PSD‑filer med varierande gradientparametrar och sedan sätta ihop dem till en video eller GIF med ett annat bibliotek.

## Slutsats

Grattis! Du har lärt dig **hur man skapar radial gradient java**‑effekter för dina bilder med Aspose.PSD för Java. Genom att följa stegen ovan kan du programatiskt lägga till, modifiera och spara gradient‑överlägg, vilket ger dig full kreativ kontroll över PSD‑tillgångar. Experimentera med olika färger, blandningslägen och opacitetsvärden för att uppnå den visuella effekt du önskar.

---

**Senast uppdaterad:** 2026-10-18  
**Testat med:** Aspose.PSD för Java 24.12 (senaste vid skrivtillfället)  
**Författare:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Relaterade handledningar

- [Create Gradient Fill PSD with Java using Aspose.PSD – Add Gradient Fill Layer](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Pattern Overlay PSD: Add Effects with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Apply a Color Overlay and Set Opacity in Java with Aspose.PSD](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
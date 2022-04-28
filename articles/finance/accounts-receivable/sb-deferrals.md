---
title: Uitgestelde opbrengsten en onkosten in Facturering van abonnementen
description: In dit onderwerp wordt uitgelegd hoe u uitgestelde opbrengsten en onkosten instelt in Facturering van abonnementen.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 5ff8d2f4663c53bf6dece1ef9af6609d5f0c5b50
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544481"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Uitgestelde opbrengsten en onkosten in Facturering van abonnementen

In dit onderwerp wordt uitgelegd hoe u uitgestelde opbrengsten en onkosten instelt en gebruikt in Facturering van abonnementen. Uitstelplanningen zijn altijd gebaseerd op en afhankelijk van een onderliggend oorspronkelijk document of factureringsplanning. Omdat ze worden gemaakt op basis van standaardwaarden, kunnen ze niet afzonderlijk worden ingevoerd of gemaakt.

Het proces van het instellen en gebruiken van uitgestelde opbrengsten en onkosten vindt plaats op meerdere pagina's:

- Op de pagina **Parameters voor uitgestelde opbrengsten en onkosten** kunt u de bedrijfsvoorkeuren definiëren.
- Op de pagina **Standaardinstellingen voor uitstellen** kunt u de standaardrekeningen en -sjablonen instellen die moeten worden gebruikt voor de uitstelplanningen.
- Op de pagina's **Uitstelsjablonen** en **Op gebeurtenissen gebaseerde uitstelsjablonen** kunt u de sjablonen definiëren die moeten worden gebruikt voor de uitstelplanningen.
- Op de pagina **Alle uitstelplanningen** kunt u uitstelplanningen weergeven en bewerken.

Uitgestelde opbrengsten en onkosten kunnen samen met terugkerende contractfacturering worden gebruikt.

## <a name="revenue-and-expense-deferral-parameters"></a>Uitstelparameters voor opbrengsten en onkosten

De pagina **Parameters voor uitgestelde opbrengsten en onkosten** bevat de volgende velden.

| Veld | Description |
|---|---| 
| Het tabblad **Planning** | |
| Gelijk per periode | <p>Geef op of het aantal dagen in een periode moet worden gebruikt wanneer het bedrag per periode wordt berekend voor een uitstelplanning:</p><ul><li>**Ja**: het bedrag voor elke periode is gelijk, ongeacht het aantal dagen in de periode. Gedeeltelijke perioden (zoals perioden aan het begin of einde van een uitstelplanning) worden evenredig gecorrigeerd.</li><li>**Nee**: het bedrag wordt berekend op basis van het aantal dagen in elke periode.</li></ul><p>U kunt deze instelling overschrijven op transactieniveau.</p> |
| Uitsteloptie voor verkoopkorting | <p>Geef op of afzonderlijke uitstelplanningen moeten worden gemaakt voor de kortings- en verkooporderbedragen:</p><ul><li>**Aparte planning voor korting**: het kortingsbedrag wordt gescheiden gehouden van het opbrengstbedrag.<p>In dit geval worden er twee uitstelplanningen gemaakt wanneer een verkooporder wordt gemaakt en vervolgens wordt geboekt. De kortings- en opbrengstbedragen worden naar verschillende uitstelrekeningen geboekt.</p></li><li>**Korting samenvoegen met opbrengst**: het kortingsbedrag wordt gecombineerd met het opbrengstbedrag. Er wordt één uitstelplanning gemaakt en zowel het kortingsbedrag als het opbrengstbedrag wordt naar dezelfde uitstelrekening geboekt.<p>In dit geval wordt er één uitstelplanning gemaakt wanneer een verkooporder wordt gemaakt en vervolgens wordt geboekt. Zowel het kortingsbedrag als het opbrengstbedrag wordt naar dezelfde uitstelrekening geboekt.</p></li></ul><p>**Opmerking:** als u kortingen wilt toepassen op artikelen die gebruikmaken van de functie voor niet-gefactureerde opbrengst, selecteert u de optie **Afzonderlijke planning voor korting**. Kortingen kunnen vervolgens op alle artikelen worden toegepast, ongeacht of de functie voor niet-gefactureerde opbrengst wordt gebruikt. Als de optie **Korting samenvoegen met opbrengst** is geselecteerd, kunnen kortingen niet worden toegepast op artikelen die gebruikmaken van de functie voor niet-gefactureerde opbrengst.</p> |
| Uitsteloptie voor inkoopkorting | <p>Geef op of afzonderlijke uitstelplanningen moeten worden gemaakt voor de kortings- en inkooporderbedragen:</p><ul><li>**Aparte planning voor korting**: het kortingsbedrag wordt gescheiden gehouden van het onkostenbedrag.<p>In dit geval worden er twee uitstelplanningen gemaakt wanneer een inkooporder wordt gemaakt en vervolgens wordt geboekt. De kortings- en onkostenbedragen worden naar verschillende uitstelrekeningen geboekt.</p></li><li>**Korting samenvoegen met opbrengst**: het kortingsbedrag wordt gecombineerd met het onkostenbedrag. Er wordt één uitstelplanning gemaakt en zowel het kortingsbedrag als het onkostenbedrag wordt naar dezelfde uitstelrekening geboekt.<p>In dit geval wordt er één uitstelplanning gemaakt wanneer een inkooporder wordt gemaakt en vervolgens wordt geboekt. Zowel het kortingsbedrag als het onkostenbedrag wordt naar dezelfde uitstelrekening geboekt.</p></li></ul> |
| Eerdere perioden consolideren | <p>Geef op of uitstelplanningsregels voor eerdere perioden worden geconsolideerd:</p><ul><li>**Ja**: als de begindatum van de uitstel in een periode vóór de transactiedatum valt, worden alle bedragen tot en met de periode van de transactiedatum samengevoegd op één uitstelplanningsregel.</li><li>**Nee**: de bedragen uit alle perioden worden op afzonderlijke regels van de uitstelplanning gehouden.<p>Als de begindatum van het uitstel in dezelfde periode of een latere periode dan de transactiedatum valt, heeft deze optie geen effect.</p></li></ul><p>Deze instelling kan worden bijgewerkt op transactieniveau.</p> |
| Standaard begindatum voor uitstel | <p>Selecteer de regel die wordt gebruikt om de begindatum van de uitstelplanning te bepalen:</p><ul><li>**Transactiedatum**: gebruik de transactiedatum als begindatum.</li><li>**Begin van huidige maand**: gebruik de eerste van de huidige maand als begindatum. Als de transactiedatum de eerste van een maand is, is de eerste van de huidige maand de begindatum.</li><li>**Begin van volgende maand**: gebruik de eerste van de volgende maand als begindatum. Als de transactiedatum de eerste dag van de maand is, wordt de transactiedatum gebruikt. Anders wordt de eerste van de volgende maand gebruikt.</li><li>**Regel van 15**: als de transactiedatum tussen de eerste en de vijftiende ligt, gebruikt u de eerste van de huidige maand als begindatum. Als de transactiedatum op de zestiende of een latere datum valt, gebruikt u de eerste van de volgende maand als begindatum.</li></ul><p>U kunt deze instelling bijwerken op transactieniveau.</p> |
| Uitstelmethode korte termijn | <p>Selecteer de uitstelmethode voor de korte termijn: **Geen**, **Doorlopende perioden** of **Vast jaar**.</p><p>|
| Boekingsmethode voor uitstel | <p>Selecteer de methode die wordt gebruikt om uitsteltransacties te maken.</p><ul><li>**Balans:** gebruik de boekingsmethode voor balansen om uitsteltransacties te maken.</li><li>**Winst en verlies**: gebruik de boekingsmethode voor winst en verlies om uitsteltransacties te maken. Wanneer transacties worden geboekt, kunt u het factuurboekstuk controleren om de extra vermeldingen te zien die de tegenbedragen voor de eerste toerekening en toerekening in balans brengen.</li></ul> |
| Winst en verlies omkeren op krediet | <p>**Opmerking**: dit veld is alleen beschikbaar als het veld **Uitgestelde boekingsmethode** is ingesteld op **Winst en verlies**.</p><p>Geef op of de winst- en verliesbedragen worden teruggeboekt wanneer een omkering, beëindiging of restitutie wordt toegepast op een factureringsplanning of verkooporder:</p><ul><li>**Ja**: de winst- en verliesbedragen worden omgekeerd en op de uitstelplanning wordt een creditcorrectiebedrag toegepast.<p>Als de omkering tijdens een factureringsperiode plaatsvindt, worden de bedragen gecorrigeerd.</p></li><li>**Nee**: er wordt geen terugboektransactie gemaakt voor de winst- en verliesbedragen wanneer een omkering, beëindiging of restitutie wordt toegepast op een factureringsplanning of verkooporder.</li></ul> |
| Het tabblad **Toerekening** | |
| Algemene journalen automatisch boeken | <p>Geef op of journaalposten die door uitgestelde opbrengsten en onkosten worden gemaakt, automatisch worden geboekt:</p><ul><li>**Ja**: journaalposten die door uitgestelde opbrengsten en onkosten worden gemaakt, worden automatisch geboekt.<p>**Tip:** als u **Ja** selecteert, kunt u inconsistenties in de boekhouding voorkomen die worden veroorzaakt door handmatige wijzigingen in boekstukken.</p></li><li>**Nee**: journaalposten die door uitgestelde opbrengsten en onkosten worden gemaakt, worden niet automatisch geboekt. U moet journalen handmatig boeken.</li></ul> |
| Toerekeningsjournaal samenvatten | <p>Geef op of toerekeningsboekstukken standaard worden geconsolideerd:</p><ul><li>**Ja**: maak een enkel boekstuk voor alle toerekeningsregels met dezelfde datum. Alle regels in een boekstuk met dezelfde rekening worden geconsolideerd op één regel.</li><li>**Nee**: maak een boekstuk voor elke toerekeningsregel.</li></ul><p>U kunt deze instelling bijwerken op de pagina **Verwerking van toerekening**.</p> |
| Standaardjournaalnaam | Selecteer de journaalnaam voor journalen die zijn gemaakt op basis van processen voor uitgesteld opbrengsten en onkosten, zoals de verwerking van toerekeningen. |
| Beschrijving van journaalregel voor toerekening | <p>Selecteer de beschrijving die wordt weergegeven in de omschrijving van de journaalboekstukregel:</p><ul><li>**Planningsregeldatums**: de planningsregeldatums worden weergegeven in de journaalregelbeschrijving.</li><li>**Oorspronkelijke transactiedetails**: de oorspronkelijke transactiegegevens worden weergegeven in de journaalregelbeschrijving.<p>**Voorbeeld:** USMF-0001, CIV-00839, Softwareopbrengsten</p></li></ul> |
| Het tabblad **Nummerreeksen** | Op dit tabblad kunt u de standaardwaarden voor leasenummerreeksen instellen. De wizard voor het genereren van nummerreeksen wordt gebruikt om automatisch nummerreeksen te genereren en toe te wijzen. U hoeft de nummerreeks alleen te wijzigen als u handmatig wijzigingen wilt aanbrengen in de gegenereerde nummerreeksen. |
| Planningsnummer | Het nummer in de nummerreeks die wordt gebruikt voor uitstelplanningen. |

## <a name="deferral-templates"></a>Uitstelsjablonen

Gebruik de pagina **Uitstelsjablonen** om lineaire sjablonen te definiëren die worden gebruikt voor uitstelplanningen.

Hier volgen enkele voordelen van het gebruik van een sjabloon:

* De lengte van het uitstel wordt automatisch berekend.
* U staat uitstelplanningen toe met perioden waarin de toerekening wordt overgeslagen.
* U kunt uitstellen automatiseren door de sjabloon toe te wijzen aan een product, een productgroep, een productcategorie, klanten of een klantgroep. Sjabloontoewijzing wordt uitgevoerd vanaf de pagina **Standaardinstellingen voor uitstellen**.

Er zijn verschillende periodefrequenties beschikbaar voor sjablonen: dagelijks, maandelijks of boekperioden.

De sjabloonregels bestaan uit een type (**Herkend** of **Overgeslagen**) en de lengte van de periode. Overgeslagen regels hebben een bedrag van 0 (nul) op de uitstelplanningsregels. Dit gedrag kan nuttig zijn als u niet in alle perioden opbrengsten wilt toerekenen.

### <a name="create-a-deferral-template"></a>Een uitstelsjabloon maken

Volg deze stappen om een uitstelsjabloon te maken.

1. Selecteer **Nieuw** op de pagina **Uitstelsjablonen**.
2. Voer in het veld **Sjabloon** een naam in.
3. Voer in het veld **Beschrijving** een beschrijving in.
4. Selecteer in het veld **Periodefrequentie** de periodefrequentie.
5. Selecteer **Toevoegen** om een regel toe te voegen aan het begin van de lijst met regels of selecteer **Toevoegen** om een regel toe te voegen aan het einde van de lijst.
6. Selecteer in het veld **Type** het type periode.
7. Geef in het veld **Periode** de lengte van de periode op.
8. Herhaal stap 5 tot en met 7 voor elke regel die u nodig hebt.
9. Selecteer **Opslaan**.

## <a name="deferral-defaults"></a>Standaardwaarden voor uitstel

Gebruik de pagina **Standaardinstellingen voor uitstellen** voor het instellen van standaardrekeningen voor uitstellen voor artikelen en voor het toewijzen van standaardsjablonen aan artikelen die kunnen worden uitgesteld. U kunt ook uitstelrekeningen voor toeslagen instellen en sjablonen toewijzen aan de uit te stellen toeslagen.

**Uitstellen per artikel**

Voor transacties met een artikel (bijvoorbeeld verkooporders) kunt u rekeningen en sjablonen toewijzen aan specifieke artikelen en klanten. Deze instellingen worden gebruikt als standaardwaarden wanneer een transactie wordt uitgesteld. Om de transactie standaard uitstelbaar te maken, moet u de artikelen instellen op de pagina **Artikelen die kunnen worden uitgesteld**.

**Uitstellen per rekening**

Voor transacties die geen artikelen hebben (bijvoorbeeld algemene journalen), kunt u de uitstelrekeningen opgeven. Wanneer deze rekeningen worden gebruikt op een transactieregel, wordt de transactie automatisch gemarkeerd als uitgesteld. De bijbehorende sjabloon- en toerekeningsrekening worden toegewezen aan de transactieregel.

**Alle transactietypen (bijvoorbeeld op de tabbladen Verkooporder, Inkoop en Algemeen)**

De rekeningen op de pagina zijn de hoofdrekeningen die geen financiële dimensies hebben. De financiële dimensies van de toerekeningsrekening zijn afkomstig van de klant of het artikel, gebaseerd op uw organisatie.

Elke sjabloonregel moet een lineaire sjabloon of een op gebeurtenissen gebaseerde sjabloon bevatten. Het kan niet beide bevatten.

### <a name="for-sales-orders"></a>Voor verkooporders

Als u de standaardwaarden voor uitstel voor verkooporders wilt opgeven, gaat u als volgt te werk.

1. Selecteer het type uitstel op het tabblad **Verkooporder**.
2. Selecteer **Toevoegen** om een regel toe te voegen.
3. Selecteer de artikelcode in het veld **Artikelcode**. De artikelcode bepaalt hoe de standaardwaarden voor uitstel worden toegepast.
4. Geef op hoe de artikelcode wordt toegepast:

    * Als het veld **Artikelcode** is ingesteld op **Tabel** of **Groep**, selecteert u de artikelrelatie in het veld **Artikelrelatie**.
    * Als het veld **Artikelcode** is ingesteld op **Categorie**, selecteert u de categorierelatie in het veld **Categorierelatie**.
    * Als het veld **Artikelcode** is ingesteld op **Alle**, zijn de standaardwaarden van toepassing op alle toepasselijke records.

5. Geef op hoe de rekeningcode wordt toegepast:

    * Als het veld **Rekeningcode** is ingesteld op **Tabel** of **Groep**, selecteert u de rekeningrelatie in het veld **Rekeningrelatie**.
    * Als het veld **Rekeningcode** is ingesteld op **Alle**, is de rekening van toepassing op alle records.

6. Selecteer in het veld **Hoofdrekening** de hoofdrekening voor het uitstel.
7. Als het veld **Uitgestelde boekingsmethode** is ingesteld op **Verlies en winst**, selecteert u de rekening voor de eerste opbrengst in het veld **Rekening eerste opbrengst** en de tegenrekening voor de opbrengst in het veld **Tegenrekening opbrengst**.
8. Als het veld **Uitstelmethode korte termijn** is ingesteld op **Doorlopende perioden** of **Vast jaar**, selecteert u de rekening voor uitstel voor de korte termijn in het veld **Rekening uitstel korte termijn**.
9. Voor een sjabloon kunt u **Toevoegen** selecteren om een regel toe te voegen.
10. Selecteer de artikelcode in het veld **Artikelcode**.
11. Geef op hoe de artikelcode wordt toegepast:

    * Als het veld **Artikelcode** is ingesteld op **Tabel** of **Groep**, selecteert u de artikelrelatie in het veld **Artikelrelatie**.
    * Als het veld **Artikelcode** is ingesteld op **Categorie**, selecteert u de categorierelatie in het veld **Categorierelatie**.
    * Als het veld **Artikelcode** is ingesteld op **Alle**, zijn de standaardwaarden van toepassing op alle toepasselijke records.

12. Geef op hoe de rekeningcode wordt toegepast:

    * Als het veld **Rekeningcode** is ingesteld op **Tabel** of **Groep**, selecteert u de rekeningrelatie in het veld **Rekeningrelatie**.
    * Als het veld **Rekeningcode** is ingesteld op **Alle**, is de rekening van toepassing op alle toepasselijke records.
    * Selecteer de lineaire sjabloon in het veld **Lineaire sjabloon** of de op gebeurtenissen gebaseerde sjabloon in het veld **Op gebeurtenissen gebaseerde sjabloon**.

13. Selecteer **Opslaan**.

### <a name="for-purchase-orders"></a>Voor inkooporders

Als u de standaardwaarden voor uitstel voor inkooporders wilt opgeven, gaat u als volgt te werk.

1. Selecteer het type uitstel op het tabblad **Inkoop**.
2. Selecteer **Toevoegen** om een regel toe te voegen.
3. Selecteer de artikelcode in het veld **Artikelcode**.
4. Geef op hoe de artikelcode wordt toegepast:

    * Als het veld **Artikelcode** is ingesteld op **Tabel** of **Groep**, selecteert u de artikelrelatie in het veld **Artikelrelatie**.
    * Als het veld **Artikelcode** is ingesteld op **Categorie**, selecteert u de categorierelatie in het veld **Categorierelatie**.
    * Als het veld **Artikelcode** is ingesteld op **Alle**, zijn de standaardwaarden van toepassing op alle toepasselijke records.

5. Geef op hoe de rekeningcode wordt toegepast:

    * Als het veld **Rekeningcode** is ingesteld op **Tabel** of **Groep**, selecteert u de rekeningrelatie in het veld **Rekeningrelatie**.
    * Als het veld **Rekeningcode** is ingesteld op **Alle**, is de rekening van toepassing op alle toepasselijke records.

6. Selecteer in het veld **Hoofdrekening** de hoofdrekening voor het uitstel.
7. Als het veld **Uitgestelde boekingsmethode** is ingesteld op **Verlies en winst**, selecteert u de rekening voor de eerste opbrengst in het veld **Rekening eerste opbrengst** en de tegenrekening voor de opbrengst in het veld **Tegenrekening opbrengst**.
8. Als het veld **Uitstelmethode korte termijn** is ingesteld op **Doorlopende perioden** of **Vast jaar**, selecteert u de rekening voor uitstel voor de korte termijn in het veld **Rekening uitstel korte termijn**.
9. Voor een sjabloon selecteert u **Toevoegen** om een regel toe te voegen. 
10. Selecteer de artikelcode in het veld **Artikelcode**.
11. Geef op hoe de artikelcode wordt toegepast:

    * Als het veld **Artikelcode** is ingesteld op **Tabel** of **Groep**, selecteert u de artikelrelatie in het veld **Artikelrelatie**.
    * Als het veld **Artikelcode** is ingesteld op **Categorie**, selecteert u de categorierelatie in het veld **Categorierelatie**.
    * Als het veld **Artikelcode** is ingesteld op **Alle**, zijn de standaardwaarden van toepassing op alle toepasselijke records.

12. Geef op hoe de rekeningcode wordt toegepast:

    * Als het veld **Rekeningcode** is ingesteld op **Tabel** of **Groep**, selecteert u de rekeningrelatie in het veld **Rekeningrelatie**.
    * Als het veld **Rekeningcode** is ingesteld op **Alle**, is de rekening van toepassing op alle toepasselijke records.
    * Selecteer de lineaire sjabloon in het veld **Lineaire sjabloon** of de op gebeurtenissen gebaseerde sjabloon in het veld **Op gebeurtenissen gebaseerde sjabloon**.

13. Selecteer **Opslaan**.

### <a name="for-general-journals"></a>Voor algemene journalen

Als u de standaardwaarden voor uitstel voor boekingen in het algemene journaal wilt opgeven, gaat u als volgt te werk.

1. Selecteer het tabblad **Algemeen journaal**.
2. Voor een uitstel selecteert u **Toevoegen** om een regel toe te voegen.
3. Als het veld **Uitstelmethode korte termijn** is ingesteld op **Doorlopende perioden** of **Vast jaar**, selecteert u de rekening voor uitstel voor de korte termijn in het veld **Rekening uitstel korte termijn**.
4. Selecteer de uitstelrekening in het veld **Uitstelrekening**.
5. Selecteer de toerekeningsrekening in het veld **Toerekeningsrekening**.
6. Als het veld **Uitgestelde boekingsmethode** is ingesteld op **Verlies en winst**, selecteert u de rekening voor de eerste opbrengst in het veld **Rekening eerste opbrengst** en de tegenrekening voor de opbrengst in het veld **Tegenrekening opbrengst**.
7. Selecteer de lineaire sjabloon in het veld **Lineaire sjabloon** of de op gebeurtenissen gebaseerde sjabloon in het veld **Op gebeurtenissen gebaseerde sjabloon**.
8. Selecteer **Opslaan**.

### <a name="for-free-text-invoices"></a>Voor vrije-tekstfacturen

Als u de standaardwaarden voor uitstel voor vrije-tekstfacturen wilt opgeven, gaat u als volgt te werk.

1. Selecteer het tabblad **Vrije-tekstfactuur**.
2. Voor een uitstel selecteert u **Toevoegen** om een regel toe te voegen.
3. Geef op hoe de rekeningcode wordt toegepast:

    * Als het veld **Rekeningcode** is ingesteld op **Tabel** of **Groep**, selecteert u de rekeningrelatie in het veld **Rekeningrelatie**.
    * Als het veld **Rekeningcode** is ingesteld op **Alle**, is de rekeningcode van toepassing op alle toepasselijke records.

4. Selecteer de uitstelrekening in het veld **Uitstelrekening**.
5. Als het veld **Uitstelmethode korte termijn** is ingesteld op **Doorlopende perioden** of **Vast jaar**, selecteert u de rekening voor uitstel voor de korte termijn in het veld **Rekening uitstel korte termijn**.
6. Selecteer de toerekeningsrekening in het veld **Toerekeningsrekening**.
7. Als het veld **Uitgestelde boekingsmethode** is ingesteld op **Verlies en winst**, selecteert u de rekening voor de eerste opbrengst in het veld **Rekening eerste opbrengst** en de tegenrekening voor de opbrengst in het veld **Tegenrekening opbrengst**.
8. Selecteer de lineaire sjabloon in het veld **Lineaire sjabloon** of de op gebeurtenissen gebaseerde sjabloon in het veld **Op gebeurtenissen gebaseerde sjabloon**.
9. Selecteer **Opslaan**.

### <a name="for-invoice-journals"></a>Voor factuurjournalen

Als u de standaardwaarden voor uitstel voor boekingen in factuurjournalen wilt opgeven, gaat u als volgt te werk.

1. Selecteer het tabblad **Factuurjournaal**.
2. Voor een uitstel selecteert u **Toevoegen** om een regel toe te voegen.
3. Geef op hoe de rekeningcode wordt toegepast:

    * Als het veld **Rekeningcode** is ingesteld op **Tabel** of **Groep**, selecteert u de rekeningrelatie in het veld **Rekeningrelatie**.
    * Als het veld **Rekeningcode** is ingesteld op **Alle**, is de rekeningcode van toepassing op alle toepasselijke records.

4. Selecteer de uitstelrekening in het veld **Uitstelrekening**.
5. Als het veld **Uitstelmethode korte termijn** is ingesteld op **Doorlopende perioden** of **Vast jaar**, selecteert u de rekening voor uitstel voor de korte termijn in het veld **Rekening uitstel korte termijn**.
6. Selecteer de toerekeningsrekening in het veld **Toerekeningsrekening**.
7. Als het veld **Uitgestelde boekingsmethode** is ingesteld op **Verlies en winst**, selecteert u de rekening voor de eerste opbrengst in het veld **Rekening eerste opbrengst** en de tegenrekening voor de opbrengst in het veld **Tegenrekening opbrengst**.
8. Selecteer de lineaire sjabloon in het veld **Lineaire sjabloon** of de op gebeurtenissen gebaseerde sjabloon in het veld **Op gebeurtenissen gebaseerde sjabloon**.
9. Selecteer **Opslaan**.

### <a name="items-that-are-deferred-by-default"></a>Artikelen die standaard worden uitgesteld

Gebruik de pagina **Artikelen die standaard worden uitgesteld** om op te geven welke artikelen standaard worden uitgesteld. U kunt de transactietypen instellen waarvoor de artikelen worden uitgesteld. U kunt opgeven of een enkel artikel of een hele artikelgroep of -categorie wordt uitgesteld.

Wanneer u artikelen instelt als uitgesteld, selecteert u de standaardrekeningen en sjablonen op de pagina **Standaardinstellingen voor uitstellen**. Als de rekeningen en sjablonen niet zijn geselecteerd, worden transactieregels waarop deze artikelen zijn ingevoerd, niet uitgesteld.

Voor artikelen die zijn uitgesteld op basis van de verkoop- of inkoopcategorie waar ze aan zijn gekoppeld, zijn de uitstelinstellingen gebaseerd op de categorie. Als de categorie echter niet is geselecteerd in het veld **Categorierelatie**, worden uitstelinstellingen gebruikt van de hoger gerangschikte categorie. U kunt bijvoorbeeld een verkoopcategorie **Homevideo's** toevoegen, maar geen verkoopcategorie **Televisie**. Wanneer u een uitstelartikel toevoegt dat is gekoppeld aan de categorie **Televisie**, worden de uitstelinstellingen van **Homevideo** gebruikt voor het artikel.

### <a name="set-up-deferred-items"></a>Uitgestelde artikelen instellen

Volg deze stappen om artikelen in te stellen die standaard worden uitgesteld.

1. Selecteer op de pagina **Artikelen die standaard worden uitgesteld** het gewenste tabblad (**Verkooporder** of **Inkoop**).
2. Selecteer **Toevoegen** om een regel toe te voegen.
3. Selecteer de artikelcode in het veld **Artikelcode**.
4. Geef op hoe de artikelcode wordt toegepast:

    * Als het veld **Artikelcode** is ingesteld op **Groep** of **Tabel**, selecteert u de artikelrelatie in het veld **Artikelrelatie**.
    * Als het veld **Artikelcode** is ingesteld op **Categorie**, selecteert u de categorierelatie in het veld **Categorierelatie**.

5. Herhaal stap 2 tot en met 4 voor elke regel die u nodig hebt.
6. Selecteer **Opslaan**.

## <a name="deferred-charges"></a>Uitgestelde toeslagen

Gebruik de pagina **Uitsteltoeslagen** om op te geven welke toeslagen standaard worden uitgesteld.

> [!NOTE]
> * Op dit moment zijn uitstelbare toeslagen alleen beschikbaar voor verkooporders.
> * Wijzigingen kunnen alleen worden uitgesteld op regelniveau. Als u een toeslag op koptekstniveau van de verkooporder wilt uitstellen, kunt u de toeslag instellen als uitgesteld artikel op een aparte regel op de verkooporder.
> * Als u een toeslag voor een vrije-tekstfactuur wilt uitstellen, moet u de toeslag als een aparte regel voor een uitgestelde factuur invoeren.
> * Deze functionaliteit is niet beschikbaar voor ondersteuningstoeslagen en de functionaliteit voor opbrengstsplitsing.

### <a name="set-up-deferred-charges"></a>Uitgestelde toeslagen instellen

Voer de onderstaande stappen uit om uitgestelde toeslagen in te stellen:

1. Selecteer **Toevoegen** op de pagina **Uitsteltoeslagen** om een regel toe te voegen.
2. Selecteer de toeslagcode in het veld **Toeslagcode**.
3. Selecteer de toeslagrelatie in het veld **Toeslagrelatie**.
4. Herhaal stap 1 tot en met 3 voor elke regel die u nodig hebt.
5. Selecteer **Opslaan**.

## <a name="event-based-deferral-templates"></a>Op gebeurtenissen gebaseerde uitstelsjablonen

Gebruik de pagina **Op gebeurtenissen gebaseerde uitstelsjablonen** om op gebeurtenissen gebaseerde uitstelsjablonen te definiëren die u kunt gebruiken in uitsteltransacties en kunt toewijzen op de pagina **Standaardinstellingen voor uitstellen**.

### <a name="create-an-event-based-template"></a>Een sjabloon op basis van gebeurtenissen maken

Volg deze stappen om een op gebeurtenissen gebaseerde uitstelsjabloon te maken.

1. Selecteer **Nieuw** op de pagina **Op gebeurtenissen gebaseerde uitstelsjablonen**.
2. Voer in het veld **Sjabloon** een unieke naam voor de sjabloongroep in.
3. Voer in het veld **Beschrijving** een beschrijving in.
4. Selecteer het toewijzingstype in het veld **Toewijzingstype**.

    * **Variabel bedrag**: wijs een specifiek bedrag toe voor elke regel die wordt ingevoerd.
    * **Gelijk bedrag**: wijs hetzelfde bedrag toe voor elke regel die wordt ingevoerd. 
    * **Percentage**: wijs een bedrag toe dat is gebaseerd op de percentagewaarde die voor elke regel wordt ingevoerd.
    * **Voltooiingspercentage:** wijs een cumulatieve voltooiingswaarde toe voor elke regel die wordt ingevoerd.
    * **Variabele hoeveelheid**: wijs een specifieke hoeveelheid toe voor elke regel die wordt ingevoerd.

5. Stel de optie **Afzonderlijke gebeurtenissen per eenheid maken** in op **Ja** als u wilt dat elke gebeurtenisregel gelijkmatig wordt gesplitst op basis van het aantal eenheden in de factuurtransactie. Stel de optie in op **Nee** als u de gebeurtenisregels niet wilt splitsen.
6. Selecteer de verlooprekening in het veld **Verlooprekening**.
7. Selecteer **Toevoegen** om een regel toe te voegen aan het begin van de lijst met regels of selecteer **Toevoegen** om een regel toe te voegen aan het einde van de lijst.
8. Voer in het veld **Beschrijving** een beschrijving voor de gebeurtenis in.
9. Als u **Percentage** hebt geselecteerd in het veld **Toewijzingstype**, geeft u in het veld **Toewijzingspercentage** het toewijzingspercentage op. Het percentage moet tussen 0 en 100 liggen. Als u het veld **Toewijzingspercentage** leeg laat, wordt het percentage beschouwd als 0. De som van de percentages wordt weergegeven in het veld **Totale percentage** onder aan de pagina en moet gelijk zijn aan 100.
10. Geef in het veld **Maanden tot vervaldatum** het aantal maanden op dat de gebeurtenis geldig is. De vervaldatum van de transactie-uitstel wordt automatisch ingevoerd op basis van deze waarde.
11. Schakel het selectievakje **Toerekenen bij boeking** in om opbrengsten automatisch toe te rekenen wanneer de transactie wordt geboekt. Als u het selectievakje uitgeschakeld laat, moet de opbrengst handmatig worden toegerekend.
12. Selecteer in het veld **Toerekeningsrekening** de toerekeningsrekening voor de gebeurtenis als voor de gebeurtenis een andere rekening wordt gebruikt dan voor de hele uitstelplanning. Dit veld wordt samen met het selectievakje **Toerekenen bij boeking** gebruikt.
13. Herhaal stap 7 tot en met 12 voor elke regel die u nodig hebt.
14. Selecteer **Opslaan**.

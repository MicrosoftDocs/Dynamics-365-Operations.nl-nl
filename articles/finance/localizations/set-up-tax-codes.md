---
title: Belastingcodes instellen
description: In dit artikel wordt uitgelegd hoe u belastingcodes instelt in de service voor belastingberekening.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 1bc250716763ce9d8e25c8850c8a3676bf65fb0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862923"
---
# <a name="set-up-tax-codes"></a>Belastingcodes instellen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u belastingcodes instelt in de service voor belastingberekening. Het bevat de instelling voor een eenvoudig scenario om de belastingcode te laten werken en informatie over bepaalde geavanceerde functionaliteit voor btw-code voor complexe scenario's.

> [!IMPORTANT]
> De instelling van belastingcodes in de service voor belastingberekening is onafhankelijk van rechtspersoon. U kunt deze configuratie maar één keer voltooien in RCS (Regulatory Configuration Service). Belastingcodes worden automatisch gesynchroniseerd met Microsoft Dynamics 365 Finance wanneer u de service voor belastingberekening inschakelt voor een geselecteerde rechtspersoon in Finance.

## <a name="simple-setup"></a>Eenvoudige instellingen

Volg deze stappen om een belastingcode te gebruiken in een eenvoudig scenario, zoals een scenario waarbij er slechts één belastingtarief is.

1. Meld u aan bij [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Ga in naar **Werkruimten** \> **Globaliseringsfuncties** \> **Belastingberekening**.
3. Selecteer de functie en versie die u wilt instellen en selecteer **Bewerken**.
4. Selecteer **Configuratieversie** op het tabblad **Algemeen**.
5. Selecteer op het tabblad **Belastingcodes** de optie **Toevoegen** en voer de belastingcode en een beschrijving in.
6. Selecteer **Oorsprong van berekening**. Een berekeningsoorsprong is een groep methoden die worden gedefinieerd in de versie van de geselecteerde belastingconfiguratie. Selecteer voor dit eenvoudige scenario de optie **Op nettobedrag**.
7. Selecteer **Opslaan**. Er komen meer velden beschikbaar, op basis van de berekeningsoorsprong die u hebt geselecteerd.
8. Selecteer **Toevoegen** op het sneltabblad **Tarieven** om één belastingtarief voor deze belastingcode toe te voegen.
9. Selecteer **Opslaan**.

## <a name="calculation-origin"></a>Berekeningsoorsprong

De berekeningsoorsprong bepaalt hoe het basisbedrag van de belasting en het belastingbedrag worden berekend. Deze wordt geconfigureerd op basis van de belastingconfiguratie in de werkruimte **Elektronische rapportage**. De volgende waarden zijn beschikbaar in het veld **Oorsprong van berekening**:

- Op nettobedrag
- Op brutobedrag
- Op hoeveelheid
- Op marge
- Belasting op belasting

### <a name="by-net-amount"></a>Op nettobedrag

Als u **Op nettobedrag** selecteert in het veld **Oorsprong van berekening**, wordt het belastingbedrag berekend als een percentage van het inkoop- of verkoopbedrag, exclusief eventuele andere belastingcodes.

Als het belastingtarief bijvoorbeeld 25 procent is, bevat de factuurregel een hoeveelheid van 10 artikelen van 1,00 per stuk en krijgt de klant een regelkorting van 10 procent. In dit geval worden bedragen als volgt berekend:

- **Nettobedrag:** (10 × 1,00) – 10 procent = 9,00 
- **Btw:** 9,00 × 25 procent = 2,25 
- **Totaal factuurbedrag:** 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Op brutobedrag

Als u **Op brutobedrag** selecteert in het veld **Oorsprong van berekening**, wordt het belastingbedrag berekend als een percentage van het brutoverkoopbedrag. Het brutobedrag is het nettobedrag van de regel plus alle belastingen en toeslagen voor de regel behalve de ene belasting waarvoor het veld **Oorsprong van berekening** is ingesteld op **Op brutobedrag**.

De belastingdienst heeft bijvoorbeeld een artikel met speciale heffingen belast. De heffingsbedragen worden toegevoegd aan het nettobedrag voordat de belasting wordt berekend. De volgende belastingcodes worden gebruikt:

- **Heffing 1**: het tarief is 10 procent en de berekeningsmethode **Op nettobedrag** wordt gebruikt.
- **Heffing 2**: het tarief is 20 procent en de berekeningsmethode **Op nettobedrag** wordt gebruikt.
- **Belastingtarief**: het tarief is 25 procent en de berekeningsmethode **Op brutobedrag** wordt gebruikt.

Als het nettobedrag 10,00 is, is het bedrag van heffing 1 1,00 (10,00 × 10 procent) en is het bedrag van heffing 2 2,00 (10,00 × 20 procent). In dit geval worden bedragen als volgt berekend: 

- **Brutobedrag:** nettobedrag + bedrag heffing 1 + bedrag heffing 2 = 10,00 +1,00 + 2,00 = 13,00 
- **Belastingbedrag:** 13,00 × 25 procent = 3,25 
- **Totaal van heffingen en belasting** = 1,00 + 2,00 + 3,25 = 6,25 
- **Totaal factuurbedrag:** 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Op hoeveelheid

Als u **Op hoeveelheid** in het veld **Oorsprong van berekening** selecteert, wordt het belastingbedrag als vast bedrag per eenheid berekend en vermenigvuldigd met de hoeveelheid die op de documentregel wordt ingevoerd. Het bedrag per eenheid wordt opgegeven op het sneltabblad **Tarieven**.

De belastingcode is bijvoorbeeld ingesteld als 1,20 per eenheid. Op een verkoopfactuurregel worden 25 eenheden van een artikel verkocht. In dit geval wordt het belastingbedrag berekend als 25 x 1,20 = 30,00.

### <a name="by-margin"></a>Op marge

Als u **Op marge** selecteert in het veld **Oorsprong van berekening**, wordt het belastingbedrag berekend als een percentage van de verkoopmarge. De verkoopmarge is het verkoopbedrag min de kostprijs. Deze berekeningsmethode geldt alleen voor verkooptransacties.

Als het belastingtarief bijvoorbeeld 25 procent is, bevat de factuurregel een hoeveelheid van 10 artikelen van 10,00 per stuk en bedragen de kosten per artikel 6. In dit geval worden bedragen als volgt berekend:

- **Verkoopmarge:** 10 x (10,00 – 6,00) = 40,00
- **Belastingbedrag:** 40,00 × 25 procent = 10,00
- **Totaal factuurbedrag:** 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Belasting op belasting

Als u **Belasting op belasting** selecteert in het veld **Oorsprong van berekening**, wordt de btw berekend als een percentage van alle andere belastingbedragen op dezelfde documentregel.

De volgende belastingcodes kunnen worden gebruikt:

- **Heffing 1**: het tarief is 10 procent en de berekeningsmethode **Op nettobedrag** wordt gebruikt.
- **Heffing 2**: het tarief is 20 procent en de berekeningsmethode **Op nettobedrag** wordt gebruikt.
- **Belasting op heffing**: het tarief is 25 procent en de berekeningsmethode **Belasting op belasting** wordt gebruikt.

In dit geval worden bedragen als volgt berekend:

- **Nettobedrag:** 10,00 
- **Heffing 1:** 10,00 x 10 procent = 1,00 
- **Heffing 2:** 10,00 x 20 procent = 2,00 
- **Heffing op belasting:** 3,00 × 25 procent = 0,75
- **Totale belasting:** 1,00 + 2,00 + 0,75 = 3,75 
- **Totaal factuurbedrag:** 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Geavanceerde functionaliteit

In deze sectie wordt een aantal geavanceerde functionaliteiten van de belastingcodeconfiguratie voor complexe scenario's uitgelegd.

### <a name="tax-exemption"></a>Belastingvrijstelling

Als u de optie **Is vrijgesteld** op **Ja** instelt op het sneltabblad **Algemeen**, wordt het belastingbedrag altijd overschreven door 0 (nul), ongeacht het daadwerkelijke belastingtarief.

U kunt het veld **Vrijstellingscode** instellen om de reden voor de vrijstelling op te geven. 

U kunt het opzoeken van hoofdgegevens voor het veld **Vrijstellingscode** inschakelen. Op die manier kunt u kiezen uit de vrijstellingscodewaarden die in Finance zijn gedefinieerd. Zie [Zoeken van hoofdgegevens voor btw-berekeningsconfiguratie inschakelen](tax-service-set-up-environment-master-data-lookup.md) voor informatie over het inschakelen van het opzoeken van hoofdgegevens.

Het belastingtarief is bijvoorbeeld 25 procent en de optie **Is vrijgesteld** is ingesteld op **Ja** voor de belastingcode. De factuurregel bevat een hoeveelheid van 10 artikelen voor € 1,00 per stuk en de klant heeft recht op een regelkorting van 10 procent. In dit geval worden bedragen als volgt berekend:

- **Nettobedrag:** (10 × 1,00) – 10 procent = 9,00 
- **Btw:** 0,00 
- **Totaal factuurbedrag:** 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Gebruiksbelasting

Als u de optie **Is gebruiksbelasting** op **Ja** instelt op het sneltabblad **Algemeen**, wordt het belastingbedrag naar de account **Te betalen gebruiksbelasting** geboekt in plaats van naar de account **Overzichtsrekening**.

Het belastingtarief is bijvoorbeeld 25 procent en de optie **Is gebruiksbelasting** is ingesteld op **Ja** voor de belastingcode. De factuurregel bevat een hoeveelheid van 10 artikelen voor € 1,00 per stuk en de klant heeft recht op een regelkorting van 10 procent. In dit geval worden bedragen als volgt berekend:

- **Nettobedrag:** (10 × 1,00) – 10 procent = 9,00 
- **Gebruiksbelasting:** 9,00 × 25 procent = 2,25
- **Totaal factuurbedrag:** 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Als zowel **Is vrijgesteld** als **Is gebruiksbelasting** is ingesteld op **Ja** voor een belastingcode, wordt de code herkend als vrijgesteld van btw voor verkooptransacties en gebruiksbelasting voor inkooptransacties.

### <a name="reverse-charges"></a>Terugboekingen

Als u de optie **Is terugboeking** op het sneltabblad tabblad **Algemeen** op **Ja** instelt, kan het btw-tarief als negatief worden ingesteld. Stel voor een terugboekingsscenario twee belastingcodes in, waarvan de ene een positief belastingtarief heeft en de andere een negatief belastingtarief. Beide belastingcodes moeten dezelfde tariefwaarde hebben en de optie **Is terugboeking** moet worden ingesteld op **Ja** voor de belastingcode met een negatief belastingtarief. Zie [Mechanisme voor omgekeerde toeslagen van btw/GST-schema](emea-reverse-charge.md) voor meer informatie over de terugboekingsoplossing in Finance.

Er worden bijvoorbeeld twee belastingcodes bepaald op één factuurregel. Eén belastingtarief is 25 procent. Het andere belastingtarief is -25 procent en de optie **Is terugboeking** is ingesteld op **Ja** voor de tweede belastingcode. Op de factuurregel staat een hoeveelheid van 10 artikelen voor 1,00 per stuk. In dit geval worden de bedragen als volgt berekend:

- **Nettobedrag:** (10 × 1,00) = 10,00 
- **Belastingcode 1:** 10,00 × 25 procent = 2,50
- **Belastingcode 2:** 10 × -25 procent = -2,50
- **Totaal factuurbedrag:** 10,00 + 2,50 -2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Uitsluiting van berekeningen van basisbedrag

Als u de optie **Uitsluiten van berekening van basisbedrag** op **Ja** instelt op het sneltabblad **Algemeen**, wordt het berekende belastingbedrag van de belastingcode uitgesloten van het basisbedrag voor belastingen voor andere belastingcodeberekeningen in het prijsinclusieve scenario.

Zie voor meer informatie [Belasting berekenen over prijzen wanneer Prijzen inclusief belastingen is ingeschakeld](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Tarieven

Op het sneltabblad **Tarief** kunt u verschillende belastingtarieven definiëren voor verschillende bereiken van belastingbasisbedragen. Voor het berekenen van het belastingbedrag wordt door de service voor belastingberekening altijd het tarief gebruikt dat overeenkomt met het basisbedrag voor belasting.

Belastingtarieven kunnen bijvoorbeeld zo worden geconfigureerd als in de volgende tabel wordt weergegeven.

| Minimumbedrag | Maximumbedrag | Belastingtarief   |
| -------------- | -------------- | ---------- |
| 0              | 1.000          | 10 procent |
| 1.000          | 5.000          | 15 procent |
| 5.000          | 10,000         | 20 procent |
| 10,000         | 0              | 30 procent |

In dit geval wordt het belastingbedrag als volgt berekend:

- Als het belastingbasisbedrag 300,00 is, is het belastingpercentage 10 procent en is het belastingbedrag 300,00 × 10 procent = 30,00.
- Als het belastingbasisbedrag 3000,00 is, is het belastingpercentage 15 procent en is het belastingbedrag 3000,00 × 15 procent = 450,00.
- Als het belastingbasisbedrag 6000,00 is, is het belastingpercentage 20 procent en is het belastingbedrag 6000,00 × 10 procent = 1200,00.
- Als het belastingbasisbedrag 20.000,00 is, is het belastingpercentage 30 procent en is het belastingbedrag 20.000,00 × 30 procent = 6.000,00.

> [!NOTE]
> Als het belastingbasisbedrag zowel met het maximumbedrag op de ene regel als met het minimumbedrag op de andere regel kan overeenkomen, wordt het belastingtarief gebruikt dat overeenkomt met het minimumbasisbedrag. Dus als het belastingbasisbedrag 1000,00 is, is het belastingpercentage 15 procent en is het belastingbedrag 1.000,00 × 15 procent = 150,00.

### <a name="limits"></a>Grenswaarden

Op het sneltabblad **Limieten** kunt u belastinglimieten definiëren om het berekende belastingbedrag te overschrijven als het belastingbedrag binnen het minimum-/maximumbereik valt.

- Als het berekende belastingbedrag hoger dan of gelijk is aan het maximale belastingbedrag dat op het sneltabblad **Limieten** is ingesteld, is het uiteindelijke belastingbedrag gelijk aan het maximale belastingbedrag.
- Als het berekende belastingbedrag lager is dan het minimale belastingbedrag op het sneltabblad **Limieten**, is het uiteindelijke belastingbedrag 0 (nul).

De belastinglimieten worden bijvoorbeeld als volgt geconfigureerd:

- **Minimaal belastingbedrag:** 100 
- **Maximaal belastingbedrag:** 1000

Als het berekende belastingbedrag 2000 is, is het uiteindelijke belastingbedrag 1000.

Als het berekende belastingbedrag 500 is, is het uiteindelijke belastingbedrag 500.

Als het berekende belastingbedrag 80 is, is het uiteindelijke belastingbedrag 0 (nul).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

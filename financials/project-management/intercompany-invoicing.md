---
title: intercompany-facturering
description: Dit artikel bevat informatie en voorbeelden met betrekking tot intercompany-facturering voor projecten in Microsoft Dynamics 365 for Operations.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 65c20479af9d2184bd7f3b92f4c0718553425502
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="intercompany-invoicing"></a>intercompany-facturering

[!include[banner](../includes/banner.md)]


Dit artikel bevat informatie en voorbeelden met betrekking tot intercompany-facturering voor projecten in Microsoft Dynamics 365 for Operations.

Uw organisatie kan meerdere afdelingen, dochterondernemingen en andere rechtspersonen hebben die producten en services aan elkaar overdrachten voor projecten. De rechtspersoon die het product of de service levert, wordt de *uitlenende rechtspersoon* genoemd en de rechtspersoon die de service of het product ontvangt, de *lenende rechtspersoon*. 

In de volgende afbeelding ziet u een typisch scenario waarbij twee rechtspersonen, SI FR (de lenende rechtspersoon) en SI VS (de uitlenende rechtspersoon) bronnen delen voor het leveren van een project aan klant A. In dit scenario is SI FR gecontracteerd om het werk aan klant A te leveren. 

[![Voorbeeld van intercompany-facturering](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Het doel is kostenbeheer, verantwoording van opbrengsten, belastingen en verrekenprijs voor intercompany-projecttransacties flexibeler en krachtiger te maken. Daarnaast worden de volgende mogelijkheden geboden:

-   Klantfacturen voor een project bij een lenende rechtspersoon maken met behulp van intercompany-roosters, kosten en facturen van leveranciers bij een uitlenende rechtspersoon.
-   Btw-berekeningen en indirecte kosten ondersteunen.
-   Verantwoording van opbrengsten in een uitlenende rechtspersoon en het moment waarop een lenende rechtspersoon de kosten moet verantwoorden uitstellen.
-   OHW-omzet (onderhanden werk) in de uitlenende rechtspersoon toerekenen.
-   Transferprijzen instellen die kunnen worden gebaseerd op verschillende prijsmodellen. Hieronder vindt u enkele voorbeelden:
    -   **Hoeveelheid** – Het bedrag dat u invoert in het veld **Prijscalculatie** zijn de werkelijke kosten per hoeveelheid of eenheid.
    -   **Bedrag van toeslagen** – De prijs/kosten per transactie plus het bedrag aan toeslagen. Dit bedrag wordt ingevoerd in het veld **Prijscalculatie** .
    -   **Percentage van toeslagen** – De verrekenprijs is de prijs/kosten per transactie vermenigvuldigd met het percentage van toeslagen. Dit percentage wordt ingevoerd in het veld **Prijscalculatie**.
    -   **Percentage van verkoopprijs** – Het percentage van de verkoopprijs dat wordt overgebracht naar de uitlenende rechtspersoon.
    -   **Bedrag beneden verkoopprijs** – Het bedrag dat de lenende rechtspersoon achterhoudt van de verkoopprijs voor overdracht aan de uitlenende rechtspersoon.
    -   **Bijdrageverhouding** – Het getal dat u invoert in het veld **Prijscalculatie** is de bijdrageverhouding, uitgedrukt als een percentage van de verkoopprijs.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Voorbeeld 1: Parameters voor intercompany-facturering instellen
In dit voorbeeld is USSI een uitlenende rechtspersoon en rapporteren de resources tijd tegen de lenende rechtspersoon, FRSI, die eigenaar is van het contract met de eindklant. Uren en kosten die werknemers van USSI rapporteren kunnen worden opgenomen in de projectfactuur die FRSI genereert. Bovendien is er een derde bron van transacties die afkomstig kunnen zijn van de uitlenende rechtspersoon (USSI in dit voorbeeld) wanneer deze gedeelde leveranciersservices levert aan dochterondernemingen (zoals FRSI) en vervolgens deze kosten doorgeeft aan projecten binnen die dochterondernemingen. Alle overeenkomende factuurdocumenten en btw-berekeningen worden uitgevoerd door Dynamics 365 for Operations. 

In dit voorbeeld moet FRSI een klant zijn in de rechtspersoon USSI en moet USSI een leverancier zijn in de rechtspersoon FRSI. U kunt vervolgens een intercompany-relatie opzetten tussen de twee rechtspersonen. De volgende procedure laat zien hoe de parameters zodanig kunnen worden ingesteld dat beide rechtspersonen kunnen deelnemen aan intercompany-facturering.

1.  Stel FRSI in als een klant in de rechtspersoon USSI en stel USSI in als een leverancier in de rechtspersoon FRSI. Er zijn drie ingangspunten voor de stappen die zijn vereist voor deze taak.
    | Stap | Invoerpunt                                                                       | Omschrijving   |
    |------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | A    | Klik in USSI op **Klanten** &gt; **Klanten** &gt; **Alle klanten**. | Maak een nieuwe klantrecord voor FRSI en selecteer de klantgroep.                                                                                                                                                                                                                           |
    | B    | Klik in FRSI op **Leveranciers** &gt; **Leveranciers** &gt; **Alle leveranciers**.        | Maak een nieuwe leveranciersrecord voor USSI en selecteer de leveranciersgroep.                                                                                                                                                                                                                               |
    | C    | Open in FRSI de leveranciersrecord die u zojuist hebt gemaakt.                            | Klik in het actievenster op het tabblad **Algemeen** in de groep **Instellen** op **Intercompany**. Stel op de pagina **Intercompany**, op het tabblad **Handelsrelatie**, de schuifregelaar **Actief** in op **Ja**. Selecteer in het veld **Klantbedrijf** de klantrecord die u hebt gemaakt in stap A. |

2.  Klik op **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Projectbeheer- en boekhoudingsparameters** en klik vervolgens op het tabblad **Intercompany**. De manier waarop u de parameters instelt, is afhankelijk van of u de lenende rechtspersoon of de uitlenende rechtspersoon bent.
    -   Als u de lenende rechtspersoon bent, selecteert u de aanschaffingscategorie die moet worden gebruikt voor het afstemmen van de leveranciersfacturen, die automatisch worden gegenereerd.
    -   Als u de uitlenende rechtspersoon bent, selecteert u voor elke lenende rechtspersoon een standaard projectcategorie voor elk transactietype. Projectcategorieën worden gebruikt voor btw-configuratie wanneer de gefactureerde categorie in intercompany-transacties alleen bestaat in de lenende rechtspersoon. U kunt de opbrengst samenvoegen voor intercompany-transacties. Deze samenvoeging vindt plaats wanneer de transacties worden geboekt en wordt vervolgens omgekeerd wanneer de intercompany-factuur wordt geboekt.

3.  Klik op **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Prijzen** &gt; **Prijs overboeken**.
4.  Selecteer een valuta, transactietype en prijsmodel voor overboeking. De valuta die wordt gebruikt op de factuur is de valuta die is geconfigureerd in de klantrecord voor de lenende rechtspersoon bij de uitlenende rechtspersoon. De valuta wordt gebruikt voor het afstemmen van vermeldingen in de tabel met verrekenprijzen.
5.  Klik op **Grootboek** &gt; **Boekingsinstellingen** &gt; **Intercompany-boekhouding** en stel een relatie in voor USSI en FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Voorbeeld 2: Een intercompany-urenstaat maken en boeken
USSI, de uitlenende rechtspersoon, moet de urenstaat maken en boeken voor een project van FRSI, de lenende rechtspersoon. Er zijn twee ingangspunten voor de stappen die zijn vereist voor deze taak.

| Stap | Invoerpunt                                                                       | Omschrijving                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projectbeheer en boekhouding** &gt; **Urenstaten** &gt; **Alle urenstaten** | Maak een nieuwe urenstaat. Selecteer op de urenstaatregel, in het veld **Rechtspersoon**, de optie **FRSI**. Selecteer het correcte project in RSI in het veld **Project-id**. Voer de uren in voor elke dag van de week. |
| B    | Pagina **Urenstaat**                                                                | Nadat de werkstroom wordt uitgevoerd, boekt u de urenstaat en noteert u het boekstuknummer.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Voorbeeld 3: Een intercompany-leveranciersfactuur maken en boeken
USSI, de uitlenende rechtspersoon, moet de intercompany-leveranciersfactuur maken en boeken voor een project van FRSI, de lenende rechtspersoon. Deze leveranciersfactuur vertegenwoordigt het uitbestede werk en kosten die zijn uitgevoerd door leveranciers die worden betaald door USSI. Er zijn twee ingangspunten voor de stappen die zijn vereist voor deze taak.

| Stap | Invoerpunt                                                                                      | Omschrijving                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Leveranciers** &gt; **Facturen** &gt; **Openstaande leveranciersfacturen** &gt; **Nieuwe leveranciersfactuur** | Maak een nieuwe leveranciersfactuur en voer de services in die zijn aangeschaft voor het project van FRSI.                                                                                                                                                                                  |
| B    | De pagina **Leveranciersfactuur**                                                                      | Voer regels in die de uitbestede services die zijn uitgevoerd namens FRSI vertegenwoordigen. Voer op het sneltabblad **Regeldetails**, op het tabblad **Project** voor de factuurregel, in het veld **Projectbedrijf** de waarde **FRSI** in. Voer het project en de bijbehorende informatie in. Boek vervolgens de leveranciersfactuur. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Voorbeeld 4: De intercompany-factuur maken en boeken
USSI, de uitlenende rechtspersoon, moet de intercompany-factuur maken en boeken. Er zijn twee ingangspunten voor de stappen die zijn vereist voor deze taak.

| Stap | Invoerpunt                                                                                             | Omschrijving                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projectbeheer en boekhouding** &gt; **Projectfacturen** &gt; **Intercompany-klantfactuur**  | Klik op **Nieuw** om de pagina **Intercompany-factuur maken** te openen.                                                                                  |
| B    | **Projectbeheer en boekhouding** &gt; **Projectfacturen** &gt; **Intercompany-klantfacturen** | Voer op de pagina **Intercompany-factuur maken** de rechtspersoon in, geef de transactie op die moet worden opgenomen en klik vervolgens op **Zoeken**. |
| C    | **Projectbeheer en boekhouding** &gt; **Projectfacturen** &gt; **Intercompany-klantfacturen** | Selecteer de te factureren transacties of klik op **Alles selecteren** om alle transacties in de lijst te factureren en klik vervolgens op **OK**.                  |
| D    | De pagina **Intercompany-factuur**                                                                       | Het voorstel voor de intercompany-klantfactuur wordt weergegeven.                                                                                             |
| E    | De pagina **Intercompany-factuur**                                                                       | Klik op **Boeken**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Voorbeeld 5: De leveranciersfactuur boeken en de klant factureren
Wanneer de uitlenende rechtspersoon, USSI, de intercompany-klantfactuur boekt, wordt een overeenkomende openstaande leveranciersfactuur gemaakt in de lenende rechtspersoon, FRSI. Nadat deze leveranciersfactuur is geboekt, factureert FRSI tevens de projectklant voor de uren die USSI heeft ingevoerd. Er zijn drie ingangspunten voor de stappen die zijn vereist voor deze taak.

| Stap | Invoerpunt                                                                                        | Omschrijving                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Leveranciers** &gt; **Facturen** &gt; **Openstaande leveranciersfacturen**                            | Bekijk de factuur om te controleren of de waarden van de urenstaat zijn opgenomen en boek vervolgens de leveranciersfactuur.                  |
| B    | **Projectbeheer en boekhouding** &gt; **Projectfacturen** &gt; **Projectfactuurvoorstellen** | Maak een nieuwe projectfactuur voor het project en controleer of de uurtransacties die zijn geboekt worden weergegeven.            |
| C    | De pagina **Projectfactuur**                                                                       | Selecteer de projectfactuur en klik vervolgens op **Details weergeven** om de kosten en omzetbedragen te controleren. Boek vervolgens de factuur. |







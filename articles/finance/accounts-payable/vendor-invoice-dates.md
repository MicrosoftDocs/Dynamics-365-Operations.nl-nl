---
title: Datums leveranciersfactuur
description: In dit artikel worden de datums beschreven die op leveranciersfacturen staan. Verder wordt uitgelegd hoe de boekingsdatum automatisch wordt aangepast.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 022fd0ce07fbb4c54afcf7334c1c9411e01dcf26
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775263"
---
# <a name="vendor-invoice-dates"></a>Datums leveranciersfactuur

[!include [banner](../includes/banner.md)]

In dit artikel worden de datums beschreven die op leveranciersfacturen staan. Verder wordt uitgelegd hoe de boekingsdatum automatisch wordt aangepast.

De factuurkoptekst op de pagina **Details leveranciersfactuur in behandeling** bevat vier datums: de **Ontvangstdatum voor factuur**, **Factuurdatum**, **Boekingsdatum** en **Vervaldatum**. Wanneer u een leveranciersfactuur maakt, worden de volgende datums standaard ingevoerd:

- **Ontvangstdatum factuur** – Dit veld is ingesteld op de huidige systeemdatum.
- **Boekingsdatum** – Dit veld is ingesteld op de huidige systeemdatum. 
- **Vervaldatum** – De datum in dit veld wordt berekend op basis van de boekingsdatum en betalingsvoorwaarden.
- **Factuurdatum**: dit veld is standaard leeg. U kunt echter zo nodig een waarde invoeren. In dat geval wordt de datum in het veld **Vervaldatum** opnieuw berekend op basis van de factuurdatum en betalingsvoorwaarden.

Soms is de status van een leveranciersfactuur lange tijd In behandeling na het sluiten van de periode. Wanneer deze gereed is voor boeken, wordt nog steeds de oude boekingsdatum van de afgelopen boekingsperiode gebruikt. Deze periode is echter nu afgesloten. Daarom moet een leveranciersmedewerker handmatig alle boekingsdatums wijzigen in de nieuwe boekingsperiode voor alle eerder gemaakte facturen in behandeling.

Met de functie die in dit artikel wordt beschreven, kunt u de boekingsdatum automatisch aanpassen aan de behoeften van het bedrijf.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parameter voor het automatisch aanpassen van de boekingsdatum van de leveranciersfactuur

Volg deze stappen om de boekingsdatum voor leveranciersfacturen automatisch aan te passen.

1.  Ga naar **Leveranciers \> Instellen \> Parameters leveranciers**.
2.  Selecteer op het tabblad **Grootboek en btw** in het veld **Boekingsdatum automatisch aanpassen** een van de volgende waarden:

    - **Geen wijziging**: de boekingsdatum wordt niet automatisch gewijzigd tijdens het boeken. Standaard is deze waarde geselecteerd.
    - **Boekingsdatum altijd wijzigen in systeemdatum**: de boekingsdatum wordt tijdens het boeken automatisch gewijzigd in de systeemdatum.
    - **De boekingsdatum wijzigen in de systeemdatum wanneer de boekingsdatumperiode wordt afgesloten of in de wachtstand wordt gezet**: de boekingsdatum wordt tijdens het boeken automatisch gewijzigd in de systeemdatum, maar alleen als de bijbehorende periode van de boekingsdatum de status **Afgesloten** of **In wachtstand** heeft.
    - **De boekingsdatum wijzigen in de eerste dag van de nieuwe periode wanneer de boekingsdatumperiode wordt afgesloten of in de wachtstand wordt gezet**: de boekingsdatum wordt gewijzigd in de eerste dag van de nieuwe open periode, maar alleen als de bijbehorende periode van de boekingsdatum de status **Afgesloten** of **In wachtstand** heeft.

> [!NOTE]
> Als de nieuwe boekingsdatum die automatisch is gecorrigeerd in een nieuw boekjaar valt, wordt de boekingsdatum van de factuur niet bijgewerkt. De gebruiker krijgt de foutmelding Het boekjaar is gewijzigd. Controleer dit en voer de boekingsdatum opnieuw in. De factuurboekingsdatum moet worden bijgewerkt naar de datum van het nieuwe boekjaar om deze te kunnen boeken.

## <a name="impact-of-posting-date-changes"></a>Impact van wijzigingen boekingsdatum

Wanneer de boekingsdatum op een leveranciersfactuur in behandeling wordt gewijzigd, heeft de wijziging de volgende effecten:

- **Vervaldatum**

    - Als het veld **Vervaldatum** leeg is, wordt de vervaldatum opnieuw berekend op basis van de nieuwe boekingsdatum en betalingsvoorwaarden.
    - Als het veld **Factuurdatum** eerder is ingesteld, heeft de wijziging van de boekingsdatum geen invloed op de vervaldatum.

- **Datum voor contantkorting**

    - Als het veld **Factuurdatum** leeg is, wordt de nieuwe boekingsdatum gebruikt om de contantkorting te berekenen.
    - Als het veld **Factuurdatum** eerder is ingesteld, wordt de contantkorting niet gewijzigd.

- **Wisselkoers**: de wisselkoersdatum wordt bepaald door de instelling van de optie **Leveranciersboekhouding bijwerken met de factuurdatum** op het tabblad **Factuur** van de pagina **Leveranciersparameters** (**Leveranciers \> Instellingen \> Parameters leveranciers**).

    - Als deze optie is ingesteld op **Ja** wordt de **factuurdatum** gebruikt en heeft de wijziging van de **boekingsdatum** geen invloed op de wisselkoers.
    - Als deze optie is ingesteld op **Nee**, wordt de boekingsdatum gebruikt om de wisselkoers te berekenen. Wanneer de boekingsdatum wordt bijgewerkt, worden de bedragen voor boekhouding en rapportage opnieuw berekend. Daarom moet vereffeningsvalidatie opnieuw worden uitgevoerd.

## <a name="validation"></a>Validatie

Twee andere velden op het tabblad **Factuur** van de pagina **Parameters van module Leveranciers** (**Leveranciers \> Instellingen \> Parameters leveranciers**) beïnvloeden factuurverwerking:

- Als het veld **Het gebruikte factuurnummer controleren** is ingesteld op **Duplicaten in fiscaal jaar afwijzen**, wordt de boekingsdatum gebruikt om te controleren op dubbele facturen tijdens factuurboeking.
- Als het veld **Documentdatum vereisen voor leveranciersfactuur** is ingesteld op **Foutoptie**, is het veld **Factuurdatum op factuurkoptekst in behandeling** verplicht. Als de factuurdatum later is dan de boekingsdatum, wordt een foutbericht weergegeven.

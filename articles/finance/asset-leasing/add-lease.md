---
title: Leases toevoegen of kopiëren (preview)
description: In dit artikel wordt beschreven hoe u een nieuwe lease maakt door informatie in te voeren in Activa leasen of door gegevens uit een bestaande lease te kopiëren.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 798ab3ece45ee6f21694a364cfb7a4ff14a9c8aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880927"
---
# <a name="add-or-copy-leases-preview"></a>Leases toevoegen of kopiëren (preview)

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u een geheel nieuwe lease maakt in Activa leasen en hoe u een lease kunt maken door een bestaande lease te kopiëren. Het proces voor het maken van een nieuwe lease omvat het invoeren van gegevens voor de nieuwe lease en het maken van een leaseschema. Nadat er ten minste één lease is ingesteld, kunt u de informatie uit een bestaande lease kopiëren en vervolgens de gegevens bewerken die u nodig hebt om een nieuwe lease te maken.

## <a name="create-a-lease"></a>Een lease maken

Volg deze stappen om een lease te maken in Activa leasen.

1. Selecteer op de pagina **Leaseoverzicht** in het actievenster de optie **Nieuw**.
2. Voer gegevens over de lease in. Vereiste velden hebben een rode rand.

De begindatum voor de leasebetaling kan niet voor de begindatum van de lease vallen. Als u een begindatum opgeeft voor de leasebetaling die eerder is dan de begindatum voor de lease, wordt een foutbericht weergegeven.

De optie **Betalingsbedrag opsplitsen** op het sneltabblad **Algemeen** van de pagina **Leasedetails** is standaard ingesteld op **Nee** als de optie **Betaling opsplitsen toestaan** op de pagina **Parameters voor Activa leasen** is ingesteld op **Ja**. 

Als de optie **Betalingsbedrag opsplitsen** is ingesteld op **Ja**, is het veld **Betalingsbedrag** op het sneltabblad **Betalingsschemaregels** vergrendeld. Deze wordt ingesteld op het totaal van de betalingsbedragen die later worden ingevoerd in de catalogus **Opsplitsing van betalingsbedragen**.

Selecteer **Opsplitsing van betalingsbedragen** om een pagina te openen waar u de gespecificeerde betalingstypen kunt toevoegen. Met de knop **Totalen toevoegen aan betalingsbedrag** worden de totalen naar het veld **Betalingsbedrag** verplaatst.

> [!NOTE]
> Als u een gespecificeerd betalingsbedrag toevoegt en vervolgens op **Esc** drukt, worden de ingevoerde bedragen niet toegevoegd aan het veld **Betalingsbedrag** op het sneltabblad **Betalingsschemaregels**. In plaats daarvan worden ze opgeslagen in het dialoogvenster **Opsplitsing van betalingsbedragen**. Als u wilt dat in het dialoogvenster het totaalbedrag wordt weergegeven, selecteert u de kolom **Bedrag**, selecteert u deze waarde en houdt u deze vast (of klikt u met de rechtermuisknop) en selecteert u vervolgens **Deze kolom totaliseren**. 

Met de knop **Regel kopiëren** kopieert u de gespecificeerde betalingsbedragen.

## <a name="create-a-lease-schedule"></a>Een leaseschema maken

Nadat u de gegevens voor de lease hebt ingevoerd, voert u de volgende stappen uit om een leaseschema te maken.

> [!NOTE]
> De financiële dimensies kunnen op basis van aangepaste financiële dimensies worden gewijzigd.

1. Selecteer **Schema's maken** om de leaseboeken te genereren. De leaseboeken omvatten de schema's voor betaling, aflossing, afschrijving en onkosten.
2. Als u de leaseboeken wilt openen en de nieuwe schema's wilt weergeven, selecteert u het tabblad **Boeken**.

    De pagina **Boekdetails** geeft aan hoe de lease wordt verwerkt in de boeken die aan de lease zijn toegewezen. Hier kunt u de leaseschema's bekijken.

    Het betalingsschema bevat de invoer uit het tabblad **Betalingsschemaregels** op de pagina **Lease toevoegen**. U kunt nog steeds alle betalingsbedragen en variabele betalingen wijzigen. De leaseverplichtingen worden berekend op basis van het aangepaste betalingsschema.

    > [!NOTE]
    > De begindatum voor de leasebetaling moet dezelfde of een latere datum zijn dan de begindatum voor de lease. U ontvangt een foutbericht als de begindatum voor de leasebetaling eerder is dan de begindatum voor de lease. 

4. Wanneer u klaar bent met het controleren van het betalingsschema, selecteert u **Schema bevestigen**. Nadat het schema is bevestigd, kan de lease niet meer worden bewerkt.

    > [!NOTE]
    > De leaseperiode wordt automatisch berekend op basis van de regels van het betalingsschema op de pagina **Lease toevoegen**.
    >
    > Voor het berekenen van de leasetermijn in maanden neemt het systeem het verschil tussen de begin- en einddatum van een specifieke betalingsschemaregel. Vervolgens wordt op de volgende betalingsschemaregel opnieuw het verschil berekend. Ten slotte telt het systeem alle bedragen op om de leasetermijn in maanden te bepalen.

5. Als u rentekosten voor de berekende periode wilt weergeven, opent u de pagina **Afschrijvingsschema leaseverplichtingen**. Als u berekende lineaire afschrijving wilt weergeven, opent u de pagina **Afschrijvingsschema voor activa**.
6. Nadat u het berekende bedrag hebt gecontroleerd, kunt u de eerste journaalpost voor toerekening maken op de pagina **Eerste toerekening**. U ontvangt een bericht waarin wordt gemeld dat het journaal is gemaakt.

    > [!NOTE]
    > De journaalpost wordt pas naar het grootboek geboekt als u de post handmatig boekt.

7. Als u de voorgestelde eerste toerekeningspost wilt controleren voordat u deze boekt, selecteert u **Activaleasejournaal**.

    > [!NOTE]
    > Het Activaleasejournaal kan niet handmatig worden gemaakt. Het wordt automatisch gemaakt wanneer er leaseschema's worden gemaakt.

8. Wanneer u klaar bent met het controleren van de eerste journaalpost voor toerekening en gereed bent om deze te boeken, selecteert u **Boeken** om het activum met gebruiksrecht en de leaseverplichtingen in het grootboek te verantwoorden.

## <a name="copy-a-lease"></a>Een lease kopiëren

Met Activa leasen kunt u de details van een lease kopiëren om een nieuwe lease te maken met dezelfde informatie. U kunt de leasevelden vervolgens wijzigen voordat u de schema's voor de gekopieerde lease maakt.

1. Selecteer op de pagina **Leaseoverzicht** de lease die u wilt kopiëren en selecteer vervolgens in het actievenster **Lease kopiëren**.

    > [!NOTE]
    > Als de parameter **Handmatig** is uitgeschakeld voor de nummerreeks voor lease-id's, wordt het volgende nummer in de reeks automatisch gegenereerd als de lease-id van de gekopieerde lease. Als de parameter **Handmatig** is ingeschakeld, ontvangt u een bericht waarin u wordt gevraagd de lease-id op te geven voordat u doorgaat met het kopiëren van de lease.

2. Selecteer **Kopiëren**. De leasegegevens van de geselecteerde lease worden naar een nieuwe lease gekopieerd. U kunt vervolgens de details van de nieuwe lease bewerken voordat u deze opslaat en de leaseschema's maakt.

## <a name="asset-leasing-journal"></a>Activaleasejournaal

Alle journaalposten die zijn gemaakt in Activa leasen worden opgenomen in het activaleasejournaal. Op de pagina **Activaleasejournaal** (**Activa leasen \> Journaalboekingen \> Activaleasejournaal**) kunt u filteren op boekingsstatus, specifieke journaalboekingen en boekstukken weergeven en niet-geboekte journaalboekingen boeken.

> [!NOTE]
> Het Activaleasejournaal kan niet handmatig worden gemaakt. Het wordt automatisch gemaakt wanneer er leaseschema's worden gemaakt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Leases toevoegen of kopiëren (preview)
description: In dit onderwerp wordt beschreven hoe u een nieuwe lease maakt door informatie in te voeren in Activa leasen of door gegevens uit een bestaande lease te kopiëren.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b495c9a02a872d4b360b5f7216b1db3f7d366daf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814147"
---
# <a name="add-or-copy-leases-preview"></a>Leases toevoegen of kopiëren (preview)

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een geheel nieuwe lease maakt in Activa leasen en hoe u een lease kunt maken door een bestaande lease te kopiëren. Het proces voor het maken van een nieuwe lease omvat het invoeren van gegevens voor de nieuwe lease en het maken van een leaseschema. Nadat er ten minste één lease is ingesteld, kunt u de informatie uit een bestaande lease kopiëren en vervolgens de gegevens bewerken die u nodig hebt om een nieuwe lease te maken.

## <a name="create-a-lease"></a>Een lease maken

Volg deze stappen om een lease te maken in Activa leasen.

1. Selecteer op de pagina **Leaseoverzicht** in het actievenster de optie **Nieuw**.
2. Voer gegevens over de lease in. Vereiste velden hebben een rode rand.

## <a name="create-a-lease-schedule"></a>Een leaseschema maken

Nadat u de gegevens voor de lease hebt ingevoerd, voert u de volgende stappen uit om een leaseschema te maken.

> [!NOTE]
> De financiële dimensies kunnen op basis van aangepaste financiële dimensies worden gewijzigd.

1. Selecteer **Schema's maken** om de leaseboeken te genereren. De leaseboeken omvatten de schema's voor betaling, aflossing, afschrijving en onkosten.
2. Als u de leaseboeken wilt openen en de nieuwe schema's wilt weergeven, selecteert u het tabblad **Boeken**.

    De pagina **Boekdetails** geeft aan hoe de lease wordt verwerkt in de boeken die aan de lease zijn toegewezen. Hier kunt u de leaseschema's bekijken.

    Het betalingsschema bevat de invoer uit het tabblad **Betalingsschemaregels** op de pagina **Lease toevoegen**. U kunt nog steeds alle betalingsbedragen en variabele betalingen wijzigen. De leaseverplichtingen worden berekend op basis van het aangepaste betalingsschema.

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
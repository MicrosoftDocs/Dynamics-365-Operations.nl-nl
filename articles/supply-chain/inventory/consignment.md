---
title: Consignatie
description: In dit onderwerp wordt uitgelegd hoe u gebruik maakt van de processen voor inkomende consignatievoorraad.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a6e3f0e58e14cc4d68d2249a4e3b69515f23e838
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="consignment"></a>Consignatie

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u gebruik maakt van de processen voor inkomende consignatievoorraad.

De consignatievoorraad is de voorraad die eigendom is van een leverancier, maar die op uw locatie is opgeslagen. Wanneer u klaar bent om de voorraad te verbruiken of te gebruiken, neemt u het eigendom van de voorraad over. Dit onderwerp bevat informatie over het fysiek ontvangen van voorhanden voorraad in eigendom van de leverancier zonder grootboektransacties te maken, over het starten van een productieproces waarin de voorraad in eigendom van de leverancier fysiek kan worden gereserveerd. en over het wijzigen van het eigendom van de grondstoffen om het verbruik als onderdeel van de verwerking van productieorders te kunnen verwerken. U vindt ook informatie over hoe leveranciers het verbruik van hun voorraad kunnen volgen door middel van de interface van de leverancierssamenwerking. Informatie over het inschakelen en configureren van inkomende consignatieprocessen vindt u in [Consignatie instellen](set-up-consignment.md).

## <a name="overview-of-the-consignment-process"></a>Overzicht van het consignatieproces
In dit voorbeeldscenario heeft het bedrijf USMF een consignatieovereenkomst met leverancier US-104 voor de grondstof M9211CI.

1.  Een consignatieaanvullingsorder wordt handmatig aangemaakt door iemand in USMF, op basis van de verwachte vraag. De order wordt gemaakt voor leverancier US-104 en een regel wordt toegevoegd voor artikel MS9211CI.
2.  De leverancier wordt geïnformeerd over de verwachte levering. Dit kan op een van drie manieren gebeuren:
    -   Iemand bij USMF verzendt de orderinformatie naar de leverancier.
    -   De leverancier kan ook de verwachte voorhanden voorraad op de klantlocatie bewaken via de interface voor leverancierssamenwerking.
    -   Iemand bij USMF filtert de gegevens op de pagina **Voorhanden voorraad**, zodat alleen de records voor leverancier US-104 worden weergegeven die de ontvangststatus **Besteld** hebben en verzendt deze informatie naar de leverancier.

3.  De voorraad wordt geleverd van US-104 naar USMF.
4.  Wanneer het materiaal bij USMF aankomt, wordt de consignatieaanvullingsorder bijgewerkt met een productontvangstbon. Alleen de fysieke hoeveelheid van de voorraad in eigendom van de leverancier wordt geregistreerd. Er worden geen grootboektransacties gemaakt, omdat de voorraad nog eigendom van de leverancier is.
5.  De leverancier volgt updates van de fysiek voorhanden voorraad door middel van de pagina **Voorhanden consignatievoorraad**.
6.  Nu de fysieke voorraad voorhanden is, reserveert het productieproces de voorraad in eigendom van de leverancier en begint met de productieorder voor de afgewerkte goederen waarvoor de grondstof M9211CI wordt verbruikt.
7.  De eigenaar van de gereserveerde grondstoffen die in de productie van vandaag worden verbruikt, wordt gewijzigd van US-104 naar USMF. Dit wordt gedaan door middel van een journaal voor wijzigingen aan voorraadeigendom. Dit proces maakt inkooporders waarin het veld **Oorsprong** is ingesteld op **Consignatie**.
8.  De leverancier volgt het verbruik (overgang van eigendom) op de pagina **Producten ontvangen uit consignatievoorraad** en geeft een factuur uit op basis van de overeenkomst tussen de twee bedrijven.
9.  Het productieproces verbruikt de grondstof via een productieorderverzamellijst. De fysieke reservering wordt automatisch bijgewerkt om aan te geven dat de voorhanden voorraad nu eigendom is van USMF.
10. De factuur van US-104 wordt verwerkt voor de inkooporders die automatisch zijn genereerd toen het journaal voor voorraadseigendomswijzigingen werd verwerkt. De betaling voor de verbruikte voorraad wordt uitgevoerd aan leverancier US-104.

USMF voert nog extra periodieke processen uit:

-   De fysieke verplaatsing van de voorraad in eigendom van de leverancier tussen verschillende magazijnen wordt verwerkt door middel van een overboekingsjournaal.
-   De fysieke voorhanden voorraad wordt bijgewerkt door middel van een **Artikeltellijst**. Tellen kan ook door de leverancier worden gebruikt om de voorhanden voorraad bij te werken, als hij hiervoor is gemachtigd.

Leverancier US-104 kan de updates volgen met de pagina **Voorhanden consignatievoorraad**.

## <a name="consignment-replenishment-orders"></a>Consignatieaanvullingsorders
Een consignatieaanvullingsorder is een document dat wordt gebruikt om voorraadhoeveelheden op te vragen en te volgen van producten die een leverancier binnen een bepaald datumbereik wil leveren door transacties voor bestelde voorraad te maken. Doorgaans is dit gebaseerd op de geprognosticeerde en werkelijke vraag van de specifieke producten. De voorraad die wordt ontvangen voor de consignatieaanvullingsorder blijft eigendom van de leverancier. Alleen het eigendom van de producten die gerelateerd zijn aan de fysieke ontvangstupdate wordt geregistreerd, en daardoor komen geen updatetransacties in het grootboek voor. De dimensie **Eigenaar** wordt gebruikt om informatie scheiden voor de voorraad die eigendom is van de leverancier en voorraad die eigendom is van de ontvangende rechtspersoon. Consignatieaanvullingsorderregels hebben de status **Openstaande order** zolang de volledige hoeveelheid van de regels niet is ontvangen of geannuleerd. Wanneer de volledige hoeveelheid is ontvangen of geannuleerd, wordt de status gewijzigd in **Voltooid**. De fysieke voorhanden voorraad die is gekoppeld aan een consignatieaanvullingsorder kan worden geregistreerd met een registratieproces of met een updateproces voor een productontvangstbon. De registratie kan worden uitgevoerd als onderdeel van het artikelontvangstproces of door de orderregels handmatig bij te werken. Wanneer het updateproces voor productontvangstbonnen wordt gebruikt, wordt een record gemaakt in het productontvangstbonjournaal waarmee de ontvangst van goederen bij de leveranciers kan worden bevestigd.

[![consignatieaanvullingsorder](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Journaal voor wijzigingen aan voorraadeigendom
Het proces voor het wijzigen van het eigendom van de voorraad van de leverancier naar de ontvangende rechtspersoon wordt uitgevoerd met een Journaal voor wijzigingen aan voorraadeigendom. Er worden geen verwachte voorraadtransacties gegenereerd voor het journaal. De enige voorraadtransacties die worden gemaakt, zijn degene die samenhangen met een geboekt journaal. Wanneer het journaal wordt geboekt:

-   De voorraad in eigendom van de leverancier wordt uitgegeven met een verwijzing **Wijziging aan eigendom** met de status **Verkocht**.
-   Voorhanden voorraad wordt ontvangen door de rechtspersoon die het gebruikt, door middel van een voorraadtransactie van het type 'productontvangsbon bijgewerkt' op de inkooporder Dit stelt de status van de order in op **Ontvangen**. Voor inkooporders voor consignatie wordt het veld **Oorsprong** ingesteld op **Consignatie**.

Het is niet mogelijk om de hoeveelheden voor consignatieinkooporderregels bij te werken nadat de order is gemaakt.

[![journaal-wijziging-voorraadeigendom](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Leverancierssamenwerking in consignatieprocessen
De interface van de leverancierssamenwerking heeft drie pagina's die gerelateerd zijn aan het proces voor inkomende consignaties:

-   **Inkooporders** **die consignatievoorraad verbruiken**: toont gedetailleerde inkooporderinformatie die verband houdt met de eigendomswijziging uit het consignatieproces.
-   **Producten ontvangen uit consignatievoorraad**: toont informatie over de artikelen en hoeveelheden waarvoor productontvangstbonnen zijn bijgewerkt tijdens het proces van de eigendomwijziging.
-   **Voorhanden consignatievoorraad**: toont informatie over de consignatieartikelen waarvan de levering wordt verwacht en de artikelen die al fysiek beschikbaar zijn op de klantlocatie.

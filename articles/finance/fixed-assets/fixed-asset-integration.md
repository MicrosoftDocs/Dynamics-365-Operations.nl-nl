---
title: Integratie vaste activa
description: Vaste activa kunnen worden gebruikt in Grootboek, Voorraadbeheer, Klanten en Leveranciers. U kunt vaste activa ook integreren met inkooporders.
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba1fad55082abaaeaf1874698d7475597f23904f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240909"
---
# <a name="fixed-assets-integration"></a>Integratie vaste activa

[!include [banner](../includes/banner.md)]

Vaste activa kunnen worden gebruikt in Grootboek, Voorraadbeheer, Klanten en Leveranciers. U kunt vaste activa ook integreren met inkooporders.

<a name="general-ledger"></a>Grootboek
--------------

In de module Grootboek wordt de waarde van alle vaste activa doorgaans samengevat op meerdere hoofdrekeningen die nodig zijn voor de financiële rapportage. Op de pagina **Vaste activa** kunt u echter veel records van vaste activa maken. Deze records kunnen gegevens bevatten zoals de aanschafprijs, afschrijving en waardering. Telkens wanneer u een transactie voor vaste activa boekt, worden de betreffende hoofdrekeningen bijgewerkt. Op de hoofdrekeningen voor vaste activa staat altijd de bijgewerkte waarde van de vaste activa.

Op de pagina **Boekingsprofielen voor vaste activa** definieert u de hoofdrekeningen waar transacties van het vaste-activaboek worden geboekt. U kunt ook de soorten transacties voor vaste activa opgeven die op elke hoofdrekening worden geboekt. U kunt diverse combinaties van hoofdrekeningen maken vaste activa, afhankelijk van het gewenste detailniveau dat u voor de vaste activa in het grootboek wilt. Hoofdrekeningen kunnen worden gebaseerd op transactietypes, boeken en andere hoofdrekeningen.

## <a name="inventory-management"></a>Voorraadbeheer
In het voorraadjournaal voor vaste activa, kunt u de verwerving invoeren van vaste activa door de rechtspersoon geproduceerd of voor zichzelf gebouwd. U kunt voorraadartikelen vervolgens overbrengen naar vaste activa als een overname of als onderdeel van een overname. 

Ook kunt u met behulp van inkooporders activa aanschaffen. Wanneer inkooporders voorraadartikelen bevatten die als vaste activa zijn ingesteld, bepaalt de instelling van de optie **Bijboekingen van activa vanuit Inkoop toestaan** op de pagina **Parameters vaste activa** of een verwerving wordt geboekt voor het vaste activum wanneer de factuur wordt geboekt. Eén inkoopregel maakt slechts één vast activum, ongeacht de hoeveelheid. De gevolgen van de verwerving van vaste activa op voorraad is afhankelijk van de instellingen van de rechtspersoon. 

Wanneer een voorraadartikel via het voorraadjournaal of via een inkooporder een verwerving vaste activa wordt, wordt er een inkooporder, verwervingsvoorstel of verwervingstransactie van het vaste-activaboek gemaakt. Als een boekverwerving een afgeleid boek bevat, wordt ook een verwervingstransactie voor het afgeleide boek gemaakt. 

De afname van de voorraad door het boeken van de verwerving wordt gecontroleerd door de boekingsregels die zijn ingesteld op de pagina **Boeking** in Voorraadbeheer. De voorraad wordt echter niet altijd kleiner wanneer u facturen voor vaste activa boekt. In sommige gevallen kunnen de vaste activa worden gekocht voor intern gebruik. Een voorbeeld is een laptop die voor de verkoopafdeling wordt gekocht. Wanneer u met inkooporders werkt, kunt u artikelen gebruiken die voor zowel de verkoop als voor intern gebruik zijn ingesteld. 

Als u bepaalde ontvangst- en uitgifterekeningen voor vaste activa in artikelengroepen gebruikt, kunt u hetzelfde voorraadartikel voor zowel interne inkopen als voor voorraadverkopen gebruiken. 

Vaste activa die voor intern gebruik zijn, zijn zo ingesteld dat ze een rekeningtype **Ontvangst van vaste activa** hebben. Dit rekeningtype wordt gebruikt voor het bijhouden van de ontvangst van het vaste activum. Wanneer u een leveranciersfactuur boekt, gebruikt u de ontvangstrekening voor vaste activa als aan een van de volgende voorwaarden wordt voldaan:

-   De factuurregel bevat een bestaand vast activum voor interne doeleinden.
-   Het selectievakje **Nieuwe vaste activa?** is ingeschakeld voor de productontvangstregel die is geboekt.
-   Het selectievakje **Nieuwe vaste activa maken** wordt ingeschakeld voor de leveranciersfactuurregel.

Deze rekening is doorgaans een onkostenrekening. U kunt het rekeningtype **Ontvangst van vaste activa** instellen voor een artikelengroep of een afzonderlijk artikel met behulp van het tabblad **Inkooporder** op de pagina **Artikelgroep** of **Boeking**.

Vaste activa die voor intern gebruik zijn, kunnen eveneens zo worden ingesteld dat ze een rekeningtype **Uitgifterekeningen voor vaste activa** hebben. Dit rekeningtype wordt gebruikt voor het bijhouden van de uitgifte van het vaste activum aan de ontvanger. Wanneer een activum wordt verworden door een inkooporder, fungeert de uitgifterekening voor vaste activa als de tegenrekening voor de debetrekening vaste activa. De verwerving van de activa kan worden geboekt wanneer u een leveranciersfactuur boekt of wanneer u de verwerving van de activa boekt in het vaste-activajournaal, mogelijk via een verwervingsvoorstel. U kunt het rekeningtype **Uitgifte van vaste activa** instellen voor een artikelengroep of een afzonderlijk artikel met behulp van het tabblad **Vooraad** op de pagina **Artikelgroep** of **Artikelboeking**. 

De hoofdrekeningen die worden gebruikt voor het boeken worden uiteindelijk bepaald door de opties die zijn opgegeven voor de grootboekintegratie voor de artikelmodelgroep. Bovendien hangen de gebruikte hoofdrekeningen af van het feit of een activum wordt toegewezen aan de inkooporderregel. De rekeningen worden afgeleid van het boekingsprofiel voor elke artikelengroep. 
**Opmerking:** als er voorraad is gereserveerd wanneer productontvangstbonnen worden geboekt, kunt u geen vast activum toewijzen of een vast activum voor de regel maken. 

De rekeningen waarnaar de vaste-activatransacties worden geboekt, zijn afhankelijk van twee factoren: of de activa zijn aangeschaft of door de rechtspersoon zijn gebouwd en ook van het type transactie van de activa. 

Het transactietype verbindt de voorraadtransactie met het boekingsprofiel in Vaste activa. Omdat door het boekingsprofiel in Vaste activa wordt bepaald welke rekeningen er worden bijgewerkt, is de keuze van een transactietype voor vaste activa indirect ook een keuze van de hoofdrekeningen waarnaar de transactie wordt geboekt. Voor zowel vervaardigde als aangeschafte vaste activa is het transactietype doorgaans **Verwerving** of **Verwervingscorrectie**.

## <a name="accounts-receivable"></a>Klanten  
De integratie van vaste activa met klanten gebruikt boekingsprofielen die zijn ingesteld in vaste activa. Deze Boekingsprofielen worden geactiveerd wanneer een vast activum, een boek en het VA-transactietype zijn geselecteerd voor een factuur van de klant voordat de factuur van de klant is geboekt. Omdat vaste activa geen onderdeel van Voorraadbeheer zijn, moet u bij de verkoop van vaste activa de pagina **Vrije-tekstfactuur** gebruiken. 

Als het boek een afgeleid boek bevat, wordt er een boekingstransactie voor het afgeleide boek gemaakt wanneer u de klantfactuur boekt.

## <a name="accounts-payable"></a>Leveranciers    
Vaste activa worden doorgaans aangeschaft bij externe leveranciers. Met de pagina **Parameters vaste activa** kunt u opgeven of bijboekingen van vaste activa altijd worden geboekt wanneer u leveranciersfacturen boekt of dat bijboekingen van vaste activa alleen vanuit Vaste activa kunnen worden geboekt. Als u het boeken van verwervingen van activa vanuit Leveranciers inschakelt, worden de vaste-activarekeningen bijgewerkt wanneer een leverancierfactuur voor een verwerving van vaste activa wordt geboekt. 

Als u een verwerving van vaste activa mag boeken wanneer er een factuur wordt geboekt, wordt de transactie geboekt volgens de boekingsprofielen in Vaste activa voor de diverse typen vaste-activatransacties. Het boeken wordt gecontroleerd door de vaste activa, het boek en het type vaste-activatransactie die op de pagina **Inkooporder** worden geselecteerd voordat de leverancierfactuur wordt geboekt. 

Als het boek een afgeleid boek bevat, wordt er een boekingstransactie voor het afgeleide boek gemaakt wanneer u de leverancersfactuur boekt.

De integratie wordt voor elke orderregel geactiveerd op het tabblad **Vaste activa** op het sneltabblad **Regeldetails** op de pagina **Inkooporder**. U kunt een inkooporder voor een vast activum verzenden naar de leverancier. Echter, vaste activa en hoofdrekeningen worden alleen bijgewerkt wanneer u de leveranciersfactuur boekt na ontvangst van het vaste activum. Aangezien inkooporders alleen voorraadartikelen kunnen bevatten, hangt de invloed van de verwerving van vaste activa op voorraad af van de instelling van de rechtspersoon.

## <a name="project-management-and-accounting"></a>Projectbeheer en boekhouding
U kunt een project koppelen aan een activum dat door het project wordt beïnvloed. Ook kunt u elke fase, elke taak of elk subproject aan een ander activum koppelen. Een activum kan worden gekoppeld aan een record van elk project. U brengt de koppeling tot stand wanneer u het nummer van het vaste activum invoert in het veld **Vaste-activanummer** op de pagina **Projecten**. Het projecttype moet **Intern** zijn of **Kostenproject**. 

Ook kunt u met de pagina **Projecten** details bekijken over activa die aan projecten zijn gekoppeld. U geeft de record voor vaste activa weer door te klikken op de koppeling van het activum op het sneltabblad **Instellingen** en zo de pagina **Vaste activa** te openen. Klik vervolgens op **Projecten** &gt; **Alle projecten** om de projecten weer te geven die aan het vaste activum zijn gekoppeld. 

U koppelt vaste activa gewoonlijk met projecten wanneer de projecten zijn gerelateerd aan het werk, onderhoud of verbeteringen voor het activum. Wanneer het project is voltooid, wordt een opwaarderingscorrectie voor het activum niet automatisch gemaakt. Daarom moet u de opwaarderingscorrectie handmatig maken als dit nodig is. 

U verwijdert de koppeling tussen een project en een activum door het veld **Vaste-activanummer** op de pagina **Projecten** leeg te maken. 

U kunt ook een vast activum aangeven dat u als onderdeel van een ramingsproject maakt. Aan het eind van het ramingsproject kunt u automatisch een bijboekingstransactie voor een activum boeken.

Zie voor meer informatie [Verwerving van activa via inkoop](acquire-assets-procurement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
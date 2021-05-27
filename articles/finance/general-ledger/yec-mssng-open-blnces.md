---
title: Ontbrekende openingssaldi in jaarafsluiting
description: In dit onderwerp wordt uitgelegd waarom openingssaldi kunnen ontbreken wanneer u een jaar afsluit en hoe u deze saldi opnieuw kunt opbouwen als ze ontbreken.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028557"
---
# <a name="year-end-close-missing-opening-balances"></a>Ontbrekende openingssaldi in jaarafsluiting

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd waarom openingssaldi kunnen ontbreken wanneer u een jaar afsluit en hoe u deze saldi opnieuw kunt opbouwen als ze ontbreken.

### <a name="symptom"></a>Symptoom

Waarom zijn er geen beginsaldi na het uitvoeren van de jaarafsluiting van het grootboek? 

### <a name="resolution"></a>Oplossing

Controleer het volgende als u een jaar in het grootboek hebt afgesloten en vervolgens een proefbalans hebt gegenereerd waarin geen openingssaldi voor het volgende boekjaar worden weergegeven.

Als het veld **Vorige afsluiting ongedaan maken** is ingesteld op **Ja**, wordt de vorige jaarafsluiting voor hetzelfde boekjaar ongedaan gemaakt. Wanneer u een proces uitvoert om de jaarafsluiting ongedaan te maken, worden alle boekingen voor eind- en openingssaldi verwijderd, alsof het jaar nooit is afgesloten. De boekstukken worden ook verwijderd. Het jaarafsluitingsproces wordt niet automatisch opnieuw uitgevoerd. U moet het proces opnieuw starten en deze keer de optie **Vorige afsluiting ongedaan maken** bijwerken naar **Nee**.

Dit scenario wordt behandeld in het onderwerp over jaarafsluiting in de veelgestelde vragen. Zie [Veelgestelde vragen over jaarafsluitingsactiviteiten](faq-year-end-activities.md) voor meer informatie.

### <a name="symptom"></a>Symptoom

Ik heb een jaarafsluiting uitgevoerd met de optie **Vorige afsluiting ongedaan maken** ingesteld op **Nee** en ik heb nog steeds geen openingssaldi voor mijn boekjaar.

### <a name="resolution"></a>Oplossing

Controleer eerst de status van de batchtaak. Het afsluiten van een jaar omvat een aantal afzonderlijke taken, maar de belangrijkste stap is de batchtaak met de taakbeschrijving **Stap 5.0.0**. Het boeken van de openingstransacties, en eventueel de afsluittransacties, naar het grootboek vindt plaats tijdens deze stap. 

[![Lijst batchhistorie](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Als deze stap is beëindigd, maar u geen openingssaldi ziet op de querypagina **Proefbalans** (**Grootboek > Query's en rapporten > Proefbalans**), bekijkt u de resultaten van de batchtaak voor de jaarafsluiting om te zien of de stap voor het opnieuw opbouwen van saldi is voltooid.

[![Resultaten van batchtaak voor jaarafsluiting](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Als deze stap om welke reden dan ook mislukt, zijn de openingstransacties en eventuele afsluittransacties waarschijnlijk geboekt. U kunt via de querypagina **Boekstuktransacties** controleren of de grootboektransacties zijn geboekt door het boekstuknummer en de datum op te geven die in het dialoogvenster voor de jaarafsluiting zijn opgegeven voor het jaar dat u hebt afgesloten (**Grootboek > Query's en rapporten > Boekstuktransacties**).

[![Query Boekstuktransacties](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Als de openingsboektukken, en eventueel de afsluitingsboekstukken, aanwezig zijn, hoeft u de jaarafsluiting niet opnieuw uit te voeren. Zie in plaats daarvan de volgende sectie voor informatie over hoe u verder kunt gaan.

### <a name="symptom"></a>Symptoom

Moet ik het hele proces voor de jaarafsluiting opnieuw uitvoeren als de stap voor het opnieuw opbouwen van saldi in de jaarafsluiting is mislukt?

### <a name="resolution"></a>Oplossing

Met de stap voor het opnieuw opbouwen van saldi worden de grootboeksaldi bijgewerkt die worden gebruikt wanneer de query Proefbalans wordt gegenereerd.  Dit is de laatste stap in het jaarafsluitingsproces.  Als dit de enige stap is die mislukt, zijn de grootboektransacties geboekt.  In dat geval hoeft u de jaarafsluiting niet opnieuw uit te voeren. U kunt het proces voor het handmatig opnieuw opbouwen van de saldi uitvoeren via de pagina **Financiële dimensiesets** (**Grootboek > Rekeningschema > Dimensies > Financiële dimensiesets**).

[![De knop Saldi opnieuw opbouwen op de pagina Financiële dimensiesets](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Als de verwerking van deze stap lang duurt, raden we u aan de aanbevolen procedures voor financiële dimensiesets te bekijken die worden beschreven in [Aanbevolen procedures voor het bijwerken van financiële dimensiesets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 


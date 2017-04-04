---
title: Toename van de project-kosten op ontvangstbewijzen voor aankopen
description: Dit onderwerp wordt beschreven hoe Transitorische projectkosten van inkoop ontvangsten in Microsoft Dynamics 365 voor bewerkingen kunnen worden getraceerd.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Toename van de project-kosten op ontvangstbewijzen voor aankopen

Dit onderwerp wordt beschreven hoe Transitorische projectkosten van inkoop ontvangsten in Microsoft Dynamics 365 voor bewerkingen kunnen worden getraceerd. 

Facturen voor een project vaak binnenkomen later dan de goederen en diensten worden geleverd, die mogelijk een aanzienlijke gevolgen hebben voor project prestatie-indicatoren (KPI's). Het belangrijk dat u deze transacties zowel financiële bijhouden en project rapporten.

Het volgende voorbeeldscenario illustreert dit. 

Raadpleging van Contoso is een nieuw cloud deployment project gestart. Een inkooporder is gemaakt om te kopen van een computer voor het project. De computer wordt $1500 kosten en de installatie wordt $150. De leverancier heeft geleverd en de computer geïnstalleerd, maar de factuur is nog niet is bereikt Contoso raadpleging. De projectmanager wilt toename van de project-kosten van $1650 zien voordat de factuur wordt geleverd. Deze kosten moet ook doorgevoerd in het bedrijf maand einde financiële overzichten. 

De transitorische kosten moet worden vastgelegd op de financiële niveau en de projectniveau voor rapportagedoeleinden. In Dynamics 365 voor bewerkingen, kan de financiële bijwerking van de productontvangstbon voor het artikel en aanschaffingscategorieën categorieën worden bijgehouden. 

Voor artikelen op de **leverancierparameters** pagina, selecteer de **productontvangstbonnen in grootboek boeken** optie.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Voor aanschaffingscategorieën, op de **categoriebeleidsregel** pagina **inkoop** beleid en selecteer vervolgens **transitorische opdracht kosten bij ontvangst** voor elke aanschaffingscategorie.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

De **niet-gefactureerde inkoopuitgave** en **inkooptoerekening** in de rekeningen **boekingsinstellingen** wordt gebruikt bij het boeken van boekstukken die betrekking hebben op de productontvangstbon.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Met dit hetzelfde scenario, kijken welke boeken van een productontvangstbon gevolgen hebben voor het grootboek en projectgegevens. 

**Stap 1:** maken en een nieuwe inkooporder voor het project voor het vastleggen van de aankoop van een computer voor diensten voor $150 $1500 en installatie bevestigen.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Wanneer de inkooporder wordt bevestigd, worden transacties voor de toegezegde kosten gemaakt voor het project. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> De transacties voor de toegezegde kosten heeft de **de oorsprong van transactie** veld ingesteld op **inkooporder**. Maakt en bevestigt een inkooporder maakt geen transacties voor een project. 

**Stap 2:** verzonden goederen en diensten en een productontvangstbon is geregistreerd. 

Boeken van een productontvangstbon genereren en een boekstuk naar het grootboek boekt. Het boekstuk de inkoopuitgave, niet-gefactureerde rekening te debiteren en toerekening van inkoop bijgeschreven. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Een productontvangstbon boeken gebruikt de boekingsinstellingen voor aanschaffingscategorieën en producten en niet de boekingsinstellingen voor de projectcategorieën. Deze instelling moet worden afgestemd om correct weerspiegelen financiële invloed van transitorische posten voor inkoop. 

Het is mogelijk aanschaffingscategorieën naar projectcategorieën toewijzen op de **aanschaffingscategorie** pagina.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Stap 3:** een leveranciersfactuur concept maken. 

In Dynamics 365 voor bewerkingen, heeft een productontvangstbon boeken geen invloed op projectgegevens. Als een oplossing kan u een leveranciersfactuur concept direct na het boeken van de inkoopontvangst genereren. Ga naar de **inkooporder** pagina &gt;**tabblad factuur**&gt;**genereren**&gt;**factuur**. Hiermee maakt u een factuur in behandeling-document waarmee projectgegevens worden bijgewerkt. 

Maken van een leveranciersfactuur concept genereert projecttransacties in behandeling. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

In de **toegezegde kosten** pagina gemaakt in stap 1 records zal worden gesloten en nieuwe records worden gemaakt zodat kosten toezegging die afkomstig zijn van de leveranciersfactuur in behandeling. De **de oorsprong van transactie** veld voor de toegezegde kosten worden ingesteld op **leveranciersfactuur**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

De leveranciersfactuur blijft in behandeling totdat de werkelijke leveranciersfactuur binnenkomt.



---
title: Toerekening van inkoopontvangsten aan projectkosten
description: In dit artikel wordt beschreven hoe toegerekende projectkosten van inkoopontvangsten in Microsoft Dynamics 365 Finance kunnen worden getraceerd.
author: mukumarm
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: twheeloc
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: mukumarm
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 56b8b5a6f91c6a18b53739b1e9369bda64131a06
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715851"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Toerekening van inkoopontvangsten aan projectkosten

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe toegerekende projectkosten van inkoopontvangsten in Microsoft Dynamics 365 Finance kunnen worden getraceerd. 

Facturen voor een project komen vaak later aan dan de geleverde goederen en diensten, wat een aanzienlijke impact kan hebben op prestatie-indicatoren (KPI's) voor projecten. Het is belangrijk dat deze transacties zowel in financiële als ook in projectrapporten kunnen worden gevolgd.

Dit wordt geïllustreerd in het volgende voorbeeldscenario. 

Contoso Consulting is gestart met een nieuw project voor cloudimplementatie. Een inkooporder wordt gemaakt een computer aan te schaffen voor het project. De computer kost EUR 1500 en de installatie kost EUR 150. De leverancier heeft de computer geleverd en geïnstalleerd, maar de factuur is nog niet aangekomen bij Contoso Consulting. De projectmanager wilt de project-kosten van EUR 1650 laten toerekenen voordat de factuur aankomt. Deze kosten moet ook worden doorgevoerd in de financiële overzichten voor het maandeinde van het bedrijf. 

Voor rapportagedoeleinden moeten de toegerekende kosten worden vastgelegd op zowel het financiële niveau als ook het projectniveau. De financiële update van de productontvangstbon voor het artikel en inkoopcategorieën kan worden bijgehouden. 

Voor artikelen op de pagina **Parameters van leveranciers** selecteert u de optie **Productontvangstbonnen in grootboek boeken**.
[![De pagina Parameters van module Leveranciers.](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Voor aanschaffingscategorieën selecteert u op de pagina **Categoriebeleidsregel** de optie **Inkoopbeleid** en vervolgens **Inkoopkosten samenvoegen voor ontvangst** voor elke aanschaffingscategorie.
[![De pagina Categoriebeleidsregel.](./media/accruals2-1024x569.png)](./media/accruals2.png) 

De rekeningen **Inkoopuitgave, niet-gefactureerd** en **Inkoop, toerekening** in **Boekingsinstellingen** worden gebruikt bij het boeken van boekstukken die betrekking hebben op de productontvangstbon.

Laten we met hetzelfde scenario eens kijken welke invloed het boeken van een productontvangstbon heeft voor het grootboek en projectgegevens. 

**Stap 1:** Maak en bevestig een nieuwe inkooporder voor het project, waarmee de aankoop van een computer voor EUR 1500 en installatiediensten voor $150 worden geregistreerd.
[![Nieuwe inkooporder maken.](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Wanneer de inkooporder wordt bevestigd, worden transacties voor de toegezegde kosten gemaakt voor het project. 
[![Gemaakte transacties.](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> In de transacties voor de toegezegde kosten is het veld **Transactieoorsprong** ingesteld op **Inkooporder**. Als u een inkooporder maakt en bevestigt, worden hiermee geen transacties voor een project aangemaakt. 

**Stap 2:** Goederen en diensten worden geleverd en een productontvangstbon wordt geregistreerd. 

Als u een productontvangstbon boekt, wordt hiermee een boekstuk gegenereerd en in het grootboek geboekt. Het boekstuk debiteert de inkoopuitgave, de niet-gefactureerde rekening, en crediteert de rekening voor inkooptoerekening. 
[![Boekstuktransacties.](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Als u een productontvangstbon boekt, worden de boekingsinstellingen voor aanschaffingscategorieën en -producten gebruikt, niet de boekingsinstellingen voor de projectcategorieën. Deze instelling moet worden afgestemd om correct de financiële invloed van inkooptoerekeningen weer te geven. 

U kunt aanschaffingscategorieën toewijzen aan projectcategorieën op de pagina **Aanschaffingscategorie**.
[![De pagina Aanschaffingscategorie.](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Stap 3:** Maak een conceptleveranciersfactuur 

Het boeken van een productontvangstbon heeft geen invloed op projectgegevens. Als workaround kunt u een conceptleveranciersfactuur genereren meteen nadat u de inkoopontvangst hebt geboekt. Ga naar de pagina **Inkooporder** &gt; **tabblad Factuur** &gt; **Genereren** &gt; **Factuur**. Hiermee maakt u een in behandeling zijnd factuurdocument waarmee projectgegevens worden bijgewerkt. 

Als u een conceptleveranciersfactuur aanmaakt, genereert u hiermee in behandeling zijnde projecttransacties. 
[![Projecttransacties in behandeling.](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Op de pagina **Toegezegde kosten** worden records die u in stap 1 hebt gemaakt, gesloten en nieuwe records worden gemaakt om kostentoezeggingen uit de in behandeling zijnde leveranciersfactuur weer te geven. Het veld **Oorsprong van transactie** voor de toegezegde kosten wordt ingesteld op **Leveranciersfactuur**.
[![De pagina Toegezegde kosten.](./media/accruals9-1024x200.png)](./media/accruals9.png)

De leveranciersfactuur blijft in behandeling, totdat de werkelijke leveranciersfactuur wordt ontvangen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

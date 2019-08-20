---
title: Toevoegen van projectkosten op inkoopontvangsten
description: In dit onderwerp wordt beschreven hoe toegerekende projectkosten van inkoopontvangsten in Microsoft Dynamics 365 for Finance and Operations kunnen worden getraceerd.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c1397107c179da56e8dcf4b556140dc06d8f14d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834580"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Toevoegen van projectkosten op inkoopontvangsten

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe toegerekende projectkosten van inkoopontvangsten in Microsoft Dynamics 365 for Finance and Operations kunnen worden getraceerd. 

Facturen voor een project komen vaak later aan dan de geleverde goederen en diensten, wat een aanzienlijke impact kan hebben op prestatie-indicatoren (KPI's) voor projecten. Het is belangrijk dat deze transacties zowel in financiële als ook in projectrapporten kunnen worden gevolgd.

Dit wordt geïllustreerd in het volgende voorbeeldscenario. 

Contoso Consulting is gestart met een nieuw project voor cloudimplementatie. Een inkooporder wordt gemaakt een computer aan te schaffen voor het project. De computer kost EUR 1500 en de installatie kost EUR 150. De leverancier heeft de computer geleverd en geïnstalleerd, maar de factuur is nog niet aangekomen bij Contoso Consulting. De projectmanager wilt de project-kosten van EUR 1650 laten toerekenen voordat de factuur aankomt. Deze kosten moet ook worden doorgevoerd in de financiële overzichten voor het maandeinde van het bedrijf. 

Voor rapportagedoeleinden moeten de toegerekende kosten worden vastgelegd op zowel het financiële niveau als ook het projectniveau. In Finance and Operations kan de financiële update van de productontvangstbon voor het artikel en inkoopcategorieën worden bijgehouden. 

Voor artikelen op de pagina **Parameters van leveranciers** selecteert u de optie **Productontvangstbonnen in grootboek boeken**.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Voor aanschaffingscategorieën selecteert u op de pagina **Categoriebeleidsregel** de optie **Inkoopbeleid** en vervolgens **Inkoopkosten samenvoegen voor ontvangst** voor elke aanschaffingscategorie.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

De rekeningen **Inkoopuitgave, niet-gefactureerd** en **Inkoop, toerekening** in **Boekingsinstellingen** worden gebruikt bij het boeken van boekstukken die betrekking hebben op de productontvangstbon.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Laten we met hetzelfde scenario eens kijken welke invloed het boeken van een productontvangstbon heeft voor het grootboek en projectgegevens. 

**Stap 1:** Maak en bevestig een nieuwe inkooporder voor het project, waarmee de aankoop van een computer voor EUR 1500 en installatiediensten voor $150 worden geregistreerd.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Wanneer de inkooporder wordt bevestigd, worden transacties voor de toegezegde kosten gemaakt voor het project. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> In de transacties voor de toegezegde kosten is het veld **Transactieoorsprong** ingesteld op **Inkooporder**. Als u een inkooporder maakt en bevestigt, worden hiermee geen transacties voor een project aangemaakt. 

**Stap 2:** Goederen en diensten worden geleverd en een productontvangstbon wordt geregistreerd. 

Als u een productontvangstbon boekt, wordt hiermee een boekstuk gegenereerd en in het grootboek geboekt. Het boekstuk debiteert de inkoopuitgave, de niet-gefactureerde rekening, en crediteert de rekening voor inkooptoerekening. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Als u een productontvangstbon boekt, worden de boekingsinstellingen voor aanschaffingscategorieën en -producten gebruikt, niet de boekingsinstellingen voor de projectcategorieën. Deze instelling moet worden afgestemd om correct de financiële invloed van inkooptoerekeningen weer te geven. 

U kunt aanschaffingscategorieën toewijzen aan projectcategorieën op de pagina **Aanschaffingscategorie**.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Stap 3:** Maak een conceptleveranciersfactuur 

In Finance and Operations heeft het boeken van een productontvangstbon geen invloed op projectgegevens. Als workaround kunt u een conceptleveranciersfactuur genereren meteen nadat u de inkoopontvangst hebt geboekt. Ga naar de pagina **Inkooporder** &gt; **tabblad Factuur** &gt; **Genereren** &gt; **Factuur**. Hiermee maakt u een in behandeling zijnd factuurdocument waarmee projectgegevens worden bijgewerkt. 

Als u een conceptleveranciersfactuur aanmaakt, genereert u hiermee in behandeling zijnde projecttransacties. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Op de pagina **Toegezegde kosten** worden records die u in stap 1 hebt gemaakt, gesloten en nieuwe records worden gemaakt om kostentoezeggingen uit de in behandeling zijnde leveranciersfactuur weer te geven. Het veld **Oorsprong van transactie** voor de toegezegde kosten wordt ingesteld op **Leveranciersfactuur**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

De leveranciersfactuur blijft in behandeling, totdat de werkelijke leveranciersfactuur wordt ontvangen.




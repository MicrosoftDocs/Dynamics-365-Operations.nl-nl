---
title: Het boekjaar afsluiten
description: Deze procedure legt de stappen uit in het proces voor jaarafsluiting dat saldi naar een nieuw boekjaar overboekt.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b82cc7e4077a1bd50eab30f234c2f63c79e81d84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994685"
---
# <a name="close-the-fiscal-year"></a>Het boekjaar afsluiten

[!include [banner](../../includes/banner.md)]

Deze procedure legt de stappen uit in het proces voor jaarafsluiting dat saldi naar een nieuw boekjaar overboekt.


## <a name="validate-year-end-close-parameters"></a>Parameters voor de jaarafsluiting valideren
1. Ga naar **Navigatievenster > Modules > Grootboek > Grootboek instellen > Grootboekparameters**.
2. Vouw de sectie **Afsluiting fiscaal jaar** uit.
3. Selecteer Ja of Nee voor de optie **Jaareindetransacties verwijderen tijdens overboeking**.
    
    Als het boekjaar al is afgesloten en jaarafsluiting opnieuw wordt uitgevoerd, wordt deze instelling belangrijk. Als de waarde is ingesteld op Ja, wordt het boekstuk voor de vorige jaarafsluiting verwijderd en een nieuw boekstuk aangemaakt voor de beginsaldi voor alle accounts. Als de waarde is ingesteld op Nee, wordt het boekstuk behouden en wordt een nieuw boekstuk alleen gemaakt om invoeren aan te passen die na de laatste jaarafsluiting zijn geboekt.

4. Selecteer Ja of Nee voor de optie **Afsluittransacties tijdens overboeking maken**.

    Als de waarde is ingesteld op Ja, worden twee transacties gemaakt. Één boekstuk wordt gemaakt in het boekjaar dat wordt afgesloten, om de saldi van de grootboekrekeningen van W&V op nul in te stellen. Een tweede boekstuk wordt gemaakt in het volgende boekjaar voor de beginsaldi. Als de waarde is ingesteld op Nee, wordt één boekstuk gemaakt in het volgende boekjaar voor de beginsaldi.  

5. Selecteer Ja of Nee voor de optie **Status fiscaal jaar instellen op definitief afgesloten**.

    Als de waarde is ingesteld op Ja, wordt de status van het boekjaar ingesteld op Definitief gesloten.  Omdat een definitief afgesloten jaar niet kan worden heropend, zou het een best practice zijn om deze optie op Nee in te stellen.  

6. Selecteer Ja of Nee voor de optie **Boekstuknummer moet worden ingevuld tijdens de jaarafsluiting**.

    Als de waarde is ingesteld Ja, moet een boekstuknummer handmatig in het jaarafsluitingsproces worden ingevoerd. Dit boekstuknummer wordt niet gegenereerd op basis van een nummerreeks. Het is een best practice om dit op Ja in te stellen.  

7. Sluit de pagina.
8. Ga naar **Grootboek > Afgesloten periode > Jaarafsluiting**.
9. Klik op **Nieuw** om een jaarafsluitingssjabloon te maken.

    Een sjabloon kan voor een groep rechtspersonen worden gemaakt waarvoor de jaarafsluiting moet worden uitgevoerd. U kunt deze sjabloon elk jaar opnieuw gebruiken.  

10. Voer in het veld **Groepsnaam** de naam van de jaarafsluitingssjabloon in.
11. Selecteer in het veld **Fiscale kalender** het fiscaal jaar waarvoor de sjabloon wordt gemaakt.

    Alleen rechtspersonen die hetzelfde boekjaar gebruiken, kunnen samen in de jaarafsluitingssjabloon worden gegroepeerd. Dit is omdat de jaarafsluiting wordt uitgevoerd door een boekjaar te selecteren in plaats van een datum.  

12. Klik in het **Actievenster** op **Opslaan**.
13. Klik in de sectie **Rechtspersonen** op **Toevoegen** om de rechtspersonen voor deze sjabloon te selecteren.
    
    Rechtspersonen kunnen worden toegevoegd door selectie van de rechtspersonen of van een organisatiehiërarchie.  Alleen de rechtspersonen die de organisatiehiërarchie hebben met dezelfde fiscale kalender worden toegevoegd.  

14. Selecteer de rechtspersonen of de organisatiehiërarchie.
15. Klik op **OK**.
16. Selecteer Ja of Nee in **Balansdimensie overboeken**.

    Het is een best practice om deze optie voor Balansrekeningen in te stellen op Ja. Hierme worden de financiële dimensies op geboekte transacties bewaard, wanneer de beginsaldi worden gemaakt voor de balansrekeningen. Voor winst- en verliesrekeningen kunt u ervoor kiezen om de financiële dimensies te bewaren (Alles sluiten) wanneer de saldi worden verplaatst naar Ingehouden winst, of om de financiële dimensies te vervangen door een andere dimensiewaarde (Eén sluiten). Als u Eén sluiten kiest, kunt u een specifieke dimensiewaarde definiëren voor elke dimensie of een waarde zelfs leeg laten.  

17. Klik op **Opslaan**.
18. Start de jaarafsluiting door in het **Actievenster** de optie **Jaarafsluiting uitvoeren** te kiezen. De jaarafsluiting wordt voor de geselecteerde sjabloon uitgevoerd.  
19. Selecteer alle rechtspersonen in de sjabloon of een deel daarvan waarvoor de jaarafsluiting moet worden uitgevoerd.

    Wanneer de jaarafsluiting voor het eerst wordt uitgevoerd, kiezen de meeste organisaties ervoor om de jaarafsluiting voor alle rechtspersonen in de sjabloon uit te voeren, om beginsaldi te krijgen. Als daarna nog aanpassende invoeren worden gedaan, kunt u ervoor kiezen de jaarafsluiting alleen uit te voeren voor de rechtspersonen waarvoor correcties zijn aangebracht.  

20. Klik op **OK**.
21. Selecteer de fiscale kalender waarvoor u de jaarafsluiting wilt uitvoeren.
22. Typ een waarde in het veld **Boekstuk**. Het is een best practice om het boekjaar in het boekstuknummer op te nemen, om het jaareindeboekstuk vinden dat wordt gemaakt, gemakkelijker te vinden.  
23. De jaarafsluiting wordt standaard in de batchmodus uitgevoerd. Het is een best practice om processen met een lange uitvoeringstijd in batchmodus uit te voeren. Dit is meestal een dergelijk proces, en daarom wordt standaard de batchmodus geselecteerd.  
24. Klik op **OK**.


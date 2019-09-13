---
title: Onderhoudsrondes
description: In dit onderwerp wordt uitgelegd wat onderhoudsronden zijn in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a0ac4820d2efa37387382c2890e3ddc7dbc0878b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875585"
---
# <a name="maintenance-rounds"></a>Onderhoudsrondes


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


In **Activabeheer** kunt u onderhoudsronden maken voor verschillende activa. Daarop kunt u met regelmatige tussenpozen een soortgelijke taak uitvoeren. Bijvoorbeeld smeertaken of veiligheidsinspectietaken die voor een aantal machines binnen dezelfde intervallen moeten worden uitgevoerd. De eerste stap bestaat uit het maken van een onderhoudsronde, inclusief activa waarvoor eenzelfde onderhoudstaak moet worden uitgevoerd. Vervolgens plant u de onderhoudsronden. Wanneer u de planning van de onderhoudsronden hebt voltooid, kunt u alle taakrecords voor de ronden bekijken in **Hele onderhoudsschema** en **Openstaande onderhoudsschemaregels**.

>[!NOTE]
>Op het moment dat een op ronde gebaseerde werkorder wordt gemaakt, kunnen onderhoudsronden ook worden ingesteld voor functionele locaties als deze ronden moeten worden voltooid voor de activa die op de functionele locatie zijn geïnstalleerd. Zie [Functionele locaties maken](../functional-locations/create-functional-locations.md) voor meer informatie over het instellen van onderhoudsronden voor functionele locaties.

## <a name="set-up-a-maintenance-round"></a>Een onderhoudsronde instellen

1. Klik op **Activabeheer** > **Instellen** > **Preventief onderhoud** > **Onderhoudsronden**.

2. Klik op **Nieuw** om een nieuwe onderhoudsronde te maken.

3. Type een id in het veld **Onderhoudsronde** en een naam voor de onderhoudsronde in het veld **Naam**.

4. Selecteer een begindatum voor de ronde in het veld **Begindatum**.

5. In de velden **Voltooien binnen dagen** en **Voltooien binnen uren** kunt u de verwachte einddatum in dagen of uren invoegen. De verwachte einddatum wordt berekend ten opzichte van de begindatum. Deze wordt berekend wanneer de onderhoudsschemaregels worden gemaakt. Zo kunt u 7 in het veld **Voltooien binnen dagen** invoeren als u wilt aangeven dat de betreffende taak binnen een week vanaf de begindatum moet worden voltooid.

6. Selecteer Ja op de wisselknop **Automatisch maken** als werkorders automatisch moeten worden gemaakt op basis van onderhoudsschemaregels die op basis van deze onderhoudsronde zijn gemaakt.

7. Selecteer in het veld **Werkordertype** het werkordertype dat moet worden gebruikt voor werkorders die zijn gemaakt op basis van deze onderhoudsronde.

8. Selecteer in het veld **Serviceniveau** het serviceniveau voor de werkorder dat moet worden gebruikt voor werkorders die zijn gemaakt op basis van deze onderhoudsronde.

9. Klik op het sneltabblad **Activaregels** op **Toevoegen** om een activum aan de onderhoudsronde toe te voegen.

10. In het veld **Regelnummer** wordt automatisch een regelnummer ingevoegd om de volgorde van de activa in de onderhoudsronde aan te geven.

11. Selecteer het activum in het veld **Activum**.

12. Selecteer het type onderhoudstaak voor het activum in het veld **Type onderhoudstaak**.

13. Selecteer zo nodig **Variant van type onderhoudstaak** en **Handel** voor het type onderhoudstaak.

14. Selecteer het terugkeerpatroon (dag, week enzovoort) in het veld **Periodetype**.

15. Voer in het veld **Periodefrequentie** het aantal herhalingen voor de onderhoudsronde in. Voorbeeld: als u in het veld **Periodetype** de optie Dag hebt geselecteerd en u het getal 7 in dit veld opgeeft, worden er eenmaal per week nieuwe onderhoudsronderegels gemaakt tijdens de planning van preventief onderhoud.

16. Selecteer in het veld **Begindatum** een begindatum voor het activum dat u wilt opnemen in de onderhoudsronde. Deze datum kan verschillen van de begindatum die is ingesteld in de onderhoudsronde.

17. Herhaal stap 9 tot en met 16 als u meer activa aan de onderhoudsronde wilt toevoegen.

18. Klik op het sneltabblad **Regels voor functionele locatie** op **Toevoegen** om een functionele locatie aan de onderhoudsronde toe te voegen. Zie de beschrijving van de betreffende velden hierboven. Dezelfde velden zijn beschikbaar voor het maken van een activumregel, maar u kunt indien nodig ook **Fabrikant** en **Model** voor een functionele locatie selecteren. Als u alleen een functionele locatie op een regel selecteert, maar geen selecties opgeeft in **Activatype**, **Fabrikant**, **Model**, **Type onderhoudstaak**, **Variant van type onderhoudstaak** en **Handel**, worden alle activa voor deze functionele locatie op het moment van de onderhoudsplanning opgenomen in de onderhoudsronde.

19. Klik op het sneltabblad **Groepen** op **Toevoegen** om een werkordergroep te selecteren die u wilt opnemen in de onderhoudsronde. Verschillende werkordergroepen kunnen worden gekoppeld aan één onderhoudsronde.

20. Sla de instellingen op.

>[!NOTE]
>In de velden **Activa** en **Regels** in de groep **Details** van het sneltabblad **Koptekst** ziet u het totaal aantal activa en regels voor de geselecteerde onderhoudsronde.

![Figuur 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Onderhoudsrondes plannen

Wanneer u een onderhoudsronde hebt ingesteld, voert u een planningstaak uit om alle taken voor de onderhoudsronde te plannen.

1. Klik op **Activabeheer** > **Periodiek** > **Preventief onderhoud** > **Onderhoudsronden plannen**, of **Activabeheer** > **Algemeen** > **Onderhoudsschema** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen** > selecteer een onderhoudsschemaregel in de lijst > knop **Onderhoudsronden**.

2. Selecteer in het veld **Periode** het periodetype dat u voor de planningstaak wilt gebruiken.

3. Voer in het veld **Periodefrequentie** het aantal perioden in dat u in de planningstaak wilt opnemen. De huidige datum is de begindatum van de planning.

4. Selecteer Ja op de wisselknop **Automatisch maken** als een werkorder automatisch moet worden gemaakt op basis van een onderhoudsronde.

>[!NOTE]
>Als deze wisselknop is ingesteld op Ja en de wisselknop **Automatisch maken** voor de onderhoudsronde in het formulier **Onderhoudsronden** ook is ingeschakeld op Ja, worden werkorders gemaakt op basis van de regels in de onderhoudsronde en worden onderhoudsschemaregels met de status 'Werkorder gemaakt' ook gemaakt. Als slechts een van de wisselknoppen voor **Automatisch maken** in deze vervolgkeuzelijst of in **Onderhoudsronden** is ingesteld op Ja, worden alleen regels in onderhoudsronden gemaakt die de status Gemaakt hebben. In dat geval worden er geen werkorders gemaakt.

5. U kunt zo nodig specifieke ronden of een andere begindatum voor de planningstaak selecteren. Klik op **Filter** en voeg de ronden toe die u wilt opnemen.

6. Klik op **OK**.

7. Nu kunt u de taken van de onderhoudsronden bekijken in **Activabeheer** > **Algemeen** > **Onderhoudsschema** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels**. Als de geplande ronden zijn gekoppeld aan een werkordergroep, ziet u ook onderhoudsschemaregels in **Openstaande onderhoudsschemagroepen**. Onderhoudsschemaregels op basis van een ronde hebben het verwijzingstype Onderhoudsronden.

![Figuur 2](media/14-preventive-maintenance.png)

![Figuur 3](media/15-preventive-maintenance.png)

- Wanneer werkorders handmatig worden gemaakt voor activa die onder een leveranciersgarantie vallen, wordt er een dialoogvenster weergegeven om de gebruiker te informeren over de garantie. Het maken van de werkorder kan dan worden geannuleerd. De controle op een garantierelatie wordt achterwege gelaten voor werkorders die automatisch worden gemaakt.  
- U kunt een batchtaak instellen op het sneltabblad **Op de achtergrond uitvoeren** als u de ronden met vaste intervallen wilt plannen.  
- Als een ronde is opgenomen in verschillende werkordergroepen (zie [Werkordergroepen](../work-orders/work-order-pools.md)), wordt één record voor elke groep weergegeven in **Openstaande onderhoudsschemagroepen**. Dit wordt gedaan om de filteropties voor werkordergroepen te optimaliseren.


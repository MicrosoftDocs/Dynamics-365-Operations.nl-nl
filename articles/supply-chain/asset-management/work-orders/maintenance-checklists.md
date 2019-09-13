---
title: Onderhoudscontrolelijsten
description: In dit onderwerp wordt beschreven hoe u onderhoudscontrolelijsten maakt in Activabeheer.
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
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875594"
---
# <a name="maintenance-checklists"></a>Onderhoudscontrolelijsten


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Onderhoudscontrolelijsten worden ingesteld voor typen onderhoudstaken en worden gebruikt wanneer u aan een werkorder werkt. Het invullen van onderhoudscontrolelijsten maakt deel uit van het voltooien van een werkorder. Zie de sectie [Categorieën onderhoudstaaktypen en typen onderhoudstaken, varianten van typen onderhoudstaken, specialismen voor onderhoudstaken en onderhoudscontrolelijsten](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) voor meer informatie over het instellen van onderhoudscontrolelijsten voor onderhoudstaaktypen in het formulier **Standaardinstellingen voor type onderhoudstaak**.

Wanneer u met onderhoudscontrolelijsten in een werkorder werkt, kunt u de vooraf gedefinieerde onderhoudscontrolelijsten voor typen onderhoudstaken invullen. Het is ook mogelijk om extra onderhoudscontrolelijsten toe te voegen.

## <a name="fill-out-a-maintenance-checklist"></a>Een onderhoudscontrolelijst invullen

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder en klik op **Onderhoudscontrolelijst**.

3. In **Controlelijst voor onderhoudstaken voor werkorders** ziet u onderhoudscontrolelijsten voor alle werkordertaken. Als de werkordertaken verschillende typen onderhoudstaken hebben, kunnen de onderhoudscontrolelijsten verschillen voor elke werkordertaak. Selecteer een werkordertaak om met de gerelateerde onderhoudscontrolelijst te werken. Details van een geselecteerde regel in een onderhoudscontrolelijst worden weergegeven op het sneltabblad **Regeldetails**.

4. Vul alle regels van de onderhoudscontrolelijst één voor één in in de volgorde waarin ze worden weergegeven. Een regel van het type Koptekst in de onderhoudscontrolelijst wordt gebruikt als kop om de regels van de onderhoudscontrolelijst eronder te groeperen. U hoeft geen koptekst in te vullen, maar zoals voor alle regeltypen voor onderhoudscontrolelijsten is het mogelijk om een **notitie** toe te voegen aan de koptekst.

5. Als instructies betrekking hebben op een regel in een onderhoudscontrolelijst, is het selectievakje **Instructies** ingeschakeld. Lees de instructies voor de geselecteerde regel in de onderhoudscontrolelijst in de sectie **Instructies** op het sneltabblad **Regeldetails**.

6. Welke informatie nodig is om een regel in een onderhoudscontrolelijst te voltooien, kan variëren, afhankelijk van het bijbehorende type onderhoudscontrolelijst. U voltooit een regel in een onderhoudscontrolelijst door de velden op het sneltabblad **Regeldetails** in te vullen. Op een regel van het type Tekst voegt u bijvoorbeeld een **notitie** toe waarin wordt uitgelegd wat het resultaat is van die controlelijstregel. Op een regel van het type Meting voegt u de **tellerwaarde** toe die u hebt gelezen op de apparatuur en kunt u zo nodig ook een **notitie** toevoegen.

- Wanneer u een regel in een onderhoudscontrolelijst hebt ingevuld, schakelt u het selectievakje **Gecontroleerd** op de regel in om deze als voltooid te markeren. Als u een regel in een onderhoudscontrolelijst wilt negeren omdat deze niet relevant is voor de werkordertaak, schakelt u het selectievakje **N.v.t.** op de regel in. Als een regel in een onderhoudscontrolelijst is gemarkeerd als **Verplicht**, moet u deze markeren als Gecontroleerd of N.v.t.  
- U kunt registraties van onderhoudscontrolelijsten alleen bijwerken als de werkorder de levenscyclusstatus [Actief](../setup-for-work-orders/work-order-lifecycle-states.md) heeft.  


## <a name="add-a-maintenance-checklist-line"></a>Een regel toevoegen aan een onderhoudscontrolelijst

Onderhoudscontrolelijsten worden gemaakt op basis van de definitie in de standaardinstellingen voor onderhoudstaaktypen en worden overgebracht naar een werkordertaak. Indien nodig kunt u onderhoudscontrolelijstregels toevoegen aan een werkordertaak. Handmatig toegevoegde regels in onderhoudscontrolelijsten krijgen de referentie Handmatig.

1. In **Controlelijst voor onderhoudstaken voor werkorders** selecteert u de werkordertaak waarvoor u een onderhoudscontrolelijst wilt toevoegen.

2. Selecteer op het sneltabblad **Onderhoudscontrolelijstregels** een regel voor onderhoudscontrolelijsten en druk op de pijl-omlaag op het toetsenbord als u een nieuwe regel wilt invoegen na de geselecteerde regel in de onderhoudscontrolelijst. Het volgende nummer in de reeks wordt automatisch ingevoegd in het veld **Regelnummer**. U kunt ook een onderhoudscontrolelijstregel selecteren en op de knop **Regel toevoegen** klikken als u een nieuwe regel wilt invoegen boven de geselecteerde onderhoudscontrolelijstregel.

3. Typ een naam voor de regel voor de onderhoudscontrolelijst in het veld **Naam**.

4. Typ een naam voor de regel voor de onderhoudscontrolelijst in het veld **Type**. Voor elk type onderhoudscontrolelijst worden de gerelateerde velden weergegeven op het sneltabblad **Regeldetails**.  
  a. Tekst wordt gebruikt om een regel in een onderhoudscontrolelijst toe te voegen met een beschrijving van wat er moet worden gedaan. U kunt dit type onderhoudscontrolelijst gebruiken als u wilt dat een medewerker iets controleert of inspecteert, zonder een specifiek (meetbaar) resultaat te verwachten. Voeg een omschrijving in van wat er moet worden gedaan in de sectie **Instructies** op het sneltabblad **Regeldetails**. b. Koptekst wordt gebruikt als koptekst voor het groeperen van de onderhoudscontrolelijstregels die onder de koptekst worden weergegeven. Dit is handig als u verschillende onderhoudscontrolelijstregels hebt die in specifieke gebieden kunnen worden onderverdeeld. Voer in het veld **Naam** een omschrijvende naam in.  
  c. Sjabloon is niet van toepassing wanneer u handmatig een onderhoudscontrolelijstregel toevoegt aan een werkordertaak.  
  d. Variabele wordt gebruikt om een mogelijk resultaat in een bereik te definiëren op een onderhoudscontroleregel. In [Categorieën van onderhoudstaaktypen en onderhoudstaaktypen, varianten van onderhoudstaaktypen, onderhoudstaakspecialismen en onderhoudscontrolelijsten](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) wordt beschreven hoe u variabelen voor onderhoudscontrolelijsten instelt. Voeg in het veld **Naam** een naam in om de variabele te beschrijven. Selecteer de variabele in het veld **Variabele**. Voeg een omschrijving in van wat er moet worden gedaan in de sectie **Instructies** op het sneltabblad **Regeldetails**.  
  e. Meting wordt gebruikt om een specifieke meting vast te leggen. Typ een naam voor de meting in het veld **Naam**. Selecteer op het sneltabblad **Regeldetails** de opties **Teller** en **Eenheid**. Geef in de sectie **Instructies** op wat er moet worden gedaan.  

5. Wanneer u klaar bent met het handmatig toevoegen van onderhoudscontrolelijstregels, vult u de regels in zoals wordt beschreven in de bovenstaande sectie.

>[!NOTE]
>In **Controlelijst voor onderhoudstaken voor werkorders** kunt u onderhoudscontrolelijstregels met de verwijzing Taaktype niet verwijderen. U kunt alleen onderhoudscontrolelijstregels verwijderen die de verwijzing Handmatig hebben en handmatig zijn gemaakt door u of andere onderhoudsmedewerkers.


![Figuur 1](media/14-work-orders.png)


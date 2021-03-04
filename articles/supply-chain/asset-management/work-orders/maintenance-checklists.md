---
title: Onderhoudscontrolelijsten
description: In dit onderwerp wordt beschreven hoe u onderhoudscontrolelijsten maakt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderChecklist, EntAssetMobileWorkOrderLineChecklistDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1091af424f84265ffa7983fca8ddc3f66138a5cd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425263"
---
# <a name="maintenance-checklists"></a>Onderhoudscontrolelijsten

[!include [banner](../../includes/banner.md)]



Onderhoudscontrolelijsten worden ingesteld voor typen onderhoudstaken. U kunt onderhoudscontrolelijsten invullen als onderdeel van het voltooien van een werkorder. Raadpleeg **Categorieën onderhoudstaaktypen en typen onderhoudstaken, varianten van typen onderhoudstaken, specialismen voor onderhoudstaken en onderhoudscontrolelijsten** voor meer informatie over het instellen van onderhoudscontrolelijsten voor onderhoudstaaktypen in het formulier [Standaardinstellingen voor type onderhoudstaak](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Wanneer u met onderhoudscontrolelijsten in een werkorder werkt, kunt u de vooraf gedefinieerde onderhoudscontrolelijsten voor typen onderhoudstaken invullen. U kunt ook meer onderhoudscontrolelijsten toevoegen.


## <a name="fill-in-a-maintenance-checklist"></a>Een onderhoudscontrolelijst invullen

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder en selecteer vervolgens in het actievenster op het tabblad **Werkorder** in de groep **Regels** de optie **Onderhoudscontrolelijst**.

3. In **Controlelijst voor onderhoudstaken voor werkorders** ziet u controlelijsten voor alle werkordertaken. Als de werkordertaken verschillende typen onderhoudstaken hebben, kunnen de onderhoudscontrolelijsten verschillen voor elke werkordertaak. Selecteer een werkordertaak om met de gerelateerde onderhoudscontrolelijst te werken. Details van de geselecteerde regel in een onderhoudscontrolelijst worden weergegeven op het sneltabblad **Regeldetails**.

4. Vul alle regels van de onderhoudscontrolelijst één voor één in in de volgorde waarin ze worden weergegeven. U voltooit een regel in een onderhoudscontrolelijst door de velden op het sneltabblad **Regeldetails** in te vullen. De informatie die nodig is voor het invullen van een regel kan variëren, afhankelijk van het regeltype. Op een regel van het type **Tekst** voegt u bijvoorbeeld een notitie toe waarin wordt uitgelegd wat het resultaat is van die controle. Op een regel van het type **Meting** voert u de tellerwaarde in die u hebt afgelezen op de apparatuur en kunt u zo nodig ook een notitie toevoegen. Een regel van het type **Koptekst** in de onderhoudscontrolelijst wordt gebruikt als kop om de regels van de onderhoudscontrolelijst eronder te groeperen. U hoeft geen koptekst in te vullen. Net als voor alle andere typen onderhoudscontrolelijstregels kunt u een notitie toevoegen aan een regel van het type **Koptekst**.

5. Als instructies betrekking hebben op een regel in een onderhoudscontrolelijst, is het selectievakje **Instructies** ingeschakeld. Lees de instructies voor de geselecteerde regel in de onderhoudscontrolelijst in het veld **Instructies** op het sneltabblad **Regeldetails**.

6. Wanneer u een regel in een onderhoudscontrolelijst hebt ingevuld, schakelt u het selectievakje **Gecontroleerd** op die regel in om deze als voltooid te markeren. Als u een regel in een onderhoudscontrolelijst wilt negeren omdat deze niet relevant is voor de werkordertaak, schakelt u het selectievakje **N.v.t.** op de regel in. Als het selectievakje **Verplicht** is ingeschakeld op een onderhoudscontrolelijstregel, schakelt u het selectievakje **Ingeschakeld** of **N.v.t.** in.

>[!NOTE]
>U kunt registraties van onderhoudscontrolelijsten alleen bijwerken als de werkorder de levenscyclusstatus [Actief](../setup-for-work-orders/work-order-lifecycle-states.md) heeft.  


## <a name="add-a-maintenance-checklist-line"></a>Een regel toevoegen aan een onderhoudscontrolelijst

Onderhoudscontrolelijsten worden gemaakt op basis van de definitie in de standaardinstellingen voor onderhoudstaaktypen en worden overgebracht naar een werkordertaak. Indien nodig kunt u onderhoudscontrolelijstregels toevoegen aan een werkordertaak. Handmatig toegevoegde regels in onderhoudscontrolelijsten krijgen de referentie **Handmatig**.

1. Op de pagina **Controlelijst voor onderhoudstaken voor werkorders** selecteert u de werkordertaak waarvoor u een onderhoudscontrolelijst wilt toevoegen.

2. Selecteer in het sneltabblad **Regels onderhoudscontrolelijsten** een regel voor een onderhoudscontrolelijst. Druk vervolgens op de **pijl-omlaag** om een nieuwe regel in te voegen na de geselecteerde regel. Het volgende nummer in de reeks wordt automatisch ingevoerd in het veld **Regelnummer**. Selecteer **Regel toevoegen** om een nieuwe regel in te voegen voor de geselecteerde regel. 

3. Typ een naam voor de regel voor de onderhoudscontrolelijst in het veld **Naam**.

4. Typ een naam voor de regel voor de onderhoudscontrolelijst in het veld **Type**. Voor elk type onderhoudscontrolelijst worden de gerelateerde velden weergegeven op het sneltabblad **Regeldetails**.
    - **Tekst**: gebruik dit type om een onderhoudscontrolelijstregel met tekst toe te voegen die beschrijft wat moet worden gedaan. U kunt dit type onderhoudscontrolelijst bijvoorbeeld gebruiken als u wilt dat een medewerker iets controleert of inspecteert, zonder een specifiek (meetbaar) resultaat te verwachten. Nadat u dit type hebt geselecteerd, voert u op het sneltabblad **Regelsdetails** in het veld **Instructies** de tekst in waarin wordt beschreven wat moet worden gedaan.
    - **Koptekst**: een regel van dit type in de onderhoudscontrolelijst wordt gebruikt als kop om de regels van de onderhoudscontrolelijst eronder te groeperen. Dit type is handig als u verschillende onderhoudscontrolelijstregels hebt die in specifieke gebieden kunnen worden onderverdeeld. Nadat u dit type hebt geselecteerd, voert u een beschrijvende naam in het veld **Naam** in.
    - **Sjabloon**: dit type is niet van toepassing wanneer u handmatig een onderhoudscontrolelijstregel toevoegt aan een werkordertaak.  
    - **Variabele**: dit type wordt gebruikt om een mogelijk resultaat in een bereik te definiëren op de onderhoudscontroleregel. Raadpleeg [Categorieën van onderhoudstaaktypen en onderhoudstaaktypen, varianten van onderhoudstaaktypen, onderhoudstaakspecialismen en onderhoudscontrolelijsten](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) voor meer informatie over hoe u variabelen voor onderhoudscontrolelijsten instelt. Nadat u dit type hebt geselecteerd, voert u een beschrijvende naam voor de variabele in het veld **Naam** in. Selecteer de variabele in het veld **Variabele** op het sneltabblad **Regeldetails**. Voer in het veld **Instructies** een omschrijvende tej=kst in voor wat moet worden gedaan.
    - **Meting**: gebruik dit type om een specifieke meting op de onderhoudscontrolelijstregel vast te leggen. Nadat u dit type hebt geselecteerd, voert u een naam voor de meting in het veld **Naam** in. Selecteer op het sneltabblad **Regeldetails** in de velden **Teller** en **Eenheid** de toepasselijke waarden. Voer in het veld **Instructies** een omschrijvende tej=kst in voor wat moet worden gedaan.

5. Wanneer u de regels voor de onderhoudscontrolelijst handmatig hebt toegevoegd, vult u de regels in zoals wordt beschreven in de sectie **Een onderhoudscontrolelijst invullen** hierboven.

>[!NOTE]
>Op de pagina **Controlelijst voor onderhoudstaken voor werkorders** kunt u onderhoudscontrolelijstregels met de verwijzing **Taaktype** niet verwijderen. U kunt alleen onderhoudscontrolelijstregels verwijderen die handmatig zijn gemaakt door u of andere onderhoudsmedewerkers en die de verwijzing **Handmatig** hebben.

In de onderstaande afbeelding ziet u een voorbeeld van een onderhoudscontrolelijst.

![Figuur 1](media/14-work-orders.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
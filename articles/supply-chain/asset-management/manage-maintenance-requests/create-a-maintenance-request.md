---
title: Onderhoudsverzoeken maken
description: In dit onderwerp wordt uitgelegd hoe u een onderhoudsverzoek maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7fc9ec2f6a9a8a11d824e4b5c13d5aa173541454
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571916"
---
# <a name="create-maintenance-requests"></a>Onderhoudsverzoeken maken

[!include [banner](../../includes/banner.md)]

 

Onderhoudsverzoeken kunnen worden gebruikt als onderhoudsmedewerkers of productiemedewerkers ontdekken dat apparatuur moet worden gerepareerd, maar de reparatie niet meteen kan worden uitgevoerd.

**Voorbeeld:** terwijl een onderhoudsmedewerker een reparatie doet, ontdekt ze dat een ander activum op dezelfde locatie moet worden onderhouden. De onderhoudsmedewerker heeft echter niet de tijd of de vereiste reserveonderdelen om de reparatietaak uit te voeren. Daarom maakt ze een onderhoudsverzoek voor het activum en voert ze een korte beschrijving van het probleem in.

De sectie **Actieve onderhoudsverzoeken** van het deelvenster **Verwante informatie** aan de rechterkant van de pagina **Alle activa** of **Actieve activa** (**Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa** of **Actieve activa**) bevat de actieve onderhoudsverzoeken die aan het geselecteerde activum gekoppeld zijn.

1. Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**.
2. Selecteer **Nieuw**.
3. Selecteer het type onderhoudsverzoek in het dialoogvenster **Aanvraag maken** in het veld **Type onderhoudsverzoek**. Er wordt een standaardtype voorgesteld.
4. Voer in het veld **Beschrijving** een naam of titel in die kort het onderhoudsverzoek beschrijft.
5. Selecteer in de velden **Functionele locatie** en **Activum** een functionele locatie of een activum, of een combinatie van een functionele locatie en een activum, indien nodig. U kunt een onderhoudsverzoek maken zonder een activum te selecteren en het activum kan later aan het onderhoudsverzoek worden toegevoegd. Als de onderhoudsmedewerker die is aangemeld, is gekoppeld aan een resource die is gerelateerd aan een activum, wordt het veld **Activum** automatisch ingesteld.

    Als er al een onderhoudsverzoek is gekoppeld aan het geselecteerde activum, verschijnt een berichtenbalk boven aan het dialoogvenster **Aanvraag maken** met de id van het bestaande onderhoudsverzoek. Een berichtenbalk waarschuwt u ook als het activum onder een garantieovereenkomst valt.

6. Selecteer in het veld **Serviceniveau** een serviceniveau dat de urgentie van de aanvraag aangeeft.
7. Als u een activum hebt geselecteerd in stap 5, kunt u de velden **Foutsymptoom**, **Foutgebied** en **Fouttype** gebruiken om een foutregistratie te maken.
8. Als het onderhoudsverzoek uitvaltijd voor onderhoud heeft veroorzaakt, voert u de begindatum en -tijd van de uitvaltijd in.

    Het veld **Gestart door** wordt automatisch ingesteld op uw naam.

10. Het veld **Werkelijke begin** wordt automatisch ingesteld op de huidige datum en tijd. U kunt deze waarde echter zo nodig wijzigen.
11. Voer in het veld **Notities** eventuele aanvullende notities in die vereist zijn.
12. Selecteer **OK**.

![Onderhoudsverzoek maken](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Daaropvolgende verwerking van onderhoudsverzoeken

Nadat een onderhoudsverzoek is gemaakt, maar voordat deze wordt omgezet in een werkorder, moeten er verschillende gegevens worden bijgewerkt. Normaal gesproken voert een planner of een andere administratieve medewerker deze taak uit.

- Op de pagina **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken** selecteert u de aanvraag waarmee moet worden gewerkt en vervolgens **Bewerken**.

In de detailweergave u diverse gegevens bijwerken. Hieronder vindt u enkele voorbeelden:

- Selecteer en verifieer het activum. Als u later een ander activum moet selecteren, kunt u de optie **Activum geverifieerd** instellen op **Nee**.
- Selecteer een verantwoordelijke groep onderhoudsmedewerkers en/of een verantwoordelijke onderhoudsmedewerker. Zie [Verantwoordelijke onderhoudsmedewerkers](../setup-for-maintenance-requests/responsible-workers.md) voor meer informatie over de vereiste stap.
- Selecteer een type onderhoudstaak en, als deze informatie relevant is, een gerelateerde onderhoudstaakvariant en een vakgebied.
- Voer in de velden **Breedtegraad** en **Lengtegraad** de geografische coördinaten in. Alle coördinaten die aan een onderhoudsverzoek worden toegevoegd, worden automatisch overgebracht naar een gerelateerde werkorder. 

![Onderhoudsverzoek bijwerken](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Als u een activum selecteert wanneer u een onderhoudsverzoek maakt, kunt u één fout aan het activum toevoegen. Nadat het onderhoudsverzoek is gemaakt, kunt u zo nodig meer fouten toevoegen. Als u fouten wilt toevoegen, selecteert u **Activafout** op de pagina **Alle onderhoudsverzoeken**.

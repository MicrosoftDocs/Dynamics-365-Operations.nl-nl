---
title: Handmatig gemaakte werkorders
description: In dit onderwerp wordt uitgelegd hoe u werkorders handmatig maakt in Activabeheer.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875587"
---
# <a name="manually-created-work-orders"></a>Handmatig gemaakte werkorders

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


U kunt werkorders op twee manieren handmatig maken:

- in **Alle werkorders** of **Actieve werkorders**  
- in **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken** of **De onderhoudsverzoeken van mijn functionele locatie**.  

## <a name="create-work-order"></a>Werkorder maken

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Klik op de knop **Nieuw**.

3. Selecteer een type werkorder in de vervolgkeuzelijst **Werkorder maken**.

4. Selecteer zo nodig een beschrijving.

5. Selecteer het activum voor de werkorder en het type onderhoudstaak.

>[!NOTE]
>Wanneer u een activum selecteert, zijn er mogelijk drie tabbladen beschikbaar: het tabblad **Mijn activa** bevat activa voor de functionele locaties waaraan u (de medewerker die is aangemeld bij het systeem) kan worden toegewezen (ingesteld in [Onderhoudsmedewerkers en medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md)). Als er geen functionele locaties voor een medewerker zijn ingesteld in [Onderhoudsmedewerkers en medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md), is het tabblad **Mijn activa** niet zichtbaar. Het tabblad **Actieve activa** bevat een lijst met alle activa met de levenscyclusstatus 'Actief' voor activa. Op het tabblad **Activaweergave** wordt een structuurweergave getoond van functionele locaties en elementen die op die locaties zijn geïnstalleerd.

6. Selecteer indien nodig de **variant van type onderhoudstaak** en **Handel**.

7. Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.

8. Selecteer de verwachte begin- en einddatums in de daarvoor bestemde velden.

9. Klik op **OK** om een nieuwe werkorder te maken.

10. Bewerk zo nodig de werkorder in **Alle werkorders**.

- In **Alle werkorders** kunt u verschillende activa aan een werkorder toevoegen in de detailweergave. Daarvoor voegt u regels toe op het sneltabblad **Onderhoudstaken voor werkorders**. Op een activum kunt u alleen de typen onderhoudstaken selecteren die zijn gedefinieerd voor het activumtype dat voor het activum is geselecteerd.  
- Als u het serviceniveau of de kritikaliteit van een activum hebt gewijzigd nadat u het activum in een werkorder hebt gebruikt, (zie [Serviceniveaus van activa](../setup-for-objects/object-priorities.md) en [Kritikaliteiten van activa](../setup-for-objects/object-criticalities.md)), wordt het serviceniveau of de kritikaliteit van de werkorder niet dienovereenkomstig bijgewerkt.
- Telkens wanneer een werkorderregel wordt toegevoegd aan of verwijderd uit de werkorder, wordt de kritikaliteit van een werkorder opnieuw berekend.
- In de detailweergave **Alle werkorders** > weergave **Koptekst** > sneltabblad **Planning** kunt u een verantwoordelijke onderhoudsmedewerkersgroep of een verantwoordelijke onderhoudsmedewerker selecteren in het veld **Verantwoordelijke groep** of **Verantwoordelijke**. Deze instellingen kunnen worden gewijzigd zolang de werkorder actief is, bijvoorbeeld wanneer de levenscyclusstatus van de werkorder verandert. De automatische selectie tijdens het maken van de werkorder is gebaseerd op de instellingen in **Verantwoordelijke onderhoudsmedewerkers**. Als u werkordertaken toevoegt of verwijdert nadat u een werkorder hebt gemaakt, en de velden **Verantwoordelijke groep** en **Verantwoordelijke** leeg zijn wanneer u de werkorder bijwerkt, zoekt Activabeheer naar een mogelijke overeenkomst in het instellingenformulier voor een verantwoordelijke onderhoudsmedewerkersgroep of een verantwoordelijke onderhoudsmedewerker. Als het veld **Verantwoordelijke groep** of het veld **Verantwoordelijke** al is ingevuld wanneer u de werkorder bijwerkt, worden er geen wijzigingen aangebracht. 

- In **Onderhoudsstatus** kunt u een berekening uitvoeren om een overzicht te krijgen van de werkbelasting met betrekking tot inkomende en voltooide werkorders.  

- Gebruik op het sneltabblad **Regeldetails** de velden **Breedtegraad** en **Lengtegraad** om geografische coördinaten toe te voegen voor het activum dat is geselecteerd in de werkordertaak.  

## <a name="create-related-work-order"></a>Gerelateerde werkorder maken

U kunt een gerelateerde werkorder maken voor een bestaande werkorder, bijvoorbeeld als u met primaire en secundaire werkorders wilt werken. Een nieuwe werkorder is gebaseerd op een werkordertaak op basis van een bestaande werkorder.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder waarvoor u een gerelateerde werkorder wilt maken.

3. Klik op **Gerelateerde werkorder**.

4. Selecteer in het dialoogvenster **Gerelateerde werkorder maken** de werkordertaak waarvoor u een gerelateerde werkorder wilt maken in het veld **Werkordertaak**.

5. Selecteer een type onderhoudstaak in het veld **Type onderhoudstaak** en indien nodig een variant van het type gerelateerde onderhoudstaak en handel in de velden **Variant van type onderhoudstaak** en **Handel**.

6. Als dit de eerste gerelateerde werkorder is die u maakt, klikt u op het keuzerondje **Nieuwe werkorder**.

7. Selecteer een **Werkordertype** en een **Beschrijving** in de betreffende velden.

8. Indien nodig kunt u het serviceniveau van de werkorder wijzigen in het veld **Serviceniveau**.

9. Voeg de verwachte begin- en einddatums in de daarvoor bestemde velden in.

10. Klik op **OK**. De nieuwe gerelateerde werkorder wordt weergegeven in de lijst **Alle werkorders**.

11. Als u een gerelateerde werkorder maakt voor een werkorder die al gerelateerde werkorders heeft, kunt u de werkordertaak toevoegen aan een reeds gerelateerde werkorder. U doet dit door te klikken op het keuzerondje **Toevoegen aan gerelateerde werkorder** in stap 6. Vervolgens selecteert u de gerelateerde werkorder waaraan u een nieuwe werkordertaak wilt toevoegen. Bewerk indien nodig de velden **Serviceniveau**, **Verwachte begindatum** en **Verwachte einddatum** en klik op **OK**. De werkordertaak wordt toegevoegd aan de bestaande gerelateerde werkorder.


![Figuur 1](media/03-work-orders.png)

**Opmerking:** als u een masker voor verwante werkorders hebt ingesteld in **Parameters voor activabeheer** > koppeling **Werkorders** > **Verwante-werkordermasker**, worden werkorder-id's gemaakt op basis van de maskerinstellingen. Als er geen verwante-werkordermasker is ingesteld, wordt de volgende beschikbare werkorder-id gebruikt voor gerelateerde werkorders.

## <a name="copy-work-order"></a>Werkorder kopiëren

Het is mogelijk om snel een nieuwe werkorder te maken op basis van een bestaande werkorder. Deze manier van werken met werkorders verschilt van het maken van werkorders op basis van onderhoudsplannen. Het is bijvoorbeeld handig als u een werkorder hebt die veel werkordertaken bevatten met verschillende taken voor verschillende activa en die regelmatig moeten worden voltooid.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder waaruit u inhoud wilt kopiëren.

3. Klik op **Werkorder kopiëren**. De werkorderinstellingen van de geselecteerde werkorder worden weergegeven. U kunt zo nodig enkele velden bewerken.

4. Klik op **OK** om de nieuwe werkorder te maken.

5. Bewerk zo nodig de werkorder in **Alle werkorders**.

>[!NOTE]
>Wanneer de nieuwe werkorder wordt gemaakt, worden bepaalde gegevens rechtstreeks uit de bestaande werkorder gekopieerd. Informatie over prognoses, hulpmiddelen, onderhoudscontrolelijsten, functionele locatie, adressen en planning wordt niet gekopieerd, maar geïnitialiseerd vanuit de huidige instellingen in Activabeheer. Dit betekent dat wijzigingen die in de gegevens worden aangebracht in de periode tussen het moment dat de eerste werkorder is gemaakt en het moment waarop u de werkorder kopieert, worden opgenomen in de nieuwe werkorder die u hebt gemaakt. Voorbeelden zijn wijzigingen in prognoses of bijgewerkte onderhoudscontrolelijsten.


![Figuur 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Een werkorder maken op basis van een onderhoudsverzoek

1. Klik op **Activabeheer** > **Algemeen** > **Onderhoudsverzoeken** > **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**.

2. Selecteer het onderhoudsverzoek waarvoor u een werkorder wilt maken en klik op **Bewerken**.

3. Klik in **Alle aanvragen** op **Werkorder**.

4. Vul de vervolgkeuzelijst **Werkorder** in. Als er een type onderhoudstaak is geselecteerd in het onderhoudsverzoek, kunt u indien nodig een ander type onderhoudstaak selecteren wanneer u de werkorder maakt.

5. Klik op **OK**. Er wordt een bericht weergegeven waarin wordt gemeld dat de werkorder is gemaakt.

6. Als u wilt zien welke werkorders aan een onderhoudsverzoek zijn gekoppeld, selecteert u het onderhoudsverzoek in de lijsten **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken** en klikt u op de knop **Werkorders**.


![Figuur 3](media/05-work-orders.png)


>[!NOTE]
>Werkorders kunnen ook automatisch worden gemaakt door onderhoudsplantaken te plannen of door het 'automatisch maken' van onderhoudsplannen of onderhoudsronden in te stellen voor een activum. Werkorders die zijn gemaakt op basis van onderhoudsverzoeken in **Onderhoudsschema**, worden gemaakt met de typen onderhoudstaken die in de onderhoudsverzoeken zijn geselecteerd.


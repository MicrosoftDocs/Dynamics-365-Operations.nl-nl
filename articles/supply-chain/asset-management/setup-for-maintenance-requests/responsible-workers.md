---
title: Verantwoordelijke onderhoudsmedewerkers
description: In dit onderwerp wordt uitgelegd hoe u verantwoordelijke onderhoudsmedewerkers instelt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b5f83474e56c996a40bdbdf7d3a7c8d495429c6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208933"
---
# <a name="responsible-maintenance-workers"></a>Verantwoordelijke onderhoudsmedewerkers

[!include [banner](../../includes/banner.md)]

 

Verantwoordelijke onderhoudsmedewerkers kunnen worden gerelateerd aan activumtypen, activa, functionele locaties, categorieën met typen onderhoudstaken, typen onderhoudstaken, varianten op typen onderhoudstaken en transacties. Ze kunnen worden gebruikt met werkorders en onderhoudsverzoeken om een voorkeur aan te geven voor de onderhoudsmedewerkers die verantwoordelijk moeten zijn voor een werkorder. (Deze onderhoudsmedewerkers zijn echter niet noodzakelijkerwijs dezelfde medewerkers die zijn gepland om de werkorder uit te voeren.) Het gebruik van deze functionaliteit is optioneel. Deze kan bijvoorbeeld worden gebruikt om verantwoordelijke medewerkers of medewerkersgroepen voor specifieke werktypen of werkgebieden te selecteren.

Tijdens de levenscyclus van een werkorder of een onderhoudsverzoek kunnen verantwoordelijke onderhoudsmedewerkers worden gewijzigd of bijgewerkt. Deze wijziging of update kan worden gerelateerd aan bijvoorbeeld een wijziging in de levenscyclusstatus van het onderhoudsverzoek of de levenscyclusstatus van de werkorder.

De instellingen op de pagina **Verantwoordelijke onderhoudsmedewerkers** worden *niet* gebruikt tijdens de planning van de werkorder.

> [!NOTE]
> In Activabeheer kunt u ook *voorkeuren* opgeven voor onderhoudsmedewerkers die mogelijk aan werkorders worden toegewezen tijdens de planning van de werkorder.

Voordat u verantwoordelijke onderhoudsmedewerkers kunt instellen, moet u de medewerkers en onderhoudsmedewerkersgroepen instellen die beschikbaar moeten zijn voor selectie. Zie [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor informatie over het instellen van medewerkers en onderhoudswerknemersgroepen.

## <a name="set-up-responsible-maintenance-workers"></a>Verantwoordelijke onderhoudsmedewerkers instellen

1. Selecteer **Activabeheer** \> **Instellen** \> **Medewerkers** \> **Verantwoordelijke onderhoudsmedewerkers**
2. Selecteer **Nieuw** om een record te maken.
3. Maak eerst standaardinstellingen voor een verantwoordelijke onderhoudsmedewerker of verantwoordelijke medewerkersgroep, waarbij u alleen het veld **Verantwoordelijke onderhoudsmedewerkersgroep** en/of het veld **Verantwoordelijke medewerker** instelt. Laat de overige velden leeg. Deze standaardinstellingen worden gebruikt tijdens de planning van de werkorder als er geen andere, specifiekere combinatie overeenkomt met de inhoud van de werkorder.

    > [!NOTE]
    > Wanneer er tijdens het maken van een onderhoudsverzoek een verantwoordelijke onderhoudsmedewerker of een verantwoordelijke onderhoudsmedewerkersgroep beschikbaar is gesteld voor selectie op de pagina **Alle onderhoudsverzoeken**, doorloopt Activabeheer alle verantwoordelijke onderhoudsmedewerkersrecords om te controleren op een mogelijke overeenkomst. De meest specifieke combinatie wordt altijd als eerste gecontroleerd. Dat wil zeggen dat Activabeheer eerst controleert op een overeenkomst voor het veld **Handel**. Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Variant op type onderhoudstaak**. Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Type onderhoudstaak** enzovoort. Zoals u aan de indeling van de pagina ziet, betekent dit gedrag dat Activabeheer, om de meest specifieke combinatie te vinden, elke record van rechts naar links controleert op een overeenkomst (eerst **Handel**, vervolgens **Variant op type onderhoudstaak**, **Type onderhoudstaak**, **Categorie van type onderhoudstaak**, **Functionele locatie**, **Activum** en tot slot **Activumtype**). Als er geen overeenkomst wordt gevonden, wordt in deze zeven velden de standaardrecord zonder selecties gebruikt.

In de volgende afbeelding ziet u een voorbeeld van de pagina **Verantwoordelijke onderhoudsmedewerkers**.

![Pagina Verantwoordelijke onderhoudsmedewerkers](media/08-setup-for-requests.png)

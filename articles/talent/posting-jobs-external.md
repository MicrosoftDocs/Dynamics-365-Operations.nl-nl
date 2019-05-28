---
title: Functies publiceren naar externe vacaturesites via Attract
description: In dit onderwerp wordt uitgelegd hoe u Dynamics 365 for Talent - Attract gebruikt voor het publiceren van functies naar externe wervingssites
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517717"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Functies publiceren naar externe vacaturesites via Attract

[!include [banner](../includes/banner.md)]

U wilt uw openstaande posities aan zoveel mogelijk kandidaten voorleggen. Wervingssites, zoals Broadbean, helpen u bij het realiseren van dit doel. Met Microsoft Dynamics 365 Talent: Attract kunt u nu functies publiceren naar Broadbean en Microsoft biedt voortdurend nieuwe aanbiedingen in dit gebied.

## <a name="post-jobs-to-broadbean"></a>Functies naar Broadbean publiceren

Voordat u functies naar Broadbean kunt publiceren, moet u de Broadbean-integratie configureren.

> [!NOTE]
> - Als u functies naar externe sites wilt publiceren, moet u over de [Uitgebreide invoegtoepassing voor aanstellingen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) beschikken.
> - Van deze functie kan momenteel een voorbeeld worden bekeken. Als u de functie wilt proberen, moet u [deze inschakelen in de beheerinstellingen van Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>Broadbean-integratie configureren

1. Meld u aan bij Attract als beheerder.
2. Selecteer de knop **Instellingen** (het tandwielsymbool) in de rechterbovenhoek van de pagina en selecteer vervolgens **Beheercentrum**.
3. Schakel de integratie in op het tabblad **Functiebordinstellingen** in de sectie **Broadbean-integratie inschakelen**.
4. Neem contact op met Broadbean en voer uw gegevens in **Gebruikersnaam, Client-ID, Coderingstoken** in.

> [!WARNING]
> Uw Broadbean-referenties zijn gevoelig en vertrouwelijk. Bewaar deze daarom zorgvuldig en deel ze op verantwoorde wijze. Iedereen met een beheerdersrol in Attract kan deze referenties weergeven.

> [!NOTE]
> Microsoft en Attract zijn niet betrokken bij het maken en onderhouden van deze waarden. Het is uw verantwoordelijkheid ze om up-to-date te houden in Attract en te werken met Broadbean om eventuele problemen op te lossen die betrekking hebben op uw referenties.

### <a name="post-a-job-to-broadbean"></a>Een functie naar Broadbean publiceren

Nadat Broadbean is ingeschakeld, kunnen wervers en beheerders er een functie naar publiceren. U kunt een sollicitatie-URL voor de functie hebben.

1. Open in Attract de functie die u wilt publiceren naar Broadbean.
2. Selecteer in de sectie **Publicaties** de knop **Nu publiceren** die hoort bij Broadbean.
3. Volg de instructies in het Broadbean-venster.

Attract geeft de volgende gegevens door naar Broadbean:

- Aanvraag-ID
- Functie
- Taakomschrijving
- Functielocatie
- Sollicitatie-URL
- Informatie van wervingsbureau

Nadat in Broadbean de publicatie is voltooid, wordt in de sectie **Publicaties** van de functie in Attract de Broadbean-status als **Gepubliceerd** weergegeven.

> [!NOTE]
> - Voor Broadbean is het veld **Bedrijfstak** vereist. Momenteel is dit veld standaard ingesteld op **IT**. U kunt de waarde echter wijzigen voor de juiste bedrijfstak in het venster voor Broadbean-functiepublicatie.
> - Het duurt enige tijd voordat Broadbean de publicatie van uw functie naar alle door u geselecteerde functieborden heeft voltooid. Daarom kan er enige vertraging optreden voordat Attract een statusupdate voor de functie geeft.

### <a name="view-a-broadbean-job-posting"></a>Een Broadbean-functiepublicatie weergeven

Nadat u een functie naar Broadbean hebt gepubliceerd, kunt u deze weergeven via Attract.

1. Open in Attract de functie die u wilt weergeven in Broadbean.
2. Selecteer in de sectie **Publicaties** de ellipsknop (**...**) die hoort bij Broadbean en selecteer vervolgens **Weergave**.

De Broadbean-functiepublicatie wordt weergegeven in een nieuw venster.

### <a name="update-a-broadbean-job-posting"></a>Een Broadbean-functiepublicatie bijwerken

U kunt een Broadbean-functiepublicatie op twee manieren bijwerken.

1. Open in Attract de functie die u wilt bijwerken.
2. Selecteer in de sectie **Publicaties** de knop **Publicatie bijwerken** die hoort bij Broadbean.
3. Bewerk de publicatie in het Broadbean-venster.

– of –

1. Open in Attract de functie die u wilt weergeven in Broadbean.
2. Selecteer in de sectie **Publicaties** de ellipsknop (**...**) die hoort bij Broadbean en selecteer vervolgens **Weergave**.
3. Bewerk in het Broadbean-venster de functiedetails en publiceer de functie opnieuw. De functiedetails in Attract worden niet gewijzigd.

### <a name="remove-a-broadbean-job-posting"></a>Een Broadbean-functiepublicatie verwijderen

U kunt desgewenst een functiepublicatie uit Broadbean verwijderen.

1. Open in Attract de functie die u wilt verwijderen.
2. Selecteer in de sectie **Publicaties** de ellipsknop (**...**) die hoort bij Broadbean en selecteer vervolgens **Publicatie verwijderen**.

Na de functie uit Broadbean is verwijderd, bevat het Broadbean-item in Attract de knop **Nu publiceren**. De aanwezigheid van deze knop geeft aan dat de functie is verwijderd en opnieuw kan worden gepubliceerd.

### <a name="troubleshoot-the-broadbean-integration"></a>Problemen met Broadbean-integratie oplossen

Als u problemen hebt met het publiceren van een functie naar Broadbean, probeert u deze stappen.

1. Controleer of de Broadbean-referenties die u hebt ingevoerd in Attract, geldig en juist zijn.
2. Als de referenties geldig en juist zijn, neemt u contact op met [Broadbean-ondersteuning](https://www.broadbean.com/resources/support/).
3. Als het probleem zich blijft voordoen, neemt u contact op met [Microsoft-ondersteuning](./talent-support.md).

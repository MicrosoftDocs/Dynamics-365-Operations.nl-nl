---
title: Plannen hoe u het algemene adresboek en extra adresboeken configureert
description: "In dit artikel worden de overwegingen en de beslissingen beschreven die u tijdens het planningsproces moet maken, voordat u het globale adresboek en eventuele aanvullende adresboeken instelt en configureert In Microsoft Dynamics 365 for Finance and Operations. Voor enkele beslissingen moet u de beslissingen bevestigen die voor andere gebieden van het product zijn gemaakt, zoals de organisatiehiërarchie."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a>Plannen hoe u het algemene adresboek en extra adresboeken configureert

[!include[banner](../includes/banner.md)]


In dit artikel worden de overwegingen en de beslissingen beschreven die u tijdens het planningsproces moet maken, voordat u het globale adresboek en eventuele aanvullende adresboeken instelt en configureert In Microsoft Dynamics 365 for Finance and Operations. Voor enkele beslissingen moet u de beslissingen bevestigen die voor andere gebieden van het product zijn gemaakt, zoals de organisatiehiërarchie.

<a name="global-address-book"></a>Algemeen adresboek
-------------------

Voordat u met het algemene adresboek begint te werken, moet u de standaardwaarden hiervoor definiëren. Deze standaardwaarden worden vervolgens gebruikt voor alle aanvullende adresboeken die u maakt. 

**Beslissingen:**

-   In welke volgorde wilt u namen weergeven voor partijregistraties van het type **Persoon**? Eén volgorde is bijvoorbeeld achternaam, tweede voornaam, voornaam.
-   Moeten partijregistraties worden verwijderd uit het adresboek wanneer de rolregistratie wordt verwijderd? Moet de partijregistratie bijvoorbeeld ook worden verwijderd als een klantregistratie wordt verwijderd?
-   Moeten gebruikers op de hoogte worden gesteld wanneer er een nieuwe registratie is gemaakt waardoor er een dubbele registratie voorkomt in het algemene adresboek?
-   Moet het DUNS-nummer (Data Universal Numbering System) in de partijregistratiegegevens worden opgenomen?
-   Moet de uniciteit van het nummer worden gecontroleerd als het DUNS-nummer in een partijregistratie wordt opgenomen?
-   Wilt u een standaardpartijtype, persoon of organisatie wanneer in het algemene adresboek een partijregistratie wordt gemaakt?
-   Welke gebruikersrollen moeten toegang kunnen krijgen tot privéadressen en contactgegevens van partijregistraties?

## <a name="additional-address-books"></a>Extra adresboeken
Nadat u het algemene adresboek hebt gemaakt, kunt u desgewenst extra adresboeken maken, zoals een apart adresboek voor elk bedrijf in uw organisatie of voor elke bedrijfstak. Fabrikam is bijvoorbeeld een internationale organisatie met meerdere bedrijven en meerdere bedrijfstakken. Fabrikam is van plan om een adresboek te maken voor elke bedrijfstak. Voor bedrijfstakken die op meer dan één locatie voorkomen, zoals de bedrijfstak voor pneumatisch gereedschap, wil Fabrikam een adresboek maken voor elke locatie. Chris, de IT-manager van Fabrikam, heeft de volgende lijst met adresboeken gemaakt die nodig zijn. In deze lijst worden ook de partijregistraties beschreven die elk adresboek moet bevatten.

-   **Contracten in de openbare sector (PubSC)**: partijregistraties voor alle partijen die betrokken zijn in contracten van Fabrikam met de openbare sector.
-   **Contracten in de privésector (PubSC)**: partijregistraties voor alle partijen die betrokken zijn bij contracten met de privésector.
-   **Elektronisch gereedschap (ET)**: partijregistraties voor alle partijen die betrokken zijn bij de aankoop of verkoop van elektronisch gereedschap of die op een andere manier omgaan met het elektronisch gereedschap dat wordt geleverd door of gekocht voor Fabrikam in het Japanse bedrijf van Fabrikam.
-   **Pneumatisch gereedschap (PTJPN)**: partijregistraties voor alle partijen die betrokken zijn bij de aankoop of verkoop van pneumatisch gereedschap of die op een andere manier omgaan met het pneumatisch gereedschap dat wordt geleverd door of gekocht voor Fabrikam in het Japanse bedrijf van Fabrikam.
-   **Pneumatisch gereedschap (PTJPN)**: partijregistraties voor alle partijen die betrokken zijn bij de aankoop of verkoop van pneumatisch gereedschap of die op een andere manier omgaan met het pneumatisch gereedschap dat wordt geleverd door of gekocht voor Fabrikam in het Amerikaanse bedrijf van Fabrikam.

**Beslissing:**

-   Hoeveel extra adresboeken maakt u?

### <a name="address-book-security"></a>Beveiliging van adresboeken

U kunt adresboeken op elk moment maken en u kunt ook op elk moment beveiligingsparameters instellen voor de adresboeken. U hoeft geen beveiligingsbevoegdheden in te stellen voor een adresboek, maar in dat geval kunnen alle werknemers in uw organisatie wel alle partijregistraties in dat adresboek bekijken. U kunt beveiligingsbevoegdheden voor partijregistraties instellen via adresboeken. Beveiligingbevoegdheden worden gebaseerd op teams. Op deze manier kunnen alleen werknemers die aan een team zijn toegewezen dat toegang heeft tot een adresboek, de partijregistraties in dat adresboek weergeven. U moet de teams selecteren die toegang hebben tot elk adresboek. Voor elk adresboek kunt u beveiligingsbevoegdheden instellen die toegang geven of weigeren aan specifieke teams. Wanneer u een team toegang geeft tot een adresboek, kunnen alle teamleden de registraties in het adresboek weergeven. Als u een team geen toegang tot een adresboek verleent, kunnen de teamleden het adresboek of de inhoud ervan niet zien. 

**Beslissing:**

-   Welke teams moeten toegang hebben tot elk nieuw adresboek dat u maakt?





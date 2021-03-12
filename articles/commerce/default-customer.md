---
title: Een standaardklant maken
description: In dit onderwerp wordt beschreven hoe u een standaardklant kunt maken die u kunt gebruiken wanneer u een kanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1dd4dfc5b8ca7af66941d081b4c20be0f5d6001d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993395"
---
# <a name="create-a-default-customer"></a>Een standaardklant maken


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een standaardklant kunt maken die u kunt gebruiken wanneer u een kanaal maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Wanneer u een kanaal maakt, moet u een standaardklant opgeven. U kunt eenvoudig een standaardklant maken nadat u eerst de klantgroep en het adresboek van de klant hebt gemaakt.

## <a name="create-a-customer-group"></a>Een klantgroep maken

Als er nog geen klantgroepen zijn, kunt u er een maken. Voorbeelden zijn groepen die verschillende klantgroepen vertegenwoordigen, zoals groothandel, internet, werknemers, enzovoort.

Volg deze stappen om een klantgroep te maken.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Klanten \> Klantgroepen**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het vak **Klantgroep** een klantgroep-id in.
1. Voer in het vak **Omschrijving** een passende beschrijving in.
1. Voer in het vak **Betalingsvoorwaarden** een toepasselijke waarde in.
1. Voer in het vak **Tijd tussen vervaldatum van factuur en betalingsdatum** een toepasselijke waarde in.
1. Voer in het vak **Standaardbelastinggroep** een belastinggroep in, indien van toepassing.
1. Schakel het selectievakje **Prijzen inclusief btw** in, indien van toepassing.
1. Voer in het vak **Standaardreden voor afschrijving** een toepasselijke waarde in, indien van toepassing.

De volgende afbeelding geeft een aantal geconfigureerde klantgroepen weer.

![Klantengroepen](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Een nieuw adresboek voor een klant maken

Een klant moet aan een adresboek zijn gekoppeld. Als er nog geen is gemaakt, moet u er een maken.

Volg deze stappen om een nieuw klantadresboek te maken.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Kanaalinstellingen \> Adresboeken**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het vak **Naam** een naam in.
1. Voer in het vak **Omschrijving** een beschrijving in.
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeld van een adresboek.

![Adresboek](media/address-book.png)

## <a name="create-a-default-customer"></a>Een standaardklant maken

Volg deze stappen om een standaardklant te maken.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Klanten \> Alle klanten**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer 'Persoon' in de vervolgkeuzelijst **Type**.
1. Selecteer in de vervolgkeuzelijst **Klantrekening** een rekeningnummer of voer dit in (bijvoorbeeld '100001').
1. Selecteer of typ in de vervolgkeuzelijst **Voornaam** een naam (bijvoorbeeld 'Standaard').
1. Selecteer of typ in de vervolgkeuzelijst **Tweede voornaam** een naam (bijvoorbeeld 'Retail').
1. Selecteer of typ in de vervolgkeuzelijst **Achternaam** een naam (bijvoorbeeld 'Klant').
1. Selecteer of typ in de vervolgkeuzelijst **Valuta** een valuta (bijvoorbeeld 'EUR').
1. Selecteer in de vervolgkeuzelijst **Valuta** de zojuist gemaakte klantgroep.
1. Selecteer in de vervolgkeuzelijst **Adresboeken** een bestaand adresboek van de klant.
1. Selecteer **Opslaan** en ga terug naar het scherm met klantgegevens voor de nieuwe klant.

> [!NOTE]
> Het is niet nodig om een adres voor een standaardklant toe te voegen.

In de volgende afbeelding ziet u hoe een klant wordt gemaakt.

![Een standaardklant maken](media/default-customer-creation.png)

In de volgende afbeelding wordt de configuratie van een standaardklant weergegeven.

![Voorbeeld van klantconfiguratie](media/default-customer-configuration1.png)

De meeste standaardwaarden in het detailscherm van de klant kunnen blijven staan, maar twee waarden moeten worden gewijzigd.

1. Vouw in het scherm met klantgegevens de **Standaardwaarden verkooporders** uit.
1. Selecteer in de vervolgkeuzelijst **Site** een vooraf geconfigureerde site of voer deze in.
1. Selecteer in de vervolgkeuzelijst **Magazijn** een vooraf geconfigureerd magazijn of voer dit in.

In de volgende afbeelding ziet u hoe een klant wordt geconfigureerd.

![Voorbeeld van klantconfiguratie](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

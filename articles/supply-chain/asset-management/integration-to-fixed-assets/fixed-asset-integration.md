---
title: Beheer van bedrijfsmiddelen integreren met vaste activa
description: In dit onderwerp wordt uitgelegd hoe u de modules Asset Management en Vaste activa integreert, zodat u vaste activa kunt koppelen aan onderhoudsactiva.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425334"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Beheer van bedrijfsmiddelen integreren met vaste activa

[!include [banner](../../includes/banner.md)]

Als u de modules **Asset Management** en **Vaste activa** integreert, kunt u vaste activa kunt koppelen aan onderhoudsactiva. Vaste activa-gebruikers kunnen vervolgens een onderhoudsactivum maken van een nieuw of bestaand vast activum en gebruikers van Asset Management kunnen een onderhoudsactivum koppelen aan een bestaand vast activum. Met deze functie kunnen gebruikers van Vaste activa ook gemakkelijk de kosten bekijken die zijn geboekt vanuit werkorders voor gerelateerde onderhoudsactiva.

> [!NOTE]
> In dit onderwerp verwijzen *onderhoudsactiva* naar activa van de module **Asset Management** en *vaste activa* naar activa uit de module **Vaste activa**.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Een standaardlocatie instellen voor nieuwe onderhoudsactiva die worden gemaakt op basis van vaste activa (optioneel)

Met deze optionele configuratie kunt u een standaard functionele locatie instellen voor nieuwe onderhoudsactiva die zijn gemaakt op basis van vaste activa. Deze configuratie wordt normaal gesproken slechts één keer uitgevoerd als dit van toepassing is.

Volg deze stappen om de configuratie te voltooien.

1. Ga naar **Asset Management \> Instellingen \> Parameters voor Asset Management**.
1. Selecteer op het tabblad **Vaste activa** in het veld **Functionele locatie** de standaardlocatie.
1. Selecteer **Opslaan** in het actievenster.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Werken met geïntegreerde onderhoudsactiva en vaste activa

In deze sectie vindt u een verzameling procedures waarin verschillende manieren worden weergegeven waarop u kunt werken met de geïntegreerde functies Asset Management en Vaste activa.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Een bestaand onderhoudsactivum aan een vast activum koppelen

Volg deze stappen om een bestaand onderhoudsactivum aan een vast activum te koppelen

1. Ga naar **Asset Management \> Activa \> Alle activa** (of **Actieve activa**).
1. Selecteer een activum.
1. Selecteer op het sneltabblad **Vaste activa** in het veld **Vaste-activanummer** een bestaand vast activum.
1. Selecteer **Opslaan** in het actievenster.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Het vaste activum weergeven dat is gekoppeld aan een geselecteerd onderhoudsactivum

Volg deze stappen om het vaste activum weer te geven dat is gekoppeld aan een geselecteerd onderhoudsactivum.

1. Ga naar **Asset Management \> Activa \> Alle activa** (of **Actieve activa**).
1. Selecteer een activum.
1. Selecteer de koppeling op het sneltabblad **Vaste activa** in het veld **Vaste-activanummer**.

    De pagina **Vaste activa** voor het geselecteerde activum wordt geopend. (Gewoonlijk vindt u deze pagina via **Vaste activa \> Vaste activa \> Vaste activa**.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Het onderhoudsactivum weergeven dat is gekoppeld aan een geselecteerd vast activum

Volg deze stappen om het onderhoudsactivum weer te geven dat is gekoppeld aan een geselecteerd vast activum.

1. Ga naar **Vaste activa \> Vaste activa \> Vaste activa**.
1. Selecteer een activum.
1. Selecteer in het actievenster op het tabblad **Asset Management** in de groep **Weergeven** de optie **Onderhoudsactivum**.

    De pagina **Onderhoudsactivum** voor het activum dat is gekoppeld aan het geselecteerde vaste activum, wordt geopend. (Gewoonlijk vindt u deze pagina via **Asset Management \> Activa \> Alle activa**.)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Onderhoudskosten weergeven die zijn gekoppeld aan een vast activum

Asset Management-werkorders kunnen worden geboekt voor onderhoudsactiva, en elk van deze werkorders heeft meestal een kostprijs. Wanneer een vast activum wordt gekoppeld aan een onderhoudsactivum, kunt u direct vanuit het vaste activum de gerelateerde kosten weergeven.

Volg deze stappen om de onderhoudskosten weer te geven die samenhangen met een vast activum.

1. Ga naar **Vaste activa \> Vaste activa \> Vaste activa**.
1. Selecteer een activum.
1. Selecteer in het actievenster op het tabblad **Asset Management** in de groep **Weergeven** de optie **Onderhoudskosten**.

    De pagina **Onderhoudskosten** wordt geopend met de gerelateerde kosten.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Een nieuw onderhoudsactivum maken voor een bestaand vast activum

Volg deze stappen om een nieuw onderhoudsactivum te maken voor een bestaand vast activum.

1. Ga naar **Vaste activa \> Vaste activa \> Vaste activa**.
1. Selecteer een activum.
1. Selecteer in het actievenster op het tabblad **Asset Management** in de groep **Nieuw** de optie **Onderhoudsactivum maken**. (Als deze optie niet beschikbaar is, is er mogelijk al een onderhoudsactivum gekoppeld aan het geselecteerde vaste activum.)
1. Voltooi het maken van het activum zoals wordt beschreven in [Een activum maken](../objects/create-an-object.md).

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Een nieuw vast activum maken en een nieuw onderhoudsactivum toevoegen

Volg deze stappen om een nieuw vast activum te maken en een onderhoudsactivum ervoor toe te voegen.

1. Ga naar **Vaste activa \> Vaste activa \> Vaste activa**.
1. Selecteer **Nieuw** in het actievenster.
1. Voltooi het maken van het vaste activum zoals wordt beschreven in [Een vast activum maken](../../../finance/fixed-assets/tasks/create-fixed-asset.md).
1. Selecteer in het actievenster op het tabblad **Asset Management** in de groep **Nieuw** de optie **Onderhoudsactivum maken**.
1. Voltooi het maken van het activum zoals wordt beschreven in [Een activum maken](../objects/create-an-object.md).

### <a name="remove-the-association-between-two-assets"></a>De koppeling tussen twee activa verwijderen

In sommige gevallen moet u een onderhoudsactivum mogelijk loskoppelen van het vaste activum. Als u bijvoorbeeld [een nieuw onderhoudsactivum wilt maken](#new-maintenance-from-fixed) vanuit een vast activum, moet u eerst een bestaande koppeling verwijderen.

Volg deze stappen om een bestaande koppeling tussen een onderhoudsactivum en een vast activum te verwijderen.

1. Ga naar **Asset Management \> Activa \> Alle activa** (of **Actieve activa**).
1. Zoek het vaste activum en open het.
1. Wis op het sneltabblad **Vast activum** de waarde uit het veld **Functionele locatie**.
1. Selecteer **Opslaan** in het actievenster.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Inhoud kopiëren naar een andere landinstelling
description: In dit artikel wordt beschreven hoe u bestaande inhoud kopieert naar een andere landinstelling op een site in Microsoft Dynamics 365 Commerce Site Builder.
author: josaw1
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6afa871048bde22133ae083b8d56b6e99e49c401
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269256"
---
# <a name="copy-content-to-another-locale"></a>Inhoud kopiëren naar een andere landinstelling

[!include[banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u bestaande inhoud kopieert naar een andere landinstelling op een site in Microsoft Dynamics 365 Commerce Site Builder.

Wanneer u inhoud maakt in Commerce Site Builder, is deze altijd gekoppeld aan een landinstellingen-id, bijvoorbeeld 'en-us'. U kunt afzonderlijke pagina's en activa naar een andere landinstelling binnen dezelfde e-commercesite kopiëren door van de ene naar de andere landinstelling over te schakelen wanneer u een inhoudsitem bewerkt en vervolgens een nieuwe variant van het item maakt. In sommige gevallen, zoals wanneer u een geheel nieuwe landinstelling in uw winkelketen start, heeft het zin om alle inhoudsitems in een bestaande landinstelling te dupliceren naar de nieuwe landinstelling. Als de nieuwe landinstelling dezelfde standaardtaal heeft als een van de bestaande landinstellingen, kunt u de bestaande landinstelling gebruiken als de bronlandinstelling voor de kopieerbewerking van de landinstelling. (De landinstellingen en-us- en en-au gebruiken bijvoorbeeld beide de Engelse taal.) Op deze manier kunt u de inspanning beperken die nodig is om de inhoud te lokaliseren in de nieuwe landinstelling.

In de volgende procedures wordt uitgelegd hoe u een nieuwe landinstelling aan een bestaand kanaal toevoegt, alle inhoudsitems van een bestaande landinstelling kopieert naar een nieuwe landinstelling en de status van een kopieerbewerking van een landinstelling controleert.

## <a name="add-a-new-locale"></a>Een nieuwe landinstelling toevoegen

Voer de volgende stappen uit om een nieuwe landinstelling toe te voegen in Commerce Site Builder.

1. Ga naar uw site in Site Builder.
1. Selecteer in het linkernavigatievenster de optie **Site-instellingen** en selecteer vervolgens **Kanalen**.
1. Selecteer onder **Kanaal** het kanaal waaraan u de nieuwe landinstelling wilt toevoegen.
1. Selecteer **Een landinstelling toevoegen** in het dialoogvenster voor kanalen dat rechts wordt weergegeven.
1. Selecteer een landinstelling in het dialoogvenster **Een landinstelling toevoegen** in het veld **Te ondersteunen landinstelling**.
1. Controleer of de waarde **Domein** juist is.
1. Voer onder **Pad** een uniek URL-pad in (bijvoorbeeld **en-us** of **english-us**).
1. Selecteer **OK**.
1. Sluit het dialoogvenster voor kanalen.
1. Controleer onder **Kanaal** of de nieuwe landinstelling naast het juiste kanaal staat.
1. Selecteer **Opslaan en publiceren**.

> [!NOTE]
> Voordat de nieuwe landinstelling in Site Builder kan worden geconfigureerd, moet deze worden toegevoegd aan het bijbehorende online winkelkanaal in Commerce Headquarters.

## <a name="copy-all-content-items-to-a-new-locale"></a>Alle inhoudsitems naar een nieuwe landinstelling kopiëren

Voer de volgende stappen uit om alle inhoudsitems naar een nieuwe landinstelling te kopiëren in Commerce Site Builder.

1. Ga naar uw site in Site Builder.
1. Selecteer in het linkernavigatievenster de optie **Site-instellingen** en selecteer vervolgens **Kanalen**.
1. Selecteer op de opdrachtbalk **Kopie van landinstelling maken**.
1. Controleer in het dialoogvenster **Kopie van landinstelling maken** dat rechts onder **Bronsite** wordt weergegeven, dat de juiste site is geselecteerd.
1. Selecteer het bronkanaal in het veld **Bronkanaal**.
1. Selecteer hetzelfde bronkanaal in het veld **Kanaal van bestemming**.
1. Selecteer de landinstelling voor bron in het veld **Landinstelling voor bron**.
1. Selecteer de nieuwe landinstelling in het veld **Landinstelling voor bestemming**.
1. Selecteer **Landinstelling kopiëren**. Met een melding wordt bevestigd dat de kopieerbewerking voor landinstelling is gestart.

> [!NOTE]
> U kunt ook inhoud kopiëren tussen verschillende kanalen.

## <a name="monitor-the-status-of-the-locale-copy"></a>De status van de kopie van de landinstelling controleren

Als u de status van de kopieerbewerking van een landinstelling wilt controleren, gaat u als volgt te werk.

1. Ga naar uw site in Site Builder.
1. Selecteer in het linkernavigatievenster de optie **Site-instellingen** en selecteer vervolgens **Taken**.
1. Selecteer onder **Huidige taken** de taak die u wilt controleren. In het dialoogvenster dat rechts wordt weergegeven, worden taakdetails weergegeven.

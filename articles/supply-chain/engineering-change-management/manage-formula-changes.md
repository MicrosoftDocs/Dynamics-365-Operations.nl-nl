---
title: Wijzigingen in formules en de ingrediënten beheren
description: In dit onderwerp wordt beschreven hoe u formulebeheer uitvoert en wijzigingen in de hoofdgegevens van de procesfabricage kunt beheren.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 31953fd29c471e52bd63dbb02c20f5f224c3cae2
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103034"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Wijzigingen in formules en de ingrediënten beheren

[!include [banner](../includes/banner.md)]

Als u de procesfabricagemogelijkheden van Microsoft Dynamics 365 Supply Chain Management gebruikt, kunt u ook de gerelateerde formulebeheermogelijkheden gebruiken om de volgende wijzigingen te beheren:

- **Formule- en planningsartikelen**: hiermee kunt u wijzigingen in ingrediënten in formules en de co- en bijproducten beheren.
- **Co- en bijproducten**: hiermee kunt u hoeveelheden en andere gegevens van de co- en bijproducten in een formule bewerken.
- **Catch weight-artikelen**: hiermee kunt u wijzigingen in artikelen met een catch weight beheren.

## <a name="turn-this-feature-on-or-off"></a>Deze functie in- of uitschakelen

Voor deze functie moeten de functies *Beheer voor technische wijzigingen* en *Wijzigingen in formules en hun ingrediënten beheren* zijn ingeschakeld voor uw systeem. Zie [Overzicht van technisch wijzigingsbeheer](product-engineering-overview.md) voor meer informatie over het in- of uitschakelen van deze functies.

## <a name="feature-naming-conventions"></a>Naamgevingsconventies voor functies

In de gebruikersinterface en documentatie van Supply Chain Management wordt de functionaliteit voor wijzigingsbeheer meestal *technisch wijzigingsbeheer* genoemd. De beheerbare producten worden meestal *technische producten* genoemd. Hoewel deze terminologie doorgaans niet is gekoppeld aan het beheer van formules voor procesfabricage, moet u technisch wijzigingsbeheer als eenvoudig wijzigingsbeheer zien, en technische producten als producties met versies.

## <a name="work-with-formula-change-management-features"></a>Werken met functies voor het wijzigingsbeheer van formules

In de volgende lijst wordt samengevat hoe de functies voor technisch wijzigingsbeheer van toepassing zijn op formulebeheer. Deze lijst bevat ook koppelingen naar meer informatie. Aangezien bij formulewijzigingsbeheer gebruik wordt gemaakt van de functies voor technisch wijzigingsbeheer, moet u weten hoe technisch wijzigingsbeheer in het algemeen werkt, zodat u de formules en de ingrediënten kunt beheren.

- **Gecentraliseerde productgegevensbeheer**: hiermee kunt u een organisatie instellen die via een beheerd vrijgaveproces zorgt voor nauwkeurige en relevante productgegevens die beschikbaar zijn voor gebruikers in de hele onderneming. Zie [Technische bedrijven en regels voor gegevenseigendom](engineering-org-data-ownership-rules.md) voor meer informatie.
- **Versiebeheer voor producten**: hiermee kunt u wijzigingen in producten bijhouden via productversies en het product gedurende alle fasen van de toeleveringsketen controleren. Op deze manier kunt u de wijzigingen in uw formules bijhouden. Zie [Technische versies en categorieën van technische producten](engineering-versions-product-category.md) voor meer informatie.
- **Productlevenscyclusbeheer**: hiermee kunt u de zichtbaarheid van productgegevens in de gehele organisatie beheren en de beschikbaarheid van productversies in elke fase van de toeleveringsketen controleren. U hebt gedetailleerde controle over wanneer een productversie kan worden gebruikt in specifieke bedrijfsprocessen en u kunt uw eigen levenscyclusstatussen maken om aan uw bedrijfsbehoeften te voldoen. Zie voor meer informatie [Levenscyclusstatussen en transacties van producten](product-lifecycle-state-transactions.md).
- **Formulewijzigingsbeheer**: gebruikers in uw hele organisatie kunnen wijzigingen in formules aanvragen. Met wijzigingsorders kunt u het effect van voorgestelde wijzigingen beoordelen en documenteren. U kunt werkstromen toevoegen om het wijzigingsproces en de vrijgave van nieuwe versies van het product en de formule te beheren. Zie [Wijzigingen in technische producten beheren](engineering-change-management.md) voor meer informatie.
- **Gereedheidscontrole**: gebruik systeemcontroles en gebruikersadvies (vragenlijsten en controlelijsten) om ervoor te zorgen dat alle vereiste productgegevens volledig zijn ingevoerd voordat het product wordt vrijgegeven. Zie voor meer informatie [Productgereedheid](product-readiness.md).
- **Verbeterde functionaliteit voor productvrijgave**: u kunt volledig gedefinieerde versies van een product en de bijbehorende formule vrijgeven vanuit een organisatie (rechtspersoon) aan andere rechtspersonen. U kunt zelfs beslissen of de productgegevens moeten worden gecontroleerd of bewerkt vóór de vrijgave. Zie [Productstructuren van de vrijgave](release-product-structure.md) voor meer informatie.

De meeste onderwerpen waaraan wordt gekoppeld in de vorige lijst, bevatten voorbeelden die zijn gebaseerd op stuklijsten. Formules werken echter op dezelfde manier. Hieronder vindt u enkele extra concepten die handig zijn om te weten wanneer u wijzigingsbeheer (of alleen formulewijzigingsbeheer) gebruikt voor het beheren van formules en stuklijsten:

- Voor elke [technische productcategorie](engineering-versions-product-category.md) kunt u het productietype (stuklijst, formule of planningsartikel) opgeven. U kunt ook opgeven of catch weight-ondersteuning vereist is voor producten waarvoor die categorie wordt gebruikt.
- Co- en bijproducten zijn geen technische producten. Daarom hebben ze bepaalde versies. Als u deze moet wijzigen, maakt u gewoon een nieuw product. Deze benadering maakt het onderhoud eenvoudiger.
- U kunt eindartikelen beheren die stuklijsten zijn en onderliggende formuleartikelen hebben. De functionaliteit werkt voor elke combinatie van stuklijsten die formules en/of formules met stuklijsten bevatten.

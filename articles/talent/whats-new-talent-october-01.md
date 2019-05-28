---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (1 oktober 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 15b5fd7095a62aa9b7b79ebfcada667959b756aa
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517738"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (1 oktober 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.1035.0**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.

## <a name="turn-off-electronic-payment-validation"></a>Validatie van elektronische betalingen uitschakelen

De validatie van elektronische betalingsgegevens wordt uitgevoerd als u voorschotten voor automatische overmaking instelt via het werkgebied **Selfservice werknemer** of rechtstreeks in het werknemerformulier. Deze optie biedt u de flexibiliteit om die validatie te verwijderen als u geen behoefte hebt aan de validatiecontroles voor bedragen en resterende waarden. Deze functie is handig als u een integratie met een externe salarisadministratie met verschillende vereisten uitvoert.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Selfservice manager - Voeg doelstellingen voor teamleden toe via de tegel Teamprestatiedoelstellingen

Vóór deze versie konden managers doelstellingen aan hun individuele werknemers toevoegen via de prestatiedoelstellingen die aan elke werknemer waren gekoppeld. Met deze update kunnen managers de tegel **Teamprestatiedoelstellingen** openen en nieuwe doelstellingen maken door een van hun directe ondergeschikten te selecteren.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Selfservice manager - Voeg beoordelingen voor teamleden toe via de tegel Beoordelingen van teamprestaties

Vóór deze versie konden managers beoordelingen aan hun individuele werknemers toevoegen via de beoordelingen die aan elke werknemer waren gekoppeld. Met deze update kunnen managers de tegel **Beoordelingen van teamprestaties** openen en nieuwe beoordelingen maken door een van hun directe ondergeschikten te selecteren.

## <a name="configure-proration-options-by-leave-plan"></a>Opties voor betaling naar rato configureren per verlofplan

Organisaties kennen vrije tijd verschillend toe, afhankelijk van wanneer werknemers in dienst treden of het bedrijf verlaten. In sommige organisaties krijgen werknemers hun volledige toewijzing op de begindatum toegekend terwijl andere bedrijven voor een evenredige toekenning kiezen. In deze versie zijn nieuwe opties beschikbaar zodat u kunt kiezen hoe de beloningen en toekenningen moeten worden omgeslagen voor nieuwe en vertrekkende werknemers in een organisatie. Tot de opties behoren: Evenredig, Volledige toerekening en Geen toerekening.

## <a name="other-changes"></a>Andere wijzigingen

-   Entiteit Werknemer bijgewerkt: de tegel **Persoonlijk** kan nu worden bijgewerkt met de Excel-invoegtoepassing/gegevensbeheer.

-   Wijziging in de beveiliging om de knoppen **Verwijderen** en **Deactiveren** te kunnen verwijderen in de selfservice voor werknemers voor betalingsgegevens.

## <a name="known-issue"></a>Bekend probleem

-   **Probleem:** als een nieuwe bijlage wordt toegevoegd aan een werknemer, zijn de knoppen **Nieuw** en **Bewerken** niet beschikbaar. **Oplossing:** voordat u de pagina van de bijlage opent, controleert u of de feitenvakken op de pagina **Werknemer** zijn gesloten. Als de feitenvakken zijn gesloten wanneer de pagina **Werknemer** wordt geladen, worden de knoppen **Bijlagen** ingeschakeld. (Dit probleem wordt opgelost in de volgende platformupdate.)

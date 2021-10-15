---
title: Workflows voor inkoopbeheer
description: Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd. U kunt een budgetteringsworkflow maken om een workflow in te stellen.
author: Henrikan
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a819093d9ee6f999e637281e54905968fe361566
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575531"
---
# <a name="procurement-and-sourcing-workflows"></a>Workflows voor inkoopbeheer

[!include [banner](../includes/banner.md)]

Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd. U kunt een budgetteringsworkflow maken om een workflow in te stellen.

Een workflow vertegenwoordigt een bedrijfsproces. Een werkstroom definieert hoe een document zich door het systeem begeeft en geeft aan wie een taak moet voltooien of een document moet goedkeuren. Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:

- **Consistente processen**: u kunt het goedkeuringsproces voor specifieke documenten definiëren, zoals opdrachten tot inkoop en onkostennota's. Door gebruik van het werkstroomsysteem garandeert u dat documenten op een consistente, efficiënte manier worden verwerkt en goedgekeurd.
- **Zichtbaarheid van processen**: met het werkstroomsysteem kunt u de status, historie en prestatiegegevens van een specifiek workflowexemplaar volgen. Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.
- **Gecentraliseerde werklijst**— Gebruikers kunnen een gecentraliseerde werklijst raadplegen die werkstroomtaken en goedkeuringen weergeven die aan hen zijn toegewezen in alle werkstromen waaraan ze deelnemen. Dit is beschikbaar op de pagina Werkitems.

## <a name="the-types-of-workflows-that-you-can-create"></a> De typen werkstromen die u kunt maken

De volgende workflowtypen zijn beschikbaar voor Inkoop en sourcing.

| Type | Met dit type kunt u |
|---|---|
| Controle inkoopbestelopdracht | Controle- en goedkeuringsworkflows maken voor opdrachten tot inkoop. |
| Controle van opdracht tot inkoopregel | Controle- en goedkeuringsworkflows maken voor regels van opdrachten tot inkoop. |
| Workflow voor inkooporders | Controle- en goedkeuringsworkflows maken voor inkooporders. |
| Workflow voor inkooporderregels | Controle- en goedkeuringsworkflows maken voor inkooporderregels. |
| Workflow voor toepassing voor het toevoegen van leveranciers | Controle- en goedkeuringsworkflows maken voor het toevoegen van nieuwe leveranciers via leverancieraanvragen. |

> [!IMPORTANT]
> Wanneer u een nieuwe werkstroom toevoegt, worden mogelijk ook de volgende verouderde werkstromen weergegeven in het dialoogvenster **Werkstroom maken**. Deze zijn gerelateerd aan de functionaliteit *bevestiging van ontvangst* die beschikbaar was in [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), maar die nu is afgeschaft. Deze werkstromen worden momenteel niet ondersteund.
> 
> - Workflow voor melding van vervaldatum levering
> - Workflow voor melding van ontvangen factuur
> - Workflow voor melding van mislukte productontvangstbon
> - Workflow voor meldingen van de afwijzing van een onbevestigde productontvangstbon

## <a name="creating-a-workflow"></a>Een werkstroom maken

Om een werkstroom te maken, gaat u naar Inkoop en sourcing &gt; Instellingen &gt; Werkstromen voor inkoop en sourcing en maakt u een nieuwe werkstroom door het type werkstroom te selecteren dat u wilt maken. 

U kunt in het werkstroomcanvas werkstroomelementen in de ontwerper slepen en de elementen in een stroom koppelen. De werkstroomelementen moeten worden geconfigureerd. Voor goedkeurings- en taakwerkstroomelementen kunt u configureren welke deelnemer de actie moet uitvoeren.

## <a name="types-of-participants"></a>Typen deelnemers

U kunt een goedkeuringsstap toewijzen aan de volgende groepen deelnemers.

| Gebruikersgroep | Beschrijving |
|---|---|
| Deelnemer | De goedkeuringsstap aan leden van een groep of rol toewijzen. |
| Hiërarchie | De goedkeuringsstap aan gebruikers in een specifieke organisatiehiërarchie toewijzen. |
| Werkstroomgebruiker | De goedkeuringsstap aan gebruikers van deze workflow toewijzen. |
| Wachtrij | De goedkeuringsstap aan een wachtrij voor werkitems toewijzen. |
| Gebruiker | Wijs de goedkeuringsstap aan specifieke gebruikers toe. |

## <a name="additional-resources"></a>Aanvullende resources

- [Bedrijfsprocesworkflows voor opdrachten tot inkoop definiëren](https://www.microsoft.com/download/details.aspx?id=101821)
- [Workflow voor opdrachten tot inkoop](purchase-requisitions-workflow.md)
- [Leveranciers onboarden](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
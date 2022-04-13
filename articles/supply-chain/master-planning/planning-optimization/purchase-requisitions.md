---
title: Opdrachten tot inkoop
description: In dit onderwerp wordt beschreven hoe opdrachten tot inkoop worden ondersteund in Planningsoptimalisatie.
author: t-benebo
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 0328342fbe322225a5ecb095d3b0165caa6d18d3
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469640"
---
# <a name="purchase-requisitions"></a>Opdrachten tot inkoop

[!include [banner](../../includes/banner.md)]

Via de hoofdplanning kunnen goedgekeurde opdrachten tot inkoop worden aangevuld. Daarom hoeven gebruikers voor het uitvoeren van opdrachten tot inkoop geen werkstroom te gebruiken om inkooporders te maken. In plaats daarvan kunnen opdrachten tot inkoop worden uitgevoerd door de hoofdplanning. Dankzij deze functionaliteit kan een opdracht tot inkoop een inkooporder, een overboekingsorder of een productieorder produceren, afhankelijk van de waarde van het **Geplande ordertype** die is ingesteld voor het gerelateerde product.

## <a name="enable-master-plans-to-include-requisitions"></a>Hoofdplannen inschakelen om opdrachten tot inkoop op te nemen

Voer de volgende stappen uit om tijdens de behoefteplanningsberekening voor een hoofdplan opdrachten tot inkoop op te nemen.

1. Ga naar **Hoofdplanning** \> **Instellingen** \> **Plannen** \> **Hoofdplannen**.
1. Maak of selecteer een hoofdplan.
1. Stel op het sneltabblad **Algemeen** de optie **Bestelaanvragen opnemen** in op *Ja*.
1. Herhaal stap 2 en 3 voor elk extra hoofdplan waarin u opdrachten tot inkoop wilt opnemen.

## <a name="approved-requisitions-time-fence"></a>Time fence goedgekeurde bestelaanvragen

Met de *time fence goedgekeurde bestelaanvragen* legt u vast hoe ver terug (in dagen) een hoofdplan de vraag omvat van goedgekeurde bestelaanvragen voor aanvulling. U kunt een time fence voor goedgekeurde bestelaanvragen instellen op zowel het niveau van de behoefteplanningsgroep als het niveau van het hoofdplan.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>De time fence voor goedgekeurde bestelaanvragen voor een behoefteplanningsgroep instellen

1. Ga naar **Hoofdplanning** \> **Instellen** \> **Behoefteplanning** \> **Behoefteplanningsgroepen**.
1. Maak of selecteer een behoefteplanningsgroep.
1. Stel in het veld **Time fence goedgekeurde bestelaanvragen (dagen)** op het sneltabblad **Overig** het aantal dagen in dat in de time fence moet worden opgenomen.
1. Herhaal stap 2 en 3 voor elke aanvullende behoefteplanningsgroep waarin u een time fence voor goedgekeurde bestelaanvragen wilt instellen.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>De time fence voor goedgekeurde bestelaanvragen voor afzonderlijke hoofdplannen instellen

Wanneer u een time fence voor goedgekeurde bestelaanvragen wilt instellen voor een afzonderlijk hoofdplan, wordt daarmee de instelling van de time fence voor elke toepasselijke behoefteplanningsgroep overschreven.

1. Ga naar **Hoofdplanning** \> **Instellingen** \> **Plannen** \> **Hoofdplannen**.
1. Maak of selecteer een hoofdplan.
1. Stel in het veld **Time fence goedgekeurde bestelaanvragen (dagen)** op het sneltabblad **Time fences in dagen** het aantal dagen in dat in de time fence moet worden opgenomen.
1. Herhaal stap 2 en 3 voor elk aanvullend hoofdplan waarin u een time fence voor goedgekeurde bestelaanvragen wilt instellen.

> [!IMPORTANT]
> **Binnenkort:** times fences voor goedgekeurde bestelaanvragen worden nog niet ondersteund voor Planningsoptimalisatie. Tot die tijd worden alle waarden die u invoert in het veld **Time fence goedgekeurde bestelaanvragen (dagen)** genegeerd.

## <a name="independent-supply-regardless-of-coverage-code"></a>Onafhankelijke levering, ongeacht behoefteplanningscode

Opdrachten tot inkoop worden altijd gedekt door onafhankelijke geplande orders, ongeacht de behoefteplanningscode. Dit gedrag zorgt voor duidelijke traceerbaarheid en werkstromen tussen opdrachten tot inkoop en aanvullingsorders.

### <a name="example-1"></a>Voorbeeld 1

Een product is zo ingesteld dat het een waarde voor **Behoefteplanningscode** van *Min/max* heeft. Het heeft de volgende statuswaarden voor voorraad en aanvraag:

- Hoeveelheid voorhanden voorraad = 10.
- Minimale voorraadhoeveelheid = 15.
- Maximale voorraadhoeveelheid = 20.
- Er bestaat een opdracht tot inkoop voor één stuk. De aangevraagde datum is vandaag.

Bij het uitvoeren van de hoofdplanning worden twee geplande orders gemaakt: een voor 10 stuks om de voorraad aan te vullen tot de maximumhoeveelheid en een voor één stuk om de opdracht tot inkoop aan te vullen.

### <a name="example-2"></a>Voorbeeld 2

Een product is zo ingesteld dat het een waarde voor **Behoefteplanningscode** van *Min/max* heeft. Het heeft de volgende statuswaarden voor voorraad en aanvraag:

- Hoeveelheid voorhanden voorraad = 17.
- Minimale voorraadhoeveelheid = 15.
- Maximale voorraadhoeveelheid = 20.
- Er bestaat een opdracht tot inkoop voor één stuk. De aangevraagde datum is vandaag.

Wanneer de hoofdplanning wordt uitgevoerd, wordt één geplande order voor één stuk gemaakt om de opdracht tot inkoop aan te vullen.

### <a name="example-3"></a>Voorbeeld 3

Een product is zo ingesteld dat het een waarde voor **Behoefteplanningscode** van *Periode* heeft en een periodelengte van zeven dagen. Het heeft de volgende statuswaarden voor voorraad, verkooporder en bestelaanvraag:

- Hoeveelheid voorhanden voorraad = 0.
- Er bestaat een verkooporder voor vijf stuks. De verwachte verzenddatum is vandaag plus één dag.
- Er bestaat een opdracht tot inkoop voor drie stuks. De aangevraagde datum is vandaag plus drie dagen.

Bij het uitvoeren van de hoofdplanning worden twee geplande orders gemaakt: een voor drie stuks om de opdracht tot in koop aan te vullen en een voor vijf stuks om de verkoopordervraag aan te vullen.

> [!NOTE]
> Nadat een geplande order die is vastgelegd voor een opdracht tot inkoop is gefiatteerd, bewaart de planningsengine de behoeftetracering voor de opdracht tot inkoop. Als later wordt geconstateerd dat in de gefiatteerde order een bepaalde hoeveelheid ontbreekt die nodig is om aan de opdracht tot inkoop te voldoen, wordt een nieuwe geplande order gemaakt voor het verschil.

Zie [Overzicht van opdrachten tot inkoop](../../procurement/purchase-requisitions-overview.md) voor meer informatie over opdrachten tot inkoop.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
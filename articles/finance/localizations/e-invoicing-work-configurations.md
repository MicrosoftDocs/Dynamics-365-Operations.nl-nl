---
title: Werken met configuraties
description: Dit onderwerp biedt een overzicht van het hoofdscenario voor het werken met ER-configuraties (Electronic Reporting) vanuit de werkruimte voor globalisatiefuncties.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4318399ee58ed54b29f8d360345b8930238ea9f2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371588"
---
# <a name="work-with-configurations"></a>Werken met configuraties

[!include [banner](../includes/banner.md)]

ER-configuraties (Electronic Reporting) zijn een van de hoofdsets van componenten van functies voor elektronische facturering. Een ER-configuratie bevat de instellingen van de bestandsstructuur en een set transformatieregels voor het op twee manieren omzetten van gegevens:

- **Configuratie export ER-indeling**: deze configuratie transformeert gegevens van de centrale interne structuur (ER-model) naar de elektronische bestandsindeling.
- **Configuratie import ER-indeling**: deze configuratie transformeert gegevens van de elektronische bestandsindeling naar de centrale interne structuur (ER-model).

Naast het genereren van uitgaande elektronische bestanden in de vooraf gedefinieerde indeling, worden ER-configuraties op grote schaal gebruikt om binnenkomende berichten van externe webservices als antwoorden te bekijken. Met deze functionaliteit kunt u configureerbare logica opbouwen om de resultaten van communicatie met externe kanalen te verkrijgen, deze resultaten (codes, berichten en logboeken) te converteren naar de door de gebruiker leesbare structuur en vervolgens die informatie door te sturen naar de clienttoepassing.

Als u ER-configuraties in uw elektronische factureringsfunctie wilt gaan gebruiken, moet u deze aan de functie koppelen en deze beschikbaar maken op het tabblad **Configuraties** voor de huidige functieversie. U kunt werken met een gekoppelde ER-configuratie door **Toevoegen**, **Verwijderen**, **Bewerken** of **Weergeven** te selecteren.

Voordat u een koppeling naar een ER-configuratie kunt toevoegen, moet de configuratie bestaan in de RCS-opslagplaats (Regulatory Configuration Service). Volg deze stappen om de ER-configuraties te bekijken die beschikbaar zijn in uw RCS-opslagplaats.

1. Meld u aan bij uw RCS-account.
2. Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.

Zie [Elektronische rapportage](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) voor informatie over het maken van een nieuwe ER-configuratie of het importeren van een bestaande ER-configuratie vanuit de algemene opslagplaats.

Als u een gekoppelde ER-configuratie wilt aanpassen, selecteert u **Bewerken** op het tabblad **Configuraties** voor de huidige elektronische factureringsfunctie. Er wordt automatisch een versie van de ER-configuratie gemaakt. Als de huidige versie niet is gemaakt door de actieve configuratieprovider, wordt een afgeleide versie gemaakt die uw configuratieprovider gebruikt. Als de huidige versie is gemaakt door de actieve configuratieprovider, wordt een nieuwe versie gemaakt. In beide gevallen kunt u de versie die wordt gemaakt wijzigen en vervolgens automatisch alle vereiste updates doen.

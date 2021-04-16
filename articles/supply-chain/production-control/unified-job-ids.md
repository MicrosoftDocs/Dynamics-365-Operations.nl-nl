---
title: Geïntegreerde nummerreeks voor taak-id's
description: Deze functie biedt één uniforme nummerreeks die taak-id's genereert voor de modules Productiebeheer, Productie-uitvoering en Tijd en aanwezigheid.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824936"
---
# <a name="unified-number-sequence-for-job-ids"></a>Geïntegreerde nummerreeks voor taak-id's

[!include [banner](../includes/banner.md)]

Deze functie biedt één uniforme nummerreeks die taak-id's genereert voor de modules Productiebeheer, Productie-uitvoering en Tijd en aanwezigheid. Voorheen kon u voor elk van deze modules een andere nummerreeks kiezen, wat kon leiden tot conflicterende taak-id's als twee of meer van deze reeksen een identieke indeling gebruikten. Een dergelijk conflict kan leiden tot gegevensbeschadiging.

## <a name="turn-on-this-feature-for-your-system"></a>Deze functie inschakelen voor uw systeem

Als de functie die in dit onderwerp wordt beschreven, nog niet in het systeem aanwezig is, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Geïntegreerde nummerreeks voor taak-id's* in.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>De geïntegreerde nummerreeks voor taak-id's instellen

Nadat u deze functie hebt ingeschakeld, worden de bestaande instellingen voor de nummerreeks van **Taakidentificatie** op de parameterpagina's voor de modules Productiebeheer, Productie-uitvoering en Tijd en aanwezigheid afgeschaft en wordt een nieuw veld **Geïntegreerde taak-id** toegevoegd. De waarde **Geïntegreerde taak-id** wordt gedeeld door alle drie de modules, zodat alle modules naar dezelfde nummerreeks verwijzen. Taak-id's zullen daarom uniek zijn in alle drie de modules en er zal nooit een conflict optreden.

De geïntegreerde nummerreeks voor taak-id's instellen:

1. Schakel de functie in zoals beschreven in de vorige sectie.
1. Identificeer de nummerreeks die u wilt gebruiken voor uw geïntegreerde taak-id's of maak een nieuwe. Zie [Overzicht van nummerreeksen](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) voor meer informatie.
1. Ga naar de pagina **Parameters van productiebeheer**, **Parameters van Productie-uitvoering** of **Parameters in Tijd en aanwezigheid**. Het maakt niet uit welke u kiest, want wanneer u deze instelling op een van deze pagina's maakt, worden alle andere pagina's automatisch bijgewerkt.
1. Open het tabblad **Nummerreeksen** op uw geselecteerde pagina met parameters.
1. Wijs de **nummerreekscode** die u eerder hebt geïdentificeerd toe aan de rij **Geïntegreerde taak-id's** van het raster.

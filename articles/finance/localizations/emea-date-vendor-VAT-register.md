---
title: Datum van btw-register leverancier
description: Dit onderwerp biedt informatie over de functie voor het inschakelen van de datum van het btw-register voor leveranciers.
author: anasyash
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: global
ms.author: anasyash
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 882d5a8718d819cff80bfa5b86e054a39e9db159
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7992059"
---
# <a name="date-of-vendor-vat-register"></a>Datum van btw-register leverancier

In Microsoft Dynamics 365 Finance versie 10.0.24 is een nieuw veld **Datum van btw-register voor leveranciers** beschikbaar voor leveranciersfacturen. Dit veld geeft de datum van de belastbare levering voor een inkoop aan.

Als u het nieuwe veld wilt inschakelen, gaat u naar het werkgebied **Functiebeheer**, selecteert u de functie **Datum van btw-register leverancier op leveranciersfacturen inschakelen** en selecteert u **Nu inschakelen**.

Binnenkomende facturen van uw leveranciers kunnen twee datums hebben: de datum waarop de leverancier de factuur heeft afgegeven en de datum van de belastbare levering (dat wil zeggen de datum waarop de leverancier de belasting toegevoegde waarde [btw] in rekening heeft gebracht). In sommige scenario's kunnen deze twee datums verschillen.

U kunt het inkomende btw-bedrag voor een inkoopfactuur aftrekken en die factuur later op btw-aangiften opnemen op een datum die verschilt van beide eerder genoemde datums. Deze datum wordt bepaald door de lokale wetgevingregels over uitgestelde inkomende btw-inhouding voor bepaalde scenario's. Dit verschilt per land of regio.

Bepaalde btw-rapporten, zoals het rapport [Btw-controleoverzicht](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) in de Tsjechische Republiek, vereisen dat de datum van de belastbare levering voor een inkoopdocument wordt gerapporteerd. Deze datum moet worden gerapporteerd zodat de belastingdienst de btw-aangifte tussen partijen kan afstemmen.

In Finance kunt u datums definiëren in de volgende velden:

- **Factuurdatum**: de datum waarop de factuur is uitgegeven door de leverancier.
- **Datum van het btw-register**: de datum waarop het btw-bedrag op de inkoopfactuur wordt ingehouden.
- **Datum van btw-register leverancier**: de datum van de belastbare levering van de leverancier.
- **Ontvangstdatum document**: de datum waarop u de factuur hebt ontvangen.

Deze velden staan op de volgende pagina's:

- Leveranciersfactuur
- Leveranciersfactuurregister
- Goedkeuring leveranciersfactuur
- Leveranciersfacturenjournaal

Nadat de leveranciersfactuur is geboekt, kunt u de datums controleren op de pagina's **Facturenjournaal** en **Leverancierstransacties**.

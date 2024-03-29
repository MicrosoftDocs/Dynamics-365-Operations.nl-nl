---
title: Uitbreidbaarheid van Planningsoptimalisatie
description: In dit artikel worden de uitbreidbaarheidsscenario's beschreven die in Planningsoptimalisatie worden ondersteund.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d649110959e6bcfdaeb32dd53c55dbc446ed1be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857539"
---
# <a name="planning-optimization-extensibility"></a>Uitbreidbaarheid van Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

In dit artikel worden de uitbreidbaarheidsscenario's beschreven die in Planningsoptimalisatie worden ondersteund. Deze mogelijkheden zijn beschikbaar vanaf Microsoft Dynamics 365 Supply Chain Management versie 10.0.13.

## <a name="custom-processing-when-master-planning-is-completed"></a>Aangepaste verwerking wanneer de hoofdplanning wordt voltooid

In het meest gangbare uitbreidbaarheidsscenario in Planningsoptimalisatie wordt een aangepaste verwerking uitgevoerd nadat het plan is bijgewerkt. U wilt bijvoorbeeld een kolom toevoegen aan de tabel met geplande orders (`ReqPO`) of statistische informatie afleiden uit het gegenereerde plan. Het belangrijkste uitbreidbaarheidspunt dat deze scenario's mogelijk maakt, is de methode `jobCompletedSuccessfully` in de klasse `MpsMasterPlanningEvents`.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Hier is een voorbeeld van een uitbreiding waarmee een aangepast veld `CstmOrderPriority` wordt ingesteld voor de geplande order.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Wanneer u aangepaste logica toevoegt, moet u rekening houden met de volgende beperkingen en best practices:

- De methode `jobCompletedSuccessfully` wordt aangeroepen buiten het transactiebereik. Het plan is dus al zichtbaar voor de gebruiker wanneer de aangepaste logica wordt uitgevoerd. Als met uw aanpassing extra velden in geplande orders worden ingesteld, is het belangrijk dat u gebruikers laat weten dat de waarden van die velden uiteindelijk consistent zullen zijn (met andere woorden, ze zijn mogelijk direct verouderd nadat een planningstaak is voltooid).
- Er kan een andere hoofdplanningstaak worden gestart wanneer de methode `jobCompletedSuccessfully` wordt aangeroepen. De nieuwe taak kan van invloed zijn op het volledige plan of een deel van het plan. Met de nieuwe taak kunnen dezelfde geplande orders of behoeftetransacties worden bijgewerkt of verwijderd als de orders of transacties die zijn gemaakt of bijgewerkt als onderdeel van de planningstaak die is verwerkt in `jobCompletedSuccessfully`. Uitzonderingen met updateconflicten moeten worden verwerkt wanneer deze gebeurtenis wordt uitgebreid.
- Gebruik niet één transactiebereik als u deze methode uitbreidt. Een uitvoering van één hoofdplanning kan miljoenen behoeftetransacties en honderdduizenden geplande orders produceren. Als al deze transacties en geplande orders worden verwerkt in het bereik van één transactie, treden er veel SQL-vergrendelingen op en worden andere planningsprocessen geblokkeerd. Als de transactie een lange tijd wordt aangehouden, worden er bovendien 'ghost-records' in de SQL-database gemaakt. Ghost-records hebben een negatieve invloed op elk proces in het systeem.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
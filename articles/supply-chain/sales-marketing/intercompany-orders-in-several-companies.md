---
title: Het maken van intercompany-inkooporders en -verkooporders in diverse bedrijven
description: In dit onderwerp wordt uitgelegd hoe u intercompany-inkooporders of -verkooporders in diverse bedrijven maakt
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5d756a82abb7e7b19080128353d863f29837fc5b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548189"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Het maken van intercompany-inkooporders en -verkooporders in diverse bedrijven

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management kan meer dan alleen één productiebedrijf en diverse verkoopbedrijven afhandelen. Het is mogelijk om zowel handelsmaatschappijen als productiebedrijven voor intercompany in te stellen.

Als een bepaald artikel door meerdere bedrijven kan worden geleverd, bent u vrij om te kiezen voor een bedrijf. De updates worden ook verwerkt als één enkele verkooporder wordt omgezet in meerdere inkooporders.

Op dezelfde manier waarop u automatisch één intercompany-inkooporder maakt, kunt u een verkooporder in uw bedrijf maken en de order door verschillende intercompany-leveranciers laten afhandelen door meerdere intercompany-inkooporders te maken. Microsoft Dynamics 365 Supply Chain Management maakt automatisch intercompany-verkooporders bij de leveranciers.

Hiervoor moeten alle bedrijven zijn ingesteld als handelsrelaties. De bedrijven van de leveranciers moeten in Microsoft Dynamics 365 Supply Chain Management zijn ingesteld als intercompany-leveranciers en moeten de primaire leverancier voor het desbetreffende artikel zijn. Op de verkooporder moet u in de **koptekstweergave** het veld **Intercompany-orders automatisch maken** en het veld **Rechtstreekse levering** op het sneltabblad **Intercompany-instellingen** selecteren. Dit is de standaardinstelling.

U maakt de verkoopregels zoals gebruikelijk. Als u de record afsluit, wordt er een melding weergegeven met het bericht dat de intercompany-inkooporders en intercompany-verkooporders zijn gemaakt. De melding bevat koppelingen naar de nieuwe orders. Als u de intercompany-verkooporders wilt bekijken die in de bedrijven van uw leveranciers zijn gemaakt, opent u de oorspronkelijke verkooporder en selecteert u vervolgens op het tabblad **Algemeen** in de groep **Verwante informatie** de optie **Referenties**.

Als u de intercompany-verkooporders voor de leveranciers opent, dan ziet u dat in Microsoft Dynamics 365 Supply Chain Management voor iedere leverancier automatisch het oorspronkelijke verkoopordernummer en het intercompany-inkoopordernummer zijn ingevuld.

Ook als u de intercompany-verkooporders voor de leveranciers opent, ziet u dat in Microsoft Dynamics 365 Supply Chain Management voor iedere leverancier automatisch het oorspronkelijke verkoopordernummer en het intercompany-inkoopordernummer zijn ingevuld.

> [!NOTE]
> Als de in bestelling zijnde artikelen wel bij een van de intercompany-leveranciers maar niet bij de andere leverancier verkrijgbaar zijn, maakt Microsoft Dynamics 365 Supply Chain Management intercompany-orders voor de leverancier die het artikel kan leveren, maar stopt met het maken van de order voor de andere leverancier. Er verschijnt een melding wanneer dit gebeurt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

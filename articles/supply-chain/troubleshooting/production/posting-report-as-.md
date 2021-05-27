---
title: Fout wanneer het Gereedmeldingsjournaal wordt geboekt
description: Wanneer u het Gereedmeldingsjournaal boekt, ontvangt u een foutbericht waarin wordt staat dat de bestelde hoeveelheid niet kan worden verminderd.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026394"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Fout wanneer het Gereedmeldingsjournaal wordt geboekt

KB-nummer: 4612891

## <a name="symptoms"></a>Symptomen

Wanneer u het **Gereedmeldingsjournaal** boekt, treedt er een fout op en wordt het volgende foutbericht weergegeven:

> Bestelde hoeveelheid kan niet worden verminderd omdat er onvoldoende openstaande voorraadtransacties met de status Besteld zijn. De artikelen zijn Ingekocht, Ontvangen of Geregistreerd.

Deze fout treedt alleen op als het veld **Slechte hoeveelheid** is ingesteld op de eerste regel van het **Gereedmeldingsjournaal** en het veld **Goede hoeveelheid** op de laatste regel is ingesteld. Als het veld **Slechte hoeveelheid** is ingesteld op de laatste regel, treedt er geen fout op.

## <a name="resolution"></a>Oplossing

Om deze fout te voorkomen opent u de pagina **Parameters van productiebeheer** en stelt u vervolgens op het tabblad **Algemeen** de optie **Resterende hoeveelheid verhogen met fouthoeveelheid** in op *Ja*.

---
title: Werkgebied voor samenwerkingsfacturering van leveranciers
description: In dit onderwerp wordt beschreven hoe u leveranciersfacturen kunt weergeven en facturen indient vanuit het samenwerkingswerkgebied voor leveranciersfacturering.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 2368fae3913f67d9d2ce0bbe6b2e0bee7968bb15
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="vendor-collaboration-invoicing-workspace"></a>Werkgebied voor samenwerkingsfacturering van leveranciers

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u leveranciersfacturen kunt weergeven en facturen indient vanuit het samenwerkingswerkgebied voor leveranciersfacturering.

Het werkgebied **Leverancierssamenwerkingsfacturen** kan worden gebruikt om leveranciersfactuurinformatie weer te geven en facturen te verzenden naar Microsoft Dynamics 365 for Finance and Operations met workflowmogelijkheden.


<a name="vendor-collaboration-invoicing-workspace"></a>Werkgebied voor samenwerkingsfacturering van leveranciers
----------------------------------------

### <a name="summary-tiles"></a>Overzichtstegels

De tegels **Overzicht** geven een overzicht van de facturen voor de geselecteerde leverancier. U kunt facturen op hun status weergeven.
-   Conceptfacturen zijn niet ingediend bij de workflow.
-   De verzonden, niet-goedgekeurde facturen zijn facturen die de leverancier heeft ingediend, maar die niet zijn geboekt in Finance and Operations.
-   Goedgekeurde, niet-betaalde facturen zijn facturen die zijn geboekt in Finance and Operations maar die nog niet volledig zijn betaald.
-   Betaalde facturen zijn facturen die volledig zijn betaald in Finance and Operations.

Klik op een tegel om een gefilterde weergave van de pagina **Facturenlijst** te openen.

### <a name="tabular-lists"></a>Lijsten in tabelvorm

In de sectie **Lijsten in tabelvorm** wordt de factureringsstatus onderverdeeld als de overzichtstegels: Concept en Verzonden, niet-goedgekeurde lijsten. In de Conceptstatus kan een factuur naar de workflow zijn verzonden of zijn verwijderd. De laatste lijst in tabelvorm is een optie om facturen te zoeken. U kunt filteren tijdens het zoeken, zodat het zoeken sneller verloopt.

### <a name="all-vendor-invoices-list-page"></a>Lijstpagina met alle leveranciersfacturen

U kunt alle geboekte en niet-geboekte leveranciersfacturen weergeven op de lijstpagina **Samenwerkingsfacturen van leveranciers**. Gebruik deze lijstpagina om de betalingsstatus van de facturen weer te geven. De betalingsstatussen zijn Niet-geboekt, Onbetaald, Gedeeltelijk betaald en Volledig betaald.
Een nieuwe factuur maken van een inkooporder

U kunt een nieuwe leveranciersfactuur maken door **Nieuwe** actie te selecteren in het werkgebied **Samenwerkingsfacturering van leveranciers**. Het inkoopordernummer en het factuurnummer moeten door de leverancier worden opgegeven. Standaard worden alle regels van de inkooporder van de leverancier op de nieuwe factuur weergegeven. Gegevens over de hoeveelheid en de kostprijs kunnen worden bewerkt vóór het verzenden van de leveranciersfactuur naar de workflow. U kunt bestanden, notities, afbeeldingen en URL's aan een factuur koppelen voordat deze wordt verzenden.

Zie voor meer informatie [Leverancierssamenwerking met externe leveranciers](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md).





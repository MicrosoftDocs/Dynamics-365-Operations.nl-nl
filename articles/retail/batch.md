---
title: Verbeterde afhandeling van artikelen met batchtracering
description: In dit onderwerp worden de verbeteringen beschreven die zijn aangebracht in de batchafhandeling van artikelen met batchtracering tijdens het proces voor boeken van detailhandeloverzichten.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617384"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Verbeterde afhandeling van artikelen met batchtracering

In Microsoft Dynamics 365 for Retail Point of Sale (POS) kunnen op het moment van verkoop geen batchnummers worden vastgelegd voor artikelen met batchtracering. Voor specifieke configuraties wanneer de verkoop wordt geboekt in het hoofdkantoor via klantorders of het boeken van overzichten, verwacht het Microsoft Dynamics-systeem dat er geldige batchnummers zijn voor artikelen met batchtracering en dat deze worden gebruikt bij de facturering.

Als er geldige batchnummers beschikbaar zijn voor producten, worden deze gebruikt door de factureringsprocessen voor klantorder en verkooporder op basis van de overzichtboekingen. Anders kan het factureringsproces voor de klantorder niet worden geboekt en ontvangt de POS-gebruiker een foutmelding. De overzichtboeking gaat vervolgens naar een foutstatus. Deze foutstatus vindt ook plaats wanneer negatieve voorraad is ingeschakeld voor de producten.

Verbeteringen in Microsoft Dynamics for Retail versie 10.0.4 en later zorgen dat wanneer negatieve voorraad is ingeschakeld voor artikelen met batchtracering, facturering van klantorder en verkooporder via overzichtboekingen niet worden geblokkeerd voor deze artikelen als de voorraad 0 (nul) is of er geen batchnummer beschikbaar is. Bij de nieuwe functionaliteit wordt een standaard batch-id gebruikt voor de verkoopregels wanneer er geen batchnummers beschikbaar zijn.

Als u de standaard batch-id wilt definiëren die wordt gebruikt voor klantorders, gaat u op de pagina **Detailhandelparameters** naar het tabblad **Klantorders** en stelt u op het sneltabblad **Order** het veld **Standaard batch-id** in.

Als u de standaard batch-id wilt definiëren die wordt gebruikt voor de facturering van verkooporders op basis van overzichtboekingen, gaat u op de pagina **Detailhandelparameters** naar het tabblad **Boeking** en stelt u op het sneltabblad **Voorraad bijwerken** het veld **Standaard batch-id** in.

> [!NOTE]
> Deze functionaliteit is alleen beschikbaar wanneer geavanceerde magazijnfuncties zijn ingeschakeld voor het specifieke winkelmagazijn en de artikelen. In een latere versie wordt de functionaliteit ook ondersteund voor scenario's waarbij geavanceerd magazijnbeheer niet wordt gebruikt.

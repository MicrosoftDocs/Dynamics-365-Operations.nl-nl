---
title: Verbeterde afhandeling van artikelen met batchtracering
description: In dit onderwerp worden de verbeteringen beschreven die zijn aangebracht in de batchafhandeling van artikelen met batchtracering tijdens het proces voor boeken van overzichten.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: ef946df30c68373b83660fce98b472dc94b42719
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989588"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Verbeterde afhandeling van artikelen met batchtracering


[!include [banner](includes/banner.md)]


In Point of Sale (POS) kunnen op het moment van verkoop geen batchnummers worden vastgelegd voor artikelen met batchtracering. Voor specifieke configuraties wanneer de verkoop wordt geboekt in het hoofdkantoor via klantorders of het boeken van overzichten, verwacht het Microsoft Dynamics-systeem dat er geldige batchnummers zijn voor artikelen met batchtracering en dat deze worden gebruikt bij de facturering.

Als er geldige batchnummers beschikbaar zijn voor producten, worden deze gebruikt door de factureringsprocessen voor klantorder en verkooporder op basis van de overzichtboekingen. Anders kan het factureringsproces voor de klantorder niet worden geboekt en ontvangt de POS-gebruiker een foutmelding. De overzichtboeking gaat vervolgens naar een foutstatus. Deze foutstatus vindt ook plaats wanneer negatieve voorraad is ingeschakeld voor de producten.

Verbeteringen in Retail versie 10.0.4 en later zorgen dat wanneer negatieve voorraad is ingeschakeld voor artikelen met batchtracering, facturering van klantorder en verkooporder via overzichtboekingen niet worden geblokkeerd voor deze artikelen als de voorraad 0 (nul) is of er geen batchnummer beschikbaar is. Bij de nieuwe functionaliteit wordt een standaard batch-id gebruikt voor de verkoopregels wanneer er geen batchnummers beschikbaar zijn.

Als u de standaard batch-id wilt definiëren die wordt gebruikt voor klantorders, gaat u op de pagina **Commerce-parameters** naar het tabblad **Klantorders** en stelt u op het sneltabblad **Order** het veld **Standaard batch-id** in.

Als u de standaard batch-id wilt definiëren die wordt gebruikt voor de facturering van verkooporders op basis van overzichtboekingen, gaat u op de pagina **Commerce-parameters** naar het tabblad **Boeking** en stelt u op het sneltabblad **Voorraad bijwerken** het veld **Standaard batch-id** in.

> [!NOTE]
> Deze functionaliteit is alleen beschikbaar wanneer geavanceerde magazijnfuncties zijn ingeschakeld voor het specifieke winkelmagazijn en de artikelen. In een latere versie wordt de functionaliteit ook ondersteund voor scenario's waarbij geavanceerd magazijnbeheer niet wordt gebruikt.

> [!NOTE]
> Ondersteuning voor de verbeterde verwerking van artikelen met batchtracering tijdens overzichtsboekingen voor niet-geavanceerde magazijnbeheerscenario's is geïntroduceerd in Retail versie 10.0.5.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
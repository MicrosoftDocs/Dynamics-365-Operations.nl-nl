---
title: De status van een experiment controleren
description: In dit onderwerp wordt uitgelegd welke status een experiment heeft in de levenscyclus van het experiment in Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5ae29fe5ac49d92c261c59d115664b50e87880a0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965097"
---
# <a name="review-the-status-of-an-experiment"></a>De status van een experiment controleren
Er zijn diverse stappen betrokken bij het instellen en uitvoeren van een experiment in Dynamics 365 Commerce. Zie [Experimenten in Dynamics 365 Commerce](experimentation-overview.md) voor informatie over de levenscyclus van experimenten.

Selecteer **Experimenten** in het linkernavigatievenster in Commerce Site Builder als u wilt weten waar een experiment zich in de levenscyclus bevindt. Er wordt een lijst met experimenten weergegeven met de status van elk experiment in zowel Commerce als de service van derden die wordt gebruikt om experimenten te maken, variaties toe te wijzen en gegevens te analyseren.

In de kolom **Commerce-status** kunnen de volgende waarden worden weergegeven. 
- **Concept**: het experiment is verbonden met een pagina of fragment in Commerce en wordt bewerkt.
- **Gepubliceerd**: de experimentvariaties zijn klaar om op uw website te worden weergegeven. Als het experiment wordt uitgevoerd in de service van derden, zien de gebruikers van de website een variatie op de pagina of het fragment zoals deze is geselecteerd door de service van derden.
- **Niet-gepubliceerd**: het experiment is niet meer beschikbaar op uw website. Zelfs als het experiment wordt uitgevoerd in de service van derden, zien de gebruikers van de website alleen de standaardversie van de pagina of het fragment.
- **Voltooid**: het experiment is uitgevoerd en er is een variatie gepromoveerd voor gebruik op de live site voor alle websitegebruikers.

Zo ook kunnen in de kolom **Status van derden** de volgende waarden worden weergegeven om aan te geven welke status de experimenten hebben in de service van derden.
- **Concept**: het experiment is ingesteld in de service van derden, maar is niet gestart.
- **Actief**: het experiment is gestart in de service van derden en er worden gegevens verzameld.
- **Onderbroken**: het experiment is onderbroken en er worden geen gegevens verzameld. U moet het experiment hervatten om gegevens opnieuw te verzamelen.
- **Gearchiveerd**: het experiment is uitgevoerd en is gecatalogiseerd in de service van derden voor toekomstige naslag.

In het onderstaande diagram ziet u beide sets statuswaarden en de relatie tussen deze twee sets.

[ ![Statuswaarden van experimenten](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)

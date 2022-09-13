---
title: Documenten in behandeling voor boekhouding
description: In dit artikel wordt beschreven hoe u de functionaliteit gebruikt voor de pagina Documenten in behandeling voor boekhouding.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: e915c248abd1c842f8f01490a49db9b824644a29
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9424361"
---
# <a name="documents-pending-accounting"></a>Documenten in behandeling voor boekhouding

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In dit artikel wordt beschreven hoe u de functionaliteit gebruikt voor de pagina **Documenten in behandeling voor boekhouding**.

In Microsoft Dynamics 365 Finance 10.0.30 is de functie **Verbeterde prestaties van boekhoudraamwerk voor brondocument** beschikbaar. Deze functie verbetert de boekingsprocessen voor documentboekingen die voor brondocument zijn ingeschakeld, te beginnen met het boekingsproces voor vrije-tekstfacturen.

Wanneer deze functie is ingeschakeld, wordt het boeken van het subadministratiedocument afzonderlijk uitgevoerd van het genereren van boekhouding of het *journaliseringsproces* waarmee de volledige boekhoudingsdetails worden gemaakt die worden overgeboekt naar het grootboek. In het boekingsproces voor vrije-tekstfacturen wordt bijvoorbeeld de klantfactuur in de module **Klanten** geregistreerd voordat de volledige boekhouding wordt gegenereerd. Door deze verbeterde prestatiefunctie kunnen klantfacturen sneller worden geregistreerd als het genereren van boekhouding vertraagd is.

De volgende knoppen zijn beschikbaar op de pagina **Documenten in behandeling voor boekhouding**.

- **Boekhouding genereren**: een document indienen dat momenteel wacht op het genereren van een rekening voor journalisering.
- **Verdelingen weergeven**: de boekhoudingsverdelingen weergeven voor een geselecteerd document in de lijst.
- **Foutlogboek weergeven**: foutberichtdetails weergeven die bestaan voor een document waarvoor de boekhoudstatus fouten vermeldt. U kunt dezelfde foutberichtdetails weergeven door de koppeling **Foutlogboek** op de documentregel te selecteren.

Het genereren van de boekhouding wordt uitgevoerd door een geautomatiseerd achtergrondproces met de naam **Verwerkfunctie van boekhoudraamwerk**. Zie [Procesautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md) voor meer informatie over de instellingen en de configuratie van alle procesautomatiseringen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

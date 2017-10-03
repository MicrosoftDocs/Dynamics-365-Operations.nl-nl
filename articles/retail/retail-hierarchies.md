---
title: "Detailhandelhiërarchieën"
description: "In dit artikel worden detailhandelhiërarchieën in Microsoft Dynamics 365 for Retail beschreven."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: a425680fb4d2e2da8d96acd843694ea9a07e29f0
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017

---

# <a name="retail-hierarchies"></a>Detailhandelhiërarchieën

[!include[banner](includes/banner.md)]


In dit artikel worden detailhandelhiërarchieën in Microsoft Dynamics 365 for Retail beschreven.

U kunt één detailhandelcategoriehiërarchie maken om alle producten die u via uw detailhandelkanalen verkoopt, in te delen. U kunt detailhandelproducthiërarchieën gebruiken voor het categoriseren of groeperen van producten. Deze producten kunt u vervolgens gebruiken om productassortimenten en klantloyaliteitsprogramma's te maken. U kunt tevens productkenmerken en -eigenschappen toewijzen, een prijsstructuur toewijzen, de producten in productpromoties opnemen en producten gebruiken voor rapportages. U kunt één detailhandelcategoriehiërarchie maken die alle producten en categorieën in uw organisatie vertegenwoordigt. U kunt deze categoriehiërarchie vervolgens voor meerdere doeleinden gebruiken. Het is ook mogelijk om meerdere detailhandelcategoriehiërarchieën te maken voor speciale doeleinden, zoals productpromoties. Als u een detailhandelproducthiërarchie maakt, moet u een type categoriehiërarchie toewijzen om het doel van de categoriehiërarchie te identificeren. Er wordt bijvoorbeeld alleen naar producthiërarchieën verwezen die het type **Detailhandelnavigatiehïerarchie** hebben toegewezen gekregen wanneer u online of in een verkooppunt in producten op categorie bladert.

## <a name="retail-hierarchy-types"></a>Typen detailhandelhiërarchie
In de volgende tabel worden de beschikbare typen detailhandelcategoriehiërarchieën en het algemene doel van de afzonderlijke typen weergegeven.

| Type categoriehiërarchie       | Doel                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Producthiërarchie detailhandel      | Gebruik dit hiërarchietype om de algemene producthiërarchie voor uw organisatie te definiëren. U kunt dit hiërarchietype gebruiken voor merchandising, prijzen en promoties, rapportage en assortimentplanning. Er kan aan dit hiërarchietype slechts één detailhandelproducthiërarchie worden toegewezen.                                       |
| Aanvullende detailhandelhiërarchie | Gebruik dit hiërarchietype voor eventuele aanvullende detailhandelcategoriehiërarchieën die u wilt maken. In de lente is er bijvoorbeeld een promotie voor zwemkleding. Daarom neemt u uw zwemkledingproducten op in een aparte categoriehiërarchie en past u speciale promotieprijzen toe op de verschillende productcategorieën. |
| Detailhandelnavigatiehiërarchie   | Gebruik dit hiërarchietype om producten te groeperen en organiseren in categorieën zodat u online of in POS in producten kunt bladeren.                                                                                                                                                                                       |

U kunt gebruikmaken van een detailhandelcategoriehiërarchie voor het structureren van uw producten, zodat u productkenmerken en -eigenschappen kunt instellen en onderhouden op het categorieniveau. Deze kenmerken en eigenschappen omvatten instellingen voor productdimensies en POS-instellingen. Alle producten die u aan de categorieën toewijst, nemen de kenmerken en eigenschappen die u definieert automatisch over. Het is ook mogelijk om de eigenschapinstellingen van een product naar meerdere producten tegelijk in een geselecteerde categorie te kopiëren.




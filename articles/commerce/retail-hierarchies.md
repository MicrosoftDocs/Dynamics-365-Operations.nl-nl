---
title: Commerce-hiërarchieën
description: In dit artikel worden hiërarchieën in Dynamics 365 Commerce beschreven.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8f7e4d01970f459f66934fe434ec7307104b39b2
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895276"
---
# <a name="commerce-hierarchies"></a>Commerce-hiërarchieën

[!include [banner](includes/banner.md)]

In dit artikel worden hiërarchieën in Dynamics 365 Commerce beschreven.

U kunt één categoriehiërarchie maken om de producten in te delen die u via uw kanalen verkoopt. U kunt producthiërarchieën gebruiken voor het categoriseren of groeperen van producten. Deze producten kunt u vervolgens gebruiken om productassortimenten en klantloyaliteitsprogramma's te maken. U kunt tevens productkenmerken en -eigenschappen toewijzen, een prijsstructuur toewijzen, de producten in productpromoties opnemen en producten gebruiken voor rapportages. U kunt één categoriehiërarchie maken die alle producten en categorieën in uw organisatie vertegenwoordigt. U kunt deze categoriehiërarchie vervolgens voor meerdere doeleinden gebruiken. Het is ook mogelijk om meerdere categoriehiërarchieën te maken voor speciale doeleinden, zoals productpromoties. Als u een producthiërarchie maakt, moet u een type categoriehiërarchie toewijzen om het doel van de categoriehiërarchie te identificeren. Er wordt bijvoorbeeld alleen naar producthiërarchieën verwezen die het type **Commerce-navigatiehïerarchie** hebben toegewezen gekregen wanneer u online of in een verkooppunt in producten op categorie bladert.

## <a name="hierarchy-types"></a>Hiërarchietypen

In de volgende tabel worden de beschikbare typen categoriehiërarchieën en het algemene doel van de afzonderlijke typen weergegeven.

| Type categoriehiërarchie       | Doel |
|-------------------------------|---------|
| Producthiërarchie      | Gebruik dit hiërarchietype om de algemene producthiërarchie voor uw organisatie te definiëren. U kunt dit hiërarchietype gebruiken voor merchandising, prijzen en promoties, rapportage en assortimentplanning. Er kan aan dit hiërarchietype slechts één producthiërarchie worden toegewezen. |
| Aanvullende hiërarchie | Gebruik dit hiërarchietype voor eventuele aanvullende categoriehiërarchieën die u wilt maken. In de lente is er bijvoorbeeld een promotie voor zwemkleding. Daarom neemt u uw zwemkledingproducten op in een aparte categoriehiërarchie en past u speciale promotieprijzen toe op de verschillende productcategorieën. |
| Navigatiehiërarchie   | Gebruik dit hiërarchietype om producten te groeperen en organiseren in categorieën zodat u online of in POS in producten kunt bladeren. |

U kunt gebruikmaken van een categoriehiërarchie voor het structureren van uw producten, zodat u productkenmerken en -eigenschappen kunt instellen en onderhouden op het categorieniveau. Deze kenmerken en eigenschappen omvatten instellingen voor productdimensies en POS-instellingen. Alle producten die u aan de categorieën toewijst, nemen de kenmerken en eigenschappen die u definieert automatisch over. Het is ook mogelijk om de eigenschapinstellingen van een product naar meerdere producten tegelijk in een geselecteerde categorie te kopiëren.

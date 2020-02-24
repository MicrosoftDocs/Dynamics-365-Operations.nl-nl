---
title: Een nieuwe producthiërarchie maken
description: In dit onderwerp wordt beschreven hoe u een nieuwe producthiërarchie maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 73cecb0c6aacebf5c6fcf8a0edbc7513b3ce175d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001893"
---
# <a name="create-a-new-product-hierarchy"></a>Een nieuwe producthiërarchie maken


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een nieuwe producthiërarchie maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Dynamics 365 Commerce ondersteunt meerdere detailhandelkanalen. Deze detailhandelskanalen zijn o.a. online winkels, call centers en winkels (ook fysieke winkels genoemd). Iedere Retail-winkelkanaal kan zijn eigen betalingsmethoden, prijsgroepen, verkooppuntkassa's (POS), inkomsten- en uitgavenrekeningen en personeel hebben. U moet al deze elementen instellen voordat u een Retail-winkelkanaal kunt maken. 

Gebruik een Commerce-producthiërarchietype om de algemene producthiërarchie voor uw organisatie te definiëren. U kunt een Commerce-producthiërarchie gebruiken voor merchandising, prijzen en promoties, rapportage en assortimentplanning. Er kan per organisatie slechts één Commerce-producthiërarchie worden toegewezen.

## <a name="create-and-configure-a-product-hierarchy"></a>Een producthiërarchie maken en configureren

Voer de volgende stappen uit om een Commerce-producthiërarchie te maken en te configureren.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Commerce-producthiërarchie**.
1. Als er nog geen hiërarchie bestaat, selecteert u in het **actievenster** de optie **Nieuw** om de basis van de hiërarchie te maken.
1. Onder **Algemeen**:
    1. Voer in het vak **Naam** een naam in.
    1. Voer in het vak **Omschrijving** een beschrijving in.
    1. Voer in het vak **Beschrijvende naam** een beschrijvende naam in.
    1. Stel **Actief** in op **Ja**.

## <a name="add-hierarchy-nodes"></a>Hiërarchieknooppunten toevoegen

Voer de volgende stappen uit om hiërarchieknooppunten toe te voegen.

1. Klik in het actievenster op **Categoriehiërarchie**.
1. Selecteer het bovenliggende knooppunt waaraan u een nieuwknoop punt wilt toevoegen en selecteer **Nieuw categorieknooppunt**.
1. Geef in de sectie **Algemeen** een **Naam**, **Beschrijving**, **Beschrijvende naam** en **Trefwoorden** op.
1. Onder **Algemeen**:
    1. Voer in het vak **Naam** een naam in.
    1. Voer in het vak **Omschrijving** een beschrijving in.
    1. Voer in het vak **Beschrijvende naam** een beschrijvende naam in.
    1. Voer in het vak **Trefwoorden** relevante trefwoorden in.
    1. Voer in het vak **Weergavevolgorde** een getal voor de weergavevolgorde in (optioneel).
1. Selecteer **Opslaan** in het actievenster.
1. Herhaal de bovenstaande stappen om extra knooppunten toe te voegen.

De volgende afbeelding toont het maken van een nieuw knooppunt voor een producthiërarchie.

![Een producthiërarchie maken](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Overige instellingen

Categoriekenmerkgroepen kunnen ook naar behoefte worden toegewezen aan elke groep.  

## <a name="additional-resources"></a>Aanvullende resources

[Detailhandelhiërarchieën](retail-hierarchies.md)

[Productcategorieën en producten beheren ](category-management-product-creation.md)

[De sorteervolgorde voor entiteiten voor merchandising wijzigen](custom-order-categories-nav-retail-prod-hierarchy.md)

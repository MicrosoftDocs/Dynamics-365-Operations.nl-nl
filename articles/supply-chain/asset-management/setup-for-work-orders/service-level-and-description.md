---
title: Serviceniveau en -beschrijving
description: In dit onderwerp worden serviceniveau en -beschrijving in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e645c25208f55b1032bc7f7c181c72db7a2f265
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874642"
---
# <a name="service-level-and-description"></a>Serviceniveau en -beschrijving

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Wanneer u een werkorder maakt, kunt u de serviceniveaus hiervoor definiëren en er een algemene omschrijving aan toevoegen. U kunt serviceniveaus voor werkorders maken op de pagina **Serviceniveaus voor werkorders** en omschrijvingen op de pagina **Omschrijvingen voor werkorders**.

## <a name="create-a-service-level"></a>Een serviceniveau maken

1. Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Serviceniveau**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Serviceniveau** het serviceniveau in (bijvoorbeeld een nummer).
4. Voer in het veld **Naam** een naam in.

    Op het Sneltabblad **Werkorders** kunt u de verwachte begin- en einddatums en -tijden definiëren. De velden op dit Sneltabblad definiëren de periode waarin werkorders moeten worden gestart en beëindigd. Deze worden gebruikt voor werkorders die handmatig worden gemaakt en werkorders die worden gemaakt op basis van onderhoudsaanvragen. 

5. Voer in het veld **Begindatum** een aantal dagen in om de periode te definiëren waarin de werkorder moet beginnen. Het aantal dagen wordt berekend vanaf de aanmaakdatum van de werkorder. Als de werkorder bijvoorbeeld moet beginnen wanneer deze wordt gemaakt, voert u **0** in. Als de werkorder bijvoorbeeld een week nadat deze is gemaakt moet beginnen, voert u **7** in.
6. Als u een begintijd voor de werkorder wilt instellen, moet u behalve de begindatum ook de optie **Begintijd instellen** op **Ja** instellen. Voer vervolgens de begintijd in het veld **Begintijd** in. Als u de optie op **Nee** instelt, wordt de huidige tijd van de dag gebruikt.
7. Voer in het veld **Einddatum** een aantal dagen in om de periode te definiëren waarin de werkorder moet eindigen. Het aantal dagen wordt berekend vanaf de begindatum van de werkorder. Als de werkorder bijvoorbeeld binnen één week na de begindatum moet eindigen, voert u **7**in.
8. Als u een eindtijd voor de werkorder wilt instellen, moet u behalve de einddatum ook de optie **Eindtijd instellen** op **Ja** instellen. Voer vervolgens de eindtijd in het veld **Eindtijd** in. Als u de optie op **Nee** instelt, wordt de huidige tijd van de dag gebruikt.
9. Selecteer **Opslaan**.

![Figuur 1](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Een omschrijving maken

1. Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Omschrijvingen**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Omschrijving** een omschrijving in.
4. Selecteer **Opslaan**.
---
title: Financiële-dimensiesets
description: In dit onderwerp worden financiële dimensiesets beschreven en vindt u enkele tips voor optimalisatie van het gebruik.
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864407"
---
# <a name="financial-dimension-sets"></a>Financiële-dimensiesets

[!include [banner](../includes/banner.md)]

In dit onderwerp worden financiële dimensiesets beschreven en vindt u enkele tips voor optimalisatie van het gebruik.

Een dimensieset is een geordende lijst met financiële dimensies die kan worden gebruikt om grootboekgegevens op een door de gebruiker gedefinieerde manier samen te vatten. De primaire toepassing van dimensiesets is het definiëren van een proefbalans.

De enige standaarddimensieset is de dimensieset die alleen de hoofdrekening bevat.

U gebruikt de pagina **Financiële dimensiesets** om financiële dimensiesets te maken en te beheren.

## <a name="dimension-set-balances"></a>Saldi van dimensiesets

Een dimensieset kan saldi hebben die zijn gebaseerd op de financiële dimensies. De saldi bestaan in het grootboek en zijn gebaseerd op de dimensiesetdefinitie. De saldi worden samengevat uit de grootboekgegevens om de prestaties te verbeteren wanneer deze worden opgehaald (bijvoorbeeld wanneer er een proefbalans wordt gegenereerd).

## <a name="create-balances"></a>Saldi maken

Gebruik de knop **Saldi maken** om de saldi te initialiseren voor een dimensieset die momenteel geen saldi heeft.

> [!NOTE]
> Het is raadzaam om het aantal dimensiesets met saldi te beperken, omdat saldo-updates van invloed zijn op alle boekingsactiviteiten in het grootboek.

## <a name="update-balances"></a>Saldi bijwerken

Gebruik de knop **Saldi bijwerken** om de laatste boekingsactiviteit voor grootboek op te nemen in de saldi. Saldo-updates zijn lichte bewerkingen. Ze worden verwerkt alleen voor de boekingsactiviteit in het grootboek van na de laatste update.

> [!NOTE]
> De weergave van de proefbalans dwingt een update af om ervoor te zorgen dat de weergegeven saldi actueel zijn. U kunt een terugkerende batchtaak gebruiken, zodat de meest gebruikte dimensiesets snel kunnen worden bijgewerkt. Op deze manier beperkt u de tijd dat gebruikers van de proefbalans moeten wachten.

## <a name="rebuild-balances"></a>Saldi opnieuw maken

Gebruik de knop **Saldi opnieuw maken** om de saldi weer helemaal opnieuw te maken. Op deze manier zorgt u ervoor dat ze overeenkomen met de gegevens in het grootboek. Voor het opnieuw samenstellen van de saldi is veel verwerkingskracht vereist en dat is meestal niet nodig.

> [!NOTE]
> Als u een scenario hebt waarin het saldo regelmatig opnieuw moet worden opgebouwd, kunt u het beste contact opnemen met de klantenondersteuning. Klantenondersteuning kan u helpen om te bepalen waarom saldi niet overeenkomen met de gegevens in het grootboek.

## <a name="clear-balances"></a>Saldi wissen

Gebruik de knop **Saldi wissen** maken om de saldi te verwijderen en verdere updates te stoppen. De dimensieset heeft dan geen invloed meer op boekingsactiviteiten in het grootboek.

Zie voor meer informatie het onderwerp [Financiële dimensies](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

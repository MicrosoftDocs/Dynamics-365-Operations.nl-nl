---
title: Handmatig publiceren van beoordelingen en recensies inschakelen door een moderator
description: In dit onderwerp wordt beschreven hoe u handmatig publiceren van beoordelingen en recensies door een moderator in Microsoft Dynamics 365 Commerce inschakelt en hoe u handmatig beoordelingen en recensies publiceert.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 25ae7074fcf39bf4408ea1fa0acfc334281bb254
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675044"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Handmatig publiceren van beoordelingen en recensies inschakelen door een moderator

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u handmatig publiceren van beoordelingen en recensies door een moderator in Microsoft Dynamics 365 Commerce inschakelt en hoe u handmatig beoordelingen en recensies publiceert.

De oplossing voor beoordelingen en recensies van Dynamics 365 Commerce gebruikt Azure Cognitive Services om automatisch grof taalgebruik in beoordelingstitels en -inhoud te bewerken en om beoordelingen en recensies te publiceren. Handmatige tussenkomst is dus niet nodig om beoordelingen en recensies op uw e-commercesite te beoordelen en te publiceren.

Sommige bedrijven geven er echter de voorkeur aan om beoordelingen handmatig door moderators te laten bewerken en goed te keuren voordat ze worden gepubliceerd. Als u het handmatig publiceren van beoordelingen en recensies door een moderator wilt inschakelen, moet u de functie **Moderator vereisen voor beoordelingen en recensies** in Commerce Site Builder inschakelen.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>De functie Moderator vereisen voor beoordelingen en recensies in Commerce Site Builder

Neem de volgende stappen om de functie **Moderator vereisen voor beoordelingen en recensies** in Commerce Site Builder in te schakelen.

1. Ga naar **Start \> Recensies \> Instellingen**.
1. Stel de optie **Moderator vereisen voor beoordelingen en recensies** in op **Aan**.

> [!NOTE]
> Door de functie **Moderator vereisen voor beoordelingen en recensies** in te schakelen, stopt u het automatisch publiceren van beoordelingen en recensies, zodat nu handmatige publicatie is vereist. Azure Cognitive Services blijft echter grof taalgebruik bewerken in beoordelingstitels en inhoud.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Beoordelingen en recensies publiceren

Als u de functie **Moderator vereisen voor beoordelingen en recensies** inschakelt, moet een moderator handmatig beoordelingen en recensies beoordelen en publiceren om ze op uw e-commercesite weer te geven.

Voer de volgende stappen uit om beoordelingen en recensies te beoordelen en te publiceren in Commerce Site Builder.

1. Ga naar **Recensies \> Moderator**.
1. Als in het raster het veld **Status** voor een rij is ingesteld op **Niet-gepubliceerd**, zijn de beoordeling en recensie in die rij nog niet gepubliceerd. Als u alleen niet-gepubliceerde beoordelingen en recensies wilt weergeven, selecteert u **Status: Moet worden geëvalueerd** in het statusfilter boven het raster.
1. Selecteer een of meer beoordelingen en recensies met de status **Niet-gepubliceerd** en selecteer **Publiceren** op de opdrachtbalk. De geselecteerde beoordelingen en recensies worden toegevoegd aan de publicatiewachtrij en worden weergegeven op de e-commercesite nadat ze zijn gepubliceerd.

> [!NOTE]
> - Nadat een beoordeling en een recensie zijn gepubliceerd, verandert de statuswaarde van **Niet-gepubliceerd** in een null-waarde (leeg veld).
> - Als u meerdere beoordelingen en recensies selecteert met verschillende statussen en vervolgens **Publiceren** selecteert, worden nog niet-gepubliceerde beoordelingen en recensies gepubliceerd. Beoordelingen en recensies die al zijn gepubliceerd, worden echter niet opnieuw gepubliceerd.

In de volgende afbeelding ziet u een voorbeeld van drie niet-gepubliceerde beoordelingen en recensies die zijn geselecteerd op de pagina **Moderator** in Commerce Site Builder.

![Drie niet-gepubliceerde beoordelingen en recensies die zijn geselecteerd op de pagina Moderator in Commerce Site Builder.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

---
title: Een variant promoveren en een experiment voltooien
description: In dit onderwerp wordt beschreven hoe u een geslaagde variant kunt promoveren en een experiment kunt voltooien in Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
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
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930168"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Een variant promoveren en een experiment voltooien

In dit onderwerp wordt beschreven hoe u de variatie die de beste resultaten heeft opgeleverd in uw experiment kunt promoveren en hoe u het experiment kunt voltooien. In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce. Extra stappen worden in afzonderlijke onderwerpen behandeld.

[ ![Traject van gebruiker voor experimenten - controleren en voltooien](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Nadat u [uw experiment hebt uitgevoerd](experimentation-run-monitor.md) en voldoende gegevens hebt verzameld om te bepalen welke variatie u op uw live site wilt gebruiken, promoveert u de variatie en beëindigt u het experiment.

## <a name="promote-a-variation"></a>Een variatie promoveren
Gebruik de gegevens en analyse met betrekking tot het experiment in de service van derden om te bepalen welke variatie de beste resultaten heeft opgeleverd. Als u de huidige inhoud op de live site wilt vervangen met de winnende variatie zodat deze beschikbaar is voor alle gebruikers van uw website, gaat u als volgt te werk. 

1. Ga naar het tabblad **Experimenten** in Site Builder en selecteer het experiment.
1. Selecteer **Experiment voltooien** op de bovenste balk.
1. Selecteer in het dialoogvenster **Experiment voltooien** de optie **Experimentgegevens controleren**. De service van derden wordt geopend, waar u de metrische gegevens kunt valideren en kunt bepalen welke variatie de beste resultaten geeft.
1. Selecteer in het menu van het dialoogvenster **Experiment voltooien** in Site Builder de winnende variatie en selecteer **Volgende**.
1. Open de service van derden en stop het experiment.
1. Selecteer in Site Builder de functie **Voltooien** om de oorspronkelijke live pagina te overschrijven en de winnende variatie te publiceren zodat deze beschikbaar is voor alle gebruikers van uw website. 

> [!NOTE]
> Als u de huidige live pagina wilt behouden en geen variatie wilt publiceren, selecteert u **De oorspronkelijke pagina opnieuw publiceren**.

## <a name="delete-your-experiment"></a>Uw experiment verwijderen
Hoewel het niet nodig is om een voltooid experiment te verwijderen in Commerce, kunt u het verwijderen om ruimte te besparen of om uw werkruimte op te schonen. Ga als volgt te werk om een experiment te verwijderen.

1. Ga naar het tabblad **Experimenten** in Site Builder en selecteer het experiment. 
    > [!NOTE]
    > Als het experiment nog steeds actief is, stopt u het experiment in de service van derden voordat u verder gaat.
1. Selecteer **Publicatie ongedaan maken** op de opdrachtbalk om de variatie-inhoud van de live site te verwijderen.
1. Selecteer **Verwijderen** op de opdrachtbalk om het experiment te verwijderen.

## <a name="previous-step"></a>Vorige stap
[Een experiment uitvoeren en controleren](experimentation-run-monitor.md)

---
title: Een variant promoveren en een experiment voltooien
description: In dit artikel wordt beschreven hoe u een geslaagde variant kunt promoveren en een experiment kunt voltooien in Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942732"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Een variant promoveren en een experiment voltooien

In dit artikel wordt beschreven hoe u de variatie die de beste resultaten heeft opgeleverd in uw experiment kunt promoveren en hoe u het experiment kunt voltooien. In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce. Extra stappen worden in afzonderlijke artikelen behandeld.

[ ![Traject van gebruiker voor experimenten - controleren en voltooien.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Nadat u [uw experiment hebt uitgevoerd](experimentation-run-monitor.md) en voldoende gegevens hebt verzameld om te bepalen welke variatie u op uw live site wilt gebruiken, promoveert u de variatie en beëindigt u het experiment.

## <a name="promote-a-variation"></a>Een variatie promoveren
Gebruik de gegevens en analyse met betrekking tot het experiment in de service van derden om te bepalen welke variatie de beste resultaten heeft opgeleverd. U kunt de variatie vervolgens promoveren door de huidige inhoud op de live site te vervangen met de winnende variatie zodat deze beschikbaar is voor alle gebruikers van uw website.

Voer de volgende stappen uit om de winnende variatie te promoveren. 

1. Selecteer **Experimenten** in het linkernavigatievenster in Commerce Site Builder en selecteer het experiment vervolgens.
1. Selecteer **Experiment voltooien** op de opdrachtbalk.
1. Selecteer in het dialoogvenster **Experiment voltooien** de optie **Experimentgegevens controleren**. De service van derden wordt geopend, waar u de metrische gegevens kunt valideren en kunt bepalen welke variatie de beste resultaten geeft.
1. Selecteer in het dialoogvenster **Experiment voltooien** de winnende variatie en selecteer vervolgens **Volgende**.
1. Open de service van derden en stop het experiment.
1. Selecteer in Site Builder de functie **Voltooien** om de oorspronkelijke live pagina te overschrijven en de winnende variatie te publiceren zodat deze beschikbaar is voor alle gebruikers van uw website. 

> [!NOTE]
> Als u de huidige live pagina wilt behouden en geen variatie wilt publiceren, selecteert u **De oorspronkelijke pagina opnieuw publiceren**.

## <a name="delete-your-experiment"></a>Uw experiment verwijderen
Hoewel het niet nodig is om een voltooid experiment te verwijderen in Commerce, kunt u het verwijderen om ruimte te besparen of om uw werkruimte op te schonen. 

Voer de volgende stappen uit om een voltooid experiment te verwijderen in Commerce Site Builder.

1. Selecteer **Experimenten** in het linkernavigatievenster en selecteer het experiment vervolgens. 
    > [!NOTE]
    > Als het experiment nog steeds actief is, stopt u het experiment in de service van derden voordat u verder gaat.
1. Selecteer **Publicatie ongedaan maken** op de opdrachtbalk om de variatie-inhoud van de live site te verwijderen.
1. Selecteer **Verwijderen** om het experiment te verwijderen.

## <a name="previous-step"></a>Vorige stap
[Een experiment uitvoeren en controleren](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Nummerreeksen instellen voor detailhandeloverzichten
description: In dit onderwerp wordt beschreven hoe u de nummerreeksen configureert die vereist zijn voor detailhandeloverzichten in Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: db47ca4ee8bac0d55b9a9c732183d2734bce660f
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649198"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Nummerreeksen instellen voor detailhandeloverzichten

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u de nummerreeksen configureert die vereist zijn voor detailhandeloverzichten in Microsoft Dynamics 365 Commerce.

In Dynamics 365 Commerce worden twee typen detailhandeloverzichten gebruikt. 

- **Transactieoverzichten** zijn bedoeld om vaak te worden gemaakt en geboekt. Hiermee worden alle niet-financiële transacties in de winkel geboekt naar Dynamics 365 Commerce Headquarters. 
- **Financiële overzichten** zijn bedoeld om één keer per werkdag te worden gemaakt en geboekt. Deze bevatten alleen afgesloten ploegen uit de winkels die via de P-taak naar Commerce Headquarters zijn geüpload.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Een nummerreeks configureren voor het boeken van overzichten

Wanneer u de configuratie van een winkel hebt voltooid, moet u in Commerce Headquarters een unieke nummerreeks configureren die wordt gebruikt voor overzichten tijdens het maken van overzichten.

Voer de volgende stappen uit om een nummerreeks voor het boeken van overzichten te configureren in Commerce Headquarters.

1. Ga naar **Organisatiebeheer \> Nummerreeksen \> Nummerreeksen**.
1. Selecteer **Nieuw \> Nummerreeks** om een nieuwe reeks te maken.
1. Voer op het sneltabblad **Identificatie**, in het veld **Nummerreekscode** een code voor een nummerreeks in.
1. Voer in het veld **Naam nummerreeks** een naam in.
1. Selecteer op het sneltabblad **Bereikparameters** in het veld **Bereik** de waarde **Operationele eenheid**.
1. Selecteer in het veld **Operationele eenheid** de winkel waarvoor de nummerreeks wordt gebruikt.
1. Definieer op het sneltabblad **Segmenten** de segmenten.
1. Stel op het sneltabblad **Verwijzingen** het veld **Gebied** in op **Detailhandelwinkel**.
1. Stel het veld **Verwijzing** in op **Overzichtsnummer** en selecteer **OK**.

    ![De sneltabbladen Id, Bereikparameters, Segmenten en Verwijzingen op de pagina Nummerreeksen.](media/retail-statements-num-seq-setup-01.png)

1. Werk op het sneltabpunt **Algemeen** in de sectie **Nummertoewijzing** de velden **Kleinste** en **Grootste** bij, zodat deze overeenkomen met de lengte van het segment **Alfanumeriek** dat u hebt gedefinieerd op het sneltabblad **Segmenten**.
1. Op het sneltabblad **Prestaties** is het raadzaam om de optie **Voorafgaande toewijzing** in te stellen op **Ja** en het veld **Aantal nummers** op **25**.

    ![De sneltabbladen Algemeen en Prestaties op de pagina Nummerreeksen.](media/retail-statements-num-seq-setup-02.png)

1. Selecteer in het actievenster **Opslaan** om uw wijzigingen op te slaan en de pagina af te sluiten.

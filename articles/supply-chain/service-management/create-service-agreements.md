---
title: Serviceovereenkomsten maken
description: In dit artikel wordt beschreven hoe u serviceovereenkomsten maakt met de functies in de modules Servicebeheer en Projectbeheer en boekhouding.
author: sorenva
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d18d279cd437e98cad6495def953978cb78e723e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901758"
---
# <a name="create-service-agreements"></a>Serviceovereenkomsten maken

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u serviceovereenkomsten maakt met de functies in de modules Servicebeheer en Projectbeheer en boekhouding.

## <a name="create-a-service-agreement-from-service-management"></a>Een serviceovereenkomst maken via Servicebeheer

1. Ga naar **Servicebeheer**.
2. Selecteer **Serviceovereenkomsten** om in de koptekst van de pagina een nieuwe serviceovereenkomstregel te maken. 
3. Selecteer **Nieuw**. Voer een omschrijving in, selecteer een verwijzing naar een project in het veld **Project-id** en vul de rest van de velden en regels voor de serviceovereenkomst in. Selecteer **Opslaan**.
4. Selecteer op het tabblad **Relaties** de optie **Serviceobjecten** of **Servicetaken** om serviceobject- of servicetaakrelaties voor de serviceovereenkomst te maken. U kunt de serviceobjecten en -taken waarvoor u relaties hebt gemaakt, toevoegen aan de regels van de serviceovereenkomst.
5. Maak serviceovereenkomstregels in het onderste deel van de pagina door regels te kopiëren uit een servicesjabloon of een andere serviceovereenkomst of door de serviceovereenkomstregels handmatig te maken.

> [!NOTE]
> Als u regels vanuit een andere serviceovereenkomst kopieert naar de desbetreffende serviceovereenkomst, kunt u aangeven of u ook serviceobject- en servicetaakrelaties wilt kopiëren. Als u deze relaties kopieert, worden deze toegevoegd aan de bestaande relaties in de serviceovereenkomst. Als u serviceovereenkomstregels kopieert uit een servicesjabloon, worden de serviceobject- en servicetaakrelaties automatisch naar de nieuwe serviceovereenkomstregels gekopieerd als serviceobjectrelaties en servicetaakrelaties.

## <a name="create-service-agreement-lines-manually"></a>Handmatig serviceovereenkomstregels maken

1. Voeg vanaf de pagina **Serviceovereenkomsten** een serviceovereenkomstregel toe in het lijnenraster. 
2. Voer de juiste gegevens voor de serviceovereenkomstregel in. 
3. Selecteer **Opslaan** om de regel op te slaan en sluit de pagina.

## <a name="create-a-service-agreement-from-project"></a>Een serviceovereenkomst maken via Project

1. Selecteer **Projectbeheer en boekhouding**.
2. Selecteer **Alle projecten**.
3. Selecteer het project in de lijst.
4. Selecteer in het **actiedeelvenster** de optie **Beheren**. Selecteer in de groep **Nieuwe actie** de optie **Service** en selecteer **Serviceovereenkomst**.
5. Voer de beschreven stappen in de sectie **Een serviceovereenkomst maken** uit om de projectverwijzing in te voeren.


## <a name="related-articles"></a>Gerelateerde artikelen

[Overzicht van Servicelevelovereenkomsten opstellen en tot stand brengen](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
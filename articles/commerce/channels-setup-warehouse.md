---
title: Een magazijn instellen
description: In dit artikel wordt beschreven hoe u een magazijn instelt dat kan worden gebruikt met een nieuw kanaal in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ae091d0b75abfdb001402ea71cc0df36bc1a20c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885230"
---
# <a name="warehouse-set-up"></a>Magazijninstellingen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een magazijn instelt dat kan worden gebruikt met een nieuw kanaal in Microsoft Dynamics 365 Commerce.

Aan elk Commerce-kanaal moet een geconfigureerd magazijn worden gekoppeld. De volgende procedures bieden de minimale configuratie die is vereist voor het instellen van een magazijn voor een Commerce-kanaal. Zie [Overzicht van Magazijnbeheer](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over magazijninstellingen.

## <a name="configure-a-warehouse-site"></a>Een magazijnlocatie configureren

Voordat u een magazijn instelt, moet u een magazijnlocatie configureren.

Voer de volgende stappen uit om een magazijnlocatie te configureren.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Locaties**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer een waarde in het veld **Locatie** in.
1. Voer een waarde in het veld **Naam** in.
1. Stel in de sectie **Algemeen** de juiste **Tijdzone** in.
1. Voer in het veld **Adressen** een adres in.
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeld van magazijnlocatie.

![Voorbeeld van magazijnlocatie.](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Een magazijn instellen

Voer deze stappen uit om een magazijn in te stellen.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Magazijnen**.
1. Selecteer **Nieuw** in het actievenster.
1. Typ een waarde in het veld **Magazijn**.  Als dit een 1:1-toewijzing is voor een winkel, kunt u de naam van de winkel of van een regionaal distributiecentrum gebruiken.
1. Voer een waarde in het veld **Naam** in.
1. Selecteer in de vervolgkeuzelijst **Locatie** de zojuist gemaakte magazijnlocatie.
1. Selecteer in het veld **Type** de optie **Standaard**.
    - Als u een **Quarantainemagazijn** wilt instellen, moet u eerst deze stappen uitvoeren om een extra magazijn te maken waarvoor het **Type** is ingesteld op **Quarantaine**.
    - Als u een **Transitmagazijn** wilt instellen, moet u eerst deze stappen uitvoeren om een extra magazijn te maken waarvoor het **Type** is ingesteld op **Transit**.
1. Selecteer **Opslaan** in het actievenster.

## <a name="set-up-inventory-aisles"></a>Voorraadgangen instellen

Voer de onderstaande stappen uit om voorraadgangen in te stellen:

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Locatie-instellingen \> Voorraadgangen**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer in de vervolgkeuzelijst **Magazijn** het zojuist gemaakte magazijn.
1. Geef in het veld **Gang** een naam op (bijvoorbeeld Def).
1. Geef in het veld **Naam** een naam op (bijvoorbeeld Standaardgang).
1. Selecteer **Opslaan** in het actievenster.

## <a name="set-up-warehouse-inventory-locations"></a>Magazijnvoorraadlocaties instellen

Voer de volgende stappen uit om magazijnvoorraadlocaties in te stellen voor standaard-, beschadigde en geretourneerde voorraad.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Magazijnen**.
1. Selecteer het magazijn dat u eerder hebt gemaakt.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer op de actiepagina **Magazijn** en selecteer vervolgens **Voorraadlocatie**.
1. Selecteer **Nieuw** in het actievenster. De vervolgkeuzelijst **Magazijn** wordt nu standaard ingesteld op het nieuwe magazijn.
    1. Voer in het vak **Gang** de naam in van de gang die u eerder hebt opgegeven. 
    1. Stel **Handmatig bijwerken** in op **Ja**
    1. Voer in het vak **Locatie** de naam in van het magazijn.
    1. Selecteer **Opslaan** in het actievenster.
 1. Selecteer **Nieuw** in het actievenster.  De vervolgkeuzelijst **Magazijn** wordt nu standaard ingesteld op het nieuwe magazijn.
    1. Voer in het vak **Gang** de naam in van de gang die u eerder hebt opgegeven.  
    1. Stel **Handmatig bijwerken** in op **Ja**
    1. Voer in het vak **Locatie** de tekst 'Beschadigd' in.
    1. Selecteer **Opslaan** in het actievenster.
 1. Selecteer **Nieuw** in het actievenster.  De vervolgkeuzelijst **Magazijn** wordt nu standaard ingesteld op het nieuwe magazijn.
    1. Voer in het vak **Gang** de naam in van de gang die u eerder hebt opgegeven. 
    1. Stel **Handmatig bijwerken** in op **Ja**
    1. Voer in het vak **Locatie** de tekst 'Retouren' in.
    1. Selecteer **Opslaan** in het actievenster.
    
In de volgende afbeelding ziet u de instellingen voor een magazijnvoorraadlocatie in San Francisco.

![Voorbeeld van voorraadlocatie-instellingen.](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Magazijninstellingen voltooien

Volg deze stappen om de magazijninstellingen te voltooien.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Afzetkanaalinstellingen \> Magazijnen**.
1. Selecteer het magazijn dat u eerder hebt gemaakt.
1. Selecteer **Bewerken** in het actievenster.
1. Onder **Voorraad- en magazijnbeheer**:
    1. Stel **Standaardlocatie voor ontvangst** in op de hierboven gemaakte standaardlocatie.
    1. Selecteer **Standaardlocatie voor uitgifte** in op de hierboven gemaakte standaardlocatie.
1. Voer in de sectie **Adressen** het adres van een magazijn in.
1. In de sectie **Detailhandel**: 
    1. Voer in het vak **Standaardlocatie voor retournering** de eerder gemaakte locatie voor retouren in.
    1. Stel **Opslag** in op **Ja**.
    1. Stel **Gewicht** in op **1,00**. 
    1. Voer in het vak **Opslagdimensies** de eerder gemaakte standaardlocatie in.
1. Stel in de sectie **Magazijn** de **Fysieke negatieve voorraad** in op **Ja**.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont details voor een geconfigureerd magazijn.

![Voorbeeld van geconfigureerd magazijn.](media/warehouse-sample.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van Magazijnbeheer](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Een detailhandelafzetkanaal instellen](channel-setup-retail.md)
    
[Een online afzetkanaal instellen](channel-setup-online.md)

[Een callcenterkanaal instellen](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]

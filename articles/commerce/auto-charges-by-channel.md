---
title: Automatische toeslagen per kanaal inschakelen en configureren
description: In dit onderwerp wordt uitgelegd hoe u automatische toeslagen per kanaal kunt inschakelen en configureren in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d37b2b785dd29850dcd02d0905e5872445384990
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993723"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Automatische toeslagen per kanaal inschakelen en configureren

In dit onderwerp wordt uitgelegd hoe u automatische toeslagen per kanaal kunt inschakelen en configureren in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

U kunt bijvoorbeeld scenario's hebben waarbij recyclingkosten of andere kosten moeten worden toegepast op een groep producten die worden verkocht in alle of een aantal winkels in een bepaalde staat (bijvoorbeeld Californië). Met de functie **Automatische toeslagen per kanaal inschakelen** in Commerce kunt u automatische toeslagen per kanaal opgeven (bijvoorbeeld voor een bepaald winkelkanaal). Deze functie is beschikbaar in Dynamics 365 Commerce versie 10.0.10 en hoger.

Als u automatische toeslagen per kanaal wilt inschakelen en configureren, moet u de volgende taken uitvoeren:

- Schakel de functie **Automatische toeslagen per kanaal inschakelen** in.
- Configureer de organisatiehiërarchiedoelstelling.
- Definieer automatische toeslagen per kanaal.

> [!NOTE]
> De functie **Automatische toeslagen per kanaal inschakelen** werkt alleen als de functie voor geavanceerde automatische toeslagen is ingeschakeld. Zie [Geavanceerde automatische toeslagen voor meerdere kanalen](omni-auto-charges.md) voor informatie over het inschakelen van de functie voor geavanceerde automatische toeslagen.

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>De functie Automatische toeslagen per kanaal inschakelen

Voer de volgende stappen uit om automatische toeslagen per kanaal in te schakelen in Commerce.

1. Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.
1. Ga op het tabblad **Niet ingeschakeld** naar de lijst **Functienaam** en selecteer **Automatische toeslagen per kanaal inschakelen**.
1. Selecteer rechtsonder **Nu inschakelen**. Nadat de functie is ingeschakeld, wordt deze weergegeven in de lijst op het tabblad **Alles**.
1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.
1. Zoek en selecteer in het linkerdeelvenster de taak **1110** (**Algemene configuratie**).
1. Selecteer **Nu uitvoeren** in het actievenster om de configuratiewijzigingen door te voeren.

> [!WARNING]
> Als u de functie **Automatische toeslagen per kanaal inschakelen** hebt uitgeschakeld nadat u deze al hebt gebruikt, wordt het veld **Relatie detailhandelskanaal** onder **Automatische toeslagen** niet meer weergegeven en verliest u alle bestaande configuraties. Als het verwijderen van de configuraties voor **Relatie detailhandelskanaal** ertoe leidt dat de automatische toeslagregels worden gedupliceerd, zal een poging om de functie uit te schakelen mislukken. Voordat u de functie uitschakelt, moet u alle regels voor automatische toeslagen controleren en eventueel vereiste wijzigingen aanbrengen.

## <a name="configure-the-organization-hierarchy-purpose"></a>De organisatiehiërarchiedoelstelling configureren

Een nieuwe organisatiehiërarchiedoelstelling met de naam **Automatische toeslagen detailhandel** is gemaakt om de hiërarchie voor automatische toeslagen per kanaal te beheren.

Voer de volgende stappen uit om een standaardhiërarchie toe te wijzen aan een organisatiehiërarchiedoelstelling in Commerce.
        
1. Ga naar **Organisatiebeheer \> Organisaties \> Organisatiehiërarchiedoelstellingen**.
1. Selecteer in het linkerdeelvenster de optie **Automatische toeslagen detailhandel**.
1. Selecteer **Toevoegen** onder **Toegewezen hiërarchieën**.
1. Selecteer in het dialoogvenster **Organisatiehiërarchieën** een organisatiehiërarchie (bijvoorbeeld **Detailhandelwinkels per regio**) en selecteer **OK.**
1. Selecteer **Als standaard instellen** onder **Toegewezen hiërarchieën**.
1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.
1. Zoek en selecteer in het linkerdeelvenster de taak **1040** (**Producten**).
1. Selecteer **Nu uitvoeren** in het actievenster.
1. Herhaal de voorgaande twee stappen om de taken **1070** (**Kanaalconfiguratie**) en **1110** (**Algemene configuratie**) uit te voeren.

![Configuratie van de organisatiehiërarchiedoelstelling Automatische toeslagen detailhandel](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Automatische toeslagen per kanaal definiëren

Nadat u de functie **Automatische toeslagen per kanaal inschakelen** hebt ingeschakeld en de organisatiehiërarchiedoelstelling **Automatische toeslagen detailhandel** hebt geconfigureerd, kunnen automatische toeslagen per kanaal worden gedefinieerd op het niveau van de orderkoptekst of het niveau van de orderregel.

Voer de volgende stappen uit om automatische toeslagen per kanaal te definiëren in Commerce.

1. Ga naar **Klanten \> Instelling van toeslagen \> Automatische toeslagen**.
1. Selecteer in het linkerdeelvenster in het veld **Niveau** de optie **Koptekst** of **Regel**, afhankelijk van uw zakelijke vereisten.
1. Selecteer in het veld **Code detailhandelskanaal** de toepasselijke kanaalcode (bijvoorbeeld **Tabel** of **Groep**). Als de standaardinstelling **Alle** wordt gebruikt, worden toeslagregels op alle kanalen toegepast.

    - Als u **Groep** selecteert, moet u ervoor zorgen dat er een toeslagengroep voor een detailhandelskanaal wordt gemaakt in **Detailhandel en commerce \> Afzetkanaalinstellingen \> Toeslagen \> Toeslaggroepen voor detailhandelkanaal**.
    - Als u **Tabel** selecteert, kunt u een specifiek kanaal selecteren (bijvoorbeeld **San Francisco**) in het veld **Relatie detailhandelkanaal**.

1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.
1. Zoek en selecteer in het linkerdeelvenster de taak **1040** (**Producten**).
1. Selecteer **Nu uitvoeren** in het actievenster.
1. Herhaal de voorgaande twee stappen om de taken **1070** (**Kanaalconfiguratie**) en **1110** (**Algemene configuratie**) uit te voeren.
    
![Automatische toeslagen gedefinieerd per kanaal](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Voorbeeldscenario

In het volgende voorbeeld vindt u een overzicht van de stappen die nodig zijn om een product te configureren, zodat recyclingkosten in rekening worden gebracht wanneer het product wordt verkocht via een winkelafzetkanaal voor San Francisco. In het voorbeeld ziet u ook hoe de automatische toeslagen worden weergegeven in de POS-toepassing (Commerce Point of Sale).

De organisatie definieert een toeslagcode met de naam **RECYCLE**, zoals wordt weergegeven in de volgende afbeelding.

![Toeslagcode RECYCLE](media/Auto-charges-charge-code.png)

Er wordt op regelniveau een automatische toeslag gemaakt. Deze heeft de volgende configuratie:

- Het veld **Rekeningcode** wordt ingesteld op **Alle**.
- Het veld **Artikelcode** wordt ingesteld op **Tafel**.
- Het veld **Artikelrelatie** wordt ingesteld op product-id **91001**.
- Het veld **Code van leveringsmethode** wordt ingesteld op **Alle**.
- Het veld **Code detailhandelskanaal** wordt ingesteld op **Tafel**.
- Het veld **Relatie detailhandelskanaal** wordt ingesteld op de winkel in **San Francisco**.

Er wordt een regel met automatische toeslagen gemaakt. Deze heeft de volgende configuratie:

- Het veld **Valuta** wordt ingesteld op **USD**.
- Het veld **Toeslagcode** wordt ingesteld op **RECYCLE**.
- Het veld **Categorie** wordt ingesteld op **Vast**.
- Het veld **Toeslagen** wordt ingesteld op **$6,25**.

![Configuratie van de automatische toeslag op regelniveau en de automatische toeslagregel](media/Auto-charges-recyclingfee-line-fee.png)

In de POS-toepassing wordt een verkooporder gemaakt in het detailhandelskanaal **San Francisco**. Op de regel **Toeslagen** worden de recyclingkosten van **$6,25** weergegeven.

Selecteer **Transactieopties \> Toeslagen \> Toeslagen beheren** in de POS-toepassing als u de toeslagcode en de omschrijving voor de recyclingkosten wilt bekijken.

![Recyclingkosten in de POS-toepassing](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Geavanceerde automatische toeslagen voor meerdere kanalen](omni-auto-charges.md)

[Toeslagen voor koptekst naar rato verdelen voor overeenkomende verkoopregels](pro-rate-charges-matching-lines.md)

---
title: Voorraadbuffers en voorraadniveaus configureren
description: In dit onderwerp wordt uitgelegd hoe u voorraadbuffers en voorraadniveaus configureert waarmee berichten voor voorraadbeschikbaarheid op Microsoft Dynamics 365 Commerce-sites worden bepaald.
author: boycezhu
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: ef58dbb756c7bed3924010cb33eff27af66cd0bd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411405"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Voorraadbuffers en voorraadniveaus configureren

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u voorraadbuffers en voorraadniveaus configureert waarmee de berichten over voorraadbeschikbaarheid op Microsoft Dynamics 365 Commerce-sites worden bepaald.

## <a name="overview"></a>Overzicht

Dynamics 365 Commerce Headquarters omvat voorraadgegevens en diverse kanalen, zoals POS-toepassingen (Point of Sale), webwinkels en andere aangepaste geïntegreerde toepassingen die op asynchrone wijze voorraad verplaatsen. De waarden voor beschikbare voorraad die via de pagina voor voorhanden voorraad in Commerce Headquarters worden verkregen, via de POS-gebruikersinterface en de e-Commerce-API's voor voorraadbeschikbaarheid, zijn daarom niet altijd 100 procent nauwkeurig in realtime.

In plaats van de werkelijke voorraadwaarden in webwinkels te tonen, geven veel detailhandelaren er de voorkeur aan om berichten over de beschikbaarheidsstatus van de voorraad (bijvoorbeeld Beschikbaar Niet op voorraad) weer te geven om klanten te informeren over de beschikbaarheid van een artikel. Voor deze aanpak moeten voorraadbuffers en voorraadniveaus die de berichten over voorraadbeschikbaarheid bepalen, beschikbaar worden gemaakt en geconfigureerd.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Vereiste: de functie voor voorraadbuffers en -niveaus inschakelen

De functie voor voorraadbuffers en voorraadniveaus wordt bestuurd via Functiebeheer in Commerce Headquarters. Voer de volgende stappen uit om de functie in te schakelen.

1. Ga naar **Systeembeheer** \> **Werkruimten** \> **Functiebeheer**.
1. Zoek de functie **Voorraadbuffers en voorraadniveaus inschakelen**, selecteer de rij en selecteer **Nu inschakelen**.

Nadat de functie is ingeschakeld, kunt u voorraadniveaus zoeken in **Retail en Commerce \> Voorraadbeheer**.

## <a name="create-and-configure-an-inventory-level-profile"></a>Een voorraadniveauprofiel maken en configureren

Een *voorraadniveauprofiel* bepaalt of een bepaalde status van een producthoeveelheid wordt beschouwd als op voorraad, niet op voorraad of een andere aangepaste status. U kunt meerdere voorraadniveauprofielen per rechtspersoon maken en configureren. Elk profiel bestaat uit een set voorraadniveaus en elk niveau wordt gedefinieerd door een *bereik*, een *code* en een *label*.

- **Bereik**: elk bereik wordt gedefinieerd door een *beginhoeveelheid* en een *eindhoeveelheid*. Een hoeveelheidswaarde valt in een bereik als deze meer is dan de beginhoeveelheid van dat bereik en niet meer dan de eindhoeveelheid.
- **Code**: een code is een interne afkorting die voor het niveau staat. Klanten die rechtstreeks met de voorraad-API's worden geïntegreerd, kunnen codes gebruiken om extra logica te maken voor een bepaald voorraadniveau. Ze kunnen bijvoorbeeld de inkoopmogelijkheid voor een product uitschakelen wanneer de voorraadniveaucode is **NOV** (niet op voorraad) is.
- **Label**: een label is een duidelijk klantbericht dat een voorraadniveau doorgeeft aan klanten op een e-commercesite.

### <a name="create-an-inventory-level-profile"></a>Een voorraadniveauprofiel maken

Voer de volgende stappen uit om een voorraadniveauprofiel te maken.

1. Ga naar **Retail en Commerce** \> **Voorbeheer** \> **Voorraadniveaus**.
1. Selecteer in het actievenster de optie **Nieuw** en voer waarden in de velden **Profiel-id** en **Omschrijving** in.
1. Selecteer op het sneltabblad **Bereiken** de optie **Toevoegen** om een nieuw niveau toe te voegen en voer vervolgens waarden in de kolommen **Beginhoeveelheid**, **Eindhoeveelheid**, **Code** en **Label** in voor dat niveau. Herhaal deze stap om meer niveaus toe te voegen. Indien nodig kunt u de waarden in het gegevensraster bewerken of u kunt **Verwijderen** selecteren om een niveau te verwijderen.
1. Selecteer **Opslaan** in het actievenster.

Wanneer een nieuw profiel wordt gemaakt, worden twee voorraadniveaus automatisch geïnitialiseerd:

- **NOV**: het niveau Niet op voorraad, waarbij de ondergrens van het bereik negatief oneindig is. De beginhoeveelheid en code kunnen niet worden bewerkt voor dit niveau.
- **BESCH**: het niveau Beschikbaar, waarbij de bovengrens van het bereik oneindig is. De eindhoeveelheid en code kunnen niet worden bewerkt voor dit niveau.

> [!NOTE]
> Er kunnen geen gaten of overlappen tussen de bereiken in de profieldefinitie bestaan.

Met de knop **Vertalingen** in het actievenster kunt u gelokaliseerde tekenreeksen voor het labelbericht configureren. U moet vervolgens de distributieplanningstaak **1110** (**Globale configuratie**) uitvoeren om de gelokaliseerde tekenreeksen naar kanalen te synchroniseren.

### <a name="configure-an-inventory-level-profile"></a>Een voorraadniveauprofiel configureren

U kunt een voorraadniveauprofiel configureren op het niveau van de productcategorie of het afzonderlijke productniveau. Wanneer een voorraadniveauprofiel is geconfigureerd voor een product, wordt het voorraadniveau bepaald op basis van de bereiken die zijn gedefinieerd in het gekoppelde profiel. Anders wordt het voorraadniveau Beschikbaar of Niet op voorraad bepaald op basis van het feit of het product een positieve voorhanden hoeveelheid heeft.

Voer de volgende stappen uit om een voorraadniveauprofiel voor een categorie te configureren.

1. Ga naar **Retail en Commerce** \> **Producten en categorieën** \> **Commerce-producthiërarchie**.
1. Selecteer de categorie om een voorraadniveauprofiel voor te configureren.
1. Selecteer een rechtspersoon op het sneltabblad **Eigenschappen verkooppoduct**.
1. Selecteer in de sectie **Commerce-voorraad** in het veld **Voorraadniveauprofiel** een van de vooraf gedefinieerde profielen voor voorraadniveaus.

Met de knop **Producten bijwerken** in het actievenster kunt u de waarde van het profiel op categorieniveau doorgeven aan de onderliggende producten van de categorie. Zie [Productcategorieën en producten beheren](category-management-product-creation.md) voor meer informatie.

Voer de volgende stappen uit om een voorraadniveauprofiel voor een vrijgegeven product te configureren.

1. Ga naar **Retail en Commerce** \> **Producten en categorieën** \> **Vrijgegeven producten per categorie**.
1. Selecteer een product en open vervolgens de pagina met productgegevens.
1. Selecteer op het sneltabblad **Verkopen** in de sectie **Commerce-voorraad** in het veld **Voorraadniveauprofiel** een van de vooraf gedefinieerde profielen voor voorraadniveaus.

Wanneer een nieuw product wordt gemaakt, wordt het veld **Voorraadniveauprofiel**, net als vele andere kenmerken op productniveau, ingesteld op de waarde die is geconfigureerd voor de categorie waaraan het product is gekoppeld.

> [!NOTE]
> Het voorraadniveauprofiel is een specifiek kenmerk voor rechtspersonen. Voor dezelfde categorie of hetzelfde product kan de waarde voor voorraadniveauprofiel per rechtspersoon verschillen.

Voer de volgende stappen uit om de configuraties van voorraadniveauprofielen te synchroniseren naar kanalen.

1. Ga naar **Retail en Commerce** \> **Retail en Commerce IT** \> **Distributieplanning**.
1. Voer de distributieplanning **1040** (**Product**) uit.

## <a name="configure-an-inventory-buffer"></a>Een voorraadbuffer configureren

De *voorraadbuffer* is een door de gebruiker gedefinieerde waarde waarmee de extra hoeveelheid van een artikel wordt afgetrokken van de oorspronkelijke hoeveelheid om de geschatte hoeveelheid te berekenen. Deze geschatte hoeveelheid geeft detailhandelaren een veilige buffer, zodat er niet meer van een product wordt verkocht dan de werkelijke voorhanden voorraad. U kunt de voorraadbuffer configureren op het niveau van de productcategorie of het afzonderlijke productniveau. Als er geen vooraadbuffer is opgegeven, wordt de standaardwaarde **0** (nul) gebruikt.

Voer de volgende stappen uit om de voorraadbuffer voor een categorie te configureren.

1. Ga naar **Retail en Commerce** \> **Producten en categorieën** \> **Commerce-producthiërarchie**.
1. Selecteer de categorie waarvoor u de voorraadbuffer wilt configureren.
1. Selecteer een rechtspersoon op het sneltabblad **Eigenschappen verkooppoduct**.
1. Voer in de sectie **Commerce-voorraad** in het veld **Voorraadbuffer** een positieve waarde in.

Met de knop **Producten bijwerken** in het actievenster kunt u de waarde van de buffer op categorieniveau doorgeven aan de onderliggende producten van de categorie. Zie [Productcategorieën en producten beheren](category-management-product-creation.md) voor meer informatie.

Voer de volgende stappen uit om de voorraadbuffer voor een vrijgegeven product te configureren.

1. Ga naar **Retail en Commerce** \> **Producten en categorieën** \> **Vrijgegeven producten per categorie**.
1. Selecteer een product en open vervolgens de pagina met productgegevens.
1. Voer op het tabblad **Verkopen** in de sectie **Commerce-voorraad** in het veld **Voorraadbuffer** een positieve waarde in.

Wanneer een nieuw product wordt gemaakt, wordt het veld **Voorraadbuffer** ingesteld op de waarde die is geconfigureerd voor de categorie waaraan het product is gekoppeld.

> [!NOTE]
> Als zowel de voorraadbuffer als de voorraadniveauprofielen voor een product zijn geconfigureerd, wordt de geschatte hoeveelheid van het product (de oorspronkelijke hoeveelheid min de bufferwaarde) gebruikt voor het berekenen van het voorraadniveau.

Voer de volgende stappen uit om de configuraties van voorraadbuffers te synchroniseren naar kanalen.

1. Ga naar **Retail en Commerce** \> **Retail en Commerce IT** \> **Distributieplanning**.
1. Voer de distributieplanning **1040** (**Product**) uit.

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Voorraadbuffers en voorraadniveaus gebruiken in een e-commerce-scenario

In Commerce Site Builder worden de mogelijkheden voor voorraadbuffers en voorraadniveaus in Commerce Headquarters gebruikt om berichten over de beschikbaarheid van voorraad op e-commerce-sites te bepalen. Zie [Voorraadinstellingen toepassen](inventory-settings.md) voor meer informatie.

Als u integreert met een e-commerce-oplossing van derden, kunt u ook de API's **GetEstimatedAvailability** en **GetEstimatedProductWarehouseAvailability** gebruiken om de beschikbaarheid van voorraad voor een product in uw e-commerce-scenario weer te geven. Zie [Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen](calculated-inventory-retail-channels.md)  voor meer informatie over deze API's.

Door de introductie van voorraadbuffers en voorraadniveaus kunnen deze API's de voorraadniveaucodes retourneren en berichten labelen die worden bepaald op basis van de totale beschikbaarheid en de beschikbare fysieke waarden. De API's kunnen verder worden geconfigureerd om te bepalen of de voorraadhoeveelheid samen met het bericht wordt geretourneerd en of de beschikbare hoeveelheid wordt verminderd met de voorraadbufferwaarde.

Voer de volgende stappen uit om de respons van de API's voor productbeschikbaarheid te configureren.

1. Ga naar **Retail en Commerce** \> **Instelling van hoofdkantoor** \> **Parameters** \> **Commerce-parameters**.
1. In de sectie **Winkelvoorraad** op het tabblad **Voorraad** selecteert u een waarde in het veld **API's voor productbeschikbaarheid vor e-commerce**.
1. Voer de distributieplanningstaak **1110** (**Algemene configuratie**) uit om de instellingen toe te passen op kanalen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Productcategorieën en producten beheren](category-management-product-creation.md)

[Voorraadinstellingen toepassen](inventory-settings.md)

[Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen](calculated-inventory-retail-channels.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
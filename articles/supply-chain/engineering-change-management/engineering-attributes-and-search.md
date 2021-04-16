---
title: Technische kenmerken en de zoekfunctie voor technische kenmerken
description: In dit onderwerp wordt uitgelegd hoe u met technische kenmerken alle niet-standaardkenmerken kunt opgeven om er zeker van te zijn dat alle productmodelgegevens in het systeem kunnen worden geregistreerd. Verder wordt uitgelegd hoe u de zoekfunctie voor technische kenmerken kunt gebruiken om producten eenvoudig te vinden op basis van die geregistreerde kenmerken.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 01752bfc9bab662064baf30635ae6879358c5bbe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830071"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Technische kenmerken en de zoekfunctie voor technische kenmerken

[!include [banner](../includes/banner.md)]

Als u er zeker van wilt zijn dat alle productmodelgegevens in het systeem kunnen worden geregistreerd, moet u technische kenmerken gebruiken om alle niet-standaardkenmerken op te geven. Vervolgens kunt u de zoekfunctie voor technische kenmerken gebruiken om producten eenvoudig te vinden op basis van die geregistreerde kenmerken.

## <a name="engineering-attributes"></a>Technische kenmerken

Technische producten hebben doorgaans veel kenmerken en eigenschappen die u moet vastleggen. Hoewel u sommige eigenschappen kunt registreren met behulp van de standaardproductvelden, kunt u ook waar nodig nieuwe technische eigenschappen maken. U kunt uw eigen *technische kenmerken* definiëren en deze onderdeel van de productdefinitie maken.

### <a name="create-engineering-attributes-and-attribute-types"></a>Technische kenmerken en kenmerktypen maken

Elk technisch kenmerk moet behoren tot een *kenmerktype*. Deze vereiste bestaat omdat elk technisch kenmerk een *gegevenstype* moet hebben dat definieert welke de typen waarden het kan bevatten. Een type technisch kenmerk kan een standaardtype zijn (zoals vrije tekst, een geheel getal of een decimaal) of een aangepast type (zoals tekst met een specifieke set waarden waaruit u kunt kiezen). U kunt elk kenmerktype opnieuw gebruiken met elk aantal technische kenmerken.

#### <a name="set-up-engineering-attribute-types"></a>Typen technische kenmerken instellen

Voer de volgende stappen uit om een type technisch kenmerk weer te geven, te maken of te bewerken.

1. Ga naar **Technisch wijzigingsbeheer \> Instellen \> Kenmerken \> Kenmerktypen**.
1. Selecteer een bestaand type kenmerk in het lijstvenster of selecteer **Nieuw** in het actievenster om een nieuw kenmerktype te maken.
1. Stel de volgende velden in:

    - **Naam van kenmerktype**: voer een naam in voor het kenmerktype.
    - **Type**: selecteer een standaardgegevenstype (*Valuta*, *Datum/tijd*, *Decimaal*, *Geheel getal*, *Tekst*, *Booleaanse waarde* of *Verwijzing*).
    - **Vaste lijst**: deze optie is alleen beschikbaar als u het veld **Type** instelt op *Tekst*. Stel dit in op *Ja* om specifieke waarden te definiëren voor kenmerken van dit type. In dit geval wordt een vervolg keuzelijst gemaakt. U gebruikt het sneltabblad **Waarde** om de beschikbare waarden voor dit kenmerktype vast te leggen. Stel deze optie in op *Nee* als u wilt toestaan dat gebruikers elke waarde kunnen invoeren. In dit geval wordt er een invoerveld gemaakt.
    - **Waardebereik**: deze optie is alleen beschikbaar als u het veld **Type** instelt op *Geheel getal*, *Decimaal* of *Valuta*. Stel *Ja* in om minimum- en maximumwaarden vast te leggen die worden geaccepteerd voor kenmerken van dit type. U gebruikt het sneltabblad **Bereik** om de minimum- en maximumwaarden vast te stellen en (voor valuta) de valuta die van toepassing is op de limieten die u hebt ingevoerd. Stel *Nee* in als u elke waarde wilt accepteren. 
    - **Maateenheid**: dit veld is alleen beschikbaar als u het veld **Type** instelt op *Geheel getal* of *Decimaal*. Selecteer de maateenheid die van toepassing is op dit type kenmerk. Als er geen eenheid vereist is, laat u dit veld leeg.

#### <a name="set-up-engineering-attributes"></a>Technische kenmerken instellen

Voer de volgende stappen uit om een technisch kenmerk weer te geven, te maken of te bewerken.

1. Ga naar **Technisch wijzigingsbeheer \> Instellen \> Kenmerken \> Technische kenmerken**.
1. Selecteer een bestaand kenmerk in het lijstvenster of selecteer **Nieuw** in het actievenster om een nieuw kenmerk te maken.
1. Stel de volgende velden in:

    - **Naam**: voer een naam in voor het kenmerk. Deze naam wordt alleen weergegeven op de pagina **Technische kenmerken**. Elders in het systeem wordt de waarde van het veld **Beschrijvende naam** doorgaans weergegeven om het kenmerk aan te duiden.
    - **Type kenmerk**: selecteer een kenmerktype dat u in de vorige sectie hebt gedefinieerd.
    - **Beschrijvende naam**: voer een naam in waarmee het kenmerk in het systeem wordt aangeduid (behalve op de pagina **Technische kenmerken**). 
    - **Beschrijving**: voer een beschrijving van het kenmerk in.
    - **Help-tekst**: voer Help-tekst in waarmee andere gebruikers wordt verteld waarvoor het kenmerk is.
    - **Standaardwaarde**: voer een standaardwaarde voor het kenmerk in. Welke opties worden weergegeven, is afhankelijk van het geselecteerde kenmerktype.
    - **Valuta**: als het geselecteerde kenmerktype een valuta is, selecteert u de valuta die het kenmerk accepteert en waarin waarden worden weergegeven.

1. Als het geselecteerde kenmerktype een geheel getal of decimaal is, wordt het sneltabblad **Bereik** weergegeven. Stel op dit sneltabblad de volgende velden naar wens in:

    - **Tolerantieactie**: selecteer hoe het systeem moet reageren als een gebruiker een waarde buiten het opgegeven bereik invoert. Als u *Waarschuwing* selecteert, wordt een waarschuwing weergegeven, maar kan de gebruiker de waarde wel opslaan. Als u *Niet toegestaan* selecteert, wordt een waarschuwing weergegeven en kan de waarde pas worden opgeslagen als de gebruiker deze corrigeert.
    - **Minimum**: voer de minimaal aanbevolen of geaccepteerde waarde in.
    - **Maximum**: voer de maximaal aanbevolen of geaccepteerde waarde in.

### <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Technische kenmerken koppelen aan een categorie van technische producten

Sommige technische kenmerken zijn van toepassing op alle producten, terwijl andere specifiek zijn bedoeld voor afzonderlijke producten of productcategorieën. Elektrische kenmerken zijn bijvoorbeeld niet vereist voor mechanische producten. Daarom kunt u *categorieën voor technische producten* instellen. Een categorie voor technische producten bepaalt de collectie technische kenmerken die deel moeten uitmaken van de definitie voor producten die tot die categorie behoren. U kunt ook opgeven welke technische kenmerken verplicht zijn en of er een standaardwaarde is.

Zie voor meer informatie over het werken met categorieën voor technische producten, waaronder informatie over het verbinden van kenmerken met categorieën, het onderwerp [Technische versies van en categorieën voor technische producten](engineering-versions-product-category.md).

### <a name="set-values-for-engineering-attributes"></a>Waarden voor technische kenmerken instellen

De technische kenmerken die aan een categorie voor technische producten zijn gekoppeld, worden weergegeven wanneer u een nieuw technisch product maakt dat op die categorie is gebaseerd. Op dat moment kunt u waarden voor de kenmerken instellen. Deze waarden kunnen later worden gewijzigd op de pagina **Technische versie** of als onderdeel van het beheer van technische wijzigingen in een order voor technische wijzigingen. Zie [Wijzigingen in technische producten beheren](engineering-change-management.md) voor meer informatie.

### <a name="create-an-engineering-product"></a>Een technisch product maken

Open de pagina **Vrijgegeven producten** om een technisch product te maken. Selecteer **Technisch product** in de groep **Nieuw** op het tabblad **Product** in het actievenster.

Geef de technische categorie op waartoe het product behoort. De categorie stelt alle standaardwaarden en -kenmerken voor het product in. Ook worden de kenmerken ingesteld die van toepassing zijn op het product. Nadat de categorie is geselecteerd, worden waarden voor de kenmerken ingesteld. U kunt deze waarden vervolgens wijzigen.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Producten zoeken met behulp van waarden van technische kenmerken

U kunt de zoekfunctie voor technische kenmerken gebruiken om producten te zoeken door te zoeken naar de waarden van de technische kenmerken. U kunt dus eenvoudig technische producten vinden op basis van hun kenmerken. U kunt zoeken in de producten die behoren tot een categorie voor technische producten of u kunt zoeken in alle technische producten.

De zoekfunctie is beschikbaar op pagina's met hoofdgegevens van producten en op basis van transactionele artikelen in het systeem, zoals verkooporders. Voor een transactioneel artikel kunt u de pagina **Zoeken naar technische kenmerken** gebruiken om naar een product te zoeken. U kunt vervolgens de knop **Toevoegen als nieuwe regel gebruiken** om het product aan de verkooporderregels toe te voegen. Producten in de zoekresultaten kunnen ook direct aan de order worden toegevoegd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Verschillende dimensies voor verpakking en opslag instellen
description: In dit onderwerp wordt aangegeven voor welk proces (verpakking, opslag of geneste verpakking) elke opgegeven dimensie wordt gebruikt.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078250"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Verschillende dimensies voor verpakking en opslag instellen

[!include [banner](../includes/banner.md)]

Sommige artikelen worden verpakt of opgeslagen op een manier die u mogelijk nodig hebt om fysieke dimensies op een andere manier bij te houden voor elk van de verschillende processen. Met de functie *Verpakkingsproductdimensie* kunt u voor elk product een of meer typen dimensies instellen. Elk dimensietype biedt een reeks fysieke afmetingen (gewicht, breedte, diepte en hoogte) en legt het proces vast waarin deze fysieke metingwaarden van toepassing zijn. Wanneer deze functie is ingeschakeld, ondersteunt het systeem de volgende typen dimensies:

- *Opslag*: opslagdimensies worden samen met locatievolumemaatstaven gebruikt om te bepalen hoeveel van elk artikel op diverse magazijnlocaties kan worden opgeslagen.
- *Verpakking*: verpakkingsdimensies worden gebruikt tijdens de containervorming en het handmatige verpakkingsproces om te bepalen hoeveel van elk artikel in de verschillende containertypen past.
- *Geneste verpakking*: geneste verpakkingsdimensies worden gebruikt wanneer het verpakkingsproces meerdere niveaus bevat.

*Opslag*: dimensies worden zelfs ondersteund wanneer de functie *Verpakkingsproductdimensie* niet is ingeschakeld. U stelt deze in via de pagina **Fysieke dimensie** in Supply Chain Management. Deze dimensies worden gebruikt door alle processen waarbij geen verpakkings- en geneste verpakkingsdimensies zijn opgegeven.

*Verpakkings*- en *geneste verpakkings* dimensies worden ingesteld met de pagina **Fysieke productdimensies** die wordt toegevoegd wanneer u de functie *Verpakkingsproductdimensie* inschakelt.
In dit onderwerp vindt u een scenario dat laat zien hoe u deze functie moet gebruiken.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>De functie Verpakkingsproductdimensie inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Verpakkingsproductdimensies*

## <a name="example-scenario"></a>Voorbeeldscenario

### <a name="set-up-the-scenario"></a>Het scenario configureren

Voordat u het voorbeeldscenario kunt uitvoeren, moet u het systeem voorbereiden zoals beschreven in deze sectie.

#### <a name="enable-demo-data"></a>Demogegevens inschakelen

Als u dit scenario wilt doorlopen met de hier opgegeven demorecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon *USMF* selecteren voordat u begint.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Een nieuwe fysieke dimensie aan een product toevoegen

Voeg als volgt een nieuwe fysieke dimensie voor een product toe:

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer het product met **Artikelnummer** *A0001*.
1. Open in het actievenster het tabblad **Voorraad beheren** en selecteer in de groep **Magazijn** de optie **Fysieke productdimensies**.
1. De pagina **Fysieke productdimensies** wordt geopend. Selecteer in het actievenster **Nieuw** om een nieuwe dimensie toe te voegen aan het raster met de volgende instellingen:
    - **Type fysieke dimensie** - *Verpakking*
    - **Fysieke eenheid** - *stuks*
    - **Gewicht** - *4*
    - **Gewichtseenheid** - *kg*
    - **Diepte** - *3*
    - **Hoogte** - *4*
    - **Breedte** - *3*
    - **Lengte** - *cm*
    - **Volume-eenheid** - *cm3*

Het veld **Volume** wordt automatisch berekend op basis van de instellingen **Diepte**, **Hoogte** en **Breedte**.

#### <a name="create-a-new-container-type"></a>Een nieuw containertype maken

Ga naar **Magazijnbeheer \> Instellingen \> Containers \> Containertypen** en maak een nieuwe record met de volgende instellingen:

- **Containertypecode** - *kleine doos*
- **Beschrijving** - *kleine doos*
- **Maximaal nettogewicht** - *50*
- **Volume** - *144*
- **Lengte** - *6*
- **Breedte** - *6*
- **Hoogte** - *4*

#### <a name="create-a-container-group"></a>Een containergroep maken

Ga naar **Magazijnbeheer \> Instellingen \> Containers \> Containergroepen** en maak een nieuwe record met de volgende instellingen:

- **Containergroep-id** - *kleine doos*
- **Beschrijving** - *kleine doos*

Voeg een nieuwe regel aan de sectie **Details** toe. Stel het **Containertype** in op *Kleine doos*.

#### <a name="set-up-a-container-build-template"></a>Een containervormingsjabloon instellen

Ga naar **Magazijnbeheer \> Instellingen \> Containers \> Containervormingssjablonen** en selecteer **Dozen**. Wijzig de **Containergroep-id** in *Kleine doos*.

### <a name="run-the-scenario"></a>Het scenario uitvoeren

Nadat u het systeem hebt voorbereid zoals beschreven in de vorige sectie, kunt u het scenario uitvoeren zoals beschreven in de volgende sectie.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Een verkooporder maken en een zending maken

In dit proces maakt u een zending op basis van de *verpakkings* dimensie van het artikel, waarvan de hoogte minder dan 3 is.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *63*

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Deze moet een nieuwe, lege regel bevatten in het raster op het sneltabblad **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *5*

1. Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.
1. Sluit de pagina.
1. Open in het actievenster het tabblad **Magazijn** en selecteer de optie **Vrijgeven aan magazijn** om werk voor het magazijn te maken.
1. Selecteer op het sneltabblad **Verkooporderregels** **Magazijn \> Details van zending**.
1. Open in het actievenster het tabblad **Transport** en selecteer **Containers weergeven**. Bevestig dat het artikel is verpakt in de twee containers van het type *Kleine doos*.

#### <a name="place-an-item-into-storage"></a>Een artikel in de opslag plaatsen

1. Open het mobiele apparaat, meld u aan bij magazijn 63 en ga naar **Voorraad \> Aanpassen in**.
1. Voer **Loc** = *SHORT-01* in. Maak een nieuwe nummerplaat met **Artikel** = *A0001* en **Hoeveelheid** = *1 st*.
1. Selecteer **OK**. U ontvangt de fout "Locatie SHORT-01 is mislukt omdat artikel A0001 niet in de opgegeven dimensies van de locatie past". Dit komt omdat de dimensies van het type *Opslag* van het product groter zijn dan de dimensies die in het locatieprofiel zijn opgegeven.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
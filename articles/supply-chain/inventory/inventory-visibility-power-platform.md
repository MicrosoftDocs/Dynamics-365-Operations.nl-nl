---
title: App Voorraadzichtbaarheid
description: In dit onderwerp wordt beschreven hoe u de app Voorraadzichtbaarheid gebruikt.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a60fc00642a77d3dc595a6222727637f0d7cd588
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475055"
---
# <a name="use-the-inventory-visibility-app"></a>De app Voorraadzichtbaarheid gebruiken

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In dit onderwerp wordt beschreven hoe u de app Voorraadzichtbaarheid gebruikt.

Voorraadzichtbaarheid biedt een modelgestuurde app voor visualisatie. De app bevat drie pagina's: **Configuratie**, **Operationele zichtbaarheid** en **Voorraadoverzicht**. De app biedt de volgende functies:

- De app biedt een gebruikersinterface (UI) voor een voorhanden configuratie en een zachte reservering.
- De app ondersteunt voorhanden voorraadquery's in realtime voor diverse dimensiecombinaties.
- De app biedt een gebruikersinterface voor het boeken van reserveringsaanvragen.
- De app biedt een aangepaste weergave van de voorhanden voorraad voor producten, samen met alle dimensies.

## <a name="prerequisites"></a>Vereisten

Installeer voordat u begint eerst de invoegtoepassing Voorraadzichtbaarheid en stel de app in zoals beschreven in [Voorraadzichtbaarheid installeren en instellen](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>De app Voorraadzichtbaarheid openen

Als u de app Voorraadzichtbaarheid wilt openen, meldt u zich aan bij uw Power Apps-omgeving en opent u **Voorraadzichtbaarheid**.

## <a name="configuration"></a><a name="configuration"></a>Configuratie

Op de pagina **Configuratie** van de app Voorraadzichtbaarheid kunt u de configuratie van voorhanden voorraad en zachte reservering instellen. Als u de invoegtoepassing hebt geïnstalleerd, bevat de standaardconfiguratie een standaardinstelling voor Microsoft Dynamics 365 Supply Chain Management (de `fno`-gegevensbron). U kunt de standaardinstelling controleren. Hierna kunt u op basis van uw bedrijfsbehoeften en de vereisten voor voorraadboekingen van uw externe systeem de configuratie wijzigen om de manier te standaardiseren waarop voorraadwijzigingen kunnen worden geboekt, geordend en opgevraagd in de verschillende systemen.

Zie [Voorraadzichtbaarheid configureren](inventory-visibility-configuration.md) voor de volledige informatie over het configureren van de oplossing.

## <a name="operational-visibility"></a>Operationele zichtbaarheid

Op de pagina **Operationele zichtbaarheid** worden de resultaten van een realtime voorhanden voorraadquery weergegeven op basis van verschillende dimensiecombinaties. Wanneer de functie *OnHandReservion* is ingeschakeld, kunt u ook reserveringsaanvragen boeken vanaf de pagina **Operationele zichtbaarheid**.

### <a name="on-hand-query"></a>Voorhanden query

Op het tabblad **Voorhanden query** worden de resultaten weergegeven van een realtime voorhanden voorraadquery.

Wanneer u het tabblad **Voorhanden query** selecteert, vraagt het systeem om uw referenties zodat het de Bearer-token kan ophalen dat nodig is om de query op de service Voorraadzichtbaarheid uit te voeren. U hoeft het Bearer-token alleen maar in het veld **Bearer-token** te plakken en het dialoogvenster te sluiten. U kunt vervolgens een voorhanden queryaanvraag boeken.

Als het Bearer-token niet geldig is of als dit is verlopen, moet u een nieuw token in het veld **Bearer-token** plakken. Voer de juiste waarden voor **Client-id**, **Tenant-id** en **Clientgeheim** in en selecteer vervolgens **Vernieuwen**. Het systeem haalt automatisch een nieuw, geldig Bearer-token op.

Als u een voorhanden query wilt boeken, voert u de query in de aanvraagbody in. Gebruik het patroon dat in [Een query uitvoeren met de post-methode](inventory-visibility-api.md#query-with-post-method)

![Voorhanden query-instellingen](media/inventory-visibility-query-settings.png "Voorhanden query-instellingen")

### <a name="reservation-posting"></a>Reserveringen boeken

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Gebruik het tabblad **Reserveringen boeken** om een reserveringsaanvraag te boeken. Voordat u een reserveringsaanvraag kunt boeken, moet u de functie *OnHandReservation* inschakelen. Zie [Reserveringen van Voorraadzichtbaarheid](inventory-visibility-reservations.md) voor meer informatie over deze functie.

Als u een reserveringsaanvraag wilt boeken, moet u een waarde in de aanvraagbody invoeren. Gebruik het patroon dat is beschreven in [Eén reserveringsgebeurtenis maken](inventory-visibility-api.md#create-one-reservation-event). Selecteer vervolgens **Boeken**. Als u details van het antwoord op de aanvraag wilt weergeven, selecteert u **Details weergeven**. U kunt ook de waarde `reservationId` uit de antwoorddetails ophalen.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Voorraadoverzicht

**Voorraadoverzicht** is een aangepaste weergave voor de entiteit *Inventory OnHand Sum*. Het overzicht biedt een voorraadoverzicht voor producten samen met alle dimensies. De overzichtsgegevens van de voorraad worden periodiek gesynchroniseerd vanuit Voorraadzichtbaarheid. Voordat u gegevens kunt bekijken op het tabblad **Voorraadoverzicht**, moet u de functie *OnHandMostSpecificBackoverzichtService* op het tabblad **Functiebeheer** inschakelen.

Met het **Geavanceerde filter** dat Dataverse biedt, kunt u een persoonlijke weergave maken met de rijen die belangrijk voor u zijn. Met de opties van het geavanceerde filter kunt u een breed scala weergaven maken, van eenvoudig tot complex. Met deze filters kunt u ook gegroepeerde en geneste voorwaarden aan de filters toevoegen. Zie [Persoonlijke weergaven maken of bewerken met geavanceerde rasterfilters](/powerapps/user/grid-filters-advanced) voor meer informatie over het gebruik van **Geavanceerd filter**.

Boven aan de aangepaste weergave ziet u drie velden: **Standaarddimensie**, **Aangepaste dimensie** en **Meting**. U kunt deze velden gebruiken om te bepalen welke kolommen worden weergegeven.

U kunt de kolomkop selecteren om het huidige resultaat te filteren of te sorteren.

Onder aan de aangepaste weergave wordt informatie weergegeven, zoals '50 records (29 geselecteerd)' of '50 records'. Deze informatie verwijst naar de op dat moment geladen records van het resultaat van **Geavanceerd filter**. De tekst '29 geselecteerd' verwijst naar het aantal records dat is geselecteerd met het kolomkoptekstfilter voor de geladen records.

Onder aan de weergave bevindt zich de knop **Meer laden** waarmee u meer records van Dataverse kunt laden. Het standaardaantal records dat wordt geladen, is 50. Als u **Meer laden** selecteert, worden de volgende 1000 beschikbare records in de weergave geladen. Het getal op de knop **Meer laden** geeft het momenteel geladen aantal records en het totale aantal records aan voor het resultaat van het **Geavanceerde filter**.

![Voorraadoverzicht](media/inventory-visibility-onhand-list.png "Voorraadoverzicht")

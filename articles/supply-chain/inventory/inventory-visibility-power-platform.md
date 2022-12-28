---
title: App Voorraadzichtbaarheid
description: In dit artikel wordt beschreven hoe u de app Voorraadzichtbaarheid gebruikt.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0a4e436cc1af6b71049f75fb66bdfb89ca38df9f
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831769"
---
# <a name="use-the-inventory-visibility-app"></a>De app Inventory Visibility gebruiken

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u de app Voorraadzichtbaarheid gebruikt.

Voorraadzichtbaarheid biedt een modelgestuurde app voor visualisatie. De app bevat drie pagina's: **Configuratie**, **Operationele zichtbaarheid** en **Voorraadoverzicht**. De app biedt de volgende functies:

- De app biedt een gebruikersinterface (UI) voor een voorhanden configuratie en een zachte reservering.
- De app ondersteunt voorhanden voorraadquery's in realtime voor diverse dimensiecombinaties.
- De app biedt een gebruikersinterface voor het boeken van reserveringsaanvragen.
- De app biedt een weergave van de voorhanden voorraad van producten, samen met alle dimensies.
- De app biedt een weergave van de voorhanden voorraadlijst voor producten, samen met vooraf gedefinieerde dimensies. De lijstweergave voor voorhanden voorraad kan een volledig overzicht zijn of een vooraf geladen resultaat van een voorraadquery.

## <a name="prerequisites"></a>Vereisten

Installeer voordat u begint eerst de invoegtoepassing Voorraadzichtbaarheid en stel de app in zoals beschreven in [Voorraadzichtbaarheid installeren en instellen](inventory-visibility-setup.md).

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a>De app Voorraadzichtbaarheid openen en verifiëren

Volg deze stappen om de app Voorraadzichtbaarheid te openen en te verifiëren.

1. Meld u aan bij uw Power Apps-omgeving.
1. Open de app **Voorraadzichtbaarheid**.
1. Open de pagina **Operationele zichtbaarheid** vanuit het linkerdeelvenster.
1. Selecteer de knop **Instellingen** (tandwielpictogram) bovenaan de pagina.
1. Voer in het dialoogvenster **Instellingen** de waarden **Client-id**, **Tenant-id** en **Clientgeheim** in die u hebt genoteerd bij [het installeren en instellen van Voorraadzichtbaarheid](inventory-visibility-setup.md).
1. Selecteer de knop **Vernieuwen** naast het veld **Bearer-token**. Er wordt een nieuw bearer-token gegenereerd op basis van de informatie die u hebt ingevoerd.

    ![Voorhanden query-instellingen.](media/inventory-visibility-query-settings.png "Voorhanden query-instellingen")

1. Wanneer u een geldig bearer-token ontvangt, sluit u het dialoogvenster. Het bearer-token vervalt na een bepaalde tijd. Daarom moet u deze soms vernieuwen wanneer u de configuratie moet bijwerken, gegevens moet plaatsen of querygegevens moet uitvoeren.

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a>De Voorraadzichtbaarheid-app configureren

Op de pagina **Configuratie** van de app Voorraadzichtbaarheid kunt u de configuratie voor algemeen gegevensbeheer en functies instellen. Als u de invoegtoepassing hebt geïnstalleerd, bevat de standaardconfiguratie een standaardinstelling voor Microsoft Dynamics 365 Supply Chain Management (de `fno`-gegevensbron). U kunt de standaardinstelling controleren. Daarna kunt u op basis van uw bedrijfsbehoeften en de vereisten voor voorraadboekingen van uw externe systeem de configuratie wijzigen om de manier te standaardiseren waarop voorraadwijzigingen kunnen worden geboekt, geordend en opgevraagd in de verschillende systemen.

Zie [Voorraadzichtbaarheid configureren](inventory-visibility-configuration.md) voor de volledige informatie over het configureren van de oplossing.

## <a name="operational-visibility"></a>Operationele zichtbaarheid

Op de pagina **Operationele zichtbaarheid** worden de resultaten van een realtime voorhanden voorraadquery, reserveringsboeking en toewijzing weergegeven op basis van verschillende dimensiecombinaties. Wanneer de functie *OnHandReservation* is [ingeschakeld](inventory-visibility-configuration.md), kunt u ook reserveringsaanvragen boeken vanaf de pagina **Operationele zichtbaarheid**.

### <a name="on-hand-query"></a>Voorhanden query

Op het tabblad **Query voorhanden** van de pagina **Operationele zichtbaarheid** kunt u een realtime voorhanden voorraadquery uitvoeren. Voer de onderstaande stappen uit om een query in te stellen en uit te voeren.

1. Open de app **Voorraadzichtbaarheid**.
1. Open de pagina **Operationele zichtbaarheid** vanuit het linkerdeelvenster.
1. Voer op het tabblad **Query voorhanden** de waarden **Organisatie-id**, **Site-id** en **Locatie-id** in die u wilt opvragen.
1. Voer in het veld **product-id** een of meer product-id's in om een exacte overeenkomst voor uw query te krijgen. Als u het veld **Product-id** leeg laat, bevatten de resultaten alle producten op de opgegeven site en locatie.
1. Als u een gedetailleerder resultaat wilt weergeven (bijvoorbeeld een weergave per dimensiewaarde, zoals kleur en grootte), selecteert u dimensies voor groeperen in het veld **Resultaat groeperen op**.
1. Als u artikelen wilt zoeken met een specifieke dimensiewaarde (zoals kleur = rood), selecteert u de dimensie in het veld **Filterdimensies** en voert u vervolgens een dimensiewaarde in.
1. Selecteer **Query**. Er wordt een bericht met succes (groen) of een mislukt (rood) weergegeven. Als de query mislukt, controleert u uw querycriteria en en of het [bearer-token](#open-authenticate) niet is vervallen.

Een andere manier om een query voor voorhanden voorraad te maken, is het uitvoeren van directe API-aanvragen. U kunt `/api/environment/{environmentId}/onhand/indexquery` of `/api/environment/{environmentId}/onhand` gebruiken. Zie [Openbare API's voor Voorraadzichtbaarheid](inventory-visibility-api.md) voor meer informatie.

### <a name="reservation-posting"></a>Reserveringen boeken

Gebruik het tabblad **Reserveringen boeken** op de pagina **Operationele zichtbaarheid** om een reserveringsaanvraag te plaatsen. Voordat u een reserveringsaanvraag kunt boeken, moet u de functie *OnHandReservation* inschakelen. Zie [Reserveringen van Voorraadzichtbaarheid](inventory-visibility-reservations.md) voor meer informatie over deze functie en hoe u deze kunt inschakelen.

> [!NOTE]
> De mogelijkheid om een zachte reservering te maken via de gebruikersinterface is bedoeld om u de functie te laten testen. Elke aanvraag voor zachte reservering moet worden gekoppeld aan een wijziging in de transactieorderregel (maken, wijzigen, verwijderen, e.d.). Daarom is het raadzaam om alleen zachte reserveringen te maken die aan een back-endorder zijn gekoppeld. Zie [Voorraadzichtbaarheid reserveringen](inventory-visibility-reservations.md) voor meer informatie.

Volg deze stappen om een aanvraag voor zachte reservering te boeken met behulp van de gebruikersinterface.

1. Open de app **Voorraadzichtbaarheid**.
1. Open de pagina **Operationele zichtbaarheid** vanuit het linkerdeelvenster.
1. Geef op het tabblad **Reserveringen boeken** in het veld **Hoeveelheid** op hoeveel u wilt reserveren.
1. Schakel het selectievakje **Negatieve voorraad inschakelen voor ondersteunen van te hoge verkoop** uit om te voorkomen dat er teveel voorraad wordt verkocht of gereserveerd.
1. Selecteer in het veld **Operator** de gegevensbron en de fysieke meting die van toepassing zijn op de zachte reserveringshoeveelheid.
1. Voer op het tabblad **Organisatie-id** de waarden **Site-id**, **Locatie-id** en **Product-id** in die u wilt opvragen.
1. Selecteer een gegevensbron, dimensies en dimensiewaarden om een gedetailleerder resultaat te krijgen.

Een andere manier om een zachte reservering te boeken, is het maken van directe API-aanvragen. Gebruik het patroon dat is beschreven in [Eén reserveringsgebeurtenis maken](inventory-visibility-api.md#create-one-reservation-event). Selecteer vervolgens **Boeken**. Als u details van het antwoord op de aanvraag wilt weergeven, selecteert u **Details weergeven**. U kunt ook de waarde `reservationId` uit de antwoorddetails ophalen.

### <a name="allocation"></a>Toewijzing

Zie [Voorraadtoewijzing voorraadzichtbaarheid](inventory-visibility-allocation.md) voor informatie over het beheren van toewijzingen via de gebruikersinterface en API's.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Voorraadoverzicht

De pagina **Voorraadoverzicht** biedt een voorraadoverzicht voor producten samen met alle dimensies. Het is een aangepaste weergave voor de entiteit *Inventory OnHand Sum*. De overzichtsgegevens van de voorraad worden periodiek gesynchroniseerd vanuit Voorraadzichtbaarheid.

Volg deze stappen om de pagina **Voorraadoverzicht** in te schakelen en de synchronisatiefrequentie in te stellen:

1. Open de pagina **Configuratie**.
1. Open het tabblad **Functiebeheer en instellingen**.
1. Stel de schakelknop voor de functie *OnHandMostSpecificBackgroundService* in op *Ja*.
1. Wanneer de functie is ingeschakeld, wordt de sectie **Serviceconfiguratie** beschikbaar en bevat deze een rij voor het configureren van de functie **OnHandMostSpecificBackgroundService**. Met deze instelling kunt u de frequentie kiezen waarmee voorraadoverzichtsgegevens worden gesynchroniseerd. Gebruik de knoppen **Omhoog** en **Omlaag** in de kolom **Waarde** om de tijd tussen synchronisatie te wijzigen (met een minimum van vijf minuten). Selecteer **Save**.

    ![De instelling OnHandMostSpecificBackgroundService](media/inventory-visibility-ohms-freq.png "De instelling OnHandMostSpecificBackgroundService")

1. Selecteer **Configuratie bijwerken** om alle wijzigingen op te slaan.

> [!NOTE]
> Met de functie *OnHandMostSpecificBackgroundService* worden alleen wijzigingen in voorhanden inventaris bijgehouden die hebben plaatsgevonden nadat u de functie hebt ingeschakeld. Gegevens voor producten die niet zijn gewijzigd nadat u de functie hebt ingeschakeld, worden niet van de voorraadservicecache naar de Dataverse-omgeving gesynchroniseerd. Als op uw pagina **Voorraadoverzicht** niet alle informatie wordt weergegeven die u verwacht, opent u Supply Chain Management en gaat u naar **Voorraadbeheer > Periodieke taken > Integratie met Voorraadoverzicht** en schakelt u de batchtaak uit en weer in. De eerste push wordt nu uitgevoerd, en alle gegevens worden de volgende 15 minuten gesynchroniseerd met de entiteit *Totaal voorhanden voorraad*. Als u deze functie *OnHandMostSpecificBackgroundService* wilt gebruiken, raden we u aan om deze in te schakelen voordat u wijzigingen in voorhanden voorraad aanbrengt en de batchtaak **Integratie van voorraadzichtbaarheid** inschakelt.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a>Vooraf laden van een gestroomlijnde voorhanden query

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management slaat veel informatie over uw huidige voorhanden voorraad op en maakt deze beschikbaar voor allerlei doeleinden. Vele bewerkingen en integraties van derden vereisen echter slechts een kleine subset van deze details, en het opvragen van het systeem voor al deze bewerkingen kan resulteren in grote gegevenssets die tijd nodig hebben om te worden samengesteld en overgedragen. Daarom kan de service voor voorraadzichtbaarheid periodiek een gestroomlijnde set voorhanden voorraadgegevens ophalen en opslaan om ervoor te zorgen dat geoptimaliseerde informatie continu beschikbaar is. De details van de opgeslagen voorhanden voorraadgegevens worden gefilterd op basis van configureerbare bedrijfscriteria, om ervoor te zorgen dat alleen de meest relevante informatie wordt opgenomen. Aangezien de gefilterde voorhanden voorraadlijsten lokaal worden opgeslagen in de service Voorraadzichtbaarheid en regelmatig worden bijgewerkt, ondersteunen ze snelle toegang, export van gegevens op aanvraag en de integratie met externe systemen.

De pagina **Overzicht voorraadzichtbaarheid vooraf laden** biedt een weergave voor de entiteit *Resultaten van voorhanden vooraf geladen index-query*. In tegenstelling tot de entiteit *Voorraadoverzicht* biedt de *Resultaten van voorhanden vooraf geladen index-query* een voorhanden voorraadlijst van producten met geselecteerde dimensies. Voorraadzichtbaarheid synchroniseert elke 15 minuten de vooraf geladen overzichtsgegevens.

Om gegevens te bekijken op het tabblad **Overzicht voorraadzichtbaarheid vooraf laden**, moet u de functie *OnHandIndexQueryPreloadBackgroundService* inschakelen. Zie [Query's vooraf geladen voorraadzichtbaarheid inschakelen en configureren](inventory-visibility-configuration.md#query-preload-configuration) voor instructies.

> [!NOTE]
> Net als de functie *OnHandMostSpecificBackgroundService* traceert de functie *OnHandIndexQueryPreloadBackgroundService* alleen wijzigingen in de voorhanden voorraad die hebben plaatsgevonden nadat u de functie hebt ingeschakeld. Gegevens voor producten die niet zijn gewijzigd nadat u de functie hebt ingeschakeld, worden niet van de voorraadservicecache naar de Dataverse-omgeving gesynchroniseerd. Als op uw pagina **Voorraadoverzicht** niet alle informatie wordt weergegeven die u verwacht, gaat u naar **Voorraadbeheer > Periodieke taken > Integratie met Voorraadoverzicht** en schakelt u de batchtaak uit en weer in. De eerste push wordt nu uitgevoerd en alle gegevens worden de volgende 15 minuten gesynchroniseerd met de entiteit *Resultaten van voorhanden vooraf geladen index-query*. Als u deze functie wilt gebruiken, raden we u aan om deze in te schakelen voordat u wijzigingen in voorhanden voorraad aanbrangt en de batchtaak **Integratie van voorraadzichtbaarheid** inschakelt.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>De voorraadoverzichten filteren en doorzoeken

Met het **Geavanceerde filter** dat Dataverse biedt, kunt u een persoonlijke weergave maken met de rijen die belangrijk voor u zijn. Met de opties van het geavanceerde filter kunt u een breed scala weergaven maken, van eenvoudig tot complex. Met deze filters kunt u ook gegroepeerde en geneste voorwaarden aan de filters toevoegen. Zie [Persoonlijke weergaven maken of bewerken met geavanceerde rasterfilters](/powerapps/user/grid-filters-advanced) voor meer informatie over het gebruik van geavanceerde filters.

De pagina **Voorraadoverzicht** bevat drie velden boven het raster (**Standaarddimensie**, **Aangepaste dimensie** en **Meting**) waarmee u kunt bepalen welke kolommen zichtbaar zijn. U kunt ook een willekeurige kolomkop selecteren om het huidige resultaat te filteren of te sorteren op die kolom. In de volgende schermopname markeren de beschikbare velden dimensie-, filter-, resultaattelling en ´meer laden´ op de pagina **Voorraadoverzicht**.

![De pagina Voorraadoverzicht.](media/inventory-visibility-onhand-list.png "De pagina Voorraadoverzicht")

Aangezien u vooraf de dimensies hebt gedefinieerd die worden gebruikt voor het laden van overzichtsgegevens, geeft de pagina **Overzicht voorraadzichtbaarheid vooraf laden** kolommen weer die aan dimensies zijn gerelateerd. *De dimensies kunnen niet worden aangepast.&mdash;Het systeem ondersteunt alleen site- en locatiedimensies voor vooraf geladen voorhanden voorraden.* De pagina **Overzicht voorraadzichtbaarheid vooraf laden** biedt filters die vergelijkbaar zijn met die op de pagina **Voorraadoverzicht**, behalve dat de dimensies al zijn geselecteerd. In de volgende schermopname markeert de filtervelden die beschikbaar zijn op de pagina **Overzicht voorraadzichtbaarheid vooraf laden**.

![Overzicht voorraadzichtbaarheid vooraf laden](media/inventory-visibility-preload-onhand-list.png "De pagina Overzicht voorraadzichtbaarheid vooraf laden")

Onderaan de pagina's **Overzicht voorraadzichtbaarheid vooraf laden** en **Voorraadoverzicht** vindt u informatie als "50 records (29 geselecteerd)" of "50 records". Deze informatie verwijst naar de op dat moment geladen records van het resultaat van **Geavanceerd filter**. De tekst '29 geselecteerd' verwijst naar het aantal records dat is geselecteerd met het kolomkoptekstfilter voor de geladen records. Er is ook een knop **Meer laden** waarmee u meer records van Dataverse kunt laden. Het standaardaantal geladen records is 50. Als u **Meer laden** selecteert, worden de volgende 1000 beschikbare records in de weergave geladen. Het getal op de knop **Meer laden** geeft het momenteel geladen aantal records en het totale aantal records aan voor het resultaat van het **Geavanceerde filter**.

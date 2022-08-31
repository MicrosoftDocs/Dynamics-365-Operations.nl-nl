---
title: Omleidingen configureren voor stappen in menu-items van mobiele apparaten
description: In dit artikel wordt beschreven hoe u omleidingen configureert voor menu-items zodat werknemers de huidige taak kunnen parkeren, een andere taak kunnen uitvoeren en vervolgens naar de oorspronkelijke taak kunnen terugkeren zonder dat er informatie verloren gaat.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 50f899cd7f28a4b7fd23db5f049de02896e8d8e9
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336120"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Omleidingen configureren voor stappen in menu-items van mobiele apparaten

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> De functies die in dit artikel worden beschreven, zijn alleen van toepassing op de nieuwe mobiele app van Warehouse Management. Deze hebben geen invloed op de oude magazijn-app, die nu is afgeschaft.

In dit artikel wordt beschreven hoe u omleidingen configureert voor menu-items zodat werknemers de huidige taak kunnen 'parkeren', een andere taak kunnen uitvoeren en vervolgens naar de oorspronkelijke taak kunnen terugkeren zonder dat er informatie verloren gaat.

Een omleiding is een apart menu-item dat u kunt openen vanuit een stap in een hoofdtaak. Aan het einde van de omleiding wordt de werknemer teruggestuurd naar de plaats waar ze de hoofdtaak hebben verlaten. Tijdens het configureren geeft u het menu-item op dat als omleiding moet fungeren. U selecteert ook welke veldwaarden uit de hoofdtaak automatisch moeten worden doorgestuurd (gekopieerd) naar de omleiding en daar worden ingevoerd. Daarom moet u weten waar in de taakstroom de omleiding beschikbaar moet zijn voor werknemers. U moet er ook voor zorgen dat de informatie die naar de omleiding moet worden gekopieerd, beschikbaar is voor die stap in de taakstroom.

## <a name="enable-detours-in-your-system"></a>Omleidingen in het systeem inschakelen

Voordat u omleidingen voor stappen in menu-items van mobiele apparaten kunt configureren, moet u de volgende procedure uitvoeren om de vereiste functies in te schakelen en de vereiste veldnamen te genereren in de mobiele app Warehouse Management.

1. Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.
1. Zorg ervoor dat de functie *stap-instructies voor de magazijn-app* is ingeschakeld voor het systeem. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld. Zie voor meer informatie over de *stapinstructies voor de Warehouse-app* de informatie in [Stappentitels en instructies voor de mobiele app Warehouse Management aanpassen](mobile-app-titles-instructions.md). Deze functie is een vereiste voor de functie *Omleidingen in de app Warehouse Management*.
1. Schakel de functie *Omleidingen van app Warehouse Management* in. Deze functie is de enige functie die in dit artikel wordt beschreven. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld.
1. Als de functie *Omleidingen van de app Warehouse Management* niet al was ingeschakeld, werk dan de veldnamen in de mobiele app Warehouse Management bij door te gaan naar **Warehouse management \> Instellingen \> Mobiel apparaat \> Veldnamen van Warehouse-app** en **Standaardinstelling aanmaken** te selecteren. Herhaal deze stap voor elke rechtspersoon (bedrijf) waar u de mobiele app Warehouse Management gebruikt. Zie [Velden configureren voor de mobiele app Magazijnbeheer](configure-app-field-names-priorities-warehouse.md) voor meer informatie.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Een omleiding configureren vanuit een menuspecifieke overschrijving

Gebruik de volgende procedure om een omleiding in te stellen vanuit een menuspecifieke overschrijving.

1. Maak een menuspecifieke overschrijving voor het relevante menu en de relevante stap, zoals beschreven in [Staptitels en instructies aanpassen voor de mobiele app Warehouse Management](mobile-app-titles-instructions.md).
1. Zoek de combinatie van de waarden **Stap-ID** en **Naam van het menu-item** die u wilt bewerken, en selecteer vervolgens de waarde in de kolom **Stap-ID**.
1. Geef op het sneltabblad **Beschikbare omleidingen (menu-items)** van de pagina die verschijnt, het menu-item op dat als omleiding moet fungeren. U kunt ook selecteren welke veldwaarden uit de hoofdtaak automatisch moeten worden gekopieerd naar en van de omleiding. Zie de scenario´s verderop in dit artikel voor voorbeelden over het gebruik van deze instellingen.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a>Voorbeeldscenario 1: Verzamelen voor verkoop waarbij een locatievraag als een omleiding fungeert

Dit scenario laat zien hoe u een locatievraag als een omleiding kunt configureren in een door de werknemer doorgestuurde taakstroom voor verkoop verzamelen. Door deze omleiding kunnen werknemers alle nummerplaten opzoeken op de locatie waar ze verzamelen en kunnen ze de nummerplaat kiezen die ze willen gebruiken om de verzameling te voltooien. Dit type omleiding kan handig zijn als de streepjescode is beschadigd en daardoor onleesbaar is voor het scannerapparaat. Het kan ook nuttig zijn als een werknemer moet weten wat er in het systeem werkelijk voorhanden is. Dit scenario werkt alleen als er wordt verzameld op nummerplaatlocaties.

### <a name="enable-sample-data"></a>Voorbeeldgegevens inschakelen

Als u de gespecifieerde voorbeeldrecords en -waarden wilt gebruiken om dit scenario te doorlopen, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd. U moet ook de rechtspersoon **USMF** selecteren voordat u begint.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Een menuspecifieke overschrijving maken en de omleiding configureren voor scenario 1

In deze procedure configureert u een omleiding voor het menu-item **Verzamelen voor verkoop** in de nummerplaatstap.

1. Ga naar **Warehouse management \> Instellen \> Mobiel apparaat \> Stappen voor mobiel apparaat**
1. Zoek de stap-ID met de naam *LicensePlateId* en selecteer deze.
1. Selecteer **Stapconfiguratie toevoegen** in het actievenster.
1. Gebruik in het vervolgkeuzedialoogvenster het veld **Menu-item** om *Verzamelen voor verkoop* te zoeken en selecteren.
1. Selecteer **OK**.
1. De detailpagina voor de overschrijving die u zojuist hebt gemaakt, wordt weergegeven. Selecteer op het sneltabblad **Beschikbare omleidingen (menu-items)** de optie **Toevoegen** op de werkbalk.
1. Selecteer in het dialoogvenster **Omleiding toevoegen** de optie **Locatieonderzoek** als de omleiding die beschikbaar zal zijn in de mobiele app Warehouse Management.
1. Selecteer **OK**.
1. Selecteer op het sneltabblad **Beschikbare omleidingen (menu-items)** de omleiding die u zojuist hebt toegevoegd en selecteer **Te verzenden velden selecteren** op de werkbalk.
1. Geef in het dialoogvenster **Velden selecteren voor verzenden** de informatie op die u wilt verzenden vanuit en naar de omleiding. In dit scenario stelt u werknemers in staat om de locatie waar ze moeten verzamelen, te gebruiken als invoer voor de locatieonderzoeksomleiding. Selecteer daarom in de sectie **Verzenden vanuit orderverzamelen** de optie **Toevoegen** op de werkbalk om een rij aan het raster toe te voegen. Stel daarna de volgende waarden in voor de nieuwe rij:

    - **Kopiëren uit Orderverzamelen:** *Locatie*
    - **Plakken in Locatieonderzoek:** *Locatie*

1. Omdat de omleiding in dit scenario wordt geconfigureerd voor de nummerplaatstap, is het handig als werknemers de nummerplaat van het onderzoek weer in de hoofdstroom kunnen brengen. Selecteer daarom in de sectie **Terugbrengen vanuit locatieonderzoek** de optie **Toevoegen** op de werkbalk om een rij aan het raster toe te voegen. Stel daarna de volgende waarden in voor de nieuwe rij:

    - **Kopiëren uit Locatieonderzoek:** *Nummerplaat*
    - **Plakken in Orderverzamelen:** *Nummerplaat*

1. Selecteer **OK**.

De omleiding is nu volledig geconfigureerd. Een knop om de omleiding **Locatieonderzoek** te starten wordt nu weergegeven op de nummerplaatstap voor het menu-item **Orderverzamelen**.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Verzamelen voor verkoop voltooien op een mobiel apparaat en de omleiding gebruiken

In deze procedure voltooit u een orderverzameling met de mobiele app Warehouse Management. U gebruikt de omleiding die u zojuist hebt geconfigureerd om de nummerplaat te zoeken die u gebruikt om de verzamelstap te voltooien.

1. Maak in Microsoft Dynamics 365 Supply Chain Management een verkooporder waarvoor een orderverzamelingsstap is vereist om te verzamelen van een locatie die met een nummerplaat wordt getraceerd. U moet daarna de verkooporder aan het magazijn vrijgeven. Noteer de werk-id die wordt gegenereerd.
1. Open de mobiele app Warehouse Management en meld u aan bij magazijn 24. (In de standaard demogegevens meldt u zich aan met *24* als gebruikers-id en *1* als wachtwoord.)
1. Selecteer het menu **Uitgaand** en dan het menu-item **Orderverzameling**.
1. Volg de instructies voor gegevensinvoer op het scherm om de werk-ID in te voeren die in stap 1 is gegenereerd.
1. Bij de stap die de tekst **Een nummerplaat scannen** bevat, opent u het menu met acties. Er moet een nieuwe knop met de naam **Locatieonderzoek** worden weergeven. Een pijl in de linkerbovenhoek geeft aan dat er een omleiding wordt begonnen met de knop. Selecteer **Locatieonderzoek**.
1. De omleiding wordt gestart. Op de volgende pagina bevestigt u de locatie die uit de hoofdstroom is gekopieerd.
1. In de lijst met beschikbare nummerplaten in de locatie, tikt u op de nummerplaat die u naar de hoofdstroom wilt kopiëren. Klik vervolgens op **Terug**.
1. U bent weer terug bij de hoofdstroom van verkoop verzamelen en de nummerplaat is hier vanaf de omleiding naar gekopieerd. Bevestig de waarde om door te gaan naar de volgende stap.
1. U kunt nu de rest van de standaardstroom voltooien door de gevraagde instructies voor de gegevensinvoer in te vullen.

Het magazijnwerk is nu voltooid. De werknemer heeft met succes een omleiding geopend om een secundaire taak (locatieonderzoek) uit te voeren zonder zijn plaats in de hoofdtaak te verliezen en heeft de informatie die nodig was om de hoofdtaak te voltooien teruggebracht.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>Voorbeeldscenario 2: artikelonderzoek met verplaatsings- en correctie-omleidingen

Dit scenario laat zien hoe u verplaatsingen en correcties als meerdere omleidingen kunt configureren in de taakstroom voor locatieonderzoek. Deze mogelijkheid kan handig zijn wanneer een werknemer op een locatie aankomt, vindt dat de voorraad op de locatie verschilt van wat in het systeem is geregistreerd en daarom goederen moet aanpassen of verplaatsen.

U kunt het locatieonderzoek vervangen door een nummerplaatonderzoek of een artikelonderzoek zoals u dat nodig hebt.

### <a name="enable-sample-data"></a>Voorbeeldgegevens inschakelen

Als u de gespecifieerde voorbeeldrecords en -waarden wilt gebruiken om dit scenario te doorlopen, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd. U moet ook de rechtspersoon **USMF** selecteren voordat u begint.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Een menuspecifieke overschrijving maken en de omleiding configureren voor scenario 2

In deze procedure configureert u een omleiding voor het menu-item **Verzamelen voor verkoop** in de nummerplaatstap.

1. Ga naar **Warehouse management \> Instellen \> Mobiel apparaat \> Stappen voor mobiel apparaat**
1. Zoek en selecteer de stap-ID met de naam *LocationInquiryList*.

    > [!NOTE]
    > Als u een artikelonderzoek wilt gebruiken in plaats van een locatieonderzoek, selecteert u een rij met de stap-ID *ItemInquiryList*. Als u een nummerplaatonderzoek wilt gebruiken, selecteert u een rij met de stap-ID *LPInquiryList*.

1. Selecteer **Stapconfiguratie toevoegen** in het actievenster.
1. Gebruik in het vervolgkeuzedialoogvenster het veld **Menu-item** om *Locatieonderzoek* te zoeken en selecteren.
1. Selecteer **OK**.
1. De detailpagina voor de overschrijving die u zojuist hebt gemaakt, wordt weergegeven. Selecteer op het sneltabblad **Beschikbare omleidingen (menu-items)** de optie **Toevoegen** op de werkbalk.
1. Selecteer in het dialoogvenster **Omleiding toevoegen** de optie **Verplaatsing** als de omleiding die beschikbaar zal zijn in de mobiele app Warehouse Management.
1. Selecteer **OK**.
1. Selecteer op het sneltabblad **Beschikbare omleidingen (menu-items)** de omleiding die u zojuist hebt toegevoegd en selecteer **Te verzenden velden selecteren** op de werkbalk.
1. Geef in het dialoogvenster **Velden selecteren voor verzenden** de informatie op die u wilt verzenden vanuit en naar de omleiding. In dit scenario verwacht u dat werknemers gaan zoeken naar nummerplaatlocaties. Het is daarom handig om de nummerplaat van het onderzoek te kopiëren naar de omleiding **Verplaatsing**. Selecteer in de sectie **Verzenden vanuit orderverzamelen** de optie **Toevoegen** op de werkbalk om een rij aan het raster toe te voegen. Stel daarna de volgende waarden in voor de nieuwe rij:

    - **Kopiëren uit Locatieonderzoek:** *Locatie*
    - **Plakken in Verplaatsing:** *LOC/LP*

    In deze omweg verwacht u geen informatie om terug te kopiëren, omdat de hoofdstroom een onderzoek was waarbij geen extra stappen vereist zijn.

1. Selecteer **OK**.

De omleiding is nu volledig geconfigureerd. Een knop om de omleiding **Verplaatsing** te starten wordt nu weergegeven op de nummerplaatstap voor het menu-item **Locatieonderzoek**.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Een locatieonderzoek uitvoeren op een mobiel apparaat en de omleiding gebruiken

In deze procedure voert u een locatieonderzoek uit met de mobiele app Warehouse Management. U gebruikt vervolgens de omleiding om een verplaatsing van goederen te voltooien.

1. Open de mobiele app Warehouse Management en meld u aan bij magazijn 24. (In de standaard demogegevens meldt u zich aan met *24* als gebruikers-id en *1* als wachtwoord.)
1. Selecteer het menu **Voorraad** en dan het menu-item **Locatieonderzoek**.
1. Hier kunt u een locatie invoeren waar u informatie over wilt opvragen, zoals *FL-001*.
1. Wanneer de lijst wordt weergegeven, tikt u op een van de kaarten in de lijst (laat de muisknop niet los) om de beschikbare omleidingen weer te geven.
1. Selecteer **Verplaatsing**.
1. De nummerplaat is gekopieerd van de kaart die u hebt geselecteerd. Bevestig de waarde.
1. U kunt nu de standaardtaakstroom volgen om de verplaatsing te voltooien. Nadat het werk is voltooid, opent u het menu Acties en selecteert u **Annuleren**.
1. U bent weer terug op de pagina **Locatieonderzoek**. De waarden worden niet automatisch bijgewerkt. Daarom moet u de pagina handmatig vernieuwen om de wijzigingen van de verplaatsingsomleiding weer te geven.

---
title: Gepropageerde velden configureren voor stappen in de mobiele app Warehouse Management
description: In dit artikel wordt beschreven hoe u specifieke informatie propageert en markeert voor stappen in de taakstromen voor de mobiele app Warehouse Management.
author: Mirzaab
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8ecca2d00b8753a405faa8d4c67c3cbb1eef6907
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218969"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Gepropageerde velden configureren voor stappen in de mobiele app Warehouse Management

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> De functies die in dit artikel worden beschreven, zijn alleen van toepassing op de nieuwe mobiele app van Warehouse Management. Deze hebben geen invloed op de oude magazijn-app, die nu is afgeschaft.

In dit artikel wordt beschreven hoe u specifieke informatie propageert en markeert voor stappen in de taakstromen voor de mobiele app Warehouse Management. Deze mogelijkheid kan de aandacht van werknemers op de belangrijkste velden helpen houden wanneer ze een stroom verwerken. Voor elke stap in elk proces kunnen beheerders selecteren welke velden moeten worden gepropageerd en gemarkeerd.

## <a name="enable-promoted-fields-in-your-system"></a>Gepropageerde velden in het systeem inschakelen

Voordat u gepropageerde velden kunt instellen, moet u de volgende procedure uitvoeren om de vereiste functies in te schakelen en de vereiste veldnamen te genereren in de mobiele app Warehouse Management.

1. Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.
1. Zorg ervoor dat de functie *stap-instructies voor de magazijn-app* is ingeschakeld voor het systeem. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld. Zie voor meer informatie over de *stapinstructies voor de Warehouse-app* de informatie in [Stappentitels en instructies voor de mobiele app Warehouse Management aanpassen](mobile-app-titles-instructions.md). Deze functie is een vereiste voor de functie *Gepropageerde velden van magazijnapp*.
1. Schakel de functie in die op de volgende manier wordt weergegeven:

    - **Module:** *Magazijnbeheer*
    - **Functienaam:** *Gepropageerde velden van magazijnapp*

    Deze functie is de functie die in dit artikel wordt beschreven.

1. Werk de veldnamen in de mobiele app Warehouse Management bij door te gaan naar **Magazijnbeheer \> Instellingen \> Mobiel apparaat \> Veldnamen van Warehouse-app** en **Standaardinstelling maken** te selecteren. Zie [Velden configureren voor de mobiele app Magazijnbeheer](configure-app-field-names-priorities-warehouse.md) voor meer informatie.
1. Herhaal de vorige stap voor elke rechtspersoon (bedrijf) waar u de mobiele app Warehouse Management gebruikt.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Gepropageerde velden configureren vanuit een menuspecifieke overschrijving

U kunt de volgende procedure gebruiken om gepropageerde velden in te stellen.

1. Maak een menuspecifieke overschrijving voor het relevante menu en de relevante stap, zoals beschreven in [Staptitels en instructies aanpassen voor de mobiele app Warehouse Management](mobile-app-titles-instructions.md).
1. Zoek de combinatie van de waarden **Stap-ID** en **Naam van het menu-item** die u wilt bewerken, en selecteer vervolgens de waarde in de kolom **Stap-ID**.
1. Selecteer op de pagina die verschijnt, het sneltabblad **Gepropageerde velden selecteren** en **Velden selecteren** op de werkbalk.
1. Selecteer in het dialoogvenster **Gepropageerde velden** de velden die u wilt propageren. U kunt ook maximaal twee van de geselecteerde velden markeren. Gemarkeerde velden worden vet weergegeven in de mobiele app Warehouse Management. Houd er bij het selecteren van velden rekening mee dat sommige schermen groot genoeg zijn om alleen de bovenste een of twee gepropageerde velden weer te geven. Zie het scenario verderop in dit artikel voor een voorbeeld over het gebruik van deze instellingen.

    > [!NOTE]
    > De lijst **Beschikbare velden** beperkt zich tot de velden die kunnen worden weergegeven voor het menu-item. Andere factoren (zoals artikelsamenstelling) bepalen echter of een veld werkelijk in de mobiele app Warehouse Management wordt weergegeven. Als u gepropageerde velden hebt geconfigureerd, worden alleen de geselecteerde velden weergegeven op de hoofdpagina van de mobiele app Warehouse Management. Werknemers kunnen echter nog steeds de resterende velden bekijken door te tikken op de detailpagina.

1. Selecteer **OK** om de instellingen toe te passen. Uw geselecteerde velden worden nu weergegeven op het sneltabblad **Gepropageerde velden selecteren**.

## <a name="example-scenario"></a>Voorbeeldscenario

### <a name="enable-sample-data"></a>Voorbeeldgegevens inschakelen

Als u de gespecifieerde voorbeeldrecords en -waarden wilt gebruiken om dit scenario te doorlopen, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd. U moet ook de rechtspersoon **USMF** selecteren voordat u begint.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Verzamelen voor verkoop configureren met gepropageerde stappen voor de nummerplaatstap

In deze procedure stelt u de gepropageerde en gemarkeerde velden in voor het menu-item **Verzamelen voor verkoop** in de nummerplaatstap.

1. Ga naar **Warehouse management \> Instellen \> Mobiel apparaat \> Stappen voor mobiel apparaat**
1. Zoek de stap-ID met de naam *LicensePlateId* en selecteer deze.
1. Selecteer **Stapconfiguratie toevoegen** in het actievenster.
1. Gebruik in het vervolgkeuzedialoogvenster het veld **Menu-item** om *Verzamelen voor verkoop* te zoeken en selecteren.
1. Selecteer **OK**.
1. De detailpagina voor de overschrijving die u zojuist hebt gemaakt, wordt weergegeven. Selecteer op het sneltabblad **Gepropageerde velden selecteren** de optie **Velden selecteren** op de werkbalk.
1. U kunt in het dialoogvenster **Gepropageerde velden** de velden selecteren die u wilt propageren en markeren. Zoek en selecteer de volgende velden in de lijst **Beschikbare velden** en gebruik de knoppen om de velden naar de lijst **Geselecteerde velden** te verplaatsen:

    - Locatie
    - Artikel
    - Productnaam
    - Voorraadstatus

1. Met de pijl-omhoog en pijl-omlaag kunt u de volgorde van de velden in de lijst **Geselecteerde velden** aanpassen. In de mobiele app Warehouse Management worden de velden weergegeven in de volgorde die u hier instelt.
1. Selecteer het veld **Locatie** en selecteer **Markeren**.
1. Selecteer **OK** om de configuratie op te slaan.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>De gepropageerde velden weergeven in de mobiele app Warehouse Management

In deze procedure opent u de mobiele app Warehouse Management en gaat u door de stappen om de velden weer te geven die u hebt gepropageerd en gemarkeerd in de vorige procedure.

1. Maak in Microsoft Dynamics 365 Supply Chain Management een verkooporder waarvoor een orderverzamelingsstap is vereist om te verzamelen van een locatie die met een nummerplaat wordt getraceerd. U moet daarna de verkooporder aan het magazijn vrijgeven. Noteer de werk-id die wordt gegenereerd.
1. Open de mobiele app Warehouse Management en meld u aan bij magazijn 24. (In de standaard demogegevens meldt u zich aan met *24* als gebruikers-id en *1* als wachtwoord.)
1. Selecteer het menu **Uitgaand** en dan het menu-item **Orderverzameling**.
1. Volg de instructies voor gegevensinvoer op het scherm om de werk-ID in te voeren die in stap 1 is gegenereerd.
1. In de stap met de tekst **Scan een nummerplaat** moet u de wijzigingen zien die u op de detailpagina hebt aangebracht. De velden worden weergegeven in de volgorde die u instelt voor de gepropageerde velden en het veld **Locatie** wordt vet weergegeven.

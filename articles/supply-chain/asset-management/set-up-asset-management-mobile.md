---
title: Mobiel werkgebied voor activabeheer instellen
description: In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 Supply Chain Management en de mobiele app Finance and Operations (Dynamics 365) kunt instellen voor het uitvoeren van een mobiel werkgebied voor activabeheer waarmee medewerkers taken voor activabeheer kunnen uitvoeren.
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 54da27a022dcc800438b96224370228aa8eed261
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226142"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Mobiel werkgebied voor activabeheer instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 Supply Chain Management en de mobiele app Finance and Operations (Dynamics 365) kunt instellen voor het uitvoeren van het mobiele werkgebied **Activabeheer** waarmee medewerkers taken voor activabeheer kunnen uitvoeren.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Onderhoudsmedewerkers instellen in Supply Chain Management

Voer de volgende stappen uit voor elke gebruiker die toegang nodig heeft tot het mobiele werkgebied **Activabeheer**.

1. Ga in Supply Chain Management naar **Human resources \> Medewerkers** en zorg ervoor dat er een medewerkersrecord bestaat voor de gebruiker die u wilt instellen. Maak desgewenst een nieuwe medewerkersrecord.
1. Ga naar **Activabeheer \> Instellingen \> Medewerkers \> Medewerkers** en zorg ervoor dat de medewerkersrecord die u in de vorige stap hebt geïdentificeerd (of gemaakt) is toegewezen aan een onderhoudsmedewerkersrecord. Maak waar nodig een nieuwe record voor de onderhoudsmedewerker en stel het veld **Medewerker** in op de medewerkersrecord uit de vorige stap.
1. Ga naar **Activabeheer \> Instellingen \> Medewerkers \> Onderhoudsmedewerkersgroepen** en zorg ervoor dat de onderhoudsmedewerkersrecord die u in de vorige stap hebt geïdentificeerd (of gemaakt), behoort tot een onderhoudsmedewerkersgroep.
1. Ga naar **Systeembeheer \> Gebruikers**.
1. Selecteer de relevante gebruiker in het raster.
1. Stel op het sneltabblad **Gebruikersgegevens** het veld **Persoon** in op de medewerkersaccount die u aan de huidige gebruikersaccount wilt koppelen. Deze medewerkersaccount moet de medewerkersrecord zijn die u in stap 1 hebt geïdentificeerd (of gemaakt) en die u in stap 2 aan een onderhoudsmedewerkerrecord hebt toegewezen.

> [!NOTE]
> Gebruikersmachtigingen en beveiligingsrollen zijn van toepassing op de functies van het mobiele werkgebied **Activabeheer**, net zoals deze van toepassing zijn op de functies van de gebruikersinterface Supply Chain Management. Daarom moet elke gebruiker die u instelt voor toegang tot het mobiele werkgebied **Activabeheer**, de beveiligingsrollen hebben die zijn vereist om vergelijkbare bewerkingen rechtstreeks in Supply Chain Management uit te voeren.

## <a name="publish-the-asset-management-mobile-workspace"></a>Het mobiele werkgebied Activabeheer publiceren

Als u activabeheerfuncties beschikbaar wilt maken in de mobiele app Finance and Operations (Dynamics 365), moet u het mobiele werkgebied **Activabeheer** publiceren.

1. Selecteer in Supply Chain Management de knop **Instellingen** (het tandwielsymbool in de rechterbovenhoek) en selecteer vervolgens **Mobiele app** in het menu.
1. Zoek in het dialoogvenster **Mobiele app beheren** de tegel **Activabeheer**. Als het de tekst "In metagegevens - niet gepubliceerd" bevat, is het werkgebied nog niet gepubliceerd. Als het de tekst "In metagegevens - gepubliceerd" bevat, is het werkgebied al gepubliceerd en kunt u de rest van deze procedure overslaan.

    ![Het dialoogvenster Mobiele app beheren](media/mobile-workspaces.png "Het dialoogvenster Mobiele app beheren")

1. Selecteer de tegel **Activabeheer** en selecteer **Publiceren** op de werkbalk. Na enkele seconden ontvangt u een melding dat het werkgebied met succes is gepubliceerd. Daarnaast moet de tekst op de tegel veranderen in 'In metagegevens - gepubliceerd'.

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>De mobiele app Finance and Operations (Dynamics 365) installeren en instellen

1. Ga naar een van de volgende app-stores om de app **Microsoft Finance and Operations (Dynamics 365)** op uw mobiele apparaat te installeren:

    - [Voor Google Android-apparaten](https://go.microsoft.com/fwlink/?linkid=850662)
    - [Voor Apple iOS-apparaten](https://go.microsoft.com/fwlink/?linkid=850663)

1. Open de app Finance and Operations (Dynamics 365). De aanmeldingspagina moet worden weergegeven. Voer in het veld **Aanmelden** uw Supply Chain Management-URL in of selecteer een recente URL in de lijst **Recente omgevingen** en tik op **Verbinden**.

    ![Aanmeldingspagina](media/mobile-app-sign-in.png "Aanmeldingspagina")

1. Als u wordt gevraagd de verbinding te bevestigen, schakelt u het selectievakje **Ik begrijp het** in en tikt u vervolgens op **Verbinden**.
1. Gebruik uw Microsoft-account op de pagina **Een rekening kiezen** om u aan te melden bij de mobiele toepassing.

    De pagina **Werkgebieden** wordt weergegeven. Op deze pagina worden alle mobiele werkgebieden weergegeven die door uw Supply Chain Management-exemplaar zijn gepubliceerd.

    ![Lijst met werkgebieden](media/mobile-app-workspaces.png "Lijst met werkgebieden")

1. Als u de rechtspersoon (bedrijf) moet veranderen, tikt u op de menuknop (waarnaar soms wordt verwezen als de hamburger of hamburgerknop) in de linkerbovenhoek en tik vervolgens op **Bedrijf wijzigen**.

    ![De rechtspersoon wijzigen](media/mobile-app-change-comp.png "De rechtspersoon wijzigen")

1. Selecteer op de pagina **Werkgebieden** het werkgebied waarmee u wilt werken om het te openen.

    ![Mobiel werkgebied voor activabeheer](media/mobile-app-asset-workspace.png "Mobiel werkgebied voor activabeheer")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Werken met het mobiele werkgebied Activabeheer

Zie [Het mobiele werkgebied Activabeheer gebruiken](asset-management-mobile-workspace.md) voor meer informatie over het werken met het mobiele werkgebied **Activabeheer**.

Zie de [Startpagina van mobiele app](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md) voor meer informatie over de mobiele app Finance and Operations (Dynamics 365).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
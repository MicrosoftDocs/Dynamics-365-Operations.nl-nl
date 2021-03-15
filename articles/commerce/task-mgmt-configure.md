---
title: Taakbeheer configureren
description: In dit onderwerp wordt beschreven hoe u functies voor taakbeheer configureert in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e880305d02fd9f10464fe3f65a2774a44da258c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006230"
---
# <a name="configure-task-management"></a>Taakbeheer configureren

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u functies voor taakbeheer configureert in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Voordat managers en werknemers die met Dynamics 365 Commerce werken de functies voor taakbeheer in Commerce kunnen gebruiken, moet taakbeheer worden geconfigureerd. Configuratiestappen omvatten het verlenen van machtigingen aan managers en werknemers, het distribueren van machtigingen aan POS-clients, het instellen van POS-meldingen en het configureren van de tegel **Taken** op de startpagina van een POS-toepassing.

## <a name="configure-permissions-for-store-managers"></a>Machtigingen voor winkelmanagers configureren

Elke werknemer in een bepaalde winkel kan alle taken weergeven die aan deze winkel zijn toegewezen. Ze kunnen ook de status bijwerken van de taken die aan hen zijn toegewezen. Persoonlijkheden zoals winkelmanagers moeten echter beschikken over machtigingen voor taakbeheer om taken te kunnen beheren van taken die aan de winkel zijn toegewezen en om taken met een enkel doel te kunnen maken.

Voer de volgende stappen uit om machtigingen voor taakbeheer voor winkelmanagers te configureren.

1. Ga naar **Detailhandel en commerce \> Werknemers \> Machtigingsgroepen**.
1. Selecteer een specifieke machtigingsgroep (bijvoorbeeld **Manager**) en selecteer vervolgens **Bewerken**.
1. Stel op het sneltabblad **Machtigingen** de optie **Taakbeheer toestaan** in op **Ja**.
1. Voeg op het sneltabblad **Meldingen** de bewerking **Taakbeheer** toe en voer een waarde in het veld **Weergavevolgorde** in. Voer bijvoorbeeld **2** in als de bewerking **Orderafhandeling** al een waarde voor **Weergavevolgorde** van **1** heeft.
    
> [!NOTE]
> Als een persoon die geen manager is de machtigingen voor taakbeheer moet hebben in het POS, kunt u deze persoon machtigen. U kunt ook een nieuwe machtigingsgroep voor niet-managers maken en de optie **Taakbeheer toestaan** instellen op **Ja**.

De volgende illustratie laat zien hoe u machtigingen voor taakbeheer kunt configureren voor winkelmanagers.

![Machtigingen voor taakbeheer configureren voor winkelmanagers](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Machtigingen voor werknemers configureren

Werknemers moeten over machtigingen beschikken om takenlijsten te kunnen maken, toewijzingscriteria te kunnen beheren en het terugkeerpatroon van een willekeurige takenlijst te kunnen configureren. Als u deze machtigingen wilt configureren, wijst u werknemers toe aa de rol **Taakbeheer detailhandel**.

Ga als volgt te werk om machtigingen te configureren voor een werknemer.

1. Ga naar **Detailhandel en commerce \> Werknemers \> Gebruikers**.
1. Selecteer een werknemer.
1. Selecteer op het sneltabblad **Rollen van gebruiker** op **Rollen toewijzen**.
1. Selecteer in het dialoogvenster **Rollen toewijzen aan gebruiker** de rol **Taakbeheer detailhandel** en selecteer vervolgens **OK**.

## <a name="distribute-permissions-to-pos-clients"></a>Machtigingen naar POS-clients distribueren

Voordat werknemers POS-clients kunnen gebruiken, moeten machtigingen worden gedistribueerd en gesynchroniseerd met deze clients.

Voer de volgende stappen uit om machtigingen naar POS-clients te distribueren.

1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**.
1. Selecteer de distributieplanning **1060** (**Personeel**) en selecteer vervolgens **Nu uitvoeren**.
1. Selecteer de distributieplanning **1070** (**Afzetkanaalconfiguratie**) en selecteer vervolgens **Nu uitvoeren**.

## <a name="configure-pos-notifications-for-tasks"></a>POS-meldingen voor taken configureren

Taakbeheer moet zo worden geconfigureerd dat er meldingen in de POS-toepassing beschikbaar zijn.

Ga als volgt te werk om POS-meldingen voor taken te configureren.

1. Ga naar **Detailhandel en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> POS-bewerkingen**.
1. Zoek bewerking **1400** (**Taakbeheer**) en schakel hiervoor het selectievakje **Meldingen inschakelen** in.

In de volgende afbeelding ziet u de bewerking **Taakbeheer** op de pagina **POS-bewerkingen**.

![Bewerking Taakbeheer op de pagina POS-bewerkingen](media/HQ-POS-Tasks-Notifications.png)

Zie [Meldingen over orders op het verkooppunt (POS) weergeven](notifications-pos.md) voor meer informatie over het configureren van POS-meldingen.

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>De tegel Taken configureren op de startpagina van een POS-toepassing

Zie [Schermindelingen voor het verkooppunt (POS)](pos-screen-layouts.md) voor informatie over het configureren en toevoegen van nieuwe knoppen aan een POS-schermindeling voordat u de tegel **Taken** configureert op de startpagina van een POS-toepassing.

Ga als volgt te werk om de tegel **Taken** te configureren op de startpagina van een POS-toepassing.

1. Ga naar **Detailhandel en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> Schermindelingen**.
1. Selecteer een schermindeling, selecteer een indelingsgrootte en selecteer een knoppenraster.
1. Selecteer **Designer** op het sneltabblad **Knoppenrasters** om het geselecteerde knoppenraster te bewerken.
1. Voeg een tegel **Taken** toe aan de desbetreffende sectie van de startpagina.

In de volgende afbeelding ziet u een voorbeeld van een tegel **Taken** op een POS-startpagina.

![Tegel Taken op een POS-startpagina](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van taakbeheer](task-mgmt-overview.md)

[Takenlijsten maken en taken toevoegen](task-mgmt-create-lists.md)

[Takenlijsten toewijzen aan winkels of werknemers](task-mgmt-assign-lists.md)

[Taakbeheer in POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
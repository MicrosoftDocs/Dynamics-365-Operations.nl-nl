---
title: Mobiel werkgebied voor activabeheer
description: Dit onderwerp bevat informatie over het mobiele werkgebied voor activabeheer.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: fd6f45a7dc9d062a3602499e89a6473b3b4aeaee
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278371"
---
# <a name="asset-management-mobile-workspace"></a>Mobiel werkgebied voor activabeheer

[!include [banner](../../includes/banner.md)]


Dit onderwerp bevat informatie over het mobiele werkgebied voor activabeheer. Met dit werkgebied kunnen gebruikers onderhoudsaanvragen en werkorders weergeven en maken. Gebruikers kunnen de toegewezen werkordertaken ook weergeven in een kalender- of een lijstweergave. Activa en functionele locaties kunnen ook worden weergegeven en gezocht.


## <a name="overview"></a>Overzicht

Activabeheer is een geavanceerde module voor het beheren van activa en werkordertaken in Dynamics 365 Supply Chain Management. Met het mobiele werkgebied voor **activabeheer** kunnen gebruikers snel toegewezen werkordertaken weergeven op het mobiele apparaat van hun keuze. Gebruikers kunnen ook onderhoudsverzoeken maken en beheren, de levenscyclusstatus bijwerken en gegevens over activa en functionele locaties bekijken met behulp van hun mobiele apparaat.

Gebruikers kunnen met het mobiele werkgebied **Activabeheer** de volgende taken uitvoeren:

- Onderhoudsverzoeken maken, weergeven en bewerken, een foto nemen of een bestaande afbeelding aan het onderhoudsverzoek koppelen, de status van de levenscyclus van het onderhoudsverzoek wijzigen. 
- Werkorders maken, weergeven en bewerken, een foto nemen of een bestaande afbeelding aan de werkorder koppelen, de levenscyclusstatus van de werkorder wijzigen, werkordertaken weergeven.
- Toegewezen werkordertaken weergeven in een kalenderweergave.
- Werkordertaken maken, weergeven en bewerken, activatellers bijwerken, onderhoudscontrolelijsten weergeven, notities over werkordertaken weergeven en bewerken, de hulpmiddelen voor de werkordertaak weergeven.
- Een specifiek activum of een functionele locatie weergeven of zoeken.


## <a name="prerequisites"></a>Vereisten

De vereisten verschillen, afhankelijk van de versie van Dynamics 365 Supply Chain Management die voor uw organisatie is geïmplementeerd.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-supply-chain-management"></a>Vereisten als u Microsoft Dynamics 365 Supply Chain Management gebruikt 
Als Microsoft Dynamics 365 Supply Chain Management is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Activabeheer** publiceren. Zie voor meer informatie [Een mobiel werkgebied publiceren](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren
Download en installeer de mobiele app Dynamics 365 for Unified Operations:

- [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
- [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app
1. Start de app op uw mobiele apparaat.

2. Voer uw Dynamics 365-URL in.

3. De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren. Voer uw referenties in.

4. Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven. Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.

![Figuur 1](media/am-mobile-01.png)


## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Toegewezen werkordertaken weergeven in een kalenderweergave

1. Open op uw mobiele apparaat het werkgebied **Activabeheer**.

2. Selecteer **Mijn kalender met werkordertaken**.

3. Selecteer de datum waarvoor u werkordertaken wilt bekijken. In de lijst ziet u de activum-id en de functionele locatie-id voor elke werkordertaak.

4. Selecteer een werkordertaak in de lijst om taakdetails te bekijken: details over activa en functionele locaties en andere navigatiekoppelingen voor het weergeven van **bijlagen**, **controlelijsten**, **hulpmiddelen**, **activatellers**, **notities**, **journalen**.

![Figuur 2](media/am-mobile-02.png)


## <a name="create-a-work-order-job"></a>Een werkordertaak maken

1. Open op uw mobiele apparaat het werkgebied **Activabeheer**.

2. Selecteer **Alle onderhoudswerkorders**.

3. Selecteer de werkorder waarvoor u een nieuwe werkordertaak wilt maken.

4. Selecteer de knop **Regel toevoegen**.

5. Selecteer het **Activum** waarvoor u een nieuwe werkordertaak wilt maken.

6. Selecteer **Type onderhoudstaak**, **Variant van type onderhoudstaak** en **Specialisme**.

7. Selecteer **Gereed**.

![Figuur 3](media/am-mobile-03.png)


## <a name="add-attachment-to-a-work-order-job"></a>Bijlagen aan een werkordertaak toevoegen

1. Open op uw mobiele apparaat het werkgebied **Activabeheer**.

2. Selecteer **Alle onderhoudswerkorders**.

3. Selecteer de werkorder > werkordertaak waaraan u een bijlage wilt toevoegen.
    - U kunt ook **Mijn kalender met werkordertaken** of **Mijn lijst met werkordertaken** selecteren op de startpagina om naar de pagina **Werkordertaakgegevens** te navigeren.

4. Selecteer **Bijlagen** op de pagina **Werkordertaakgegevens**.

5. U ziet bestaande bijlagen voor de werkordertaak. Selecteer **Bijlage toevoegen**.

6. Voer **Naam** en **Notities** voor de bijlage in.

7. Selecteer **Afbeelding kiezen** als u een foto uit de mobiele galerie wilt selecteren of **Foto maken** om een foto te maken.

8. Selecteer **Gereed**.

![Figuur 4](media/am-mobile-04.png)


## <a name="view-maintenance-checklist-on-a-work-order-job"></a>Controlelijst voor een werkordertaak weergeven

1. Open op uw mobiele apparaat het werkgebied **Activabeheer**.

2. Selecteer **Alle onderhoudswerkorders**.

3. Selecteer de werkorder > werkordertaak waarvoor u de controlelijsten wilt weergeven.
    - U kunt ook **Mijn kalender met werkordertaken** of **Mijn lijst met werkordertaken** selecteren op de startpagina om naar de pagina **Werkordertaakgegevens** te navigeren.

4. Selecteer **Controlelijsten** op de pagina **Werkordertaakgegevens**.

5. U ziet een lijst met controlelijstregels die betrekking hebben op de werkordertaak. Selecteer een controlelijstregel om **Instructies** weer te geven en **Notities** toe te voegen.

6. Selecteer de knop Terug (**<**) om terug te gaan naar de vorige pagina.

![Figuur 5](media/am-mobile-05.png)


## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Activatellers op een werkordertaak weergeven en bijwerken

1. Open op uw mobiele apparaat het werkgebied **Activabeheer**.

2. Selecteer **Alle onderhoudswerkorders**.

3. Selecteer de werkorder > werkordertaak waarvoor u de activatellers wilt weergeven.
    - U kunt ook **Mijn kalender met werkordertaken** of **Mijn lijst met werkordertaken** selecteren op de startpagina om naar de pagina **Werkordertaakgegevens** te navigeren.

4. Selecteer **Activatellers** op de pagina **Werkordertaakgegevens**.

5. U ziet een lijst met activatellers die betrekking hebben op de werkordertaak. Selecteer het potloodpictogram op de regel van de activateller om de tellerwaarde bij te werken.

6. Voer een nieuwe tellerwaarde in en selecteer **Gereed**.

![Figuur 6](media/am-mobile-06.png)


## <a name="register-consumption-on-a-work-order-job"></a>Verbruik voor een werkordertaak registreren

1. Open op uw mobiele apparaat het werkgebied **Activabeheer**.

2. Selecteer **Alle onderhoudswerkorders**.

3. Selecteer de werkorder > werkordertaak waarvoor u de verbruikregistraties wilt toevoegen.
    - U kunt ook **Mijn kalender met werkordertaken** of **Mijn lijst met werkordertaken** selecteren op de startpagina om naar de pagina **Werkordertaakgegevens** te navigeren.

4. Selecteer **Journalen** op de pagina **Werkordertaakgegevens**.

5. Selecteer **Uren toevoegen** om werkuurregistraties te maken.
    1. Selecteer de **Categorie** uit de opzoekbewerking.
    2. Voer in het veld **Uren** het aantal werkuren in dat aan de werkordertaak is besteed.
    3. Selecteer de desbetreffende **Regeleigenschap**.
    4. Selecteer **Gereed**.

6. Selecteer **Artikelen toevoegen** om artikelregistraties te maken.
    1. Selecteer **Artikelnummer** artikel uit de opzoekbewerking.
    2. Selecteer de **Vestiging** uit de opzoekbewerking.
    3. Geef de **Hoeveelheid** in voor het aantal verbruikte artikelen.
    4. Selecteer **Gereed**.

7. Selecteer **Onkosten toevoegen** om onkostenregistraties te maken.
    1. Selecteer de **Categorie** uit de opzoekbewerking.
    2. Voer de hoeveelheid voor de onkostenregistratie in.
    3. Selecteer de **Verkoopvaluta** uit de opzoekbewerking.
    4. Voer de **Kostprijs** voor de onkostenregistratie in.
    5. Selecteer **Gereed**.

![Figuur 7](media/am-mobile-07.png)


## <a name="update-lifecycle-state-on-a-work-order"></a>Levenscyclusstatus van een werkorder bijwerken

1. Open op uw mobiele apparaat het werkgebied **Activabeheer**.

2. Selecteer **Alle onderhoudswerkorders**.

3. Selecteer de werkorder waarvoor u de levenscyclusstatus wilt bijwerken.

4. Selecteer de knop **Status bijwerken** onder in het scherm.

5. Selecteer een nieuwe levenscyclusstatus in de lijst.

6. Selecteer **Gereed**.

![Figuur 8](media/am-mobile-08.png)


## <a name="create-a-maintenance-request"></a>Een onderhoudsaanvraag maken

1. Open op uw mobiele apparaat het werkgebied **Activabeheer**.

2. Selecteer **Alle onderhoudsverzoeken**.

3. Selecteer **Acties** onder in het scherm en selecteer **Onderhoudsverzoek maken**.

4. Als de nummerreeks is ingeschakeld voor onderhoudsverzoeken in **Activabeheer**, is het veld **Onderhoudsverzoek** verborgen omdat het automatisch wordt ingevuld. Als het **veld Onderhoudsverzoek** zichtbaar is, voert u een onderhoudsverzoek-id in.

5. Selecteer een **Type onderhoudsverzoek**.

6. Voer een **Beschrijving** voor het onderhoudsverzoek in.

7. Selecteer het **Activum** waarvoor u het verzoek wilt maken.

8. Selecteer het **Serviceniveau** voor het onderhoudsverzoek.

9. Selecteer **Gereed**.

![Figuur 9](media/am-mobile-09.png)


## <a name="add-attachment-to-a-maintenance-request"></a>Bijlage toevoegen aan een onderhoudsverzoek

1. Open op uw mobiele apparaat het werkgebied **Activabeheer**.

2. Selecteer **Alle onderhoudsverzoeken**.

3. Selecteer het onderhoudsverzoek waaraan u een bijlage wilt toevoegen.

4. Selecteer **Bijlagen** onder in het scherm.

5. Selecteer **Bijlagen toevoegen**.

6. Voer **Naam** en **Notities** voor de bijlage in.

7. Selecteer **Afbeelding kiezen** als u een foto uit de mobiele galerie wilt selecteren of **Foto maken** om een foto te maken.

8. Selecteer **Gereed**.

![Figuur 10](media/am-mobile-10.png)


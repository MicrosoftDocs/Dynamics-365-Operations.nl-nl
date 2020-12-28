---
title: Openingstijden maken en bijwerken
description: In dit onderwerp wordt beschreven hoe u openingstijden kunt maken en bijwerken in Commerce Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 4706432234437d2dc7943fb194cd01004ab7e6b7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687506"
---
# <a name="create-and-update-store-hours"></a>Openingstijden maken en bijwerken

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Overzicht

Vanaf één locatie kunnen detailhandelaren de openingstijden voor verschillende winkels in verschillende geografische regio's maken, onderhouden en beheren. De openingstijden kunnen vervolgens worden weergegeven op POS-terminals (Point of Sale). Op deze manier kunnen kassamedewerkers openingstijden delen met klanten en kopers die geïnteresseerd zijn in voorraad in andere winkels beter helpen. De openingstijden kunnen ook op betalingsbewijzen worden afgedrukt, voor het geval klanten later nog willen terugkeren naar de winkel.

U kunt meerdere openingstijden configureren via verschillende kanalen. Tot deze kanalen behoren fysieke winkels, callcenters, mobiele apparaten en e-Commerce-sites.

Als een klant een ophaalorder voor een andere winkel heeft, kan de kassamedewerker datums selecteren wanneer het artikel kan worden opgehaald in die winkel. Het zoekresultaat van de winkel bevat een verwijzing naar de datums en openingstijden. De kassamedewerker kan een datum en locatie selecteren en tevens een ontvangstbewijs van ophalen afdrukken dat de openingstijden van de winkel bevat.

Deze functionaliteit is beschikbaar in Microsoft Dynamics 365 Retail 8.1.2 en hoger.

## <a name="configure-store-hours"></a>Openingstijden configureren

Volg deze stappen om openingstijden te configureren.

1. Ga naar **Detailhandel en commerce** \> **Kanaalinstellingen** \> **Openingstijden**.
2. Selecteer **Nieuw** om een nieuwe sjabloon voor openingstijden te maken. Als u een bestaande sjabloon wilt gebruiken, selecteert u de sjabloon in het linkerdeelvenster.
3. Definieer in het dialoogvenster **Bereik toevoegen** het datumbereik, de openingstijden en en eventuele vereiste vrije dagen.

    - Als de openingstijden niet veranderen, selecteert u **Nooit beëindigen** in het veld **Einddatum**.
    - Als de openingstijden betrekking hebben op een bepaalde maand, week of dag, stelt u de gewenste datums in de velden **Begindatum** en **Einddatum** in.

    > [!NOTE]
    > U kunt meerdere sjablonen maken met overlappende begin- en einddatums. Daarom kunt u bijvoorbeeld openingstijden voor winkels in verschillende tijdzones definiëren.

    ![Het dialoogvenster Bereik toevoegen](../dev-itpro/media/Storehours1.png "Het dialoogvenster Bereik toevoegen")

4. Koppel de sjabloon voor openingstijden aan de winkels waar deze wordt gebruikt. Selecteer in het dialoogvenster **Organisatieknooppunten kiezen** de winkels, regio's en organisaties waaraan de sjabloon moet worden gekoppeld.

    - U kunt slechts één sjabloon voor openingstijden aan elke winkel koppelen.
    - Gebruik de pijlknoppen om winkels, regio's of organisaties te selecteren. De kalender is beschikbaar voor de winkels of winkelketens en is ter referentie zichtbaar in het POS.

    ![Het dialoogvenster Organisatieknooppunten kiezen](../dev-itpro/media/Storehours2.png "Dialoogvenster Organisatieknooppunten kiezen")

5. Voer op de pagina **Distributieplanning** de taken **1070** en **1090** uit om de openingstijden beschikbaar te maken voor het POS.

## <a name="add-store-hours-to-printed-receipts"></a>Winkeltijden toevoegen aan afgedrukte ontvangstbewijzen

Voer de volgende stappen uit om openingstijden toe te voegen aan de afgedrukte POS-ontvangstbewijzen.

1. Open de functie voor het ontwerpen van ontvangstbewijzen.
2. Selecteer **Voettekst** in de linkerbenedenhoek.
3. Sleep het element **Winkeltijden** van het linkerdeelvenster naar de voettekst onder aan de sjabloon voor ontvangstbewijzen.
4. U kunt het standaardlabel van het element **Openingstijden** naar wens bewerken.
5. Sla het ontvangstbewijs op en sluit de ontwerpfunctie.
6. Voer op de pagina **Distributieplanning** de taken **1070** en **1090** uit.
7. Meld u aan bij het POS.
8. Voltooi een verkoop en kis ervoor om een ontvangstbewijs af te drukken.

POS-ontvangstbewijzen bevatten nu de openingstijden. Als de sjabloon feestdagen bevat, worden deze weergegeven op het ontvangstbewijs.

![Voorbeeld van ontvangstbewijs](../dev-itpro/media/Storehours3.png "Voorbeeld van ontvangstbewijs")

---
title: Een callcenterkanaal instellen
description: In dit onderwerp wordt beschreven hoe u een nieuw callcenterkanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057874"
---
# <a name="set-up-a-call-center-channel"></a>Een callcenterkanaal instellen


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een nieuw callcenterkanaal maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

In Dynamics 365 Commerce is een callcenter een type afzetkanaal dat kan worden gedefinieerd in de toepassing. Door een afzetkanaal voor uw callcenter-entiteiten te definiëren, kan het systeem specifieke gegevens en orderverwerkingsinstellingen koppelen aan verkooporders. Een bedrijf kan meerdere callcenterkanalen definiëren in Commerce. 

Controleer vóór het maken van een nieuw callcenterkanaal of u de [Vereisten voor het instellen van kanalen](channels-prerequisites.md) hebt voltooid.

## <a name="create-and-configure-a-new-call-center-channel"></a>Een nieuw callcenterafzetkanaal maken en configureren

Voer de volgende stappen uit om een nieuw callcenterafzetkanaal te maken en te configureren.

1. Ga in het navigatievenster naar **Modules \> Kanalen \> Callcenters \> Alle callcenters**.
1. Selecteer **Nieuw** in het actievenster.
1. Typ in het veld **Naam** een naam voor het nieuwe kanaal.
1. Selecteer de juiste **Rechtspersoon** in de vervolgkeuzelijst.
1. Selecteer de juiste **Magazijn**locatie in de vervolgkeuzelijst.
1. Geef in het veld **Standaardklant** een geldige standaardklant op.
1. Geef in het veld **Profiel voor e-mailmelding** een geldig profiel voor e-mailmeldingen op.
1. Geef een infocode op voor **Prijsoverschrijving**. Het is mogelijk dat u hiervoor eerst een informatiecode moet maken.
1. Geef een infocode op voor **Wachtstandcode**. Het is mogelijk dat u hiervoor eerst een informatiecode moet maken.
1. Een infocode op voor **Krediet**. Het is mogelijk dat u hiervoor eerst een informatiecode moet maken.
1. Selecteer **Opslaan**.

De volgende afbeelding toont het maken van een nieuw callcenterafzetkanaal.

![Nieuw callcenterafzetkanaal](media/channel-setup-callcenter-1.png)

In de volgende afbeelding ziet u een voorbeeld van een callcenterafzetkanaal.

![Voorbeeld van callcenterafzetkanaal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Aanvullende afzetkanaalinstellingen

Aanvullende taken die nodig zijn voor het instellen van callcenterkanalen, zijn onder andere het instellen van betalingsmethoden en leveringsmethoden.

De volgende afbeelding toont de instellingsopties voor **Leveringsmethoden** en **Betalingsmethoden** op het tabblad **Instellingen**.

![Aanvullende acties voor het instellen van een callcenterkanaal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Betalingsmethoden instellen

Volg deze stappen om betalingsmethoden in te stellen voor elk betalingstype dat op dit kanaal wordt ondersteund.

1. Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Betalingsmethoden**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer in het navigatievenster een gewenste betalingsmethode.
1. Geef in de sectie **Algemeen** een naam op in **Bewerkingsnaam** en configureer eventuele andere instellingen.
1. Configureer eventuele aanvullende instellingen voor het betalingstype.
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeld van een contante betalingsgmethode.

![Voorbeeldbetalingsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Leveringsmethoden instellen

U kunt de geconfigureerde leveringsmethoden bekijken door **Leveringsmethoden** te selecteren op het tabblad **Instellingen** van het **actievenster**.  

Voer de volgende stappen uit als u een leveringsmethode wilt wijzigen of toevoegen.

1. Ga in het navigatiedeelvenster naar **Modules \> Voorraadbeheer \> Leveringsmethoden**.
1. Selecteer in het actievenster de optie **Nieuw** als u een nieuwe leveringsmethode wilt maken of selecteer een bestaande methode.
1. Selecteer in de sectie **Detailhandelkanalen** de optie **Regel toevoegen** om het kanaal toe te voegen. Als u kanalen toevoegt met organisatieknooppunten in plaats van elk kanaal afzonderlijk toe te voegen, kunt u het toevoegen van kanalen stroomlijnen.

In de volgende afbeelding ziet u een voorbeeld van een leveringsmethode.

![Leveringsmethoden instellen](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Aanvullende resources

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Verkoopfunctionaliteit callcenter](call-center-functionality.md)

[Orderverwerkingsopties voor callcenter instellen](set-up-order-processing-options.md)

[Callcentercatalogi](call-center-catalogs.md)

[Instellen en werken met fraudewaarschuwingen](set-up-fraud-alerts.md)

[Continuïteitsprogramma's instellen voor callcenters](set-up-continuity-program.md)

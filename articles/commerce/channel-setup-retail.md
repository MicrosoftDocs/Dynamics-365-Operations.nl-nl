---
title: Een detailhandelkanaal instellen
description: In dit onderwerp wordt beschreven hoe u een nieuw detailhandelkanaal maakt in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113823"
---
# <a name="set-up-a-retail-channel"></a>Een detailhandelafzetkanaal instellen


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een nieuw detailhandelkanaal maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Dynamics 365 Commerce ondersteunt meerdere detailhandelkanalen. Deze detailhandelskanalen zijn o.a. online winkels, call centers en winkels (ook fysieke winkels genoemd). Iedere Retail-winkelkanaal kan zijn eigen betalingsmethoden, prijsgroepen, verkooppuntkassa's (POS), inkomsten- en uitgavenrekeningen en personeel hebben. U moet al deze elementen instellen voordat u een Retail-winkelkanaal kunt maken. 

Controleer vóór het maken van een detailhandelkanaal of u de [Vereisten voor afzetkanalen](channels-prerequisites.md) hebt gevolgd.

## <a name="create-and-configure-a-new-retail-channel"></a>Een nieuw detailhandelafzetkanaal maken en configureren

1. Ga in het navigatievenster naar **Modules \> Kanalen \> Winkels \> Alle winkels**.
1. Selecteer **Nieuw** in het actievenster.
1. Typ in het veld **Naam** een naam voor het nieuwe kanaal.
1. Geef in het veld **Winkelnummer** een uniek winkelnummer op. Het nummer kan alfanumeriek zijn met een maximum van 10 tekens.
1. Voer in de vervolgkeuzelijst **Rechtspersoon** de toepasselijke rechtspersoon in.
1. Voer in de vervolgkeuzelijst **Magazijn** het juiste magazijn in.
1. Selecteer in het veld **Winkeltijdzone** de juiste tijdzone.
1. Selecteer in de vervolgkeuzelijst **Btw-groep** een toepasselijke btw-groep voor de winkel.
1. Selecteer in het veld **Valuta** de juiste valuta.
1. Geef in het veld **Adresboek klant** een geldig adresboek op.
1. Geef in het veld **Standaardklant** een geldige standaardklant op.
1. Selecteer in het veld **Functionaliteitsprofiel** een functionaliteitsprofiel, indien van toepassing.
1. Geef in het veld **Profiel voor e-mailmelding** een geldig profiel voor e-mailmeldingen op.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont het maken van een nieuw detailhandelkanaal.

![Nieuw detailhandelafzetkanaal](media/channel-setup-retail-1.png)

In de volgende afbeelding ziet u een voorbeeld van een detailhandelafzetkanaal.

![Voorbeeld van detailhandelafzetkanaal](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Overige instellingen

Er zijn talloze andere optionele instellingen die u op basis van de behoeften van de detailhandelwinkel kunt instellen in de secties **Overzicht/afsluiting** en **Overige**.

Zie ook [Schermindelingen voor het POS](pos-screen-layouts.md) voor informatie over het instellen van de standaardschermindeling in de sectie **Schermindeling** en [Retail-hardwarestation configureren en installeren](retail-hardware-station-configuration-installation.md) voor informatie het instellen van de sectie **Hardwarestations**.

In de volgende afbeelding ziet u een voorbeeldconfiguratie van een detailhandelafzetkanaal.

![Voorbeeldconfiguratie van detailhandelafzetkanaal](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Aanvullende kanaalinstellingen

Er zijn nog meer zaken die u moet instellen voor een kanaal. Deze vindt u in de sectie **Instellingen** van het **Actievenster**.

Aanvullende taken die nodig zijn voor het instellen van online kanalen, zijn onder andere het instellen van betalingsmethoden, contantdeclaraties, leveringsmethoden, inkomsten- en onkostenrekeningen, secties, de toewijzing van afhandelingsgroepen en kluizen.

De volgende afbeelding toont diverse aanvullende opties voor het instellen van detailhandelskanalen op het tabblad **Instellingen**.

![Kanaal instellen](media/channel-setup-retail-4.png)

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

### <a name="set-up-cash-declaration"></a>Contantdeclaratie instellen

1. Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Contantdeclaratie**.
1. Selecteer in het actievenster de optie **Nieuw** en maak vervolgens alle **Munt**- en **Coupure**-denominaties die van toepassing zijn.

In de volgende afbeelding ziet u een voorbeeld van een contantdeclaratie.

![Contantdeclaraties instellen](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Leveringsmethoden instellen

U kunt de geconfigureerde leveringsmethoden bekijken door **Leveringsmethoden** te selecteren op het tabblad **Instellingen** van het **actievenster**.  

Voer de volgende stappen uit als u een leveringsmethode wilt wijzigen of toevoegen.

1. Ga in het navigatiedeelvenster naar **Modules \> Voorraadbeheer \> Leveringsmethoden**.
1. Selecteer in het actievenster de optie **Nieuw** als u een nieuwe leveringsmethode wilt maken of selecteer een bestaande methode.
1. Selecteer in de sectie **Detailhandelkanalen** de optie **Regel toevoegen** om het kanaal toe te voegen. Als u kanalen toevoegt met organisatieknooppunten in plaats van elk kanaal afzonderlijk toe te voegen, kunt u het toevoegen van kanalen stroomlijnen.

In de volgende afbeelding ziet u een voorbeeld van een leveringsmethode.

![Leveringsmethoden instellen](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Inkomsten-/uitgavenrekening instellen

Volg deze stappen om een inkomsten-/uitgavenrekening in te stellen.

1. Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Inkomsten-/uitgavenrekening**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer een naam in onder **Naam**.
1. Voer onder **Zoeknaam** een zoeknaam in.
1. Voer onder **Rekeningtype** een type rekening in.
1. Voer zo nodig tekst in voor **Berichtregel 1**, **Berichtregel 2**, **Strooktekst 1** en **Strooktekst 2**.
1. Voer onder **Boeking** boekingsinformatie in.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont een voorbeeld van een inkomsten-/uitgavenrekening.

![Inkomsten-/uitgavenrekeningen instellen](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Secties instellen

Volg deze stappen om secties in te stellen.

1. Selecteer in het actievenster het tabblad **Instellingen** en klik op **Secties**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer onder **Sectienummer** een sectienummer in.
1. Voer onder **Beschrijving** een beschrijving in.
1. Voer onder **Sectiegrootte** een sectiegrootte in.
1. Configureer naar behoefte aanvullende instellingen voor **Algemeen** en **Verkoopstatistieken**.
1. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-a-fulfillment-group-assignment"></a>De toewijzing van een afhandelingsgroep instellen

Volg deze stappen als u de toewijzing van een afhandelingsgroep wilt instellen.

1. Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Toewijzing afhandelingsgroep**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer een afhandelingsgroep in de vervolgkeuzelijst **Afhandelingsgroep**.
1. Voer in de vervolgkeuzelijst **Beschrijving** een beschrijving in.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont een voorbeeld van de instellingen voor de toewijzing van een afhandelingsgroep.

![Toewijzingen van een afhandelingsgroep instellen](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Kluizen instellen

Volg deze stappen om kluizen in te stellen.

1. Selecteer in het actievenster het tabblad **Instellingen** en klik op **Kluizen**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer een naam in voor de kluis.
1. Selecteer **Opslaan** in het actievenster.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Een online afzetkanaal instellen](channel-setup-online.md)

[Een callcenterkanaal instellen](channel-setup-callcenter.md)


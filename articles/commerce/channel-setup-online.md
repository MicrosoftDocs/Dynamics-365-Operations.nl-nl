---
title: Een online afzetkanaal instellen
description: In dit onderwerp wordt beschreven hoe u een nieuw online afzetkanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dc76c3c8c3da11202ebb29f4c5c0df72892c094a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351171"
---
# <a name="set-up-an-online-channel"></a>Een online afzetkanaal instellen


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een nieuw online afzetkanaal maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Dynamics 365 Commerce ondersteunt meerdere detailhandelkanalen. Deze detailhandelskanalen zijn o.a. online winkels, call centers en winkels (ook fysieke winkels genoemd). Een online winkel biedt klanten de mogelijkheid om producten zowel in de online winkel als in de fysieke winkel van de detailhandelaar te kopen.

Als u een online winkel in Commerce wilt maken, moet u eerst een online kanaal maken. Controleer vóór het maken van een nieuw online kanaal of u de [Vereisten voor het instellen van kanalen](channels-prerequisites.md) hebt voltooid.

Voordat u een nieuwe site kunt maken, moet er minimaal één online winkel zijn gemaakt in Commerce. Zie voor meer informatie [Een e-commerce-site maken](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Een nieuw online afzetkanaal maken en configureren

Voer de volgende stappen uit om een nieuw online afzetkanaal te maken en te configureren.

1. Ga in het navigatievenster naar **Modules \> Kanalen \> Online winkels**.
1. Selecteer **Nieuw** in het actievenster.
1. Typ in het veld **Naam** een naam voor het nieuwe kanaal.
1. Voer in de vervolgkeuzelijst **Rechtspersoon** de toepasselijke rechtspersoon in.
1. Voer in de vervolgkeuzelijst **Magazijn** het juiste magazijn in.
1. Selecteer in het veld **Winkeltijdzone** de juiste tijdzone.
1. Selecteer in het veld **Valuta** de juiste valuta.
1. Geef in het veld **Standaardklant** een geldige standaardklant op.
1. Geef in het veld **Adresboek klant** een geldig adresboek op.
1. Selecteer in het veld **Functionaliteitsprofiel** een functionaliteitsprofiel, indien van toepassing.
1. Geef in het veld **Profiel voor e-mailmelding** een geldig profiel voor e-mailmeldingen op.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont het maken van een nieuw online afzetkanaal.

![Nieuw online afzetkanaal.](media/channel-setup-online-1.png)

In de volgende afbeelding ziet u een voorbeeld van een online afzetkanaal.

![Voorbeeld van online afzetkanaal.](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a>Talen instellen

Als uw e-Commerce site ondersteuning biedt voor meerdere talen, vouwt u de sectie **Talen** uit en voegt u de toepasselijke extra talen toe.

## <a name="set-up-payment-account"></a>Betalingsrekening instellen

In de sectie **Betalingsrekening** kunt u een externe betalingsverschaffer toevoegen. Zie [Dynamics 365-betalingsconnector voor Adyen](./dev-itpro/adyen-connector.md) voor meer informatie over het instellen van een Adyen-betalingsconnector.

## <a name="additional-channel-setup"></a>Aanvullende afzetkanaalinstellingen

Aanvullende taken die nodig zijn voor het instellen van online kanalen, zijn onder andere het instellen van betalingsmethoden, leveringsmethoden en de toewijzing van afhandelingsgroepen.

De volgende afbeelding toont de instellingsopties voor **Leveringsmethoden**, **Betalingsmethoden** en **Toewijzing van afhandelingsgroepen** op het tabblad **Instellingen**.

![Aanvullende acties voor het instellen van een online kanaal.](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Betalingsmethoden instellen

Volg deze stappen om betalingsmethoden in te stellen voor elk betalingstype dat op dit kanaal wordt ondersteund.

1. Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Betalingsmethoden**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer in het navigatievenster een gewenste betalingsmethode.
1. Geef in de sectie **Algemeen** een naam op in **Bewerkingsnaam** en configureer eventuele andere instellingen.
1. Configureer eventuele aanvullende instellingen voor het betalingstype.
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeld van een contante betalingsgmethode.

![Voorbeeldbetalingsmethoden.](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Leveringsmethoden instellen

U kunt de geconfigureerde leveringsmethoden bekijken door **Leveringsmethoden** te selecteren op het tabblad **Instellingen** van het **actievenster**.  

Voer de volgende stappen uit als u een leveringsmethode wilt wijzigen of toevoegen.

1. Ga in het navigatiedeelvenster naar **Modules \> Voorraadbeheer \> Leveringsmethoden**.
1. Selecteer in het actievenster de optie **Nieuw** als u een nieuwe leveringsmethode wilt maken of selecteer een bestaande methode.
1. Selecteer in de sectie **Detailhandelkanalen** de optie **Regel toevoegen** om het kanaal toe te voegen. Als u kanalen toevoegt met organisatieknooppunten in plaats van elk kanaal afzonderlijk toe te voegen, kunt u het toevoegen van kanalen stroomlijnen.

In de volgende afbeelding ziet u een voorbeeld van een leveringsmethode.

![Leveringsmethoden instellen.](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>De toewijzing van een afhandelingsgroep instellen

Volg deze stappen als u de toewijzing van een afhandelingsgroep wilt instellen.

1. Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Toewijzing afhandelingsgroep**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer een afhandelingsgroep in de vervolgkeuzelijst **Afhandelingsgroep**.
1. Voer in de vervolgkeuzelijst **Beschrijving** een beschrijving in.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont een voorbeeld van de instellingen voor de toewijzing van een afhandelingsgroep.

![Toewijzing van een afhandelingsgroep instellen.](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Een detailhandelafzetkanaal instellen](channel-setup-retail.md)

[Een callcenterkanaal instellen](channel-setup-callcenter.md)

[Dynamics 365-betalingsconnector voor Adyen](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Een online kanaal instellen
description: In dit artikel wordt beschreven hoe u een nieuw online afzetkanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: be9fafe8ece771ad6577db1cdb70af6f48e054cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272875"
---
# <a name="set-up-an-online-channel"></a>Een online kanaal instellen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een nieuw online afzetkanaal maakt in Microsoft Dynamics 365 Commerce.

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

## <a name="assign-the-channel-to-a-commerce-scale-unit"></a>Het kanaal toewijzen aan een Commerce Scale Unit

Uw nieuwe kanaal moet worden toegewezen aan een Commerce Scale Unit. Zie [Kanalen configureren om Commerce Scale Unit te gebruiken](../fin-ops-core/dev-itpro/deployment/initialize-retail-channels.md#configure-channels-to-use-commerce-scale-unit) voor instructies.

## <a name="set-up-languages"></a>Talen instellen

Als uw e-Commerce-site ondersteuning biedt voor meerdere talen, vouwt u de sectie **Talen** uit en voegt u desgewenst extra talen toe.

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

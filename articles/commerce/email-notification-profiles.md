---
title: Een profiel voor e-mailmeldingen instellen
description: In dit onderwerp wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
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
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 17ffdcbf4b1801bd6ee9c9ddc18622d5d04b8a98
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180190"
---
# <a name="set-up-an-email-notification-profile"></a>Een profiel voor e-mailmeldingen instellen


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Voordat u kanalen gaat maken, moet u een profiel instellen om ervoor te zorgen dat e-mailmeldingen kunnen worden verzonden voor verschillende gebeurtenissen, zoals het maken van orders, het verzenden van orders en het mislukken van de betaling.

Zie [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over het configureren van e-mail.

## <a name="create-an-email-notification-profile"></a>Een profiel voor e-mailmeldingen maken

Voer de volgende stappen uit om een e-mailmeldingsprofiel te maken.

1. Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.
1. Klik in het actievenster op **Nieuw**.
1. Voer in het veld **E-mailmeldingsprofiel** een naam in om het profiel te identificeren.
1. Voer in het veld **Beschrijving** een relevante beschrijving in.
1. Stel de schakeloptie **Actief** in op **Ja**.

### <a name="create-an-email-template"></a>Een e-mailsjabloon maken

Voordat een e-mailmelding kan worden gemaakt, moet u een e-mailsjabloon voor de organisatie maken die de e-mailgegevens van de afzenders en de e-mailsjabloon bevat.

Volg deze stappen om een e-mailsjabloon te maken.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen voor organisatie**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **E-mail-id** een id in om deze sjabloon te helpen identificeren.
1. Voer in het veld **Naam afzender** de naam van de afzender in.
1. Voer in het veld **Beschrijving van e-mail** een betekenisvolle beschrijving in.
1. Voer in het veld **E-mailadres afzender** het e-mailadres van de afzender in.
1. Vul in de sectie **Algemeen** alle optionele informatie in die nodig is (zoals de e-mailprioriteit).
1. Vouw de sectie **Inhoud van e-malbericht** uit en selecteer **Nieuw** om de sjablooninhoud te maken. Selecteer voor elk inhoudsitem de taal en geef de onderwerpregel van het e-mailbericht op. Als het e-mailbericht tekst bevat, controleert u of het vak **Heeft hoofdtekst** is ingeschakeld.
1. Selecteer **E-mailbericht** in het actievenster om een sjabloon voor e-mailteksten op te geven.

De volgende afbeelding toont enkele voorbeelden van e-mailsjablooninstellingen.

![Instellingen van e-mailsjabloon](media/email-template.png)

### <a name="create-an-email-event"></a>Een e-mailgebeurtenis maken

Volg deze stappen om een e-mailgebeurtenis te maken.

1. Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.
1. Zoek en selecteer de gewenste record in de lijst. 
1. Selecteer de e-mailsjabloon in de vervolgkeuzelijst **E-mail-id**.
1. Selecteer het toepasselijke **E-mailmeldingstype** in de vervolgkeuzelijst.
1. Schakel het selectievakje **Actief** in.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont enkele voorbeelden van instellingen voor meldingen van meldingen.

![Instellingen voor melding van gebeurtenissen](media/email-notification-profile.png)

### <a name="next-steps"></a>Volgende stappen

Voordat u e-mailberichten kunt verzenden, moet u de service voor uitgaande e-mail configureren en een batchtaak instellen. Zie [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) voor meer informatie.


## <a name="additional-resources"></a>Aanvullende bronnen

[E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Overzicht van Organisaties en organisatiehiërarchieën](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

---
title: Een profiel voor e-mailmeldingen instellen
description: In dit onderwerp wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a92c21a93766e6583882f50222837366ed4c9a24c2bbfd93933763bd4ffa46bb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771026"
---
# <a name="set-up-an-email-notification-profile"></a>Een profiel voor e-mailmeldingen instellen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.

Wanneer u kanalen maakt, kunt u een e-mailmeldingsprofiel instellen. Op die manier kunnen e-mails worden verzonden naar klanten voor verschillende transactiegebeurtenissen, zoals het maken van orders, de verzendingsstatus van de order en het mislukken van een betaling.

Zie [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over het configureren van e-mail.

## <a name="create-an-email-notification-profile"></a>Een profiel voor e-mailmeldingen maken

Voer de volgende stappen uit om een e-mailmeldingsprofiel te maken.

1. Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.
1. Klik in het actievenster op **Nieuw**.
1. Voer in het veld **E-mailmeldingsprofiel** een naam in om het profiel te identificeren.
1. Voer in het veld **Beschrijving** een relevante beschrijving in.
1. Stel de schakeloptie **Actief** in op **Ja**.

### <a name="create-an-email-template"></a>Een e-mailsjabloon maken

Voordat een e-mailmeldingstype kan worden ingeschakeld, moet u een e-mailsjabloon van de organisatie maken in Commerce Headquarters. Met deze sjabloon definieert u het e-mailbericht, de afzender, de standaardtaal en de hoofdtekst van de e-mail voor elke taal die u wilt ondersteunen.

Volg deze stappen om een e-mailsjabloon te maken.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen voor organisatie**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **E-mail-id** een id in om deze sjabloon te helpen identificeren.
1. Voer in het veld **Naam afzender** de naam van de afzender in.
1. Voer in het veld **Beschrijving van e-mail** een betekenisvolle beschrijving in.
1. Voer in het veld **E-mailadres afzender** het e-mailadres van de afzender in.
1. Selecteer in de sectie **Algemeen** een standaardtaal voor de e-mailsjabloon. De standaardtaal wordt gebruikt als er geen gelokaliseerde sjabloon voor de opgegeven taal bestaat.
1. Vouw de sectie **Inhoud van e-malbericht** uit en selecteer **Nieuw** om de sjablooninhoud te maken. Selecteer voor elk inhoudsitem de taal en geef de onderwerpregel van het e-mailbericht op. Als het e-mailbericht tekst bevat, controleert u of het vak **Heeft hoofdtekst** is ingeschakeld.
1. Selecteer **E-mailbericht** in het actievenster om een sjabloon voor e-mailteksten op te geven.

De volgende afbeelding toont enkele voorbeelden van e-mailsjablooninstellingen.

![Instellingen van e-mailsjabloon.](media/email-template.png)

### <a name="create-an-email-event"></a>Een e-mailgebeurtenis maken

Volg deze stappen om een e-mailgebeurtenis te maken.

1. Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.
1. Zoek en selecteer de gewenste record in de lijst. 
1. Selecteer de e-mailsjabloon in de vervolgkeuzelijst **E-mail-id**.
1. Selecteer het toepasselijke **E-mailmeldingstype** in de vervolgkeuzelijst.
1. Schakel het selectievakje **Actief** in.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont enkele voorbeelden van instellingen voor meldingen van meldingen.

![Instellingen voor melding van gebeurtenissen.](media/email-notification-profile.png)

### <a name="next-steps"></a>Volgende stappen

Voordat u e-mailberichten kunt verzenden, moet u de service voor uitgaande e-mail configureren en een batchtaak instellen. Zie [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) voor meer informatie.


## <a name="additional-resources"></a>Aanvullende bronnen

[E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Overzicht van Organisaties en organisatiehiërarchieën](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

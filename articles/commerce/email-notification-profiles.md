---
title: Een profiel voor e-mailmeldingen instellen
description: In dit artikel wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292130"
---
# <a name="set-up-an-email-notification-profile"></a>Een profiel voor e-mailmeldingen instellen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een profiel voor e-mailmeldingen maakt in Microsoft Dynamics 365 Commerce.

Wanneer u kanalen maakt, kunt u een e-mailmeldingsprofiel instellen. Met het e-mailmeldingsprofiel worden de gebeurtenissen van een verkooptransactie gedefinieerd (zoals de gebeurtenissen gemaakte order, verpakte order en gefactureerde order) waarvoor u meldingen naar uw klanten verzendt. 

Zie [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over het configureren van e-mail.



## <a name="create-an-email-template"></a>Een e-mailsjabloon maken

Voordat een e-mailmeldingstype kan worden ingeschakeld, moet u een e-mailsjabloon voor de organisatie maken in Commerce Headquarters voor elk meldingstype dat u wilt ondersteunen. Met deze sjabloon definieert u het onderwerp van het e-mailbericht, de afzender, de standaardtaal en de hoofdtekst van de e-mail voor elke ondersteunde taal.

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

Zie [E-mailsjablonen maken voor transactiegebeurtenissen](email-templates-transactions.md) voor meer informatie over het maken van e-mailsjablonen. 

## <a name="create-an-email-notification-profile"></a>Een profiel voor e-mailmeldingen maken

Voer de volgende stappen uit om een e-mailmeldingsprofiel aan te maken in headquarters.

1. Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **E-mailmeldingsprofiel** een naam in om het profiel te identificeren.
1. Voer in het veld **Beschrijving** een relevante beschrijving in.
1. Stel de schakeloptie **Actief** in op **Ja**.

## <a name="add-a-notification-type"></a>Voer een type e-mailmelding toe

Volg deze stappen om een e-mailgebeurtenis te maken.

1. Ga in het navigatievenster naar **Modules \> Detailhandel en Commerce \> Instelling van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.
1. Selecteer onder **Instellingen voor melding van detailhandele-mails** **Nieuw**.
1. Selecteer het toepasselijke **E-mailmeldingstype** in de vervolgkeuzelijst.
1. Selecteer de e-mailsjabloon die hierboven is aangemaakt uit de vervolgkeuzelijst **ID e-mail**.
1. Schakel het selectievakje **Actief** in.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont enkele voorbeelden van instellingen voor meldingen van meldingen.

![Instellingen voor melding van gebeurtenissen.](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>Een terugkerende taak voor het verwerken van e-mailmeldingen plannen

Als u e-mailmeldingen wilt verzenden, moet de taak **E-mailmelding voor detailhandelorder verwerken** worden uitgevoerd.

Ga als volgt te werk om in headquarters een batch-taak in te stellen voor het verzenden van transactionele e-mails.

1. Ga naar **Retail en commerce \> IT retail en commerce \> E-mail en meldingen \> E-mailmelding verzenden**.
1. Selecteer **Terugkeerpatroon** in het dialoogvenster **E-mailmelding voor detailhandelorder verwerken**.
1. Selecteer **Geen einddatum** in het dialoogvenster **Terugkeerpatroon definiëren**.
1. Selecteer **Minuten** onder **Terugkeerpatroon** en stel het veld **Aantal** in op **1**. Met deze instellingen zorgt u ervoor dat e-mailmeldingen zo snel mogelijk worden verwerkt.
1. Selecteer **OK** om terug te keren naar het dialoogvenster **E-mailmelding voor detailhandelorder verwerken**.
1. Selecteer **OK** om het instellen van de taak af te ronden.

## <a name="next-steps"></a>Volgende stappen

Voordat e-mailberichten kunnen worden verzonden, moet u de service voor uitgaande e-mail configureren. Zie [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

[E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Overzicht van Organisaties en organisatiehiërarchieën](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

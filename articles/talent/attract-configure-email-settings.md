---
title: E-mailinstellingen configureren in Microsoft Dynamics 365 for Talent - Attract
description: In dit onderwerp wordt uitgelegd hoe u instellingen configureert voor e-mail die door Microsoft Dynamcis 365 for Talent - Attract wordt verzonden.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a8cf59064dd2f66ee50a0b0566aa712ba1f72dea
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739490"
---
# <a name="configure-email-settings"></a>E-mailinstellingen configureren

[!include[banner](../includes/banner.md)]

Uw merk wekt vertrouwen en helpt u al een vertrouwensrelatie tot stand te brengen met kandidaten voordat deze solliciteren voor uw functies. Een positieve merkperceptie trekt de beste talenten aan en vergroot de loyaliteit van bestaande werknemers. Met Microsoft Dynamics 365 for Talent: Attract kunt u e-mailberichten zo configureren dat deze het merk van uw bedrijf weerspiegelen. Zo kunt u functiekandidaten een consistente ervaring bieden tijdens het sollicitatieproces.

Met Attract kunt u de volgende acties uitvoeren:

- E-mailinstellingen configureren zodat de Microsoft Exchange-e-mailserviceaccount van het bedrijf wordt gebruikt. Op deze manier weten kandidaten dat de e-mails afkomstig zijn van uw bedrijf. U kunt de instellingen bijvoorbeeld zo configureren dat kandidaten e-mails ontvangen van `recruiting@contoso.com` in plaats van `contoso@microsoft.com`.
- Zorg voor een consistent merkbeeld voor alle e-mailcommunicatie door een globale kop- en voettekst voor alle e-mailsjablonen in te stellen. 

> [!NOTE]
> Als u Attract zo wilt configureren dat het e-mailserviceaccount van uw bedrijf wordt gebruikt om e-mail te verzenden, hebt u Uitgebreide invoegtoepassing voor aanstellingen nodig.

## <a name="connect-an-email-service-account"></a>Een e-mailserviceaccount verbinden

Door de e-mailserviceaccount van uw bedrijf te verbinden, kunt u een e-mailervaring met een huisstijl maken voor uw sollicitanten. Als u de bedrijfsaccount niet verbindt, wordt de standaard e-mailserviceaccount van Microsoft gebruikt.

1. Selecteer **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en selecteer vervolgens **Beheercentrum**.
2. Selecteer op het tabblad **E-mailinstellingen** onder **E-mailserviceaccounts** de optie **Een bedrijfsacccount verbinden**.

    ![De e-mailserviceaccount van het bedrijf verbinden in Attract](./media/attract-admin-email-service-accounts.png)

    Zie [Gedeelde postvakken in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes) voor meer informatie over het maken van een gedeelde e-mailaccount.

3. Meld u aan met uw bedrijfsreferenties aan in het aanmeldingsvenster van Microsoft.
4. Als u nog geen e-mailserviceaccount hebt ingesteld of als u een nieuwe wilt toevoegen, selecteert **Nieuwe serviceaccount toevoegen** en geeft u vervolgens uw e-mailgegevens op. Als u de e-mailserviceaccount die u wilt gebruiken al hebt ingesteld, selecteert u deze.

Wanneer uw e-mailserviceaccount is geconfigureerd, wordt deze weergegeven onder **E-mailserviceaccounts**.

## <a name="disconnect-an-email-service-account"></a>De verbinding met een e-mailserviceaccount verbreken

Als u het domein van uw bedrijf niet meer wilt gebruiken in e-mailcommunicatie via Attract, kunt u de verbinding met een e-mailserviceaccount verbreken.

1. Selecteer **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en selecteer vervolgens **Beheercentrum**.
2. Selecteer op het tabblad **E-mailinstellingen** onder **E-mailserviceaccounts** de knop **Meer** (drie verticale punten) naast de e-mailserviceaccount waarmee u de verbinding wilt verbreken.
3. Selecteer **Verbinding met e-mailaccount verbreken**.

    ![De verbinding met de e-mailserviceaccount van het bedrijf verbreken](./media/attract-admin-disconnect-email-account.png)

4. Selecteer **Verbinding verbreken** wanneer u wordt gevraagd de bewerking te bevestigen.

    ![Het verbreken van de verbinding met de e-mailserviceaccount van het bedrijf bevestigen](./media/attract-admin-email-confirm-disconnect.png)

Als u geen andere e-mailserviceaccount verbindt, wordt voor e-mails die worden verzonden vanuit Attract de standaard-e-mailserviceaccount van Microsoft gebruikt.

## <a name="configure-email-template-settings"></a>E-mailsjablooninstellingen configureren

U kunt een afbeelding van het logo van uw bedrijf en andere informatie uploaden als huisstijlkoptekst voor uw e-mailberichten. U kunt ook koppelingen naar uw privacybeleid en gebruiksvoorwaarden in e-mailvoetteksten opgeven.

> [!NOTE]
> U moet voldoen aan alle toepasselijke wetgeving van uw land of regio en de wetgeving die van toepassing is in het land of de regio van de e-mailontvanger. Deze wetten omvatten voorschriften voor ongewenste e-mail.

1. Selecteer **Instellingen** (het tandwielsymbool) in de rechterbovenhoek en selecteer vervolgens **Beheercentrum**.
2. Sleep op het tabblad **E-mailinstellingen** onder **Instellingen van e-mailsjabloon** de afbeelding die u als uw e-mailkoptekst wilt gebruiken naar het afbeeldingsvak of klik in het afbeeldingsvak om het bestand te zoeken. Als u een bestaande afbeelding wilt vervangen, moet u eerst **Verwijderen** ernaast selecteren. De afbeelding moet een JPEG-, JPG-, PNG- of SVG-bestand zijn. De aanbevolen grootte voor afbeeldingen ligt tussen 25 en 800 pixels breed en 25 en 150 pixels hoog. De maximale bestandsgrootte voor de koptekst is 1 MB.

    ![Een afbeelding toevoegen voor de e-mailkoptekst van uw bedrijf](./media/attract-admin-email-header.png)

3. Geef onder **Uw privacybeleid voor communicatie** een koppeling naar het privacybeleid van uw bedrijf op. Geef onder **Uw algemene voorwaarden voor communicatie** een koppeling naar de gebruiksvoorwaarden van uw bedrijf op.

    ![Koppelingen naar het privacybeleid en de gebruiksvoorwaarden van uw bedrijf toevoegen voor de e-mailvoettekst](./media/attract-admin-email-footer.png)

4. Selecteer **Opslaan** om de e-mailsjablooninstellingen op te slaan.

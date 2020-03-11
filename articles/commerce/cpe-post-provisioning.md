---
title: Een previewomgeving voor Dynamics 365 Commerce configureren
description: In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce configureert na inrichting.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d72caee25c03e8167b94dd387c7861f98bd0f4cb
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057712"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a>Een previewomgeving voor Dynamics 365 Commerce configureren


[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een preview-omgeving van Microsoft Dynamics 365 Commerce configureert na inrichting.

## <a name="overview"></a>Overzicht

Voltooi de procedures in dit onderwerp pas nadat uw preview-omgeving van Commerce is ingericht. Zie [Een preview-omgeving van Commerce inrichten](provisioning-guide.md) voor meer informatie over hoe u uw preview-omgeving van Commerce inricht.

Nadat uw preview-omgeving van Commerce end-to-end is ingericht, moeten extra configuratiestappen worden voltooid voordat u kunt beginnen met het evalueren van de omgeving. Als u deze stappen wilt uitvoeren, moet u Microsoft Dynamics Lifecycle Services (LCS) en Dynamics 365 Commerce gebruiken.

## <a name="before-you-start"></a>Voordat u begint

1. Meld u aan bij de [LCS-portal](https://lcs.dynamics.com).
1. Ga naar uw project.
1. Selecteer in het bovenste menu de optie **Cloudomgevingen**.
1. Selecteer uw omgeving in de lijst.
1. Klik op **Volledige details** in de omgevingsgegevens rechts.
1. Selecteer **Aanmelden** om een menu te openen en selecteer **Aanmelden bij omgeving**.
1. Zorg ervoor dat de rechtspersoon **USRT** is geselecteerd rechtsboven.

## <a name="configure-the-point-of-sale-in-lcs"></a>Het verkooppunt configureren in LCS

### <a name="associate-a-worker-with-your-identity"></a>Een medewerker aan uw identiteit koppelen

Ga als volgt te werk om een medewerker te koppelen aan uw identiteit in LCS.

1. Ga in het menu links naar **Modules \> Detailhandel en commerce \> Werknemers \> Medewerkers**.
1. Zoek en selecteer record **000713 - Andrew Collette**.
1. Selecteer **Detailhandel** in het actievenster.
1. Selecteer **Bestaande identiteit koppelen**.
1. Typ uw e-mailadres in het veld **E-mail** rechts van **Zoeken met behulp van e-mail**.
1. Selecteer **Zoeken**.
1. Selecteer de record met uw naam.
1. Selecteer **OK**.
1. Selecteer **Opslaan**.

### <a name="activate-cloud-pos"></a>Cloud POS activeren

Ga als volgt te werk om Cloud POS in LCS te activeren.

1. Selecteer in het bovenste menu de optie **Cloudomgevingen**.
1. Selecteer uw omgeving in de lijst.
1. Klik op **Volledige details** in de omgevingsgegevens rechts.
1. Selecteer **Aanmelden** om een menu te openen en selecteer **Aanmelden bij cloud-verkooppunt** om het verkooppunt (POS) te openen.
1. Selecteer **Volgende**.
1. Meld u aan met uw Microsoft Azure Active Directory (Azure AD)-account.
1. Onder **Winkelnaam** selecteert u **San Francisco**.
1. Selecteer **Volgende**.
1. Onder **Kassa en apparaat** selecteert u **SANFRAN-1**.
1. Selecteer **Activeren**. U bent afgemeld en de POS-aanmeldingspagina wordt geopend.
1. U kunt u nu aanmelden bij Cloud POS met operator-id **000713** en wachtwoord **123**.

## <a name="set-up-your-site-in-commerce"></a>Uw site instellen in Commerce

Ga als volgt te werk om te beginnen met het instellen van uw voorbeeldsite in Commerce.

1. Meld u aan bij het beheerhulpprogramma van de site met de URL die u hebt genoteerd tijdens de initialisatie van e-Commerce tijdens het inrichten (zie [e-Commerce initialiseren](provisioning-guide.md#initialize-e-commerce)).
1. Selecteer **Fabrikam** om het dialoogvenster met instellingen voor de site te openen.
1. Selecteer het domein dat u hebt ingevoerd bij het initialiseren van e-Commerce.
1. Selecteer **Uitgebreide Fabrikam online winkel** als het standaardkanaal. Zorg ervoor dat u de **uitgebreide** online winkel selecteert.
1. Als standaardtaal selecteert u **en-us**.
1. Laat de waarde van het veld **Pad** ongewijzigd.
1. Selecteer **OK**. De lijst met pagina's op de site wordt weergegeven.

## <a name="enable-jobs"></a>Taken inschakelen

Ga als volgt te werk om taken in Commerce in te schakelen.

1. Meld u aan bij de omgeving (HQ).
1. Ga in het menu links naar **Detailhandel en commerce \> Query's en rapporten \> Batchtaken**.

    De resterende stappen van deze procedure moeten worden voltooid voor elk van de volgende taken:

    * E-mailmelding voor detailhandelorder verwerken
    * Beschikbaarheid product
    * P-0001
    * Taak orders synchroniseren

1. Gebruik het snelfilter om de taak te zoeken aan de hand van de naam.
1. Als de status van de taak **Blokkeren** is, voert u de volgende stappen uit:

    1. Selecteer de record.
    1. Selecteer in het actievenster op het tabblad **Batchtaak** de optie **Status wijzigen**.
    1. Selecteer **Wachten** en vervolgens **OK**.

### <a name="run-full-data-synchronization"></a>Volledige gegevenssynchronisatie uitvoeren

Voer de volgende stappen uit om een volledige gegevenssynchronisatie in Commerce uit te voeren.

1. Ga in het menu links naar **Modules \> Detailhandel en commerce \> Instelling van hoofdkantoor \> Detailhandel planner \> Kanaaldatabase**.
1. In de lijst links is het kanaal **Standaard** geselecteerd. Selecteer het andere beschikbare kanaal. Dit kanaal heeft de naam **scXXXXXXXXX**.
1. Selecteer **Volledige gegevenssynchronisatie** in het actievenster.
1. Voer **9999** in als de distributieplanning.
1. Selecteer **OK**.
1. Selecteer **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Creditcardgegevens testen voor het uitvoeren van testinkopen

Voor het uitvoeren van testtransacties op de site kunt u de volgende creditcardgegevens testen:

- **Kaartnummer:** 4111-1111-1111-1111
- **Verloopdatum:** 10/20
- **CVV-code:** 737

> [!IMPORTANT]
> Gebruik in geen geval echte creditcardgegevens op de testsite.

## <a name="next-steps"></a>Volgende stappen

Als de inrichtings- en configuratiestappen zijn voltooid, bent u klaar om uw preview-omgeving te evalueren. Gebruik de URL van het beheerhulpprogramma van de e-Commerce-site om naar de ontwerpomgeving te gaan. Gebruik de URL van de e-Commerce-site om naar de omgeving van de site van de detailhandelklant te gaan.

Zie [Optionele functies voor een preview-omgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw preview-omgeving van Commerce configureert.

## <a name="additional-resources"></a>Aanvullende resources

[Omgevingsoverzicht Dynamics 365 Commerce-preview](cpe-overview.md)

[Een previewomgeving voor Dynamics 365 Commerce inrichten](provisioning-guide.md)

[Optionele functies voor een Dynamics 365 Commerce-preview-omgeving configureren](cpe-optional-features.md)

[Veelgestelde vragen over Dynamics 365 Commerce-preview-omgeving](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)

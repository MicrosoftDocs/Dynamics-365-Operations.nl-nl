---
title: Een sandbox-omgeving van Dynamics 365 Commerce configureren
description: In dit artikel wordt uitgelegd hoe u een sandbox-omgeving van Microsoft Dynamics 365 Commerce configureert na inrichting.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ae6a8c63721ac32f525e1846a10c0b2caeb08f9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270341"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>Een sandbox-omgeving van Dynamics 365 Commerce configureren

[!include [banner](includes/banner.md)]

In dit artikel wordt uitgelegd hoe u een sandbox-omgeving van Microsoft Dynamics 365 Commerce configureert na inrichting.

Voltooi de procedures in dit artikel pas nadat uw sandbox-omgeving van Commerce is ingericht. Zie [Een sandbox-omgeving van Commerce inrichten](provisioning-guide.md) voor meer informatie over hoe u uw sandbox-omgeving van Commerce inricht.

Nadat uw sandbox-omgeving van Commerce end-to-end is ingericht, moeten extra configuratiestappen worden voltooid voordat u kunt beginnen met het gebruiken van de omgeving. Als u deze stappen wilt uitvoeren, moet u Microsoft Dynamics Lifecycle Services (LCS) en Dynamics 365 Commerce gebruiken.

## <a name="before-you-start"></a>Voordat u begint

1. Meld u aan bij de [LCS-portal](https://lcs.dynamics.com).
1. Ga naar uw project.
1. Selecteer uw omgeving in de lijst.
1. Klik op **Aanmelden bij omgeving** in de omgevingsgegevens rechts. U wordt doorgestuurd naar Commerce Headquarters.
1. Zorg ervoor dat de rechtspersoon **USRT** is geselecteerd rechtsboven. Deze rechtspersoon is vooraf geconfigureerd in de demogegevens.
1. Ga naar **Commerce-parameters \> Configuratieparameters** en controleer of er een vermelding bestaat voor **ProductSearch.UseAzureSearch** die is ingesteld op **true**. Als dit item ontbreekt, voegt u deze toe en stelt u de waarde in op **waar**.
1. Ga naar **Detailhandel en commerce \> Instellingen van hoofdkantoor \> Commerce-planner \> Commerce-planner initialiseren**. Controleer in het fly-outmenu **Commerce-planner initialiseren** of de optie **Bestaande configuratie verwijderen** is ingesteld op **Ja** en selecteer vervolgens **OK**.
1. De store- en e-commercekanalen moeten moeten voor een goede werking worden toegevoegd aan Commerce Scale Unit. Ga naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Commerce-planner \> Kanaaldatabase** en selecteer Commerce Scale Unit in het deelvenster links. Voeg op het sneltabblad **Detailhandelafzetkanaal** de afzetkanalen **AW online store**, **AW Business online store** en **Fabrikam extended online store** toe als u die e-commercekanalen wilt gebruiken. U kunt ook detailhandels toevoegen als u POS gebruikt ( bijvoorbeeld **Seattle**, **San Francisco** en/of **San Jose**).
1. Als u ervoor wilt zorgen dat alle wijzigingen worden gesynchroniseerd met de kanaaldatabase, selecteert u **Kanaaldatabase \> Volledige gegevenssynchronisatie** voor Commerce Scale Unit.

Controleer tijdens het activiteiten na het inrichting in Commerce Headquarters of de rechtspersoon **USRT** altijd is geselecteerd.

## <a name="configure-the-point-of-sale"></a>Het verkooppunt configureren

### <a name="associate-a-worker-with-your-identity"></a>Een medewerker aan uw identiteit koppelen

Ga als volgt te werk om een medewerker te koppelen aan uw identiteit in Commerce Headquarters

1. Ga in het menu links naar **Modules \> Detailhandel en commerce \> Werknemers \> Medewerkers**.
1. Zoek en selecteer record **000713 - Andrew Collette**. Deze voorbeeldgebruiker is gekoppeld aan de winkel in San Francisco die wordt gebruikt in de volgende sectie.
1. Selecteer in het actievenster de optie **Commerce**.
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
1. Klik op **Aanmelden bij cloud-verkooppunt** in de omgevingsgegevens rechts.
1. Klik op **Volgende** om het dialoogvenster **Voordat u begint** te openen.
1. Laat het veld **Server-URL** ongewijzigd. Selecteer **Volgende**.
1. Meld u aan met uw Microsoft Azure Active Directory (Azure AD)-account.
1. Selecteer onder **Winkelnaam** **San Francisco** en selecteer **Volgende**.
1. Onder **Kassa en apparaat** selecteert u **SANFRAN-1**.
1. Selecteer **Activeren**. U bent afgemeld en de POS-aanmeldingspagina wordt geopend.
1. U kunt u nu aanmelden bij Cloud POS met operator-id **000713** en wachtwoord **123**.

## <a name="set-up-your-e-commerce-sites"></a>Uw e-commercesites instellen

Er zijn drie demosites voor e-commerce beschikbaar: Fabrikam, Adventure Works en Adventure Works Business. Volg de onderstaande stappen om elke demonstratiesite te configureren.

1. Meld u aan bij de site builder met de URL die u hebt genoteerd tijdens de initialisatie van e-Commerce tijdens het inrichten (zie [e-Commerce initialiseren](provisioning-guide.md#initialize-e-commerce)).
1. Selecteer de site (**Fabrikam**, **Adventure Works** of **Adventure Works Business**) om het dialoogvenster voor het instellen van de site te openen.
1. Selecteer het domein dat u hebt ingevoerd bij het initialiseren van Commerce.
1. Selecteer in Headquarts het vooraf geconfigureerde online winkelkanaal (**Uitgebreide online winkel Fabrikam**, **AW online store** of **AW Business online store**) die overeenkomt met het standaardkanaal.
1. Als standaardtaal selecteert u **en-us**.
1. Configureer de padvelden. U kunt deze leeg laten voor één site, maar u moet deze wel configureren als u dezelfde domeinnaam voor meerdere sites gebruikt. Als de domeinnaam bijvoorbeeld `https://www.constoso.com` is, kunt u een leeg pad gebruiken voor Fabrikam (`https://contoso.com`) en vervolgens aw gebruiken voor Adventure Works (`https://contoso.com/aw`) en awbusiness voor de bedrijfssite van Adventure Works (`https://contoso.com/awbusiness`).
1. Selecteer **OK**. De lijst met pagina's op de site wordt weergegeven.
1. Herhaal eventueel stap 2-7 om de andere demonstratiesites zo nodig te configureren.

## <a name="enable-jobs"></a>Taken inschakelen

Ga als volgt te werk om taken in Commerce in te schakelen.

1. Meld u aan bij uw Headquarters-omgeving.
1. Ga in het menu links naar **Detailhandel en commerce \> Query's en rapporten \> Batchtaken**.

    De resterende stappen van deze procedure moeten worden voltooid voor elk van de volgende taken:

    * E-mailmelding voor detailhandelorder verwerken
    * Beschikbaarheid product
    * P-0001
    * Taak orders synchroniseren

1. Gebruik het snelfilter om de taak te zoeken aan de hand van de naam.
1. Als de status van de taak **Uitvoeren** is, voert u de volgende stappen uit:

    1. Selecteer de record.
    1. Selecteer in het actievenster op het tabblad **Batchtaak** de optie **Status wijzigen**.
    1. Selecteer **Annuleren** en vervolgens **OK**.

1. Als de status van de taak **Ingehouden** is, voert u de volgende stappen uit:

    1. Selecteer de record.
    1. Selecteer in het actievenster op het tabblad **Batchtaak** de optie **Status wijzigen**.
    1. Selecteer **Wachten** en vervolgens **OK**.

U kunt desgewenst ook het terugkeerinterval instellen op één (1) minuut voor de volgende taken:

* E-mailmeldingtaak voor detailhandelorder verwerken
* P-0001 taak
* Taak orders synchroniseren

### <a name="run-full-data-synchronization"></a>Volledige gegevenssynchronisatie uitvoeren

Voer de volgende stappen uit om een volledige gegevenssynchronisatie in Commerce Headquarters uit te voeren.

1. Ga in het menu links naar **Modules \> Detailhandel en commerce \> Instelling van hoofdkantoor \> Commerce-planner \> Kanaaldatabase**.
1. Selecteer het kanaal met de naam **scXXXXXXXXX**.
1. Selecteer **Volledige gegevenssynchronisatie** in het actievenster.
1. Voer **9999** in als de distributieplanning.
1. Selecteer **OK**.
1. Selecteer **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Creditcardgegevens testen voor het uitvoeren van testinkopen

Voor het uitvoeren van testtransacties op de site kunt u de volgende creditcardgegevens testen:

- **Kaartnummer:** 4111-1111-1111-1111
- **Verloopdatum:** 10/30
- **CVV-code:** 737

> [!IMPORTANT]
> Gebruik in geen geval echte creditcardgegevens op de testsite.

## <a name="next-steps"></a>Volgende stappen

Als de inrichtings- en configuratiestappen zijn voltooid, bent u klaar om uw sandbox-omgeving te gebruiken. Gebruik de site builder-URL voor de Commerce-site om naar de ontwerpomgeving te gaan. Gebruik de URL van de Commerce-site om naar de omgeving van de site van de detailhandelklant te gaan.

Zie [Optionele functies voor een sandbox-omgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw sandbox-omgeving van Commerce configureert.

Om e-commercegebruikers in staat te stellen zich bij de e-commercesite aan te melden, is aanvullende configuratie vereist om siteverificatie in te schakelen via Azure Active Directory business-to-consumer (B2C). Zie [Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md) voor instructies.

## <a name="troubleshooting"></a>Problemen oplossen

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Kanaallijst van Site Builder is leeg bij configureren van site

Als er door Site Builder geen online winkelkanalen worden weergegeven, moet u er in Headquarters voor zorgen dat de kanalen zijn toegevoegd aan Commerce Scale Unit, zoals beschreven in de sectie [Voordat u begint](#before-you-start) hierboven. Voer ook **Commerce-planner initialiseren** uit met de waarde **Bestaande configuratiewaarde** ingesteld op **Ja**.  Nadat deze stappen zijn voltooid, voert u op de pagina **Kanaaldatabase** (**Retail en Commerce \> Instelling van hoofdkantoor \> Commerce-planner \> Kanaaldatabase**) de taak **9999-taak** uit voor Commerce Scale Unit.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Kleurstalen worden niet op de categoriepagina weergegeven, maar op de pagina met productdetails

Volg deze stappen om ervoor te zorgen dat de kleur- en formaatstalen opnieuw kunnen worden gedefinieerd.

1. Ga in Headquarters naar **Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.
1. Selecteer in het linkerdeelvenster het online winkelkanaal en selecteer vervolgens **Metagegevens van kenmerken instellen**.
1. Stel de optie **Kenmerk in kanaal weergeven** in op **Ja**, stel de optie **Kan worden verfijnd** in op **Ja** en selecteer **Opslaan**. 
1. Keer terug naar de pagina voor het online winkelkanaal en selecteer **Kanaalupdates publiceren**.
1. Ga naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Commerce-planner \> Kanaaldatabase** en voer de taak **9999** voor Commerce Scale Unit uit.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Bedrijfsfuncties lijken niet te zijn ingeschakeld voor de bedrijfssite AdventureWorks

Controleer in Headquarters of het online winkelkanaal is geconfigureerd met **Klanttype** ingesteld op **B2B**. Als **Klanttype** is ingesteld op **B2C**, moet er een nieuw kanaal worden gemaakt omdat het bestaande kanaal niet kan worden bewerkt. 

Demonstratiegegevens in Commerce versie 10.0.26 en eerder bevatten een fout waarbij het kanaal **AW Business online store** onjuist was geconfigureerd. Als oplossing moet een nieuw kanaal met dezelfde instellingen en configuraties worden gemaakt, behalve voor **Klanttype**, dat moet worden ingesteld op **B2B**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een sandbox-omgeving inrichten voor Dynamics 365 Commerce](provisioning-guide.md)

[Optionele functies voor een sandbox-omgeving van Dynamics 365 Commerce configureren](cpe-optional-features.md)

[BOPIS configureren in een sandbox-omgeving van Dynamics 365 Commerce](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)

[Een B2C-tenant instellen in Commerce](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

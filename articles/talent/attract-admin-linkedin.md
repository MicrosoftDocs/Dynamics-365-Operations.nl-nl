---
title: LinkedIn-integratie met Attract instellen
description: In dit onderwerp wordt uitgelegd hoe u LinkedIn-Integratie configureert voor Microsoft Dynamics 365 Talent - Attract, zodat u eenvoudig vacatures op LinkedIn kunt plaatsen vanuit Attract en uw wervers hun wervingsinformatie kunnen synchroniseren met het LinkedIn-profiel van een kandidaat.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4c518fb7036d44aa52c8db859ee3616fc4e58a06
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460828"
---
# <a name="set-up-linkedin-integration-with-attract"></a>LinkedIn-integratie met Attract instellen

[!include [banner](includes/banner.md)]

Help uw wervers en aanstellende managers toptalent te werven door LinkedIn-integratie met Microsoft Dynamics 365 Talent: Attract te configureren. Met Attract kunt u vacatures direct op LinkedIn plaatsen, het grootste onlinenetwerk voor professionals.

Vacatures die u op LinkedIn plaatst via Attract, zijn Limited Listings en worden zonder extra kosten voor uw bedrijf geleverd. Deze vermeldingen zijn alleen beschikbaar via LinkedIn-softwarepartners, zoals Attract. Ze worden niet weergegeven in het deelvenster **Carrières** op de LinkedIn-pagina van uw bedrijf omdat hier alleen betaalde vermeldingen worden weergegeven. Ze worden echter wel weergegeven wanneer potentiële kandidaten alle beschikbare functies weergeven. Beperkte aanbiedingen worden ook weergegeven in LinkedIn-zoekopdrachten naar functies.

Attract biedt twee manieren om te integreren met LinkedIn om kandidaten te zoeken via deze populaire vacaturesite:

- Plaats vacatures vanuit Attract op LinkedIn.
- Zoek kandidaten vanuit LinkedIn op Attract.

U kunt beide opties configureren op het tabblad **LinkedIn-integratie** in het beheercentrum. Ga naar <https://attract.talent.dynamics.com/adminsettings> om het beheercentrum te openen.

> [!NOTE]
> Om LinkedIn Recruiter-integratie met Attract te kunnen gebruiken, hebt u de [licenties voor Uitgebreide invoegtoepassing voor aanstellingen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) en [LinkedIn Recruiter nodig](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Zie [Welke versie van Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md) voor meer informatie.

Zie [Problemen met integratie met LinkedIn en Microsoft Dynamics 365 Talent - Attract oplossen](./attract-troubleshoot-linkedin.md) als u problemen hebt met het plaatsen van vacatures in LinkedIn.

Zie [Veelgestelde vragen over integratie van Attract met LinkedIn](./attract-linkedin-faq.md) voor meer informatie over andere manieren om vacatures op LinkedIn te plaatsen.

## <a name="configure-job-posting-to-linkedin"></a>Het plaatsen van vacatures op LinkedIn configureren

Voordat u vacatures vanuit Attract op LinkedIn kunt plaatsen, hebt u een [bedrijfs-ID voor LinkedIn](https://aka.ms/findID) nodig. Uw bedrijfs-ID voor LinkedIn is een reeks cijfers die een unieke identificatie vormen van uw bedrijf in LinkedIn. Raadpleeg [Associëren uw LinkedIn bedrijf ID met de LinkedIn Job Board-Veelgestelde vragen](https://aka.ms/findID) voor meer informatie.

Attract verzendt een feed van uw geplaatste vacatures naar LinkedIn en in LinkedIn wordt de feed vervolgens ongeveer eenmaal per dag gecontroleerd. Het kan 48 uur duren voordat uw vacatures op de site zijn geplaatst.

Vacatures die worden gepubliceerd naar LinkedIn, worden weergegeven op de live LinkedIn-site. Er is geen testomgeving voor het plaatsen van vacatures op LinkedIn. Zorg er daarom voor dat u niet per ongeluk testvacatures plaatst. 

1. Selecteer in het menu **Instellen** (het tandwielsymbool) in de rechterbovenhoek de optie **Beheercentrum**. U kunt ook naar <https://attract.talent.dynamics.com/adminsettings> gaan.
2. Selecteer het tabblad **LinkedIn-integratie**.
3. Voer onder **Bedrijfsnaam** de naam van uw bedrijf in en voer onder **Bedrijfs-ID** uw bedrijfs-ID voor LinkedIn in. Controleer of de bedrijfsnaam overeenkomt met de naam die wordt weergegeven op de LinkedIn-pagina van uw bedrijf. Raadpleeg [Associëren uw LinkedIn bedrijf ID met de LinkedIn Job Board-Veelgestelde vragen](https://www.linkedin.com/help/linkedin/answer/98972) voor meer informatie over bedrijfs-ID's voor LinkedIn.

    Zie [Het adres en de technische contactpersoon van uw organisatie en meer wijzigen](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more) als u gegevens voor uw organisatie wilt wijzigen. Neem contact op met de [ondersteuning van LinkedIn](https://www.linkedin.com/help/linkedin) als u nog steeds problemen ondervindt.

4. Selecteer **Opslaan**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>LinkedIn Recruiter met Attract instellen 

Als u wervers wilt machtigen om functies te zoeken via LinkedIn Recruiter, moet u de integratie met LinkedIn Recruiter in Attract configureren. Als u het configuratieproces wilt voltooien, moet u werken met de gebruiker die een beheerder is in het LinkedIn Recruiter-contract van uw organisatie.

1. Selecteer in het menu **Instellen** (het tandwielsymbool) in de rechterbovenhoek de optie **Beheercentrum**. U kunt ook naar <https://attract.talent.dynamics.com/adminsettings> gaan.
2. Selecteer het tabblad **LinkedIn-integratie**.

    [![Attract-beheerweergave om LinkedIn Recruiter-integratie te starten](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Selecteer **Verbinding maken** om de instelling te starten. U wordt door het LinkedIn-aanmeldingsproces geleid.
4. Als u seats in meerdere LinkedIn-contracten hebt, selecteert u het contract dat u wilt verbinden met het Attract-systeem. Als u een seat in slechts één LinkedIn-contract hebt, kunt u deze stap overslaan.
5. Selecteer onder **Recruiter System Connect (RSC)** de optie **Aanvragen**.

    [![Attract-beheerweergave om LinkedIn Recruiter-integratie aan te vragen](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. De instelling **Recruiter System Connect (RSC)** moet nu worden weergegeven als **Partner gereed**. Als u **Partner waarschuwen** op deze pagina ziet, wacht u enkele seconden, selecteert u **Partner waarschuwen** en vernieuwt u de pagina. De instelling wordt nu weergegeven als **Partner gereed**.

    [![Attract-beheerweergave om aan te geven dat de Attract-zijde van aanvragen is voltooid](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Als u de volgende stappen wilt uitvoeren, hebt u beheerdersbevoegdheden nodig in uw LinkedIn Recruiter-contract.

    1. Meld u aan bij LinkedIn via uw beheerdersaccount en selecteer **LinkedIn Recruiter** in de rechterbovenhoek. 
    2. Selecteer in het menu **Meer** boven aan de pagina de optie **Beheerinstellingen** en selecteer vervolgens het tabblad **ATS**.
    3. Als u met één klik exporteren voor slechts één contract wilt inschakelen, schakelt u **Toegang op contractniveau (voor elke seat in dit contract)** in. Als u dit voor het hele bedrijf wilt inschakelen, schakelt u **Toegang op bedrijfsniveau (voor alle contracten in uw bedrijf)** in.

    [![Attract-integratie inschakelen vanuit LinkedIn Recruiter-beheerweergave](./media/EnableRSC.png)](./media/EnableRSC.png)

8. Selecteer in het Attract-beheercentrum het tabblad **LinkedIn-integratie**. De instelling **Recruiter System Connect (RSC)** wordt nu als **Ingeschakeld** weergegeven.

    [![LinkedIn Recruiter-integratie voltooid](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Solliciteren met LinkedIn instellen in Attract

U kunt kandidaten toestaan om op uw functies te solliciteren via hun LinkedIn-profielen. Ga naar [The Power of LinkedIn Everywhere: Apply with LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin) (Engelstalig) voor meer informatie over Solliciteren met LinkedIn.

Van deze functie kan momenteel een voorbeeld worden bekeken. Voordat u deze stappen uitvoert, moet u controleren of Solliciteren met LinkedIn is ingeschakeld. Zie [Toegang tot voorbeeldfuncties in Microsoft Dynamics 365 Talent](./access-preview-feature.md) voor meer informatie over het inschakelen van voorbeeldfuncties.

1. Selecteer in het menu **Instellen** (het tandwielsymbool) in de rechterbovenhoek de optie **Beheercentrum**. U kunt ook naar <https://attract.talent.dynamics.com/adminsettings> gaan.
2. Selecteer het tabblad **LinkedIn-integratie**.

    [![Attract-beheerweergave om LinkedIn Recruiter-integratie te starten](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Selecteer naast **Solliciteren met LinkedIn** de optie **Verbinden** om het instellen te starten. U wordt door de rest van het proces met LinkedIn geleid.

## <a name="see-also"></a>Zie ook

[Veelgestelde vragen over integratie van Attract met LinkedIn](./attract-linkedin-faq.md)

[Vacatures plaatsen op externe vacaturesites vanuit Attract](./posting-jobs-external.md)

[Kandidaten zoeken met LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md)

[Functies maken, goedkeuren en boeken in Attract](./creating-jobs-attract.md)

[Problemen met integratie met LinkedIn en Microsoft Dynamics 365 Talent - Attract oplossen](./attract-troubleshoot-linkedin.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
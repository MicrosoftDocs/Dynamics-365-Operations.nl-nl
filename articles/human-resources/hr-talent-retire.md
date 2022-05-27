---
title: Buitengebruikstelling van Dynamics 365 Talent - Attract- en Onboard-apps
description: In dit onderwerp wordt de buitengebruikstelling van Dynamics 365 Talent - Attract- en Onboard-apps beschreven.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e17b92621f05ad8483a7c578bfaece58a530df2d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691997"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Buitengebruikstelling van Dynamics 365 Talent: Attract- en Onboard-apps


In december 2019 hebben we de buitengebruikstelling aangekondigd van Dynamics 365 Talent - Attract- en Onboard-apps op 1 februari 2022. Zo hadden onze klanten twee jaar de tijd om zich voor te bereiden.

Zie voor meer informatie over de buitengebruikstelling van deze apps:
 - [Dynamics 365 Talent - Attract- en Dynamics 365 Talent: Onboard-apps buiten gebruik stellen](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Een succesvoller personeelsbestand opbouwen met Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Wij blijven ondersteuning bieden aan Dynamics 365 Human Resources, wat onze klanten helpt bij het verkrijgen van inzicht in het personeel dat nodig is om gegevensgestuurde werknemerservaring op te bouwen op verschillende gebieden, zoals:

- Compensatie
- Voordelen
- Verlof en verzuim
- Conformiteit
- Salaris
- Feedback prestaties
- Training en certificering
- Selfserviceprogramma's

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Veelgestelde vragen over buitengebruikstelling van Dynamics 365 Talent-apps

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Wat is de gebruikerservaring voor zowel Dynamics 365 Talent - Attract als Onboard-apps vanaf 1 februari 2022?

Gebruikers kunnen de toepassingen niet meer gebruiken en worden omgeleid naar een buitengebruikstellingspagina.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Kunnen klanten voor zowel Dynamics 365 Talent - Attract- als Onboard-apps na 1 februari 2022 gegevens blijven exporteren?
  
Nee, de buitengebruikstelling is aangekondigd in december 2019 en de vereiste exportmogelijkheden werden tot 1 februari 2022 verschaft. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Worden de gegevens van de klant met betrekking tot de Dynamics 365 Talent - Attract- en Onboard-apps in Dataverse na 1 februari 2022 verwijderd?

Nee, de Dataverse-entiteiten blijven zelfs na de buitengebruikstelling in de Microsoft Dataverse-omgeving van de klant aanwezig, tenzij de oplossing Human Capital Management Talent wordt verwijderd.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Ik weet de naam van de Talent-omgeving. Hoe kan ik de Attract- en Onboard-gegevens in Dataverse bekijken?

1.  Meld u aan bij Power Apps: https://make.powerapps.com
2.  Selecteer de omgeving waarin u Attract- en Onboard-gegevens wilt bekijken.
3.  Ga naar **Dataverse > Tabellen**. 
4.  Typ 'msdyn_' in **Zoeken**. Als u de lijst met tabellen ziet die beginnen met 'msdyn_' + tabelnamen (voorbeeld: msdyn_candidate), hebt u de omgeving met Attract- en Onboard-gegevens gevonden.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Ik weet de naam van de Talent-omgeving niet. Hoe kan ik de omgeving vinden met de gegevens voor de toepassingen Dynamics 365 Talent: Attract en Dynamics 365 Talent: Onboard?

1)  Meld u aan bij het Power Platform-beheercentrum: https://admin.powerplatform.microsoft.com/
2)  Selecteer **Omgevingen**.
3)  Selecteer een bepaalde omgeving om te evalueren.
4)  Selecteer **Resources > Dynamics 365-apps**.
5)  Als u ziet dat de oplossing **HCM Talent** is geïnstalleerd, moeten de Attract- en Onboard-gegevens in deze omgeving zijn opgeslagen. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> De oplossing **HCM Talent** wordt ook gebruikt in Dynamics 365 Human Resources.

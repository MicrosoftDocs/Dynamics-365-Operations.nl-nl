---
title: Voorbeeldquery voor kandidaten voor aanstelling
description: Dit artikel geeft een voorbeeldquery voor de entiteit Kandidaten voor aanstelling in Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2dd744665d4f0b6c64f4ee45a01c237081018514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848337"
---
# <a name="example-query-for-candidate-to-hire"></a>Voorbeeldquery voor kandidaten voor aanstelling


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dit artikel geeft een voorbeeldquery voor de entiteit Kandidaten voor aanstelling in Dynamics 365 Human Resources.

In dit artikel wordt beschreven hoe u *diepte-invoegingen* kunt gebruiken om alle details van een nieuwe kandidaatrecord in één API-bewerking te maken. Zie [Verwante entiteitsrecords maken in één bewerking](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation) voor meer informatie over diepte-invoegingen.

De entiteit **mshr_hcmcandidatetohireentity** is uniek vanwege de relatie met de entiteit **mshr_dirpersonentity**. Veel van de eigenschappen in de entiteit **mshr_hcmcandidatetohireentity** (bijvoorbeeld **mshr_firstname**, **mshr_lastname** en **mshr_birthdate**) zijn afgeleid van de record **mshr_dirpersonentity**. Als u een record voor een nieuwe kandidaat boekt op **mshr_hcmcandidatetohireentity** zonder diepte-invoegingen te gebruiken, kunt u waarden voor deze eigenschappen rechtstreeks in de record **mshr_hcmcandidatetohireentity** definiëren. De bijbehorende recors **mshr_dirpersonentity** wordt speciaal gemaakt met de gedefinieerde waarden voor de eigenschappen. U kunt vervolgens andere gerelateerde entiteitsrecords (zoals vaardigheden of opleiding) maken als afzonderlijke API-aanroepen.

Als u echter diepte-invoegingen wilt gebruiken om alle verwante entiteiten in één bewerking te maken, moeten de eigenschappen die specifiek zijn voor de entiteit **mshr_dirpersonentity** worden gedefinieerd op het geneste niveau van de bewerking.

In dit voorbeeld kunt u een kandidaatrecord, de bijbehorende persoonsrecord en de vaardigheden en opleiding van de persoon op drie geneste niveaus maken door middel van diepte-invoegingen in één API-bewerking.

> [!NOTE]
> Het voorbeeld bevat niet alle eigenschappen van elk van de API-entiteiten. De functie is vereenvoudigd voor demonstratiedoeleinden.

**Aanvragen**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**Antwoord**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

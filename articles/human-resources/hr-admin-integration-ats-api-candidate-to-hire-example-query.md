---
title: Voorbeeldquery voor kandidaten voor aanstelling
description: Dit onderwerp geeft een voorbeeldquery voor de entiteit Kandidaten voor aanstelling in Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ea6fc745ffb5892a32196394cb28cb5e646b7639
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795064"
---
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="0e9e4-103">Voorbeeldquery voor kandidaten voor aanstelling</span><span class="sxs-lookup"><span data-stu-id="0e9e4-103">Example query for Candidate to hire</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0e9e4-104">Dit onderwerp geeft een voorbeeldquery voor de entiteit Kandidaten voor aanstelling in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0e9e4-105">In dit onderwerp wordt beschreven hoe u *diepte-invoegingen* kunt gebruiken om alle details van een nieuwe kandidaatrecord in één API-bewerking te maken.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="0e9e4-106">Zie [Verwante entiteitsrecords maken in één bewerking](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation) voor meer informatie over diepte-invoegingen.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-106">For more information about deep inserts, see [Create related entity records in one operation](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="0e9e4-107">De entiteit **mshr_hcmcandidatetohireentity** is uniek vanwege de relatie met de entiteit **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="0e9e4-108">Veel van de eigenschappen in de entiteit **mshr_hcmcandidatetohireentity** (bijvoorbeeld **mshr_firstname**, **mshr_lastname** en **mshr_birthdate**) zijn afgeleid van de record **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="0e9e4-109">Als u een record voor een nieuwe kandidaat boekt op **mshr_hcmcandidatetohireentity** zonder diepte-invoegingen te gebruiken, kunt u waarden voor deze eigenschappen rechtstreeks in de record **mshr_hcmcandidatetohireentity** definiëren.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="0e9e4-110">De bijbehorende recors **mshr_dirpersonentity** wordt speciaal gemaakt met de gedefinieerde waarden voor de eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="0e9e4-111">U kunt vervolgens andere gerelateerde entiteitsrecords (zoals vaardigheden of opleiding) maken als afzonderlijke API-aanroepen.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="0e9e4-112">Als u echter diepte-invoegingen wilt gebruiken om alle verwante entiteiten in één bewerking te maken, moeten de eigenschappen die specifiek zijn voor de entiteit **mshr_dirpersonentity** worden gedefinieerd op het geneste niveau van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="0e9e4-113">In dit voorbeeld kunt u een kandidaatrecord, de bijbehorende persoonsrecord en de vaardigheden en opleiding van de persoon op drie geneste niveaus maken door middel van diepte-invoegingen in één API-bewerking.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="0e9e4-114">Het voorbeeld bevat niet alle eigenschappen van elk van de API-entiteiten.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="0e9e4-115">De functie is vereenvoudigd voor demonstratiedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="0e9e4-116">**Aanvragen**</span><span class="sxs-lookup"><span data-stu-id="0e9e4-116">**Request**</span></span>

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

<span data-ttu-id="0e9e4-117">**Antwoord**</span><span class="sxs-lookup"><span data-stu-id="0e9e4-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="0e9e4-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0e9e4-118">See also</span></span>

[<span data-ttu-id="0e9e4-119">Integratie-API voor sollicitantenvolgsysteem - Inleiding</span><span class="sxs-lookup"><span data-stu-id="0e9e4-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
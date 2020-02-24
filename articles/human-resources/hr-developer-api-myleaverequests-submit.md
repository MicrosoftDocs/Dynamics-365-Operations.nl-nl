---
title: Een verlofverzoek indienen bij een werkstroom
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008666"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="1a07a-102">Een verlofverzoek indienen bij een werkstroom</span><span class="sxs-lookup"><span data-stu-id="1a07a-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="1a07a-103">In Microsoft Dynamics 365 Human Resources kunt u de API (Application Programming Interface) MyLeaveRequests submit() gebruiken om een verlofaanvraag in te dienen bij de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="1a07a-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="1a07a-104">Deze API wordt als actie weergegeven in de entiteit MyLeaveRequests OData.</span><span class="sxs-lookup"><span data-stu-id="1a07a-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1a07a-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="1a07a-105">Prerequisites</span></span>

<span data-ttu-id="1a07a-106">De verlofaanvraag moet worden opgeslagen in de database en moet kunnen worden opgehaald via de entiteit MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="1a07a-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="1a07a-107">Machtigingen</span><span class="sxs-lookup"><span data-stu-id="1a07a-107">Permissions</span></span>

<span data-ttu-id="1a07a-108">Een van de volgende machtigingen is vereist om deze API te kunnen aanroepen.</span><span class="sxs-lookup"><span data-stu-id="1a07a-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="1a07a-109">Zie [Verificatie](hr-developer-api-authentication.md) voor meer informatie over machtigingen en het selecteren hiervan.</span><span class="sxs-lookup"><span data-stu-id="1a07a-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="1a07a-110">Machtigingstype</span><span class="sxs-lookup"><span data-stu-id="1a07a-110">Permission type</span></span>                    | <span data-ttu-id="1a07a-111">Machtigingen (van laagste naar hoogste bevoegdheidsniveau)</span><span class="sxs-lookup"><span data-stu-id="1a07a-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="1a07a-112">Gedelegeerd (werk- of schoolaccount)</span><span class="sxs-lookup"><span data-stu-id="1a07a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1a07a-113">gebruikers\_imitatie</span><span class="sxs-lookup"><span data-stu-id="1a07a-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="1a07a-114">HTTPS-aanvraag</span><span class="sxs-lookup"><span data-stu-id="1a07a-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="1a07a-115">De aanvraag voldoet aan OData-normen.</span><span class="sxs-lookup"><span data-stu-id="1a07a-115">The request conforms to OData standards.</span></span> <span data-ttu-id="1a07a-116">De parameters {requestId}, {leaveType}, {leaveDate} en {dataArea} verwijzen naar de velden die de samengestelde natuurlijke sleutel vormen voor de entiteit MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="1a07a-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="1a07a-117">Terwijl de velden voor de entiteit MyLeaveRequests verwijzen naar een afzonderlijke regel in de verlofaanvraag, wordt door het aanroepen van de Submit-API de volledige aanvraag voor het verlof (alle regels) ingediend bij de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="1a07a-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="1a07a-118">Kopteksten voor aanvraag</span><span class="sxs-lookup"><span data-stu-id="1a07a-118">Request headers</span></span>

| <span data-ttu-id="1a07a-119">Koptekst</span><span class="sxs-lookup"><span data-stu-id="1a07a-119">Header</span></span>         | <span data-ttu-id="1a07a-120">Value</span><span class="sxs-lookup"><span data-stu-id="1a07a-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="1a07a-121">Autorisatie</span><span class="sxs-lookup"><span data-stu-id="1a07a-121">Authorization</span></span>  | <span data-ttu-id="1a07a-122">Bearer {token} (vereist)</span><span class="sxs-lookup"><span data-stu-id="1a07a-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="1a07a-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1a07a-123">Content-Type</span></span>   | <span data-ttu-id="1a07a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1a07a-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="1a07a-125">Aanvraagtekst</span><span class="sxs-lookup"><span data-stu-id="1a07a-125">Request body</span></span>

<span data-ttu-id="1a07a-126">Geef voor deze methode geen aanvraagtekst op.</span><span class="sxs-lookup"><span data-stu-id="1a07a-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="1a07a-127">Antwoord</span><span class="sxs-lookup"><span data-stu-id="1a07a-127">Response</span></span>

<span data-ttu-id="1a07a-128">Een geslaagde respons is altijd een respons **204 Geen inhoud**.</span><span class="sxs-lookup"><span data-stu-id="1a07a-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="1a07a-129">Niet-geautoriseerde aanroepers ontvangen een respons **401 Niet-geautoriseerd** of **403 Verboden**.</span><span class="sxs-lookup"><span data-stu-id="1a07a-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="1a07a-130">Als de indiening mislukt (bijvoorbeeld vanwege de validatie), is de respons **500 Serverfout** en bevat de responstekst een JSON-object met nadere details.</span><span class="sxs-lookup"><span data-stu-id="1a07a-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="1a07a-131">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="1a07a-131">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="1a07a-132">Validatie- en foutberichten</span><span class="sxs-lookup"><span data-stu-id="1a07a-132">Validation and error messages</span></span>

<span data-ttu-id="1a07a-133">Als onderdeel van de aanroep van de Submit-API voert Human Resources de validatie van bedrijfslogica uit vóór indiening, waardoor de verlofaanvraag een geldige status heeft voor indiening.</span><span class="sxs-lookup"><span data-stu-id="1a07a-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="1a07a-134">De mogelijke foutberichten die worden weergegeven in de respons als validaties mislukken zijn:</span><span class="sxs-lookup"><span data-stu-id="1a07a-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="1a07a-135">Met de aanvraag wordt het saldo '{LeaveTypeId}' onder het toegestane minimumsaldo van {date} gezet.</span><span class="sxs-lookup"><span data-stu-id="1a07a-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="1a07a-136">Verlofaanvraag met status Voltooid kan niet worden ingediend.</span><span class="sxs-lookup"><span data-stu-id="1a07a-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="1a07a-137">Kan de aanvraag niet indienen of opslaan omdat er geen wijzigingen zijn aangebracht.</span><span class="sxs-lookup"><span data-stu-id="1a07a-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="1a07a-138">Voeg het bedrag of het verloftype toe of werk het bij en probeer vervolgens het opnieuw.</span><span class="sxs-lookup"><span data-stu-id="1a07a-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="1a07a-139">De ingevoerde verlofaanvraag bevat een of meer dagen met dezelfde datum en hetzelfde verloftype als een bestaande aanvraag in behandeling.</span><span class="sxs-lookup"><span data-stu-id="1a07a-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="1a07a-140">Trek de bestaande aanvraag in om wijzigingen aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="1a07a-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="1a07a-141">Redencode '{ReasonCodeId}' is niet van toepassing op een van de verloftypen in de aanvraag.</span><span class="sxs-lookup"><span data-stu-id="1a07a-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="1a07a-142">Voor verloftype '{LeaveTypeId}' is een redencode vereist.</span><span class="sxs-lookup"><span data-stu-id="1a07a-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="1a07a-143">Selecteer het toepasselijke type en de bijbehorende redencode.</span><span class="sxs-lookup"><span data-stu-id="1a07a-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="1a07a-144">Het indienen van het verlof is mislukt.</span><span class="sxs-lookup"><span data-stu-id="1a07a-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="1a07a-145">Het verlof is opgeslagen als een conceptaanvraag.</span><span class="sxs-lookup"><span data-stu-id="1a07a-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a07a-146">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1a07a-146">See also</span></span>

- [<span data-ttu-id="1a07a-147">MyLeaveRequests-overzicht</span><span class="sxs-lookup"><span data-stu-id="1a07a-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="1a07a-148">Verificatie</span><span class="sxs-lookup"><span data-stu-id="1a07a-148">Authentication</span></span>](hr-developer-api-authentication.md)
---
title: Een verlofverzoek indienen bij een werkstroom
description: In Microsoft Dynamics 365 Human Resources kunt u de API (Application Programming Interface) MyLeaveRequests submit() gebruiken om een verlofaanvraag in te dienen bij de werkstroom.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9b3151cb042012a167854a1e69b55b36981dab19
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054567"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="e9692-103">Een verlofverzoek indienen bij een werkstroom</span><span class="sxs-lookup"><span data-stu-id="e9692-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e9692-104">In Microsoft Dynamics 365 Human Resources kunt u de API (Application Programming Interface) MyLeaveRequests submit() gebruiken om een verlofaanvraag in te dienen bij de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="e9692-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="e9692-105">Deze API wordt als actie weergegeven in de entiteit MyLeaveRequests OData.</span><span class="sxs-lookup"><span data-stu-id="e9692-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e9692-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="e9692-106">Prerequisites</span></span>

<span data-ttu-id="e9692-107">De verlofaanvraag moet worden opgeslagen in de database en moet kunnen worden opgehaald via de entiteit MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="e9692-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="e9692-108">Machtigingen</span><span class="sxs-lookup"><span data-stu-id="e9692-108">Permissions</span></span>

<span data-ttu-id="e9692-109">Een van de volgende machtigingen is vereist om deze API te kunnen aanroepen.</span><span class="sxs-lookup"><span data-stu-id="e9692-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="e9692-110">Zie [Verificatie](hr-developer-api-authentication.md) voor meer informatie over machtigingen en het selecteren hiervan.</span><span class="sxs-lookup"><span data-stu-id="e9692-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="e9692-111">Machtigingstype</span><span class="sxs-lookup"><span data-stu-id="e9692-111">Permission type</span></span>                    | <span data-ttu-id="e9692-112">Machtigingen (van laagste naar hoogste bevoegdheidsniveau)</span><span class="sxs-lookup"><span data-stu-id="e9692-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="e9692-113">Gedelegeerd (werk- of schoolaccount)</span><span class="sxs-lookup"><span data-stu-id="e9692-113">Delegated (work or school account)</span></span> | <span data-ttu-id="e9692-114">gebruikers\_imitatie</span><span class="sxs-lookup"><span data-stu-id="e9692-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="e9692-115">HTTPS-aanvraag</span><span class="sxs-lookup"><span data-stu-id="e9692-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="e9692-116">De aanvraag voldoet aan OData-normen.</span><span class="sxs-lookup"><span data-stu-id="e9692-116">The request conforms to OData standards.</span></span> <span data-ttu-id="e9692-117">De parameters {requestId}, {leaveType}, {leaveDate} en {dataArea} verwijzen naar de velden die de samengestelde natuurlijke sleutel vormen voor de entiteit MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="e9692-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="e9692-118">Terwijl de velden voor de entiteit MyLeaveRequests verwijzen naar een afzonderlijke regel in de verlofaanvraag, wordt door het aanroepen van de Submit-API de volledige aanvraag voor het verlof (alle regels) ingediend bij de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="e9692-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="e9692-119">Kopteksten voor aanvraag</span><span class="sxs-lookup"><span data-stu-id="e9692-119">Request headers</span></span>

| <span data-ttu-id="e9692-120">Koptekst</span><span class="sxs-lookup"><span data-stu-id="e9692-120">Header</span></span>         | <span data-ttu-id="e9692-121">Value</span><span class="sxs-lookup"><span data-stu-id="e9692-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="e9692-122">Autorisatie</span><span class="sxs-lookup"><span data-stu-id="e9692-122">Authorization</span></span>  | <span data-ttu-id="e9692-123">Bearer {token} (vereist)</span><span class="sxs-lookup"><span data-stu-id="e9692-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="e9692-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e9692-124">Content-Type</span></span>   | <span data-ttu-id="e9692-125">application/json</span><span class="sxs-lookup"><span data-stu-id="e9692-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="e9692-126">Aanvraagtekst</span><span class="sxs-lookup"><span data-stu-id="e9692-126">Request body</span></span>

<span data-ttu-id="e9692-127">Geef voor deze methode geen aanvraagtekst op.</span><span class="sxs-lookup"><span data-stu-id="e9692-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="e9692-128">Antwoord</span><span class="sxs-lookup"><span data-stu-id="e9692-128">Response</span></span>

<span data-ttu-id="e9692-129">Een geslaagde respons is altijd een respons **204 Geen inhoud**.</span><span class="sxs-lookup"><span data-stu-id="e9692-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="e9692-130">Niet-geautoriseerde aanroepers ontvangen een respons **401 Niet-geautoriseerd** of **403 Verboden**.</span><span class="sxs-lookup"><span data-stu-id="e9692-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="e9692-131">Als de indiening mislukt (bijvoorbeeld vanwege de validatie), is de respons **500 Serverfout** en bevat de responstekst een JSON-object met nadere details.</span><span class="sxs-lookup"><span data-stu-id="e9692-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="e9692-132">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="e9692-132">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="e9692-133">Validatie- en foutberichten</span><span class="sxs-lookup"><span data-stu-id="e9692-133">Validation and error messages</span></span>

<span data-ttu-id="e9692-134">Als onderdeel van de aanroep van de Submit-API voert Human Resources de validatie van bedrijfslogica uit vóór indiening, waardoor de verlofaanvraag een geldige status heeft voor indiening.</span><span class="sxs-lookup"><span data-stu-id="e9692-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="e9692-135">De mogelijke foutberichten die worden weergegeven in de respons als validaties mislukken zijn:</span><span class="sxs-lookup"><span data-stu-id="e9692-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="e9692-136">Met de aanvraag wordt het saldo '{LeaveTypeId}' onder het toegestane minimumsaldo van {date} gezet.</span><span class="sxs-lookup"><span data-stu-id="e9692-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="e9692-137">Verlofaanvraag met status Voltooid kan niet worden ingediend.</span><span class="sxs-lookup"><span data-stu-id="e9692-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="e9692-138">Kan de aanvraag niet indienen of opslaan omdat er geen wijzigingen zijn aangebracht.</span><span class="sxs-lookup"><span data-stu-id="e9692-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="e9692-139">Voeg het bedrag of het verloftype toe of werk het bij en probeer vervolgens het opnieuw.</span><span class="sxs-lookup"><span data-stu-id="e9692-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="e9692-140">De ingevoerde verlofaanvraag bevat een of meer dagen met dezelfde datum en hetzelfde verloftype als een bestaande aanvraag in behandeling.</span><span class="sxs-lookup"><span data-stu-id="e9692-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="e9692-141">Trek de bestaande aanvraag in om wijzigingen aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="e9692-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="e9692-142">Redencode '{ReasonCodeId}' is niet van toepassing op een van de verloftypen in de aanvraag.</span><span class="sxs-lookup"><span data-stu-id="e9692-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="e9692-143">Voor verloftype '{LeaveTypeId}' is een redencode vereist.</span><span class="sxs-lookup"><span data-stu-id="e9692-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="e9692-144">Selecteer het toepasselijke type en de bijbehorende redencode.</span><span class="sxs-lookup"><span data-stu-id="e9692-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="e9692-145">Het indienen van het verlof is mislukt.</span><span class="sxs-lookup"><span data-stu-id="e9692-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="e9692-146">Het verlof is opgeslagen als een conceptaanvraag.</span><span class="sxs-lookup"><span data-stu-id="e9692-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9692-147">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e9692-147">See also</span></span>

- [<span data-ttu-id="e9692-148">MyLeaveRequests-overzicht</span><span class="sxs-lookup"><span data-stu-id="e9692-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="e9692-149">Verificatie</span><span class="sxs-lookup"><span data-stu-id="e9692-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
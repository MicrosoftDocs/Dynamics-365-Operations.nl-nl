---
title: Een verlofverzoek indienen bij een werkstroom
description: In Microsoft Dynamics 365 Human Resources kunt u de API (Application Programming Interface) MyLeaveRequests submit() gebruiken om een verlofaanvraag in te dienen bij de werkstroom.
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba2867646ac03953a43404984a5d04d4edb1f5ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686990"
---
# <a name="submit-a-leave-request-to-workflow"></a>Een verlofverzoek indienen bij een werkstroom


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In Microsoft Dynamics 365 Human Resources kunt u de API (Application Programming Interface) MyLeaveRequests submit() gebruiken om een verlofaanvraag in te dienen bij de werkstroom. Deze API wordt als actie weergegeven in de entiteit MyLeaveRequests OData.

## <a name="prerequisites"></a>Vereisten

De verlofaanvraag moet worden opgeslagen in de database en moet kunnen worden opgehaald via de entiteit MyLeaveRequests.

## <a name="permissions"></a>Machtigingen

Een van de volgende machtigingen is vereist om deze API te kunnen aanroepen. Zie [Verificatie](hr-developer-api-authentication.md) voor meer informatie over machtigingen en het selecteren hiervan.

| Machtigingstype                    | Machtigingen (van laagste naar hoogste bevoegdheidsniveau) |
|------------------------------------|--------------------------------------------------------|
| Gedelegeerd (werk- of schoolaccount) | gebruikers\_imitatie                                    |

## <a name="https-request"></a>HTTPS-aanvraag

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

De aanvraag voldoet aan OData-normen. De parameters {requestId}, {leaveType}, {leaveDate} en {dataArea} verwijzen naar de velden die de samengestelde natuurlijke sleutel vormen voor de entiteit MyLeaveRequests.

> [!NOTE]
> Terwijl de velden voor de entiteit MyLeaveRequests verwijzen naar een afzonderlijke regel in de verlofaanvraag, wordt door het aanroepen van de Submit-API de volledige aanvraag voor het verlof (alle regels) ingediend bij de werkstroom.

### <a name="request-headers"></a>Kopteksten voor aanvraag

| Koptekst         | Value                     |
|----------------|---------------------------|
| Autorisatie  | Bearer {token} (vereist) |
| Content-Type   | application/json          |

### <a name="request-body"></a>Aanvraagtekst

Geef voor deze methode geen aanvraagtekst op.

### <a name="response"></a>Antwoord

Een geslaagde respons is altijd een respons **204 Geen inhoud**.

Niet-geautoriseerde aanroepers ontvangen een respons **401 Niet-geautoriseerd** of **403 Verboden**.

Als de indiening mislukt (bijvoorbeeld vanwege de validatie), is de respons **500 Serverfout** en bevat de responstekst een JSON-object met nadere details.

## <a name="example"></a>Voorbeeld

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

## <a name="validation-and-error-messages"></a>Validatie- en foutberichten

Als onderdeel van de aanroep van de Submit-API voert Human Resources de validatie van bedrijfslogica uit vóór indiening, waardoor de verlofaanvraag een geldige status heeft voor indiening. De mogelijke foutberichten die worden weergegeven in de respons als validaties mislukken zijn:

 - Met de aanvraag wordt het saldo '{LeaveTypeId}' onder het toegestane minimumsaldo van {date} gezet.
 - Verlofaanvraag met status Voltooid kan niet worden ingediend.
 - Kan de aanvraag niet indienen of opslaan omdat er geen wijzigingen zijn aangebracht. Voeg het bedrag of het verloftype toe of werk het bij en probeer vervolgens het opnieuw.
 - De ingevoerde verlofaanvraag bevat een of meer dagen met dezelfde datum en hetzelfde verloftype als een bestaande aanvraag in behandeling. Trek de bestaande aanvraag in om wijzigingen aan te brengen.
 - Redencode '{ReasonCodeId}' is niet van toepassing op een van de verloftypen in de aanvraag.
 - Voor verloftype '{LeaveTypeId}' is een redencode vereist. Selecteer het toepasselijke type en de bijbehorende redencode.
 - Het indienen van het verlof is mislukt. Het verlof is opgeslagen als een conceptaanvraag.

## <a name="see-also"></a>Zie ook

- [MyLeaveRequests-overzicht](hr-developer-api-myleaverequests-overview.md)
- [Verificatie](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Vergoedingsplan voor medewerker in salarisadministratie
description: Dit onderwerp geeft informatie over en een voorbeeldquery voor de entiteit Vergoedingenplan voor medewerker in salarisadministratie in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0837d9a153aba554d0a5293d16afb309bd37963c270da5b67e691558cae63b0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758707"
---
# <a name="payroll-worker-benefit-plan"></a>Vergoedingsplan voor medewerker in salarisadministratie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Vergoedingenplan voor medewerker in salarisadministratie voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>Beschrijving

Deze entiteit geeft informatie over het vergoedingenplan voor een bepaalde werknemer.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Personeelsnummer**</br>mshr_personnelnumber</br>*Tekenreeks* | Alleen-lezen</br>Vereist | Het unieke personeelsnummer van de werknemer. |
| **Rechtspersoon-ID**</br>mshr_legalentityID</br>*Tekenreeks* | Alleen-lezen | Geeft de rechtspersoon (bedrijf) op. |
| **Periode-ID**</br>id-mshr_periode</br>*Tekenreeks* | Alleen-lezen | De identificatie van de periode. |
| **Plan-id**</br>mshr_planid</br>*Tekenreeks* | Alleen-lezen | De ID van het plan. |
| **Dekkingsoptie**</br>id-mshr_dekkingsoptie</br>*Tekenreeks* | Alleen-lezen | De ID van de dekkingsoptie. |
| **Begindatum van inhouding**</br>mshr_startdatumtijdinhouding</br>*Verschil datum en tijd* | Alleen-lezen | Begindatum inhouding. |
| **Einddatum van inhouding**</br>mshr_einddatumtijdinhouding</br>*Verschil datum en tijd* | Alleen-lezen | Einddatum inhouding. |
| **Status**</br>mshr_status</br>*[Optieset status vergoedingsplan voor werknemer](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Alleen-lezen | Status vergoedingenplan. |
| **Geldig vanaf**</br>mshr_validfrom</br>*Verschil datum en tijd* | Alleen-lezen | Het tijdstip waarop de geldigheid van deze record ingaat. |
| **Geldig tot**</br>mshr_validto</br>*Verschil datum en tijd* |  Alleen-lezen | Het tijdstip waarop deze record niet langer geldig is. |
| **ID plantype**</br>mshr_id-plantype</br>*Tekenreeks* | Alleen-lezen | De ID van het plantype. |
| **Code van plantype**</br>mshr_plantypecode</br>*[optieset voor dekking van type vergoedingsplan](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Alleen-lezen | De specificatie van het plantype. |
| **Aantal betalingsperioden**</br>mshr_betaalperiode</br>*Geheel getal* | Alleen-lezen | Het aantal salarisperioden dat aangeeft hoe vaak de vergoedingsprovider of werknemers worden betaald. Dit bedrag wordt gebruikt om het bedrag van het jaarlijkse vergoedingssalaris voor een werknemer te berekenen. |
| **Werknemersbedrag**</br>mshr_bedragwerknemer</br>*Decimaal* | Alleen-lezen | Het percentage of bedrag voor de werknemer. |
| **Werkgeversbedrag**</br>mshr_bedragwerkgever</br>*Decimaal* | Alleen-lezen | Het percentage of bedrag voor de werkgever. |
| **Primair veld**</br>mshr_primaryfield</br>*Tekenreeks* | Door systeem gegenereerd | Primair veld. |
| **Waarde werknemer-ID** </br>_mshr_fk_werknemer_id_waarde</br>*GUID* | Refererende sleutel: mshr_id-hcmwerknemerbasisentiteit van entiteit mshr_hcmwerknemerbasisentiteit. | Door het systeem gegenereerde unieke id voor de werknemer. |
| **Waarde periode-ID**</br> _mshr_fk_periode_id_waarde</br>*GUID* | Refererende sleutel: mshr_id-vergoedingenperiodeentiteit van entiteit mshr_vergoedingenperiodeentiteit. | Door het systeem gegenereerde unieke id voor de periode. |
| **Waarde plan-ID**</br> _mshr_fk_plan_id_waarde</br>*GUID* | Refererende sleutel: mshr_id-vergoedingenplanentiteit van entiteit mshr_vergoedingenplanentiteit. | Door het systeem gegenereerde unieke id voor het plan. |
| **Waarde plantype-ID**</br> mshr_fk_plantype_id_waarde</br>*GUID* | Refererende sleutel: mshr_id-vergoedingenplantypeentiteit van entiteit mshr_vergoedingenplantypeentiteit. | Door het systeem gegenereerde unieke id voor het plan. |
| **ID-waarde dekkingsoptie**</br> _mshr_fk_dekkingsoptie_id_waarde</br>*GUID* | Refererende sleutel: mshr_id-vergoedingendekkingoptieentiteit van mshr_entiteit vergoedingendekkingoptieentiteit. | Door het systeem gegenereerde unieke id voor het plan. |
| **Waarde ID vergoedingenplan werknemer salarisadministratie**</br> mshr_id-entiteitvergoedingenplanmedewerkersalarisadministratie</br>*GUID* | Alleen-lezen </br> Door systeem gegenereerd | Door het systeem gegenereerde unieke ID voor de record. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Voorbeeldquery voor vergoedingenplan medewerker salarisadministratie

**Aanvragen**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Respons**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

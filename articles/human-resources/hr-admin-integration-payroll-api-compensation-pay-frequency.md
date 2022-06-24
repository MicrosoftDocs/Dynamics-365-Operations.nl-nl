---
title: Compensatiebetalingsfrequentie
description: Dit artikel bevat details en een voorbeeldquery voor de entiteit Compensatiebetalingsfrequentie in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9afe27776797b2355a32226bbd7fa514b5c5d962
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894609"
---
# <a name="compensation-pay-frequency"></a>Compensatiebetalingsfrequentie


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Compensatiebetalingsfrequentie in Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Omschrijving

Deze entiteit biedt informatie over de betalingstariefconversie voor een bepaalde compensatiebetalingsfrequentie.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Omschrijving |
| --- | --- | --- |
| **Jaarlijkse conversie van betalingstarief**</br>mshr_annualconversionfactor</br>*Decimaal* | Alleen-lezen | De jaarlijkse conversiefactor voor de betalingsfrequentie. |
| **Beschrijving**</br>mshr_description</br>*Tekenreeks* | Alleen-lezen | De omschrijving van de conversieverhouding. |
| **Uurconversie van betalingstarief**</br>mshr_hourlyconversionfactor</br>*Decimaal* | Alleen-lezen | De conversiefactor per uur voor de betalingsfrequentie. |
| **Maandelijkse conversie van betalingstarief**</br>mshr_monthlyconversionfactor</br>*Decimaal* | Alleen-lezen | De maandelijkse conversiefactor voor de betalingsfrequentie. |
| **Conversie van loontarief**</br>mshr_payrateconversion</br>*Tekenreeks* | Alleen-lezen | Een unieke tekenreeks om de conversieverhouding te identificeren. |
| **Periode**</br>mshr_period</br>*periode-optie instellen* | Alleen-lezen | De hoofdperiode voor de opgegeven betalingstariefconversie. |
| **Wekelijkse conversie van betalingstarief**</br>mshr_weeklyconversionfactor</br>*Decimaal* | Alleen-lezen | De wekelijkse conversiefactor voor de betalingsfrequentie. |
| **Gegevensgebied-id**</br>mshr_dataareaid</br>*Tekenreeks* | Alleen-lezen | De rechtspersoon (bedrijf). |
| **Entiteit-id van compensatiebetalingsfrequentie**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Door systeem gegenereerd | Een door het systeem gegenereerde unieke GUID-waarde (Globally Unique Identifier) om de record uniek te identificeren. |

## <a name="example-query-for-payroll-employee"></a>Voorbeeldquery voor werknemer in salarisadministratie

**Aanvraag**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Respons**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

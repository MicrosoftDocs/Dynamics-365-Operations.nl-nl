---
title: Uitbreidbaarheid van basisopsomming voor geslacht
description: Dit artikel biedt een overzicht van de uitgebreidheid van de basisopsomming voor geslacht.
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749311"
---
# <a name="gender-base-enum-extensibility"></a>Uitbreidbaarheid van basisopsomming voor geslacht

De opsomming **Geslacht** is nu uitbreidbaar. In dit artikel worden de wijzigingen beschreven die u moet aanbrengen in de codebasis als u van plan bent om de opsomming voor **Geslacht** uit te breiden.

## <a name="gender-vs-hcmpersongender"></a>Geslacht en HcmPersonGender

Er zijn twee opsommingen voor geslachtswaarden:

- **Geslacht** (toepassingsplatform)
- **HcmPersonGender** (PersonnelManagement)

**Geslacht** wordt gebruikt in Microsoft Dynamics 365 Finance en **HcmPersonGender** in HCM-functionaliteit (Human Capital Management). Als u gebruikmaakt van HCM-functionaliteit en u wijzigingen in de opsomming **Geslacht** aanbrengt, moet u overwegen dezelfde wijzigingen ook aan te brengen in **HcmPersonGender**. Als u bijvoorbeeld **Transgender** aan de opsomming **Geslacht** toevoegt, voegt u **Transgender** ook toe aan **HcmPersonGender**.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (klasse)

Er is een nieuwe klasse **HcmPersonGenderTranformUtil** gemaakt voor vertalingen tussen de twee basisopsommingen. Deze klasse bevat twee methoden: **convertGenderToHcmPersonGender** en **convertHcmPersonGenderToGender**. U moet een extensie maken met de klasse **Opdrachtstructuur** of **gebeurtenishandlers** en beide methoden uitbreiden om nieuwe waarden toe te wijzen die aan een van beide basisopsommingen zijn toegevoegd.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (klasse)

**PayrollStateWageTaxPrepDP** is de gegevensproviderklasse voor het SSRS-rapport (SQL Server Reporting Services) **Payroll State Wage Tax Prep**. Voor de Verenigde Staten zijn drie waarden beschikbaar: **Mannelijk**, **Vrouwelijk** en **Niet opgegeven**. In de methode **populatePayrollStateWageTaxPrepTmp** is een switch-instructie opgenomen die wordt gebruikt om de waarde van de opsomming **HcmPersonGender** toe te wijzen aan één van drie velden: **IsMale**, **IsFemale** of **IsUnspecifiedGender**. De standaardwaarde voor de switch-instructie is **IsUnspecifiedGender**. Als u waarden toevoegt aan **HcmPersonGender** voor een andere toewijzing, moet u een extensie maken met behulp van de klasse **Opdrachtstructuur** in plaats van de methode **populatePayrollStateWageTaxPrepTmp** om de waarde waar nodig te wijzigen.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (klasse)

Met de integratieklasse **smmOutlookSync_Contact** worden waarden van **Outlook** en **Contactpersonen** gekoppeld. **Outlook** ondersteunt drie waarden: **Mannelijk**, **Vrouwelijk** en **Niet opgegeven**. De klasse biedt twee manieren om **Genders** toe te wijzen aan **OutlookGenders**. De standaardmethode is **NonSpecific/UnSpecified**. Als u extra waarden maakt voor de opsomming **Geslacht**, moet u een extensie maken met de klasse **Opdrachtstructuur** in plaats van beide methoden te gebruiken en de vereiste toewijzingen op te geven.

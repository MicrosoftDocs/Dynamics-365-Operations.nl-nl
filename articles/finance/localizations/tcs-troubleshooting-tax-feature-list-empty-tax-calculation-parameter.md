---
title: Lege lijst met btw-functies in parameters voor belastingberekening
description: In dit onderwerp wordt uitgelegd hoe u een probleem oplost waarbij de lijst met btw-functies op de pagina Parameters van belastingberekening leeg is.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 5b87499042c9c4bfe76e182b170adf4f1cfeac4b
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388552"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Lege lijst met btw-functies in parameters voor belastingberekening

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="symptom"></a>Symptoom

U hebt een functie gepubliceerd in RCS (Regulatory Configuration Service), zodat u deze kunt gebruiken in Microsoft Dynamics 365 Finance. Wanneer u Finance opent en naar **Belasting** \> **Instellen** \> **Belastingconfiguratie** \> **Parameters voor belastingberekening** gaat en een waarde probeer te selecteren inhet veld **Naam van functie-instelling**, dan is de lijst met waarden leeg.

## <a name="reason"></a>Reden

Dit probleem treedt meestal op omdat uw Finance-omgeving en RCS-omgeving niet onder dezelfde tenant vallen.

### <a name="rcs-tenant"></a>RCS-tenant

Voer deze stappen uit om id aan uw RCS-tenant te vinden.

1. Kopieer de volledige RCS-URL. De URL kan bijvoorbeeld `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace` zijn.
2. Open een InPrivate-browservenster, plak de RCS-URL in de adresbalk en selecteer **Invoeren**. U wordt doorverwezen naar de aanmeldingspagina, waar u de tenant-id van RCS kunt vinden. Als de URL van de aanmeldingspagina bijvoorbeeld `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d` is, is de tenant-id de informatie die na `https://login.microsoftonline.com/` wordt vermeld, oftewel **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Tenant-id voor Finance-omgeving

Om de tenant-id voor uw Finance-omgeving te vinden, volgt u dezelfde stappen als die u hebt gevolgd om de RCS-tenant op te zoeken. Kopieer en plak echter de volledige URL van uw Finance-omgeving in plaats van de volledige RCS-URL.

## <a name="resolution"></a>Oplossing

Als de twee tenant-id's verschillen, ondervindt u het probleem dat in dit onderwerp wordt beschreven. Als ze hetzelfde zijn, is er sprake van een niet-gerelateerd probleem. In dat geval is het raadzaam om contact op te nemen met Microsoft Ondersteuning.

### <a name="solution-1"></a>Oplossing 1

Meld u aan bij uw RFS-omgeving in bij dezelfde tenant als waar uw Finance-omgeving is aangemeld. Maak vervolgens de belastingfunctie en publiceer deze.

### <a name="solution-2"></a>Oplossing 2

Deel de belastingfunctie met de Finance-tenant in RCS.

1. Ga in RCS naar **Globaliseringsfuncties** \> **Belastingberekening**.
2. Selecteer de functie die u wilt delen en selecteer vervolgens **Delen met** op het tabblad **Organisaties**.
3. Voer in het veld **Domeinnaam invoeren** een naam in. Voer bijvoorbeeld **contoso.onmicrosoft.com** in.
4. Selecteer **Delen**.

![Dialoogvenster Delen met externe organisatie.](media/ShareTaxFeature.png)

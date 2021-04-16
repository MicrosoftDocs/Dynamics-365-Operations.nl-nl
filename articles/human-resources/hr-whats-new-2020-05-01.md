---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (1 mei 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 1 mei 2020.
author: andreabichsel
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 52eb748fe8b3c62d6a5ebf46fd01afc291ec5572
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803412"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (1 mei 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.3196. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Nieuwe entiteiten voor prestatiebeheer beschikbaar in Data Management Framework (DMF)

De volgende entiteiten zijn nu beschikbaar. Als deze entiteiten niet worden weergegeven in de lijst met entiteiten, gebruikt u de optie **Entiteiten vernieuwen** in **Raamwerkparameters >Entiteitsinstellingen > Entiteitslijst vernieuwen**.

- **Discussiecompetentie**
- **Discussiedoelen**
- **Discussiemeting**
- **Discussie-onderwerp**
- **Prestatiejournaal**
- **Afmeting**
- **Doelmeting**

Bovendien zijn **Totale score** en **Gemiddelde score** toegevoegd aan de entiteit **Discussie**.

## <a name="increase-length-of-leave-request-comments-275641"></a>Opmerkingen voor verlofaanvragen mogen langer zijn (275641)

Opmerkingen over verlofaanvragen staan nu meer dan 100 tekens toe.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>De laatste opmerkingen over beoordelingen worden niet weergegeven wanneer de manager of werknemer is aangemeld bij een ander bedrijf (431688)

Alle opmerkingen worden nu weergegeven bij het bekijken van beoordelingen.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Door de gebruiker gedefinieerde koppelingen worden niet ondersteund op een nieuw werknemersformulier (390374)

Door de gebruiker gedefinieerde koppelingen worden nu ingeschakeld op het gestroomlijnde formulier **Werknemer**.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity veroorzaakt OData API-fout (439476)

Deze wijziging lost de API-crash op. Een dubbele naam is de oorzaak van deze fout.

## <a name="in-preview"></a>Preview

## <a name="leave-suspension"></a>Verlof opschorten

U kunt verlof en verzuim in Human Resources opschorten voor een werknemer. Als u het verlof opschort, wordt het toegerekende verlof stopgezet voor de geselecteerde verloftypen. Als het opschorten plaatsvindt nadat een toerekening is verwerkt, wordt door het onderbreken van het verlof een evenredige correctie in het verlof van de werknemer gemaakt. Zie [Verlof opschorten](hr-leave-and-absence-suspend-leave.md) voor meer informatie.

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Update voor gebruikerservaring om aan te geven dat toerekening wordt opgeschort (429550)

De gebruikerservaring geeft nu aan dat de toerekening voor een plan is opgeschort.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Toerekening voor verlof voor opgegeven verloftypen opschorten (272447)

In deze versie kan in HR een regel worden gemaakt voor het opschorten van verloftoerekeningen voor werknemers met verlofaanvragen voor onbetaald verlof. Onbetaald verlof kan een type zijn, maar dat hoeft niet. U kunt elk verlof uitstellen op basis van een ander verloftype.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-entiteit beschikbaar voor opschorten van toerekeningen (429549)

Een DMF-entiteit is nu beschikbaar voor opschorten van toerekeningen.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Redencode toevoegen voor opschorten van toerekeningen (429547)

Er zijn redencodes toegevoegd voor het opschorten van de toerekening.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Begin van overgang van HR-parameters naar verlof- en verzuimparameters

Deze release begint met het combineren van HR-parameters met verlof- en verzuimparameters.

## <a name="carry-forward-rules"></a>Regels voor transporteren

U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt. Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen. Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.

## <a name="known-issues"></a>Bekende problemen

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-voorbeeld werkt niet in sommige omgevingen

Als het documentvoorbeeld voor documenten opgeslagen in SharePoint niet werkt, voert u de volgende procedure uit:

1. Controleer voor de gebruikersaccount Beheerder of er een e-mailadres is gekoppeld aan de gebruikersrecord. Deze gegevens worden weergegeven op de pagina **Gebruiker**. Als er geen e-mailadres is ingesteld, moet u het e-mailadres en de provider toevoegen met de Excel-invoegtoepassing OData. Standaard is het e-mailadres niet aanwezig in het Excel-ontwerp. U moet het Excel-ontwerp bewerken, alle velden toevoegen, toepassen en vernieuwen. Wanneer u deze stappen hebt voltooid, kunt u de beheerdersaccount bijwerken.

2. Nadat aan de beheerdersaccount een e-mailaccount is gekoppeld, meldt u zich aan bij Human Resources met beheerdersreferenties.

3. Open een bijlage in SharePoint om de voorbeeldweergave van documenten te starten.

4. Meld u aan met een andere gebruikersaccount die toegang heeft tot bijlagen en controleer of het voorbeeld werkt zoals verwacht.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
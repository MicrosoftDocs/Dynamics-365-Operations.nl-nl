---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (14 mei 2020)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3ce1aca9cebc5b330f054a11e38b5dfc4fc9109d
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555166"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (14 mei 2020)

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Human Resources. Wijzigingen die van toepassing zijn op buildnummer 8.1.3244. De getallen tussen haakjes in sommige koppen verwijzen ter referentie naar ondersteuningsnummers in Lifecycle Services (LCS).

## <a name="platform-changes"></a>Platformwijzigingen

In de release van deze week zijn platformwijzigingen opgenomen. Zie [Platformupdates voor versie 10.0.10 van Finance and Operations-apps (mei 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34) voor meer informatie. Deze versie bevat correcties en wijzigingen in opgeslagen weergaven.
 
## <a name="ensure-common-data-service-picklists-are-consistent-with-leave-enums-436343"></a>Zorg ervoor dat Common Data Service-selectielijsten consistent zijn met Verlof-enums (436343)

Common Data Service-selectielijsten zijn nu consistent met Verlof-enums.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Gebruikers toestaan om werkstroom voor verlofverzoek te configureren op basis van het aanvraagbedrag (300044)

Gebruikers kunnen werkstromen voor verlofverzoeken configureren op basis van aanvraagbedragen.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Met het nieuwe formulier voor medewerkers worden gegevens beschikbaar gesteld via het menu Beeld als geavanceerde beveiliging is ingeschakeld (403185)

In deze release wordt de weergave van medewerkers in verschillende rechtspersonen gecorrigeerd wanneer geavanceerde toegang is ingeschakeld en medewerkerfs in andere bedrijven toegankelijk zijn.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Uitvoeren van transitorische posten toestaan voor een enkel plan of een enkel bedrijf (318844)

Met deze wijziging kunt u transitorische posten voor een bedrijf of een plan uitvoeren.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>De fulltime equivalenten van de positie weergeven in het formulier Geregistreerde medewerkers (414658)

De FTE-waarde van de positie van een medewerker bepaalt het toerekeningstarief van een medewerker wanneer de FTE-optie is ingeschakeld voor het verloftype. Dit veld is nu opgenomen in het formulier **Geregistreerde medewerkers** en het dialoogvenster **Massale inschrijving**.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Batchtaak voor vervallen van verlofsaldo toevoegen (431266)

Er is nu een nieuwe batchtaak beschikbaar die dagelijks wordt uitgevoerd. Het resterende verlofsaldo wordt verlaagd wanneer de vervaldatum de huidige datum wordt.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Bij het exporteren van persoonlijke contactpersonen voor een werknemer met de entiteit Persoonlijke contactpersoon voor medewerkers worden geen persoonlijke contactpersonen met het relatietype Bovenliggend geëxporteerd (345893)

De gegevensentiteit **Persoonlijke contactpersoon voor medewerker** (**HcmPersonalContactPersonEntity** in DMF en **PersonalContactPerson** in OData) kan geen persoonlijke contactpersonen met het relatietype **Bovenliggend** exporteren. Dit probleem is opgelost voor persoonlijke contactpersonen die na deze wijziging zijn gemaakt. Bestaande persoonlijke contactpersonen van het type **Bovenliggend** worden in een latere release gecorrigeerd.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Redencodes worden in verschillende scenario's weergegeven wanneer ze zijn gemarkeerd als Verlof en verzuim en het gestroomlijnde formulier voor werknemers is ingeschakeld (434163)

Door deze wijziging worden de redencodes beperkt tot alleen verlof- en verzuimcodes wanneer u de gestroomlijnde invoer van werknemers inschakelt.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>In de preview-functie Een verlofplan toewijzen aan werknemers in de toekomst wordt fout (433555) weergegeven

Deze wijziging corrigeert een fout als er aan een verlofplan twee verloftypen zijn toegewezen en u probeert een werknemer toe te wijzen.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Aan de slag-banner wordt weergegeven voor alle gebruikers (441731)

Met deze wijziging wordt de Aan de slag-banner verborgen voor gebruikers die geen systeembeheerder of beheerder voor gegevensbeheer zijn. 

## <a name="the-common-data-service-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>De Common Data Service-entiteit Adres medewerker werkt verschillend wat betreft datum en tijd voor ingangsdatums in Human resources (425071)

Door deze wijziging worden de adresgegevens in bepaalde scenario's uitgelijnd op basis van de datums van het adres.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Kan geen bijlage toevoegen aan een goedgekeurde verlofaanvraag (425407)

Met de release van deze week kunt u bijlagen toevoegen aan goedgekeurde verlofaanvragen zonder de verlofaanvraag te wijzigen.

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

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)
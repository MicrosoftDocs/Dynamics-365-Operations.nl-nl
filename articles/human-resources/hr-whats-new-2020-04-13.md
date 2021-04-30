---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (13 april 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 13 april 2020.
author: andreabichsel
ms.date: 04/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 93873707703ce7148c353735ce1abce795796a5e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892004"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (13 april 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.3136. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="new-production-release-cadence"></a>Nieuwe tempo voor productiereleases

Vanaf de release van deze week wordt het releasetempo voor Human Resources van wekelijks in tweewekelijks gewijzigd. De service-updates in alle regio's volgt nu een implementatie per twee weken om een aanpassing met veilige implementatiemethoden en het bijhouden van hoge standaarden voor stabiliteit en betrouwbaarheid in de service te garanderen. Er worden extra tests en controles uitgevoerd om de implementatie in elke fase van het proces te controleren. Zie [Het updateproces](hr-admin-setup-update-process.md) voor meer informatie over het releasetempo.

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Het veld Afrondingsprecisie kan niet worden bewerkt nadat een Afrondingstype is opgegeven (435616)

Met deze wijziging wordt het veld **Afrondingsprecisie** nu weergegeven nadat u het veld **Afrondingstype** hebt bijgewerkt.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>De einddatum van de verlofinschrijving kan niet worden gewijzigd als de verlofplanning geen toerekeningperioden heeft (413628)

U kunt nu de einddatum voor de inschrijving bewerken zonder de foutmelding "Veld Basis toerekendatum moet worden ingevuld".

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a>Aanstellingsentiteit wordt niet gesynchroniseerd met Dataverse (430834)

Deze wijziging corrigeert het probleem waarbij de aanstellingsgegevens niet worden gesynchroniseerd met Dataverse na het toevoegen van financiële dimensies. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Meerdere bovenliggende entiteiten verwijderen voor entiteit Tijdsinterval werkkalender (431775)

Door deze wijziging worden meerdere bovenliggende entiteiten verwijderd voor de entiteit **Tijdsinterval werkkalender**.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Filter met de CAST-functie werkt niet op de entiteit Medewerkertoewijzing voor positie in de OData-aanroep (431699)

Deze update bevat een wijziging om filter met CAST-functie in OData toe te staan voor de entiteit **Medewerkertoewijzing voor positie**.

## <a name="in-preview"></a>Preview

## <a name="leave-suspension"></a>Verlof opschorten

U kunt verlof en verzuim in Human Resources opschorten voor een werknemer. Als u het verlof opschort, wordt het toegerekende verlof stopgezet voor de geselecteerde verloftypen. Als het opschorten plaatsvindt nadat een toerekening is verwerkt, wordt door het onderbreken van het verlof een evenredige correctie in het verlof van de werknemer gemaakt. Zie [Verlof opschorten](hr-leave-and-absence-suspend-leave.md) voor meer informatie.

## <a name="carry-forward-rules"></a>Regels voor transporteren

U kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt. Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen. Zie [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md) voor meer informatie.

## <a name="known-issues"></a>Bekende problemen

## <a name="employment-details-entity"></a>Entiteit Details dienstverband

De entiteit **Details dienstverband** is bijgewerkt met de volgende velden:

- **Betalingsfrequentie**
- **Aanstellingscategorie-id**
- **Type dienstverband**
- **EmploymentType-id**
- **Status van vergoeding voor aanstelling**

De instellingsgegevens voor deze velden zijn afhankelijk van het vergoedingenbeheer dat is ingeschakeld in het werkgebied **Functiebeheer**. Vul deze velden niet in of werk ze niet bij in de entiteit **Details dienstverband**, omdat deze tijdens het importeren fouten zullen opleveren.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-voorbeeld werkt niet in sommige omgevingen

Als het documentvoorbeeld voor documenten opgeslagen in SharePoint niet werkt, voert u de volgende procedure uit:

1. Controleer voor de gebruikersaccount Beheerder of er een e-mailadres is gekoppeld aan de gebruikersrecord. Deze gegevens worden weergegeven op de pagina **Gebruiker**. Als er geen e-mailadres is ingesteld, moet u het e-mailadres en de provider toevoegen met de Excel-invoegtoepassing OData. Standaard is het e-mailadres niet aanwezig in het Excel-ontwerp. U moet het Excel-ontwerp bewerken, alle velden toevoegen, toepassen en vernieuwen. Wanneer u deze stappen hebt voltooid, kunt u de beheerdersaccount bijwerken.

2. Nadat aan de beheerdersaccount een e-mailaccount is gekoppeld, meldt u zich aan bij Human Resources met beheerdersreferenties.

3. Open een bijlage in SharePoint om de voorbeeldweergave van documenten te starten.

4. Meld u aan met een andere gebruikersaccount die toegang heeft tot bijlagen en controleer of het voorbeeld werkt zoals verwacht.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
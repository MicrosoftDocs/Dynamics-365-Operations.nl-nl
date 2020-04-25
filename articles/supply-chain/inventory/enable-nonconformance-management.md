---
title: Niet-conformiteitsbeheer
description: In dit artikel wordt de algemene configuratie beschreven die nodig is om non-conformiteiten te gebruiken. Als u kwaliteitsorders wilt gebruiken, moet u aanvullende instellingen configureren.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7bb4ffba4332314d1d7ab099232780584e75f9c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212866"
---
# <a name="nonconformance-management"></a>Niet-conformiteitsbeheer

[!include [banner](../includes/banner.md)]

In dit artikel wordt de algemene configuratie beschreven die nodig is om non-conformiteiten te gebruiken. Als u kwaliteitsorders wilt gebruiken, moet u aanvullende instellingen configureren.

Ga als volgt te werk om niet-conformeringsbeheer in te schakelen:

1.  Definieer de parameters voor voorraad- en magazijnbeheer, die betrekking hebben op niet-conformeringen:
    -   Stel de optie **Kwaliteitsbeheer gebruiken** in op **Ja**.
    -   Voer in het veld **Uurtarief** een uurtarief in de lokale valuta in. Het uurtarief wordt gebruikt voor het berekenen van de kosten voor bewerkingen die zijn gerelateerd aan een niet-conformering. Het uurtarief en de berekende kosten vormen referentiegegevens voor een niet-conformering. Ze worden niet samen met andere functies gebruikt.
    -   Gebruik het tabblad **Kwaliteitsbeheer** op de pagina **Rapportinstelling** om het type af te drukken document te definiëren. U kunt een niet-conformiteitsrapport, een niet-conformiteitslabel of een correctierapport afdrukken. U kunt meerdere records definiëren voor het afdrukken van verschillende documenttypen op een rapport of voor het afdrukken van interne en externe notities. Misschien vindt u het handig om op de pagina **Documenttype** een uniek documenttype te definiëren voor niet-conformeringen en een uniek documenttype voor correcties. U kunt bijvoorbeeld opmerkingen over een niet-conformering invoeren met behulp van het unieke documenttype voor niet-conformeringen. Identificeer in dit geval het unieke documenttype in de rapportopties.
    -   Schakel nummerreeksen voor niet-conformerings- en correctieverwijzingen in.

2.  Schakel gebruikersgoedkeuring van niet-conformeringen in. Gebruik het veld **Naam** op de pagina **Gebruikers** om een werknemer toe te wijzen aan elke gebruiker die een niet-conformering moet goedkeuren. Het systeem gebruikt de werknemers die de status van een niet-conformering wijzigen om de niet-conformeringshistorie bij te houden. Gebruikers kunnen een niet-conformering pas goedkeuren als ze een werknemers-ID hebben toegewezen.
3.  Definieer de probleemtypen die worden toegewezen aan niet-conformeringen. Gebruik de pagina **Probleemtypen** om een classificatie te definiëren van de kwaliteitsproblemen die zich voordoen voor de verschillende niet-conformeringstypen. U kunt de volgende niet-conformeringstypen instellen: **Intern**, **Klant**, **Leverancier**, **Serviceaanvraag**, **Productie** en **Productie van coproducten**. Gebruik de pagina **Niet-conformeringstypen** om een probleemtype te autoriseren dat moet worden gebruikt in een of meer niet-conformeringstypen. Een probleemtype voor een defectcode kan bijvoorbeeld van toepassing zijn op alle niet-conformeringstypen, terwijl een probleemtype voor klachten van klanten alleen van toepassing kan zijn op de niet-conformeringstypen **Klant** en **Serviceaanvraag**.
4.  Definieer de quarantainezones om richtlijnen te geven over hoe defect materiaal moet worden verwerkt. Gebruik de pagina **Quarantainezones** om zones te definiëren die kunnen worden toegewezen aan een niet-conformering. In het afgedrukte niet-conformeringslabel worden de toegewezen quarantainezone en informatie over gebruik weergegeven als richtlijn voor het verwerken van defect materiaal. De zones kunnen overeenstemmen met voorraadlocaties of bronnen voor bedrijfsactiviteiten.
5.  Definieer de diagnosetypen die u wilt toewijzen aan correcties. Gebruik de pagina **Diagnosetypen** om een classificatie van diagnostische acties te definiëren. Met een correctie wordt opgegeven welk type diagnostische actie moet worden uitgevoerd voor een goedgekeurde niet-conformering en wie de actie moet uitvoeren. Ook worden de aangevraagde voltooiingsdatum en de geplande voltooiingsdatum opgegeven.
6.  Definieer de gerelateerde bewerkingen die worden toegewezen aan niet-conformeringen. Gebruik de pagina **Bewerkingen** om een classificatie te definiëren voor het werk dat kan worden uitgevoerd voor een goedgekeurde niet-conformering. Wanneer u een gerelateerde bewerking toewijst aan een niet-conformering, kunt u gedetailleerde informatie opgeven, zoals informatie over het bijbehorende materiaal, werkuren en diverse toeslagen die vereist zijn om de bewerking uit te voeren. Deze informatie wordt gebruikt om een raming van de kosten voor de bewerking te berekenen. De gedetailleerde informatie en de kostenraming dienen ter referentie. De gerelateerde bewerkingen voor kwaliteit verschillen van de bewerkingen die kunnen worden gedefinieerd voor een productieroute.


<a name="additional-resources"></a>Aanvullende resources
--------

[Een conformiteit maken en verwerken](tasks/create-process-non-conformance.md)

[Processen voor kwaliteitsbeheer](quality-management-processes.md)

[Vereisten voor niet-conformeringsbeheer instellen](tasks/set-up-prerequisites-nonconformance-management.md)

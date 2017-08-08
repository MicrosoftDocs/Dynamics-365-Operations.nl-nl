---
title: Inkoopcatalogi
description: "Dit artikel beschrijft op een hoog niveau hoe de inkoopprofessional aanschaffingscatalogi kan instellen en onderhouden. Aanschaffingscatalogi definiëren de artikelen en services die werknemers van het bedrijf kunnen gebruiken wanneer ze artikelen en services voor intern gebruik bestellen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b94ecf3e173a2a7ce649170b6eff1e16f2626074
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="procurement-catalogs"></a>Inkoopcatalogi

[!include[banner](../includes/banner.md)]


Dit artikel beschrijft op een hoog niveau hoe de inkoopprofessional aanschaffingscatalogi kan instellen en onderhouden. Aanschaffingscatalogi definiëren de artikelen en services die werknemers van het bedrijf kunnen gebruiken wanneer ze artikelen en services voor intern gebruik bestellen.

Inkoopprofessionals kunnen catalogi van artikelen en services maken en onderhouden die kunnen worden gekocht voor intern gebruik in een organisatie. Nadat catalogi zijn ingesteld, kunnen werknemers opdrachten tot inkoop maken om uit de catalogi te bestellen. De catalogi kunnen worden gebruikt om inkoopbeleid af te dwingen, zodat werknemers alleen de artikelen en services kunnen bestellen die voor hun inkopende rechtspersoon zijn toegestaan. Wanneer u een aanschaffingscatalogus maakt, moet u de volgende taken overwegen:

-   Configureer uw hiërarchie van aanschaffingscategorieën voordat u de catalogus maakt.
-   Bepaal welke producten u wilt dat uw werknemers kunnen bestellen. U kunt specifieke producten in een catalogusknooppunt weergeven of verbergen, of alle producten in een knooppunt weergeven of verbergen.
-   Bepaal hoeveel aanschaffingscatalogi u nodig hebt. Toegang tot een aanschaffingscatalogus wordt bepaald door de beleidsregel voor de catalogus die u voor de rechtspersoon en operationele eenheid definieert waaraan een werknemer is toegewezen.

Verschillende factoren definiëren de producten die werknemers kunnen bestellen en de aanschaffingscategorieën die ze kunnen gebruiken wanneer ze opdrachten tot inkoop maken:

-   De beleidsregel voor categorietoegang in het inkoopbeleid bepaalt welke aanschaffingscategorieën in de opdracht tot inkoop beschikbaar zijn. Als geen regel is ingesteld, zijn alle aanschaffingscategorieën beschikbaar.
-   Werknemers kunnen een product alleen bestellen als het zich in de actieve aanschaffingscatalogus voor uw organisatie bevindt en als het zich in een ingeschakeld knooppunt bevindt en niet is verborgen. Het product moet zich ook bevinden in een categorie waartoe een bepaalde werknemer toegang heeft volgens de beleidsregel voor categorietoegang.
-   De catalogusbeleidsregel vermeldt de catalogus die wordt gebruikt. Als geen catalogusbeleidsregel wordt gedefinieerd, bepaalt de regel voor categorietoegang de producten die een werknemer op de opdracht tot inkoop kan bestellen.

## <a name="prerequisites"></a>Vereisten
De volgende tabel beschrijft de taken die moeten worden uitgevoerd voordat een inkoopprofessional een aanschaffingscatalogus kan maken.

| Opdracht                                                | Rol               | Beschrijving                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Een hiërarchie van aanschaffingscategorieën instellen.            | Inkoopmanager | Hiërarchieën van aanschaffingscategorieën delen artikelen of transactie in voor rapportage en analyse. Met behulp van een hiërarchie van aanschaffingscategorieën kunnen bedrijven categorieën, producten, leveranciers en andere aanschaffingsfactoren beheren vanaf een centrale locatie. Er wordt één hiërarchie van aanschaffingscategorieën bepaald voor ene hele organisatie. De catalogus is gebaseerd op de hiërarchie van aanschaffingscategorieën: de categorieën in de hiërarchie worden knooppunten in de catalogus. De leveranciers en producten zijn opgenomen in uw catalogus. |
| Voeg leveranciers en producten aan aanschaffingscategorieën toe. | Inkoopmanager | Wanneer de hiërarchie van aanschaffingscategorieën voor uw organisatie wordt gemaakt, kan elke aanschaffingscategorie aan specifieke leveranciers, producten, enz. worden gekoppeld. Deze koppelingen worden automatisch naar de catalogus gekopieerd.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Een catalogus instellen
Nadat aan de vereisten is voldaan, kunt u catalogi instellen. U kunt één catalogus maken die door uw hele organisatie wordt gebruikt of meerdere catalogi voor de verschillende afdelingen in uw organisatie. Als u één catalogus voor de hele organisatie maakt, wordt de toegang tot de catalogus bepaald door uw inkoopbeleidsregels.  

De catalogus bepaalt welke producten beschikbaar zijn wanneer de opdrachten tot inkoop worden gemaakt, maar u kunt beleidsregels voor categorietoegang gebruiken om extra beperkingen toe te passen. Omdat de knooppunten in een catalogus aanschaffingscategorieën zijn, kunnen ze door een beleidsregel voor categorietoegang worden onderdrukt. In dat geval zijn de producten in die categorie niet beschikbaar voor werknemers om in opdrachten te gebruiken. U definieert de beleidsregels voor categorietoegang op de pagina **Inkoopbeleid**. De volgende tabel beschrijft de taken die u moet uitvoeren om een catalogus in te stellen.

| Opdracht                                                   | Rol             | Beschrijving                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Een nieuwe catalogus maken.                                  | Inkoper | Wanneer u een catalogus maakt, geeft u een naam en omschrijving voor de catalogus op. U kunt ook opgeven of de catalogus handmatig of automatisch wordt bijgewerkt en de eigenaar van de catalogus opgeven.                                                                                                                                      |
| Bepaal of producten in de catalogus beschikbaar zijn. | Inkoper | Omdat de producten van de aanschaffingscategorieën zijn overgenomen, worden ze allemaal in de juiste catalogusknooppunten weergegeven. U kunt bepalen of alle producten in een knooppunt worden verborgen of weergegeven wanneer de catalogus in een opdracht tot inkoop wordt gebruikt. U kunt ook bepalen of afzonderlijke producten in een knooppunt worden verborgen of weergegeven. |
| Publiceer de catalogus.                                   | Inkoper | Voordat een catalogus in een opdracht tot inkoop kan worden gebruikt, moet u een catalogusbeleidsregel instellen voor de catalogus, moet u de status van de catalogus op **Actief** instellen en moet u de catalogus publiceren. U kunt ook catalogi uitschakelen die u niet meer beschikbaar wilt maken voor uw gebruikers.                                              |

Updates worden automatisch of handmatig gepubliceerd, afhankelijk van de optie die u selecteert voor de catalogus in het veld **Standaard bijwerktype** in de pagina **Catalogi**. De volgende standaard updatetypes zijn beschikbaar voor catalogi:

-   **Dynamisch** – De catalogi worden automatisch bijgewerkt wanneer een wijziging in de catalogus wordt aangebracht.
-   **Statisch** – De catalogi moeten handmatig worden bijgewerkt.
-   **Beide** - als de catalogus productcategorieën bevat met een standaardupdatetype **Statisch** moet deze handmatig worden bijgewerkt wanneer die categorieën worden bijgewerkt. Als de catalogus productcategorieën bevat met een standaardupdatetype **Dynamisch** worden deze automatisch bijgewerkt wanneer een wijziging wordt aangebracht.


<a name="see-also"></a>Zie ook
--------

[Een hiërarchie van aanschaffingscategorieën instellen](/dynamics365/unified-operations/supply-chain/procurement/tasks/set-up-procurement-category-hierarchy) (taakbegeleiding)





---
title: Vaste activa instellen
description: Dit onderwerp bevat een overzicht van de instellingen van de module Vaste activa.
author: twheeloc
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7a578c5198feb8481a77180e3ed95077296f4638
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fixed-assets"></a>Vaste activa instellen

[!include[banner](../includes/banner.md)]


Dit onderwerp bevat een overzicht van de instellingen van de module Vaste activa.

<a name="overview"></a>Overzicht
--------
Parameters bepalen het algemeen gedrag in Vaste activa.

Met vaste-activagroepen kunt u uw activa groeperen en standaardkenmerken voor elk activum opgeven die aan een groep is toegewezen. Er worden boeken toegewezen aan vaste-activagroepen. De boeken volgen de financiële waarde van vaste activa in de loop der tijd met de afschrijvingsconfiguratie die in het afschrijvingsprofiel is gedefinieerd.

Vaste activa worden aan een groep toegewezen wanneer ze worden gemaakt. Standaard worden de boeken die aan de vaste-activagroep zijn toegewezen vervolgens toegewezen aan vaste activa. De boeken die zijn geconfigureerd om naar het grootboek te boeken, worden gekoppeld aan een boekingsprofiel. Grootboekrekeningen worden in het boekingsprofiel gedefinieerd en gebruikt wanneer transacties voor vaste activa worden geboekt. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Afschrijvingsprofielen
Stel eerst afschrijvingsprofielen in. In het afschrijvingsprofiel configureert u hoe de waarde van eem activum in de loop der tijd wordt afgeschreven. U moet de methode van afschrijving, het afschrijvingsjaar (kalenderjaar of fiscaal jaar) en de afschrijvingsfrequentie definiëren. Zie [Afschrijvingsprofielen instellen en maken](tasks/set-up-depreciation-profiles.md) voor meer informatie.

## <a name="books"></a>Boeken
Nadat u afschrijvingsprofielen hebt ingesteld, moet u de vereiste boeken voor uw activa maken. Elk boek volgt de onafhankelijke financiële levensduur van een activum. De boeken kunnen worden geconfigureerd om gekoppelde transacties naar het grootboek te boeken. Deze configuratie is de standaardinstelling, omdat deze gewoonlijk wordt gebruikt voor financiële rapportage in ondernemingen. Boeken die niet naar het grootboek boeken, boeken alleen naar de Vaste activa-subadministratie en worden doorgaans gebruikt voor belastingaangifte.

Een primair afschrijvingsprofiel wordt toegewezen aan elk boek. De boeken hebben ook of een alternatief afschrijvingsprofiel, als dit type profiel van toepassing is. Als u het vaste-activaboek automatisch wilt opnemen in afschrijvingsruns, moet u de optie Afschrijving berekenen inschakelen. Als deze optie niet voor een activum wordt ingeschakeld, slaat het afschrijvingsvoorstel het activum over.

U kunt ook afgeleide boeken instellen. De opgegeven afgeleide transacties worden geboekt als een exacte kopie van de primaire transactie ten opzichte van de afgeleide boeken. Daarom worden afgeleide transacties gewoonlijk ingesteld voor verwervingen en afstotingen, niet voor afschrijvingstransacties.
Zie [Boeken instellen](tasks/set-up-value-models.md) voor meer informatie.

## <a name="fixed-asset-posting-profiles"></a>Boekingsprofielen vaste activa
Nadat u boeken hebt ingesteld, kunt u het boekingsprofiel maken. Het boekingsprofiel moet per boek worden gedefinieerd, maar het kan ook in meer detail worden gedefinieerd. U kunt bijvoorbeeld het boekingsprofiel definiëren voor de combinatie van een boek en een vaste-activagroep of zelfs voor een afzonderlijk vaste-activaboek. Standaard worden de gedefinieerde grootboekrekeningen gebruikt voor uw vaste-activatransacties.

U moet de grootboekrekeningen definiëren die tijdens de afstotingsprocessen worden gebruikt, zowel voor afstotingsverkopen als afstotngsuitvallen. Op het moment van afstoting worden de eerder geboekte vaste-activatransacties omgekeerd uit de oorspronkelijke rekeningen en worden de nettobedragen verplaatst naar de juiste rekening voor winst en verlies voor afstoting van vaste activa. Om te zorgen dat de transacties correct worden omgekeerd, moet u rekeningen instellen voor elk type transactie dat in uw bedrijf wordt gebruikt. De hoofdrekening moet de oorspronkelijke rekening voor dat transactietype op het boekingsprofiel zijn, en de tegenrekening moet de winst- en verliesrekening voor afstoting zijn. De uitzondering vormt de nettoboekwaarde. In dit geval moeten zowel de hoofdrekening als de tegenrekening zijn ingesteld op de winst- en verliesrekening voor afstoting. Zie [Boekingsprofielen voor vaste activa instellen](tasks/set-up-fixed-asset-posting-profiles.md) voor meer informatie.

## <a name="fixed-asset-groups"></a>Groepen vaste activa
Vaste-activagroep is het enige verplichte veld wanneer u een vast activum maakt. De waarde van dit veld bepaalt de standaardwaarde van verschillende informatievelden voor het activum. De boeken worden zo ingesteld dat een standaardboek aan elk activum in een groep wordt toegewezen. U kunt kenmerken voor de boeken instellen die specifiek zijn voor een groep activa, zoals Levensduur en Afschrijvingsconventie.

U kunt ook speciale afschrijvingsaftrek of bonusafschrijvingen definiëren voor een specifieke combinatie van een vaste-activagroep en een boek. U moet een prioriteit toewijzen aan de speciale afschrijvingsaftrek om de volgorde op te geven waarin aftrek wordt berekend als er meerdere aftrekposten aan een boek zijn toegewezen. Zie [Groepen vaste activa instellen](tasks/set-up-fixed-asset-groups.md) voor meer informatie.

## <a name="fixed-asset-parameters"></a>Vaste-activaparameters
De laatste stap is het bijwerken van de vaste-activaparameters.

Het veld **Drempel voor kapitalisatie** bepaalt de activa die zijn afgeschreven. Als een inkoopregel wordt geselecteerd als een vast activum, maar niet voldoet aan de opgegeven kapitalisatiedrempel, wordt het vaste activum wel gemaakt of bijgewerkt, maar wordt de optie Afschrijving berekenen ingesteld op Nee. Daarom wordt het activum niet automatisch afgeschreven als onderdeel van de afschrijvingsvoorstellen.

Een belangrijke optie is **Automatisch bedragen voor afschrijvingscorrecties met afstoting maken**. Als u deze optie op **Ja** instelt, wordt de afschrijving van het actium automatisch aangepast, gebaseerd op de afschrijvingsinstellingen op het moment van afstoting. Met een andere optie kunt u contantkortingen van uw verwervingsbedrag aftrekken wanneer u vaste activa aankoopt met een leveranciersfactuur.

Op het sneltabblad Inkooporders kunt u configureren hoe activa worden gemaakt als onderdeel van het inkoopproces. De eerste optie is Bijboekingen van activa vanuit Inkoop toestaan. Als u deze optie instelt op Ja, vindt activaverwerving plaats wanneer de factuur wordt geboekt. Als u deze optie instelt op Nee, kunt u een vast activum nog wel op een inkooporder en factuur opnemen, maar wordt de verwerving niet geboekt. Het boeken moet als een afzonderlijke stap worden uitgevoerd vanuit het vaste-activajournaal. Met de optie Activum maken tijdens boeken van productontvangstbon of factuur kunt u tijdens het boeken een nieuw activum maken, zodat het niet hoeft te zijn ingesteld als vast activum voor de transactie. De laatste optie Controleren of er vaste activa zijn gemaakt tijdens regelinvoer is alleen van toepassing op opdrachten tot inkoop.

U kunt redencodes zo configureren dat ze vereist zijn voor wijzigingen in een vast activum of voor specifieke vaste-activatransacties.

Tot slot definieert u op het tabblad Nummerreeksen nummerreeksen voor Vaste activa. Nummerreeks van vaste activa kan door Nummerreeks van vaste-activagroep worden genegeerd als deze is opgegeven.

Zie [Vaste activa maken](tasks/create-fixed-asset.md) voor meer informatie.



---
title: Vaste activa instellen
description: Dit onderwerp bevat een overzicht van de instellingen van de module Vaste activa.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c42522f69ecf2eb25d8d9384737115826ff4cda
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978506"
---
# <a name="set-up-fixed-assets"></a>Vaste activa instellen

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een overzicht van de instellingen van de module **Vaste activa**.

## <a name="overview"></a>Overzicht

Parameters bepalen het algemeen gedrag in Vaste activa.

Met vaste-activagroepen kunt u uw activa groeperen en standaardkenmerken voor elk activum opgeven die aan een groep is toegewezen. Er worden boeken toegewezen aan vaste-activagroepen. De boeken volgen de financiële waarde van vaste activa in de loop der tijd met de afschrijvingsconfiguratie die in het afschrijvingsprofiel is gedefinieerd.

Vaste activa worden aan een groep toegewezen wanneer ze worden gemaakt. Standaard worden de boeken die aan de vaste-activagroep zijn toegewezen vervolgens toegewezen aan vaste activa. De boeken die zijn geconfigureerd om naar het grootboek te boeken, worden gekoppeld aan een boekingsprofiel. Grootboekrekeningen worden voor elk boek gedefinieerd in het boekingsprofiel en gebruikt wanneer transacties voor vaste activa worden geboekt.

![Onderdelen van vaste activa](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Afschrijvingsprofielen

U moet eerst afschrijvingsprofielen instellen. In het afschrijvingsprofiel configureert u hoe de waarde van eem activum in de loop der tijd wordt afgeschreven. U moet de methode van afschrijving, het afschrijvingsjaar (kalenderjaar of fiscaal jaar) en de afschrijvingsfrequentie definiëren. Zie [Afschrijvingsprofielen instellen en maken](tasks/set-up-depreciation-profiles.md) voor meer informatie.

## <a name="books"></a>Boeken

Nadat u afschrijvingsprofielen hebt ingesteld, moet u de vereiste boeken voor uw activa maken. Elk boek volgt de onafhankelijke financiële levensduur van een activum. De boeken kunnen worden geconfigureerd om gekoppelde transacties naar het grootboek te boeken. Deze configuratie is de standaardinstelling, omdat deze gewoonlijk wordt gebruikt voor financiële rapportage van de onderneming. Boeken die niet naar het grootboek boeken, boeken alleen naar de Vaste activa-subadministratie en worden doorgaans gebruikt voor belastingrapportage.

Een primair afschrijvingsprofiel wordt toegewezen aan elk boek. De boeken hebben ook of een alternatief afschrijvingsprofiel, als dit type profiel van toepassing is. Als u het vaste-activaboek automatisch wilt opnemen in afschrijvingsruns, moet u de optie **Afschrijving berekenen** inschakelen. Als deze optie niet voor een activum is ingeschakeld, slaat het afschrijvingsvoorstel het activum over.

U kunt ook afgeleide boeken instellen. De opgegeven afgeleide transacties worden geboekt tegen de afgeleide boeken, als een exacte kopie van de primaire transactie. Daarom worden afgeleide transacties gewoonlijk ingesteld voor verwervingen en afstotingen, niet voor afschrijvingstransacties. Zie [Waardemodellen instellen](tasks/set-up-value-models.md) voor meer informatie.

## <a name="fixed-asset-posting-profiles"></a>Boekingsprofielen vaste activa

Nadat u boeken hebt ingesteld, kunt u het boekingsprofiel maken. Het boekingsprofiel moet per boek worden gedefinieerd, maar het kan ook in meer detail worden gedefinieerd. U kunt bijvoorbeeld het boekingsprofiel definiëren voor de combinatie van een boek en een vaste-activagroep of zelfs voor een afzonderlijk vaste-activaboek. Standaard worden de gedefinieerde grootboekrekeningen gebruikt voor uw vaste-activatransacties.

U moet de grootboekrekeningen definiëren die tijdens de afstotingsprocessen worden gebruikt, zowel voor afstotingsverkopen als afstotngsuitvallen. De vaste-activatransacties die eerder zijn geboekt worden op het moment van afboeking teruggeboekt uit de oorspronkelijke accounts. De nettobedragen worden vervolgens verplaatst naar de juiste rekening voor winst en verlies voor activa-afboeking. Om te zorgen dat de transacties correct worden omgekeerd, moet u rekeningen instellen voor elk type transactie dat in uw bedrijf wordt gebruikt. De hoofdrekening moet de oorspronkelijke rekening voor dat transactietype op het boekingsprofiel zijn, en de tegenrekening moet de winst- en verliesrekening voor afstoting zijn. De uitzondering vormt de nettoboekwaarde. In dit geval moeten zowel de hoofdrekening als de tegenrekening zijn ingesteld op de winst- en verliesrekening voor afstoting. Zie [Boekingsprofielen voor vaste activa instellen](tasks/set-up-fixed-asset-posting-profiles.md) voor meer informatie.

## <a name="fixed-asset-groups"></a>Groepen vaste activa

Het veld **Vaste-activagroep** is het enige verplichte veld wanneer u een vast activum maakt. De waarde van dit veld bepaalt de standaardwaarde van verschillende informatievelden voor het activum. De boeken worden zo ingesteld dat een standaardboek aan elk activum in een groep wordt toegewezen. Op deze manier kunnen de kenmerken die u voor de boeken instelt, specifiek zijn voor een groep activa. Deze kenmerken omvatten de levensduur en de afschrijvingsconventie.

U kunt ook speciale afschrijvingsaftrek of bonusafschrijvingen definiëren voor een specifieke combinatie van een vaste-activagroep en een boek. U moet een prioriteit toewijzen aan de speciale afschrijvingsaftrek om de volgorde op te geven waarin aftrek wordt berekend als er meerdere aftrekposten aan een boek zijn toegewezen. Zie [Groepen vaste activa instellen](tasks/set-up-fixed-asset-groups.md) voor meer informatie.

## <a name="journal-names"></a>Journaalnamen

Op de pagina **Journaalnamen** moet u de journaalnamen maken die moeten worden gebruikt met het vaste-activajournaal. U moet het veld **Journaaltype** instellen op **Vaste activa boeken**. Stel het veld **Boekstuknummering** zo in dat de journaalnamen worden gebruikt voor het vaste-activajournaal. Vaste activa-journalen moeten de instelling **Maximaal één boekstuknummer** niet gebruiken, omdat een uniek boekstuknummer vereist is voor verschillende geautomatiseerde processen, zoals overboekingen en splitsingen.

## <a name="fixed-asset-parameters"></a>Vaste-activaparameters

De laatste stap is het bijwerken van de vaste-activaparameters.

Het veld **Drempel voor kapitalisatie** bepaalt de activa die zijn afgeschreven. Als een inkoopregel wordt geselecteerd als een vast activum, maar niet voldoet aan de opgegeven kapitalisatiedrempel, wordt het vaste activum wel gemaakt of bijgewerkt, maar wordt de optie **Afschrijving berekenen** ingesteld op **Nee**. Daarom wordt het activum niet automatisch afgeschreven als onderdeel van de afschrijvingsvoorstellen.

Eén belangrijke optie heet **Automatisch bedragen voor afschrijvingscorrecties met afstoting maken**. Als u deze optie op **Ja** instelt, wordt de afschrijving van het activum automatisch aangepast, gebaseerd op de afschrijvingsinstellingen op het moment van afstoting. Met een andere optie kunt u contantkortingen van het verwervingsbedrag aftrekken wanneer u vaste activa aankoopt met een leveranciersfactuur.

Op het sneltabblad **Inkooporders** kunt u configureren hoe activa worden gemaakt als onderdeel van het inkoopproces. De eerste optie heet **Bijboekingen van activa vanuit Inkoop toestaan**. Als u deze optie instelt op **Ja**, vindt activaverwerving plaats wanneer de factuur wordt geboekt. Als u deze optie instelt op **Nee**, kunt nog een vast activum wel op een inkooporder en factuur opnemen, maar wordt de verwerving niet geboekt. Het boeken moet als een afzonderlijke stap worden uitgevoerd vanuit het vaste-activajournaal. Met de optie **Activum maken tijdens boeken van productontvangstbon of factuur** kunt u 'al doende' een nieuw activum maken tijdens het boeken. Daarom hoeft het activum niet te worden ingesteld als een vast activum vóór de transactie. De laatste optie **Controleren of er vaste activa zijn gemaakt tijdens regelinvoer** is alleen van toepassing op opdrachten tot inkoop.

U kunt redencodes zo configureren dat ze vereist zijn voor wijzigingen in een vast activum of voor specifieke vaste-activatransacties.

Tot slot definieert u op het tabblad **Nummerreeksen** nummerreeksen voor vaste activa. De nummerreeks van het **Vaste activum** kan worden overschreven door de nummerreeks van de **Vaste-activagroep** als deze is opgegeven.

Zie [Vaste activa maken](tasks/create-fixed-asset.md) voor meer informatie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
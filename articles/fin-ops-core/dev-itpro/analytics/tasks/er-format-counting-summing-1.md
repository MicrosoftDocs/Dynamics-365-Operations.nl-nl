---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 1: Indeling maken)'
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage configureert voor tellen en totaliseren op basis van de gegevens van de reeds gegenereerde tekstuitvoer. (Deel 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a3639b5ac28f8a571642e983906d658dabf05b1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093017"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>ER Indeling configureren voor tellen en totaliseren (deel 1: Indeling maken)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Toegang krijgen tot de lijst met configuraties die door Microsoft zijn geleverd
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Zorg ervoor dat de leverancier "Litware, Inc." beschikbaar is en als actief gemarkeerd.  
2. Selecteer "Litware, Inc." .
3. Klik op Opslagplaatsen.
    * Als een opslagplaats van het type Bron voor bedrijfsactiviteiten bestaat, slaat u de resterende stappen van de huidige deeltaak over.  
4. Klik op Toevoegen om het dialoogvenster te openen.
5. Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.
6. Klik op Opslagplaats maken.
7. Klik op OK.

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Intrastat-configuraties ophalen die door Microsoft worden geleverd
1. Klik op Openen.
2. Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.
3. Klik op Importeren.
    * Klik op Importeren voor versie 1.1 van de geselecteerde configuratie.  
4. Klik op Ja.
5. Sluit de pagina.
6. Sluit de pagina.
7. Klik op Rapportconfiguraties.
8. Vouw in de structuur 'Intrastat-model' uit.
9. Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.


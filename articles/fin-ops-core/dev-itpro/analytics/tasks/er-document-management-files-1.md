---
title: 'ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 1: Gegevensmodel voorbereiden)'
description: In dit artikel wordt beschreven hoe u een indeling voor elektronische rapportage (ER) configureert om documentbeheerbestanden (bijlagen) te gebruiken in ER-uitvoer. (Deel 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7818b4916de7f3afbead0da39aa471f690d8f5e7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908379"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 1: Gegevensmodel voorbereiden)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Toegang krijgen tot de lijst met configuraties die door Microsoft zijn geleverd
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.

    Zorg ervoor dat de leverancier 'Litware, Inc.' beschikbaar is en als actief gemarkeerd.  

2. Selecteer 'Litware, Inc.' .
3. Klik op Opslagplaatsen.

    Als een opslagplaats van het type Bron voor bedrijfsactiviteiten bestaat, slaat u de resterende stappen van de huidige deeltaak over.  

4. Klik op Toevoegen om het dialoogvenster te openen.
5. Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.
6. Klik op Opslagplaats maken.
7. Klik op OK.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Haal de Klantfactuurmodelconfiguraties op die door Microsoft zijn verstrekt
1. Klik op Filters weergeven.
2. Pas de volgende filters toe: voer een filterwaarde 'Bron voor bedrijfsactiviteiten' in in het veld Naam met de filteroperator 'begint met'. Voer een filterwaarde van "" in in het veld Omschrijving met de filteroperator 'begint met'.
3. Klik op Filters weergeven.
4. Klik op Openen.
5. Selecteer in de structuur Klantfactuurmodel.

    Selecteer de modelconfiguratie Klantfactuurmodel om deze te importeren.  

6. Klik op Importeren.

    Klik op Importeren voor versie 1 van de geselecteerde configuratie.  

7. Klik op Ja.
8. Sluit de pagina.
9. Sluit de pagina.
10. Klik op Rapportconfiguraties.
11. Selecteer in de structuur Klantfactuurmodel.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Maak het afgeleide model om toegang tot de Documentbeheerbestanden te ondersteunen.
U moet een eigen configuratie van het Klantfactuurmodel maken door deze af te leiden van de configuratie die door Microsoft is aangeleverd. Gebruik deze configuratie om de toegang tot de Documentbeheerbestanden te implementeren en ze beschikbaar te maken voor elektronische documenten die u op basis van dit model wilt maken.  
1. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
2. Typ in het veld Nieuw 'Afleiden van naam: Klantfactuurmodel, Microsoft'.
3. Typ 'Klantfactuurmodel (aangepast)' in het veld Naam.
4. Klik op Configuratie maken.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
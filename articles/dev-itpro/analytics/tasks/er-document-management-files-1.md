--- 
title: Een gegevensmodel voorbereiden voor het gebruik van documentbeheerbestanden in uitvoer van indelingen
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f99259056fab2d56d1ccf7487681c183551c64f
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs"></a>Een gegevensmodel voorbereiden voor het gebruik van documentbeheerbestanden in uitvoer van indelingen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.

Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Toegang krijgen tot de lijst met configuraties die door Microsoft zijn geleverd
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Zorg ervoor dat de leverancier 'Litware, Inc.' beschikbaar is en als actief gemarkeerd.  
2. Selecteer 'Litware, Inc.' .
3. Klik op Opslagplaatsen.
    * Als een opslagplaats van het type Bron voor bedrijfsactiviteiten bestaat, slaat u de resterende stappen van de huidige deeltaak over.  
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
    * Selecteer de modelconfiguratie Klantfactuurmodel om deze te importeren.  
6. Klik op Importeren.
    * Klik op Importeren voor versie 1 van de geselecteerde configuratie.  
7. Klik op Ja.
8. Sluit de pagina.
9. Sluit de pagina.
10. Klik op Rapportconfiguraties.
11. Selecteer in de structuur Klantfactuurmodel.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Maak het afgeleide model om toegang tot de Documentbeheerbestanden te ondersteunen.
    * U moet een eigen configuratie van het Klantfactuurmodel maken door deze af te leiden van de configuratie die door Microsoft is aangeleverd. Gebruik deze configuratie om de toegang tot de Documentbeheerbestanden te implementeren en ze beschikbaar te maken voor elektronische documenten die u op basis van dit model wilt maken.  
1. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
2. Typ in het veld Nieuw 'Afleiden van naam: Klantfactuurmodel, Microsoft'.
3. Typ 'Klantfactuurmodel (aangepast)' in het veld Naam.
    * Klantfactuurmodel (aangepast)  
4. Klik op Configuratie maken.



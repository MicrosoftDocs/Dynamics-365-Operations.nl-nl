---
title: Afdrukken van nummerplaatlabel inschakelen
description: Met deze procedure schakelt u het automatisch afdrukken van een SSCC-label (Serial Shipping Container Code) in nadat het laatste artikel is verzameld van de voorraad in het werkproces orderverzamelen voor verkoop.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d906ca9f5a6536870fa0c322a0792ed5672c25e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558098"
---
# <a name="enable-license-plate-label-printing"></a>Afdrukken van nummerplaatlabel inschakelen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Met deze procedure schakelt u het automatisch afdrukken van een SSCC-label (Serial Shipping Container Code) in nadat het laatste artikel is verzameld van de voorraad in het werkproces orderverzamelen voor verkoop. U kunt deze procedure in het bedrijf USMF van de demogegevens uitvoeren. Als u het met behulp van uw eigen gegevens uitvoert, moet u een ingestelde nummerreeks voor nummerplaten hebben. U moet een labelprinter instellen voordat u deze taak start. Ga naar Organisatiebeheer > Instellingen > Netwerkprinters. Klik in het actievenster op Opties en vervolgens op de knop Installatieprogramma van documentrouteringsagent downloaden. Voer het installatieprogramma uit en zorg ervoor dat een netwerkprinter Actief is voordat u met de procedure vervolgt.


## <a name="set-up-the-gs1-company-prefix"></a>Het GS1-bedrijfsvoorvoegsel instellen
1. Ga naar Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer.
2. Geef in het veld GS1-bedrijfsvoorvoegsel het 7-cijferige GS1-bedrijfsnummer op.
3. Klik op Opslaan.
4. Sluit de pagina.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>De nummerreeks voor het SSCC-nummerplaatnummer instellen
1. Ga naar Organisatiebeheer > Nummerreeksen > Nummerreeksen.
2. Selecteer een optie in het veld Gebied.
3. Selecteer een optie in het veld Verwijzing.
4. Typ een waarde in het veld Bedrijf.
5. Markeer in de lijst de geselecteerde rij.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Vouw de sectie Segmenten uit.
8. Klik op Bewerken.
9. Selecteer in de tabel Segmenten de eerste rij
10. Klik op Verwijderen.
11. Klik op Verwijderen.
12. Klik op Opslaan.
13. Sluit de pagina.

## <a name="create-the-document-route-layout"></a>De documentrouteringsindeling maken
1. Ga naar Magazijnbeheer > Instellingen > Documentroutering > Routeringsindelingen voor documenten.
    * Schakel de SSCC-indeling in.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Indelings-id.
4. Typ een waarde in het veld Omschrijving.
5. Zoek en selecteer de gewenste record in de lijst.
6. Klik op Invoegen aan het einde van de tekst.
7. Klik op Opslaan.
8. Sluit de pagina.

## <a name="set-up-the-document-routing"></a>De documentroutering instellen
1. Ga naar Magazijnbeheer > Instellingen > Documentroutering > Documentroutering.
2. Selecteer een optie in het veld Werkordertype.
3. Klik op Nieuw.
4. Typ een waarde in het veld Magazijn.
5. Typ een waarde in het veld Naam.
6. Klik op Nieuw.
7. Typ of selecteer een waarde in het veld Indelings-id.
8. Voer in het veld Naam de naam in van de printer die u wilt gebruiken.
9. Klik op Opslaan.
10. Sluit de pagina.

## <a name="create-mobile-device-menu"></a>Menu voor mobiel apparaat maken
1. Ga naar Magazijnbeheer > Instellingen > Mobiel apparaat > Menuopties voor mobiel apparaat.
2. Klik op Nieuw.
3. Typ een waarde in het veld Menuoptie.
4. Typ een waarde in het veld Titel.
5. Selecteer een optie in het veld Modus.
6. Selecteer Ja in het veld Bestaand werk gebruiken.
7. Selecteer Ja in het veld Nummerplaat maken.
8. Vouw de werkklassensectie uit.
9. Klik op Nieuw.
10. Typ een waarde in het veld Werkklasse-id.
11. Klik op Opslaan.
12. Sluit de pagina.
13. Ga naar Magazijnbeheer > Instellingen > Mobiel apparaat > Menu voor mobiel apparaat.
14. Zoek en selecteer de gewenste record in de lijst.
15. Selecteer in de structuur ´Selecteer in de structuur de menuoptie die u eerder hebt gemaakt.´.
16. Klik op Bewerken.
17. Klik op de pijl om de menuoptie aan het menu toe te voegen.
18. Klik op Opslaan.
19. Sluit de pagina.

## <a name="update-a-work-template"></a>Een werksjabloon bijwerken
1. Ga naar Magazijnbeheer > Instellingen > Werk > Werksjablonen.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik op Bewerken.
4. Klik op Nieuw.
5. Markeer in de lijst de geselecteerde rij.
6. Selecteer Afdrukken in het veld Werktype.
7. Typ of selecteer een waarde in het veld Werkklasse-id.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik op Omhoog.
10. Klik op Opslaan.
11. Sluit de pagina.


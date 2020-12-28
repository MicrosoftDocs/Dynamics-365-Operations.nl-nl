---
title: Afdrukken van nummerplaatlabel inschakelen
description: In dit onderwerp wordt beschreven hoe u het automatisch afdrukken van een SSCC-label (Serial Shipping Container Code) inschakelt nadat het laatste artikel is verzameld van de voorraad in het werkproces orderverzamelen voor verkoop.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e548e5e5528733412d47478dd740b87217cdac2
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425800"
---
# <a name="enable-license-plate-label-printing"></a>Afdrukken van nummerplaatlabel inschakelen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u het automatisch afdrukken van een SSCC-label (Serial Shipping Container Code) inschakelt nadat het laatste artikel is verzameld van de voorraad in het werkproces orderverzamelen voor verkoop. U kunt deze procedure in het bedrijf USMF van de demogegevens uitvoeren. Als u het met behulp van uw eigen gegevens uitvoert, moet u een ingestelde nummerreeks voor nummerplaten hebben. U moet een labelprinter instellen voordat u deze taak start. Ga naar Organisatiebeheer > Instellingen > Netwerkprinters. Klik in het actievenster op Opties en vervolgens op de knop Installatieprogramma van documentrouteringsagent downloaden. Voer het installatieprogramma uit en zorg ervoor dat een netwerkprinter Actief is voordat u met de procedure vervolgt.


## <a name="set-up-the-gs1-company-prefix"></a>Het GS1-bedrijfsvoorvoegsel instellen
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer**.
2. Geef in het veld **GS1-bedrijfsvoorvoegsel** het 7-cijferige GS1-bedrijfsnummer op.
3. Selecteer **Opslaan**.
4. Sluit de pagina.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>De nummerreeks voor het SSCC-nummerplaatnummer instellen
1. Ga naar **Navigatiedeelvenster > Modules > Organisatiebeheer > Nummerreeksen > Nummerreeksen**.
2. Selecteer een optie in het veld **Gebied**.
3. Selecteer een optie in het veld **Verwijzing**.
4. Typ een waarde in het veld **Bedrijf**.
5. Vouw de sectie **Segmenten** uit.
6. Selecteer **Bewerken**.
7. Selecteer in de tabel **Segmenten** de eerste rij
8. Selecteer **Verwijderen**.
9. Selecteer **Verwijderen**.
10. Selecteer **Opslaan**.
11. Sluit de pagina.

## <a name="create-the-document-route-layout"></a>De documentrouteringsindeling maken
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Documentroutering > Routeringsindelingen voor documenten**. Schakel de SSCC-indeling in.  
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Indelings-id**.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer **Invoegen aan einde van tekst**.
6. Selecteer **Opslaan**.
7. Sluit de pagina.

## <a name="set-up-the-document-routing"></a>De documentroutering instellen
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Documentroutering > Documentroutering**.
2. Selecteer een optie in het veld **Werkordertype**.
3. Selecteer **Nieuw**.
4. Typ een waarde in het veld **Magazijn**.
5. Typ een waarde in het veld **Naam**.
6. Selecteer **Nieuw**.
7. Typ of selecteer een waarde in het veld **Indelings-id**.
8. Voer in het veld **Naam** de naam in van de printer die u wilt gebruiken.
9. Selecteer **Opslaan**.
10. Sluit de pagina.

## <a name="create-mobile-device-menu"></a>Menu voor mobiel apparaat maken
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Mobiel apparaat > Menuopties voor mobiel apparaat**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Menuoptie**.
4. Typ een waarde in het veld **Titel**.
5. Selecteer een optie in het veld **Modus**.
6. Selecteer **Ja** in het veld **Bestaand werk gebruiken**.
7. Selecteer **Ja** in het veld **Nummerplaat maken**.
8. Vouw de sectie **Werkklassensectie** uit.
9. Selecteer **Nieuw**.
10. Typ een waarde in het veld **Werkklasse-id**.
11. Selecteer **Opslaan**.
12. Sluit de pagina.
13. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Mobiel apparaat > Menu voor mobiel apparaat**.
14. Selecteer in de structuur de menuoptie die u eerder hebt gemaakt.
15. Selecteer **Bewerken**.
16. Selecteer de pijl om de menuoptie aan het menu toe te voegen.
17. Selecteer **Opslaan**.
18. Sluit de pagina.

## <a name="update-a-work-template"></a>Een werksjabloon bijwerken
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Werk >Werksjablonen**.
2. Selecteer **Bewerken**.
3. Selecteer **Nieuw**.
4. Selecteer **Afdrukken** in het veld **Werktype**.
5. Typ of selecteer een waarde in het veld **Werkklasse-id**.
6. Selecteer **Omhoog verplaatsen**.
7. Selecteer **Opslaan**.
8. Sluit de pagina.


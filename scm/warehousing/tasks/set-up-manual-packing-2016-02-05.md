--- 
title: Handmatig verpakken instellen (uitsluitend februari en mei 2016)
description: In het verpakkingsproces kunt u producten valideren en verpakken in containers.
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c8cec376bcc8c50fb9a78bed039505608cd7782d
ms.contentlocale: nl-nl
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a>Handmatig verpakken instellen (uitsluitend februari en mei 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In het verpakkingsproces kunt u producten valideren en verpakken in containers. In dit proces verzamelen magazijnmedewerkers producten van de opslaglocaties en verplaatsen deze naar een inpakstation waar ze de typen en hoeveelheden van artikelen controleren en deze aan de juiste containers toewijzen. Wanneer een container volledig is verpakt, kunnen ze de container sluiten en verplaatsen naar de outbound docks. De producten zijn dan gereed om te verzenden. Bij deze procedure wordt het demobedrijf USMF gebruikt. Deze procedure is uitsluitend bedoeld voor de versies van februari 2016 en mei 2016 van Dynamics 365 for Operations.


## <a name="set-up-location-profiles"></a>Locatieprofielen instellen
1. Ga naar Magazijnbeheer > Instellingen > Magazijn > Locatieprofielen.
2. Klik op Nieuw.
    * Het locatieprofiel wordt gebruikt voor inpakstations en bevat informatie en regels voor een locatie.  
3. Typ een waarde in het veld Locatieprofiel-id.
4. Typ een waarde in het veld Naam.
5. Typ of selecteer een waarde in het veld Locatie-indeling.
6. Typ of selecteer een waarde in het veld Locatietype.
7. Selecteer Ja in het veld Gemengde artikelen toestaan.
8. Selecteer Ja in het veld Gemengde voorraadstatussen toestaan.
9. Selecteer Ja in het veld Regel voor batchdagen overschrijven.
10. Sluit de pagina.

## <a name="set-up-warehouse-management-parameters"></a>Parameters voor magazijnbeheer instellen 
1. Ga naar Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer.
2. Klik op het tabblad Verpakking.
3. Typ of selecteer een waarde in het veld Profiel-ID voor verpakkingslocatie.
    * Selecteer het locatieprofiel dat u voor verpakking wilt gebruiken.  
4. Sluit de pagina.

## <a name="set-up-container-types"></a>Containertypen instellen
1. Ga naar Magazijnbeheer > Instellingen > Containers > Containertypen.
2. Klik op Nieuw.
    * U kunt de typen containers definiëren die u wilt gebruiken. U kunt de fysieke afmetingen van de container opgeven, waaronder tarragewicht, maximumgewicht, maximumvolume, lengte, breedte en gewicht.  De kenmerken zijn aangepaste velden waarmee u extra afmetingen voor het containertype kunt toevoegen.     
3. Typ een waarde in het veld Containertype.
4. Typ een waarde in het veld Omschrijving.
5. Voer een getal in het veld Tarragewicht in.
6. Voer in het veld Maximumgewicht een getal in.
7. Voer een getal in het veld Volume in.
8. Voer een getal in het veld Lengte in.
9. Voer een getal in het veld Breedte in.
10. Voer een getal in het veld Hoogte in.
11. Klik op Opslaan.
12. Sluit de pagina.

## <a name="set-up-packing-profiles"></a>Verpakkingsprofielen instellen
1. Ga naar Magazijnbeheer > Instellingen > Verpakking > Verpakkingsprofielen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Verpakkingsprofiel-ID.
4. Typ een waarde in het veld Omschrijving.
5. Typ of selecteer een waarde in het veld Afsluitingsprofiel-ID van container.
    * Een afsluitingsprofiel-ID voor containers is optioneel en is het standaardafsluitingsprofiel voor containers voor dit verpakkingsprofiel.  
6. Selecteer een optie in het veld Modus container-ID.
    * Met deze optie wordt bepaald of een container-ID automatisch wordt gegenereerd wanneer een container wordt gemaakt of dat een container-ID handmatig wordt gemaakt.  
7. Typ of selecteer een waarde in het veld Containertype.
    * Het containertype wordt standaard worden gebruikt wanneer een nieuwe container wordt gemaakt.  
8. Schakel het selectievakje Automatisch container maken bij sluiten van container in.
9. Klik op Opslaan.
10. Sluit de pagina.

## <a name="set-up-container-closing-profiles"></a>Containerafsluitingsprofielen instellen
1. Ga naar Magazijnbeheer > Instellingen > Containers > Afsluitingsprofielen van container.
    * Met containerafsluitingsprofielen wordt bepaald wat er gebeurt wanneer een container wordt gesloten. U kunt meerdere afsluitingsprofielen voor containers instellen.       
2. Klik op Nieuw.
3. Typ een waarde in het veld Afsluitingsprofiel-ID van container.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer een optie in het veld Manifesteren op.
    * Geef op of manifesteren wordt gebruikt bij het afsluiten van containers of bij het bevestigen van de zending. Voor manifesteren is Transportbeheer vereist. Manifesteren moet in de transportengines worden geïmplementeerd. Anders werken ze niet.  
6. Typ of selecteer een waarde in het veld Magazijn.
7. Typ of selecteer een waarde in het veld Standaard locatie voor uiteindelijke verzending.
    * Dit is de locatie waarnaar producten worden verplaatst nadat de containers zijn gesloten. Voor deze locatie moet een locatieprofiel zijn gedefinieerd in de magazijnparameters.  
8. Typ of selecteer een waarde in het veld Gewichtseenheid.
9. Klik op Opslaan.


---
title: Fiscale integratie voor detailhandelafzetkanaal
description: Dit onderwerp biedt een overzicht van de fiscale integratie voor Retail POS.
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: nl-nl
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Fiscale integratie voor detailhandelafzetkanaal

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt een overzicht gegeven van de functionaliteit voor fiscale integratie die beschikbaar is in Microsoft Dynamics 365 for Retail. De functionaliteit voor fiscale integratie is een raamwerk ter ondersteuning van fiscale wetgeving die erop gericht is om fraude in de detailhandel te voorkomen. Typische scenario's die kunnen worden gedekt door fiscale integratie omvatten:

- Een fiscaal ontvangstbewijs afdrukken en geven aan de klant.
- De indiening beveiligen van informatie die gerelateerd is aan verkopen en retouren die worden uitgevoerd op het POS, bij een externe service die wordt geboden door de belastingdienst.
- Gegevensbeveiliging gebruiken met een digitale handtekening die door de belastingdienst is geautoriseerd.

Dit onderwerp bevat richtlijnen voor het instellen van fiscale integratie, zodat gebruikers de volgende taken kunnen uitvoeren. 

- Fiscale connectors configureren. Dit zijn fiscale apparaten of services die worden gebruikt voor fiscale registratiedoeleinden zoals opslaan, digitale handtekeningen en beveiligde indiening van belastinggegevens.
- De documentprovider configureren, die een uitvoermethode en een algoritme voor het genereren van fiscale documenten definieert.
- Het fiscale registratieproces configureren, dat een sequentie van stappen definieert en een groep connectors die in elke stap worden gebruikt.
- Fiscale registratieprocessen toewijzen aan POS-functionaliteitsprofielen.
- Connectortechnische profielen toewijzen aan hardwareprofielen (voor de locale fiscale connectors) of aan POS-functionaliteitsprofielen (voor andere fiscale connectortypen).

## <a name="fiscal-integration-execution-flow"></a>Uitvoeringsstroom voor fiscale integratie
In het volgende scenario ziet u de gemeenschappelijke uitvoeringsstroom voor fiscale integratie.

1. Initialisatie van het fiscale registratieproces.
  
   Na het uitvoeren van sommige acties waar fiscale registratie vereist is, bijvoorbeeld nadat een detailhandelstransactie is uitgevoerd, wordt het fiscale registratieproces gekoppeld aan het huidige POS-functionaliteitsprofiel.

1. Zoeken naar een fiscale connector.
   
   Voor elke fiscale registratiestap die is opgenomen in het fiscale registratieproces, zoekt het systeem overeenkomst met de lijst met fiscale connectors. Deze connectors hebben een functioneel profiel dat is opgenomen in de opgegeven connectorgroep, met een lijst connectors die een technisch profiel hebben gekoppeld aan het huidige hardwareprofiel (alleen voor een connectortype dat gelijk is aan **Lokaal**) of aan het huidige POS-functionaliteitsprofiel (voor andere connectortypen).
   
1. De fiscale integratie uitvoeren.

   Het systeem voert alle benodigde acties uit die worden gedefinieerd door een assembly die is gekoppeld aan de gevonden connector. Dit wordt gedaan overeenkomstig de instellingen van het functionele profiel en het technische profiel die in de vorige stap voor deze connector zijn gevonden.

## <a name="setup-needed-before-using-fiscal-integration"></a>Instelling die nodig is vóór gebruik van fiscale integratie
Voordat u de functionaliteit voor fiscale integratie gebruikt, moet u de volgende instellingen definiëren:

- Definieer de getalreeks op de pagina **Detailhandelparameters** voor het nummer van het fiscale functionele profiel.
  
- Definieer de getalreeksen op de pagina **Gedeelde parameters detailhandel** voor de volgende referenties:
  
  - Nummer van fiscaal technisch profiel
  - Nummer fiscale connectorgroep
  - Nummer van registratieproces

- Maak een **fiscale connector** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Fiscale verbindingen** voor elk apparaat of elke service die u wilt gebruiken voor fiscale integratie.

-  Maak een **Fiscale documentprovider** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Fiscale documentproviders** voor alle fiscale connectors. Toewijzing van gegevens wordt beschouwd als onderdeel van de fiscale documentprovider. Als u andere toewijzingen van gegevens voor de dezelfde connector wilt instellen (zoals staatspecifieke regelgeving), moet u verschillende fiscale documentproviders maken.

- Maak een **functioneel connectorprofiel** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Functionele connectorprofielen** voor elke fiscale documentprovider.
  - Selecteer een connectornaam.
  - Selecteer een documentprovider.
  - Geef btw-tarieven op het tabblad **Instelling service** op.
  - Geef de toewijzing van btw-codes en de toewijzing van betalingsmethoden op het tabblad **Toewijzing van gegevens** op.

  #### <a name="examples"></a>Voorbeelden 

  |  | Opmaak | Voorbeeld | 
  |--------|--------|--------|
  | Btw-tariefinstellingen | waarde : VATrate | 1 : 2000, 2 : 1800 |
  | Toewijzing van btw-codes | VATcode : waarde | vat20 : 1, vat18 : 2 |
  | Toewijzing van betalingsmethoden | TenderTyp: waarde | Contant : 1, Kaart : 2 |

- Maak **fiscale connectorgroepen** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Fiscale connectorgroep**. Een connectorgroep is een subset van functionele profielen die zijn gekoppeld aan fiscale connectors die identieke functies uitvoeren en worden gebruikt in dezelfde fase binnen een fiscaal registratieproces.

   - Voeg functionele profielen toe aan de connectorgroep. Klik op **Toevoegen** op de pagina **Functionele profielen** en selecteer een profielnummer.
   - Als u gebruik van het functionele profiel wilt onderbreken, stelt u **Uitschakelen** in op **Ja**. 
   
     Deze wijziging is alleen van invloed op de huidige connectorgroep. U kunt doorgaan met hetzelfde functionele profiel in andere connectorgroepen.

     >[!NOTE]
     > Binnen een connectorgroep kan elke fiscale connector slechts één functioneel profiel hebben.

- Maak een **technisch connectorprofiel** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Technische connectorprofielen** voor elke fiscale connector.
  - Selecteer een connectornaam.
  - Selecteer een connectortype: 
      - **Lokaal**: stel dit type in voor fysieke apparaten of toepassingen die zijn geïnstalleerd op een lokale computer.
      - **Intern**: stel dit type in voor fiscale apparaten en services die zijn verbonden met Retail Server.
      - **Extern**: voor externe fiscale services, zoals een webportal dat wordt verschaft door een belastingdienst.
    
  - Geef instellingen op het tabblad **Verbinding** op.

      
 >[!NOTE]
 > Een bijgewerkte versie van een configuratie die eerder is geladen, wordt geladen voor zowel functionele als technische profielen. Als een juiste connector of documentprovider al in gebruik is, wordt u geïnformeerd. Standaard worden alle wijzigingen die handmatig zijn aangebracht in de functionele en technische profielen, opgeslagen. Als u deze profielen wilt overschrijven met de standaardset parameters uit een configuratie, klikt u op **Bijwerken** op de pagina **Functionele connectorprofielen** en de pagina **Technische connectorprofielen**.
 
- Maak een **fiscaal registratieproces** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Fiscaal registratieproces** voor elk uniek proces van de fiscale integratie. Een registratieproces wordt gedefinieerd door de volgorde van de registratiestappen en de connectorgroep die in elke stap worden gebruikt. 
  
  - Voeg registratiestappen aan het proces toe:
      - Klik op **Toevoegen**.
      - Selecteer een connectortype.
      
      >[!NOTE]
      > Dit veld bepaalt waar wordt gezocht in een technisch profiel voor de connector: in hardwareprofielen voor connectortype **Lokaal** of in POS-functionaliteitsprofielen voor andere fiscale connectortypen.
      
   - Selecteer een connectorgroep.
   
     >[!NOTE]
     > Klik op **Valideren** om de integriteit van de structuur van het registratieproces te controleren. U wordt aangeraden validaties uit te voeren in de volgende gevallen:
       >- Voor een nieuw registratieproces nadat alle de instellingen zijn voltooid, met inbegrip van binding met POS-functionaliteitsprofielen en hardwareprofielen.
       >- Na het aanbrengen van updates in een bestaand registratieproces.

-  Verbind fiscale registratieprocessen met POS-functionaliteitsprofielen in **Detailhandel > Afzetkanaalinstellingen > POS-instellingen > POS-profielen > Functionaliteitsprofielen**.
   - Klik op **Bewerken** en selecteer een **Procesnummer** op het tabblad **Fiscaal registratieproces**.
- Verbind de technische connectorprofielen met de hardwareprofielen in **Detailhandel > Afzetkanaalinstellingen > POS-instellingen > POS-profielen > Hardwareprofielen**.
   - Klik op **bewerken** en klik vervolgens op **Nieuw** op het tabblad **Fiscaal technisch profiel**.
   - Selecteer een technisch connectorprofiel in het veld **Profielnummer**.
   
     >[!NOTE]
     > U kunt verschillende technische profielen toevoegen aan een hardwareprofiel. Dit wordt echter niet ondersteund als een hardwareprofiel meer dan één snijpunt met een connectorgroep heeft. Als u onjuiste instellingen wilt voorkomen, is het raadzaam dat u het registratieproces valideert na het bijwerken van alle hardwareprofielen.


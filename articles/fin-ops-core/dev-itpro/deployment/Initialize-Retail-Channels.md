---
title: Commerce Scale Unit initialiseren (cloud)
description: In dit artikel wordt uitgelegd hoe u Commerce Scale Unit (cloud) initialiseert in Microsoft Dynamics 365 Commerce.
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 25ca054df6422370b1e61dff7965189ad90d7fcc
ms.sourcegitcommit: 7bcaf00a3ae7e7794d55356085e46f65a6109176
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/26/2022
ms.locfileid: "9357627"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Commerce Scale Unit initialiseren (cloud)

[!include[banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u Commerce Scale Unit (cloud) initialiseert in Microsoft Dynamics 365 Commerce.

Als u een Tier-2-productieomgeving gebruikt of een productieomgeving met toepassing versie 8.1.2.x of hoger, moet u Commerce Scale Unit (cloud) initialiseren voordat u de functionaliteit voor detailhandelkanalen kunt gebruiken voor POS-bewerkingen (Point of Sale) of voor e-commercebewerkingen die Retail Server in de cloud gebruiken. Bij de initialisatie wordt een Commerce Scale Unit (cloud) geïmplementeerd.

> [!IMPORTANT]
> Voor bestaande klanten die de functionaliteit voor detailhandelkanalen in de cloud gebruiken, vereisen we met het oog op continue en onderbroken ondersteuning van uw bedrijf dat u uw detailhandelkanalen bijwerkt om Commerce Scale Unit te kunnen gebruiken. Nieuwe omgevingen die zonder Commerce Scale Unit zijn geïmplementeerd, ontvangen geen kwaliteits- en service-updates meer voor onderdelen van detailhandelkanalen in de cloud. Er is geen actie vereist voor klanten die Commerce Scale Unit (zelfgehost) exclusief gebruiken. Neem contact op met uw Microsoft FastTrack-oplossingsarchitect als u een uitbreiding nodig hebt.

## <a name="prerequisites"></a>Vereisten

1. Implementeer een Tier-2-sandbox- of productieomgeving met versie 8.1.2.x of hoger.
2. U kunt maximaal twee Commerce Scale Units per omgeving zelf implementeren. Als u meer dan twee Commerce Scale Units per omgeving nodig hebt, maakt u in Microsoft Dynamics Lifecycle Services (LCS) een ondersteuningsaanvraag en voert u **Aanvraag voor extra Commerce Scale Unit** in en geeft u de omgevings-id, het aantal Commerce Scale Units en de gewenste datacentrumregio's aan. Aan de aanvraag wordt binnen vijf werkdagen gevolg gegeven. Als u niet meer dan 2 Commerce Scale Units per omgeving nodig hebt, hoeft u geen ondersteuningsaanvraag te maken. 
3. U moet over machtigingen voor projecteigenaar in Lifecycle Services beschikken voordat u Commerce Scale Unit kunt initialiseren.
4. Zorg ervoor dat configuratiesleutels voor detailhandellicenties zijn ingeschakeld in uw omgeving. Zie voor meer informatie [Rapport Licentiecodes en configuratiesleutels](../sysadmin/license-codes-configuration-keys-report.md). U moet de volgende sleutels hebben ingeschakeld om Commerce Scale Unit te kunnen gebruiken.

    - RetailBasic
    - RetaileCommerce: als u van plan bent E-commerce voor Dynamics 365 Commerce te gebruiken.
    - RetailGiftCard: als u van plan bent om geschenkbonnen te gebruiken.
    - RetailInvent: als u van plan bent om voorraad te gebruiken.
    - RetailModernPos: als u van plan bent om POS (Point of Sale) te gebruiken.
    - RetailReplenishment: als u van plan bent om voorraadaanvullingen te gebruiken.
    - RetailScheduler
    - RetailStores: als u van plan bent om POS te gebruiken.


## <a name="region-availability"></a>Regiobeschikbaarheid
Commerce Scale Unit is beschikbaar voor implementatie in de volgende regio's.

| Globale locatie | Regio              | Beschikbaarheid        | Opmerkingen                  |
|-----------------|---------------------|---------------------|---------------------------|
| AMERIKA        | VS - oost             | Algemeen beschikbaar |  Geen opmerkingen.                         |
| AMERIKA        | VS - oost 2           | Algemeen beschikbaar |  Geen opmerkingen.                          |
| AMERIKA        | Noord-centraal VS    | Beperkte capaciteit    |  Geen opmerkingen.                            |
| AMERIKA        | Zuid-centraal VS    | Beperkte capaciteit    |  Geen opmerkingen.                            |
| AMERIKA        | VS - midden          | Algemeen beschikbaar |  Geen opmerkingen.                            |
| AMERIKA        | VS - west             | Algemeen beschikbaar |  Geen opmerkingen.                            |
| AMERIKA        | US - west 2           | Algemeen beschikbaar |  Geen opmerkingen.                            |
| AMERIKA        | Canada - centraal      | Beperkte capaciteit    |  Geen opmerkingen.                            |
| AMERIKA        | Canada - oost         | Beperkte capaciteit    |   Geen opmerkingen.                           |
| AMERIKA        | VS - west-centraal     | Beperkte capaciteit    |   Geen opmerkingen.                           |
| APAC            | Australië - oost      | Algemeen beschikbaar |   Geen opmerkingen.                           |
| APAC            | Zuidoost-Azië      | Beperkte capaciteit | Implementaties zijn niet toegestaan.    |
| APAC            | Japan - oost          | Algemeen beschikbaar |  Geen opmerkingen.                            |
| APAC            | Japan - west          | Algemeen beschikbaar |   Geen opmerkingen.                           |
| APAC            | Australië - zuidoost | Algemeen beschikbaar |   Geen opmerkingen.                           |
| APAC            | Oost-Azië           | Beperkte capaciteit    |   Geen opmerkingen.                           |
| APAC            | India - zuid         | Beperkte capaciteit | Implementaties zijn niet toegestaan.    |
| APAC            | India - centraal       | Beperkte capaciteit    | Vereist goedkeuringsproces. |
| EMEA            | West-Europa         | Algemeen beschikbaar    |  Geen opmerkingen. |
| EMEA            | Noord-Europa        | Algemeen beschikbaar    |  Geen opmerkingen. |
| EMEA            | VK -zuid            | Algemeen beschikbaar |    Geen opmerkingen.                          |
| EMEA            | VK - west             | Algemeen beschikbaar |    Geen opmerkingen.                          |
| Zwitserland     | Zwitserland - noord   | Beperkte capaciteit    | Vereist goedkeuringsproces. |
| VAE             | VAE - noord           | Beperkte capaciteit    | Vereist goedkeuringsproces. |

De implementatiecapaciteit in regio's met beperkte capaciteit is bijzonder beperkt. Aanvragen voor implementatie worden per geval in aanmerking genomen. Als u een dringende zakelijke behoefte hebt voor implementatie in regio's met beperkte capaciteit kunt u een ondersteuningsaanvraag indienen om aan de wachtlijst te worden toegevoegd. In gebieden met een beperkte capaciteit is op dit moment de implementatie van Commerce Scale Unit niet toegestaan. 

![Kaart met beschikbaarheid van regio's](media/Commerce-Scale-Unit-Region-Availability.png "Kaart met beschikbaarheid van regio's")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Commerce Scale Unit initialiseren als onderdeel van een implementatie van een nieuwe omgeving

Controleer of het hoofdkantoor beschikbaar is. Dit is nodig om de schaaleenheid bij het hoofdkantoor te registreren tijdens het initialisatieproces. Het is niet raadzaam om een schaaleenheid te initialiseren wanneer onderhoud op het hoofdkantoor wordt uitgevoerd, omdat het dan mogelijk tijdens het onderhoudsproces niet beschikbaar wordt.

1. Zorg ervoor dat de hoofdkantooromgeving beschikbaar is en niet in de [Onderhoudsmodus](../sysadmin/maintenance-mode.md) staat.
2. In LCS selecteert u **Omgevingsfuncties \> Commerce** op de pagina met omgevingsdetails.
3. Selecteer **Initialiseren** op de implementatiepagina van Commerce-instellingen.
4. Selecteer de versie van de Commerce Scale Unit die u wilt initialiseren.
5. Selecteer een regio waarin u Commerce Scale Unit wilt initialiseren.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Kanalen configureren om Commerce Scale Unit te gebruiken

Nadat Commerce Scale Unit is geïmplementeerd, moet u ervoor zorgen dat uw kanalen zijn geconfigureerd om de database ervoor te gebruiken. 

Voer de volgende stappen uit om uw kanalen te configureren voor het gebruik van de Commerce Scale Unit-database.

1. Ga in Commerce Headquarters naar **Retail en commerce \> Instelling van hoofdkantoor \> Commerce-planner \> Kanaaldatabase**.
1. Selecteer een kanaaldatabase in het linkerdeelvenster.
1. Selecteer **Toevoegen** op het sneltabblad **Detailhandelkanaal** en selecteer vervolgens uw detailhandelkanaal in de vervolgkeuzelijst.
1. Selecteer **Toevoegen** en selecteer vervolgens uw online kanaal in de vervolgkeuzelijst. 

Ga als u klaar bent naar **Retail en commerce \> Retail en commerce IT \> Distributieplanning** en voer taak 9999 uit.

> [!NOTE] 
> Met Taak 9999 worden alle nieuwe producten en klanten gesynchroniseerd met de Commerce Scale Unit. Dit proces kan even duren. Als het kanaal alleen beschikbaar moet zijn voor de configuratie van E-Commerce Site Builder, kunt u taak 1070 uitvoeren in plaats van taak 9999.

### <a name="database-refresh-and-commerce-scale-units"></a>Databasevernieuwing en Commerce Scale Units

Voordat u begint, moet u kennis hebben gemaakt met [Stappen die moeten worden voltooid na het vernieuwen van de database voor omgevingen waarin Commerce-functionaliteit wordt gebruikt](../database/database-refresh.md).

De kanaaldatabaserecords van de schaaleenheid (in het formulier Kanaaldatabase) kunnen niet tussen omgevingen worden verplaatst als onderdeel van de databasevernieuwing. Dit komt omdat de records omgevingsspecifieke configuratie vertegenwoordigen.

Nadat de database is vernieuwd, kunt u de kanaaldatabaserecord van de schaaleenheid opnieuw genereren door de schaaleenheid in LCS opnieuw te implementeren. Met elke implementatie- of onderhoudsbewerking in de schaaleenheid wordt geprobeerd de schaaleenheid bij het hoofdkantoor te registreren als de registratie als ontbrekend is gedetecteerd.

U kunt de schaaleenheid opnieuw implementeren zonder onderdelen te wijzigen door dezelfde versie te selecteren als die uw schaaleenheid al heeft. Dit kan in LCS door de volgende stappen uit te voeren:

1. Selecteer in LCS **Omgevingsfuncties \> Retail** op de pagina met omgevingsdetails.
2. Selecteer op de implementatiepagina de schaaleenheid die u opnieuw wilt implementeren.
3. Selecteer **Bijwerken** in het bewerkingsmenu van de schaaleenheid.
4. Selecteer de optie **Een versie opgeven** op de schuifregelaar in de vervolgkeuzelijst **Versie selecteren**.
5. Typ in het tekstvak onder **Een versie opgeven** de versie die voor uw schaaleenheid wordt weergegeven naast het label **Huidige versie**.
6. Klik op de knop **Bijwerken**.

U hoeft **Uitbreidingen bijwerken** niet te selecteren, zelfs niet als u uitbreidingen eerder hebt toegepast, omdat het laatste uitbreidingspakket dat op de schaaleenheid is toegepast, automatisch wordt geselecteerd bij het bijwerken van een schaaleenheid.

Als u meerdere schaaleenheden hebt, moet u de bovenstaande bewerking uitvoeren voor elke schaaleenheid. U kunt deze bewerkingen desgewenst naast elkaar uitvoeren.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Extra Commerce Scale Units implementeren (optioneel)

Nadat u Commerce Scale Unit hebt geïnitialiseerd, kunt u zelf een tweede schaaleenheid implementeren als uw licentie dat toestaat. Als u meer dan twee schaaleenheden wilt implementeren, moet u een ondersteuningsaanvraag maken. Vermeld in de ondersteuningsaanvraag het aantal Commerce Scale Unit dat u nodig hebt, de omgevingsnaam en de gewenste regio's. Zie [Dynamics 365-licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) voor meer informatie over licenties. 

Voor elke extra Commerce Scale Unit die u implementeert, raden we u aan om een afzonderlijke kanaaldatabasegroep te maken door de volgende stappen uit te voeren.

1. Ga in Commerce Headquarters naar **Retail en commerce > Retail Headquarters > Detailhandelplanner > Kanaaldatabasegroep**.
2. Maak een nieuwe afzetkanaaldatabasegroep.
3. Ga naar **Retail en commerce > Retail Headquarters > Detailhandelplanner > Kanaaldatabase** en selecteer de kanaaldatabase die overeenkomt met de nieuw gemaakte Commerce Scale Unit.
4. Selecteer **Bewerken** en selecteer de nieuwe kanaaldatabasegroep.
5. Selecteer **Opslaan**.
6. Selecteer **Volledige gegevenssynchronisatie uitvoeren** voor de geselecteerde kanaaldatabase.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Extra overwegingen als u onderdelen voor in de cloud gehoste Commerce-kanalen in een bestaande omgeving initialiseert

Als u al onderdelen van in de cloud gehoste Commerce-kanalen gebruikt in een omgeving, helpt de initialisatie van Commerce Scale Unit de downtime te verlagen wanneer deze onderdelen worden bijgewerkt. Er is extra planning vereist vóór de initialisatie van Commerce Scale Unit.

Wanneer u uw eerste Commerce Scale Unit initialiseert in een omgeving waarin onderdelen van in de cloud gehoste Commerce-kanalen worden gebruikt, migreert het initialisatieproces uw kanalen die aan de onderdelen van in de cloud gehoste kanalen zijn gekoppeld, aan de eerste schaaleenheid Kanalen die aan winkelschaaleenheden zijn gekoppeld, worden niet beïnvloed.

Het migratieproces is transparant voor de kanalen. Nadat de initialisatie van de schaaleenheid is gestart, worden de volgende bewerkingen automatisch uitgevoerd:

1. Er wordt een nieuwe Commerce Scale Unit gemaakt en aan de omgeving gekoppeld.
2. De Commerce Scale Unit wordt geregistreerd als een beschikbare kanaaldatabase in het hoofdkantoor.
3. Alle kanalen die zijn toegewezen aan de **Standaard** kanaaldatabase in het hoofdkantoor, worden bijgewerkt voor toewijzing aan de nieuwe Commerce Scale Unit.
4. Een volledige gegevenssynchronisatie van Commerce Data Exchange (CDX) wordt uitgevoerd om de kanaalgegevens naar de nieuwe schaaleenheid te brengen.

**Plannen en testen voor initialisatie van Commerce Scale Unit**: als algemene regel moet u bij de initialisatie van Commerce Scale Unit een downtime van vijf uur plannen voor winkelbewerkingen, evenals E-commerce-kanaalbewerkingen waarin Retail Server of CPOS (Cloud Point of Sale) wordt gebruikt.

1. Voer een databasevernieuwing van uw productieomgeving naar een UAT-sandboxomgeving uit. 
2. Initialiseer Commerce Scale Unit in de UAT-sandboxomgeving. 
3. Let op de initialisatietijd die moet worden voltooid voor Commerce Scale Unit. Dit is vergelijkbaar met de tijd die deze bewerking in uw productieomgeving kost, waarbij winkelbewerkingen en E-commerce-bewerkingen niet beschikbaar zijn.

U moet de volgende extra stappen uitvoeren voordat u Commerce Scale Unit initialiseert.

- **Alle POS-ploegen sluiten**: na de migratie kunnen POS-gebruikers geen ploegen sluiten die actief waren tijdens het migratieproces.
- **Controleren of alle P-taken met succes zijn voltooid**: het wordt aanbevolen dat P-taken om transacties in behandeling te synchroniseren, zijn voltooid voordat CSU wordt geïnitialiseerd.
- **Afmelden bij alle POS-apparaten**: POS-bewerkingen worden niet ondersteund tijdens de migratie.
- **Alle uitgestelde transacties op POS terugroepen en ongeldig maken**: uitgestelde transacties worden niet behouden als onderdeel van de initialisatie.

> [!IMPORTANT]
> Als onderdeel van de initialisatie van Commerce Scale Unit gaan eerder uitgestelde transacties verloren en kunnen ze niet worden teruggeroepen. 

Dit gebeurt er tijdens de initialisatieperiode:

- In de cloud gehoste Commerce-kanalen werken niet, tenzij u de mogelijkheid POS offline inschakelt.
- Van POS-apparaten waarop offline capaciteit is ingeschakeld, is de functionaliteit minder.
- Alle e-commerce-clients die afhankelijk zijn van Retail Server worden verstoord.
- Dit heeft geen invloed op kanalen die worden gehost op Commerce Scale Unit (zelfgehost).
- De functionaliteit van het hoofdkantoor wordt niet beïnvloed.

Dit gebeurt er nadat de initialisatie is voltooid:

- De status van de apparaatactivering van alle geactiveerde POS-apparaten blijft behouden, wat betekent dat de apparaten dan niet opnieuw hoeven te worden geactiveerd.
- Exemplaren van zelfstandige hardwarestations blijven werken.
- Rapporten aan POS-kanaalzijde worden opnieuw ingesteld en bevatten geen gegevens van vóór de initialisatie.
- De bewerking Journaal weergeven wordt ook opnieuw ingesteld en bevat geen gegevens van vóór de initialisatie.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

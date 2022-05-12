---
title: Fiscale integratie voor Commerce-kanalen instellen
description: Dit onderwerp bevat richtlijnen voor het instellen van de functionaliteit voor fiscale integratie voor Commerce-kanalen.
author: EvgenyPopovMBS
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 51a75ce03b0ae6b744ec56df35bd3fdb1f40cf3a
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661744"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Fiscale integratie voor Commerce-kanalen instellen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dit onderwerp bevat richtlijnen voor het instellen van de functionaliteit voor fiscale integratie voor Commerce-kanalen. Zie voor meer informatie over de fiscale integratie [Overzicht van fiscale integratie voor Commerce-kanalen](fiscal-integration-for-retail-channel.md).

## <a name="enable-features-in-commerce-headquarters"></a>Functies inschakelen in Commerce Headquarters

Volg deze stappen om functies in te schakelen die zijn gerelateerd aan de functionaliteit voor fiscale integratie voor Commerce-kanalen.

1. Ga in Commerce Headquarters naar **Systeembeheer \> Werkgebieden \> Functiebeheer**.
1. Zoek de volgende functies en schakel deze in:

    - **Directe fiscale integratie vanuit POS-kassa's**: Deze functie breidt het raamwerk voor fiscale integratie uit door de mogelijkheid toe te voegen om fiscale connectors te maken die worden uitgevoerd in het POS (Point of Sale). Dit type connector communiceert met een fiscaal randapparaat of fiscale service dat of die een HTTP-API (Application Programming Interface) levert en vereist niet een specifieke fysieke machine in de winkel. Met deze functionaliteit is fiscale integratie voor mobiele apparaten bijvoorbeeld mogelijk zonder dat er een gedeeld hardwarestation nodig is.
    - **Overschrijvingen technische profielen fiscale integratie**: Met deze functie kunt u de configuratie van fiscale integratie uitbreiden en kunt u de verbindingsparameters controleren op de instellingenpagina van een POS-kassa. Wanneer deze functie is ingeschakeld, kunt u de parameters van een technisch profiel overschrijven.
    - **Fiscale registratiestatus van POS-kassa's**: wanneer deze functie is ingeschakeld, kunt u het proces voor fiscale registratie voor specifieke POS-kassa's uitschakelen. Als de fiscale registratie voor een POS-kassa is uitgeschakeld, kunnen er op die kassa geen verkooptransacties worden uitgevoerd.
    - **Back-up lokale opslag voor fiscale integratie**: Deze functie breidt de mogelijkheden uit voor verwerking van fouten van het fiscale-integratieraamwerk. Hiermee wordt ook automatische back-up van fiscale-registratiegegevens ingeschakeld bij gegevensverlies, zodat de gegevens in de lokale opslag kunnen worden hersteld terwijl een apparaat wordt geactiveerd.

## <a name="set-up-commerce-parameters"></a>Commerce-parameters instellen

Voer de onderstaande stappen uit om Commerce-parameters in te stellen.

1. Stel op de pagina **Gedeelde Commerce-parameters** op het tabblad **Algemeen** de optie **Fiscale integratie inschakelen** in op **Ja**.
1. Definieer op het tabblad **Nummerreeksen** de nummerreeksen voor de volgende referenties:

    - Nummer van fiscaal technisch profiel
    - Nummer fiscale connectorgroep
    - Nummer van registratieproces

1. Definieer op de pagina **Commerce-parameters** de nummerreeks voor het fiscale profielnummer.

> [!NOTE]
> Nummerreeksen zijn optioneel. Nummers voor alle fiscale integratie-entiteiten kunnen worden gegenereerd uit nummerreeksen of handmatig.

## <a name="set-up-a-fiscal-registration-process"></a>Een fiscaal registratieproces instellen

Het instelproces van de fiscale integratie bevat de volgende taken:

- Fiscale connectors configureren die fiscale apparaten of services vertegenwoordigen die worden gebruikt voor fiscale registratiedoeleinden, zoals fiscale printers.
- Documentproviders configureren die fiscale documenten genereren die worden geregistreerd in fiscale apparaten of services door fiscale connectors.
- Het fiscale registratieproces configureren dat een reeks fiscale registratiestappen definieert en de fiscale connectors en fiscale documentproviders die voor elke stap worden gebruikt.
- Wijs het fiscale registratieproces aan POS-functionaliteitsprofielen toe.
- Technische connectorprofielen toewijzen aan hardwareprofielen.
- Wijs technische connectorprofielen toe aan POS-hardware of functionaliteitsprofielen.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Configuraties van fiscale documentproviders uploaden

Een fiscale documentprovider is verantwoordelijk voor het genereren van belastingdocumenten die staan voor transacties en gebeurtenissen die zijn geregistreerd in het POS in een indeling die ook wordt gebruikt voor de interactie met een fiscaal apparaat of een fiscale service. Een fiscale documentprovider kan bijvoorbeeld een voorstelling van een fiscaal ontvangstbewijs genereren in een XML-indeling.

Voer de volgende stappen uit om configuraties van fiscale documentproviders te uploaden.

1. Ga in Commerce Headquarters naar de pagina **Fiscale documentproviders** (**Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale documentproviders**).
1. Upload een XML-configuratie voor elk apparaat of elke service die u wilt gebruiken.

> [!TIP]
> Door **Weergeven** te selecteren kunt u alle functionele profielen weergeven die gerelateerd zijn aan de huidige fiscale documentprovider.

> [!NOTE]
> Toewijzing van gegevens wordt beschouwd als onderdeel van een fiscale documentprovider. Als u andere toewijzingen van gegevens voor dezelfde connector wilt instellen (bijvoorbeeld staatspecifieke regelgeving), moet u verschillende fiscale documentproviders maken.

### <a name="upload-configurations-of-fiscal-connectors"></a>Configuraties van fiscale connectors uploaden

Een fiscale connector is verantwoordelijk voor de communicatie met een fiscaal apparaat of een fiscale service. Een fiscale connector kan bijvoorbeeld een ontvangstbewijs dat een fiscale documentprovider in een XML-indeling heeft gemaakt, verzenden naar een fiscale printer. Zie voor meer informatie over fiscale integratieonderdelen [Fiscaal registratieproces en fiscale integratievoorbeelden voor fiscale apparaten en -services](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Voer de volgende stappen uit om configuraties van fiscale connectors te uploaden.

1. Ga in Commerce Headquarters naar de pagina **Fiscale connectors** (**Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectors**).
1. Upload een XML-configuratie voor elk apparaat of elke service die u wilt gebruiken met het oog op fiscale integratie.

> [!TIP]
> Door **Weergeven** te selecteren kunt u alle functionele en technische profielen weergeven die gerelateerd zijn aan de huidige fiscale connector.

Voor voorbeelden van configuraties van fiscale connectors en fiscale documentproviders kunt u [Fiscale integratievoorbeelden in de Commerce-SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk) bekijken.

### <a name="create-connector-functional-profiles"></a>Functionele connectorprofielen maken

Voer de volgende stappen uit om functionele connectorprofielen te maken.

1. Ga in Commerce Headquarters naar de pagina **Functionele connectorprofielen** (**Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Functionele connectorprofielen**).
1. Maak voor elke combinatie van een fiscale connector en een fiscale documentprovider die is gerelateerd aan deze fiscale connector, een functioneel connectorprofiel door de volgende stappen uit te voeren:

    1. Selecteer een connectornaam.
    1. Selecteer een documentprovider.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Gegevenstoewijzingsparameters in een functioneel connectorprofiel wijzigen

U kunt de gegevenstoewijzingsparameters in een functioneel connectorprofiel wijzigen. In de volgende tabel vindt u enkele voorbeelden van gegevenstoewijzingsparameters in een functioneel connectorprofiel.

| Parameter | Format | Voorbeeld |
|-----------|--------|---------|
| Btw-tariefinstellingen | waarde : VATrate | 1 : 2000, 2 : 1800 |
| Toewijzing van btw-codes | VATcode : waarde | vat20 : 1, vat18 : 2 |
| Toewijzing van betalingsmethoden | TenderType : waarde | Contant : 1, Kaart : 2 |

Als u de standaardparameters wilt herstellen die zijn gedefinieerd in de configuratie van de fiscale documentprovider, selecteert u **Bijwerken** op de pagina **Functionele connectorprofielen**.

> [!NOTE]
> Functionele connectorprofielen zijn specifiek voor het bedrijf. Als u van plan bent dezelfde combinatie van een fiscale connector en een fiscale documentprovider te gebruiken voor verschillende bedrijven, maakt u een functioneel connectorprofiel voor elk bedrijf.

### <a name="create-connector-technical-profiles"></a>Technische connectorprofielen maken

Voer de volgende stappen uit om technische connectorprofielen te maken.

1. Ga in Commerce Headquarters naar de pagina **Technische connectorprofielen** (**Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Technische connectorprofielen**).
1. Maak een technisch connectorprofiel voor elke fiscale connector door de volgende stappen uit te voeren:

    1. Selecteer een connectornaam.
    1. Selecteer een connectortype:

        - Selecteer **Lokaal** voor apparaten of services die zijn verbonden met een hardwarestation of die aanwezig zijn in het lokale netwerk.
        - Selecteer **Extern** voor externe services.
        - Selecteer **Intern** voor interne connectors in de Commerce runtime (CRT). 

    1. Selecteer een connectorlocatie:

        - Selecteer **Hardwarestation** als de connector zich op het hardwarestation bevindt.
        - Selecteer **Kassa** als de connector zich in de POS-kassa bevindt.

Parameters op de tabbladen **Apparaat** en **Instellingen** in een technisch connectorprofiel kunnen worden gewijzigd. Als u de standaardparameters wilt herstellen die zijn gedefinieerd in de configuratie van de fiscale connector, selecteert u **Bijwerken**. Wanneer een nieuwe versie van een XML-configuratie wordt geladen, ontvangt u een bericht dat de huidige fiscale connector of fiscale documentprovider al wordt gebruikt. Deze procedure overschrijft niet handmatige wijzigingen die eerder zijn aangebracht in functionele connectorprofielen en technische connectorprofielen. Als u de standaardset parameters wilt toepassen vanuit een nieuwe configuratie, selecteert u **Bijwerken** op de pagina **Functionele connectorprofielen** of de pagina **Technische connectorprofielen**.

Als u specifieke parameters moet instellen voor een afzonderlijke POS-kassa of winkel, voert u de volgende stappen uit.

1. Selecteer de menuopdracht **Overschrijven**.
1. Maak een nieuwe record op de pagina **Overschrijven**.
1. Selecteer een winkel of een POS-kassa. U kunt parameters van het geselecteerde technische profiel overschrijven voor een afzonderlijke POS-kassa of voor alle POS-kassa's in een afzonderlijke winkel.
1. Voer op het tabblad **Apparaat** parameters in voor de geselecteerde POS-kassa of winkel.

### <a name="create-fiscal-connector-groups"></a>Fiscale connectorgroepen maken

Een fiscale connectorgroep combineert een subset van functionele connectors die identieke functies uitvoeren en worden gebruikt in dezelfde stap van een fiscaal registratieproces. Als bijvoorbeeld verschillende fiscale printermodellen kunnen worden gebruikt in een winkel, kunnen fiscale connectors voor die fiscale printers worden gecombineerd in een fiscale connectorgroep.

Voer de volgende stappen uit om een fiscale connectorgroep te maken.

1. Ga naar de pagina **Fiscale connectorgroep** (**Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectorgroepen**).
1. Maak een nieuwe fiscale connectorgroep.
1. Voeg functionele profielen toe aan de connectorgroep. Selecteer op het tabblad **Functionele profielen** **Toevoegen** en selecteer een profielnummer. Elke fiscale connector in een connectorgroep kan slechts één functioneel profiel hebben.
1. Als u het gebruik van het functionele profiel wilt onderbreken, stelt u de optie **Uitschakelen** in op **Ja**. Deze wijziging is alleen van invloed op de huidige connectorgroep. U kunt doorgaan met hetzelfde functionele profiel te gebruiken in andere connectorgroepen.

### <a name="create-a-fiscal-registration-process"></a>Een fiscaal registratieproces maken

Een fiscaal registratieproces wordt gedefinieerd door de volgorde van registratiestappen en de connectorgroep die voor elke stap wordt gebruikt.

Voer de volgende stappen uit om een fiscaal integratieproces te maken.

1. Ga in Commerce Headquarters naar de pagina **Fiscaal registratieproces** (**Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscaal registratieproces**).
1. Een nieuwe record maken voor elk uniek fiscaal registratieproces.
1. Voer de volgende stappen uit om registratiestappen aan het proces toe te voegen:

    1. Selecteer **Toevoegen**.
    1. Selecteer een fiscaal connectortype.
    1. Selecteer in het veld **Groepsnummer** een geschikte fiscale connectorgroep.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Entiteiten van het fiscale registratieproces aan POS-profielen toevoegen

Voer de volgende stappen uit om entiteiten van het fiscale registratieproces aan POS-profielen toe te voegen.

1. Ga in Commerce Headquarters naar de pagina **POS-functionaliteitsprofielen** (**Retail en commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**). 
1. Wijs het fiscale registratieproces aan een POS-functionaliteitsprofiel toe.
1. Selecteer **Bewerken** en selecteer vervolgens op het tabblad **Fiscaal registratieproces** in het veld **Procesnummer** een proces.
1. Selecteer op het tabblad **Fiscale services** de technische connectorprofielen met de connectorlocatie **Register**.
1. Ga naar de pagina **POS-hardwareprofiel** (**Retail en commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Hardwareprofielen**).
1. Wijs technische connectorprofielen aan een hardwareprofiel toe. 
1. Selecteer **Bewerken** en voeg vervolgens een regel toe op het tabblad **Fiscale randapparatuur**. 
1. Selecteer een technisch connectorprofiel in het veld **Profielnummer**.
1. Selecteer op het tabblad **Fiscale randapparatuur** de technische connectorprofielen met de connectorlocatie **Hardwarestation**.

> [!NOTE]
> U kunt verschillende technische profielen toevoegen aan hetzelfde hardwareprofiel. Een hardwareprofiel of POS-functionaliteitsprofiel moet achter slechts één intersectie met een fiscale connectorgroep hebben.

De fiscale registratiestroom wordt gedefinieerd door het fiscale registratieproces en ook door sommige parameters van fiscale integratieonderdelen: de CRT-extensie voor de fiscale documentprovider en de extensie hardwarestation voor de fiscale connector.

- Het abonnement van gebeurtenissen en transacties op fiscale registratie wordt vooraf gedefinieerd in de fiscale documentprovider.
- De fiscale documentprovider is ook verantwoordelijk voor het identificeren van de fiscale connector die wordt gebruikt voor fiscale registratie. Het komt overeen met de functionele connectorprofielen die zijn opgenomen in de fiscale connectorgroep die is opgegeven voor de huidige stap van het fiscale registratieproces met het technische connectorprofiel dat is toegewezen aan het hardwareprofiel van het Hardware-station waaraan het POS is gekoppeld.
- De fiscale documentprovider gebruikt de instellingen voor gegevenstoewijzing van de configuratie van de fiscale documentprovider om transactie-/gebeurtenisgegevens, zoals belasting en betalingen, te transformeren terwijl een fiscaal document wordt gemaakt.
- Wanneer de fiscale documentprovider een fiscaal document genereert, kan de fiscale connector het zoals het is verzenden naar het fiscale apparaat of het parseren en transformeren tot een reeks opdrachten van de apparaat-API, afhankelijk van hoe de communicatie wordt verwerkt.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Kassa's met fiscale registratiebeperkingen instellen

U kunt kassa's selecteren waarbij fiscale registratie is verboden, bijvoorbeeld wanneer u alleen niet-fiscale bewerkingen hoeft op te geven zoals zoeken naar productcatalogi, zoeken naar klanten of het maken van concepttransacties.

Voer deze stappen uit om kassa's met fiscale registratiebeperkingen in te stellen.

1. Ga in Commerce headquarters naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Fiscale registratieprocessen**.
1. Selecteer het vereiste proces.
1. Selecteer het tabblad **POS-kassa's met beperkingen van het belastingproces**.
1. Voeg kassa's met beperkingen van het belastingproces toe, indien nodig.

### <a name="validate-the-fiscal-registration-process"></a>Het fiscale registratieproces valideren

Het wordt aangeraden het fiscale registratieproces in de volgende gevallen te valideren:

- U hebt alle instellingen voor een nieuw registratieproces voltooid. Deze instellingen omvatten toewijzing van registratieprocessen aan POS-functionaliteitsprofielen en hardwareprofielen.
- U hebt wijzigingen aangebracht in een bestaand fiscaal registratieproces en deze wijzigingen kunnen ertoe leiden dat een andere fiscale connector wordt geselecteerd tijdens runtime. (U hebt bijvoorbeeld de connectorgroep voor een stap in een fiscaal registratieproces gewijzigd, een functioneel connectorprofiel in een connectorgroep ingeschakeld of een nieuw functioneel connectorprofiel aan een connectorgroep toegevoegd.)
- U hebt wijzigingen aangebracht in de toewijzing van technische connectorprofielen aan hardwareprofielen.

Voer de volgende stappen uit om het fiscale integratieproces te valideren.

1. Ga in Commerce Headquarters naar de pagina **Fiscaal registratieproces** (**Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscaal registratieproces**).
1. Selecteer **Valideren** om het fiscale registratieproces te valideren.
1. Voer op de pagina **Distributieplanning** de taken **1070** en **1090** uit om gegevens over te brengen naar de kanaaldatabase.

## <a name="set-up-fiscal-texts-for-discounts"></a>Fiscale teksten voor kortingen instellen

In sommige gevallen moet een speciale tekst worden afgedrukt op een fiscaal ontvangstbewijs als een korting wordt toegepast. U kunt fiscale teksten voor kortingen instellen op de pagina **Fiscale connectorgroep** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectorgroepen**).

- Voor handmatige kortingen die worden toegepast op het POS, moet u een fiscale tekst voor de informatiecode of informatiecodegroep instellen die is opgegeven als de **Productkorting**-infocode in het POS-functionaliteitsprofiel.

    1. Selecteer op de pagina **Fiscale connectorgroep** **Tekst voor fiscaal ontvangstbewijs**.
    1. Selecteer op het tabblad **Informatiecodes** **Toevoegen** en selecteer een informatiecode of informatiecodegroep.
    1. Selecteer in het veld **Infocodenummer** een waarde.
    1. Selecteer in het veld **Subcodenummer** een waarde als een subcode vereist is voor de geselecteerde informatiecode.
    1. Geef in het veld **Tekst voor fiscaal ontvangstbewijs** een fiscale tekst op die moet worden afgedrukt op een ontvangstbewijs.
    1. Stelt de optie **Gebruikersinvoer afdrukken op fiscaal ontvangstbewijs** in op **Ja** om de tekst op een fiscaal ontvangstbewijs te overschrijven met informatie die een gebruiker handmatig invoert op het POS. Deze optie geldt alleen voor informatiecodes met het invoertype **tekst**.

    > [!NOTE]
    > U kunt een fiscale tekst opgeven voor verschillende Informatiecodes ter ondersteuning van scenario's waarbij informatiecodegroepen, gekoppelde informatiecodes en geactiveerde informatiecodes worden gebruikt. In deze scenario's bevat het fiscale ontvangstbewijs de fiscale teksten uit alle Informatiecodes die zijn gekoppeld aan de transactieregel waar de korting is toegepast.

- Voor kanaalspecifieke kortingen moet u een fiscale tekst definiëren voor de korting-id

    1. Selecteer op de pagina **Fiscale connectorgroep** **Tekst voor fiscaal ontvangstbewijs**.
    1. Selecteer op het tabblad **Kortingen** **Toevoegen** en selecteer een korting-id.
    1. Geef in het veld **Tekst voor fiscaal ontvangstbewijs** een fiscale tekst op die moet worden afgedrukt op een ontvangstbewijs.

    > [!NOTE]
    > Als verschillende kortingen worden toegepast op dezelfde transactieregel, bevat het fiscale ontvangstbewijs fiscale teksten van alle kortingen die zijn gekoppeld aan die transactieregel.

## <a name="set-error-handling-settings"></a>Instellingen voor het verwerken van fouten kiezen

De opties voor de afhandeling van fouten die beschikbaar in de fiscale integratie, worden ingesteld in het fiscale registratieproces. Zie voor meer informatie over het afhandelen van fouten in de fiscale integratie [Foutverwerking](fiscal-integration-for-retail-channel.md#error-handling).

Voer de volgende stappen uit om instellingen voor het afhandelen van fouten in te stellen.

1. Op de pagina **Fiscaal registratieproces** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale registratieprocessen**) kunt u de volgende parameters instellen voor elke stap van het fiscale registratieproces:

    - **Overslaan toestaan**: deze parameter maakt de optie **Overslaan** beschikbaar in het dialoogvenster voor foutafhandeling.
    - **Markeren als geregistreerd toestaan**: deze parameter maakt de optie **Markeren als geregistreerd** beschikbaar in het dialoogvenster voor foutafhandeling.
    - **Uitstellen toestaan**: deze parameter maakt de optie **Uitstellen** beschikbaar in het dialoogvenster voor foutafhandeling.
    - **Doorgaan bij fout** : als deze parameter is ingeschakeld, kan het proces voor fiscale registratie worden voortgezet op de POS-kassa als de fiscale registratie van een transactie of gebeurtenis mislukt. Anders moer, als u de fiscale registratie van de volgende transactie of gebeurtenis wilt uitvoeren, de operator de mislukte fiscale registratie opnieuw proberen, deze overslaan of de transactie of gebeurtenis markeren als geregistreerd. Zie voor meer informatie [Optionele fiscale registratie](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Als de parameter **Doorgaan bij fout** is ingeschakeld, worden de parameters **Overslaan toestaan** en **Markeren als geregistreerd toestaan** automatisch uitgeschakeld.

1. De opties **Overslaan** en **Markeren als geregistreerd** in het dialoogvenster voor foutafhandeling vereisen dat de machtiging **Overslaan van registratie of markeren als geregistreerd toestaan** is ingeschakeld. Als u deze machtiging wilt inschakelen, gaat u naar de pagina **Machtigingsgroepen** (**Retail en commerce \> Werknemers \> Machtigingsgroepen**) en stelt u de optie **Overslaan van registratie of markeren als geregistreerd toestaan** op **Ja** in.
1. Voor de optie **Uitstellen** in het dialoogvenster voor foutafhandeling moet de machtiging **Uitstellen toestaan** zijn ingeschakeld. Als u de machtiging wilt inschakelen, gaat u naar de pagina **Machtigingsgroepen** (**Retail en commerce \> Werknemers \> Machtigingsgroepen**) en stelt u de optie **Uitstellen toestaan** op **Ja** in.
1. Met de opties **Overslaan**, **Markeren als geregistreerd** en **Uitstellen** kunnen operators extra informatie invoeren wanneer de fiscale registratie mislukt. Als u deze functionaliteit beschikbaar wilt maken, moet u de infocodes **Overslaan**, **Markeren als geregistreerd** en **Uitstellen** opgeven in een fiscale connectorgroep. De gegevens die operators invoeren, worden vervolgens opgeslagen als een infocodetransactie die is gekoppeld aan de fiscale transactie. Zie voor meer informatie over infocodes [Informatiecodes en informatiecodegroepen](../info-codes-retail.md).

    > [!NOTE]
    > De **Product**-activeringsfunctie wordt niet ondersteund voor de informatiecodes die worden gebruikt voor **Overslaan** en **Markeren als geregistreerd** in fiscale connectorgroepen.

    - Selecteer op de pagina **Fiscale connectorgroep** op het tabblad **Informatiecodes** informatiecodes of informatiecodegroepen in de velden **Overslaan**, **Markeren als geregistreerd** en **Uitstellen**.

    > [!NOTE]
    > Eén fiscaal document en één niet-fiscaal document kunnen in elke stap van een fiscaal registratieproces worden gegenereerd. Een fiscale documentproviderextensie identificeert elk type transactie of gebeurtenis met betrekking tot fiscale of niet-fiscale documenten. De functie voor het verwerken van fouten geldt alleen voor fiscale documenten.
    >
    > - **Fiscaal document**: een verplicht document dat met succes moet worden geregistreerd (bijvoorbeeld een fiscaal ontvangstbewijs).
    > - **Niet-fiscaal document**: een aanvullend document voor de transactie of gebeurtenis (bijvoorbeeld een cadeaukaartstrook).

1. Als de operator moet kunnen doorgaan met het verwerken van de huidige bewerking (bijvoorbeeld een transactie maken of voltooien) nadat een statuscontrolefout is opgetreden, moet u de machtiging **Overslaan van statuscontrolefout toestaan** op de pagina **Machtigingsgroepen** (**Detailhandel en commerce \> Werknemers \> Machtigingsgroepen**) inschakelen. Zie voor meer informatie over de statuscontroleprocedure [Statuscontrole fiscale registratie](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Fiscale X/Z-rapporten instellen vanaf het POS

Als u fiscale X/Z-rapporten wilt inschakelen om te worden uitgevoerd vanaf het POS, moet u nieuwe knoppen toevoegen aan een POS-indeling.

- Volg op de pagina **Knoppenrasters** de instructies in [POS-bewerkingen toevoegen aan POS-indelingen met de ontwerpfunctie van het knoppenraster](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) om de ontwerper te installeren en een POS-indeling bij te werken.

    1. Selecteer de bij te werken indeling. 
    1. Voeg een nieuwe knop toe en stel de knopeigenschap **Fiscale X afdrukken** in.
    1. Voeg een nieuwe knop toe en stel de knopeigenschap **Fiscale Z afdrukken** in.
    1. Voer op de pagina **Distributionplanner** de taak **1090** uit om wijzigingen over te brengen naar de kanaaldatabase.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Handmatige uitvoering van uitgestelde fiscale registratie inschakelen

Als u een handmatige uitvoering van een uitgestelde fiscale registratie wilt inschakelen, moet u een nieuwe knop toevoegen aan een POS-indeling.

- Volg op de pagina **Knoppenrasters** de instructies in [POS-bewerkingen toevoegen aan POS-indelingen met de ontwerpfunctie van het knoppenraster](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) om de ontwerper te installeren en een POS-indeling bij te werken.

    1. Selecteer de bij te werken indeling.
    1. Voeg een nieuwe knop toe en stel de knopeigenschap **Fiscale registratie voltooien** in.
    1. Voer op de pagina **Distributieplanning** de taak **1090** uit om uw wijzigingen over te brengen naar de kanaaldatabase.


## <a name="view-connection-parameters-and-other-information-in-pos"></a>Verbindingsparameters en andere informatie in POS weergeven

Volg deze stappen om verbindingsparameters en andere informatie in POS weer te geven.

1. Open Modern POS (MPOS) of Cloud-POS (CPOS).
1. Selecteer **Instellingen**. Als fiscale integratie is ingeschakeld, wordt in de sectie **Fiscale integratie** aan de rechterkant de volgende informatie getoond:

    - De status van de fiscale integratie
    - De status van de laatste fiscale transactie
    - Het aantal uitstaande controlegebeurtenissen

1. Selecteer **Details** om de volgende informatie weer te geven:

    - Stappen in het registratieproces
    - Verbindingsparameters
    - Details van controlegebeurtenissen
 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]

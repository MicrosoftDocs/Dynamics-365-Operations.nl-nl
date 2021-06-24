---
title: Fiscale integratie voor Commerce-kanalen instellen
description: Dit onderwerp bevat richtlijnen voor het instellen van de functionaliteit voor fiscale integratie voor Commerce-kanalen.
author: josaw
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 2ac8dc8787ab0bdb796ec849f9ede3f697b09680
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193639"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Fiscale integratie voor Commerce-kanalen instellen

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Inleiding

Dit onderwerp bevat richtlijnen voor het instellen van de functionaliteit voor fiscale integratie voor Commerce-kanalen. Zie voor meer informatie over de fiscale integratie [Overzicht van fiscale integratie voor Commerce-kanalen](fiscal-integration-for-retail-channel.md).

Het instelproces van de fiscale integratie bevat de volgende taken:

1. Fiscale connectors configureren die fiscale apparaten of services vertegenwoordigen die worden gebruikt voor fiscale registratiedoeleinden, zoals fiscale printers.
2. Documentproviders configureren die fiscale documenten genereren die worden geregistreerd in fiscale apparaten of services door fiscale connectors.
3. Het fiscale registratieproces configureren dat een reeks fiscale registratiestappen definieert en de fiscale connectors en fiscale documentproviders die voor elke stap worden gebruikt.
4. Het fiscale registratieproces toewijzen aan POS-functionaliteitsprofielen (Point Of Sale).
5. Technische connectorprofielen toewijzen aan hardwareprofielen.

## <a name="set-up-a-fiscal-registration-process"></a>Een fiscaal registratieproces instellen

Voordat u de functionaliteit voor fiscale integratie gebruikt, moet u de volgende instellingen configureren.

1. Werk de Commerce-parameters bij.

    1. Stel op de pagina **Gedeelde Commerce-parameters** op het tabblad **Algemeen** de optie **Fiscale integratie inschakelen** in op **Ja**. Definieer op het tabblad **Nummerreeksen** de nummerreeksen voor de volgende referenties:

        - Nummer van fiscaal technisch profiel
        - Nummer fiscale connectorgroep
        - Nummer van registratieproces

    2. Definieer op de pagina **Commerce-parameters** de nummerreeks voor het fiscale profielnummer.

    > [!NOTE]
    > Nummerreeksen zijn optioneel. Nummers voor alle fiscale integratie-entiteiten kunnen worden gegenereerd uit nummerreeksen of handmatig.

2. Upload configuraties van fiscale connectors en fiscale documentproviders.

    Een fiscale documentprovider is verantwoordelijk voor het genereren van belastingdocumenten die staan voor transacties en gebeurtenissen die zijn geregistreerd in het POS in een indeling die ook wordt gebruikt voor de interactie met een fiscaal apparaat of een fiscale service. Een fiscale documentprovider kan bijvoorbeeld een voorstelling van een fiscaal ontvangstbewijs genereren in een XML-indeling.

    Een fiscale connector is verantwoordelijk voor de communicatie met een fiscaal apparaat of een fiscale service. Een fiscale connector kan bijvoorbeeld een ontvangstbewijs dat een fiscale documentprovider in een XML-indeling heeft gemaakt, verzenden naar een fiscale printer. Zie voor meer informatie over fiscale integratieonderdelen [Fiscaal registratieproces en fiscale integratievoorbeelden voor fiscale apparaten](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. Upload op de pagina **Fiscale connectors** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectors**) een XML-configuratie voor elk apparaat of elke service die u wilt gebruiken voor fiscale integratiedoeleinden.

        > [!TIP]
        > Door **Weergeven** te selecteren kunt u alle functionele en technische profielen weergeven die gerelateerd zijn aan de huidige fiscale connector.

    2. Upload op de pagina **Fiscale documentproviders** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale documentproviders**) een XML-configuratie voor elk apparaat of elke service die u wilt gebruiken.

        > [!TIP]
        > Door **Weergeven** te selecteren kunt u alle functionele profielen weergeven die gerelateerd zijn aan de huidige fiscale documentprovider.

    Zie voor voorbeelden van configuraties van fiscale connectors en fiscale documentproviders [Fiscale integratievoorbeelden in de Retail-SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Toewijzing van gegevens wordt beschouwd als onderdeel van een fiscale documentprovider. Als u andere toewijzingen van gegevens voor dezelfde connector wilt instellen (bijvoorbeeld staatspecifieke regelgeving), moet u verschillende fiscale documentproviders maken.

3. Maak functionele connectorprofielen en technische connectorprofielen.

    1. Maak op de pagina **Functionele connectorprofielen** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Functionele connectorprofielen**) een functioneel connectorprofiel voor elke combinatie van een fiscale connector en een fiscale documentprovider die gerelateerd is aan de fiscale connector.

        1. Selecteer een connectornaam.
        2. Selecteer een documentprovider.

        U kunt de gegevenstoewijzingsparameters in een functioneel connectorprofiel wijzigen. Als u de standaardparameters wilt herstellen die zijn gedefinieerd in de configuratie van de fiscale documentprovider, selecteert u **Bijwerken**.

        **Voorbeelden**

        | Parameter  | Format | Voorbeeld |
        |---|--------|---------|
        | **Btw-tariefinstellingen** | waarde : VATrate | 1 : 2000, 2 : 1800 |
        | **Toewijzing van btw-codes** | VATcode : waarde | vat20 : 1, vat18 : 2 |
        | **Toewijzing van betalingsmethoden** | TenderType : waarde | Contant : 1, Kaart : 2 |

        > [!NOTE]
        > Functionele connectorprofielen zijn specifiek voor het bedrijf. Als u van plan bent dezelfde combinatie van een fiscale connector en een fiscale documentprovider te gebruiken in verschillende bedrijven, maakt u een functioneel connectorprofiel voor elk bedrijf.

    2. Maak op de pagina **Technische connectorprofielen** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Technische connectorprofielen**) een technisch connectorprofiel voor elke fiscale connector.

        1. Selecteer een connectornaam.
        2. Selecteer een connectortype. Voor apparaten die zijn verbonden aan een hardwarestation, selecteert u **Lokaal**.

            > [!NOTE]
            > Alleen lokale connectors worden ondersteund.

        Parameters op de tabbladen **Apparaat** en **Instellingen** in een technisch connectorprofiel kunnen worden gewijzigd. Als u de standaardparameters wilt herstellen die zijn gedefinieerd in de configuratie van de fiscale connector, selecteert u **Bijwerken**. Wanneer een nieuwe versie van een XML-configuratie wordt geladen, ontvangt u een bericht dat de huidige fiscale connector of fiscale documentprovider al wordt gebruikt. Deze procedure overschrijft niet handmatige wijzigingen die eerder zijn aangebracht in functionele connectorprofielen en technische connectorprofielen. Als u de standaardset parameters wilt toepassen vanuit een nieuwe configuratie, klikt u op **Bijwerken** op de pagina **Functionele connectorprofielen** of de pagina **Technische connectorprofielen**.

4. Maak fiscale connectorgroepen.

    Een fiscale connectorgroep combineert een subset van functionele connectors die identieke functies uitvoeren en worden gebruikt in dezelfde stap van een fiscaal registratieproces. Als bijvoorbeeld verschillende fiscale printermodellen kunnen worden gebruikt in een winkel, kunnen fiscale connectors voor die fiscale printers worden gecombineerd in een fiscale connectorgroep.

    1. Maak op de pagina **Fiscale connectorgroep** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectorgroepen**) een nieuwe fiscale connectorgroep.
    2. Voeg functionele profielen toe aan de connectorgroep. Selecteer op het tabblad **Functionele profielen** **Toevoegen** en selecteer een profielnummer. Elke fiscale connector in een connectorgroep kan slechts één functioneel profiel hebben.
    3. Als u het gebruik van het functionele profiel wilt onderbreken, stelt u de optie **Uitschakelen** in op **Ja**. Deze wijziging is alleen van invloed op de huidige connectorgroep. U kunt doorgaan met hetzelfde functionele profiel te gebruiken in andere connectorgroepen.

5. Maak een fiscaal registratieproces.

    Een fiscaal registratieproces wordt gedefinieerd door de volgorde van registratiestappen en de connectorgroep die voor elke stap wordt gebruikt.

    1. Maak op de pagina **Fiscaal registratieproces** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale registratieprocessen**) een nieuwe record voor elk uniek fiscaal registratieproces.
    2. Voeg registratiestappen aan het proces toe:

        1. Selecteer **Toevoegen**.
        2. Selecteer een fiscaal connectortype.
        3. Selecteer in het veld **Groepsnummer** een geschikte fiscale connectorgroep.

6. Wijs entiteiten van het fiscale registratieproces toe aan POS-profielen.

    1. Wijs op de pagina **POS-functionaliteitsprofielen** (**Detailhandel en commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**) het fiscale registratieproces toe aan een POS-functionaliteitsprofiel. Selecteer **Bewerken** en selecteer vervolgens op het tabblad **Fiscaal registratieproces** in het veld **Procesnummer** een proces.
    2. Wijs op de pagina **POS-hardwareprofiel** (**Detailhandel en commerce \> Kanaalinstellingen \> POS-instellingen \> POS profielen \> Hardwareprofielen**) technische connectorprofielen toe aan een hardwareprofiel. Selecteer **Bewerken**, voeg een regel toe op het tabblad **Fiscale randapparatuur** en selecteer vervolgens in het veld **Profielnummer** een technisch connectorprofiel.

    > [!NOTE]
    > U kunt verschillende technische profielen toevoegen aan hetzelfde hardwareprofiel. Een hardwareprofiel of POS-functionaliteitsprofiel moet achter slechts één intersectie met een fiscale connectorgroep hebben.

    De fiscale registratiestroom wordt gedefinieerd door het fiscale registratieproces en ook door sommige parameters van fiscale integratieonderdelen: de runtime-extensie Commerce voor fiscale documentprovider en de extensie Hardware Station voor de fiscale connector.

    - Het abonnement van gebeurtenissen en transacties op fiscale registratie wordt vooraf gedefinieerd in de fiscale documentprovider.
    - De fiscale documentprovider is ook verantwoordelijk voor het identificeren van de fiscale connector die wordt gebruikt voor fiscale registratie. Het komt overeen met de functionele connectorprofielen die zijn opgenomen in de fiscale connectorgroep die is opgegeven voor de huidige stap van het fiscale registratieproces met het technische connectorprofiel dat is toegewezen aan het hardwareprofiel van het Hardware-station waaraan het POS is gekoppeld.
    - De fiscale documentprovider gebruikt de instellingen voor gegevenstoewijzing van de configuratie van de fiscale documentprovider om transactie-/gebeurtenisgegevens, zoals belasting en betalingen, te transformeren terwijl een fiscaal document wordt gemaakt.
    - Wanneer de fiscale documentprovider een fiscaal document genereert, kan de fiscale connector het zoals het is verzenden naar het fiscale apparaat of het ontleden en transformeren tot een reeks opdrachten van de apparaat-API (Application Programming Interface), afhankelijk van hoe de communicatie wordt verwerkt.

7. Selecteer op de pagina **Fiscaal registratieproces** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale registratieprocessen**) **Valideren** om het fiscale registratieproces te valideren.

    Het is aan te raden om dit type validatie uit te voeren in de volgende gevallen:

    - Nadat u alle instellingen voor een nieuw registratieproces hebt voltooid, inclusief wanneer u registratieprocessen toewijst aan POS-functionaliteitsprofielen en hardwareprofielen.
    - Nadat u wijzigingen in een bestaand fiscaal registratieproces hebt aangebracht en als deze wijzigingen ertoe kunnen leiden dat tijdens runtime een andere fiscale connector wordt geselecteerd (bijvoorbeeld als u de connectorgroep voor een stap in het fiscale registratieproces wijzigt, een functioneel connectorprofiel inschakelt in een connectorgroep of een nieuw functioneel connectorprofiel toevoegt aan een connectorgroep).
    - Nadat u wijzigingen hebt aangebracht in de toewijzing van technische connectorprofielen aan hardwareprofielen.

8. Voer op de pagina **Distributieplanning** de taken **1070** en **1090** uit om gegevens over te brengen naar de kanaaldatabase.

## <a name="set-up-fiscal-texts-for-discounts"></a>Fiscale teksten voor kortingen instellen

In sommige gevallen moet een speciale tekst worden afgedrukt op een fiscaal ontvangstbewijs als een korting wordt toegepast. U kunt fiscale teksten voor kortingen instellen op de pagina **Fiscale connectorgroep** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectorgroepen**).

- Voor handmatige kortingen die worden toegepast op het POS, moet u een fiscale tekst voor de informatiecode of informatiecodegroep instellen die is opgegeven als de **Productkorting**-infocode in het POS-functionaliteitsprofiel.

    1. Selecteer op de pagina **Fiscale connectorgroep** **Tekst voor fiscaal ontvangstbewijs**.
    2. Selecteer op het tabblad **Informatiecodes** **Toevoegen** en selecteer een informatiecode of informatiecodegroep.
    3. Selecteer in het veld **Infocodenummer** een waarde.
    4. Selecteer in het veld **Subcodenummer** een waarde als een subcode vereist is voor de geselecteerde informatiecode.
    5. Geef in het veld **Tekst voor fiscaal ontvangstbewijs** een fiscale tekst op die moet worden afgedrukt op een ontvangstbewijs.
    6. Stelt de optie **Gebruikersinvoer afdrukken op fiscaal ontvangstbewijs** in op **Ja** om de tekst op een fiscaal ontvangstbewijs te overschrijven met informatie die een gebruiker handmatig invoert op het POS. Deze optie geldt alleen voor informatiecodes met het invoertype **tekst**.

    > [!NOTE]
    > U kunt een fiscale tekst opgeven voor verschillende Informatiecodes ter ondersteuning van scenario's waarbij informatiecodegroepen, gekoppelde informatiecodes en geactiveerde informatiecodes worden gebruikt. In deze scenario's bevat het fiscale ontvangstbewijs de fiscale teksten uit alle Informatiecodes die zijn gekoppeld aan de transactieregel waar de korting is toegepast.

- Voor kanaalspecifieke kortingen moet u een fiscale tekst definiëren voor de korting-id

    1. Selecteer op de pagina **Fiscale connectorgroep** **Tekst voor fiscaal ontvangstbewijs**.
    2. Selecteer op het tabblad **Kortingen** **Toevoegen** en selecteer een korting-id.
    3. Geef in het veld **Tekst voor fiscaal ontvangstbewijs** een fiscale tekst op die moet worden afgedrukt op een ontvangstbewijs.

    > [!NOTE]
    > Als verschillende kortingen worden toegepast op dezelfde transactieregel, bevat het fiscale ontvangstbewijs fiscale teksten van alle kortingen die zijn gekoppeld aan die transactieregel.

## <a name="set-error-handling-settings"></a>Instellingen voor het verwerken van fouten kiezen

De opties voor de afhandeling van fouten die beschikbaar in de fiscale integratie, worden ingesteld in het fiscale registratieproces. Zie voor meer informatie over het afhandelen van fouten in de fiscale integratie [Foutverwerking](fiscal-integration-for-retail-channel.md#error-handling).

1. Op de pagina **Fiscaal registratieproces** (**Detailhandel en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale registratieprocessen**) kunt u de volgende parameters instellen voor elke stap van het fiscale registratieproces:

    - **Overslaan toestaan**: deze parameter maakt de optie **Overslaan** beschikbaar in het dialoogvenster voor foutafhandeling.
    - **Markeren als geregistreerd toestaan**: deze parameter maakt de optie **Markeren als geregistreerd** beschikbaar in het dialoogvenster voor foutafhandeling.
    - **Doorgaan bij fout** : als deze parameter is ingeschakeld, kan het proces voor fiscale registratie worden voortgezet op de POS-kassa als de fiscale registratie van een transactie of gebeurtenis mislukt. Anders moer, als u de fiscale registratie van de volgende transactie of gebeurtenis wilt uitvoeren, de operator de mislukte fiscale registratie opnieuw proberen, deze overslaan of de transactie of gebeurtenis markeren als geregistreerd. Zie voor meer informatie [Optionele fiscale registratie](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Als de parameter **Doorgaan bij fout** is ingeschakeld, worden de parameters **Overslaan toestaan** en **Markeren als geregistreerd toestaan** automatisch uitgeschakeld.

2. De opties **Overslaan** en **Markeren als geregistreerd** in het dialoogvenster voor foutafhandeling vereisen de machtiging **Overslaan van registratie of markeren als geregistreerd toestaan**. Schakel daarom op de pagina **Machtigingsgroepen** (**Detailhandel en commerce \> Werknemers \> Machtigingsgroepen**) de machtiging **Overslaan van registratie of markeren als geregistreerd toestaan** in.
3. Met de opties **Overslaan** en **Markeren als geregistreerd** kunnen operators extra informatie invoeren wanneer de fiscale registratie mislukt. Als u deze functionaliteit beschikbaar wilt maken, moet u de infocodes **Overslaan** en **Markeren als geregistreerd** opgeven in een fiscale connectorgroep. De gegevens die operators invoeren, worden vervolgens opgeslagen als een infocodetransactie die is gekoppeld aan de fiscale transactie. Zie voor meer informatie over infocodes [Informatiecodes en informatiecodegroepen](../info-codes-retail.md).

    > [!NOTE]
    > De **Product**-activeringsfunctie wordt niet ondersteund voor de informatiecodes die worden gebruikt voor **Overslaan** en **Markeren als geregistreerd** in fiscale connectorgroepen.

    - Selecteer op de pagina **Fiscale connectorgroep** op het tabblad **Informatiecodes** informatiecodes of informatiecodegroepen in de velden **Overslaan** en **Markeren als geregistreerd**.

    > [!NOTE]
    > Eén fiscaal document en één niet-fiscaal document kunnen in elke stap van een fiscaal registratieproces worden gegenereerd. Een fiscale documentproviderextensie identificeert elk type transactie of gebeurtenis met betrekking tot fiscale of niet-fiscale documenten. De functie voor het verwerken van fouten geldt alleen voor fiscale documenten.
    >
    > - **Fiscaal document**: een verplicht document dat met succes moet worden geregistreerd (bijvoorbeeld een fiscaal ontvangstbewijs).
    > - **Niet-fiscaal document**: een aanvullend document voor de transactie of gebeurtenis (bijvoorbeeld een cadeaukaartstrook).

4. Als de operator moet kunnen doorgaan met het verwerken van de huidige bewerking (bijvoorbeeld een transactie maken of voltooien) nadat een statuscontrolefout is opgetreden, moet u de machtiging **Overslaan van statuscontrolefout toestaan** op de pagina **Machtigingsgroepen** (**Detailhandel en commerce \> Werknemers \> Machtigingsgroepen**) inschakelen. Zie voor meer informatie over de statuscontroleprocedure [Statuscontrole fiscale registratie](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Fiscale X/Z-rapporten instellen vanaf het POS

Als u fiscale X/Z-rapporten wilt inschakelen om te worden uitgevoerd vanaf het POS, moet u nieuwe knoppen toevoegen aan een POS-indeling.

- Volg op de pagina **Knoppenrasters** de instructies in [POS-bewerkingen toevoegen aan POS-indelingen met de ontwerpfunctie van het knoppenraster](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) om de ontwerper te installeren en een POS-indeling bij te werken.

    1. Selecteer de bij te werken indeling. 
    2. Voeg een nieuwe knop toe en stel de knopeigenschap **Fiscale X afdrukken** in.
    3. Voeg een nieuwe knop toe en stel de knopeigenschap **Fiscale Z afdrukken** in.
    4. Voer op de pagina **Distributionplanner** de taak **1090** uit om wijzigingen over te brengen naar de kanaaldatabase.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Handmatige uitvoering van uitgestelde fiscale registratie inschakelen

Als u een handmatige uitvoering van een uitgestelde fiscale registratie wilt inschakelen, moet u een nieuwe knop toevoegen aan een POS-indeling.

- Volg op de pagina **Knoppenrasters** de instructies in [POS-bewerkingen toevoegen aan POS-indelingen met de ontwerpfunctie van het knoppenraster](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) om de ontwerper te installeren en een POS-indeling bij te werken.

    1. Selecteer de bij te werken indeling.
    2. Voeg een nieuwe knop toe en stel de knopeigenschap **Fiscale registratie voltooien** in.
    3. Voer op de pagina **Distributieplanning** de taak **1090** uit om uw wijzigingen over te brengen naar de kanaaldatabase.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
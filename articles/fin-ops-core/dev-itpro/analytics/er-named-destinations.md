---
title: Recordspecifieke ER-bestemmingen voor afdrukbeheer configureren
description: In dit onderwerp wordt uitgelegd hoe recordspecifieke bestemmingen voor afdrukbeheer geconfigureerd kunnen worden voor een ER-indeling (elektronische rapportage) die geconfigureerd wordt om uitgaande documenten te genereren.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1e06fafe8d8bbe92ddf4fcd94d7271a1fbb6362a
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413587"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Recordspecifieke ER-bestemmingen voor afdrukbeheer configureren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe een gebruiker in de rol Systeembeheerder of Debiteurenboekhouder de volgende taken kan uitvoeren:

- De toegewezen bestemmingen voor [elektronische rapportage (ER)](general-electronic-reporting.md) configureren voor een ER-oplossing die facturen met vrije tekst genereert.
- Een ER-bestemming toewijzen aan één [afdrukbeheer](document-reporting-services.md)record.

De procedures kunnen in het USMF-bedrijf worden uitgevoerd. U hoeft hiervoor geen code te schrijven.

## <a name="introduction"></a>Inleiding

U kunt [bestemmingen](electronic-reporting-destinations.md) configureren voor elke map in de bestandsuitvoercomponent van een ER[-indelings](general-electronic-reporting.md#FormatComponentOutbound)[configuratie](general-electronic-reporting.md#Configuration) die wordt gebruikt voor het genereren van uitgaande documenten. Indien u een ER-indeling van dit type uitvoert en als u over de juiste toegangsrechten beschikt, kunt u ook de geconfigureerde bestemmingsinstellingen wijzigen tijdens runtime.

In Microsoft Dynamics 365 Finance **versie 10.0.17 en hoger** kan een actiecode worden [ingesteld](er-apis-app10-0-17.md) voor een ER-indeling waarin een actie is vastgelegd die gebruikers uitvoeren door die ER-indeling uit te voeren. In de module **Debiteuren** kunt u bijvoorbeeld in de afdrukbeheerinstellingen een ER-indeling selecteren om een specifiek bedrijfsdocument te genereren, zoals een factuur met vrije tekst. U kunt vervolgens **Weergeven** selecteren om een voorbeeld van de factuur weer te geven of **Afdrukken** om deze naar een printer te sturen. Als een actie tijdens runtime voor de lopende ER-indeling wordt doorgegeven, kunt u [verschillende ER-bestemmingen voor verschillende gebruikersacties configureren](er-action-dependent-destinations.md).

In Finance **versie 10.0.21 en hoger** kan een benoemde bestemming worden [ingesteld](er-apis-app10-0-21.md) voor een ER-indeling en kan deze worden toegewezen aan de afdrukbeheerrecord die wordt verwerkt wanneer die ER-indeling wordt uitgevoerd. In de module **Debiteuren** wilt u bijvoorbeeld in de afdrukbeheerinstellingen de **Oorspronkelijke** record dusdanig configureren, dat de volgende acties worden uitgevoerd:

- Een ER-indeling uitvoeren.
- De gegenereerde factuur per e-mail naar een klant verzenden.
- De **gekopieerde** record dusdanig configureren dat het dezelfde indeling uitvoert.
- Een kopie van de factuur via een netwerkprinter afdrukken.

In dit geval moet u verschillende ER-bestemmingen configureren voor de ER-indeling die wordt uitgevoerd en moet u de bestemmingen voor verschillende afdrukbeheerrecords selecteren.

## <a name="prerequisites"></a>Vereisten

Voordat u begint, moet de functie **Instellen ER-bestemmingen voor afdrukbeheeritem toestaan** worden ingeschakeld in de werkruimte voor [Functiebeheer](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace). Tevens moet de broncode dusdanig worden gewijzigd dat de benoemde ER-bestemmingen in de huidige Finance-versie geconfigureerd kunnen worden en om de [nieuwe](er-apis-app10-0-21.md) ER API in te schakelen.

Daarnaast moet de ER-configuratie voor **Vrije-tekstfactuur (Excel)** in uw Finance-versie worden [geïmporteerd](er-download-configurations-global-repo.md).

## <a name="configure-a-new-er-destination"></a>Een nieuwe ER-bestemming configureren

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Selecteer een factuur voor klantaccount **US-001**.
3. Selecteer op de pagina **Vrije-tekstfactuur** in het tabblad **Factuur** in de groep **Afdrukbeheer** de optie **Afdrukbeheer**.
4. Vouw op de pagina **Afdrukbeheerinstellingen** de **Module - debiteuren** \> **Documenten** \> **Vrije-tekstfactuur** uit en selecteer de record **Oorspronkelijk** en voer vervolgens deze stappen uit:

    1.  Houd de huidige instellingen van de geselecteerde record aan:
        -   Het standaard-SSRS-rapport **FreeTextInvoice.Report** is geselecteerd in het veld **Rapportindeling**.
        -   De **\<Default\>** naam wordt weergegeven in het veld **Bestemming** om aan te geven dat er geen aangepaste bestemming geselecteerd is voor het toegewezen SSRS-rapport. 
    2.  Selecteer de ER-indelingsconfiguratie voor de **Vrije-tekstfactuur (Excel)** in het veld **Rapportindeling**.
        -   De naam van het veld **Bestemming** wordt gewijzigd in **Naam bestemming**.
        -   De **\<No named destination\>** naam wordt weergegeven in het veld **Naam bestemming** om aan te geven dat er geen benoemde bestemming geselecteerd is voor de toegewezen ER-indeling.
    3.  Selecteer de pijlknop rechts van het veld **Naam bestemming**.    
    4. Voer in het veld **Naam** de **Hoofdbestemming** in op de pagina **Elektronische rapportage benoemde bestemming**.
    5. Selecteer **Opslaan**.
    6. Configureer in het sneltabblad **Bestandsbestemming** [de](er-destination-type-email.md)**e-mail** bestemming voor het onderdeel **Rapport**.
    7. Sluit de pagina **Elektronische rapportage benoemde bestemming**.
    8. Selecteer op de pagina **Afdrukbeheerinstellingen** in het veld **Naam bestemming** de **Hoofdbestemming**.

    ![Een benoemde ER-bestemming configureren voor de geselecteerde ER-indeling en deze toewijzen aan een geconfigureerde afdrukbeheerrecord op de pagina Afdrukbeheerinstellingen](./media/er-named-destinations-01.gif)

    U hebt nu de benoemde ER-bestemming **Hoofdbestemming** geconfigureerd voor de indeling **Vrije-tekstfactuur (Excel)** en deze toegewezen aan de record **Oorspronkelijk** afdrukbeheer onder **Module - Debiteuren** \> **Documenten** \> **Vrije-tekstfactuur**.

5. Vouw **Module- Klanten** \> **Account - US-001** \> **Vrije-tekstfactuur** uit, selecteer de **Oorspronkelijke** record en volg vervolgens deze stappen:

    1. Selecteer de record en houd deze ingedrukt (of klik met de rechtermuisknop) en selecteer **Overschrijven**.
    2. Selecteer de pijlknop rechts van het veld **Naam bestemming**.
    3. Selecteer **Nieuw** in het actievenster op de pagina **Elektronische rapportage benoemde bestemming**.
    4. Voer in het veld **Naam** de tekst **US-001 bestemming** in.
    5. Configureer in het sneltabblad **Bestandsbestemming** [de](er-destination-type-print.md) **printer** bestemming voor het onderdeel **Rapport**.
    6. Sluit de pagina **Elektronische rapportage benoemde bestemming**.
    7. Selecteer op de pagina **Afdrukbeheerinstellingen** in het veld **Naam bestemming** de **US-001 bestemming**.

    ![Een benoemde ER-bestemming configureren voor de geselecteerde ER-indeling en deze toewijzen aan een geconfigureerde afdrukbeheerrecord op de pagina Afdrukbeheerinstellingen](./media/er-named-destinations-02.gif)

    U hebt nu de benoemde ER-bestemming **US-001 bestemming** geconfigureerd voor de indeling **Vrije-tekstfactuur (Excel)** en deze toegewezen aan de record **Oorspronkelijk** afdrukbeheer onder **Module - Debiteuren** \> **Account - US-001** \> **Vrije-tekstfactuur**.

Wanneer een vrije-tekstfactuur wordt verwerkt, wordt de ER-indeling voor de **Vrije-tekstfactuur (Excel)** uitgevoerd en vindt een van de volgende gebeurtenissen plaats:

- Als de vrije-tekstfactuur voor een andere klant is dan US-001, wordt het gegenereerde document per e-mail verzonden.
- Als de vrije-tekstfactuur voor klant US-001 is, wordt het gegenereerde document uitgeprint.

> [!NOTE]
> Wanneer er geen benoemde bestemming vastgelegd is voor een afdrukbeheerrecord die tijdens de runtime wordt verwerkt, worden de standaard ER-bestemmingen gebruikt als deze beschikbaar zijn voor de lopende ER-indeling.

> [!IMPORTANT]
> Op de pagina **Bestemming elektronische rapportage** (**Organisatiebeheer** \> **Elektronische rapportage** \> **Bestemming elektronische rapportage**) wordt u op de hoogte gebracht van de aanwezigheid van de benoemde bestemmingen als u een ER-indeling selecteert waarvoor minimaal één benoemde bestemming geconfigureerd is.
>
> ![Melding over de aanwezigheid van geconfigureerde benoemde bestemmingen voor de geselecteerde ER-indeling op de pagina Bestemming elektronische rapportage](./media/er-named-destinations-03.png)
>
> Als u de standaardbestemming verwijdert, worden alle benoemde bestemmingen ook verwijderd. Als de benoemde bestemmingen voor afdrukbeheerrecords geselecteerd zijn, wordt de selectie van deze benoemde bestemmingen geannuleerd.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Een bestaande ER-bestemming als een nieuwe benoemde bestemming kopiëren

Wanneer de standaard benoemde ER-bestemming beschikbaar is voor een ER-indeling, kan deze worden gebruikt als sjabloon voor nieuwe ER-bestemmingen. Als u een nieuwe ER-bestemming wilt aanmaken op basis van de standaardbestemming, selecteert u **Kopiëren uit de standaardwaarde** op de pagina **Elektronische rapportage benoemde bestemming**. De nieuwe bestemming krijgt de naam **Standaard**. U kunt deze stap zo vaak als nodig herhalen.

U kunt een bestaande benoemde bestemming selecteren als sjabloon voor een nieuwe benoemde bestemming. Als u een nieuwe benoemde ER-bestemming wilt aanmaken op basis van een geselecteerde benoemde bestemming, selecteert u **Kopiëren** op de pagina **Elektronische rapportage benoemde bestemming**. De nieuwe bestemming heeft dezelfde naam als de geselecteerde benoemde bestemming, maar het achtervoegsel 'Kopie' wordt eraan toegevoegd. U kunt deze stap zo vaak als nodig herhalen.

## <a name="security-considerations"></a>Beveiligingsoverwegingen

U kunt op de pagina **Afdrukbeheerinstellingen** de benoemde ER-bestemmingen alleen instellen als u voor het uitvoeren van deze taak [geautoriseerd](../sysadmin/role-based-security.md#permissions) bent. Er kan een machtiging aan u worden verleend als de **Elektronische rapporteringsindeling configureren**[-machtiging](../sysadmin/role-based-security.md#duties) aan een van uw [beveiligingsrollen](../sysadmin/role-based-security.md#security-roles) is toegewezen. Zie voor meer informatie [Beveiligingsbeleid](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)

[Wijzigingen in API voor raamwerk voor elektronische rapportage in Application update 10.0.17](er-apis-app10-0-17.md)

[Wijzigingen in API voor raamwerk voor elektronische rapportage in Application update 10.0.21](er-apis-app10-0-21.md)

[Code wijzigen om gebruikers in staat te stellen de benoemde ER-bestemmingen te configureren en te gebruiken](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Configuraties voor elektronische rapportage aanpassen om een elektronisch document te genereren
description: In dit onderwerp wordt uitgelegd hoe u de door Microsoft geleverde ER-configuraties (elektronische rapportage) kunt aanpassen, waarmee een aangepast elektronisch document wordt gegenereerd.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c8cf4866b6a8c239359d726d8cd4f03a9eb4137
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324082"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Configuraties voor elektronische rapportage aanpassen om een elektronisch document te genereren

[!include[banner](../includes/banner.md)]

Met het [Raamwerk voor elektronische rapportage (ER)](general-electronic-reporting.md) kunt u de [configuraties](general-electronic-reporting.md#Configuration) voor elektronische rapportage uploaden die Microsoft in uw Microsoft Dynamics 365 Finance aanbiedt. Op deze manier kunnen de door Microsoft geleverde configuraties fungeren als de oplossing voor elektronische rapportage die wordt gebruikt om elektronische klantfacturen (e-facturen) te genereren. U kunt deze ER-oplossing gebruiken om uw aangepaste ER-oplossing te configureren om toegang te krijgen tot uw aangepaste databasevelden en om e-facturen te genereren die voldoen aan uw specifieke behoeften, zonder dat u de broncode hoeft te bewerken.

## <a name="overview"></a>Overzicht

Voor het voorbeeld in dit onderwerp moet u een nationale belasting-ID opgeven als nieuw aangepast kenmerk van elke klant die u elektronisch factureert. Daarom moet u de structuur van de factuur die momenteel wordt gebruikt, aanpassen door een nieuw item toe te voegen dat moet worden gevuld met de belastingcode in elke elektronische factuur die wordt gegenereerd.

In de procedures in dit onderwerp wordt uitgelegd hoe een gebruiker met de rol Systeembeheerder, Ontwikkelaar voor elektronische rapportage of Functioneel consultant voor elektronische rapportage de volgende taken kan uitvoeren in uw Finance-exemplaar:

- [Configureer de minimale set ER-parameters die nodig zijn om het ER-raamwerk te gaan gebruiken](#ConfigureER).
- [Importeer de eerste versies van de ER-standaardconfiguraties die beschikbaar zijn om e-facturen te genereren](#ImportERConfigurations1).
- [Configureer de parameters van de module klanten om de ER-standaardconfiguraties te gaan gebruiken](#ConfigureAR1).
- [Configureer de parameters van de rechtspersoon om klanten te factureren](#ConfigureLE).
- [Bereid een klantrecord voor op elektronische facturering](#ConfigureCustomer1).
- [Voeg een klantfactuur toe en boek en verzend deze met behulp van ER-standaardconfiguraties](#ProcessInvoice1).
- [Voeg een aangepast databaseveld toe om een nationale belasting-ID voor klanten te beheren](#AddCustomField).
- [Vernieuw de ER-metagegevens om wijzigingen in de database mogelijk te maken voor de ontwerper van ER-modeltoewijzingen](#RefreshERMetadata).
- [Ontwerp de aangepaste ER-configuraties om e-facturen te genereren die de nieuwe belastingcode bevatten](#DesignCustomERConfigurations).
- [Configureer de parameters van de module klanten om de aangepaste ER-configuraties te gaan gebruiken](#ConfigureAR2).
- [Werk een klantrecord bij voor elektronische facturering](#ConfigureCustomer2).
- [Voeg een klantfactuur toe en boek en verzend deze met behulp van de aangepaste ER-configuraties](#ProcessInvoice2).
- [Importeer de nieuwe versies van de ER-standaardconfiguraties die beschikbaar zijn om e-facturen te genereren](#ImportERConfigurations2).
- [Neem de wijzigingen in de nieuwe versies van de ER-standaardconfiguraties op in uw aangepaste ER-configuraties](#RebaseCustomERConfigurations).
- [Voeg een klantfactuur toe en boek en verzend deze met behulp van de nieuwe versies van de aangepaste ER-configuraties](#ProcessInvoice3).

Al deze procedures kunnen in het **DEMF**-bedrijf worden uitgevoerd.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>Het ER-raamwerk configureren

Als gebruiker met de rol Functioneel consultant voor elektronische rapportage of Ontwikkelaar van elektronische rapportage moet u de minimale set met ER-parameters configureren. U kunt vervolgens het ER-raamwerk gaan gebruiken om aangepaste versies van de standaardconfiguraties van de ER-oplossing te ontwerpen die wordt gebruikt om e-facturen te genereren.

### <a name="configure-er-parameters"></a>ER-parameters configureren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Parameters van elektronische rapportage**.
3. Stel op de pagina **Parameters van elektronische rapportage** op het tabblad **Algemeen** de optie **Ontwerpmodus inschakelen** in op **Ja**.
4. Selecteer op het tabblad **Bijlagen** in het veld **Configuraties** de optie **Bestand**.
5. Selecteer in de velden **Taakarchief**, **Tijdelijk**, **Basislijn** en **Overige** het type **Bestand**.

Meer informatie over het configureren van ER-parameters vindt u in [Het ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>Een ER-configuratieprovider activeren

Elke ER-configuratie die wordt toegevoegd, wordt gemarkeerd als het eigendom van een ER-configuratieprovider. De ER-configuratieprovider die is geactiveerd in de werkruimte **Elektronische rapportage** wordt hiervoor gebruikt. Daarom moet u een ER-configuratieprovider activeren in de werkruimte **Elektronische rapportage** voordat u ER-configuraties gaat toevoegen of bewerken.

> [!NOTE]
> Alleen de eigenaar van een ER-configuratie kan deze bewerken. Daarom moet een geschikte ER-configuratieprovider worden geactiveerd in de werkruimte **Elektronische rapportage**, voordat een ER-configuratie kan worden bewerkt.

#### <a name="review-the-list-of-er-configuration-providers"></a>De lijst met ER-configuratie providers bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.
3. Op de tabelpagina **Configuratieproviders** heeft elke providerrecord een unieke naam en een unieke URL. Bekijk de inhoud van deze pagina. Als er al een record bestaat voor **Litware, Inc.** (`https://www.litware.com`), kunt u de volgende procedure, [Een nieuwe ER-configuratieprovider toevoegen](#AddProvider), overslaan.

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Een nieuwe ER-configuratieprovider toevoegen

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.
3. Selecteer **Nieuw** op de pagina **Configuratieproviders**.
4. Voer in het veld **Naam** de tekst **Litware, Inc.** in.
5. Voer in het veld **Internetadres** de tekst `https://www.litware.com` in.
6. Selecteer **Opslaan**.

#### <a name="activate-an-er-configuration-provider"></a>Een ER-configuratieprovider activeren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Litware, Inc.** en selecteer **Instellen als actief**.

Meer informatie over ER-configuratieproviders vindt u in [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>De eerste versies van ER-standaardconfiguraties importeren

Als u de ER-standaardconfiguraties wilt toevoegen aan uw huidige Finance-exemplaar, moet u deze importeren vanuit de ER-[opslagplaats](general-electronic-reporting.md#Repository) die voor dat exemplaar is geconfigureerd.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Microsoft** en selecteer vervolgens **Opslagplaatsen** om de lijst met opslagplaatsen voor de provider Microsoft weer te geven.
3. Selecteer op de pagina **Opslagplaats van configuraties** de opslagplaats van het type **Algemeen** en selecteer vervolgens **Openen**. Als u wordt gevraagd om toestemming te geven om verbinding te maken met de Regulatory Configuration Service, volgt u de instructies voor autorisatie.
4. Selecteer op de pagina **Opslagplaats van configuratie** in de configuratiestructuur in het linkerdeelvenster de indelingsconfiguratie **Peppol-verkoopfactuur**.
5. Selecteer op het sneltabblad **Versies** de versie **11.2.2**.
6. Selecteer **Importeren** om de geselecteerde versie vanuit de algemene opslagplaats te downloaden.

![Configuratie archiefpagina.](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Als u problemen ondervindt met de toegang tot de [globale opslagplaats](er-download-configurations-global-repo.md), kunt u in plaats daarvan [configuraties downloaden](download-electronic-reporting-configuration-lcs.md) van Microsoft Dynamics Lifecycle Services (LCS).

### <a name="review-the-imported-er-configurations"></a>De geïmporteerde ER-configuraties bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.
3. Vouw op de pagina **Configuraties** het sneltabblad **Configuratieonderdelen** uit.
4. Vouw in de configuratiestructuur in het linkerdeelvenster **Factuurmodel** uit en vouw vervolgens **UBL-verkoopfactuur** uit.

Naast de geselecteerde ER-indeling **Peppol-verkoopfactuur** zijn er andere vereiste ER-configuraties geïmporteerd. Omdat nieuwe versies van ER-configuraties steeds worden gepubliceerd naar de algemene opslagplaats en LCS zodat de bijbehorende oplossingen conform nieuwe vereisten blijven, zijn de laatste versies van de vereiste configuraties voor gegevensmodelconfiguratie en de bijbehorende modeltoewijzing geïmporteerd.

![Pagina Configuraties.](./media/er-quick-start3-imported-solution1a.png)

Voer de volgende stappen uit om de status te simuleren die ER-configuraties in het huidige Finance-exemplaar zouden hebben als u versie **11.2.2** van de ER-indeling **Peppol-verkoopfactuur** in het verleden hebt geïmporteerd (bijvoorbeeld op 7 augustus 2019).

- Selecteer in het actievenster de optie **Verwijderen** om alle ER-configuraties te verwijderen die zijn gepubliceerd na 7 augustus 2019. Alleen de configuraties **Factuurmodel**, **Toewijzing factuurmodellen** (heette aanvankelijk **Modeltoewijzing klantfactuur**), **UBL-verkoopfactuur** en **Peppol-verkoopfactuur** moeten overblijven.
- Selecteer voor de resterende configuraties op het sneltabblad **Versies** de optie **Verwijderen** om alle versies van ER-configuraties te verwijderen die na 7 augustus 2019 zijn gepubliceerd.

Controleer vervolgens of de volgende configuraties beschikbaar zijn in de configuratiestructuur:

- Configuratie van ER-gegevensmodel **Factuurmodel** (heette aanvankelijk **Klantfactuurmodel**):

    - Versie 11 bevat versie 10 van het ER-onderdeel gegevensmodel waarmee de gegevensstructuur van het bedrijfsdomein voor facturering wordt vertegenwoordigd. Deze ER-configuratie is geïmporteerd als een voorganger van de ER-indeling **Peppol-verkoopfactuur** die voor import is geselecteerd.
    - Versie 50 bevat versie 31 van het ER-onderdeel van het gegevensmodel. Deze ER-configuratie is geïmporteerd als een voorganger van de versie van 7 augustus 2019 voor de configuratie van ER-modeltoewijzing **Toewijzing factuurmodellen**.

    ![Configuratie van het ER-gegevensmodel voor factuurmodel op de pagina Configuraties.](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Als u versie 50 van dit gegevensmodel niet ziet, opent u de algemene opslagplaats en importeert u versie 50.19 van de ER-configuratie **Toewijzing factuurmodellen**.

- Configuratie van de ER-modeltoewijzing **Toewijzing factuurmodellen** (heette aanvankelijk **Modeltoewijzing klantfactuur**):

    - Versie 50.19 is geïmporteerd als de meest recente implementatie van versie 50 van de configuratie van het ER-gegevensmodel **Factuurmodel**. Het bevat twee ER-onderdelen voor modeltoewijzing waarmee wordt beschreven hoe het gegevensmodel tijdens de uitvoering wordt gevuld met toepassingsgegevens.

    ![Configuratie van het ER-model voor factuurmodeltoewijzing op de pagina Configuraties.](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Als u versie 50.19 van deze modeltoewijzing niet ziet, opent u de algemene opslagplaats en importeert u versie 50.19 van de ER-configuratie **Toewijzing factuurmodellen**.

- Configuratie van ER-indeling **UBL-verkoopfactuur**:

    - Versie 11.2 bevat de ER-onderdelen voor indeling en indelingstoewijzing. Het onderdeel Indeling specificeert de rapportindeling. Het onderdeel voor indelingstoewijzing bevat de modelgegevensbron en geeft aan hoe deze gegevensbron wordt gebruikt om de rapportindeling tijdens de uitvoering in te vullen. Deze ER-indeling is geconfigureerd voor het genereren van e-facturen in UBL-indeling (Universal Business Language). Deze ER-indeling is geïmporteerd als een bovenliggende indeling van de **Peppol-verkoopfactuur** die voor import is geselecteerd.

- Configuratie van ER-indeling **Peppol-verkoopfactuur**:

    - Versie 11.2.2 bevat de ER-onderdelen voor indeling en indelingstoewijzing die zijn geconfigureerd om e-facturen te genereren in PEPPOL-indeling (Pan-European Public Procurement OnLine).

    ![De configuratie van de ER-indeling van Peppol-verkoopfactuur op de pagina Configuraties.](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>De parameters van module Klanten definiëren

1. Ga naar **Klanten** \> **Instellen** \> **Parameters van module Klanten**.
2. Selecteer op het tabblad **Elektronische documenten** op het sneltabblad **Elektronische rapportage** in het veld **Verkoop- en vrije-tekstfactuur** de optie **Peppol-verkoopfactuur**.
3. Selecteer **Opslaan**.

![Tabblad Elektronische documenten op de pagina Parameters van module Klanten.](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>De parameters voor rechtspersonen configureren

1. Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen**.
2. Voer voor het geselecteerde **DEMF**-bedrijf op het sneltabblad **Bankrekeninggegevens** in het veld **Routenummer** **1234** in.
3. Selecteer **Opslaan**.
4. Sluit de pagina **Rechtspersonen**.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Een klantrecord voorbereiden

1. Ga naar **Klanten** \> **Klanten** \> **Alle klanten**.
2. Selecteer op de pagina **Alle klanten** de koppeling van de klantrekening **DE-014**.

### <a name="add-a-customer-contact"></a>Een klantcontactpersoon toevoegen

1. Ga naar **Klanten** \> **Klanten** \> **Alle klanten**.
2. Selecteer in het actievenster op het tabblad **Klant** in de groep **Rekeningen** de optie **Contactpersonen**.
3. Selecteer **Contactpersonen toevoegen**.
4. Open op de pagina **Contactpersonen** in het veld **Voornaam** de zoekopdracht, selecteer **Adam Carter** en selecteer vervolgens **Selecteren** om de zoekopdracht te sluiten.
5. Selecteer **Opslaan**.
6. Sluit de pagina **Contactpersonen**.

### <a name="define-a-primary-contact"></a>Een primaire contactpersoon definiëren

1. Ga naar **Klanten** \> **Klanten** \> **Alle klanten**.
2. Selecteer op het sneltabblad **Demografische verkoopgegevens** in het veld **Primaire contactpersoon** **Adam Carter**.

### <a name="set-the-e-invoicing-option"></a>De optie voor de e-facturering instellen

1. Ga naar **Klanten** \> **Klanten** \> **Alle klanten**.
2. Stel op het sneltabblad **Factuur en levering** de optie **eInvoice** in op **Ja**.
3. Selecteer **Opslaan**.
4. Sluit de pagina **Alle klanten**.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Een klantfactuur verwerken met behulp van ER-standaardconfiguraties

U kunt nu de ER-standaardconfiguraties gebruiken die u elektronisch hebt geïmporteerd om een vrije-tekstfactuur naar een klant te verzenden.

### <a name="add-a-new-invoice"></a>Een nieuwe factuur toevoegen

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Selecteer op de pagina **Vrije-tekstfactuur** **Nieuw**.
3. Selecteer op het sneltabblad **Koptekst vrije-tekstfactuur** in het veld **Klantrekening** **DE-014**.
4. Op het sneltabblad **Factuurregels** wordt automatisch een factuurregel toegevoegd. Stel op deze regel de volgende velden in:

    - Voer in het veld **Beschrijving** **Notebook** in.
    - Selecteer in het veld **Hoofdrekening** **401100**.
    - Voer in het veld **Eenheidsprijs** **1000** in.

5. Selecteer **Opslaan**.

![Pagina Vrije-tekstfactuur.](./media/er-quick-start3-add-invoice.png)

Zie [Een vrije-tekstfactuur maken](../../../finance/accounts-receivable/create-free-text-invoice-new.md) voor meer informatie.

### <a name="post-a-new-invoice"></a>Een nieuwe factuur boeken

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Selecteer op de pagina **Vrije-tekstfactuur** in het actievenster **Boeken**.
3. Selecteer in het dialoogvenster **Vrije-tekstfactuur boeken** **OK**.

![Pagina Details van vrije-tekstfactuur.](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Een geboekte factuur verzenden

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Selecteer op de pagina **Vrije-tekstfactuur** in het actievenster in de groep **Document** de optie **Verzenden** \> **Origineel**.

    ![Voorbeeld van de oorspronkelijke factuur.](./media/er-quick-start3-send-invoice.png)

3. Sluit de pagina **Vrije-tekstfactuur**.

### <a name="analyze-a-generated-e-invoice"></a>Een gegenereerde elektronische factuur analyseren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Elektronische rapportagetaken**.
2. Selecteer op de pagina **Elektronische rapportagetaken** de eerste record met de taakomschrijving **De eInvoice-XML verzenden**.
3. Selecteer **Bestanden weergeven** om toegang te krijgen tot de lijst met gegenereerde bestanden.

    ![Pagina Elektronische rapportagetaken.](./media/er-quick-start3-jobs-list.png)

4. Selecteer **Openen** om het gegenereerde XML-bestand voor elektronische facturen te downloaden.
5. Het XML-bestand van de elektronische factuur analyseren U ziet dat het belastingschema van de klant momenteel wordt vertegenwoordigd door de XML-kenmerken **schemeID** en **schemeAgencyID**. U ziet ook dat het XML-element **cbc:CustomizationID** momenteel de volgende tekst bevat: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` .

    ![Voorbeeld van het gegenereerde XML-bestand van de elektronische factuur.](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Een aangepast databaseveld toevoegen

U kunt de functie [Aangepast veld](../../fin-ops/get-started/user-defined-fields.md) gebruiken om de volgende aanpassing uit te voeren in het huidige Finance-exemplaar:

- Pas de databasestructuur aan door een nieuw aangepast databaseveld toe te voegen waarin een code voor nationale belasting-ID voor elke klant wordt opgeslagen.
- Pas de pagina **Klant** aan door een nieuw gegevensinvoerveld toe te voegen dat kan worden gebruikt om een belastingcodewaarde in te voeren in het nieuwe aangepaste databaseveld.

Voer de volgende stappen uit om de aanpassing uit te voeren.

1. Ga naar **Klanten** \> **Klanten** \> **Alle klanten**.
2. Selecteer op de pagina **Alle klanten** de koppeling van de klantrekening **DE-014**.
3. Klik op het sneltabblad **Algemeen** met de rechtermuisknop in een leeg gebied onder het veld **Taal** en selecteer **Aanpassen: UpperGroup**.

    De inhoud van het sneltabblad **Algemeen** wordt gemarkeerd en het menu **Aanpassen** wordt weergegeven.

4. Selecteer in het menu **Aanpassen** **Een veld toevoegen**.
5. Selecteer in het dialoogvenster **Kolommen toevoegen** **Een nieuw veld maken**.
6. Selecteer in het dialoogvenster **Nieuw veld maken** in het veld **Tabelnaam** de optie **Klanten**.
7. Voer in het veld **Naamvoorvoegsel** de waarde **FederalTaxID** in.

    > [!NOTE]
    > De gehele veldnaam is automatisch gedefinieerd als **FederalTaxID\_Aangepast**.

8. Voer in het veld **Label** **Nationale belasting-ID** in.
9. Selecteer in het veld **Type** **Tekst**.
10. Voer in het veld **Lengte** **20** in.
11. Selecteer **Opslaan**.
12. Selecteer in het berichtvak dat verschijnt **Ja** om te bevestigen dat u een nieuwe **FederalTaxID** wilt maken voor de tabel **Klanten**.
13. Selecteer **Invoegen** om <a name="insert_custom_field"></a>het veld **FederalTaxID\_Aangepast** toe te voegen aan de huidige pagina.

    ![Pagina Alle klanten.](./media/er-quick-start3-create-new-field.gif)

14. Sluit de pagina **Alle klanten**.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>De ER-metagegevens vernieuwen

U moet de ER-metagegevens vernieuwen om het aangepaste veld dat u hebt toegevoegd [zichtbaar](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) te maken in de ontwerper voor toewijzing van ER-modellen.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Tabelverwijzingen opnieuw maken**.
2. Selecteer in het dialoogvenster **Gegevensmodel bijwerken** **OK**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>De aangepaste ER-configuraties ontwerpen

U kunt de door Microsoft geleverde ER-configuraties gebruiken om uw aangepaste ER-configuraties te ontwerpen zodat er elektronische facturen mee worden gegenereerd die de nieuwe belastingcode bevatten.

### <a name="customize-the-data-model-configuration"></a>De gegevensmodelconfiguratie aanpassen

Als gebruiker met de rol Functioneel consultant van elektronische rapportage kunt u uw aangepaste ER-gegevensmodel ontwerpen.

#### <a name="add-a-custom-data-model-configuration"></a>Een aangepaste gegevensmodelconfiguratie toevoegen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Klantfactuurmodel**.
3. Selecteer **Configuratie maken** in het actievenster.
4. Selecteer in het volgende dialoogvenster in het veld **Nieuw** **Afleiden van naam: Klantfactuurmodel, Microsoft** om aan te geven dat uw nieuwe aangepaste ER-gegevensmodelconfiguratie moet worden gebaseerd op de configuratie van het ER-gegevensmodel.
5. Voer in het veld **Naam** **Factuurmodel (Litware)** in.
6. Selecteer **Configuratie maken** om de nieuwe ER-configuratie toe te voegen.

U kunt nu de ER-gegevensmodelontwerper gebruiken om versie 50.1 van de ER-configuratie **Factuurmodel (Litware)** in de status **Concept**-[status](general-electronic-reporting.md#component-versioning) te bewerken.

![Versie 50.1 van de ER-configuratie op de pagina Configuraties.](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Een aangepast gegevensmodel configureren

U moet uw aangepaste gegevensmodel wijzigen door een nieuw veld toe te voegen om de waarde van een nationale belasting-ID-code op te geven. Deze code maakt deel uit van de klantgegevens voor elke ER-indeling waarvoor dit gegevensmodel als gegevensbron wordt gebruikt.

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Factuurmodel (Litware)**.
2. Selecteer op het sneltabblad **Versies** versie **50.1** van de geselecteerde ER-gegevensmodelconfiguratie in de status **Concept**.
3. Selecteer in het actievenster **Ontwerper** voor de geselecteerde configuratieversie.
4. Selecteer **Klantgegevens (klant)** in de gegevensmodelstructuur van de pagina **Gegevensmodel ontwerpen**.
5. Selecteer **Nieuw**.
6. Accepteer in het volgende dialoogvenster in het veld **Nieuw knooppunt als een** de standaardwaarde **Onderliggende waarde van een actief knooppunt**.
7. Voer in het veld **Naam** **FederalTaxID\_Litware** in.
8. Accepteer in het veld **Itemtype** de standaardwaarde **Tekenreeks**.
9. Selecteer **Toevoegen** en vervolgens **Opslaan**.

    ![Pagina Gegevensmodel ontwerpen.](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > In de velden **Label** en **Omschrijving** wordt het doel van het nieuwe veld beschreven. U kunt deze velden in meerdere talen invullen. Zie [Meertalige rapporten ontwerpen in elektronische rapportage](er-design-multilingual-reports.md) voor meer informatie.

10. Sluit de pagina **Gegevensmodel ontwerpen**.

#### <a name="complete-a-custom-data-model-configuration"></a>Een aangepaste gegevensmodelconfiguratie uitvoeren

U moet uw werk [voltooien](general-electronic-reporting.md#component-versioning) met versie 50.1 van uw aangepaste ER-gegevensmodelconfiguratie om deze beschikbaar te maken zodat andere aangepaste ER-configuraties kunnen worden toegevoegd.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Factuurmodel** uit en selecteer **Factuurmodel (Litware)**.
3. Selecteer op het sneltabblad **Versies** de optie **Status wijzigen** \> **Voltooien** en selecteer vervolgens **OK**.

De status van versie 50.1 wordt gewijzigd van **Concept** in **Voltooid** en de versie wordt alleen-lezen. Er is een nieuwe bewerkbare versie, 50.2, toegevoegd en deze heeft de status **Concept**. U kunt deze versie gebruiken om verdere wijzigingen aan te brengen in uw aangepaste ER-gegevensmodelconfiguratie.

![Versie 50.1 voltooid op de pagina Configuraties.](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>De modeltoewijzingsconfiguratie aanpassen

Als gebruiker met de rol Ontwikkelaar van elektronische rapportage kunt u uw aangepaste ER-modeltoewijzing ontwerpen.

#### <a name="add-a-custom-model-mapping-configuration"></a>Een configuratie voor aangepaste modeltoewijzing toevoegen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Klantfactuurmodel** uit en selecteer **Toewijzing klantfactuurmodel**.
3. Selecteer **Configuratie maken** in het actievenster.
4. Selecteer in het volgende dialoogvenster in het veld **Nieuw** **Afleiden van naam: Toewijzing klantfactuurmodel, Microsoft** om aan te geven dat uw nieuwe configuratie voor aangepaste ER-modeltoewijzing moet worden gebaseerd op de configuratie van de ER-modeltoewijzing.
5. Voer in het veld **Naam** **Toewijzing factuurmodel (Litware)** in.
6. Selecteer **Factuurmodel (Litware)** in het veld **Doelmodel**.

    > [!IMPORTANT]
    > Deze stap is erg belangrijk. Als u deze stap overslaat, kunt u uw aangepaste gegevensmodel niet gebruiken in de geconfigureerde modeltoewijzing.

7. Selecteer **Configuratie maken** om de nieuwe ER-configuratie toe te voegen.

![Een configuratie van de aangepaste modeltoewijzing op de pagina Configuraties toevoegen.](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Een aangepaste modeltoewijzing configureren

U moet uw aangepaste modeltoewijzing aanpassen en opgeven hoe toepassingsgegevens in het aangepaste veld **FederalTaxID\_Litware** van het aangepaste gegevensmodel tijdens de uitvoering moeten worden ingevuld.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Klantfactuurmodel** \> **Toewijzing klantfactuurmodel** uit en selecteer **Toewijzing factuurmodel (Litware)**.
3. Selecteer **Ontwerper** in het actievenster.
4. Selecteer de toewijzing **Klantfactuur** op de pagina **Model voor gegevensbrontoewijzing**.

    ![Pagina Model voor gegevensbrontoewijzing.](./media/er-quick-start3-select-customer-mapping.png)

5. Selecteer **Ontwerper**.
6. Vouw op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensbronnen** de gegevensbron **CustInvoiceJour** waarmee de toepassingstabel **CustInvoiceJour** wordt vertegenwoordigd.
7. Vouw onder **CustInvoiceJour** **Relaties** uit om de lijst met relaties van het type veel-op-één (N:1) voor de tabel **CustInvoiceJour** te controleren.
8. Vouw onder **CustInvoiceJour** \> **Relaties** **Klanten (CustTable)** uit om toegang te krijgen tot de velden en relaties van de tabel **Klanten (CustTable)**.
9. Selecteer het gegevensbronveld **FederalTaxID\_Aangepast** dat u [eerder](#insert_custom_field) hebt geïmplementeerd.
10. Vouw in het deelvenster **Gegevensmodel** **Klantgegevens (klant)** uit en selecteer het gegevensmodelveld **FederalTaxID\_Litware**.
11. Selecteer **Binden**.

    ![Pagina voor ontwerper van modeltoewijzingen.](./media/er-quick-start3-customize-model-mapping.gif)

12. Selecteer **Opslaan**.
13. Sluit de pagina **Ontwerper modeltoewijzing**.
14. Sluit de pagina **Model aan gegevensbrontoewijzing**.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Een aangepaste modeltoewijzingsconfiguratie uitvoeren

U moet uw werk [uitvoeren](general-electronic-reporting.md#component-versioning) met versie 50.19.1 van uw configuratie van de aangepaste ER-modeltoewijzing om deze beschikbaar te maken voor gebruik.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Klantfactuurmodel** \> **Toewijzing klantfactuurmodel** uit en selecteer **Toewijzing factuurmodel (Litware)**.
3. Selecteer op het sneltabblad **Versies** de optie **Status wijzigen** \> **Voltooien** en selecteer vervolgens **OK**.

De status van versie 50.19.1 wordt gewijzigd van **Concept** in **Voltooid** en de versie wordt alleen-lezen. Er is een nieuwe bewerkbare versie, 50.19.2, toegevoegd en deze heeft de status **Concept**. U kunt deze versie gebruiken om verdere wijzigingen aan te brengen in uw aangepaste ER-modeltoewijzingsconfiguratie.

![Versie 50.19.1 voltooid op de pagina Configuraties.](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> De ondersteunde [levenscyclus](general-electronic-reporting-manage-configuration-lifecycle.md) van de configuratie dekt niet de levenscyclus van databasewijzigingen. Als u versie 50.19.1 van de configuratie **Factuurmodeltoewijzing (Litware)** vanuit het huidige Finance-exemplaar exporteert en het in een ander exemplaar probeert te importeren dat niet het aangepaste veld **FederalTaxID\_Aangepast** in de tabel **CustTable** bevat, treedt er een uitzondering op. De uitzondering geeft aan dat de geïmporteerde ER-configuratie niet compatibel is met de metagegevens van het Finance-doelexemplaar.

### <a name="customize-the-format-configuration"></a>De indelingsconfiguratie aanpassen

Als gebruiker met de rol Functioneel consultant van elektronische rapportage kunt u uw aangepaste ER-indeling ontwerpen.

#### <a name="add-a-custom-format-configuration"></a>Een aangepaste indelingsconfiguratie toevoegen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Klantfactuurmodel** \> **UBL-verkoopfactuur** uit en selecteer **Peppol-verkoopfactuur**.
3. Selecteer **Configuratie maken** in het actievenster.
4. Selecteer in het volgende dialoogvenster in het veld **Nieuw** **Afleiden van naam: Peppol-verkoopfactuur, Microsoft** om aan te geven dat uw aangepaste ER-indelingsconfiguratie moet worden gebaseerd op de configuratie van de ER-indeling.
5. Voer in het veld **Naam** **Peppol-verkoopfactuur (Litware)** in.
6. Selecteer **Factuurmodel (Litware)** in het veld **Gegevensmodel** om de onderdelen van uw aangepaste gegevensmodel en modeltoewijzing te gebruiken.

    > [!NOTE]
    > Deze stap is erg belangrijk. Als u deze stap overslaat, kunt u uw aangepaste gegevensmodel niet gebruiken in de geconfigureerde indeling.

7. Selecteer in het veld **Gegevensmodel** de basisdefinitie **InvoiceCustomer**.
8. Selecteer **Configuratie maken** om de nieuwe ER-configuratie toe te voegen.

![Een configuratie van een aangepaste indeling op de pagina Configuraties toevoegen.](./media/er-quick-start3-adding-custom-format.png)

U kunt nu de ER Operations-ontwerper gebruiken om versie 11.2.2.1 van de ER-configuratie **Peppol-verkoopfactuur (Litware)** in de status **Concept**-[status](general-electronic-reporting.md#component-versioning) te bewerken.

![Versie 11.2.2.1 van de ER-configuratie op de pagina Configuraties.](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Een aangepaste indeling configureren

U moet uw aangepaste indeling wijzigen door een nieuw opmaakelement toe te voegen om de waarde van de nationale belasting-ID van een gefactureerde klant in te vullen.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Klantfactuurmodel** \> **UBL-verkoopfactuur** \> **Peppol-verkoopfactuur** uit en selecteer **Peppol-verkoopfactuur (Litware)**.
3. Selecteer **Ontwerper** in het actievenster.
4. Vouw in de indelingsstructuur **XMLHeader** \> **Invoice** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** uit en selecteer **cbc:ID**.
5. Selecteer **Toevoegen** en vervolgens **XML** \> **Kenmerk**.
6. Voer **FederalTaxID** in het dialoogvenster **Onderdeeleigenschap** in het veld **Naam** in.
7. Selecteer **OK** om een nieuw indelingselement toe te voegen om een nieuw XML-kenmerk voor **FederalTaxID** te maken in een gegenereerd XML-bestand.
8. Selecteer in de indelingsstructuur **FederalTaxID** onder **XMLHeader** \> **Factuur** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID**.
9. Selecteer **Omhoog verplaatsen**.

![Nieuw indelingselement op de pagina Indelingsontwerper.](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Een aangepaste indelingstoewijzing configureren

1. Vouw op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** de gegevensbron **Factuur** van het type **Model** uit.
2. Vouw onder **Factuur** **Klantgegevens (klant)** uit en selecteer **FederalTaxID\_Litware**.
3. Selecteer **Binden**.

    ![Pagina Indelingsontwerper.](./media/er-quick-start3-customized-format-mapping.png)

4. Selecteer de gegevensbron **Factuur** van het type **Model** en selecteer vervolgens **Bewerken**.
5. Selecteer in het veld **Versie** **1** van uw aangepaste gegevensmodel en selecteer vervolgens **OK**.
6. Selecteer **Opslaan**.
7. Sluit de pagina **Indelingsontwerper**.

#### <a name="complete-a-custom-format-configuration"></a>Een aangepaste indelingsconfiguratie voltooien

U moet uw werk [uitvoeren](general-electronic-reporting.md#component-versioning) met versie 11.2.2.1 van uw configuratie van de aangepaste ER-indeling om deze beschikbaar te maken voor gebruik.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Klantfactuurmodel** \> **UBL-verkoopfactuur** \> **Peppol-verkoopfactuur** uit en selecteer **Peppol-verkoopfactuur (Litware)**.
3. Selecteer op het sneltabblad **Versies** de optie **Status wijzigen** \> **Voltooien** en selecteer vervolgens **OK**.

De status van versie 11.2.2.1 wordt gewijzigd van **Concept** in **Voltooid** en de versie wordt alleen-lezen. Er is een nieuwe bewerkbare versie, 11.2.2.2, toegevoegd en deze heeft de status **Concept**. U kunt deze versie gebruiken om verdere wijzigingen aan te brengen in uw aangepaste ER-indelingsconfiguratie.

![Versie 11.2.2.1 voltooid op de pagina Configuraties.](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Configureer de parameters van de module Klanten om aangepaste ER-configuraties te gaan gebruiken.

1. Ga naar **Klanten** \> **Instellen** \> **Parameters van module Klanten**.
2. Selecteer op het tabblad **Elektronische documenten** op het sneltabblad **Elektronische rapportage** in het veld **Verkoop- en vrije-tekstfactuur** de optie **Peppol-verkoopfactuur (Litware)**.
3. Selecteer **Opslaan**.

![Tabblad Elektronische documenten op de pagina Parameters van module Klanten, sneltabblad Elektronische rapportage.](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Een klantrecord bijwerken door een code voor nationale belasting-ID toe te voegen

1. Ga naar **Klanten** \> **Klanten** \> **Alle klanten**.
2. Selecteer op de pagina **Alle klanten** de koppeling van de klantrekening **DE-014**.
3. Voer **LITWARE-6789** op sneltabblad **Algemeen** in het veld **Nationale belasting-ID** in.
4. Selecteer **Opslaan**.

    ![Pagina met details van klant DE-014.](./media/er-quick-start3-added-tax-id-value.png)

5. Sluit de pagina **Alle klanten**.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Een klantfactuur verwerken met behulp van aangepaste ER-configuraties.

### <a name="select-and-send-a-posted-invoice"></a>Een geboekte factuur selecteren en verzenden

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Selecteer op de pagina **Vrije-tekstfactuur** de factuur die u eerder hebt toegevoegd en geboekt.
3. Selecteer in het actievenster in de groep **Document** **Verzenden** \> **Origineel**.
4. Sluit de pagina **Vrije-tekstfactuur**.

### <a name="analyze-a-generated-e-invoice"></a>Een gegenereerde elektronische factuur analyseren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Elektronische rapportagetaken**.
2. Selecteer op de pagina **Elektronische rapportagetaken** de laatste record met de taakomschrijving **De eInvoice-XML verzenden**.
3. Selecteer **Bestanden weergeven** om toegang te krijgen tot de lijst met gegenereerde bestanden.
4. Selecteer **Openen** om het gegenereerde XML-bestand voor elektronische facturen te downloaden.
5. Het XML-bestand van de elektronische factuur analyseren In overeenstemming met uw aanpassing bevat het belastingschema van de klant naast de XML-kenmerken **schemeID** en **schemeAgencyID** ook het aangepaste XML-kenmerk **FederalTaxID**. De waarde van dit nieuwe XML-kenmerk wordt opgegeven door de nationale belasting-ID **LITWARE-6789** die voor een gefactureerde klant is ingevoerd.

    ![Voorbeeld van het gegenereerde XML-bestand van de elektronische factuur met uw aanpassingen.](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>De laatste versies van ER-standaardconfiguraties importeren

Als u de set ER-standaardconfiguraties in uw Finance-exemplaar [up-to-date](general-electronic-reporting-manage-configuration-lifecycle.md) wilt houden, moet u nieuwe versies van deze configuraties importeren wanneer deze beschikbaar komen in de ER-[opslagplaats](general-electronic-reporting.md#Repository) die voor dat exemplaar is geconfigureerd.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Microsoft** en selecteer vervolgens **Opslagplaatsen** om de lijst met opslagplaatsen voor de provider Microsoft weer te geven.
3. Selecteer op de pagina **Opslagplaats van configuraties** de opslagplaats van het type **Algemeen** en selecteer vervolgens **Openen**. Als u wordt gevraagd om toestemming te geven om verbinding te maken met de Regulatory Configuration Service, volgt u de instructies voor autorisatie.
4. Selecteer op de pagina **Opslagplaats van configuratie** in de configuratiestructuur in het linkerdeelvenster de indelingsconfiguratie **Peppol-verkoopfactuur**.
5. Selecteer op het sneltabblad **Versies** versie **32.6.7** van de geselecteerde ER-indelingsconfiguratie die is uitgegeven ter ondersteuning van elektronische facturen voor klanten in de indeling PEPPOL BIS 3. Zie [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic) voor meer informatie.
6. Selecteer **Importeren** om de geselecteerde versie vanuit de algemene opslagplaats te downloaden naar het huidige Finance-exemplaar.

![Versie 32.6.7 geselecteerd op de pagina Opslagplaats configuratie.](./media/er-quick-start3-import-solution2.png)

Zie [Bijgewerkte versies van ER-configuraties importeren](er-download-updated-versions-global-repo.md) voor informatie over hoe dit proces kan worden geautomatiseerd.

### <a name="review-the-imported-er-configurations"></a>De geïmporteerde ER-configuraties bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.
3. Vouw het sneltabblad **Configuratieonderdelen** uit.
4. Vouw in de configuratiestructuur in het linkerdeelvenster **Factuurmodel** uit. U ziet dat de naam van **Klantfactuurmodel** is gewijzigd in **Factuurmodel** in een van de geïmporteerde ER-gegevensmodelconfiguraties.
5. Vouw in de configuratiestructuur in het linkerdeelvenster **Factuurmodeltoewijzing** uit. U ziet dat de naam van **Toewijzing klantfactuurmodel** is gewijzigd in **Toewijzing factuurmodel** in een van de geïmporteerde ER-modeltoewijzingsconfiguraties.
6. Vouw **UBL-verkoopfactuur** \> **Peppol-verkoopfactuur** uit.

Naast de geselecteerde ER-indeling **Peppol-verkoopfactuur** zijn de laatste versies van andere vereiste ER-configuraties geïmporteerd. Omdat nieuwe versies van ER-configuraties steeds worden gepubliceerd naar de algemene opslagplaats en LCS zodat de bijbehorende ER-oplossingen conform nieuwe vereisten blijven, zijn de laatste versies van de vereiste gegevensmodelconfiguratie en de bijbehorende modeltoewijzingsconfiguraties geïmporteerd.

Zorg ervoor dat de volgende ER-configuraties uiteindelijk beschikbaar zijn in de configuratiestructuur:

- ER-gegevensmodelconfiguratie **Factuurmodel**:

    - Versie 206 (of later) bevat versie 24 (of later) van het ER-onderdeel voor gegevensmodel waarmee de gegevensstructuur van het bedrijfsdomein voor facturering wordt vertegenwoordigd. Deze ER-configuratie is geïmporteerd als een voorganger van de laatst beschikbare configuratie van ER-modeltoewijzing **Toewijzing factuurmodel**.

    ![Versie 206 op de pagina Configuraties.](./media/er-quick-start3-imported-solution2b1.png)

- ER-gegevensmodelconfiguratie **Toewijzing factuurmodel**:

    - Versie 206.132 (of later) is geïmporteerd als de meest recente implementatie van versie 206 van de configuratie van het ER-gegevensmodel **Factuurmodel**. Het bevat verschillende ER-onderdelen voor modeltoewijzing waarmee wordt beschreven hoe het gegevensmodel tijdens de uitvoering wordt gevuld met toepassingsgegevens.

    ![Versie 206.132 op de pagina Configuraties.](./media/er-quick-start3-imported-solution2b2.png)

- Configuratie van ER-indeling **UBL-verkoopfactuur**:

    - Versie 32.6 bevat de ER-onderdelen voor indeling en indelingstoewijzing. Het onderdeel Indeling specificeert de rapportindeling. Het onderdeel voor indelingstoewijzing bevat de modelgegevensbron en geeft aan hoe deze gegevensbron wordt gebruikt om de rapportindeling tijdens de uitvoering in te vullen. Deze ER-indeling is geconfigureerd voor het genereren van e-facturen in UBL-indeling. Deze ER-indeling is geïmporteerd als een bovenliggende indeling van de **Peppol-verkoopfactuur** die voor import is geselecteerd.

- Configuratie van ER-indeling **Peppol-verkoopfactuur**:

    - Versie 32.6.7 bevat de ER-onderdelen voor indeling en indelingstoewijzing die zijn geconfigureerd om e-facturen te genereren in PEPPOL-indeling.

    ![Versie 32.6.7 op de pagina Configuraties.](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>De wijzigingen in de nieuwe versies van de ER-standaardconfiguraties opnemen in uw aangepaste ER-configuraties

### <a name="adopt-your-custom-er-data-model"></a>Uw aangepaste ER-gegevensmodel opnemen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Factuurmodel** uit en selecteer **Factuurmodel (Litware)**.
3. Selecteer **Rebase** op het sneltabblad **Versies** voor conceptversie **50.2** van de geselecteerde gegevensmodelconfiguratie.
4. Bevestig in het veld **Doelversie** de selectie van versie **206** van de basisconfiguratie van het ER-gegevensmodel en selecteer vervolgens **OK**.

    Het nummer van de conceptversie van uw aangepaste ER-gegevensmodelconfiguratie wordt gewijzigd van **50.2** in **206.2** om aan te geven dat deze nu uw aanpassing bevat die is samengevoegd met de wijzigingen in de meest recente versie (206) van de basisconfiguratie van het ER-gegevensmodel.

    > [!NOTE]
    > De rebase-actie kan ongedaan worden gemaakt. Als u deze rebase wilt annuleren, selecteert u versie **50.1** van het model **Factuurmodel (Litware)** op het sneltabblad **Versies** en selecteert u **Deze versie ophalen**. Versie 206.2 krijgt dan weer het nummer **50.2** en de inhoud van conceptversie 50.2 komt weer overeen met de inhoud van versie 50.1.

5. Selecteer op het sneltabblad **Versies** de optie **Status wijzigen** \> **Voltooien** en selecteer vervolgens **OK**.

De status van versie 206.2 wordt gewijzigd van **Concept** in **Voltooid** en de versie wordt alleen-lezen. Er is een nieuwe bewerkbare versie, 206.3, toegevoegd en deze heeft de status **Concept**. U kunt deze versie gebruiken om verdere wijzigingen aan te brengen in uw aangepaste ER-gegevensmodelconfiguratie.

![Versie 206.2 voltooid op de pagina Configuraties.](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Uw aangepaste ER-modeltoewijzing opnemen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Factuurmodel** \> **Toewijzing factuurmodel** uit en selecteer **Toewijzing factuurmodel (Litware)**.
3. Selecteer **Rebase** op het sneltabblad **Versies** voor conceptversie **50.19.2** van de geselecteerde modeltoewijzingsconfiguratie.
4. Bevestig in het veld **Doelversie** de selectie van versie **206.132** van de basisconfiguratie van de ER-modeltoewijzing en selecteer vervolgens **OK**.

    Het nummer van de conceptversie van uw aangepaste ER-modeltoewijzingsconfiguratie wordt gewijzigd van **50.19.2** in **206.132.2** om aan te geven dat deze nu uw aanpassing bevat die is samengevoegd met de wijzigingen in de meest recente versie (206.132) van de basisconfiguratie van de ER-modeltoewijzing.

    U ziet dat er een aantal rebaseconflicten is ontdekt. U moet deze conflicten nu handmatig oplossen.

    ![Bericht over rebaseconflicten op de pagina Configuraties.](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Selecteer **Ontwerper** in het actievenster en selecteer vervolgens **Klantfactuur** in de lijst met toewijzingen.
6. Selecteer voor elk rebaseconflict **Eigen waarde behouden**, omdat u voor elk onderdeel dat is vermeld het versienummer van uw aangepaste gegevensmodel moet behouden.

    ![Rebaseconflicten op de pagina Ontwerper modeltoewijzing.](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Selecteer **Opslaan** en sluit de pagina **Ontwerper modeltoewijzing**.
8. Selecteer **Projectfactuur** in de lijst met toewijzingen.
9. Selecteer voor elk rebaseconflict **Eigen waarde behouden**, omdat u voor elk onderdeel dat is vermeld het versienummer van uw aangepaste gegevensmodel moet behouden.
10. Selecteer **Opslaan** en sluit de pagina **Modeltoewijzingen**.

    > [!NOTE]
    > De rebase-actie kan ongedaan worden gemaakt. Als u deze rebase wilt annuleren, selecteert u versie **50.19.1** van de modeltoewijzing **Toewijzing factuurmodel (Litware)** op het sneltabblad **Versies** en selecteert u **Deze versie ophalen**. Versie 206.132.2 krijgt dan weer het nummer **50.19.2** en de inhoud van conceptversie 50.19.2 komt weer overeen met de inhoud van versie 50.19.1.

11. Selecteer op het sneltabblad **Versies** de optie **Status wijzigen** \> **Voltooien** en selecteer vervolgens **OK**.

De status van versie 206.132.2 wordt gewijzigd van **Concept** in **Voltooid** en de versie wordt alleen-lezen. Er is een nieuwe bewerkbare versie, 206.132.3, toegevoegd en deze heeft de status **Concept**. U kunt deze versie gebruiken om verdere wijzigingen aan te brengen in uw aangepaste ER-modeltoewijzingsconfiguratie.

![Versie 206.132.2 voltooid op de pagina Configuraties.](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Uw aangepaste ER-indeling opnemen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Factuurmodel** \> **UBL-verkoopfactuur** \> **Peppol-verkoopfactuur** uit en selecteer **Peppol-verkoopfactuur (Litware)**.
3. Selecteer **Rebase** op het sneltabblad **Versies** voor conceptversie **11.2.2.2** van de geselecteerde indelingsconfiguratie.
4. Bevestig in het veld **Doelversie** de selectie van versie **32.6.7** van de basisconfiguratie van de ER-indeling en selecteer vervolgens **OK**.

    Het nummer van de conceptversie van uw aangepaste ER-indelingsconfiguratie wordt gewijzigd van **11.2.2.2** in **32.6.7.2** om aan te geven dat deze nu uw aanpassing bevat die is samengevoegd met de wijzigingen in de meest recente versie (32.6.7) van de basisconfiguratie van de ER-indeling.

    U ziet dat er een aantal rebaseconflicten is ontdekt. U moet deze conflicten nu handmatig oplossen.

5. Selecteer **Ontwerper** in het actievenster.
6. Selecteer voor elk rebaseconflict **Eigen waarde behouden**, omdat u voor elk onderdeel dat is vermeld het versienummer van uw aangepaste gegevensmodel moet behouden.
7. Selecteer **Opslaan**.
8. Selecteer de gegevensbron **Factuur** van het type **Model** op het tabblad **Toewijzing** en selecteer vervolgens **Bewerken**.
9. Selecteer in het veld **Versie** **2** van uw aangepaste gegevensmodel en selecteer vervolgens **OK**.
10. Selecteer **Opslaan**.

    > [!NOTE]
    > De rebase-actie kan ongedaan worden gemaakt. Als u deze rebase wilt annuleren, selecteert u versie **11.2.2.1** van de indeling **Peppol-verkoopfactuur (Litware)** op het sneltabblad **Versies** en selecteert u **Deze versie ophalen**. Versie 32.6.7.2 krijgt dan weer het nummer **11.2.2.2** en de inhoud van conceptversie 11.2.2.2 komt weer overeen met de inhoud van versie 11.2.2.1.

11. Sluit de pagina **Indelingsontwerper**.
12. Selecteer op het sneltabblad **Versies** de optie **Status wijzigen** \> **Voltooien** en selecteer vervolgens **OK**.

De status van versie 32.6.7.2 wordt gewijzigd van **Concept** in **Voltooid** en de versie wordt alleen-lezen. Er is een nieuwe bewerkbare versie, 32.6.7.3, toegevoegd en deze heeft de status **Concept**. U kunt deze versie gebruiken om verdere wijzigingen aan te brengen in uw aangepaste ER-indelingsconfiguratie.

![Versie 32.6.7.2 voltooid op de pagina Configuraties.](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Een klantfactuur verwerken met behulp van nieuwe versies van de aangepaste ER-configuraties

### <a name="select-and-send-a-posted-invoice"></a>Een geboekte factuur selecteren en verzenden

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Selecteer op de pagina **Vrije-tekstfactuur** de factuur die u eerder hebt toegevoegd en geboekt.
3. Selecteer in het actievenster in de groep **Document** **Verzenden** \> **Origineel**.

    > [!NOTE] 
    > Omdat u nu twee versies hebt van de ER-indelingsconfiguratie **Peppol-verkoopfactuur (Litware)** en geen van de versies een waarde voor [ingangsdatum](general-electronic-reporting.md#component-date-effectivity) heeft, wordt de laatste versie gebruikt om een elektronische factuur te genereren.

4. Sluit de pagina **Vrije-tekstfactuur**.

### <a name="analyze-a-generated-e-invoice"></a>Een gegenereerde elektronische factuur analyseren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Elektronische rapportagetaken**.
2. Selecteer op de pagina **Elektronische rapportagetaken** de meest recente record met de taakomschrijving **De eInvoice-XML verzenden**.
3. Selecteer **Bestanden weergeven** om toegang te krijgen tot de lijst met gegenereerde bestanden.
4. Selecteer **Openen** om het gegenereerde XML-bestand voor elektronische facturen te downloaden.
5. Het XML-bestand van de elektronische factuur analyseren In overeenstemming met uw aanpassing bevat het belastingschema van de klant nog steeds naast de XML-kenmerken **schemeID** en **schemeAgencyID** ook het aangepaste XML-kenmerk **FederalTaxID**. Omdat de wijzigingen in de nieuwe versie van de basisindeling **UBL-verkoopfactuur** met uw aanpassing zijn samengevoegd, is de tekst van het XML-element **cbc: CustomizationID** gewijzigd van `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` in `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.

    ![Voorbeeld van het gegenereerde XML-bestand van de elektronische factuur met aanpassingen.](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [ER-configuraties downloaden uit Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice](er-download-configurations-global-repo.md)
- [Een vrije-tekstfactuur invoeren](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [Maken en werken met aangepaste velden](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

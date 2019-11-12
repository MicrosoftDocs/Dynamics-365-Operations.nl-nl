---
title: Overzicht van Beheer van bedrijfsdocumenten
description: Dit onderwerp biedt informatie over het gebruiken van de functie Beheer van bedrijfsdocumenten van het ER-raamwerk.
author: NickSelin
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 05dee1efc4e817795824e3fa1c41093d48a97d78
ms.sourcegitcommit: 219a73371638a9a4c6076d4c88b95fb2ebe95b00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2019
ms.locfileid: "2652612"
---
# <a name="business-document-management-overview"></a>Overzicht van Beheer van bedrijfsdocumenten

Zakelijke gebruikers gebruiken het [ER-raamwerk (elektronische rapportage)](general-electronic-reporting.md) om indelingen voor uitgaande documenten te configureren in overeenstemming met de wettelijke voorschriften van verschillende landen/regio's. Gebruikers kunnen ook de gegevensstroom definiëren om op te geven welke toepassingsgegevens in gegenereerde documenten worden geplaatst. Het ER-raamwerk genereert uitgaande documenten in Microsoft Office-indelingen (Excel-werkmappen of Word-documenten) met behulp van vooraf gedefinieerde sjablonen. De sjablonen worden gevuld met vereiste gegevens in overeenstemming met de geconfigureerde gegevensstroom wanneer vereiste documenten worden gegenereerd. Elke geconfigureerde indeling kan als onderdeel van een ER-oplossing worden gepubliceerd om specifieke uitgaande documenten te genereren. Dit wordt weergegeven in een configuratie met de ER-indeling die sjablonen kan bevatten die u kunt gebruiken om verschillende uitgaande documenten te genereren. Zakelijke gebruikers kunnen dit raamwerk gebruiken om vereiste bedrijfsdocumenten te beheren.

**Beheer van bedrijfsdocumenten** is gebaseerd op het ER-raamwerk en stelt zakelijke gebruikers in staat zakelijke documentsjablonen te bewerken met de Microsoft Office 365-service of de toepasselijke Microsoft Office-bureaubladtoepassing. Wijzigingen in de documenten kunnen betrekking hebben op het wijzigen in het ontwerp van bedrijfsdocumenten en het toevoegen van tijdelijke aanduidingen voor extra gegevens zonder wijzigingen in broncode en nieuwe implementaties. Er is geen kennis van het ER-raamwerk nodig om sjablonen van bedrijfsdocumenten bij te werken.

> [!NOTE]
> Houd er rekening mee dat u met Beheer van bedrijfsdocumenten sjablonen kunt wijzigen die worden gebruikt om bedrijfsdocumenten te produceren, zoals orders, facturen, enzovoort. Als een sjabloon is gewijzigd en er een nieuwe versie is gepubliceerd, wordt deze versie gebruikt om vereiste bedrijfsdocumenten te genereren. Beheer van bedrijfsdocumenten kan niet worden gebruikt om reeds gegenereerde bedrijfsdocumenten te wijzigen.

## <a name="supported-deployments"></a>Ondersteunde implementaties

Momenteel is de functie Beheer van bedrijfsdocumenten alleen geïmplementeerd voor cloudimplementaties. Als deze functie belangrijk is voor uw on-premises implementatie, laat u ons dat weten door feedback achter te laten op de site [Ideeën](https://experience.dynamics.com/ideas/).

## <a name="supported-microsoft-office-applications"></a>Ondersteunde Microsoft Office-toepassingen

Als u Beheer van bedrijfsdocumenten wilt gebruiken voor het bewerken van sjablonen in Excel- of Word-indelingen met Microsoft Office-bureaubladtoepassingen, moet Microsoft Office 2010 of hoger zijn geïnstalleerd. Dit wordt ondersteund in cloud- en on-premises implementaties.

## <a name="business-document-availability"></a>Beschikbaarheid van bedrijfsdocumenten

De volgende rapporten met Excel-sjablonen zijn beschikbaar in de release van de openbare preview:

**Klanten** (augustus 2019)

- Voorschotfactuur verkoop
- Pakbon verkooporder

**Leveranciers** (augustus 2019)

- Voorschotfactuur inkoop
- Inkooporder
- Inkooporderpakbon

Meer rapporten worden beschikbaar. Speciale meldingen over aanvullende rapporten worden afzonderlijk verzonden. 

Een volledige lijst met alle rapporten die zijn gepland voor de release van oktober 2019, vindt u in [Configureerbare rapportage voor bedrijfsdocumenten in Word en Excel](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

# <a name="example-enable-configure-and-use-business-document-management"></a>Voorbeeld: Beheer van bedrijfsdocumenten inschakelen, configureren en gebruiken

Voor meer informatie over deze functie kunt u het voorbeeld in dit onderwerp uitvoeren.

## <a name="configure-er-parameters"></a>ER-parameters configureren

Omdat Beheer van bedrijfsdocumenten bovenop het ER-raamwerk is gebouwd, moet u de ER-parameters configureren om te werken met Beheer van bedrijfsdocumenten. Hiervoor stelt u ER-parameters in, zoals wordt beschreven in [Het ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md). U moet ook een nieuwe configuratieprovider toevoegen, zoals wordt beschreven in [Een configuratieprovider maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER-werkruimte](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>ER-oplossingen importeren

U moet ER-configuraties die sjablonen voor bedrijfsdocumenten bevatten, importeren naar het huidige exemplaar. Download en bewaar de volgende bestanden lokaal om deze procedure te voltooien.

**Voorbeeld ER-oplossing voor klantfacturering**

| **Bestand**                                  | **Inhoud**                                |
|-------------------------------------------|--------------------------------------------|
| Customer invoicing model.version.2.xml    | [Configuratie van model voor ER-gegevens](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Customer FTI report (GER).version.2.3.xml | [Configuratie voor een factuur met vrije tekst](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Voorbeeld van ER-oplossing voor betalingscheques**

| **Bestand**                                  | **Inhoud**                                |
|-------------------------------------------|--------------------------------------------|
| Model for cheques.version.10.xml          | [Configuratie van model voor ER-gegevens](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Cheques printing format.version.10.9.xml  | [Configuratie van de ER-indeling voor betalingscheques](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Voorbeeld van een ER-oplossing voor buitenlandse handel**

| **Bestand**                                  | **Inhoud**                                |
|-------------------------------------------|--------------------------------------------|
| Intrastat model.version.1.xml             | [Configuratie van model voor ER-gegevens](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat report.version.1.9.xml          | [Configuratie van ER-indeling voor Intrastat-controlerapport](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Gebruik de volgende procedure om elk bestand te importeren. Importeer de configuratie voor het ER-*gegevensmodel* van elke ER-oplossing in de tabellen hierboven voordat u de bijbehorende configuratie van de ER-*indeling* importeert.

1. Open de pagina **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer **Uitwisselen** boven aan de pagina.
3. Selecteer **Laden uit XML-bestand**.
4. Selecteer **Bladeren** om het vereiste XML-bestand te laden.
5. Selecteer **OK** om het importeren van de configuratie te bevestigen.

![Pagina ER-configuraties](./media/BDM-Overview-ERSolutions.png)

Zie [De levenscyclus van de configuratie van elektronische rapportage beheren](general-electronic-reporting-manage-configuration-lifecycle.md) voor meer informatie over het importeren van ER-configuraties.

## <a name="enable-business-document-management"></a>Beheer van bedrijfsdocumenten inschakelen

Als u Beheer van bedrijfsdocumenten wilt starten, moet u het werkgebied **Functiebeheer** openen en de functie **Beheer van bedrijfsdocumenten** inschakelen.

Gebruik de volgende procedure om de functionaliteit voor Beheer van bedrijfsdocumenten voor alle rechtspersonen in te schakelen.

1. Open het het werkgebied **Functiebeheer**.
2. Selecteer op het tabblad **Nieuw** de functie **Beheer van bedrijfsdocumenten** in de lijst.
3. Selecteer **Nu inschakelen** om de geselecteerde functie in te schakelen.
4. Vernieuw de pagina om de nieuwe functie te openen.

![Werkgebied Functiebeheer](./media/BDM-Overview-FMEnabling.png)

Zie [Overzicht Functiebeheer](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)voor meer informatie over het activeren van nieuwe functies.

## <a name="configure-parameters"></a>Parameters configureren

Met de informatie in de volgende secties kunt u de basisparameters voor Beheer van bedrijfsdocumenten instellen.

### <a name="prerequisites-for-parameter-setup"></a>Vereisten voor parameterinstellingen
Voordat u Beheer van bedrijfsdocumenten kunt instellen, moet u het vereiste documenttype instellen in het raamwerk voor documentbeheer. Dit documenttype wordt gebruikt om een tijdelijke opslag van documenten op te geven in Office-indelingen (Excel en Word) die worden gebruikt als sjablonen voor ER-rapporten. De sjabloon voor tijdelijke opslag kan worden bewerkt met behulp van de Office-bureaubladtoepassingen.

Voor dit documenttype moeten de volgende kenmerkwaarden worden geselecteerd.

| **Naam van kenmerk**  | **Kenmerkwaarde**   |
|---------------------|-----------------------|
| Klasse               | Bestand koppelen           |
| Groep               | Bestand                  |
| Locatie            | SharePoint            |

Zie [Documentbeheer configureren](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) voor informatie over het instellen van de vereiste parameters voor documentbeheer en documenttypen.

![Documenttype voor Documentbeheer instellen](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a>Parameters instellen

Op de pagina **Parameters voor bedrijfsdocumenten** kunnen elementaire parameters voor Beheer van bedrijfsdocumenten worden ingesteld. Alleen specifieke gebruikers hebben toegang tot de pagina. Dit zijn:

- Gebruikers aan wie de rol **Systeembeheerder** is toegewezen.
- Gebruikers die zijn toegewezen aan een rol die is geconfigureerd voor het uitvoeren van de functie **Parameters voor Beheer van bedrijfsdocumenten onderhouden** (AOT-naam **ERBDMaintainParameters**).

Gebruik de volgende procedure om de basisparameters in te stellen voor alle rechtspersonen.

1. Meld u als een gebruiker met toegang tot de pagina **Parameters voor bedrijfsdocumenten** aan.
2. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Beheer van bedrijfsdocumenten** \> **Parameters bedrijfsdocumenten**.
3.  Definieer op de pagina **Parameters bedrijfsdocumenten**, op het tabblad **Bijlagen**, in het veld **SharePoint-documenttype** het documenttype dat moet worden gebruikt om sjablonen tijdelijk op te slaan in Office-indelingen, als ze worden bewerkt met de Office-bureaubladtoepassingen. 

> [!NOTE]
> Alleen documenttypen die met behulp van een SharePoint-locatie zijn geconfigureerd, zijn beschikbaar voor deze parameter.

![Parameters voor Beheer van bedrijfsdocumenten instellen](./media/BDM-Overview-BDMSetting.png)

Het geselecteerde documenttype is specifiek voor het bedrijf en wordt gebruikt wanneer de gebruiker werkt met Beheer van bedrijfsdocumenten in het bedrijf waarvoor het geselecteerde documenttype is geconfigureerd. Wanneer de gebruiker met Beheer van bedrijfsdocumenten werkt in een ander bedrijf, wordt hetzelfde geselecteerde documenttype gebruik als dit niet is geconfigureerd voor dit bedrijf. Wanneer wel een document type is geconfigureerd, wordt dit gebruikt in plaats van het type dat is geselecteerd in het veld **SharePoint-documenttype**.

## <a name="configure-access-permissions"></a>Toegangsmachtigingen configureren

Als er geen toegangsmachtigingen voor Beheer van bedrijfsdocumenten zijn ingeschakeld, zien alle gebruikers met toegang tot het werkgebied Beheer van bedrijfsdocumenten standaard alle sjablonen voor ER-oplossingen die beschikbaar zijn. In het bedrijfsdocument Beheer voor bedrijfsdocumenten worden alleen sjablonen weergegeven die zich in de ER-opmaakconfiguraties bevinden en die zijn gemarkeerd met een label **Bedrijfsdocumenttype**.

![Pagina ER-configuraties](./media/BDM-Overview-ERFormatTags.png)

U kunt de lijst met sjablonen die beschikbaar zijn in het werkgebied Beheer van bedrijfsdocumenten beperken door toegangsmachtigingen te configureren. Dit kan van belang zijn wanneer er verschillende sjablonen worden gebruikt om bedrijfsdocumenten te maken voor verschillende bedrijfsdomeinen (functiegebieden) en als u bepaalde gebruikers toegang wilt geven tot verschillende sjablonen om deze te bewerken in het werkgebied Beheer van bedrijfsdocumenten.

Toegangsmachtigingen voor Beheer van bedrijfsdocumenten kunnen worden ingesteld in de **Configurator van toegangsmachtigingen**. Alleen de volgende gebruikers hebben toegang tot de pagina:

- Gebruikers die zijn toegewezen aan de rol **Systeembeheerder**.
- Gebruikers die zijn toegewezen aan elke andere rol die is geconfigureerd voor het uitvoeren van de functie **Machtigingen configureren voor toegang tot bedrijfsdocumentsjablonen voor bewerken** (AOT-naam **ERBDTemplatesSecurity**).

Gebruik de volgende procedure om de toegangsmachtigingen voor Beheer van bedrijfsdocumenten voor alle rechtspersonen in te stellen.

1. Meld u als een gebruiker met toegang tot de pagina **Configurator van toegangsmachtigingen** aan.
2. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Beheer van bedrijfsdocumenten** \> **Toegangsmachtigingen beheren**.

Let op de melding dat het gebruik van toegangsmachtigingen voor Beheer van bedrijfsdocumenten momenteel niet is ingeschakeld.

![De pagina Configurator van toegangsmachtigingen voor Beheer van bedrijfsdocumenten](./media/BDM-Overview-TemplatesAccess1.png)

Met deze instelling kan elke gebruiker die is toegewezen aan een beveiligingsrol die is geconfigureerd voor het uitvoeren van de functie **Bedrijfsdocumentsjablonen beheren** (AOT-naam **ERBDManageTemplates**), het werkgebied Beheer van bedrijfsdocumenten openen en elke sjabloon bewerken die beschikbaar is.

In de volgende afbeelding ziet u wat er beschikbaar is in het werkgebied Beheer van bedrijfsdocumenten voor gebruikers die zijn toegewezen aan de rol **Klantenadministrateur**. Met de huidige instelling voor toegangsmachtigingen kan de gebruiker bedrijfsdocumentsjablonen bewerken vanuit verschillende functionele gebieden, zoals facturering, wettelijke rapportage en betalingen.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-TemplatesForAlice1.png)

3. Selecteer op de pagina **Configurator van toegangsmachtigingen** de optie **Toegangsmachtigingen instellen**.
4. Schakel in het dialoog venster **Instellingen van toegangsmachtigingen voor het bewerken van sjablonen** de optie **Geconfigureerde toegangsmachtigingen toepassen** in.
5. Selecteer **OK** om te bevestigen dat de toegangsmachtigingen voor Beheer van bedrijfsdocumenten zijn ingeschakeld.

![De pagina Configuratie van toegangsmachtigingen voor Beheer van bedrijfsdocumenten](./media/BDM-Overview-TemplatesAccess2.png)

6. Selecteer **Toevoegen** om een nieuwe zakelijke rol in te voeren waarvoor toegangsmachtigingen voor sjablonen voor Beheer van bedrijfsdocumenten moeten worden geconfigureerd.
7. Selecteer in het dialoogvenster **Beveiligingsrollen** de rol **Klantadministrateur** en selecteer vervolgens **OK** om de geselecteerde rol te bevestigen.
8. Selecteer op het tabblad **Toegangsmachtigingen met codes van configuraties** de optie **Nieuw**.
9. Selecteer in het veld **Type code** de optie **Functiegebied** en selecteer in het veld **Id** de optie **Facturering**.
10. Selecteer **Opslaan** om geconfigureerde toegangsmachtigingen voor de geselecteerde rol op te slaan.

  De huidige instelling betekent dat voor alle gebruikers die zijn toegewezen aan de rol **Klantadministrateur** en die de functie **Bedrijfsdocumentsjablonen beheren** (AOT-naam **ERBDManageTemplates**) uitvoeren, configuratiesjablonen met ER-indeling met de waarde **Facturering** voor de code **Functiegebied** beschikbaar zijn voor bewerken in het werkgebied Beheer van bedrijfsdocumenten.

11. Ga naar het deelvenster **Gerelateerde informatie** aan de rechterkant van de huidige pagina. In het deelvenster **Verwante informatie** wordt weergegeven hoe de geconfigureerde toegangsmachtigingen worden toegepast, inclusief welke ER-configuratiesjablonen er beschikbaar zijn voor gebruikers die zijn toegewezen aan de rol **Klantenadministrateur**.

![De pagina Configuratie van toegangsmachtigingen voor Beheer van bedrijfsdocumenten](./media/BDM-Overview-TemplatesAccess3.png)

12. Selecteer op het tabblad **Toegangsmachtigingen per configuratie** de optie **Toevoegen**.
13. Markeer in het dialoogvenster **Configuratie selecteren** de ER-indelingsconfiguratie **Intrastat-rapport**.
14. Selecteer **OK** om de invoer van de geselecteerde configuraties te bevestigen en selecteer **Opslaan** om de geconfigureerde toegangsmachtigingen voor de geselecteerde rol op te slaan.

De huidige instelling betekent dat voor alle gebruikers die zijn toegewezen aan de rol **Klantadministrateur** en die de functie **Bedrijfsdocumentsjablonen beheren** (AOT-naam **ERBDManageTemplates**) uitvoeren, de volgende sjablonen beschikbaar zijn voor bewerken in het werkgebied Beheer van bedrijfsdocumenten:

- Sjablonen met de waarde **Facturering** voor de code van het **functionele gebied**.
- Sjablonen uit ER-indelingsconfiguraties die worden vermeld op het tabblad **Toegangsmachtigingen per configuratie** (sjablonen uit de indeling configuratie **Intrastat-rapport** van het domein **Wettelijke rapportage** in dit voorbeeld).

![De pagina Configuratie van toegangsmachtigingen voor Beheer van bedrijfsdocumenten](./media/BDM-Overview-TemplatesAccess4.png)

In de volgende afbeelding ziet u wat het werkgebied Beheer van bedrijfsdocumenten doorgeeft aan gebruikers die zijn toegewezen aan de rol **Klantenadministrateur**. Met de huidige instelling voor toegangsmachtigingen voor Beheer van bedrijfsdocumenten kan de gebruiker sjablonen voor bedrijfsdocumenten bewerken vanuit het domein **Facturering** en de ER-indelingsconfiguratie voor **Intrastat-rapporten**. Sjablonen uit het domein **Betalingen** zijn niet toegankelijk voor de rol **Klantenadministrateur**.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> De regels voor **Toegangsmachtigingen per configuratie** worden opgeslagen met de unieke id van een ER-indelingsconfiguratie. Dit betekent dat deze regels niet worden verwijderd wanneer een ER-configuratie wordt verwijderd die ernaar verwijst. Wanneer u verwijderde configuraties weer importeert in dit exemplaar, zullen deze regels er opnieuw naar verwijzen. U hoeft de regels niet opnieuw in te stellen nadat de verwijderde configuraties opnieuw zijn geïmporteerd.

## <a name="use-business-document-management-to-edit-templates"></a>Sjablonen bewerken met Beheer van bedrijfsdocumenten

Zakelijke gebruikers hebben toegang tot bedrijfsdocumentsjablonen om deze te bewerken in het werkgebied voor Beheer van bedrijfsdocumenten. Alleen de volgende gebruikers hebben toegang tot het werkgebied Beheer van bedrijfsdocumenten:

- Gebruikers die zijn toegewezen aan de rol **Systeembeheerder**.
- Gebruikers die zijn toegewezen aan een rol die is geconfigureerd voor het uitvoeren van de functie **Sjablonen voor Beheer van bedrijfsdocumenten beheren** (AOT-naam **ERBDManageTemplates**).

Met de volgende procedure kunt u sjablonen voor vrije-tekstfacturen bewerken in het werkgebied voor Beheer van bedrijfsdocumenten. Voordat u deze procedure voltooit, moet u alle voorgaande procedures in dit onderwerp hebben voltooid.

1. Meld u als een gebruiker met toegang tot het werkgebied voor het beheer van bedrijfsdocumenten aan.
2. Open het werkgebied van Beheer van bedrijfsdocumenten.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingTemplate1.png)

Op het tabblad **Sjabloon** wordt de inhoud van de geselecteerde sjabloon weergegeven. Selecteer het tabblad **Details** om de details van de geselecteerde sjabloon weer te geven, evenals details over de ER-indelingsconfiguratie waarin deze sjabloon zich bevindt. U ziet dat alle sjablonen de status **Gepubliceerd** hebben en geen details bevatten in de kolom **Revisie**. Dit betekent dat deze sjablonen momenteel niet worden bewerkt.

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Bewerking van sjablonen starten die eigendom zijn van uw configuratieprovider

1. Selecteer in het werkgebied Beheer van bedrijfsdocumenten de sjabloon **Afdrukindeling van cheques** in de lijst.
2. Selecteer het tabblad **Details**.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingTemplate2.png)

De optie **Sjabloon bewerken** is beschikbaar voor de geselecteerde sjabloon. Deze optie is altijd beschikbaar voor een sjabloon in een ER-indelingsconfiguratie die eigendom is van de actieve ER-configuratieprovider (**Litware, Inc.** in dit voorbeeld). Wanneer de optie **Sjabloon bewerken** is geselecteerd, kan de bestaande sjabloon uit de conceptversie van de onderliggende ER-indelingsconfiguratie worden bewerkt.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Bewerking van sjablonen starten die eigendom zijn van andere providers

1. Selecteer in het werkgebied Beheer van bedrijfsdocumenten de sjabloon **FTI-rapport klant (GER)** in de lijst.
2. Selecteer het tabblad **Details**.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingTemplate3.png)

De optie **Nieuw document** is beschikbaar voor de geselecteerde sjabloon. Deze optie is altijd beschikbaar voor een sjabloon in een ER-indelingsconfiguratie die wordt geleverd door een andere provider (**Microsoft** in dit voorbeeld). Wanneer **Nieuw document** wordt geselecteerd, kan een nieuwe sjabloon worden bewerkt. De bewerkte sjabloon wordt vervolgens opgeslagen in een nieuwe ER-indelingsconfiguratie die automatisch wordt gegenereerd.

### <a name="start-editing-a-template"></a>Een sjabloon bewerken

1. Selecteer **Nieuw document** in de geselecteerde sjabloon.
2. Wijzig zo nodig in het veld **Titel** de titel van de bewerkbare sjabloon. De tekst wordt gebruikt als naam voor de ER-indelingsconfiguratie die automatisch wordt gemaakt. De conceptversie van deze configuratie (**Kopie FTI-rapport klant (GER)**) waarin de bewerkte sjabloon wordt opgenomen, wordt automatisch gemarkeerd om deze ER-indeling voor de huidige gebruiker uit te voeren. Tegelijkertijd wordt de niet-gewijzigde oorspronkelijke sjabloon van de ER-basisindelingsconfiguratie gebruikt om deze ER-indeling voor andere gebruikers uit te voeren.
3. Wijzig in het veld **Naam** de naam van de eerste revisie van de bewerkbare sjabloon die automatisch wordt gemaakt.
4. Wijzig in het veld **Opmerking** de opmerking voor de automatisch gemaakte revisie van de bewerkbare sjabloon.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingTemplate4.png)

5. Selecteer **OK** om het begin van het bewerkingsproces te bevestigen.

De pagina **BDM-sjablooneditor** wordt geopend. De geselecteerde sjabloon is beschikbaar voor on line bewerken met Office 365.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-office-365"></a>Een sjabloon bewerken in Office 365

Wijzig de sjabloon met behulp van de functionaliteit van Office 365. Wijzig in Office Online bijvoorbeeld het lettertype van de veldprompts in de sjabloonkoptekst van **Normaal** in **Vet**. Deze wijzigingen worden automatisch opgeslagen voor de bewerkbare sjabloon die is opgeslagen in de opslagruimte van de primaire sjabloon (standaard is dit de Azure Blob-opslag) die is geconfigureerd voor het ER-raamwerk.

![Sjablooneditor voor Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a>Een sjabloon bewerken in de Office-bureaubladtoepassing

1. Selecteer de optie **Openen in bureaubladtoepassing** om de sjabloon te wijzigen met behulp van de functionaliteit van de Office-bureaubladtoepassing (Excel in dit voor beeld). De bewerkbare sjabloon wordt gekopieerd van de permanente opslag naar de tijdelijke opslag die is geconfigureerd in de parameters voor Beheer van bedrijfsdocumenten als een SharePoint-map.
2. Bevestig dat u de sjabloon wilt openen vanuit de tijdelijke bestandsopslag in de Office-bureaubladtoepassing Excel.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingLayout3.png)

3. Wijzig de sjabloon. Wijzig bijvoorbeeld het lettertypekleur van de veldprompts in de sjabloonkoptekst van **Zwart** in **Blauw**.

![Sjablooneditor voor Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingLayout4.png)

4. Selecteer **Opslaan** in de Excel-bureaubladtoepassing om de wijzigingen in de sjabloon op te slaan in de tijdelijke opslag.

![Sjablooneditor voor Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingLayout5.png)

5. Sluit de Excel-bureaubladtoepassing.
6. Selecteer **Opgeslagen kopie synchroniseren** om de tijdelijke sjabloonopslag te synchroniseren met de permanente sjabloonopslag.

> [!NOTE]
> De kopie van de bewerkbare sjabloon in de tijdelijke bestandsopslag wordt alleen voor de huidige sessie van het bewerken van sjablonen bewaard. Wanneer u deze sessie hebt voltooid door de pagina **BDM-sjablooneditor** te sluiten, wordt deze kopie verwijderd. Als u de sjabloon in de tijdelijke bestandsopslag hebt aangepast en niet de optie **Opgeslagen kopie synchroniseren** hebt geselecteerd bij het sluiten van de pagina **BDM-sjablooneditor**, wordt gevraagd of u de wijzigingen wilt opslaan. Selecteer **Ja** als u de wijzigingen in de sjabloon wilt opslaan in de permanente bestandslocatie.

### <a name="validate-a-template"></a>Een sjabloon valideren

1. Selecteer op de pagina **BDM-sjablooneditor** de optie **Controleren op problemen** om de gewijzigde sjabloon te valideren op basis van de onderliggende ER-indelingsconfiguratie. Volg de aanbevelingen (indien van toepassing) om de sjabloon uit te lijnen met de structuur van de indeling van de ER-basisindelingsconfiguratie.
2. Selecteer **Indeling weergeven** om de huidige structuur van de indeling weer te geven vanuit de ER-basisindelingsconfiguratie die moet worden afgestemd op de bewerkbare sjabloon. 
3. Selecteer **Indeling verbergen** om het deelvenster te sluiten.

![Pagina BDM-sjablooneditor](./media/BDM-Overview-EditingTemplate6.png)

4. Sluit de pagina **BDM-sjablooneditor**.

De bijgewerkte sjabloon wordt weergegeven op het tabblad **Sjabloon**. U ziet dat de status van de bewerkte sjabloon nu **Concept** is en dat de huidige revisie niet meer leeg is. Dit betekent dat het proces van het bewerken van deze sjabloon is gestart.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>De gewijzigde sjabloon testen 

1. Schakel in de toepassing over naar het bedrijf **USMF**.
2. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
3. Selecteer de factuur **FTI-00000002** en selecteer **Afdrukbeheer**.
4. Selecteer het niveau **Module - Klanten** \> **Documenten** \> **Vrije-tekstfactuur** \> **Oorspronkelijk document** om het bereik van facturen voor verwerking op te geven.
5. Selecteer in het veld **Rapportindeling** de ER-indeling **Kopie FTI-rapport klant (GER)** voor het opgegeven documentniveau.

![Pagina Afdrukbeheerinstellingen](./media/BDM-Overview-TestRun1.png)

6. Druk op **ESC** om de huidige pagina te sluiten.
7. Selecteer **Afdrukken** en klik op **Geselecteerd**.
8. Download het document en open het met de Excel-bureaubladtoepassing.

![Pagina Vrije-tekstfacturen](./media/BDM-Overview-TestRun2.png)

De gewijzigde sjabloon wordt gebruikt om het rapport met vrije-tekstfacturen voor het geselecteerde artikel te genereren. Als u wilt analyseren hoe dit rapport wordt beïnvloed door de wijzigingen die u hebt aangebracht in de sjabloon, kunt u dit rapport uitvoeren in één toepassingssessie direct nadat u de sjabloon hebt gewijzigd in een andere toepassingssessie.

### <a name="create-an-alternative-template-revision"></a>Een alternatieve sjabloonrevisie maken

1. Open de pagina **BDM-sjablooneditor** en selecteer de sjabloon **Kopie FTI-rapport klant (GER)**.
2. Selecteer **Nieuw** op het tabblad **Revisies**.
3. Wijzig zo nodig in het veld **Naam** de naam van de tweede revisie en baseer deze op de huidige actieve eerste revisie.
4. Wijzig zo nodig in het veld **Opmerking** de opmerking voor de automatisch gemaakte revisie van de bewerkbare sjabloon.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-AddRevision.png)

U hebt een nieuwe revisie van uw sjabloon gemaakt die is opgeslagen in de permanente sjabloonopslag. U kunt nu doorgaan met het bewerken van de sjabloon van de tweede revisie die momenteel als actief is geselecteerd.

5. Selecteer de eerste revisie en selecteer vervolgens **Instellingen als actief**. U kunt een andere revisie als actief selecteren als u wilt terugkeren naar die revisie van de sjabloon.
6. Selecteer de tweede revisie en selecteer vervolgens **Verwijderen**.
7. Selecteer **OK** om te bevestigen dat u de geselecteerde revisie wilt verwijderen. U kunt alle niet-actieve revisies verwijderen wanneer u deze niet meer nodig hebt.

### <a name="delete-a-modified-template"></a>Een gewijzigde sjabloon verwijderen

1. Selecteer op de pagina **BDM-sjablooneditor** het tabblad **Sjabloon**.
2. Selecteer **Verwijderen**.
3. Als u **OK** selecteert om de verwijdering te bevestigen, wordt de ER-indeling **Kopie FTI-rapport klant (GER)** met de gewijzigde sjabloon verwijderd. Selecteer **Annuleren** als u andere opties wilt bekijken.

### <a name="revoke-changes-of-template"></a>Wijzigingen in de sjabloon intrekken

Wanneer u de sjabloon bewerkt vanuit een ER-indeling die eigendom is van de huidige actieve provider, krijgt u de mogelijkheid om de wijzigingen in de sjabloon in te trekken.

![Pagina Werkgebied van Beheer van bedrijfsdocumenten](./media/BDM-Overview-RevokeChanges.png)

1. Selecteer op de pagina **BDM-sjablooneditor** het tabblad **Sjabloon**.
2. Selecteer **Ongedaan maken**.
3. Als u **OK** selecteert om de wijzigingen in de sjabloon in te trekken, wordt de gewijzigde sjabloon vervangen door de oorspronkelijke sjabloon en worden alle wijzigingen verwijderd. Wanneer u de wijzigingen in de sjabloon intrekt, kunt u de sjabloon verwijderen. Selecteer **Annuleren** als u andere opties wilt bekijken.

### <a name="publish-a-modified-template"></a>Een gewijzigde sjabloon publiceren
1. Selecteer op de pagina **BDM-sjablooneditor**, op het tabblad **Sjabloon** de optie **Publiceren**.
2. Als u **OK** selecteert om de publicatie te bevestigen, wordt de conceptversie van de afgeleide ER-indeling **Kopie FTI-rapport klant (GER)** die de gewijzigde sjabloon bevat, gemarkeerd als voltooid. De gewijzigde sjabloon wordt beschikbaar voor andere gebruikers. In de voltooide versies van deze ER-indeling worden alleen de laatste actieve revisies van de sjabloon behouden. Andere revisies worden verwijderd. Selecteer **Annuleren** als u andere opties wilt bekijken.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

#### <a name="i-selected-new-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a>Ik heb **Nieuw document** geselecteerd, maar in plaats van de pagina **BDM-sjablooneditor** te openen in Finance and Operations, ben ik doorgestuurd naar de Office 365-webpagina.
Dit is een bekend probleem met de Office 365-omleiding. Dit gebeurt wanneer u zich de eerste keer aanmeldt bij Office 365. Als u dit probleem wilt verhelpen, selecteert u de knop **Vorige** in de browser om terug te gaan.

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a>Ik begrijp hoe ik een sjabloon kan bewerken met Office 365 in de eerste toepassingssessie en hoe ik de sjabloon in de tweede toepassingssessie gebruik om de sjabloon aan te passen en hoe ik mijn wijzigingen kan zien die van invloed zijn op het gegenereerde bedrijfsdocument. Kan ik dit doen met de Office-bureaubladtoepassing?
Ja, dat kan. Selecteer in de eerste toepassingssessie de optie **Openen in bureaubladtoepassing**. De sjabloon wordt opgeslagen in de tijdelijke bestandsopslag en geopend in de Office-bureaubladtoepassing. Voer de volgende stappen uit om een voorbeeld te bekijken van de wijzigingen in de sjabloon in het gegenereerde bedrijfsdocument:

1. Breng wijzigingen aan in de sjabloon met de Office-bureaubladtoepassing.
2. Selecteer **Opslaan** in de Office-bureaubladtoepassing.
3. Selecteer op de pagina **BDM-sjablooneditor** van de eerste toepassingssessie de optie **Opgeslagen kopie synchroniseren**.
4. Voer deze sjabloon met ER-indeling in de tweede toepassingssessie uit.

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a>Ik krijg de foutmelding 'Waarde kan niet null zijn. Parameternaam: externalId' als ik **Openen in bureaubladtoepassing** selecteer. Hoe kan ik dit oplossen? 
Waarschijnlijk bent u aangemeld bij het huidige exemplaar van de app van het Azure AD-domein. Dit verschilt van het Azure AD-domein dat is gebruikt om dit exemplaar te implementeren. Omdat de SharePoint-service die wordt gebruikt om sjablonen op te slaan en beschikbaar te maken voor bewerken met de Office-bureaubladtoepassingen, tot hetzelfde domein behoort, hebt u geen toegangsmachtiging tot de SharePoint-service. U kunt dit probleem oplossen door u bij het huidige exemplaar aan te melden met de referenties van een gebruiker met het juiste Azure AD-domein.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](tasks/er-design-reports-openxml-2016-11.md)

[ER-configuraties ontwerpen om rapporten in Word-indeling te genereren](tasks/er-design-configuration-word-2016-11.md)

[Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md)

[Elektronische aangifte configureren om gegevens op te halen in Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)

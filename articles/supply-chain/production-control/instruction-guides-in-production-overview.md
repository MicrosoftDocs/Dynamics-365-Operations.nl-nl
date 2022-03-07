---
title: Productiemedewerkers voorzien van mixed reality-guides
description: In dit onderwerp wordt uitgelegd hoe u de productiebeheermodule in Microsoft Dynamics 365 Supply Chain Management integreert met Dynamics 365 Guides.
author: johanhoffmann
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "61943"
- intro-internal
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 703f2cb9a1ea8691420765a8598d59f3e6cc6488
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062947"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Productiemedewerkers voorzien van mixed reality-guides

[!include [banner](../includes/banner.md)]


Medewerkers in productieprocessen zullen gebruikmaken van relevante instructies die op het juiste moment in het context van hun werk worden geleverd. *Instructies* zijn van toepassing op verschillende domeinen van werkzaamheden, waaronder: assemblage, service, bewerkingen, certificering en veiligheid. In al deze belangrijke bedrijfsfuncties kunnen doorlopende trainingsinstructies worden gebruikt om medewerkers te helpen meer te bereiken en beter te werken.

## <a name="introduction"></a>Inleiding

U kunt instructies op verschillende manieren verstrekken. Eén efficiënt systeem dat kant en klaar wordt geleverd maakt gebruik van [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).

Dynamics 365 Guides kan u helpen uw medewerkers beter te leren werken via praktijktraining. U kunt gestandaardiseerde processen definiëren met stapsgewijze instructies in de vorm van guides die uw medewerkers begeleiden bij het werken met de gereedschappen en onderdelen die ze nodig hebben en die medewerkers laten zien hoe ze deze gereedschappen moeten gebruiken in concrete werksituaties.

U kunt guides koppelen aan verschillende aspecten van productiebeheer, waaronder:

- [Bronnen](#resources)
- [Resourcegroepen](#resource-groups)
- [Vrijgegeven producten](#released-products)
- [Formules](#formulas)
- [Formuleversies](#formula-versions)
- [Stuklijsten](#bom)
- [Stuklijstversies](#bom-versions)
- [Routes](#routes)
- [Routeversies](#route-versions)
- [Routebewerkingsrelaties](#route-operation-relations)

> [!NOTE]
> U kunt ook guides aan activabeheer koppelen. Zie [Dynamics 365 Supply Chain Management (Activabeheer) integreren met Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md) voor meer informatie over die optie.

Wanneer een eerstelijnsmedewerker een taak kiest voor de werkvloer via Supply Chain Management, kan de medewerker [de relevante guides](#logic) op de taakkaart zien. Wanneer de medewerker een specifieke guide kiest, wordt op het scherm een QR-code voor die guide weergegeven. De medewerker gebruikt vervolgens de eigen HoloLens om de QR-code te scannen, waarmee guides worden gestart en de vereiste instructies worden weergegeven.

In de volgende subsecties wordt een aantal geselecteerde scenario's beschreven waarbij bedrijven in verschillende bedrijfstakken de grootste toegevoegde waarde kunnen leveren bij het gebruik van guides voor het presenteren van instructies voor de productie.

### <a name="assembly"></a>Assembly

![Guides gebruiken in assemblagetaken.](media/instruction-guides-hero-assembly.png "Guides gebruiken in servicetaken")

Guides voor assemblagebewerkingen tonen medewerkers de benodigde gereedschappen en onderdelen en geven aan hoe ze deze in concrete werksituaties moeten gebruiken.

Productiemanagers kunnen guides maken en toewijzen, bijvoorbeeld voor [productieroutes](routes-operations.md), [bewerkingsrelaties](routes-operations.md#operation-relations) of [stuklijsten](bill-of-material-bom.md). Medewerkers vinden hier de relevante instructies voor de bewerkingservaring op de werkvloer.

### <a name="service"></a>Service

![Guides gebruiken in servicetaken.](media/instruction-guides-hero-service.png "Guides gebruiken in servicetaken")

Voorzie technici van begeleide instructies op de werkplek, zodat er geen extra bezoeken hoeven te worden gepland.

Servicemanagers kunnen bijvoorbeeld guides toewijzen aan specifieke [producten](../../commerce/product.md) die de kwaliteitscontrole-routines doorlopen.

### <a name="quality"></a>Kwaliteit

![Guides gebruiken in kwaliteitscontroletaken.](media/instruction-guides-hero-quality.png "Guides gebruiken in kwaliteitscontroletaken")

Implementeer nieuwe processen en zorg voor een betere consistentie door de kennis van medewerkers in een herhaalbaar hulpmiddel te veranderen.

Managers voor kwaliteitscontrole kunnen bijvoorbeeld guides toewijzen aan specifieke [producten](../../commerce/product.md) die de routines van de kwaliteitscontrole doorlopen.

### <a name="certifications"></a>Certificaten

![Guides gebruiken voor aan certificering gerelateerde taken.](media/instruction-guides-hero-certification.png "Guides gebruiken voor aan certificering gerelateerde taken")

Zorg ervoor dat elke medewerker aan hoge normen voldoet door snel te identificeren wie hulp nodig heeft en waar.

### <a name="safety"></a>Veiligheid

![Guides gebruiken in instructies voor veilig werken.](media/instruction-guides-hero-safety.png "Guides gebruiken in instructies voor veilig werken")

Verstrek instructies die gevaarlijke procedures doorlopen, vrijwel voordat u deze probeert in de fysieke omgeving. Met een methode met mixed reality kunnen medewerkers virtueel gevaarlijke procedures uitvoeren.

Productiemanagers kunnen speciale verwerkingsinstructies bieden voor werken met gevaarlijke materiaal of delicate-afhandelingsprocedures door instructies toe te wijzen aan [productartikelen](../../commerce/product.md), [routes](routes-operations.md) en [bewerkingen](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>Aan de slag met instructies en Guides

Om instructies in productieprocessen in te schakelen, biedt Supply Chain Management een kant en klare integratie met Dynamics 365 Guides. Een gelicentieerd en geïnstalleerd toepassingsexemplaar van Guides is vereist voor het maken, onderhouden en toewijzen van instructies met mixed reality voor productieactiva en werk.

### <a name="prerequisites"></a>Vereisten

Als u deze functie wilt gebruiken, moet uw systeem het volgende bevatten:

- Dynamics 365 Supply Chain Management versie 10.0.15 of hoger
- [Twee keer wegschrijven](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md) voor Supply Chain Management-apps.
- [Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versie 400.0.1.48 of hoger

### <a name="turn-on-the-feature"></a>De functie inschakelen

Als u de functie beschikbaar wilt maken op uw systeem, moet u de bijbehorende configuratiesleutels inschakelen. U hoeft dit maar één keer te doen. Hiertoe moet een beheerder het volgende doen:

1. Plaats het systeem in de onderhoudsmodus, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**.
1. Vouw de sectie **Mixed reality** uit en schakel vervolgens het selectievakje **Mixed reality-guide** in.
1. Vouw de sectie **Productiebeheer** uit en schakel vervolgens het selectievakje **Productie-instructies** in.
1. Schakel de onderhoudsmodus uit, zoals wordt beschreven in [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Configureren hoe guides op de werkvloer worden weergegeven

Als u wilt configureren hoe guides worden weergegeven op de werkvloer, gaat u naar **Mixed reality \> Dynamics 365 Guides \> Integratie van Guides configureren**.

![Integratie van guides configureren voor productie.](media/instruction-guides-configure-integration.png "Integratie van guides configureren voor productie")

Stel de volgende velden in:

- **Microsoft Dataverse-URL**: geef de URL op voor de Microsoft Dataverse-omgeving waarin u uw guides maakt. De notatie is contoso.crm4.dynamics.com, waarbij het eerste deel van de URL meestal wordt gebaseerd op de naam van uw organisatie (zoals contoso.). Het tweede deel is specifiek voor de gegevensregio van uw omgeving (zoals crm4) en het laatste gedeelte is het domein (zoals dynamics.com). U kunt de juiste URL vinden door naar [home.dynamics.com](https://home.dynamics.com/) te gaan en vervolgens uw Guides-app te openen. Wanneer Guides wordt geopend, wordt de URL in de adresbalk van uw browser weergegeven (gebruik alleen de basis-URL, die lijkt op het vorige voorbeeld). Deze waarde wordt gebruikt om adressen voor uw guides samen te stellen en wordt gecodeerd in de QR-codes.
- **Grootte van QR-code**: stel de grootte van de gegenereerde QR-code in. Het is raadzaam om een grootte te kiezen waarbij uw beeldscherm grotendeels gevuld is, maar niet meer. Meestal is *15* een goede waarde.
- **Foutcorrectieniveau QR-code**: stel de gedetailleerdheid van de QR-code in. Een hogere mate van gedetailleerdheid kan de betrouwbaarheid van de code helpen verhogen, maar uw **grootte van de QR-code** moet groot genoeg zijn om het detailniveau voor uw geselecteerde correctieniveau te ondersteunen.

> [!TIP]
> - Het weergeven van QR-codes die te groot zijn voor uw beeldscherm duurt iets langer en de QR-codes worden vervolgens aangepast aan uw beeldscherm. Deze bieden geen voordeel.
> - QR-codes die te klein zijn, kunnen de mogelijkheid van HoloLens verminderen om de code goed te lezen in bepaalde omgevingen.
> - Het is raadzaam om de instellingen te testen voor elk apparaat waarin QR-codes voor HoloLens-gebruikers worden weergegeven. Kies instellingen die voldoende leesbaarheid bieden in uw werkvloeromgeving.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Een overzicht weergeven van alle toewijzingen van guides

Gebruik de pagina **Alle guides** om de lijst met alle beschikbare guides in uw organisatie en alle toewijzingen aan productieprocessen en resources weer te geven. Ga naar **Mixed reality \> Guides \> Alle guides** om deze te openen. In de lijst boven worden alle beschikbare guides weergegeven en kunt u het veld hier gebruiken om de lijst te filteren. In de lijst onderaan ziet u alle toewijzingen van guides en een werkbalk voor het beheren hiervan.

![Guides beheren.](media/instruction-guides-allguides.png "Guides beheren")

In de volgende secties worden de typen objecten beschreven waaraan u guides kunt toewijzen. Elke toegewezen guide bevat instructies die automatisch worden gekoppeld aan de respectieve productietaken en die beschikbaar zijn op de werkvloer.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Een guide aan een resource koppelen

Voeg een guide toe aan een [resource](operations-resources.md) om de guide aan te bieden in de context van relevante productietaken.

### <a name="typical-scenario-using-resources"></a>Standaardscenario met resources

U kunt bijvoorbeeld een guide koppelen aan algemene machinebeveiligings- of verwerkingsinstructies voor een resource van het type machine. Vervolgens is de guide beschikbaar voor alle taken die op de computer worden uitgevoerd.

### <a name="add-a-guide-to-a-resource"></a>Een guide toevoegen aan een resource

Voeg als volgt een guide toe aan een resource:

1. Ga naar **Productiebeheer \> Instellen \> Resources \> Resources**.
1. Selecteer in het lijstvenster de resource waaraan u een guide wilt toewijzen.
1. Vouw het sneltabblad **Gekoppelde guides** uit.
1. Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**. Er wordt een nieuwe regel aan het raster toegevoegd.
1. Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen. Als u een groot aantal guides hebt, kunt u de lijst filteren om de gewenste te zoeken.
    ![Guides beheren.](media/instruction-guides-allguides.png "Guides beheren")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Een guide aan een resourcegroep koppelen

U kunt een guide aan [resourcegroepen](tasks/define-discrete-manufacturing-resource-group.md) toevoegen als u deze gebruikt om groepen machines, productielijnen of werkcellen te beheren.

### <a name="typical-scenarios-using-resource-groups"></a>Standaardscenario's met resourcegroepen

**Voorbeeld 1:** u hebt een resourcegroep gedefinieerd voor meerdere machines van hetzelfde model. In plaats van de relevante guide met verwerkingsinstructies voor het machinemodel aan elke relevante resource toe te wijzen, kunt u de guide ook toewijzen aan de resourcegroep waartoe het machinemodel behoort.

**Voorbeeld 2:** u hebt een resourcegroep gedefinieerd voor een werkcel die verschillende machines bevat en u beschikt over een guide waarin algemene instructies worden geboden voor het onderhouden van de werkcel. De guide is van toepassing op elke productieactiviteit in deze werkcel.

### <a name="add-a-guide-to-a-resource-group"></a>Een guide toevoegen aan een resourcegroep

U kunt als volgt een guide toevoegen aan een resourcegroep:

1. Ga naar **Productiebeheer \> Instellen \> Resources \> Resourcegroepen**.
1. Selecteer in het lijstvenster de resourcegroep waaraan u een guide wilt toewijzen.
1. Vouw het sneltabblad **Gekoppelde guides** uit.
1. Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**. Er wordt een nieuwe regel aan het raster toegevoegd.
1. Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen. Als u een groot aantal guides hebt, kunt u de lijst filteren om de gewenste te zoeken.
    ![Een guide toevoegen aan een resourcegroep.](media/instruction-guides-resourcegroup.png "Een guide toevoegen aan een resourcegroep")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Een guide aan een vrijgegeven product koppelen

U kunt een guide toevoegen aan een willekeurig [vrijgegeven product](../pim/tasks/create-released-product-single-company.md).

### <a name="typical-scenario-using-released-products"></a>Standaardscenario bij het gebruik van vrijgegeven producten

Via guides op productniveau kunt u medewerkers op de werkvloer helpen met instructies voor het werken of verwerken van een bepaald vrijgegeven product of artikel.

### <a name="add-a-guide-to-a-released-product"></a>Een guide toevoegen aan een vrijgegeven product

U kunt als volgt een guide toevoegen aan een vrijgegeven product:

1. Ga naar **Productiegegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Open het product waaraan u een guide wilt toewijzen.
1. Open in het actievenster het tabblad **Technicus** en selecteer in de groep **Weergeven** **Gekoppelde guides**.
1. De pagina **Gekoppelde guides** worden geopend voor uw geselecteerde product.
1. Selecteer **Toevoegen** in het actievenster om nieuwe regel toe te voegen aan het raster. 
1. Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.
    ![Een guide toevoegen aan een vrijgegeven product.](media/instruction-guides-ReleasedProduct-AddGuides.png "Een guide toevoegen aan een vrijgegeven product")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Een guide aan een formule koppelen

U kunt een guide toevoegen aan een willekeurige [formule](bill-of-material-bom.md#formulas-co-products-and-by-products).

### <a name="typical-scenario-using-formulas"></a>Standaardscenario met formules
  
Guides op formuleniveau bieden medewerkers op de werkvloer begeleide verwerkingsinstructies in de context van een formule of recept. Er kunnen ook guides worden toegewezen aan versies van een formule.

> [!NOTE]
> U kunt relevante richtlijnen toewijzen voor productieprocessen die zijn gebaseerd op een formule voor een route, routeversie of routebewerkingsrelaties.  

> Er kunnen momenteel geen guides aan afzonderlijke formuleregels worden gekoppeld.

### <a name="add-a-guide-to-a-formula"></a>Een guide toevoegen aan een formule

U kunt als volgt een guide toevoegen aan een formule:

1. Ga naar **Productiegegevensbeheer \> Stuklijsten en formules \> Formules**.
1. Open de formule waaraan u een guide wilt toewijzen.
1. Open het tabblad **Koptekst** boven het bovenste sneltabblad.
1. Vouw het sneltabblad **Gekoppelde guides** uit.
1. Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**. Er wordt een nieuwe regel aan het raster toegevoegd.
1. Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.
    ![Een guide toevoegen aan een formule.](media/instruction-guides-Formula.png "Een guide toevoegen aan een formule")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Een guide aan een formuleversie koppelen

U kunt een guide toevoegen aan een willekeurige [formuleversie](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>Standaardscenario met formuleversies

Guides die aan een afzonderlijke versie van een formule zijn gekoppeld, voorzien medewerkers van instructies voor het doorlopen van de productie van die versie van het recept van de formule.

> [!TIP]
> U kunt relevante richtlijnen toewijzen voor productieprocessen die zijn gebaseerd op deze formuleversie voor een route, routeversie of routebewerkingsrelaties.  

> [!NOTE]
> Er kunnen momenteel geen guides aan afzonderlijke formuleregels worden gekoppeld.

### <a name="add-a-guide-to-a-formula-version"></a>Een guide toevoegen aan een formuleversie

U kunt als volgt een guide toevoegen aan een formuleversie:

1. Ga naar **Productiegegevensbeheer \> Stuklijsten en formules \> Formules**.
1. Open de formule die een versie bevat waaraan u een guide wilt toewijzen.
1. Open het tabblad **Koptekst** boven het bovenste sneltabblad.
1. Selecteer op het sneltabblad **Formuleversies** de versie waaraan u een guide wilt toewijzen.
1. Selecteer op de werkbalk **Formuleversies** de optie **Gekoppelde guides**.
    ![De guides openen die aan een geselecteerde formuleversie zijn gekoppeld.](media/instruction-guides-FormulaVersion.png "De guides openen die aan een geselecteerde formuleversie zijn gekoppeld")
1. De pagina **Gekoppelde guides** worden geopend voor uw formuleversie.
1. Selecteer **Toevoegen** in het actievenster om nieuwe regel toe te voegen aan het raster. 
1. Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.
    ![Een guide toevoegen aan een formuleversie.](media/instruction-guides-FormulaVersionAddGuide.png "Een guide toevoegen aan een formuleversie")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Een guide aan een stuklijst koppelen

U kunt een guide toevoegen aan elke willekeurige [stuklijst](bill-of-material-bom.md).

### <a name="typical-scenario-using-bills-of-materials"></a>Standaardscenario met stuklijsten

Guides die aan een stuklijst zijn gekoppeld, voorzien medewerkers van instructies waarin wordt uitgelegd hoe materiaal van een stuklijst kan worden voorbereid en verwerkt. Er kunnen ook guides worden toegewezen aan versies van een stuklijst.

> [!NOTE]
> Er kunnen momenteel geen guides aan afzonderlijke stuklijstregels worden gekoppeld.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Een guide toevoegen aan een stuklijst

U kunt als volgt een guide toevoegen aan een stuklijst:

1. Ga naar **Productiegegevensbeheer \> Stuklijsten en formules \> Stuklijsten**.
1. Open de stuklijst waaraan u een guide wilt toewijzen.
1. Open het tabblad **Koptekst** boven het bovenste sneltabblad.
1. Vouw het sneltabblad **Gekoppelde guides** uit.
1. Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**. Er wordt een nieuwe regel aan het raster toegevoegd.
1. Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.
    ![Een guide toevoegen aan een stuklijst.](media/instruction-guides-BOM.png "Een guide toevoegen aan een stuklijst")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Een guide aan een stuklijstversie koppelen

U kunt een guide toevoegen aan elke willekeurige [stuklijstversie](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Standaardscenario met stuklijstversies

Guides die aan een afzonderlijke stuklijstversie zijn gekoppeld, voorzien medewerkers van instructies waarin wordt uitgelegd hoe u materiaal voorbereidt en verwerkt voor een versie van een stuklijst die verschilt van de algemene stuklijst of andere versies van de stuklijst.

> [!NOTE]
> Er kunnen momenteel geen guides aan afzonderlijke stuklijstregels worden gekoppeld.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Een guide toevoegen aan een stuklijstversie

U kunt als volgt een guide toevoegen aan een stuklijstversie:

1. Ga naar **Productiegegevensbeheer \> Stuklijsten en formules \> Stuklijsten**.
1. Open de stuklijst die een versie bevat waaraan u een guide wilt toewijzen.
1. Open het tabblad **Koptekst** boven het bovenste sneltabblad.
1. Selecteer op het sneltabblad **Stuklijstversies** de versie waaraan u een guide wilt toewijzen.
1. Selecteer op de werkbalk **Stuklijstversies** de optie **Gekoppelde guides**.
    ![De guides openen die aan een geselecteerde stuklijstversie zijn gekoppeld.](media/instruction-guides-BOMVersion.png "De guides openen die aan een geselecteerde stuklijstversie zijn gekoppeld")
1. De pagina **Gekoppelde guides** worden geopend voor uw stuklijstversie.
1. Selecteer **Toevoegen** in het actievenster om nieuwe regel toe te voegen aan het raster.
1. Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.
    ![Een guide toevoegen aan een stuklijstversie.](media/instruction-guides-BOMVersionAddGuide.png "Een guide toevoegen aan een stuklijstversie")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Een guide aan een route koppelen

U kunt een guide toevoegen aan een willekeurige [route](routes-operations.md).

### <a name="typical-scenario-using-routes"></a>Standaardscenario met routes

Routes worden meestal gebruikt om op te geven hoe een bepaald vrijgegeven product moet worden geproduceerd op basis van een stuklijst of stuklijstversie en met een set resources of resourcegroepen.

Wijs een guide aan een route toe om stapsgewijze instructies te leveren voor het respectievelijke productieproces.

### <a name="add-a-guide-to-a-route"></a>Een guide toevoegen aan een route

U kunt als volgt een guide toevoegen aan een route:

1. Ga naar **Productiebeheer \> Alle routes**.
1. Open de route waaraan u een guide wilt toewijzen.
1. Vouw het sneltabblad **Gekoppelde guides** uit.
1. Selecteer **Toevoegen** op de werkbalk **Gekoppelde guides**. Er wordt een nieuwe regel aan het raster toegevoegd.
1. Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.
    ![Een guide toevoegen aan een route.](media/instruction-guides-Route.png "Een guide toevoegen aan een route")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Een guide aan een routeversie koppelen

U kunt een guide toevoegen aan een willekeurige [routeversie](routes-operations.md#route-versions).

### <a name="typical-scenario-using-route-versions"></a>Standaardscenario met routeversies

Routeversies worden meestal gebruikt om varianten van productieprocessen op basis van een bestaande route op te geven. U kunt verschillende guides toewijzen aan elke routeversie.

### <a name="add-a-guide-to-a-route-version"></a>Een guide toevoegen aan een routeversie

U kunt als volgt een guide toevoegen aan een routeversie:

1. Ga naar **Productiebeheer \> Alle routes**.
1. Open de route waaraan u een guide wilt toewijzen.
1. Selecteer op het sneltabblad **Versies** de versie waaraan u een guide wilt toewijzen.
1. Selecteer op de werkbalk **Versies** de optie **Gekoppelde guides**.
    ![De guides openen die aan een geselecteerde routeversie zijn gekoppeld.](media/instruction-guides-RouteVersion.png "De guides openen die aan een geselecteerde routeversie zijn gekoppeld")
1. De pagina **Gekoppelde guides** worden geopend voor uw stuklijstversie.
1. Selecteer **Toevoegen** in het actievenster om nieuwe regel toe te voegen aan het raster.
1. Voor de nieuwe regel gebruikt u de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen.
    ![Een guide toevoegen aan een routeversie.](media/instruction-guides-RouteVersionAddGuide.png "Een guide toevoegen aan een routeversie")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Een guide aan een routebewerkingsrelatie koppelen

U kunt een guide toevoegen aan een willekeurige [routebewerkingsrelatie](routes-operations.md#operation-relations).

### <a name="typical-scenario-using-route-operation-relations"></a>Standaardscenario met routebewerkingsrelaties

Bewerkingsrelaties zijn de meest specifieke manier om richtlijnen toe te voegen aan een productproces en de bijbehorende bewerkingen. U kunt voor elke bewerking in een route richtlijnen opgeven en verschillende richtlijnen opgeven voor de typen relatiecontext die voor een route is opgegeven, bijvoorbeeld voor specifieke artikelen, configuraties en meer. U kunt ook opgeven in welke fasen van de bewerking de richtlijnen van toepassing zijn (zoals instelling, plaatsing in de wachtrij, verwerking of transport).

> [!NOTE]
> Als u guides opgeeft voor verschillende bewerkingsrelaties van een route, wordt in deze richtlijnen alleen de guides van de meest specifieke relatie weergegeven op de werkvloer voor de gegenereerde taak.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Een guide toevoegen aan een routebewerkingsrelatie

U kunt als volgt een guide toevoegen aan een routebewerkingsrelatie:

1. Ga naar **Productiebeheer \> Alle routes**.
1. Open de route waaraan u een guide wilt toewijzen.
1. Open in het actievenster het tabblad **Route** en selecteer in de groep **Onderhouden** de optie **Routedetails**.
1. De pagina **Routedetails** wordt geopend voor de geselecteerde route.
1. Selecteer in het bovenste raster de bewerking waarvoor u richtlijnen wilt opgeven.
1. Selecteer in het onderste raster een specifieke relatie (of de algemene relatie **Alle**).
    ![Een bewerking en vervolgens een relatie selecteren.](media/instruction-guides-RouteOperationRelation.png "Een bewerking en vervolgens een relatie selecteren")
1. Open boven het onderste raster het tabblad **Gekoppelde guides**. ![Het tabblad Gekoppelde guides.](media/instruction-guides-RouteOperationRelation-AddGuide.png "Het tabblad Gekoppelde guides")
1. Selecteer **Toevoegen** in de werkbalk boven aan het onderste raster om een nieuwe regel aan het raster toe te voegen.
1. Gebruik voor de nieuwe rij de vervolgkeuzelijst in de kolom **Naam** om de guide te kiezen die u wilt toewijzen. Schakel in de rest van de rij het selectievakje in voor elke context waarin de geselecteerde guide beschikbaar moet zijn.

> [!NOTE]
> U kunt een of meer guides toevoegen voor elke fase van elke bewerking.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Guides selecteren in de uitvoeringsinterface van de werkvloer

Wanneer een medewerker een takenlijst opent in de uitvoeringsinterface voor de werkvloer, worden in Supply Chain Management de relevante guides voor de weergegeven taken gevonden. Gebruik de knop **Guides** om de relevante guides weer te geven.

![Knop Guides in de uitvoeringsinterface van de werkvloer.](media/instruction-guides-Shopfloor1.png "Knop Guides in de uitvoeringsinterface van de werkvloer")

Zet vervolgens een HoloLens op en open de desbetreffende guide door naar de QR-code te kijken en de desbetreffende guide te activeren.

![QR-code om toegang te krijgen tot guides via een HoloLens.](media/instruction-guides-Shopfloor2.png "QR-code om toegang te krijgen tot guides via een HoloLens")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>De logica voor het selecteren van guides oplossen

U kunt guides toevoegen aan de volgende productiegegevens:

- [Bronnen](#resources)
- [Resourcegroepen](#resource-groups)
- [Vrijgegeven producten](#released-products)
- [Formules](#formulas)
- [Formuleversies](#formula-versions)
- [Stuklijsten](#bom)
- [Stuklijstversies](#bom-versions)
- [Routes](#routes)
- [Routeversies](#route-versions)
- [Routebewerkingsrelaties](#route-operation-relations)

Wanneer Supply Chain Management de taken voor de productievloer genereert, worden de relevante guides van deze bronnen verzameld. Let op de volgende belangrijke regels.

- Als u een stuklijstversie of formuleversie aan een route of productieorder koppelt, worden alle guides die aan deze versie zijn gekoppeld en ook de guides die aan de bovenliggende stuklijst of formule van die versie zijn gekoppeld, weergegeven in de taak.
- Als u een routeversie of formuleversie aan een productieorder koppelt, worden alle guides die aan deze versie zijn gekoppeld en ook de guides die aan de bovenliggende route van die versie zijn gekoppeld, weergegeven in de taak.
- Als u verschillende routebewerkingsrelaties definieert die de relatie *Alle* bevatten en hieraan guides toewijst, worden alleen de guides van de meest specifieke relatie voor de taak weergegeven.  

![Diagram voor het oplossen van de relevante guides.](media/instruction-guides-Resolve.png "Diagram voor het oplossen van de relevante guides")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Schaaleenheden voor Cloud en Edge voor workloads voor productie en magazijnbeheer
description: Dit onderwerp geeft informatie over schaaleenheden voor Cloud en Edge voor workloads voor productie en magazijnbeheer.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3a23ee452535423684c6d210a448ee768379fa08
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516760"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Schaaleenheden voor Cloud en Edge voor workloads voor productie en magazijnbeheer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

De schaaleenheden voor Cloud en Edge maken distributie van de workloads voor de werkvloer en magazijn tussen verschillende omgevingen mogelijk. Deze functionaliteit kan helpen de prestaties te verbeteren, serviceonderbrekingen te voorkomen en de uptime te maximaliseren. Deze wordt geleverd door de volgende invoegtoepassingen:

- Invoegtoepassing Cloud schaaleenheid voor Dynamics 365 Supply Chain Management
- Invoegtoepassing Edge schaaleenheid voor Dynamics 365 Supply Chain Management

Bedrijven die werken met productie en distributie moeten belangrijke bedrijfsprocessen 24x7 kunnen uitvoeren, zonder onderbreking en op schaal. Met behulp van de schaaleenheden voor Cloud en Egde kunnen bedrijven belangrijke bedrijfskritische productie- en magazijnprocessen zonder onderbreking uitvoeren, zelfs niet wanneer deze met incidentele problemen met netwerkverbindingen of latentie te kampen krijgen.

## <a name="public-preview-information"></a>Informatie over openbare preview

De preview bevat één omgeving die fungeert als een cloud-hub van uw Dynamics 365 Supply Chain Management-omgeving en een omgeving die fungeert als een Cloud schaaleenheid.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Beschikbaarheid van de preview

De preview voor schaaleenheden voor Cloud en Egde wordt in oktober 2020 beschikbaar voor bestaande klanten van Supply Chain Management.

oor toegang tot de preview-release 10.0.15/platformupdate 39 van oktober voor implementatie in uw [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2)-omgeving moet u deel uitmaken van het Preview Early Access-programma (PEAP) voor Supply Chain Management. U kunt deelnemen aan PEAP als u al lid bent van het bredere [Dynamics Insider Program](https://experience.dynamics.com/insider). Selecteer het programma met de naam 'Finance + Operations: Preview Early Access-programma (PEAP).'

> [!IMPORTANT]
> De schaaleenheidsmogelijkheid voor Supply Chain Management is alleen beschikbaar voor u als u akkoord gaat met de [Voorwaarden voor Cloud + Edge Preview voor Finance and Operations](https://Aka.ms/SCMCnETerms).

### <a name="data-processing-for-the-preview"></a>Gegevensverwerking voor de preview

Tijdens de openbare preview worden sommige beheerservices alleen in de Verenigde Staten gehost. Wanneer de functie echter algemeen beschikbaar wordt, zijn deze beheerservices beschikbaar in alle geografieën die worden ondersteund door Supply Chain Management. Dit is van invloed op de overdracht en opslag van beheerinformatie die door de schaaleenhedenbeheerder wordt gebruikt, waaronder:

- Uw tenant-namen en -id's
- Uw LCS project-id's
- E-mailadressen van beheerders die zijn gebruikt om zich aan te melden
- Omgevings-id's voor hub en schaaleenheden
- Configuraties van workloads
- Verzamelde meetgegevens (zoals latentie en doorvoer), die worden weergegeven op de pagina voor kaartanalyse

Gegevens die zijn overgebracht naar en opgeslagen in de Amerikaanse datacenters, worden verwijderd wanneer de preview-omgevingen worden afgesloten.

### <a name="sign-up-for-the-preview"></a>Meld u aan voor de preview

Om u aan te melden voor de Cloud en Edge-preview voor Supply Chain Management, moet uw organisatie al beschikken over een actieve cloudomgeving voor Supply Chain Management.

De mogelijkheden voor schaaleenheden zijn momenteel in openbare preview. Wanneer u zich aanmeldt, moet u een gebruikersaccount voor de specifieke tenant gebruiken. U moet ook een projecteigenaar of een omgevingsbeheerder in LCS zijn voor een actief Dynamics 365 LCS-project in die tenant.

Wanneer u zich aanmeldt voor de preview, selecteert u een tenant en gaat u door met de aanmeldingsstappen. Zodra Microsoft de preview-capaciteit kan toewijzen, sturen we u een e-mail met daarin de inrichtingsgegevens en de promotiecodes voor twee omgevingen (een hub en een schaaleenheid) voor het desbetreffende LCS-project. Vervolgens kunt u de twee omgevingen als fase 2-sandbox-omgevingen implementeren. Deze omgevingen zijn 60 dagen geldig vanaf de aanmaakdatum van de promotiecodes. U kunt de twee omgevingen pas gebruiken als de stap die in de volgende alinea is beschreven, is voltooid.

Nadat u bij Microsoft hebt bevestigd dat de twee omgevingen zijn geïmplementeerd met behulp van de promotiecodes, wordt een van de omgevingen geconfigureerd als een hub en de andere als een schaaleenheid. U kunt vervolgens de schaaleenheden configureren en geselecteerde magazijnbeheer- en productieworkloads implementeren met behulp van de [Portal voor schaaleenhedenbeheer](https://aka.ms/SCMSUM).

Preview-omgevingen worden na 60 dagen automatisch verwijderd. Ze kunnen echter eerder worden verwijderd als ze kennelijk niet worden gebruikt. Nadat de preview-omgevingen zijn verwijderd, kunt u zich aanmelden en in de wachtrij staan voor een nieuwe preview-implementatie.

Als u zich wilt aanmelden voor de preview, gaat u naar de [Portal voor schaaleenhedenbeheer](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Beperkingen die van toepassing zijn tijdens de evaluatieperiode

> [!IMPORTANT]
> Voor de eerste fase van het previewprogramma voor deze functie ondersteunt Microsoft alleen hubs met een schaaleenheid voor de cloud, niet voor hubs met Edge-schaaleenheden. Edge-schaaleenheden worden on-premises geïnstalleerd en zullen naar verwachting beschikbaar worden tijdens een aanstaande fase van het programma.

Omdat de schaaleenheden van cloud en edge een preview-functie zijn, zijn de services die hieraan zijn gekoppeld, momenteel slechts beschikbaar in beperkte landen en regio's. Door schaaleenheden voor cloud en edge in te schakelen, bevestigt u dat bepaalde gegevens die zijn gerelateerd aan de configuratie en verwerking van cloud- en edge-schaaleenheden, kunnen worden opgeslagen in een datacenter in de Verenigde Staten. Door cloud- en edge-schaaleenheden in te schakelen, gaat u ook akkoord met de [Voorwaarden voor de Cloud + Edge Preview voor Finance and Operations](https://Aka.ms/SCMCnETerms). Zie de [documentatie](https://aka.ms/scmcne) voor meer informatie over de schaaleenheden voor cloud en edge.

Uw privacy is belangrijk voor Microsoft. Lees onze [Privacyverklaring](https://aka.ms/privacy) voor meer informatie.

> [!IMPORTANT]
> Sommige bedrijfsfuncties worden niet volledig ondersteund in de openbare preview wanneer workloads worden gebruikt voor schaaleenheden. Voor meer informatie over de functionele workloads, zie de secties verderop in dit onderwerp.

## <a name="scale-units-and-dedicated-workloads"></a>Schaaleenheden en toegewezen workloads

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 met schaaleenheden":::

Schaaleenheden bereiden uw centrale Supply Chain Management-hubomgeving uit met extra toegewezen verwerkingscapaciteit. Schaaleenheden kunnen in de cloud worden uitgevoerd. U kunt ze ook op de edge van uw lokale faciliteit gebruiken. De schaaleenheden kunnen tijdelijk worden losgekoppeld van de hub-omgeving. Wanneer deze zijn verbonden, ontvangen schaaleenheden alle informatie die nodig is om de toegewezen verwerking uit te voeren voor toegewezen workloads.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Opties voor schaaleenheden in de openbare preview":::

Voor de openbare preview kunt u een hub-omgeving met geselecteerde workloads configureren op een cloud-schaaleenheid met behulp van de portal voor schaaleenhedenbeheer. Preview-deelnemers die toegang hebben tot een LBD (Local Business Data) on-premises-omgeving, kunnen de LBD-omgeving ook configureren als edge-schaaleenheid.

Een workload is een gedefinieerde set bedrijfsfunctionaliteit die kan worden weggelaten en overgedragen aan een schaaleenheid. Op dit moment bevat de preview twee typen workloads:

- Productieregistratie
- Magazijnbeheer

U kunt een van elk type workload per schaaleenheid toewijzen. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Toegewezen workloadfuncties voor productie-uitvoering in een schaaleenheid

Voor productie-uitvoering, leveren cloud- en edge-schaaleenheden de volgende mogelijkheden, zelfs wanneer de edge-eenheden niet zijn verbonden met de cloud:

- Machineoperators en werkvloersupervisors kunnen toegang krijgen tot het operationele productieplan.
- Machineoperators kunnen het plan up-to-date houden door afzonderlijke en procesproductietaken uit te voeren.
- De werkvloersupervisor kan het operationele plan aanpassen.
- Medewerkers hebben toegang tot tijd en aanwezigheid voor in- en uitklokken op de edge, om de juiste salarisberekening voor medewerkers te garanderen.

Zie de [workload-details van productieschaaleenheid](cloud-edge-workload-manufacturing.md) voor meer informatie.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Toegewezen workloadfuncties voor magazijnbeheer in een schaaleenheid

Voor magazijnbeheer leveren cloud- en edge-schaaleenheden de volgende mogelijkheden, zelfs wanneer er geen edge-eenheden zijn verbonden met de cloud:

- De verwerking van geselecteerde wave-methoden is ingeschakeld voor verkooporders en vraagaanvulling.
- Magazijnmedewerkers kunnen in de magazijn-app het werk voor verkoop en aanvulling van het magazijn uitvoeren.
- Magazijnmedewerkers kunnen in de magazijn-app de voorhanden voorraad opzoeken.
- Magazijnmedewerkers kunnen in de magazijn-app voorraadbewegingen maken en uitvoeren.
- Magazijnmedewerkers kunnen in de magazijn-app inkooporders registreren en wegzetwerk doen.

Zie de [workload-details van magazijnschaaleenheid](cloud-edge-workload-warehousing.md) voor meer informatie.

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Schaaleenheden onboarden voor uw Supply Chain Management-omgeving

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>De preview voor cloud- en edge-schaaleenheden implementeren

In de volgende afbeelding ziet u de aanmeldings- en inrichtingsstroom voor de openbare preview voor de cloud-schaaleenheden.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Aanmeldingsstappen voor de preview":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>Uw LCS-project-tenant selecteren en het gedetailleerde preview-proces

In de openbare preview toont de [portal voor schaaleenhedenbeheer](https://aka.ms/SCMSUM) de lijst met tenants waarvan uw account deel uitmaakt en waar u eigenaar of een omgevingsbeheerder voor een LCS-project bent.

Als de tenant die u zoekt niet in deze lijst voorkomt, gaat u naar [LCS](https://lcs.dynamics.com/v2) en controleert u of u een omgevingsbeheerder of een projecteigenaar bent van het LCS-project voor die tenant. Alleen Azure Active Directory (Azure AD)-accounts van de geselecteerde tenant zijn geautoriseerd om de aanmeldingservaring te voltooien.

> [!NOTE]
> Nadat u wijzigingen hebt toegepast op LCS, kan het tot 30 minuten duren voordat de lijst met tenants de wijzigingen weergeeft.

Voor elke tenant wordt in de lijst de status van de aanmelding weergegeven.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Aanmeldingsoptie voor een tenant":::

Schakel het selectievakje **Klik hier om u aan te melden** in om uw LCS-tenant te registreren om deel te nemen aan de preview. U moet de voorwaarden accepteren. U moet ook een zakelijk e-mailadres opgeven waar Microsoft berichten met betrekking tot het aanmeldingsproces voor de preview kan verzenden.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Aanmelding indienen voor een tenant":::

Microsoft zal uw aanvraag beoordelen en u op de hoogte brengen van de volgende stappen door een e-mailbericht te verzenden naar het adres dat u hebt opgegeven op het aanmeldingsformulier.

Nadat u toegang hebt gekregen tot het preview-programma, ontvangt u twee promotiecodes voor uw LCS-project. U kunt deze promotiecodes nu gebruiken om twee omgevingen in LCS te implementeren. De omgevingen moeten PEAP-release 10.0.15 of hoger gebruiken. Wanneer u de promotiecodes hebt toegepast, geeft u dit aan Microsoft door (volgens de instructie), zodat we de omgevingen voor de preview-functies kunnen inschakelen. Microsoft laat u weten wanneer deze configuratiestap is voltooid.

U kunt nu schaaleenheden en workloads configureren in uw preview-omgeving.

> [!IMPORTANT]
> Wanneer u cloud-schaaleenheden configureert, kunt u [alle vereiste stappen uitvoeren in de portal voor schaaleenheid-beheer](#scale-unit-manager-portal).
<!-- >
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Cloud-schaaleenheden en workloads beheren via de portal voor schaaleenhedenbeheer

Ga naar de [portal voor schaaleenhedenbeheer](https://aka.ms/SCMSUM) en meld u aan met uw tenant-account. Op de pagina **Schaal eenheden configureren** kunt u een hub-omgeving toevoegen als deze nog niet wordt weergegeven. U kunt vervolgens de hub selecteren die u wilt configureren met schaaleenheden en workloads.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Schaaleenheid- en workloadbeheerervaring":::

Selecteer **Schaaleenheden toevoegen** om een of meer schaaleenheden toe te voegen die beschikbaar zijn in uw topologie. In de preview wordt de cloud-schaaleenheid weergegeven die u hebt geïmplementeerd vanuit een van de promotiecodes die u hebt ontvangen als onderdeel van het preview-programma.

<!-- > [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

Op het tabblad **Gedefinieerde workloads** kunt u de knop **Workload maken** gebruiken om een magazijnbeheer- of een productie-uitvoeringsworkload toe te voegen aan een van uw schaaleenheden. Voor elke workload moet u de context opgeven van de processen waarvan de workload de eigenaar is. Voor magazijnbeheerworkloads is de context een specifiek magazijn in een specifieke locatie en rechtspersoon. Voor productie-uitvoeringsworkloads is de context een specifieke locatie in een rechtspersoon.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Workloads maken":::

> [!IMPORTANT]
> Met de portal voor schaaleenhedenbeheer in de preview kunt u geen workloads verwijderen uit schaaleenheden of een schaaleenheid van een hub opheffen nadat de toewijzing is gemaakt. Als u een toewijzing moet verwijderen, neemt u contact op met uw contactpersoon voor preview-programmabeheer.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->

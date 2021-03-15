---
title: De uitvoeringsinterface voor de werkvloer configureren
description: In dit onderwerp wordt beschreven hoe u een of meer configuraties maakt voor de uitvoeringsinterface van de werkvloer. Wanneer u de uitvoeringsinterface van de werkvloer opent, worden automatisch een geselecteerde configuratie en een taakfilter geladen die specifiek zijn voor de browser en het apparaat. In de configuratie stelt u de beleidsregels in die toegepast moeten worden op een specifiek gebruik.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e822463ac80be3b1e498f02cb1aad2b214fed815
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077472"
---
# <a name="configure-the-production-floor-execution-interface"></a>De uitvoeringsinterface voor de werkvloer configureren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Medewerkers op de werkvloer gebruiken de uitvoeringsinterface van de werkvloer om hun dagelijkse werkzaamheden te registreren, bijvoorbeeld wanneer taken worden gestart, feedback over taken wordt geregistreerd, indirecte activiteiten worden geregistreerd en verzuim wordt gerapporteerd. Deze registraties vormen de basis voor het bijhouden van de voortgang en de kosten van productieorders, en voor het berekenen van de basis voor het salaris van de werknemers.

Wanneer u de uitvoeringsinterface van de werkvloer opent, worden automatisch een geselecteerde configuratie en een taakfilter geladen die specifiek zijn voor de browser en het apparaat. In de configuratie stelt u de beleidsregels in die toegepast moeten worden op een specifiek gebruik. Hieronder vindt u een aantal gebruiksvoorbeelden:

- Op een apparaat in de bedrijfshal klokken werknemers in wanneer ze binnenkomen op kantoor en ze klokken uit wanneer ze weer naar huis gaan.
- Op een apparaat op de werkvloer registreren machinewerkers wanneer ze taken starten en voltooien. Ze registreren ook pauzes en indirecte activiteiten.

In dit onderwerp worden de verschillende opties beschreven voor het configureren van taakkaartapparaten.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>De uitvoeringsinterface voor de werkvloer en de bijbehorende optionele functies inschakelen

De uitvoeringsinterface voor de werkvloer zelf, plus een aantal optionele instellingen die in dit onderwerp worden beschreven, moeten in uw systeem zijn ingeschakeld voordat u ze kunt gebruiken. Gebruik de pagina [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om een of meer van de functies die in de volgende subsecties worden beschreven, in te schakelen.

### <a name="the-production-floor-execution-interface"></a>De uitvoeringsinterface voor de werkvloer

Dit is de primaire functie die in dit onderwerp wordt beschreven. Hiermee wordt de uitvoeringsinterface voor de werkvloer aan uw systeem toegevoegd. Schakel deze in door de volgende functie in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in te schakelen:  
- Uitvoering werkvloer

### <a name="generate-license-plates"></a>Nummerplaten genereren

Deze functies maken de functionaliteit voor nummerplaten beschikbaar voor de uitvoeringsinterface voor de werkvloer. Als u ze wilt gebruiken, schakelt u de volgende functies in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in (in deze volgorde):

1. Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten
1. Het automatisch genereren van nummerplaatnummers inschakelen bij het gereedmelden in het apparaat voor taakkaarten

### <a name="print-labels"></a>Etiketten afdrukken

Deze functies maken de functionaliteit voor het afdrukken van labels beschikbaar voor de uitvoeringsinterface voor de werkvloer. Als u ze wilt gebruiken, schakelt u de volgende functies in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in (in deze volgorde):

1. Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten
1. Label afdrukken vanaf apparaat voor taakkaart

### <a name="allow-locking-the-touch-screen"></a>Vergrendeling van het aanraakscherm toestaan

Deze functie voegt een knop toe aan de uitvoeringsinterface voor de werkvloer waarmee werknemers het aanraakscherm kunnen opschonen. Als u hier gebruik van wilt maken, schakelt u de volgende functie in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in:

- Functie voor vergrendelen van taakkaartapparaat en taakkaartterminal zodat ze kunnen worden schoongemaakt

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Functionaliteit van activabeheer voor de uitvoeringsinterface voor de werkvloer

Met deze functie voegt u een Activabeheer-tabblad toe aan de interface voor het uitvoeren van productielijnen. Werknemers kunnen dit tabblad gebruiken om een activum te selecteren dat is verbonden met een machineresource die zich in het geselecteerde filter van de takenlijst bevindt. Voor de geselecteerde machineactiva kan de werknemer de status en de staat van het activum uit tellerwaarden weergeven voor maximaal vier geselecteerde tellers. Als u deze functie wilt gebruiken, schakelt u de volgende functie in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in:

- Functionaliteit van activabeheer voor de uitvoeringsinterface voor de werkvloer

## <a name="work-with-production-floor-execution-configurations"></a>Werken met uitvoeringsconfiguraties voor de werkvloer

Als u de apparaatconfiguraties wilt maken en beheren, gaat u naar productie **Productiebeheer \> Instellen \> Productie-uitvoering \> Uitvoering werkvloer configureren**. Op de pagina **Uitvoering werkvloer configureren** wordt een lijst met bestaande configuraties weergegeven. Op deze pagina kunt u de volgende acties uitvoeren:

- Selecteer een configuratie voor de werkvloer die in de linkerkolom staat om deze weer te geven en te bewerken.
- Selecteer **Nieuw** in het actievenster om een nieuwe apparaatconfiguratie aan de lijst toe te voegen. Voer vervolgens een naam in het veld **Configuratie** in waarmee de nieuwe configuratie wordt geïdentificeerd. De naam die u invoert, moet uniek zijn voor alle apparaatconfiguraties en u kunt deze later niet bewerken.

Configureer vervolgens de verschillende instellingen voor de geselecteerde apparaatconfiguratie. De volgende velden zijn beschikbaar:

- **Hoeveelheid rapporteren bij uitklokken**: stel deze optie in op *Ja* om werknemers te vragen om bij het uitklokken feedback te rapporteren over taken die in uitvoering zijn. Als deze optie wordt ingesteld op *Nee*, wordt dit niet aan werknemers gevraagd.
- **Werknemer vergrendelen**: wanneer deze optie is ingesteld op *Nee*, worden werknemers onmiddellijk afgemeld nadat ze een registratie hebben gemaakt (zoals een nieuwe taak). Het apparaat keert dan terug naar de aanmeldingspagina. Als deze optie is ingesteld op *Ja*, blijven werknemers aangemeld bij het taakkaartapparaat. Een werknemer kan zich echter handmatig afmelden, zodat een andere werknemer zich kan aanmelden terwijl het taakkaartapparaat actief blijft onder dezelfde systeemgebruikersaccount. Meer informatie over deze typen accounts vindt u in [Toegewezen gebruikers](config-job-card-device.md#assigned-users).
- **De werkelijke registratietijd gebruiken**: stel deze optie in op *Ja* om de tijd in te stellen voor elke nieuwe registratie die gelijk is aan de exacte tijd waarop de registratie is ingediend door de werknemer. Als deze optie is ingesteld op *Nee*, wordt in plaats daarvan de aanmeldingstijd gebruikt. U stelt deze optie meestal in op *Ja* als u de opties **Werknemer vergrendelen** en/of **Eén werknemer** hebt ingesteld op *Ja*, waarbij werknemers vaak aangemeld blijven gedurende langere perioden.
- **Eén werknemer**: stel deze optie in op *Ja* als slechts één werknemer elk taakkaartapparaat gebruikt waarvoor deze configuratie actief is. Als deze optie is ingesteld op *Ja*, wordt de optie **Werknemer vergrendelen** automatisch ingesteld op *Ja*. Bovendien wordt met deze instelling de vereiste (en de mogelijkheid) voor de werknemer om zich aan te melden met behulp van een badge-id (of een andere vergelijkbare id) verwijderd. In plaats daarvan meldt de werknemer zich aan bij Microsoft Dynamics 365 Supply Chain Management met een systeemgebruikersaccount die is gekoppeld aan een *werknemer met tijdregistratie* (uit de tabel *werknemers*) en wordt op hetzelfde moment aangemeld bij het taakkaartapparaat als die werknemer.
- **Vergrendeling van het aanraakscherm toestaan**: stel deze optie in op *Ja* om werknemers in staat te stellen het aanraakscherm van het taakkaartapparaat te vergrendelen zodat ze het kunnen schoonmaken. Als deze optie is ingesteld op *Ja*, wordt de knop **Scherm vergrendelen voor schoonmaken** toegevoegd aan de aanmeldingspagina van het apparaat. Wanneer een werknemer deze knop selecteert, wordt het aanraakscherm tijdelijk vergrendeld voor onbedoelde invoer. Er wordt ook een aftellingstimer weergegeven. De werknemer kan het apparaat en het scherm vervolgens veilig schoonmaken. Wanneer de timer is afgelopen, wordt het aanraakscherm automatisch ontgrendeld.
- **Duur schermvergrendeling**: wanneer de optie **Vergrendeling van het aanraakscherm toestaan** is ingesteld op *Ja*, gebruikt u deze optie om het aantal seconden op te geven dat het aanraakscherm moet worden vergrendeld voor schoonmaken. De duur moet tussen 5 en 120 seconden liggen.
- **Nummerplaat genereren**: stel deze optie in op *Ja* om voor elke gereedmelding op het taakkaartapparaat een nieuwe nummerplaat te genereren. Het nummerplaatnummer wordt gegenereerd op basis van een nummerreeks die is ingesteld op de pagina **Parameters voor magazijnbeheer**. Als deze optie is ingesteld op *Nee*, moeten werknemers een bestaande nummerplaat opgeven bij het gereedmelden.
- **Label afdrukken**: stel deze optie in op *Ja* om een nummerplaatlabel af te drukken wanneer de werknemer het taakkaartapparaat gebruikt voor de gereedmelding. De configuratie van het label wordt ingesteld in de documentroutering, zoals wordt beschreven in de [Indeling van documentroutering voor nummerplaatlabels](../warehousing/document-routing-layout-for-license-plates.md).
- **Tabbladselectie**: gebruik de instellingen in deze sectie om te kiezen welke tabbladen moeten worden weergegeven door de uitvoeringsinterface voor de werkvloer wanneer de huidige configuratie actief is. U kunt zo veel tabbladen ontwerpen als u nodig hebt en deze vervolgens hier toevoegen en rangschikken. Zie [De uitvoeringsinterface voor de werkvloer ontwerpen](production-floor-execution-tabs.md) voor meer informatie over het ontwerpen van tabbladen en het werken met de instellingen.

## <a name="clean-up-job-configurations"></a>Taakconfiguraties opschonen

Wanneer de werkvloersupervisor de uitvoeringsinterface van de werkvloer instelt, selecteert hij/zij een configuratie en een taakfilter. Deze selecties worden opgeslagen in een verwijzingstabel in Supply Chain Management en de browser gebruikt een ID die is opgeslagen in een lokale cookie om de juiste rij in die tabel te vinden. In de tabel worden ook de datum en tijd geregistreerd waarop een werknemer bij elk apparaat voor het laatst heeft aangemeld.

Met een batchtaak worden vermeldingen in de verwijzingstabel periodiek opgeschoond voor apparaten die gedurende de laatste 60 dagen geen activiteit hebben geregistreerd. U kunt de vermeldingen ook op elk gewenst moment handmatig opschonen door de volgende stappen uit te voeren.

1. Ga naar **Productiebeheer \> Instellen \> Productie-uitvoering \> Uitvoering werkvloer configureren**.
1. Selecteer in het actievenster de optie **Clientconfiguraties opschonen**.
1. Stel in het dialoogvenster **Clientconfiguratie opschonen** het veld **Aantal dagen** in op het aantal dagen inactiviteit (vóór vandaag) dat u in aanmerking wilt nemen. U verwijdert alle configuraties en aanmeldingsrecords voor apparaten die gedurende die tijd niet actief zijn geweest.
1. Selecteer **OK** om de relevante configuraties op basis van de instelling **Aantal dagen** op te schonen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
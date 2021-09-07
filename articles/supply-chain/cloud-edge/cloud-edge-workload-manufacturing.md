---
title: Productie-uitvoeringsworkloads voor cloud- en edge-schaaleenheden
description: In dit onderwerp wordt beschreven hoe productie-uitvoeringsworkloads werken met cloud- en edge-schaaleenheden.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 77e0a0e0eb47c331b2b219dc523ecd2c706a4638
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345293"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Werkbelasting voor productie-uitvoering voor cloud- en randschaaleenheden

[!include [banner](../includes/banner.md)]

> [!WARNING]
> De werkbelasting voor productie-uitvoering is op dit moment als voorbeeld beschikbaar.
> Sommige bedrijfsfuncties worden niet volledig ondersteund in de openbare preview wanneer workloadschaaleenheden worden gebruikt.

In de productie-uitvoering leveren schaaleenheden de volgende mogelijkheden:

- Machineoperators en werkvloersupervisors kunnen toegang krijgen tot het operationele productieplan.
- Machineoperators kunnen het plan up-to-date houden door afzonderlijke en procesproductietaken uit te voeren.
- De werkvloersupervisor kan het operationele plan aanpassen.
- Medewerkers hebben toegang tot tijd en aanwezigheid voor in- en uitklokken op de edge, om de juiste salarisberekening voor medewerkers te garanderen.

In dit onderwerp wordt beschreven hoe productie-uitvoeringsworkloads werken met cloud- en edge-schaaleenheden.

## <a name="the-manufacturing-lifecycle"></a>De levenscyclus van productie

Zoals in de volgende afbeelding wordt weergegeven, is de productielevenscyclus onderverdeeld in drie fasen: *Plannen*, *Uitvoeren* en *Voltooien*.

[![Productie-uitvoeringsfasen wanneer één omgeving wordt gebruikt](media/mes-phases.png "Productie-uitvoeringsfasen wanneer er één omgeving wordt gebruikt.")](media/mes-phases-large.png)

De _planfase_ omvat productdefinitie, planning, het maken en plannen van orders en vrijgave. De vrijgavestap geeft de overgang van de _planfase_ naar de _uitvoeringsfase_ aan. Wanneer een productieorder wordt vrijgegeven, worden de productieordertaken weergegeven op de productievloer en zijn ze klaar voor uitvoering.

Wanneer een productietaak is gemarkeerd als voltooid, wordt deze verplaatst van _uitvoeringsfase_ naar de _voltooiingsfase_. In de _voltooiingsfase_ gaan de registraties van de *uitvoeringsfase* door een goedkeuringswerkstroom, waar ze worden berekend, goedgekeurd en overgebracht. Op dat moment is de productieorder voltooid. Dan wordt de basis voor het salaris van de medewerkers gegenereerd.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>De uitvoeringsfase opsplitsen in een afzonderlijke workload

Zoals u in de volgende afbeelding kunt zien, wordt de _uitvoeringsfase_ een afzonderlijke workload opgesplitst wanneer er schaaleenheden worden gebruikt.

[![Productie-uitvoeringsfasen wanneer er schaaleenheden worden gebruikt](media/mes-phases-workloads.png "Productie-uitvoeringsfasen wanneer er schaaleenheden worden gebruikt.")](media/mes-phases-workloads-large.png)

Het model gaat nu van een installatie met één exemplaar naar een model dat is gebaseerd op hub en schaaleenheden. De _planfase_ en _voltooiingsfase_ worden uitgevoerd als back-upbewerkingen op de hub en de productie-uitvoeringsworkload wordt uitgevoerd op de schaaleenheden. Gegevens worden asynchroon overgebracht tussen de hub en schaaleenheden.

Wanneer een productieorder op de hub wordt vrijgegeven, worden alle gegevens die nodig zijn voor het verwerken van productietaken, overgebracht naar de schaaleenheid. Deze gegevens omvatten productieorders, productieroutes, stuklijsten en producten. Gegevens die niet zijn gerelateerd aan een productieorder (zoals indirecte activiteiten, verzuimcodes en productieparameters), worden ook van de hub overgezet naar de schaaleenheid. In de regel kunnen gegevens die afkomstig zijn van de hub en die worden overgebracht naar de schaaleenheid, alleen op de hub worden gemaakt of bijgewerkt. Er kan bijvoorbeeld geen nieuwe verzuimcode of indirecte activiteit worden gemaakt op de schaaleenheid&mdash;die kan alleen voor registratie worden gebruikt. De registraties die tijdens de uitvoering op de schaaleenheid worden uitgevoerd, worden vervolgens naar de hub overgebracht, waar tijd- en aanwezigheidsgoedkeuring, voorraad en financiële updates worden verwerkt.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Productie-uitvoeringstaken die kunnen worden uitgevoerd op workloads

De volgende productie-uitvoeringstaken kunnen momenteel worden uitgevoerd op workloads wanneer er schaaleenheden worden gebruikt:

- Inklokken, aanmelden, uitklokken en verzuim
- Taak beginnen
- Taken bundelen
- Voortgang melden
- Uitval rapporteren
- Indirecte activiteit
- Pauze
- Gereedmelden en wegzetten (vereist dat u ook de werkbelasting van de magazijnuitvoering op uw schaaleenheid uitvoert, zie ook [Gereedmelden en wegzetten in een schaaleenheid](#RAF))

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Werken met productie-uitvoeringsworkloads op de hub

Gewoonlijk worden de processen die nodig zijn om de productie-uitvoeringsworkloads uit te voeren, automatisch uitgevoerd om de hub en alle schaaleenheden waar nodig synchroon te houden. Als u echter problemen ondervindt, kunt u handmatig de verwerking van onbewerkte registraties activeren die worden ontvangen van workloads en/of het registratieverwerkingslogbestand controleren.

### <a name="manually-process-raw-registrations"></a>Onbewerkte registraties handmatig verwerken

Een batchtaak in Supply Chain Management wordt automatisch uitgevoerd om alle registraties te verwerken die van de workloads zijn ontvangen. Met deze taak worden de vereiste productiejournalen en logbestandsvermeldingen gemaakt wanneer een registratie wordt verwerkt voor een voltooide taak in de workload.

Hoewel de taak normaal gesproken automatisch wordt uitgevoerd, kunt u deze op elk gewenst moment handmatig uitvoeren door u aan te melden bij de hub en naar **Productiecontrole \> Periodieke taken \> Backoffice workloadbeheer \> Onbewerkte registraties verwerken** te gaan.

### <a name="check-the-raw-registration-processing-log"></a>Het verwerkingslogbestand voor onbewerkte registraties controleren

Als u het registratieverwerkingslogbestand wilt bekijken, meldt u zich aan bij de hub en gaat u naar **Productiecontrole \> Periodieke taken \> Backoffice workloadbeheer \> Logbestand onbewerkte registratieverwerking**. Op de pagina **Logbestand voor onbewerkte registratieverwerking** wordt een lijst met verwerkte onbewerkte registraties en de status van elke registratie weergegeven.

![De pagina Logbestand voor onbewerkte registratieverwerking.](media/mes-processing-log.png "De pagina Logbestand voor onbewerkte registratieverwerking")

U kunt aan elke registratie in de lijst werken door deze te selecteren en vervolgens een van de volgende knoppen in het actiedeelvenster te selecteren:

- **Verwerken**: de geselecteerde registratie handmatig verwerken. Deze actie kan handig zijn als de taak _Onbewerkte registraties verwerken_ niet is uitgevoerd of als deze is mislukt.
- **Annuleren**: de geselecteerde registratie annuleren.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Werken met productie-uitvoeringsworkloads op een schaaleenheid

Gewoonlijk worden de processen die nodig zijn om de productie-uitvoeringsworkloads uit te voeren, automatisch uitgevoerd om de hub en alle schaaleenheden waar nodig synchroon te houden. Als u echter problemen ondervindt, kunt u de geschiedenis van orders controleren die op een schaaleenheid zijn verwerkt of handmatig de taak _Berichtverwerker productiehub naar schaaleenheid_ uitvoeren.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>De geschiedenis weergeven van de productietaken die op een schaaleenheid zijn verwerkt

Als u de geschiedenis wilt weergeven van de productietaken die op een schaaleenheid zijn verwerkt, meldt u zich aan bij de computer voor de schaaleenheid en gaat u naar **Productiecontrole \> Periodieke taken \> Backoffice workloadbeheer \> Verwerkingsgeschiedenis van productietaken**. Op de pagina **Verwerkingsgeschiedenis van productietaken** wordt de verwerkingsgeschiedenis van de productieorders op de schaaleenheid weergegeven. U kunt aan elke productieorder in de lijst werken door deze te selecteren en vervolgens een van de volgende knoppen in het actiedeelvenster te selecteren:

- **Verwerken**: de geselecteerde productieorder handmatig verwerken.
- **Annuleren**: de geselecteerde productieorder annuleren.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>De taak Berichtverwerker productiehub naar schaaleenheid

De taak _Berichtverwerker productiehub naar schaaleenheid_ verwerkt gegevens van de hub naar de schaaleenheid. Deze taak wordt automatisch gestart wanneer de productie-uitvoeringsworkload wordt geïmplementeerd. U kunt dit echter op elk gewenst moment handmatig uitvoeren door naar **Productiecontrole \> Periodieke taken \> Backoffice workloadbeheer \> Berichtverwerker productiehub naar schaaleenheid** te gaan.

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a>Gereedmelden en wegzetten in een schaaleenheid

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

In de huidige versie worden de bewerkingen voor gereedmelden en wegzetten (voor eindproducten, coproducten en bijproducten) ondersteund door de [werkbelasting voor magazijnuitvoering](cloud-edge-workload-warehousing.md) (niet door de werkbelasting van de productie-uitvoering). Als u deze functionaliteit wilt gebruiken wanneer deze is gekoppeld aan een schaaleenheid, moet u daarom het volgende doen:

- Installeer zowel de werkbelasting voor magazijnuitvoering als de werkbelasting voor de productie-uitvoering in uw schaaleenheid.
- Gebruik de mobiele app Warehouse Management om gereed te melden en het wegzetwerk te verwerken. Deze processen worden momenteel niet ondersteund in de uitvoeringsinterface voor de productievloer.

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

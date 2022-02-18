---
title: Configuratiesleutels en gegevensentiteiten
description: In dit onderwerp wordt de relatie tussen configuratiesleutels en gegevensentiteiten beschreven.
author: peakerbl
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: e9cc92563c426136b2543511ad943fd64b335b70
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065734"
---
# <a name="configuration-keys-and-data-entities"></a>Configuratiesleutels en gegevensentiteiten

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Voordat u gegevensentiteiten gebruikt om gegevens te importeren of exporteren, is het raadzaam dat u eerst bepaalt wat het effect van configuratiesleutels is op de gegevensentiteiten die u van plan bent te gebruiken.

Zie voor meer informatie over configuratiesleutels het [rapport Licentiecodes en configuratiesleutels](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Configuratiesleuteltoewijzingen
Configuratiesleutels kunnen worden toegewezen aan een of alle van de volgende artefacten.

- Gegevensentiteiten
- Tabellen gebruikt als gegevensbronnen
- Tabelvelden
- Gegevensentiteitsvelden

In de volgende tabel ziet u hoe configuratiesleutelwaarden op de verschillende artefacten achter een object de verwachte werking van het object wijzigen.

| Instelling van configuratiesleutel voor gegevensentiteit | Instelling van configuratiesleutel voor tabel | Instelling van configuratiesleutel voor tabelveld | Configuratiesleutel voor gegevensentiteitveld | Verwacht gedrag |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| Uitgeschakeld                                | Niet geëvalueerd                      | Niet geëvalueerd                            | Niet geëvalueerd                          | Als de configuratiesleutel voor de gegevensentiteit is uitgeschakeld, functioneert de gegevensentiteit niet. Het maakt niet uit of de configuratiesleutels in de onderliggende tabellen en velden zijn in- of uitgeschakeld. |
| Ingeschakeld                                 | Uitgeschakeld                           | Niet geëvalueerd                            | Niet geëvalueerd                          | Als de configuratiesleutel voor een gegevensentiteit is ingeschakeld, controleert het gegevensbeheerframework de configuratiesleutel voor elk van de onderliggende tabellen. Als de configuratiesleutel voor een tabel is uitgeschakeld, is die tabel niet beschikbaar in de gegevensentiteit voor functioneel gebruik. Als een configuratiesleutel van een tabel is uitgeschakeld, worden de instellingen van de tabel- en gegevensentiteitsleutel niet geëvalueerd. Als voor de primaire tabel in de entiteit de bijbehorende configuratiesleutel uitgeschakeld is, fungeert het systeem alsof de configuratiesleutel van de entiteit uitgeschakeld is. |
| Ingeschakeld                                 | Ingeschakeld                            | Uitgeschakeld                                 | Niet geëvalueerd                          | Als de configuratiesleutel voor een gegevensentiteit is ingeschakeld en de onderliggende tabelconfiguratiesleutels zijn ingeschakeld, controleert het gegevensbeheerframework de configuratiesleutel van de velden in de tabellen. Als de configuratiesleutel voor een veld is uitgeschakeld, is dat veld niet beschikbaar in de gegevensentiteit voor functioneel gebruik, zelfs als het corresponderende gegevensentiteitveld de configuratiesleutel ingeschakeld heeft. |
| Ingeschakeld                                 | Ingeschakeld                            | Ingeschakeld                                  | Uitgeschakeld                               | Als de configuratiesleutel is ingeschakeld op alle andere niveaus, maar de configuratiesleutel van het entiteitsveld niet is ingeschakeld, is het veld niet beschikbaar voor gebruik in de gegevensentiteit. |

> [!NOTE]
> Als een entiteit een andere entiteit als gegevensbron heeft, wordt de bovenstaande logica op recursieve wijze toegepast.

### <a name="entity-list-refresh"></a>Entiteitslijst vernieuwen
Wanneer de entiteitslijst wordt vernieuwd, maakt het gegevensbeheerframework de configuratiesleutelmetagegevens voor runtimegebruik. Deze metagegevens worden gebouwd met behulp van de hierboven beschreven logica. Het wordt ten zeerste aanbevolen te wachten tot de entiteitslijst is vernieuwd voordat u taken en entiteiten in het gegevensbeheerframework gebruikt. Als u niet wacht, zijn de configuratiesleutelmetagegevens mogelijk niet up-to-date en dat kan leiden tot onverwachte resultaten. Wanneer de entiteitslijst wordt vernieuwd, wordt het volgende bericht weergegeven op de entiteitslijstpagina.

![Entiteitslijst vernieuwen.](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Pagina met gegevensentiteitlijst
De gegevensentiteitslijstpagina in de werkruimte Gegevensbeheer toont de instellingen van de configuratiesleutel voor de entiteiten. Begin vanaf deze pagina om de invloed te begrijpen van configuratiesleutels op de gegevensentiteit.

Deze informatie wordt weergegeven met de metagegevens die tijdens het vernieuwen van de entiteit worden samengesteld. De configuratiesleutelkolom bevat de naam van de configuratiesleutel die is gekoppeld aan de gegevensentiteit. Als deze kolom leeg is, betekent dit dat er geen configuratiesleutel is gekoppeld aan de gegevensentiteit. De configuratiesleutelstatuskolom bevat de status van de configuratiesleutel. Als er een vinkje staat, betekent dit dat de sleutel is ingeschakeld. Als dit veld leeg is, betekent dit dat de sleutel is uitgeschakeld of dat er geen sleutel is gekoppeld.

![Pagina met entiteitlijst.](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Doelvelden
De volgende stap is in te zoomen op de gegevensentiteit om de impact te zien van configuratiesleutels op tabellen en velden. Het doelveldenformulier voor een gegevensentiteit toont informatie over configuratiesleutels en de sleutelstatus voor de gerelateerde tabellen en velden in de gegevensentiteit. Als de gegevensentiteit zelf de bijbehorende configuratiesleutel uitgeschakeld heeft, wordt een waarschuwingsbericht weergegeven waarin wordt gemeld dat de tabellen en velden in het doelveldenformulier voor deze entiteit helemaal niet beschikbaar zullen zijn, ongeacht de status van de configuratiesleutel.

![Doelvelden.](./media/Target_fields_1.png)

### <a name="child-entities"></a>Onderliggende entiteiten 
Bepaalde entiteiten hebben andere entiteiten als gegevensbronnen of zijn samengestelde gegevensentiteiten: configuratiesleutelgegevens voor deze entiteiten worden weergegeven in het formulier Onderliggende entiteiten. Gebruik dit formulier op vergelijkbare manier als de entiteitslijstpagina die hierboven is beschreven. Het doelveldenformulier voor de onderliggende entiteit werkt ook zoals hierboven beschreven.

![Doelvelden.](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Gegevensentiteiten gebruiken
Als u het volledige effect, als dat er is, begrijpt van configuratiesleutels op de gegevensentiteiten die u wilt gebruiken, kunt u nu doorgaan met het gebruik van de gegevensentiteiten door ze toe te voegen aan gegevensprojecten. 

### <a name="run-time-validations-for-configuration-keys"></a>Runtimevalidaties voor configuratiesleutels
Met de configuratiesleutelmetagegevens die worden gemaakt tijdens het vernieuwen van de entiteitslijst worden runtimevalidaties uitgevoerd in de volgende gevallen.

- Wanneer een gegevensentiteit wordt toegevoegd aan een taak
- Wanneer de gebruiker op 'valideren' klikt in de entiteitslijst
- Wanneer de gebruiker een gegevenspakket laadt in een gegevensproject
- Wanneer de gebruiker een sjabloon laadt in een gegevensproject
- Wanneer een bestaand gegevensproject wordt geladen
- Wanneer een sjabloon wordt geladen in een gegevensproject
- Voordat de taak exporteren/importeren wordt uitgevoerd (batch, niet-batch, terugkerend, OData)
- Wanneer de gebruiker toewijzing genereert
- Wanneer de gebruiker velden in de toewijzing-UI toewijst
- Wanneer de gebruiker alleen 'importeerbare velden' toevoegt

### <a name="managing-configuration-key-changes"></a>Belangrijke configuratiesleutelwijzigingen
Elke keer dat u configuratiesleutels bijwerkt op entiteit-, tabel- of veldniveau, moet de entiteitslijst in het gegevensbeheerframework worden vernieuwd. Dit proces zorgt ervoor dat het framework de meest recente configuratiesleutelinstellingen gebruikt. Totdat de entiteitslijst is vernieuwd, wordt de volgende waarschuwing weergegeven op de entiteitslijstpagina. De bijgewerkte configuratiesleutelwijzigingen gaan direct in nadat de entiteitslijst is vernieuwd. Het wordt aangeraden om bestaande gegevensprojecten en taken te valideren om zeker te weten dat ze werken zoals verwacht nadat de configuratiesleutelwijzigingen zijn ingegaan.

![Doelvelden.](./media/Target_fields_3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

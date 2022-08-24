---
title: Inpakkingswerk voor het inpakken van uitgaande containers en het verwerken van zendingen
description: Dit artikel beschrijft het werkordertype 'Inpakken' dat het werk voor inpakken van containers beheert en gedeeltelijke verzendingen ondersteunt van ingepakte containers die zijn gerelateerd aan ladingen waarbij voorraadartikelen nog niet zijn ingepakt.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220548"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Inpakkingswerk voor het inpakken van uitgaande containers en het verwerken van zendingen

[!include [banner](../../includes/banner.md)]

Dit artikel beschrijft het werkordertype *Inpakken* dat het werk voor inpakken van containers beheert en gedeeltelijke verzendingen ondersteunt van ingepakte containers die zijn gerelateerd aan ladingen waarbij voorraadartikelen nog niet zijn ingepakt. Met inpakkingswerk kunt u de functies voor [bevestiging en overboeking](confirm-and-transfer.md) gebruiken om uitgaande zendingen te bevestigen die aan containers zijn gekoppeld.

Inpakwerk wordt automatisch gemaakt wanneer voorraad die is gerelateerd aan brondocumentwerk op locaties van het type *Inpaklocatie* wordt geplaatst. Het werk bestaat uit twee regels, een voor *orderverzamelen* en een voor *wegzetten* en wordt automatisch onderhouden als onderdeel van een proces voor het sluiten/heropenen van containers.

Zie [Containers voor verzending verpakken](packing-containers.md) voor meer informatie over het instellen en gebruiken van het containerinpakproces .

## <a name="turn-on-the-feature"></a>De functie inschakelen

Als de functies die in dit artikel worden beschreven, nog niet in het systeem aanwezig zijn, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de volgende functies in de volgende volgorde in: Beide functies maken deel uit van de module **Magazijnbeheer**.

1. *Bevestigen en overboeken*
1. *Inpakwerk voor inpakstations*

## <a name="set-up-a-location-for-packing-work"></a>Een locatie voor inpakwerk instellen

Gebruik de volgende procedure om inpaklocaties in te stellen. Voor elke locatie kunt u selecteren of het systeem automatisch inpakwerk maakt.

1. Ga naar **Magazijnbeheer \> Instellingen \> Inpakken \> Inpakstation instellen**.
1. Selecteer in het actievenster de optie **Nieuw** om een instellingsrecord voor een inpakstation toe te voegen.
1. Stel in de nieuwe record de volgende velden in:

    - **Magazijn**: selecteer of typ het magazijn waar het inpakstation zich bevindt.
    - **Location**: selecteer of typ het inpakstation. Deze locatie moet worden toegewezen aan een locatieprofiel dat het locatietype gebruikt dat op de pagina **Parameters van magazijnbeheer** is geconfigureerd als het type inpaklocatie voor uw bedrijf. Zie [Containers voor verzending verpakken](packing-containers.md) voor meer informatie.
    - **Inpakwerk maken**: schakel dit selectievakje in om inpakwerk te maken telkens als artikelen op de inpaklocatie worden geleverd. Het werk bevat koppelingen naar gerelateerde ladingregels, zodat gedeeltelijke ladingen kunnen worden ingepakt en verzonden.

## <a name="example-scenario"></a>Voorbeeldscenario

Dit voorbeeldscenario laat zien hoe u een uitgaande verkooporderstroom verwerkt door een container in te pakken en een gedeeltelijke lading te verzenden.

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

U kunt dit scenario ook gebruiken als instructie voor het gebruiken van de functie in een productiesysteem. In dat geval moet u echter uw eigen waarden opgeven voor elke instelling die hier wordt beschreven.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Inpakwerk configureren voor inpaklocatie in magazijn

Om aan de slag te kunnen, moet u het werkproces *Inpakken* configureren voor een bepaald magazijn en een specifieke locatie.

1. Ga naar **Magazijnbeheer \> Instellingen \> Inpakken \> Inpakstation instellen**.
1. Selecteer **Nieuw** in het actievenster om een instellingsrecord toe te voegen.
1. Stel in de nieuwe record de volgende waarden in:

    - **Magazijn:** *62*
    - **Locatie:** *Verpakken*
    - **Inpakwerk maken:** *Ja*

1. Sluit de pagina **Inpakstation instellen**.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Een ladingsjabloon maken waarin gedeeltelijke verzending is toegestaan

Als u wilt dat een lading verdeeld over meerdere zendingen kan worden geleverd, moet u deze koppelen aan een ladingjabloon waarmee gedeeltelijke verzending mogelijk is. Volg deze stappen om de vereiste sjabloon te maken.

1. Ga naar **Magazijnbeheer \> Instellen \> Lading \> Ladingssjablonen**.
1. Selecteer **Nieuw** in het actievenster om een instellingsrecord toe te voegen.
1. Stel in de nieuwe record de volgende waarden in:

    - **Ladingsjabloon-id:** *Gedeeltelijk*
    - **Lading splitsen toestaan tijdens verzending bevestigen:** *Ja*

1. Sluit de pagina **Ladingsjablonen**.

Zie [Bevestigen en overboeken](Confirm-and-transfer.md) voor meer informatie.

### <a name="process-a-sales-order"></a>Een verkooporder verwerken

Volg deze stappen om een verkooporder te verwerken en gedeeltelijk te verzenden.

1. Voltooi het [voorbeeldscenario](packing-containers.md#scenario) dat u vindt in [Containers inpakken voor verzending](packing-containers.md). In dat scenario maakt u een verkooporder voor twee stuks van één artikel. Vervolgens pakt u slechts een van de twee stuks in een container en sluit u de container. U moet, zoals in het scenario wordt aangegeven, een notitie maken van de zendings-id die u maakt.
1. Ga naar **Magazijnbeheer \> Werk \> Alle werk**.
1. Schakel in het filtergebied het selectievakje **Afgesloten werk weergeven** in. Voer vervolgens de zendings-ID in het veld **Filter** in en selecteer of u wilt filteren op **zendings-ID**-waarde . U moet nu drie werkkopteksten zien. Eén is voor het orderverzamelen voor verkooporders en heeft de status *Afgesloten*. Twee zijn voor het inpakproces: een is gerelateerd aan de afgesloten container en heeft de status *Afgesloten*, de andere is gerelateerd aan het resterende, nog niet ingepakte een heeft de status *Open*.
1. Selecteer de **Lading-id**-waarde voor een werkkoptekst om de pagina **Ladingdetails** te openen voor de lading.
1. Schakel over naar de weergave **Koptekst**.
1. Selecteer op het sneltabblad **Algemeen** de knop **Bewerken** voor het veld **Ladingsjabloon-id** laden. Selecteer vervolgens de ladingsjabloon voor gedeeltelijke verzending (*Gedeeltelijk*), die u voor dit scenario hebt gemaakt.
1. Selecteer in het actievenster op het tabblad **Verzenden en ontvangen** in de groep **Bevestigen** de optie **Uitgaande zending**.
1. Selecteer in het dialoogvenster **Verzending bevestigen** de optie **Hoeveelheid splitsen voor nieuwe lading**.
1. Selecteer **OK**.

U hebt nu één container verzonden die is gerelateerd aan de oorspronkelijke lading en er is een nieuwe lading gemaakt voor de resterende artikelen die nog in containers moeten worden ingepakt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

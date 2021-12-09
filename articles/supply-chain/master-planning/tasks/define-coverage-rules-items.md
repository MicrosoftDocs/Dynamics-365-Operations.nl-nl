---
title: Behoefteplanningsregels voor artikelen definiëren
description: Deze procedure toont hoe u behoefteplanningsregels maakt en behoefteplanningsinstellingen voor een specifiek artikel overschrijft. Het toont ook hoe u standaardvoorraadinstellingen opgeeft.
author: ChristianRytt
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3947c8a51facfb02012cc8e9a3ffd5887073bd9
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860608"
---
# <a name="define-coverage-rules-for-items"></a>Behoefteplanningsregels voor artikelen definiëren

[!include [banner](../../includes/banner.md)]

Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure toont hoe u behoefteplanningsregels maakt en behoefteplanningsinstellingen voor een specifiek artikel overschrijft. Het toont ook hoe u standaardvoorraadinstellingen opgeeft.

## <a name="create-a-coverage-group"></a>Een behoefteplanningsgroep maken

Maak als volgt een dekkingsgroep:

1. Ga naar **Navigatievenster > Modules > Hoofdplanning > Instellen >Behoefteplanningsgroepen**.
1. Selecteer **Nieuw**.
1. Typ een waarde in het veld **Behoefteplanningsgroep**.
1. Typ een waarde in het veld **Naam**.
1. Typ een waarde in het veld **Agenda**. Kies de agenda die tijdens hoofdplanning wordt gebruikt om aanvullingssuggesties te doen voor artikelen in deze groep.  
1. Selecteer een optie in het veld **Behoefteplanningscode**. Selecteer 'Vereiste' voor deze procedure.  
1. Voer 90 in het veld **Time fence behoefteplanning (dagen)** in. Voor artikelen in deze groep maakt de hoofdplanning aanvullingssuggesties tot maximaal 90 dagen in de toekomst.  
1. Voer 1 in het veld **Negatieve dagen** in.
1. Voer 1 in het veld **Positieve dagen** in.
1. Vouw de sectie **Overige** uit of samen.
1. Ga naar de sectie **Veiligheidsmarges in dagen** en voer in het veld **Ontvangstmarge toegevoegd aan behoeftedatum** 1 in. Als bijvoorbeeld de ontvangstmarge is ingesteld op 1 dag en een inkooporderregel is gepland voor ontvangst op 15 mei, berekent de hoofdplanning de aangepaste ontvangstdatum als 16 mei.
1. Typ 1 in het veld **Uitgiftemarge afgetrokken van behoeftedatum**. Als bijvoorbeeld de veiligheidsmarge is ingesteld op 1 dag en een verkooporderregel is gepland voor levering op 15 mei, berekent de hoofdplanning de aangepaste leveringsdatum als 14 mei.  
1. Typ 1 in het veld **Bestelmarge opgeteld bij doorlooptijd van artikel**.
1. Selecteer **Opslaan**.

## <a name="create-a-new-product"></a>Een nieuw product maken

Maak als volgt een nieuw product:

1. Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.
1. Selecteer **Nieuw**.
1. Typ een waarde in het veld **Productnummer**.
1. Typ een waarde in het veld **Productnaam**.
1. Selecteer in het veld **Artikelmodelgroep** de vervolgkeuzeknop om de zoekopdracht te openen.
1. Zoek en selecteer de gewenste record in de lijst.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Selecteer in het veld **Artikelgroep** de vervolgkeuzeknop om de zoekopdracht te openen.
1. Zoek en selecteer de gewenste record in de lijst.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Selecteer in het veld **Opslagdimensiegroep** de vervolgkeuzeknop om de zoekopdracht te openen.
1. Zoek en selecteer de gewenste record in de lijst.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Selecteer in het veld **Traceringsdimensiegroep** de vervolgkeuzeknop om de zoekopdracht te openen.
1. Zoek en selecteer de gewenste record in de lijst.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Selecteer **OK**.

## <a name="set-up-default-order-settings"></a>Standaardorderinstellingen instellen

Stel als volgt standaardorderinstellingen in:

1. Selecteer in het **Actiepaneel** de optie **Planning**.
1. Selecteer onder **Orderinstellingen** de optie **Standaardorderinstellingen**.
1. Ga naar **Inkooporder** en typ in het veld **Standaardvestiging** de vestiging die als standaard moet worden gebruikt wanneer de inkooporders worden gemaakt.
1. Typ in het veld **Standaardmagazijn** de vestiging waar het artikel is opgeslagen.
1. Vouw de sectie **Voorraad** uit of samen.
1. Typ 10 in het veld **Meerdere**.
1. Typ 10 in het veld **Min.bestelhoeveelheid**.
1. Typ 100 in het veld **Max.bestelhoeveelheid**.
1. Typ 10 in het veld **Standaardbestelhoeveelheid**.
1. Voer een numerieke waarde in het veld **Inkoopdoorlooptijd** in.
1. Schakel het selectievakje **Werkdagen** in of uit.
1. Selecteer **Opslaan**.
1. Selecteer Inkooporder in het veld **Standaardordertype**.
1. Selecteer **Opslaan**.
1. Sluit de pagina. Sluit de pagina Standaard orderinstellingen.  

## <a name="add-an-item-to-a-coverage-group"></a>Een artikel aan een behoefteplanningsgroep toevoegen

Voeg als volgt een artikel aan een planningsgroep toe:

1. Vouw de sectie **Planning** uit of samen.
1. Selecteer in het veld **Behoefteplanningsgroep** de vervolgkeuzeknop om de zoekopdracht te openen.
1. Zoek in de lijst de **Behoefteplanningssgroep** die u hebt gemaakt.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.

## <a name="create-item-coverage-rules"></a>Regels artikelbehoefteplanning maken

Maak als volgt een artikelbehoefteplanning:

1. Selecteer in het **Actiepaneel** de optie **Planning**.
1. Klik onder **Behoefteplanning** op **Artikelbehoefteplanning**.
1. Selecteer **Nieuw**.
1. Selecteer het tabblad **Algemeen**.
1. Schakel het vakje in de kop van **Instellingen behoefteplanningsgroep overschrijven** in.
1. Voer 60 in het veld **Time fence behoefteplanning (dagen)** in. Hoewel artikelen in een behoefteplanningsgroep 90 dagen vooruit worden gepland, wordt dit artikel 60 dagen vooruit gepland.  
1. Voer 2 in het veld **Negatieve dagen** in.
1. Voer 2 in het veld **Positieve dagen** in.
1. Selecteer het tabblad **Levertijd**.
1. Schakel het vakje in de kop van **Inkoop** in.
1. Voer in het veld **Inkooptijd** 5 in.
1. Selecteer **Opslaan**.

> [!NOTE]
> Voor gefabriceerde artikelen wordt **Doorlooptijd productie** gebruikt als er geen route is voor het artikel. Als een actieve route aan het artikel is gekoppeld, wordt de order gepland door de hoofdplanning en worden de datums ervan berekend volgens de routetijden en capaciteit van de resources (indien van toepassing).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

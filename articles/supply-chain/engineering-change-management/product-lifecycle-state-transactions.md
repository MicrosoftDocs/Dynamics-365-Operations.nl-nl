---
title: Levenscyclusstatussen van producten en transacties
description: In dit onderwerp wordt besproken hoe u kunt beheren welke transacties zijn toegestaan voor elke levenscyclusstatus naarmate een technisch product de levenscyclus doorloopt.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 421fae6eab20eea50b9ce677a1ae7993add6cb93
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842052"
---
# <a name="product-lifecycle-states-and-transactions"></a>Levenscyclusstatussen van producten en transacties

[!include [banner](../includes/banner.md)]

Omdat een technisch product een levenscyclus loopt, is het van belang dat u kunt bepalen welke transacties zijn toegestaan voor elke levenscyclusstatus. Producten die nog niet in een volwassen status zijn, moeten bijvoorbeeld niet op een verkooporder worden geplaatst. Als een product echter het einde van de levenscyclus heeft bereikt, kunt u de instroom van dat product beheren.

Voor een technisch product zijn wijzigingen in de levenscyclusstatus gekoppeld aan de technische versies van het product. Daarom kan de levenscyclusstatus van het product ook worden gekoppeld aan de technische versies. Wanneer de levenscyclusstatus van een product is gekoppeld aan een technische versie, kunt u de levenscyclusstatus gebruiken om te beheren welke transacties zijn toegestaan voor de technische versie.

## <a name="create-and-manage-product-lifecycle-states"></a>Levenscyclusstatussen van producten maken en beheren

Als u wilt werken met levenscyclusstatussen voor producten, gaat u naar **Beheer van technische wijzigingen \> Instellingen \> Levenscyclusstatus van product**. Voer vervolgens een van deze stappen uit.

- Als u een nieuwe levenscyclusstatus wilt maken, selecteert u **Nieuw** in het actievenster en stelt u de velden in op de wijze die wordt beschreven in de volgende subsecties.
- Als u een bestaande levenscyclusstatus wilt bewerken, selecteert u deze in het lijstvenster, selecteert u **Bewerken** in het actievenster en stelt u de velden in op de wijze die wordt beschreven in de volgende subsecties.
- Als u een bestaande levenscyclusstatus wilt verwijderen, selecteert u deze in het lijstvenster en selecteert u **Verwijderen** in het actievenster.

> [!NOTE]
> Technische producten gebruiken dezelfde levenscyclusstatussen als standaard producten (niet-technisch). U kunt ook de pagina **Levenscyclusstatus van product**, beschreven in dit onderwerp, openen door naar **Productgegevenseheer \> Instellingen \> Levenscyclusstatus van product** te gaan. Voor meer informatie over de levenscyclusstatus van producten, voor zowel technische producten als standaardproducten, gaat u naar [Overzicht van Levenscyclusstatus van producten](../pim/product-lifecycle.md).

### <a name="header"></a>Koptekst

Stel de volgende velden in de koptekst van een levenscyclus van het product in.

| Veld | Beschrijving |
|---|---|
| Staat/provincie | Voer een naam in voor de levenscyclusstatus van het product. |
| Beschrijving | Voer een omschrijving in van de levenscyclusstatus van het product. |

### <a name="general-fasttab"></a>Het sneltabblad Algemeen

Stel de volgende velden in op het sneltabblad **Algemeen**.

| Veld | Beschrijving |
|---|---|
| Standaard wanneer het aan een rechtspersoon wordt vrijgegeven | Voor standaardproducten stelt u deze optie in op *Ja* als deze levenscyclus standaard op alle producten moet worden toegepast wanneer deze voor het eerst worden vrijgegeven. Stel deze in op *Nee* als deze levenscyclusstaties later handmatig wordt toegepast.<p>Deze instelling is niet van toepassing op technische producten. De levenscyclusstatus van een technische productversie nadat deze is gemaakt in het technische bedrijf, wordt gespecificeerd in de categorie technische wijzigingen. Wanneer het product aan een operationeel bedrijf wordt vrijgegeven, wordt de levenscyclusstatus van het product gekopieerd. Met andere woorden, wanneer een technisch product wordt vrijgegeven aan een operationeel bedrijf, heeft het dezelfde levenscyclusstatus als in het technisch bedrijf. De levenscyclusstatus kan worden overschreven in het operationele bedrijf.</p> |
| Is actief voor planning | Stel deze optie in op *Ja* als u producten in deze levenscyclusstatus in berekeningen wilt opnemen op het hoofdplanningsniveau en hetstuklijstniveau. Stel deze in op *Nee* om producten in deze levenscyclusstatus uit te sluiten van de berekeningen. |

### <a name="enabled-business-processes-fasttab"></a>Sneltabblad Ingeschakelde bedrijfsprocessen

Gebruik het sneltabblad **Ingeschakelde bedrijfsprocessen** om te bepalen welke van de beschikbare bedrijfsprocessen kan worden gebruikt met producten in de huidige levenscyclusstatus. De processen die op dit sneltabblad worden vermeld, worden automatisch op de volgende manier gevonden:

- De eerste keer dat u een nieuwe levenscyclusstatus opslaat, laadt de pagina de bedrijfsprocessen die momenteel beschikbaar zijn.
- Als u nieuwe bedrijfsprocessen aan uw systeem toevoegt, kunt u de lijst op het sneltablad **Ingeschakelde bedrijfsprocessen** bijwerken voor een bestaande levenscyclusstatus door **Controleren op updates** te selecteren in het actievenster.

De volgende velden zijn beschikbaar voor elk proces dat wordt vermeld op het sneltabblad **Ingeschakelde bedrijfsprocessen**.

| Veld | Beschrijving |
|---|---|
| Proces | Dit Alleen-lezen-veld geeft de naam van een bestaand bedrijfsproces weer. |
| Procesgebied | Dit Alleen-lezen-veld geeft de naam van een bestaand procesgebied weer. |
| Polis | Selecteer een van de volgende waarden om te bepalen of en hoe het huidige proces wordt toegestaan voor producten in deze levenscyclusstatus:<ul><li>**Ingeschakeld**: het bedrijfsproces is toegestaan.</li><li>**Geblokkeerd**: het proces is niet toegestaan. Als een gebruiker het proces wil gebruiken voor een product in deze levenscyclusstatus, wordt de poging door het systeem geblokkeerd en wordt er in plaats daarvan een fout weergegeven. U kunt bijvoorbeeld blokkeren dat producten aan het einde van hun levenscyclus worden gekocht.</li><li>**Ingeschakeld met waarschuwing**: het proces is toegestaan, maar er wordt een waarschuwing weergegeven. U kunt bijvoorbeeld een prototypeproduct op een productieorder plaatsen die wordt gemaakt door de afdeling Onderzoek en ontwikkeling. Andere afdelingen moeten er echter rekening mee houden dat zij het product nog niet mogen produceren.</li></ul> |

Als u meer levenscyclusstatusregels toevoegt als aanpassing, kunt u deze regels weergeven in de gebruikersinterface door **Processen vernieuwen** te selecteren in het bovenste deelvenster. De knop **Processen vernieuwen** is alleen beschikbaar voor beheerders.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
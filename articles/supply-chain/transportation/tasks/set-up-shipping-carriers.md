---
title: Vervoerders instellen
description: In dit artikel wordt beschreven hoe u een vervoerder instelt en details bepaalt zoals service, modus van zending, transportaanbesteding, transportbeperkingen en verzendtarief.
author: Weijiesa
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48586a0ddaa7cd95a81380dadffef8f276076dd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858967"
---
# <a name="set-up-shipping-carriers"></a>Vervoerders instellen

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe u een vervoerder instelt en details bepaalt zoals service, modus van zending, transportaanbesteding, transportbeperkingen en verzendtarief. Een transportcoördinator kan vervolgens een vervoerder toewijzen aan een inkomende of uitgaande lading.

## <a name="create-a-new-shipping-carrier"></a>Een nieuwe vervoerder maken

1. Ga naar **Navigatievenster > Modules > Transportbeheer > Instellingen > Vervoerders > Vervoerders**.
2. Selecteer **Nieuw** in het actievenster.
3. Typ een waarde in het veld **Vervoerder**.
4. Typ een waarde in het veld **Naam**.
5. Selecteer in het veld **Modus** een optie in het vervolgkeuzemenu.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>De algemene informatie voor de vervoerder invullen

1. Schakel de uitbreiding van de sectie **Overzicht** om.
2. Schakel het selectievakje **Vervoerder activeren** in of uit.
3. Selecteer in het veld **Leveranciersrekening** een optie in het vervolgkeuzemenu. Selecteer de leverancierrekening waaraan de vervoerder moet worden toegewezen.  
4. Selecteer een optie in het veld **Type betalingsmethode transport**. Selecteer **Handmatig** om de pagina Transportbetalingsmethode te gebruiken of selecteer **EDI** om de betalingsmethode bij te werken met Electronic Data Interchange (EDI).  
5. Schakel het selectievakje **Vervoerdersbeoordeling** activeren in of uit.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>De nodige services voor de vervoerder maken

1. Schakel de uitbreiding van de sectie **Services** om.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Vervoerdersservice**.
4. Typ een waarde in het veld **Naam**.
5. Selecteer in het veld **Ladingsjabloon-id** een laadsjabloon die u aan de service wilt koppelen. De laadsjabloon definieert maximummetingen voor gewicht en volume van een volledige lading. Zo kan de laadsjabloon bijvoorbeeld de grootte van een container of een vrachtwagen vertegenwoordigen. Laadsjabloon-ID's worden ook opgegeven in ladingopbouwsjablonen. Wanneer u de [workbench voor ladingopbouw](load-building-workbench.md) gebruikt, kunt u ladingopbouwstrategieën toepassen om ladingen te maken. Hierdoor kan elke nieuwe lading worden afgestemd op een geschikte vervoerdersservice door de opgegeven laadsjabloon-ID's met elkaar te vergelijken.
6. Selecteer in het veld **Transportmethode** een optie in het vervolgkeuzemenu.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Het adres voor de vervoerder instellen (optioneel)

1. Schakel de uitbreiding van de sectie **Adressen** om.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Naam of omschrijving**.
4. Selecteer in het veld **Land/regio** een optie in het vervolgkeuzemenu.
5. Selecteer in het veld **Postcode** een optie in het vervolgkeuzemenu.
6. Typ een waarde in het veld **Straat**.
7. Selecteer **OK**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Het tariefprofiel voor de vervoerder instellen

1. Schakel de uitbreiding van de sectie **Beoordelingsprofielen** om.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Beoordelingsprofiel**.
4. Typ een waarde in het veld **Naam**.
5. Selecteer in het veld **Locatie** een optie in het vervolgkeuzemenu.
6. Selecteer in het veld **Magazijn** een optie in het vervolgkeuzemenu.
7. Selecteer in het veld **Tarief-engine** een optie in het vervolgkeuzemenu. Selecteer de tariefengine die in overeenstemming is met het contract dat u hebt met de vervoerder.  
8. Selecteer in het veld **Tariefmodel** een optie in het vervolgkeuzemenu.
9. Selecteer in het veld **Engine voor transittijd** een optie in het vervolgkeuzemenu.
10. Selecteer **Opslaan**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
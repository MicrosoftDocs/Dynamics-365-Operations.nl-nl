---
title: Een grootboekkalender wijzigen of opnieuw toewijzen
description: In dit onderwerp wordt uitgelegd hoe u de kalender wijzigt die momenteel aan een grootboek is toegewezen en hoe u een nieuwe kalender aan het grootboek toewijst.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039945"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Een grootboekkalender wijzigen of opnieuw toewijzen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de kalender wijzigt die momenteel aan een grootboek is toegewezen en hoe u een nieuwe kalender aan het grootboek toewijst.

## <a name="issue"></a>Probleem

Soms moeten bedrijven de bestaande kalender wijzigen die aan een grootboek is toegewezen of een nieuwe kalender toewijzen.

## <a name="resolution"></a>Oplossing

Er zijn twee scenario's voor het wijzigen of opnieuw toewijzen van een grootboekkalender. Het eerste scenario omvat het wijzigen van een bestaande kalender die al aan het grootboek is toegewezen. Het tweede scenario omvat het maken van een nieuwe kalender en het toewijzen van deze kalender aan het grootboek. Beide wijzigingen kunnen op elk moment worden doorgevoerd, zelfs nadat transacties naar het grootboek zijn geboekt.

### <a name="change-an-existing-fiscal-calendar"></a>Een bestaande fiscale kalender wijzigen

Als u een bestaande kalender wilt wijzigen die aan uw grootboek is toegewezen, gaat u naar **Grootboek \> Grootboekinstellingen \> Grootboek** en selecteert u de koppeling voor de fiscale kalender om de pagina **Grootboekkalenders** te openen.

Er zijn grenzen aan de wijzigingen die kunnen worden aangebracht in een kalender. U kunt bijvoorbeeld de begin- en einddatums van de *perioden* in een jaar wijzigen, maar niet de begin- en einddatums van een *jaar* in de kalender.

Selecteer de juiste kalender en het juiste jaar om de perioden in een jaar te wijzigen. Gebruik eerst de knop **Periode verwijderen** om enkele of alle bestaande bedrijfsperioden te verwijderen. Alle bedrijfsperioden behalve de eerste kunnen worden verwijderd. Gebruik vervolgens de knop **Periode opsplitsen** om de resterende periode of perioden op te splitsen in nieuwe perioden door een geschikte begindatum voor de volgende periode in te voeren.

Nadat u de perioden in een kalender hebt gewijzigd, moet u het proces **Grootboekperioden herberekenen** uitvoeren in elke rechtspersoon (bedrijf) waaraan de agenda is toegewezen. Hoewel er geen waarschuwingsbericht wordt weergegeven om u aan deze stap te herinneren, is het herberekeningsproces nodig om de periode bij te werken die is toegewezen aan elke geboekte transactie in het grootboek. U voert het herberekeningsproces uit door **Grootboekperioden herberekenen** op de pagina **Grootboekinstellingen** te selecteren voor elk bedrijf.

Als het herberekeningsproces niet wordt uitgevoerd, worden transactiesaldi op een proefbalans of op financiële overzichten mogelijk onjuist opgenomen in perioden. In dat geval kunt u de saldi op elk gewenst moment corrigeren door het herberekeningsproces uit te voeren.

### <a name="assign-a-new-fiscal-calendar"></a>Een nieuwe fiscale kalender toewijzen

Als u een nieuwe fiscale kalender wilt toewijzen, gaat u naar **Grootboek \> Grootboekinstellingen \> Grootboek** en selecteert u **Bewerken** om de bewerkingsmodus in te schakelen voor de pagina **Grootboek**. Selecteer vervolgens in het veld **Fiscale kalender** een nieuwe fiscale kalender.

Als u de fiscale kalender voor een grootboek hebt gewijzigd, moet u **Grootboekperioden herberekenen** uitvoeren. Wanneer u een nieuwe fiscale kalender aan een grootboek toewijst, wordt er een bericht weergegeven om u eraan te herinneren deze stap te voltooien. Hoewel het bericht erop lijkt te duiden dat het herberekeningsproces optioneel is, is het dat niet. Dit proces is vereist om de periode bij te werken die aan elke geboekte transactie in het grootboek is toegewezen. U voert het herberekeningsproces uit door **Grootboekperioden herberekenen** op de pagina **Grootboek instellen** te selecteren.

Als het herberekeningsproces niet wordt uitgevoerd, worden transactiesaldi op een proefbalans of op financiële overzichten mogelijk onjuist opgenomen in perioden. In dat geval kunt u de saldi op elk gewenst moment corrigeren door het herberekeningsproces uit te voeren.

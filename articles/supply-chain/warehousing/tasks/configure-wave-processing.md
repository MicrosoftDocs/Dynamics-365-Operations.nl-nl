---
title: Voorbeeld van waveverwerking configureren
description: In dit onderwerp wordt een voorbeeld gegeven van het instellen van de criteria die bepalen welk werk wordt gegenereerd voor een magazijn wanneer een wave wordt verwerkt en of waves handmatig of automatisch worden verwerkt.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d462427b85e12a45058a2fdea7901a83d9e85e5a562376dd438c69dec1ee8948
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769366"
---
# <a name="configure-wave-processing-example"></a>Voorbeeld van waveverwerking configureren

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt een voorbeeld gegeven van het instellen van de criteria die bepalen welk werk wordt gegenereerd voor een magazijn wanneer een wave wordt verwerkt en of waves handmatig of automatisch worden verwerkt. U kunt de criteria opgeven door wavesjablonen en query's in te stellen die overeenstemmen met een wave met vrijgegeven regels in verkooporders, productieorders of kanbanorders.

## <a name="enable-sample-data"></a>Voorbeeldgegevens inschakelen

Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard demogegevens zijn geïnstalleerd. U moet ook de rechtspersoon **USMF** selecteren voordat u begint.

## <a name="example-scenario-configure-wave-processing"></a>Voorbeeldscenario: waveverwerking configureren

In dit voorbeeldscenario wordt een groot aantal verschillende instellingen doorlopen die van invloed zijn op de manier waarop waves worden gemaakt, gevuld, verwerkt en vrijgegeven.

1. Ga naar **Navigatiedeelvenster > Modules > Magazijnbeheer > Instellen > Waves >Wave-sjablonen**.
1. Selecteer **Nieuw**.
1. Typ een waarde in het veld **Wavesjabloon**. Wanneer u een wavesjabloon instelt, kunt u de volgorde opgeven waarin de sjablonen worden gematcht met vrijgegeven regels op verkooporders, productieorders of kanbans. Wanneer een regel aan het magazijn of aan productie wordt vrijgegeven, wordt de eerste wavesjabloon gebruikt waarvoor aan de criteria wordt voldaan. Het wordt aanbevolen sjablonen met de meest specifieke criteria boven aan de lijst te plaatsen. Hoe breder de criteria, hoe waarschijnlijker het is dat een regel voldoet aan de criteria, waardoor regels aan de verkeerde wave worden toegewezen.  
1. Typ een waarde in het veld **Beschrijving van wavesjabloon**.
1. Typ of selecteer een waarde in het veld **Locatie**. Als u USMF gebruikt, kunt u locatie 2 selecteren.  
1. Typ of selecteer een waarde In het veld **Magazijn**. Als u USMF gebruikt, kunt u magazijn 24 selecteren.  
1. Stel het veld **Het maken van waves automatiseren** in op **Ja**. Selecteer deze optie om automatisch een wave te maken wanneer een verkooporder, een productieorder, of een kanban aan het magazijn wordt vrijgegeven.  
1. Stel de optie **Wave verwerken bij vrijgave door magazijn** in op **Ja**. Selecteer deze optie om de wave automatisch te verwerken en werk te maken wanneer een regel aan het magazijn wordt vrijgegeven.  
1. Stel de optie **Vrijgave waves automatiseren** in op **Ja**. Selecteer deze optie om de wave automatisch vrij te geven. Het orderverzamelwerk wordt gemaakt en wordt beschikbaar op mobiele apparaten.  
1. Stel de optie **Toewijzen aan open waves** in op **Ja**. Regels worden toegewezen aan waves op basis van het queryfilter voor de wavesjabloon.  
1. Stel de optie **Wave automatisch verwerken op drempel** in op **Ja**. Selecteer deze optie om de wave automatisch te verwerken wanneer de waarden de drempels bereiken voor gewicht, verzending en regels bepaald in de veldgroep **Wavedrempels**. Deze optie is alleen beschikbaar als **Verzending** is geselecteerd in het veld **Type wavesjabloon**.  
1. Stel de optie **Vrijgave van aanvullingswerk automatiseren** in op **Ja**. Selecteer deze optie om op vraag gebaseerd aanvullingswerk te maken en dit automatisch vrij te geven. U moet de methode van de aanvullingswave toevoegen aan de wavesjabloon en een aanvullingssjabloon maken met het type **Waveaanvraag**.  
1. Gebruik instellingen in de opgeslagen groep **Standaardwaarden** om wavekenmerken toe te wijzen. De wavekenmerken fungeren als filters om het type te beperken van artikelen die de wave kunnen gebruiken. U kunt bijvoorbeeld een artikelgroep opgeven.  
1. Vouw de sectie **Methoden** uit en stel de acties in die door de wavesjabloon worden ondernomen. Met wavesjabloonmethoden kunt u de volgorde bepalen van activiteiten die elke wave tijdens de verwerking doorloopt. U kunt bijvoorbeeld een methode hebben voor waveaanvulling. Wanneer u een methode toevoegt, wordt deze automatisch weergegeven op de juiste locatie in de reeks stappen. Als u de optie **Vrijgave van aanvullingswerk automatiseren** op **Ja** hebt ingesteld, moet u de aanvullingsmethode hier toevoegen.  
1. Selecteer **Opslaan**.
1. Sluit de pagina.
1. Ga naar **Magazijnbeheer > Instellen > Parameters voor magazijnbeheer**.
1. Vouw de sectie **Waveverwerking** uit.
1. Typ of selecteer een waarde in het veld **Batchgroep voor waveverwerking**.
1. Stel de optie **Waves verwerken in batch** in op **Ja**.
1. Voer een getal in het veld **Wachten op vergrendeling (ms)** in. Voer de tijd, uitgedrukt in milliseconden, in die een toewijzingsstap moet wachten op een systeemresource die door een andere toewijzingsstap wordt vergrendeld. Nadat deze tijd is verstreken, wordt de golf niet verwerkt en wordt er een foutbericht weergegeven.  
1. Selecteer **Opslaan**.
1. Sluit de pagina.
1. Ga naar **Navigatiedeelvenster > Modules > Productiebeheer > Instellen > Parameters van productiebeheer**.
1. Selecteer een optie in het veld **Vrijgave naar magazijn**.

    Bij verkooporders en kanbanorders moet de voorraad zijn gereserveerd voordat de order aan het magazijn wordt vrijgegeven. Anders kunnen artikelen of toewijzingsregels niet in een golf worden verwerkt. Voor productieorders hebt u ook de mogelijkheid om **Gedeeltelijke reservering toestaan** te kiezen. Dit is bijvoorbeeld handig als u de materialen hebt die u nodig hebt om een productie te starten. U kunt dan wachten totdat de extra materialen beschikbaar worden om het proces te voltooien. Als u deze optie selecteert, moet u de vrijgave naar het magazijnproces handmatig herhalen wanneer de aanvullende materialen beschikbaar worden.
1. Sluit de pagina.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Wave maken en verwerken](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

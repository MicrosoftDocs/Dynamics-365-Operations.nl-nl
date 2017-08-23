--- 
title: Waveverwerking configureren
description: In deze begeleiding wordt beschreven hoe u de criteria instelt die bepalen wat voor werk wordt gegenereerd voor een magazijn wanneer een wave wordt verwerkt en of waves handmatig of automatisch worden verwerkt.
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 50988c689995dbb957af760c9c2c3b823f557c86
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="configure-wave-processing"></a>Waveverwerking configureren

[!include[task guide banner](../../includes/task-guide-banner.md)]

In deze begeleiding wordt beschreven hoe u de criteria instelt die bepalen wat voor werk wordt gegenereerd voor een magazijn wanneer een wave wordt verwerkt en of waves handmatig of automatisch worden verwerkt. U kunt de criteria opgeven door wavesjablonen en query's in te stellen die overeenstemmen met een wave met vrijgegeven regels in verkooporders, productieorders of kanbanorders. De waveverwerking wordt gebruikt in magazijnen die de functionaliteit in de module Magazijnbeheer gebruiken, en niet in magazijnen die de functionaliteit in de module Voorraadbeheer gebruiken. U kunt deze procedure in het bedrijf USMF van de demogegevens uitvoeren.

1. Ga naar Magazijnbeheer > Instellingen > Waves > Wavesjablonen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Wavesjabloon.
    * Wanneer u een wavesjabloon instelt, kunt u de volgorde opgeven waarin de sjablonen worden gematcht met vrijgegeven regels op verkooporders, productieorders of kanbans. Wanneer een regel aan het magazijn of aan productie wordt vrijgegeven, wordt de eerste wavesjabloon gebruikt waarvoor aan de criteria wordt voldaan. Het wordt aanbevolen sjablonen met de meest specifieke criteria boven aan de lijst te plaatsen. Hoe breder de criteria, hoe waarschijnlijker het is dat een regel voldoet aan de criteria, waardoor regels aan de verkeerde wave worden toegewezen.  
4. Typ een waarde in het veld Omschrijving van wavesjabloon.
5. Typ of selecteer een waarde in het veld Locatie.
    * Als u USMF gebruikt, kunt u Vestiging 2 selecteren.  
6. Typ of selecteer een waarde in het veld Magazijn.
    * Als u USMF gebruikt, kunt u magazijn 24 selecteren.  
7. Stel het veld Het maken van waves automatiseren in op Ja.
    * Selecteer deze optie om automatisch een wave te maken wanneer een verkooporder, een productieorder, of een kanban aan het magazijn wordt vrijgegeven.  
8. Stel de optie Wave verwerken bij vrijgave door magazijn in op Ja. 
    * Selecteer deze optie om de wave automatisch te verwerken en werk te maken wanneer een regel aan het magazijn wordt vrijgegeven.  
9. Stel de optie Vrijgave waves automatiseren in op Ja. 
    * Selecteer deze optie om de wave automatisch vrij te geven. Het orderverzamelwerk wordt gemaakt en wordt beschikbaar op mobiele apparaten.  
10. Stel de optie Toewijzen aan open waves in op Ja. 
    * Regels worden toegewezen aan waves op basis van het queryfilter voor de wavesjabloon.  
11. Stel de optie Wave automatisch verwerken op drempel in op Ja. 
    * Selecteer deze optie om de wave automatisch te verwerken wanneer de waarden de drempels bereiken voor gewicht, verzending en regels bepaald in de veldgroep Wavedrempels. Deze optie is alleen beschikbaar als Verzending is geselecteerd in het veld Type wavesjabloon.  
12. Stel de optie Vrijgave van aanvullingswerk automatiseren in op Ja. 
    * Selecteer deze optie om op vraag gebaseerd aanvullingswerk te maken en dit automatisch vrij te geven. U moet de methode van de aanvullingswave toevoegen aan de wavesjabloon, en een aanvullingssjabloon maken van het type Waveaanvraag.  
13. Vouw de sectie Methoden uit.
    * Met wavesjabloonmethoden kunt u de volgorde bepalen van activiteiten die elke wave tijdens de verwerking doorloopt. U kunt bijvoorbeeld een methode hebben voor waveaanvulling. Wanneer u een methode toevoegt, wordt deze automatisch weergegeven op de juiste locatie in de reeks stappen. Als u de optie Vrijgave van aanvullingswerk automatiseren op Ja hebt ingesteld, moet u de aanvullingsmethode hier toevoegen.  
    * De wavekenmerken fungeren als filters om het type te beperken van artikelen die de wave kunnen gebruiken. U kunt bijvoorbeeld een artikelgroep opgeven.  
14. Klik op Opslaan.
15. Sluit de pagina.
16. Ga naar Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer.
17. Vouw de sectie Waveverwerking uit.
18. Typ of selecteer een waarde in het veld Batchgroep voor waveverwerking.
19. Stel de optie Waves verwerken in batch in op Ja.
20. Voer een getal in het veld Wachten op vergrendeling (ms) in.
    * Voer de tijd, uitgedrukt in milliseconden, in die een toewijzingsstap moet wachten op een systeemresource die door een andere toewijzingsstap wordt vergrendeld. Nadat deze tijd is verstreken, wordt de golf niet verwerkt en wordt er een foutbericht weergegeven.  
21. Klik op Opslaan.
22. Sluit de pagina.
23. Ga naar Productiebeheer > Instellingen > Parameters van productiebeheer.
24. Selecteer een optie in het veld Vrijgave naar magazijn.
    * Bij verkooporders en kanbanorders moet de voorraad zijn gereserveerd voordat de order aan het magazijn wordt vrijgegeven. Anders kunnen artikelen of toewijzingsregels niet in een golf worden verwerkt. Voor productieorders hebt u ook de mogelijkheid om Gedeeltelijke reservering toestaan te kiezen. Dit is bijvoorbeeld handig als u de materialen hebt die u nodig hebt om een productie te starten. U kunt dan wachten totdat de extra materialen beschikbaar worden om het proces te voltooien. Als u deze optie selecteert, moet u de vrijgave naar het magazijnproces handmatig herhalen wanneer de aanvullende materialen beschikbaar worden.  
25. Sluit de pagina.



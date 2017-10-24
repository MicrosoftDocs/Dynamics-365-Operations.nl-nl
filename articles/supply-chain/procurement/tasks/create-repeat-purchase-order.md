--- 
title: Een herhalingsinkooporder maken
description: "Deze procedure laat zien hoe u een herhalingsinkooporder (IO) kunt maken door regels vanuit een eerder inkooporderdocument naar een nieuwe inkooporder of naar een bestaande inkooporder te kopiëren."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 257582d889ff55753f9bdbd234f0540503d20f27
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-repeat-purchase-order"></a>Een herhalingsinkooporder maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een herhalingsinkooporder (IO) kunt maken door regels vanuit een eerder inkooporderdocument naar een nieuwe inkooporder of naar een bestaande inkooporder te kopiëren. Er zijn twee methoden voor het maken van herhalingsorders. U kunt de acties die beschikbaar zijn op documentniveau gebruiken vanuit het actievenster of u kunt de regeldetailacties gebruiken. De acties op documentniveau zijn voornamelijk bedoeld voor het maken van een nieuwe inkooporder door regels en koptekstinformatie vanuit een andere order toe te voegen, terwijl de regeldetailsactie voornamelijk wordt gebruikt voor het toevoegen van regels aan een bestaande order. Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf. Deze taak wordt meestal uitgevoerd door een inkoopagent.


## <a name="create-a-new-repeat-purchase-order"></a>Een nieuwe herhalingsinkooporder maken
1. Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.
    * Als eerste gaan we de optie proberen voor het kopiëren van informatie naar een nieuwe order.  
2. Klik op Nieuw.
3. Typ in het veld Leveranciersrekening de waarde US-101.
4. Klik op OK.
5. Klik in het actievenster op Inkooporder.
6. Klik op Van alle.
    * Dit is de pagina waar u vanuit bestaande orders naar uw order kunt kopiëren. Er zijn verschillende opties voor het kopiëren van de regels en verschillende typen documenten waaruit u kunt kopiëren. Wij gaan eerst de opties bekijken voor kopiëren van regels.   
7. Vouw de sectie Parameters uit.
    * Het veld Hoeveelheidsfactor is handig als u een hoeveelheid moet gebruiken die afwijkt van de hoeveelheid in de order waaruit u kopieert. Als u bijvoorbeeld tweemaal de hoeveelheid wilt bestellen die staat vermeld op de regels waaruit u kopieert, typt u '2' in dit veld. In het systeem worden vervolgens regels toegevoegd waarbij de oorspronkelijke hoeveelheid is verdubbeld.  
    * Het veld Omkeren ondersteunt eveneens het aanpassen van de bestelde hoeveelheid door wijziging van het teken van de hoeveelheid voor orderregels die worden toegevoegd. Dit kan handig zijn als u een transactie moet omkeren door orderregels te maken die de transactie tenietdoen. Deze optie wordt automatisch ingeschakeld wanneer de pagina wordt geopend vanuit de actie Creditnota maken.  
    * Met de optie Toeslagen kopiëren kunt u toeslagen naar uw nieuwe order kopiëren vanuit het document waaruit u de orderregels kopieert.  
    * Bij de optie Prijzen herberekenen worden de huidige prijzen en kortingen gebruikt in plaats van dat deze worden gekopieerd vanuit het document waaruit u andere gegevens kopieert.  
    * Met de optie Exact kopiëren wordt een exacte kopie gemaakt van de waarden in alle velden in de koptekst en regels van het orderdocument. Als deze optie niet is ingeschakeld, worden standaardwaarden gebruikt voor veel van de velden die betrekking hebben op de leverancier en de producten, zodat het lijkt alsof u de nieuwe order handmatig maakt. Als in de order die u kopieert bijvoorbeeld de standaardfactuurrekening voor de leverancier is overschreven, wordt dezelfde factuurrekening naar uw order gekopieerd. Als u de optie Exacte kopie niet hebt geselecteerd, wordt in plaats daarvan de standaardfactuurrekening voor de leverancier in uw order gebruikt.  
    * Met de optie Inkoopregels verwijderen worden alle inkooporderregels die al bestaan in de inkooporder waarnaar u kopieert verwijderd, voordat de nieuwe regels worden toegepast. Wees voorzichtig bij het gebruik van deze optie, aangezien hierbij alle bestaande regels worden verwijderd zonder verdere waarschuwing.  
    * Als u de optie Orderkoptekst kopiëren gebruikt, hoeft u de koptekstgegevens in uw nieuwe order niet handmatig te maken. Merk op dat deze optie resulteert in het gebruik van standaardwaarden voor de velden die verband houden met de leverancier. Als het document waaruit u kopieert niet-standaardwaarden bevat die u wilt kopiëren, gebruikt u tevens de optie Exact kopiëren.  
8. Vouw de sectie Parameters samen.
    * Er zijn verschillende documentbronnen waaruit u kunt kopiëren, en elke heeft een afzonderlijke sectie op deze pagina. Zo kunt u in de sectie Inkooporders bijvoorbeeld kopiëren vanuit bestaande inkooporders.  
9. Klik op de regel voor de inkooporder met een id van 00015. 
10. Selecteer de regel door op het selectievakje te klikken.
11. Schakel het selectievakje uit voor de regel zodat deze niet naar uw order wordt gekopieerd.
    * Nu zijn 4 regels geselecteerd om naar uw inkooporder te worden gekopieerd. Het is mogelijk om extra inkooporderregels uit andere inkooporders te selecteren en deze eveneens naar uw order te kopiëren. Het is ook mogelijk om regels uit andere typen inkoopdocumenten toe te voegen. In de volgende paar stappen worden de verschillende opties nader bekeken.  
12. Vouw de sectie Inkooporders samen.
13. Vouw de sectie Bevestiging uit.
    * Hier kunt u inkooporderbevestigingen selecteren waaruit u wilt kopiëren. De inkooporderbevestigingen worden geïdentificeerd aan de hand van de bijbehorende inkoopjournaal-id of inkooporder-id.  
14. Vouw de sectie Bevestiging samen.
15. Vouw de sectie Productontvangstbonnen uit.
    * Hier kunt u productontvangstjournalen selecteren waaruit u wilt kopiëren. De productontvangstjournalen worden geïdentificeerd aan de hand van de productontvangstbon of de inkooporder-id.   
16. Vouw de sectie Productontvangstbonnen samen.
17. Vouw de sectie Facturen uit.
    * Hier kunt u leveranciersfacturen selecteren waaruit u wilt kopiëren. De facturen worden geïdentificeerd aan de hand van het factuurboekstuk of de inkooporder-id.   
18. Vouw de sectie Facturen samen.
19. Vouw de sectie Te kopiëren geselecteerde regels of koptekst uit.
    * Deze weergave laat een overzicht zien van alle documenten en regels die zijn geselecteerd om naar uw order te worden gekopieerd.   
20. Vouw de sectie Te kopiëren geselecteerde regels of koptekst samen.
21. Klik op OK.
    * De 4 regels die u hebt geselecteerd zijn gekopieerd naar uw nieuwe inkooporder.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Regels kopiëren naar een bestaande inkooporder
    * In plaats van een volledige orderr te kopiëren, is het gebruikelijker om een nieuwe inkooporder te maken, informatie in te voeren in de IO-koptekst en vervolgens afzonderlijke regels te kopiëren vanuit bestaande orders.  
1. Klik op Inkooporderregel.
2. Klik op Van alle.
    * De pagina die wordt geopend is identiek aan de eerder weergegeven pagina, maar er zijn andere opties geselecteerd wanneer deze wordt geopend vanuit de weergave van de orderregels. Laten we de parameters maar eens gaan bekijken.   
3. Vouw de sectie Parameters uit.
    * De optie Inkoopregels verwijderen is niet ingeschakeld. Dit betekent dat u nieuwe regels naar uw order kunt kopiëren zonder bestaande regels te verwijderen.   
    * De optie Orderkoptekst kopiëren is eveneens niet ingeschakeld, aangezien we alleen extra regels aan de order toevoegen.   
4. Vouw de sectie Parameters samen.
    * In dit voorbeeld gaan we regels kopiëren vanuit een bestaande inkooporder.   
5. Klik op de regel voor de inkooporder met een id van 00034. 
6. Selecteer de regel door op het selectievakje te klikken.
    * Merk op dat de ene orderregel in deze inkooporder eveneens is geselecteerd.  
7. Klik op OK.
    * De extra orderregel is toegevoegd aan uw inkooporder.  



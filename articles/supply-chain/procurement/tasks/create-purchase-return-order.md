---
title: Een inkoopretourorder maken
description: Deze procedure laat zien hoe u een inkoopretourorder kunt maken door de actie Creditnota te gebruiken om regels van een leveranciersfactuurdocument naar een nieuwe inkooporder te kopiëren.
author: kamaybac
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 364f8d4478a5e89c3824ff06d34c7bc90c0ddb87
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812225"
---
# <a name="create-a-purchase-return-order"></a>Een inkoopretourorder maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een inkoopretourorder kunt maken door de actie Creditnota te gebruiken om regels van een leveranciersfactuurdocument naar een nieuwe inkooporder te kopiëren. Het laat ook zien hoe u de order kunt bevestigen en de verzending van de goederen terug naar de leverancier kunt verwerken. Het voorbeeld dat in deze procedure wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf. Deze taak wordt meestal uitgevoerd door een inkoopagent.

## <a name="create-a-new-purchase-return-order"></a>Een nieuwe inkoopretourorder maken
1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Inkooporders > Alle inkooporders**. De eerste stap is het maken van een nieuwe inkooporder die als inkoopretourorder moet worden gebruikt.  
2. Klik op **Nieuw**.
3. Typ in het veld **Leveranciersrekening** de waarde "US-102".
4. Klik op **OK**.
5. Klik in het **actievenster** op **Inkoop**.
6. Klik op **Creditnota**. Dit is de pagina waarop u vanuit een bestaande leveranciersfactuur naar uw retourorder kunt kopiëren. Dit is dezelfde pagina als wordt gebruikt voor andere kopieeracties. Maar omdat we deze pagina hebben geopend vanuit de actie Creditnota, wordt de pagina geconfigureerd om het maken van een retourorder te ondersteunen waarmee leveranciersfacturen worden verrekend.  
7. Vouw de sectie **Parameters** uit.
    - De optie **Omkeren** wordt automatisch ingeschakeld en kan niet worden gewijzigd. Dit zorgt ervoor dat het teken voor de hoeveelheden wordt gewijzigd en dat orderregels die worden toegevoegd worden verrekend met de leveranciersfactuur.  
    - De optie **Toeslagen kopiëren** wordt automatisch ingeschakeld en kan niet worden gewijzigd. Dit betekent dat toeslagen van de leveranciersfactuur worden toegevoegd aan inkoopretourorder om de oorspronkelijke toeslag te verrekenen. Het is mogelijk om de wijzigingen in de orderkop en regels later te wijzigen.  
    - De optie **Exact kopiëren** wordt automatisch ingeschakeld en kan niet worden gewijzigd. Dit zorgt ervoor dat een exacte kopie wordt gemaakt van de waarden in alle velden in de koptekst en regels van leveranciersfacturen. Dit betekent dat een inkoopretourorder wordt gemaakt met waarden die voldoen aan alle voorwaarden die in het leveranciersfactuurdocument worden gebruikt. 
    - Met de optie **Inkoopregels verwijderen** worden alle inkooporderregels verwijderd die al bestaan in de inkooporder voordat de nieuwe regels worden toegevoegd. In dit voorbeeld hebben we nog geen regels toegevoegd aan de inkoopretourorder, zodat dit geen effect heeft. Wees voorzichtig bij het gebruik van deze optie, aangezien hierbij alle bestaande regels worden verwijderd zonder verdere waarschuwing.  
    * De optie **Orderkoptekst kopiëren** wordt automatisch ingeschakeld en kan niet worden gewijzigd. Dit zorgt ervoor dat informatie van de leveranciersfactuur wordt gekopieerd en wordt toegepast op de koptekst van de inkoopretourorder. Dit is handig omdat het helpt ervoor te zorgen dat de inkoopretourorder wordt verrekend met de factuur aan de hand van vergelijkbare voorwaarden.  
8. Vouw de sectie **Parameters** samen.
9. Vouw de sectie **Facturen** uit. De pagina is geopend vanuit de actie Creditnota, zodat het kopiëren van informatie vanuit leveranciersfacturen de enige beschikbare optie is. Op dit tabblad worden alle beschikbare facturen weergegeven voor de leverancierrekening die is opgegeven in de inkoopretourorder die u eerder hebt gemaakt.   De facturen worden geïdentificeerd aan de hand van het factuurboekstuk of de inkooporder-id's.
10. Zoek de leveranciersfactuur met het factuurnummer AP-0006 en markeer die regel door op een willekeurig veld in deze regel te klikken.
11. Selecteer de regel door op het selectievakje voor de regel te klikken. Merk op dat de regels die beschikbaar zijn in de leveranciersfactuur automatisch samen worden geselecteerd met de order. Deze specifieke leveranciersfactuur heeft 2 orderregels. In dit voorbeeld retourneren we een deel van de hoeveelheid van de tweede regel.
12. Markeer de tweede regel (de regel met artikel M0006) door op een willekeurig veld in deze regel te klikken.
13. Wijzig de hoeveelheid in 10 in het veld **Hoeveelheid**. Dit is de hoeveelheid die we aan de leverancier gaan retourneren. 
14. Markeer de eerste regel (de regel met artikel M0005) door op een willekeurig veld in deze regel te klikken.
15. Schakel het selectievakje uit voor de regel. Alleen de regels die u hebt geselecteerd worden naar uw order gekopieerd.
16. Vouw de sectie **Facturen** samen.
17. Vouw de sectie **Te kopiëren geselecteerde regels of koptekst** uit. Deze weergave laat een overzicht zien van alle documenten en regels die u hebt geselecteerd om naar uw order te kopiëren.  
18. Vouw de sectie **Te kopiëren geselecteerde regels of koptekst** samen.
19. Klik op **OK**. De regel die u hebt geselecteerd is nu naar uw nieuwe inkoopretourorder gekopieerd. In het veld **Hoeveelheid** wordt -10 weergegeven.   
20. Klik in het gedeelte **Inkooporderregel** op **Voorraad**.
21. Klik op **Markering**. De orderregel die is gemaakt is gemarkeerd met de voorraadtransactie van de leveranciersfactuur. Dit zorgt ervoor dat de voorraad die aan de leverancier wordt geretourneerd dezelfde is als de voorraad die eerder van deze leverancier is ontvangen. Er zijn sommige situaties waarin het markeren niet plaatsvindt, bijvoorbeeld als de voorraad al is gemarkeerd als Verbruikt of als het product geen gebruikmaakt van markering.  

22. Klik op **OK**.

## <a name="confirm-and-record-the-shipment-of-goods"></a>De verzending van goederen bevestigen en registreren
1. Klik op **Acties > Bevestigen**.
2. Klik in het **actievenster** op **Ontvangen**.
3. Klik op **Productontvangstbon**.
    - Deze pagina wordt gebruikt om productontvangsten voor inkooporders te registreren en ook de retournering van goederen terug naar de leverancier te verwerken. Orderregels met een negatieve hoeveelheid geven aan dat goederen aan de leverancier moeten worden geretourneerd, en het document dat van deze pagina kan worden gegenereerd kan als pakbon voor dit gebruik dienen.   
    - Selecteer in het veld **Hoeveelheid** de optie Bestelde hoeveelheid voor dit voorbeeld. Dit zorgt ervoor dat de verzending wordt verwerkt voor de volledige bestelde hoeveelheid waarmee de orderregels zijn gemaakt.   
4. Typ een waarde in het veld **Productontvangstbon**. Dit veld wordt gebruikt om een verwijzing in te voeren die als boekstuk voor het productontvangstbonjournaal wordt gebruikt.  
5. Klik op **OK**. De goederen zijn nu geregistreerd als verzonden voor de inkoopretourorder, en er is een productontvangstbonjournaal gemaakt. U kunt de actie Productontvangstbon gebruiken om de journalen te controleren die voor de inkooporder zijn gemaakt en om te zien wat is ontvangen of geretourneerd, en wanneer.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
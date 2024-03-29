---
title: Een herhalingsinkooporder maken
description: In dit artikel wordt beschreven hoe u een herhalingsinkooporder (IO) kunt maken door regels vanuit een eerder inkooporderdocument naar een nieuwe inkooporder of naar een bestaande inkooporder te kopiëren.
author: GalynaFedorova
ms.date: 09/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335461d60fa0bc92e9711806c6e42643a3f75d02
ms.sourcegitcommit: 073604c07116e0a87f78ab2c76cb89ae83ebba3c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608101"
---
# <a name="create-a-repeat-purchase-order"></a>Een herhalingsinkooporder maken

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe u een herhalingsinkooporder (IO) kunt maken door regels vanuit een eerder inkooporderdocument naar een nieuwe inkooporder of naar een bestaande inkooporder te kopiëren. Er zijn twee methoden voor het maken van herhalingsorders. U kunt de acties die beschikbaar zijn op documentniveau gebruiken vanuit het actievenster of u kunt de regeldetailacties gebruiken. De acties op documentniveau zijn bedoeld voor het maken van een nieuwe inkooporder door regels en koptekstinformatie vanuit een andere order toe te voegen, terwijl de regeldetailsactie voornamelijk wordt gebruikt voor het toevoegen van regels aan een bestaande order. Het voorbeeld dat in deze handleiding wordt weergegeven, kan worden gebruikt in het USMF-demobedrijf. Deze taak wordt meestal uitgevoerd door een inkoopagent.

## <a name="create-a-new-repeat-purchase-order"></a>Een nieuwe herhalingsinkooporder maken

1. Ga in het navigatievenster naar **Modules \> Inkoopbeheer \> Inkooporders \> Alle inkooporders**. Als eerste gaan we de optie proberen voor het kopiëren van informatie naar een nieuwe order.  
1. Selecteer **Nieuw**.
1. Typ `US-101` in het veld **Leveranciersrekening**.
1. Selecteer **OK**.
1. Open in het actievenster het tabblad **Inkooporder** en selecteer in de groep **Kopiëren** de optie **Van alle**. Het dialoogvenster **Kopiëren uit andere documenten** wordt geopend. Hier kunt u bestaande orders naar uw order kopiëren. Er zijn verschillende opties voor het kopiëren van de regels en verschillende typen documenten waaruit u kunt kopiëren. Wij gaan eerst de opties bekijken voor kopiëren van regels.
1. Vouw het sneltabblad **Parameters** uit.

    - Het veld **Hoeveelheidsfactor** is handig als u een hoeveelheid moet gebruiken die afwijkt van de hoeveelheid in de order waaruit u kopieert. Als u bijvoorbeeld tweemaal de hoeveelheid wilt bestellen die staat vermeld op de regels waaruit u kopieert, typt u '2' in dit veld. In het systeem worden vervolgens regels toegevoegd waarbij de oorspronkelijke hoeveelheid is verdubbeld.  
    - Het veld **Omkeren** ondersteunt eveneens het aanpassen van de bestelde hoeveelheid door wijziging van het teken van de hoeveelheid voor orderregels die worden toegevoegd. Dit kan handig zijn als u een transactie moet omkeren door orderregels te maken die de transactie tenietdoen. Deze optie wordt automatisch ingeschakeld wanneer de pagina wordt geopend vanuit de actie **Creditnota maken**.  
    - Met de optie **Toeslagen kopiëren** kunt u toeslagen naar uw nieuwe order kopiëren vanuit het document waaruit u de orderregels kopieert.  
    - Bij de optie **Prijzen herberekenen** worden de huidige prijzen en kortingen gebruikt in plaats van dat deze worden gekopieerd vanuit het document waaruit u andere gegevens kopieert.  
    - Met de optie **Exact kopiëren** worden de waarden van verschillende velden in de koptekst en regels van de order gekopieerd. Als deze optie niet is ingeschakeld, worden standaardwaarden gebruikt voor veel van de velden die betrekking hebben op de leverancier en de producten, zodat het lijkt alsof u de nieuwe order handmatig maakt. Als in de order die u kopieert bijvoorbeeld **Exactie kopie** instelt op *Ja* en een order kopieert die de standaardfactuurrekening voor de leverancier overschrijft, wordt dezelfde factuurrekening naar uw nieuwe order gekopieerd. Als u **Exacte kopie** instelt op *Nee*, wordt in plaats daarvan de standaardfactuurrekening voor de leverancier in uw nieuwe order gebruikt. Waarden voor de volgende velden worden gekopieerd wanneer **Exacte kopie** is ingesteld op *Ja*:
        - Taal
        - Betalingsvoorwaarden
        - Betalingswijze
        - Betalingsspecificatie
        - Nummerreeksgroep
        - Contantkorting
        - Kortingspercentage
        - Valuta
        - Leveringsvoorwaarden
        - Leveringsmethode
        - Dimensie
        - Btw-groep
        - Btw-overschrijving
        - Prijzen inclusief btw
        - Transport
        - Haven
        - Statistiekprocedure
        - Sjabloon-ID
        - Leveringsnaam
        - Postadres
        - Verwijzing
        - Verwijzingstabel-id
    - Met de optie **Inkoopregels verwijderen** worden alle inkooporderregels die al bestaan in de inkooporder waarnaar u kopieert verwijderd, voordat de nieuwe regels worden toegepast. Wees voorzichtig bij het gebruik van deze optie, aangezien hierbij alle bestaande regels worden verwijderd zonder verdere waarschuwing.  
    - Als u de optie **Orderkoptekst kopiëren** gebruikt, hoeft u de koptekstgegevens in uw nieuwe order niet handmatig te maken. Deze optie resulteert in het gebruik van standaardwaarden voor de velden die verband houden met de leverancier. Als het document waaruit u kopieert niet-standaardwaarden bevat die u wilt kopiëren, gebruikt u tevens de optie **Exact kopiëren**.
    - Er zijn verschillende documentbronnen waaruit u kunt kopiëren, en elke heeft een afzonderlijke sectie op deze pagina. Zo kunt u in de sectie **Inkooporders** bijvoorbeeld kopiëren vanuit bestaande inkooporders.  

1. Selecteer in de sectie **Inkooporders** de regels die u naar het klembord wilt kopiëren. Het is mogelijk om extra inkooporderregels uit andere inkooporders te selecteren en deze eveneens naar uw order te kopiëren. Het is ook mogelijk om regels uit andere typen inkoopdocumenten toe te voegen. In de volgende paar stappen worden de verschillende opties nader bekeken.  
1. Vouw de sectie **Bevestiging** uit. Hier kunt u inkooporderbevestigingen selecteren waaruit u wilt kopiëren. De inkooporderbevestigingen worden geïdentificeerd aan de hand van de bijbehorende inkoopjournaal-id of inkooporder-id.  
1. Vouw de sectie **Productontvangstbonnen** uit. Hier kunt u productontvangstjournalen selecteren waaruit u wilt kopiëren. De productontvangstjournalen worden geïdentificeerd aan de hand van de productontvangstbon of de inkooporder-id.
1. Vouw de sectie **Facturen** uit. Hier kunt u leveranciersfacturen selecteren waaruit u wilt kopiëren. De facturen worden geïdentificeerd aan de hand van het factuurboekstuk of de inkooporder-id.
1. Vouw de sectie **Te kopiëren geselecteerde regels of koptekst** uit. Deze weergave laat een overzicht zien van alle documenten en regels die zijn geselecteerd om naar uw order te worden gekopieerd.
1. Selecteer **OK**. De regels die u hebt geselecteerd zijn gekopieerd naar uw nieuwe inkooporder.

## <a name="copy-lines-to-an-existing-purchase-order"></a>Regels kopiëren naar een bestaande inkooporder  

In plaats van een volledige order te kopiëren, is het gebruikelijker om een nieuwe inkooporder te maken, informatie in te voeren in de IO-koptekst en vervolgens afzonderlijke regels te kopiëren vanuit bestaande orders.  

1. Selecteer **Inkooporderregel**.
1. Selecteer **Van alle**. De pagina die wordt geopend is identiek aan de eerder weergegeven pagina, maar er zijn andere opties geselecteerd wanneer deze wordt geopend vanuit de weergave van de orderregels. Laten we de parameters maar eens gaan bekijken.
1. Vouw de sectie **Parameters** uit.

    - De optie **Inkoopregels verwijderen** is niet ingeschakeld. Dit betekent dat u nieuwe regels naar uw order kunt kopiëren zonder bestaande regels te verwijderen.
    - De optie **Orderkoptekst kopiëren** is eveneens niet ingeschakeld, aangezien we alleen extra regels aan de order toevoegen.
    - In dit voorbeeld gaan we regels kopiëren vanuit een bestaande inkooporder.

1. Selecteer de regel met de gewenste inkooporder. Merk op dat de ene orderregel in deze inkooporder eveneens is geselecteerd.  
1. Selecteer **OK**. De extra orderregel is toegevoegd aan uw inkooporder.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Bankafschriften afstemmen via geavanceerde bankafstemming
description: Met de functie Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en deze automatisch afstemmen met banktransacties in Microsoft Dynamics 365 Finance. In dit onderwerp wordt het afstemmingsproces uitgelegd.
author: saraschi2
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: roschlom
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92c04a47b134584280736f4d3d2fa401d2a2a9b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969423"
---
# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Bankafschriften afstemmen via geavanceerde bankafstemming

[!include [banner](../includes/banner.md)]

Met de functie Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en deze automatisch afstemmen met banktransacties in Dynamics 365 Finance. In dit onderwerp wordt het afstemmingsproces uitgelegd.  

<a name="import-an-electronic-bank-statement"></a>Een elektronisch bankafschrift importeren
-----------------------------------

U importeert uw bankafschriften met behulp van de actie **Afschrift importeren** op de pagina **Bankafschriften**. De bankrekening wordt op het bankafschrift geïdentificeerd door een combinatie van waarden die zijn ingesteld voor de bankrekeninggegevens. Deze waarden omvatten de banknaam, het bankrekeningnummer, het routenummer, de SWIFT-code (Society for Worldwide Interbank Financial Telecommunication) en het internationale bankrekeningnummer (IBAN-nummer). 

U kunt een bankafschrift uploaden dat informatie bevat voor één rekening of voor meerdere rekeningen. Als het om meerdere rekeningen gaat, kunnen de rekeningen zich bevinden in andere rechtspersonen.

-   Als u een enkel bankafschriftbestand wilt importeren voor een enkele rekening, stelt u de optie **Afschrift importeren voor meerdere bankrekeningen in alle rechtspersonen** in op **Nee** en selecteert u de bankrekening die is gekoppeld aan het afschrift. Klik op **Bladeren** om het bijbehorende bankafschriftbestand te selecteren en klik vervolgens op **Uploaden**.
-   Als u een enkel bankafschriftbestand wilt importeren voor meerdere rekeningen, stelt u de optie **Afschrift importeren voor meerdere bankrekeningen in alle rechtspersonen** in op **Ja**. Klik op **Bladeren** om het bijbehorende bankafschriftbestand te selecteren en klik vervolgens op **Uploaden**.

Als afschriften in het elektronisch bestand niet aan een bankrekening kunnen worden gekoppeld, of als een afschrift is gekoppeld aan meerdere bankrekeningen door middel van de identificatievelden, worden deze niet geïmporteerd. Andere afschriften in het bestand kunnen echter nog wel worden geïmporteerd. De gebruiker ontvangt een bericht waarin wordt gemeld dat het importeren van bankafschriften voor specifieke bankrekeningen niet is geslaagd. Let erop dat de gebruiker die het bankafschriftbestand importeert, toegang tot een rechtspersoon moet hebben om afschriften voor de bankrekeningen van die rechtspersoon te kunnen importeren. 

U kunt ook door middel van een zip-bestand in één proces meerdere afschriftbestanden uploaden naar Finance. Als u wilt meerdere bankafschriftbestanden wilt importeren voor meerdere rekeningen, combineert u alle bankafschriftbestanden in één zipbestand. Stel in het dialoogvenster **Bankafschriften importeren** de optie **Afschrift importeren voor meerdere bankrekeningen in alle rechtspersonen** in op **Ja**. Klik op **Bladeren** om het zip-bestand te selecteren dat de bankafschriftbestanden bevat en klik vervolgens op **Uploaden**. Het importproces herkent het zip-bestand en uploadt alle afschriften daaruit, ongeacht de rechtspersoon waaraan de bankrekening is gekoppeld.

Er is een optie **Afstemmen na importeren** beschikbaar. Als u deze optie instelt op **Ja**, valideert het systeem automatisch het bankafschrift, maakt een nieuwe bankafstemming en werkblad en voert de set met standaardregels voor afstemming uit als het bankafschrift wordt geüpload. Deze functie automatiseert het proces tot aan het punt waar transacties handmatig moeten worden afgestemd.

## <a name="validate-the-bank-statement"></a>Het bankafschrift valideren
Als u een afschrift wilt valideren, klikt u op de pagina **Bankafschriften** op **Valideren**. Bankafschriften moeten worden gevalideerd voordat zij kunnen worden afgestemd. Deze stap wordt automatisch uitgevoerd als u de optie **Afstemmen na importeren** instelt op **Ja** wanneer u de import uitvoert. 

Bij validatie van bankafschriften worden de volgende gegevens geverifieerd:

-   Het bankafschrift moet overeenkomen met de geselecteerde bankrekening.
-   De valuta van de bankafschrift moet overeenkomen met de valuta van de bankrekening.
-   Het beginsaldo van het afschrift moet gelijk zijn aan het eindsaldo van het vorige afschrift voor de bankrekening.
-   De datum mag de datum voor een ander bankafschrift voor dezelfde bankrekening niet overlappen.
-   Er mogen geen tussenruimten zijn tussen de datums voor afschriften voor de bankrekening.
-   Datums op de afschriftregels moeten tussen de begindatum en einddatum van het bankafschrift liggen.
-   Het beginsaldo en samengevatte regelbedragen moeten gelijk zijn aan het eindsaldo.

Wanneer de validatie is voltooid, wordt de status van het bankafschrift bijgewerkt naar **gevalideerd**. Een bankafschrift moeten worden gevalideerd voordat dit kan worden afgestemd.

## <a name="reconcile-the-bank-statement"></a>Het bankafschrift afstemmen
Nadat u een elektronisch bankafschrift hebt geïmporteerd en het afschrift hebt gevalideerd op de pagina **Bankafschriften**, kunt u het bankafschrift afstemmen met behulp van de pagina's **Bankafstemming** en **Werkblad voor bankafstemming**. 

Klik op de pagina **Bankafstemming** op **Nieuw** om een nieuwe afstemming te maken en selecteer vervolgens de bankrekening van het afschrift dat is geïmporteerd. Een bankrekening kan slechts één open bankafstemming hebben. De afsluitdatum bepaalt de bankafschrifttransacties en Operations-banktransacties die zijn opgenomen op het werkblad voor afstemming. Standaard wordt de huidige systeemdatum wordt gebruikt als de afsluitdatum, maar u kunt de datum voor afstemming wijzigen. De resterende koptekstinformatie wordt automatisch opgehaald uit het afschrift. Deze stap wordt automatisch uitgevoerd als u de optie **Afstemmen na importeren** instelt op **Ja** wanneer u de import uitvoert. 

Klik op de pagina **Bankafstemming** op **Werkblad** om de pagina **Werkblad voor bankafstemming** te openen. Als u de optie **Afstemmen na importeren** instelt op **Ja**, wordt automatisch de set met standaardregels voor afstemming uitgevoerd voor de afstemming. Als u handmatig afstemmingsregels wilt uitvoeren, klikt u op **Afstemmingsregels uitvoeren** om de sets met afstemmingsregels of de afstemmingsregels te selecteren die u wilt uitvoeren op de banktransacties. Als u veel transacties te verwerken hebt, kunt u deze stap uitvoeren als een batchproces. 

De pagina **Werkblad voor bankafstemming** heeft vier rasters die transacties bevatten. De bovenste twee rasters bevatten transacties van het bankafschrift en Operations-transacties die nog niet zijn afgestemd. De onderste twee rasters geven afgestemde transacties weer. Het tabblad **Details van bankafschrift-transactie** bevat details voor de niet-afgestemde bankafschrifttransactie die is geselecteerd in het bovenste raster. 

Er zijn drie manieren om bankafschrifttransacties af te stemmen:

-   De transacties afstemmen met Operations-banktransacties.
-   De transacties afstemmen met een omgekeerde bankafschrifttransactie.
-   Markeer de transacties als **Nieuw**, zodat zij later kunnen worden geboekt als een banktransactie in Finance.

Als u transacties handmatig wilt afstemmen, selecteert u de transacties in het raster **Bankafschrifttransacties**, selecteert u de bijbehorende transacties in het raster **Operations-banktransacties** en klikt u vervolgens op **Afstemmen**. De geselecteerde transacties worden verplaatst van de bovenste rasters voor niet-afgestemde transacties naar de lagere rasters voor afgestemde transacties. Bovendien worden de afgestemde en niet-afgestemde totaalbedragen bijgewerkt. U kunt één-op-één, veel-op-één en veel-op-veel transactieafstemmingen hebben. Afstemmingen moeten voldoen aan de regels voor toegestane datumverschillen en toewijzing van het transactietype. Deze regels worden ingesteld op de pagina **Parameters voor Contanten en bankbeheer**.

In uw afstemming kunnen afrondingsverschillen optreden. U kunt een enkele bankafschrifttransactie en een enkele Operations-banktransactie met afrondingsverschillen afstemmen als de afrondingen binnen het tolerantiebedrag liggen dat is gedefinieerd door het veld **Toegestane afrondingsverschil** van de bankrekening. Het bedrag wordt weergegeven in het veld **Correctiebedrag** in de gecorrigeerde Operations-banktransactie. Wanneer de bankafstemming is gemarkeerd als afgestemd, worden de correcties automatisch geboekt door middel van de hoofdrekening die voor het gekoppelde banktransactietype is gedefinieerd. Correcties wordt niet ondersteund voor de documenttypen **Cheque** en **Deposito**. 

Terugboekingen van bankafschrifttransacties worden afgestemd met behulp van het werkblad voor afstemming. Twee afschriftregels kunnen worden afgestemd als de bedragen tegengesteld zijn en als een van de transacties is gemarkeerd als een terugboeking. U kunt ook een afstemmingsregel opstellen voor de actie **Terugboekingsregels op een afschrift wissen**.

Teruggeboekte Operations-banktransacties moeten worden afgestemd met behulp van de pagina **Operations-banktransacties**. U kunt twee Operations-banktransacties samen afstemmen als de documenten dezelfde bankrekening, dezelfde documentsoort en hetzelfde betalingskenmerk hebben, plus tegengestelde bedragen. U kunt ook één geannuleerde cheque afstemmen om te voorkomen dat deze transacties worden weergegeven op het werkblad voor afstemming. 

Als er nieuwe, door de bank geïnitieerde transacties zijn, zoals rente en kosten, die nog niet in Finance zijn opgenomen, kunt u ze toevoegen aan een journaal dat is gekoppeld aan de geselecteerde bankafschriftafstemming. Selecteer een bankafschrifttransactie in het raster **Bankafschrifttransacties** voor niet-gerelateerde transacties en klik vervolgens op **Markeren als nieuw**. De status van de transactie is ingesteld op **Nieuw** en de transactie wordt verplaatst naar het raster **Bankafschrifttransacties** voor afgestemde transacties. U boekt transacties die zijn gemarkeerd als **Nieuw** op een later tijdstip, vanaf de pagina **Bankafschrift**. 

U kunt de afstemming ongedaan maken van transacties die niet goed zijn afgestemd. Selecteer de afgestemde bankafschrifttransactie en klik vervolgens op **Afstemming ongedaan maken**. Alle bijbehorende transacties worden teruggeplaatst naar de bovenste rasters voor niet-afgestemde transacties en de afgestemde en niet-afgestemde totaalbedragen worden bijgewerkt. 

Nadat uw afstemmingsproces is voltooid, moet u het werkblad voor bankafstemming als afgestemd markeren.  Met dit proces worden automatisch correctiebedragen geboekt via de rekeningen ingesteld op de pagina **Banktransactietype**.  De bankafstemming voor een overzicht kan op elk moment worden gemarkeerd als afgestemd, zelfs als er regels van bankafschriften nog niet zijn afgestemd.  De niet-afgestemde transacties worden automatisch naar het volgende afstemmingswerkblad verplaatst als niet-afgestemde bankafschrifttransacties die moeten worden afgestemd.  Wanneer een bankafschriftafstemming is gemarkeerd als afgestemd, kan dit niet ongedaan worden gemaakt.  De afstemming kan niet meer worden bewerkt en u kunt die afstemming niet meer bijwerken.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Nieuwe transacties boeken die aan de afstemming zijn gekoppeld
Bankafschrifttransacties die u hebt gemarkeerd als **Nieuw** op het werkblad voor afstemming, worden geboekt op de pagina **Bankafschrift**. Selecteer op de pagina **Bankafschrift** de afschrift-id om de details van het afschrift te bekijken. In het menu **Boekhouding** kunt u de opties **Verdelingen weergeven** en **Boekhouding weergeven** gebruiken om details achter de nieuwe transacties en de bijbehorende grootboekvermeldingen te bekijken. Selecteer de optie **Boeken** om de bankafschriftregels die zijn gemarkeerd als **Nieuw** naar het grootboek te boeken. Houd er rekening mee dat boeken slechts één keer per bankafschrift kan worden voltooid.




--- 
title: De onderdelen van indelingen toewijzen aan gegevensmodelelementen
description: In de volgende procedure ziet u hoe een gebruiker in de rol van systeembeheerder of de ER-ontwikkelaar elementen van gegevensmodellen kan toewijzen aan onderdelen van de gemaakte ER-configuratie, waarin een elektronisch document voor het zakelijk domein van betalingen wordt gedefinieerd.
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: e065cfbfc645bb7ac48134fe43d87bec013e8c81
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="map-the-components-of-formats-to-data-model-elements"></a>De onderdelen van indelingen toewijzen aan gegevensmodelelementen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende procedure ziet u hoe een gebruiker in de rol van systeembeheerder of de ER-ontwikkelaar elementen van gegevensmodellen kan toewijzen aan onderdelen van de gemaakte ER-configuratie, waarin een elektronisch document voor het zakelijk domein van betalingen wordt gedefinieerd. Met deze indeling worden later elektronische documenten gegenereerd voor de verwerking van betalingen. In dit voorbeeld maakt u een indelingsconfiguratie voor het voorbeeldbedrijf Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd wanneer ER-configuraties tussen alle bedrijven worden gedeeld. Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de taakbegeleiding 'Een indelingsconfiguratie maken' uitvoeren.


## <a name="select-a-format-configuration"></a>Een indelingsconfiguratie selecteren
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Rapportconfiguraties.
3. Vouw 'Betalingen (vereenvoudigd model)' in de structuur uit.
4. Selecteer 'Betalingen (vereenvoudigd model)\BACS (UK fictief)' in de structuur uit.
5. Klik op Ontwerper.

## <a name="map-format-components-to-data-model-elements"></a>Indelingsonderdelen toewijzen aan gegevensmodelelementen
1. Klik op Uitvouwen/samenvouwen.
2. Klik op het tabblad Toewijzing.
3. Vouw in de structuur "model" uit.
4. Selecteer in de structuur 'Xml\Message\ProcessingDate\DateTime'.
5. Selecteer in de structuur 'model\ProcessingDateTime'.
6. Klik op Binden.
7. Selecteer in de structuur 'Xml\Message\MessageId\String'.
8. Selecteer in de structuur 'model\MessageIdentification'.
9. Klik op Binden.
10. Vouw "model\Payments" uit in de structuur.
11. Selecteer in de structuur 'Xml\Message\Payments\Item\Amount\String'.
12. Selecteer in de structuur 'model\Payments\InstructedAmount'.
13. Klik op Binden.
14. Selecteer in de structuur 'Xml\Message\Payments\Item\TransDate\DateTime'.
15. Selecteer in de structuur 'model\Payments\TransactionDate'.
16. Klik op Binden.
17. Selecteer in de structuur 'Xml\Message\Payments\Item\Description\String'.
18. Selecteer "model\Payments\Description" in de structuur.
19. Klik op Binden.
20. Selecteer in de structuur 'Xml\Message\Payments\Item\Currency\String'.
21. Selecteer 'model\Payments\Currency' in de structuur.
22. Klik op Binden.
23. Selecteer in de structuur 'Xml\Message\Payments\Item\Id'.
24. Selecteer in de structuur 'model\Payments\End2EndID'.
25. Klik op Binden.
26. Vouw "model\Payments\Creditor" uit in de structuur.
27. Vouw "model\Payments\Creditor\Account" uit in de structuur.
28. Vouw "model\Payments\Creditor\Agent" uit in de structuur.
29. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Name\String'.
30. Selecteer "model\Payments\Creditor\Name" in de structuur.
31. Klik op Binden.
32. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.
33. Selecteer in de structuur 'model\Payments\Creditor\Agent\RoutingNumber'.
34. Klik op Binden.
35. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.
36. Selecteer "model\Payments\Creditor\Account\Number" in de structuur.
37. Klik op Binden.
38. Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Name\String'.
39. Vouw "model\Payments\Debtor" uit in de structuur.
40. Vouw "model\Payments\Debtor\Account" uit in de structuur.
41. Vouw "model\Payments\Debtor\Agent" uit in de structuur.
42. Selecteer "model\Payments\Debtor\Name" in de structuur.
43. Klik op Binden.
44. Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.
45. Selecteer in de structuur 'model\Payments\Debtor\Agent\RoutingNumber'.
46. Klik op Binden.
47. Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.
48. Selecteer "model\Payments\Debtor\Account\Number" in de structuur.
49. Klik op Binden.
50. Selecteer in de structuur 'Xml\Message\Payments\Item'.
51. Selecteer "model\Payments" in de structuur.
52. Klik op Binden.
53. Klik op Opslaan.

## <a name="validate-format-mapping"></a>Indelingstoewijzing valideren
1. Klik op Valideren.
    * De nieuwe toewijzing valideren om te controleren of alle bindingen in orde zijn.  
2. Sluit de pagina.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Status van de huidige versie van de indelingsconfiguratie wijzigen
    * In de volgende stappen gaat u de status van de indelingsconfiguratie wijzigen van Concept naar Voltooid, om deze beschikbaar te maken voor het genereren van betalingsdocumenten.  
1. Klik op Status wijzigen.
2. Klik op Voltooien.
3. Typ een waarde in het veld Omschrijving.
    * Bijvoorbeeld: 'versie 1'.  
4. Klik op OK.
5. Selecteer de ingevulde versie van de huidige configuratie.
    * Merk op dat de configuratie wordt opgeslagen als voltooide versie 1.1: versie 1 van de indeling, gebaseerd op versie 1 van het gegevensmodel.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Ingangsdatum voor voltooide versie van indeling definiëren
    * Elke indelingsversie kan worden geconfigureerd als beschikbaar voor gebruik vanaf een bepaalde datum. Wanneer meer dan één indelingsversie actief is op een bepaalde datum, wordt de meest recente indeling (op basis van versienummer) geselecteerd voor gebruik. De waarde van de sessiedatum wordt gebruikt voor selectie van de juiste versie.  

## <a name="restrict-access-to-created-format-from-companies"></a>Toegang tot gemaakte indeling van bedrijven beperken
1. Vouw de sectie ISO-land-/regiocodes uit.
    * Elke indelingstoegang kan worden beperkt door bepaalde landen/regio's te identificeren waarin een indeling van toepassing is. Als de lijst met landen/regio's voor een specifieke indeling leeg is, kan deze indeling worden gebruikt in elk bedrijf. Als enkele ISO-land-/regiocodes worden ingevoegd in de lijst met landen/regio's, kan deze indeling alleen in bedrijven worden gebruikt waarvan het primaire adres in de land-/regiocode uit die lijst is gelegen.  



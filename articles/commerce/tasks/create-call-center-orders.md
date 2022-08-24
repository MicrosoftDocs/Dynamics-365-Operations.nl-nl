---
title: " Callcenterorders maken"
description: Dit artikel doorloopt een voorbeeldprocedure waarin een callcenter-gebruiker een klant opzoekt, een nieuwe order aanmaakt, een product opzoekt en een betaling van de klant int in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228505"
---
# <a name="create-call-center-orders"></a> Callcenterorders maken

[!include [banner](../includes/banner.md)]

Dit artikel doorloopt een voorbeeldprocedure waarin een callcenter-gebruiker een klant opzoekt, een nieuwe order aanmaakt, een product opzoekt en een betaling van de klant int in Microsoft Dynamics 365 Commerce. Deze procedure gebruikt het demobedrijf USRT en is bedoeld voor de verkoopordermedewerker. 

## <a name="prerequisites"></a>Vereisten

De gebruiker die deze procedure uitvoert moet als een callcenter-gebruiker zijn ingesteld. De halfjaarlijkse catalogus van Fabrikam kan optioneel worden gepubliceerd met minimaal één broncode.

### <a name="add-yourself-as-a-call-center-user"></a>Voeg uzelf toe als callcenter-gebruiker

Doorloop deze stappen als u uzelf als callcenter-gebruiker wilt toevoegen.

1. Ga in Commerce Headquarters naar **Retail en commerce \> Afzetkanalen \> Callcenters \> Alle callcenters**.
1. In het veld **Gebruikers** selecteert u **Kanaalgebruikers**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Gebruikers-id** uw gebruikers-id in.
1. Voer in het veld **Naam** uw gebruikersnaam in. De gebruikersnaam mag niet hetzelfde zijn als de gebruikers-id.
1. Selecteer **Opslaan** in het actievenster.
1. Terug naar **Retail en commerce \> Afzetkanalen \> Callcenters \> Alle callcenters**.
1. Selecteer de id van het detailhandelskanaal van het callcenter.
1. Bevestig dat de optie **Ordervoltooiing inschakelen** is ingesteld op **Ja**. Als de optie niet zichtbaar is, kunt u deze stap overslaan.

## <a name="complete-the-example-call-center-procedure"></a>De voorbeeldprocedure voor het callcenter voltooien

Volg deze stappen om de voorbeeldprocedure voor het callcenter te voltooien.

1. Ga naar **Retail en Commerce \> Klanten \> Klantenservice**.
1. Voer op het tabblad **Klant zoeken** de zoekcriteria in om de klant te zoeken. Voor deze voorbeeldprocedure voert u **Karen** in.
1. Selecteer **Zoeken**. Het dialoogvenster **Klant zoeken** verschijnt met de zoekresultaten.
1. Selecteer het klantenrecord voor **Karen Berg** met het accountnummer **2001** en kies vervolgens **Selecteren**.
1. Selecteer **Nieuwe verkooporder** in het actievenster.
1. Kies aan de rechterkant het tabblad **Header**.
1. Selecteer op het sneltabblad **Levering** in het veld **Leveringsmethode** de optie **99 Standard**.

    ![Een leveringsmethode selecteren.](../media/Select_Mode_of_Delivery.png)

1. Selecteer aan de rechterkant het tabblad **Regels**.
1. Voer in de sectie **Verkooporderregels** in de nieuwe regel voor de nieuwe verkoopregel, in het veld **Itemnummer** het itemnummer in om naar te zoeken. Voor deze voorbeeldprocedure **81327** in en selecteer het product in de vervolgkeuzelijst om dit aan de verkooporder toe te voegen.
1. Voer in het veld **Hoeveelheid** de hoeveelheid verkopen in.
1. Selecteer in het veld **Broncode** de naam van de broncode voor de catalogus. Als er geen actieve broncodes zijn, kunt u deze stap overslaan.
1. Selecteer **Voltooien** in het actievenster om de klantbetaling vast te leggen. Met deze actie wordt de **Overzicht van verkooporder** geopend waarin het totale bedrag dat moet worden betaald wordt weergegeven. Deze actie triggert ook de berekening van eventuele kosten zoals verzending en verwerking en toont deze in het dialoogvenster **Overzicht van verkooporder**.

    ![Voltooi de knop.](../media/Complete_button.png)

1. In het dialoogvenster **Overzicht van verkooporder** op het sneltabblad **Betalingen** selecteert u **Toevoegen** om de betalingen vast te leggen.

    ![Dialoogvenster Overzicht van verkopen.](../media/order_summary.png)

1. In het dialoogvenster **Klantbetalingsgegevens invoeren** in het veld **Betalingsmethode** selecteert u de betalingsmethode. Selecteer **Cash** voor deze voorbeeldprocedure.
1. Voer in het veld **Betalingsbedrag** het te betalen bedrag in. Voer voor dit voorbeeld **120,00** in, wat gelijk is aan het ordersaldo dat in het dialoogvenster **Overzicht verkooporder** wordt weergegeven. Door dit bedrag in te voeren, kunt u de order dan voltooien als volledig betaald.
1. Selecteer **OK**.
1. Selecteer **Indienen**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Transactionele e-mails aanpassen per leveringsmethode](../customize-email-delivery-mode.md)

[Leveringsmethode wijzigen in POS](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

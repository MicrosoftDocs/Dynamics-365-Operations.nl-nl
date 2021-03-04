---
title: " Callcenterorders maken"
description: Deze procedure doorloopt het opzoeken van een klant, het maken van een nieuwe order, het zoeken naar een product en het innen van betaling van de klant.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c875eaa85d9da997b75b296ad9ace99ae1e91798
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594231"
---
# <a name="create-call-center-orders"></a> Callcenterorders maken

[!include [banner](../includes/banner.md)]

Deze procedure doorloopt het opzoeken van een klant, het maken van een nieuwe order, het zoeken naar een product en het innen van betaling van de klant. Deze procedure gebruikt het demobedrijf USRT en is bedoeld voor de verkoopordermedewerker. Vereisten: de gebruiker die de procedure uitvoert, is ingesteld als een callcentergebruiker en de halfjaarlijkse catalogus van Fabrikam wordt gepubliceerd met minimaal één broncode.

1. Ga naar **Retail en Commerce \> Klanten \> Klantenservice**.
2. Voer bij **Zoektekst** de zoekcriteria in om de klant te zoeken.
    * Voor deze voorbeeldprocedure voert u 'Karen' in en selecteert u **Tab**.  
3. Selecteer Zoeken.
    * Aangezien er slechts één klant met de naam Karen voorkomt in de demogegevens, wordt het resultaat automatisch geselecteerd.  
4. Selecteer **Nieuwe verkooporder**.
5. Vouw de koptekstsectie **Verkooporder** uit of samen.
6. Selecteer de broncode voor de catalogus.
    * Als er geen actieve broncodes zijn, kunt u deze stap overslaan.  
7. Selecteer **Regel toevoegen**.
8. Voer voor **Artikelnummer** de zoekterm voor het artikel in.
    * Voor deze voorbeeldprocedure voert u het gedeeltelijke artikelnummer 8111 in en drukt u op Tab. Het venster voor het zoeken van artikelen wordt dan weergegeven.  
9. Selecteer het product dat aan de verkooporder moet worden toegevoegd.
10. Voer de verkoophoeveelheid in.
11. Selecteer **Maken**.
12. Selecteer **Voltooien** om de betaling van de klant vast te leggen.
13. Selecteer **Toevoegen**.
    * De koppeling Toevoegen bevindt zich op het tabblad Betalingen. Vouw het tabblad Betalingen uit als het is samengevouwen.  
14. Selecteer de betalingsmethode.
    * Selecteer voor deze procedure de contante betalingsmethode.  
15. Sluit de pagina.
16. Geef het bedrag op.
    * Voor deze procedure voert u een bedrag in dat gelijk is aan het ordersaldo dat wordt weergegeven op de pagina Overzicht van verkooporder, links van het bedragveld. U kunt de order dan voltooien als volledig betaald.  
17. Selecteer **OK**.
18. Selecteer **Indienen**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Transactionele e-mails aanpassen per leveringsmethode](../customize-email-delivery-mode.md)

[Leveringsmethode wijzigen in POS](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
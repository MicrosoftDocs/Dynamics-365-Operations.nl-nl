---
title: Betalingsmethoden in een callcenter
description: In dit onderwerp komen de verschillende betalingsmethoden aan bod die u in een callcenter in Dynamics 365 for Retail kunt gebruiken.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 52b3e2e78a03ac67507ee65a03e0884e5ed44678
ms.openlocfilehash: 321d03d154c224b55ffedbe55a2d5952c2b29d9a
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

---

# <a name="payment-methods-in-a-call-center"></a>Betalingsmethoden in een callcenter

[!include[banner](includes/banner.md)]


In dit onderwerp komen de verschillende betalingsmethoden aan bod die u in een callcenter in Dynamics 365 for Retail kunt gebruiken.

De betalingsmethoden die in andere kanalen worden gebruikt, zoals contant geld, cheques, creditcards en geschenkbonnen, kunnen ook in callcenters worden gebruikt. Nadat u een betalingsmethode voor een callcenter hebt ingesteld, verschijnt deze als een van de opties in het gedeelte **Betalingen** van de pagina **Verkooporder** voor callcentersgebruikers. Bovendien kunt u coupons instellen om kortingen aan te bieden aan klanten die een order plaatsen bij het callcenter van uw organisatie. Coupons kunnen voor een vast kortingsbedrag zijn of voor een percentage van een artikelprijs of voor het ordertotaal. Bijvoorbeeld, een op een bedrag gebaseerde coupon biedt klanten mogelijk een korting van 75,00 aan wanneer de klant 750,00 of meer besteedt. U kunt verschillende typen kortingsbonnen maken, bovenliggende/onderliggende coupons instellen en een coupon kopiëren of ongeldig maken. Gebruik de opties in de volgende tabel voor het maken van coupons.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kenmerk**             | Voer in het veld **Inwisseltarief** het verwachte inwisseltarief van de coupon in als percentage en selecteer vervolgens of de coupon één keer kan worden gebruikt, of deze automatisch opnieuw wordt uitgegeven en of deze specifiek is voor een klant.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Geldig**                 | Voer in de velden **Begindatum** en **Einddatum** de eerste en laatste datum in waarop de coupon geldig is.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Regels opnemen/uitsluiten** | Selecteer in de velden **Catalogi** en **Artikelen** of er catalogi of artikelen zijn waarvoor de coupon geldig of ongeldig is. Als u **Opnemen** of **Uitsluiten** selecteert, klikt u op **Instellen**, selecteert u **Catalogi opnemen/uitsluiten** of **Producten opnemen/uitsluiten** en voert u informatie over de catalogus of het artikel in. Als u **Geen** selecteert in deze velden, worden alle catalogi of artikelen opgenomen in de coupon.                                                                                                                                                                                                                          |
| **Overige**         | Als deze coupon niet kan worden gebruikt in combinatie met andere kortingen, schakelt u het selectievakje **Exclusief** in. Vervolgens selecteert u in het veld **Oorsprong** waar de coupon kan worden gebruikt. Als deze coupon een coupon van de fabrikant is, schakelt u het selectievakje **Fabrikantcoupon** in.                                                                                                                                                                                                                                                                                                                                                                |
| **Toekomstige coupon**         | Als deze coupon als bovenliggende coupon wordt gekoppeld aan andere coupons, schakelt u het selectievakje **Bovenliggende coupon** in. Als deze coupon als onderliggende coupon aan een bestaande coupon moet worden gekoppeld, selecteert u de bovenliggende coupon in het veld **Id van bovenliggende coupon**. Zo kunt u bijvoorbeeld een coupon maken voor de komende lentecatalogus. Alle andere coupons die u voor de lentecatalogus maakt. zijn dan onderliggende kortingen van de coupon van de lentecatalogus. Onderliggende coupons kunnen een korting van 20 procent voor nieuwe klantorders bevatten, een korting van 10 procent op een nieuw artikel of een korting van 95,00 voor orders van 1.000,00 of meer. |

Als u een van creditcardbetaling indient vanaf de pagina **Verkooporder** en een bericht ontvangt waarin staat dat de kaart niet is geautoriseerd, kunt u de autorisatie handmatig verwerken. U kunt een creditcardtransactie toestaan, weigeren of opnieuw indienen met behulp van de pagina **Autorisatiebeheer**. U gebruikt de pagina met callcenterparameters om extra opties voor betalingsverwerking te configureren:

-   Met Chequeblokkeringen kan financieel personeel orders verwerken die in de wachtstrand zijn geplaatst omdat een cheque is gebruikt als betalingsmethode en het drempelbedrag voor chequeblokkering is overschreden. De blokkering kan handmatig worden vrijgegeven of verloopt automatisch aan het einde van de geconfigureerde periode.
-   U kunt drempels instellen waarboven restituties die worden verstrekt via cheques en creditcards handmatig moeten worden goedgekeurd. Elke restitutie die het drempelbedrag overschrijdt, wordt toegevoegd aan de goedkeuringswachtrij. Nadat u de restitutie goedkeurt, kan de retourverkooporder worden gefactureerd.






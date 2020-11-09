---
title: Productontvangst tegen inkooporders
description: In dit onderwerp worden de verschillende opties voor het registreren van producten als ontvangen beschreven.
author: mkirknel
manager: tfehr
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, VendPackingSlipJournalListPage, VendPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cead310eaa86d755399e512f99d6782bfa551211
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018854"
---
# <a name="product-receipt-against-purchase-orders"></a>Productontvangst tegen inkooporders

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de verschillende opties voor het registreren van producten als ontvangen beschreven.

Productontvangst is het proces van het vastleggen van de ontvangst van bestelde producten, zodat de inkooporderregels (IO) vervolgens kunnen worden verwerkt voor facturering. In sommige gevallen doorlopen producten een proces van voorafgaande registratie, waarbij aanvullende informatie van de leverancier wordt vastgelegd voordat de producten worden ontvangen. Wanneer producten binnenkomen, worden zij eerst gemarkeerd als **Geregistreerd**. De producten doorlopen vervolgens mogelijk aanvullende processen, zoals kwaliteitsbeheer, voordat zij definitief worden gemarkeerd als **Ontvangen**.

## <a name="preregistration-asn"></a>Registratie vooraf (ASN)
Mogelijk delen leveranciers informatie over producten die worden verzonden. In dat geval kunt u de producten vooraf registreren om deze informatie vast te leggen voordat de producten worden ontvangen. Door producten vooraf te registreren, kunt u de hoeveelheid werk die is vereist tijdens artikelregistratie en -ontvangst verminderen. Leveranciers kunnen productinformatie in elektronische vorm aanbieden door middel van een Advance Shipping Notice (ASN) die vervolgens automatisch wordt vastgelegd in het systeem. De informatie in de ASN bevat de hoeveelheid producten die zal worden verzonden en de datum waarop ze worden verzonden. De ASN biedt mogelijk ook informatie zoals batch- of serienummers. Registratie van de ASN vindt plaats in de module **Transportbeheer**.

## <a name="registration"></a>Registratie
Productontvangstregistratie treedt vaak op bij de inbound docks in een magazijn. Deze wordt uitgevoerd met behulp van een handheld-apparaat of via ontvangstjournalen. U kunt ook handmatig de ontvangst van producten registreren met behulp van de actie **Registratie** op de pagina **Inkooporder**. In beide gevallen, worden de producten gemarkeerd als **Geregistreerd**. Merk op dat de producten nog niet zijn gemarkeerd als **Ontvangen**.  

Producten die worden ontvangen in een magazijn kunnen kwaliteitscontrole doorlopen voordat ze worden weggezet in de voorraad. Kwaliteitsorders of quarantaineorders kunnen worden gebruikt voor het uitvoeren van kwaliteitscontrole. Als kwaliteitsorders worden gebruikt, kunt u het proces zodanig configureren producten tijdelijk worden geblokkeerd door middel van een reservering terwijl ze worden gecontroleerd. Als quarantaineorders worden gebruikt, worden producten naar een ander magazijn verplaatst voor inspectie. Dit magazijn staat bekend als het quarantainemagazijn. In beide processen voor kwaliteitsinspectie wordt een aantal van de goederen mogelijk buiten gebruik gesteld, omdat zij niet aan de kwaliteitsverwachtingen voldoen of de kwaliteitscontrole het destructieve testen van een monster van het product behelst.

## <a name="product-receipt"></a>Productontvangstbon
In de meeste gevallen, wordt de actie **Productontvangst** op de pagina **Inkooporders** gebruikt voor het markeren van producten als **Ontvangen** op de inkooporder. De pagina **Productontvangstbon boeken** heeft verschillende opties voor de hoeveelheid die administratief wordt verwerkt als ontvangen. U kunt bijvoorbeeld het veld **Hoeveelheid** instellen op **Bestelde hoeveelheid** of **Hoeveelheid nu ontvangen**. Ook zult u, als een magazijnontvangstproces is gebruikt, vaak dit veld instellen op **Geregistreerde hoeveelheid**. U kunt de hoeveelheden op elke orderregel die wordt gemarkeerd als **Ontvangen** wijzigen ten behoeve van eventuele afwijkingen, zoals minderlevering en meerlevering. Tijdens de ontvangst van producten, moet u een id van de productontvangstbon opgeven, die meestal een verwijzing naar de pakbon van de leverancier vormt. Deze id is vereist voor de boekhouding, omdat deze controles of audits van de pakbonnen van leveranciers tegen wat is ontvangen en de naberekende voorraad of onkosten mogelijk maakt.  

Inkooporders kunnen worden gemaakt voor producten die niet zijn bedoeld als voorraad, maar als onkosten worden beschouwd. Deze categorie bevat orderregels waarop de producten zijn gemarkeerd als **Niet-voorradig** door hun voorraadmodelgroep en ook regels die inkoopcategorieën gebruiken. In dit geval doorlopen de artikelen mogelijk de aankomstregistratie en ontvangst in het magazijn niet. In plaats daarvan, wordt de actie **Productontvangstbon** gebruikt voor het rechtstreeks in de inkooporder vastleggen van de ontvangst en is de ontvangst gebaseerd op de bestelde hoeveelheid, niet een geregistreerde hoeveelheid.  

U kunt inkooporderregels maken waarbij de optie **Nieuw vast activum** is ingeschakeld. Deze optie geeft aan dat de aankoop moet worden beschouwd als een vast activum in plaats van als voorraad. In dit geval bepalen de regels voor de bepaling van vaste activa die zijn geconfigureerd of de aankoop van het product of de categorie bepaalde drempelwaarden overschrijdt, en daarom als activum moet worden verwerkt en beheer van vaste activa moet doorlopen. Aankopen kunnen ook worden gedaan voor een bestaand vast activum. In dit geval wordt het bedrag zo nodig aangepast.  

U kunt meerdere orders selecteren en de ontvangst verwerken voor alle orders tegelijk. Deze benadering wordt niet vaak gebruikt, maar u kunt deze gebruiken als een leverancier geconsolideerde zendingen voor u heeft in een enkele lading. Tijdens de productontvangst voor de aankoop is er een functie voor het bijwerken van overzichten. Bij bijgewerkte overzichten kunt u een enkele pakbon van de leverancier boeken voor meer dan één inkooporder.  

Mogelijk kunnen inkooporders worden gemaakt op basis van een verkooporder waarvoor de **Rechtstreekse levering** is geselecteerd. Als rechtstreekse levering wordt gebruikt, komen de producten nooit in uw magazijn binnen, maar worden zij rechtstreeks van de leverancier naar de klant verzonden. In dit geval wordt de ontvangst meestal direct in de inkooporder vastgelegd. De ontvangst kan automatisch worden gedaan, bijvoorbeeld via EDI-integratie (Electronic Data Interchange) met de leverancier. Ook automatiseert Supply Chain Management de ontvangst op de intercompany-verkooporder als verzending plaatsvindt indien de inkooporder een intercompany-inkooporder is. Als rechtstreekse levering wordt gebruikt, worden producten nog steeds als voorraad beschouwd, hoewel zij niet fysiek in het magazijn aankomen. Daarom wordt, als de ontvangst van producten in de inkooporder wordt vastgelegd, de verkooporder automatisch bijgewerkt met een pakbon, zodat de totale wijziging in de voorraad 0 (nul) is. In scenario's voor rechtstreekse levering, moet u geen voorafgaande registratie vereisen. Als u magazijnen gebruikt die zijn ingeschakeld voor magazijnbeheer, kunt u het vereiste voor nummerplaatregistratie omzeilen door een virtueel magazijn op te geven. U geeft dit magazijn op in het veld **Rechtstreekse levering magazijn** op het product. 

Nadat de ontvangst van producten is verwerkt op de inkooporder, wordt de status van de inkooporder ingesteld op **Ontvangen** om aan te geven dat de factuur voor de order kan worden verwerkt. U kunt informatie over producten die al zijn ontvangen bekijken met behulp van de pagina **Productontvangstjournalen**.  

U kunt toegang tot deze pagina krijgen vanuit de actiegroep **Ontvangst** op de pagina **Inkooporder**. De informatie in de journalen bevat details over de hoeveelheden, datums en dimensies.

<a name="additional-resources"></a>Aanvullende resources
--------

[Overzicht van inkooporders](purchase-order-overview.md)

[Inkooporders maken](purchase-order-creation.md)

[Inkooporders goedkeuren en bevestigen](purchase-order-approval-confirmation.md)

[Overzicht van leveranciersfacturen](../../financials/accounts-payable/vendor-invoices-overview.md)




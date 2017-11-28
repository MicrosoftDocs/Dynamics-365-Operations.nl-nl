---
title: Instelling, autorisatie en registratie van creditcards
description: Dit artikel bevat een overzicht van de creditcardautorisatie in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Het bevat informatie over het instellen van een betaalservice, het toevoegen van een creditcard aan een verkooporder en het ongeldig maken van een autorisatie.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations, Core, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 40d636cac477871f094286d29edc32cd5616ad44
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="credit-card-setup-authorization-and-capture"></a>Instelling, autorisatie en registratie van creditcards

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Dit artikel bevat een overzicht van de creditcardautorisatie in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Het bevat informatie over het instellen van een betaalservice, het toevoegen van een creditcard aan een verkooporder en het ongeldig maken van een autorisatie.

<a name="setting-up-the-credit-card-payment-service"></a>De service voor betaling per creditcard instellen
------------------------------------------

Als u creditcards wilt gebruiken, moet u een betalingsservice instellen en activeren op de pagina Betalingsservices. Een betalingsservice fungeert als brug tussen uw rechtspersoon en de bank die de creditcardbetalingen van een klant verwerkt. U moet met een creditcardmaatschappij werken die in het veld Betalingsconnector staat vermeld en een rekening openen bij die provider. U moet vervolgens de andere opties op de pagina Betalingsservices instellen, de creditcardtypen instellen voor American Express, Discover, MasterCard en Discover op de pagina Typen creditcard en de provider activeren als de standaardprovider. U moet ook deze stappen uitvoeren om uw instelling te voltooien:
-   Geef op de pagina Parameters van module Klanten parameters op voor het gebruik van creditcardautorisaties.
-   Stel op de pagina Betalingsvoorwaarden betalingsvoorwaarden voor creditcards in. Selecteer Creditcard in het veld Type betaling.
-   Voer op de pagina Creditcards van klant creditcardgegevens voor klanten in.

## <a name="adding-a-new-credit-card"></a>Een nieuwe creditcard toevoegen
U kunt nieuwe creditcardrecords maken op de pagina Klanten door Klant, Instellingen, Creditcard te gebruiken. U kunt ook creditcardrecords maken wanneer u verkooporders invoert op de pagina Vverkooporder door gebruik te maken van Beheren, Klant, Creditcard, Registreren.
Een creditcard toevoegen aan een verkooporder
-------------------------------------

U kunt een creditcard toevoegen aan een verkooporder door een creditcard te selecteren in het zoekveld voor creditcards op het sneltabblad Prijs en kortingen op de pagina Verkooporder. U kunt het autorisatieproces starten door in het actievenster op het tabblad Beheren Creditcard en Autoriseren te selecteren.
Een creditcard autoriseren
-------------------------

Wanneer een creditcard wordt geautoriseerd, worden het kaartnummer en de naam van de kaarthouder geverifieerd en wordt ook het creditsaldo gecontroleerd. Eventueel worden de waarde voor kaartverificatie en het adres van de kaarthouder gecontroleerd. Het factuurbedrag wordt vervolgens afgetrokken van het creditsaldo van de klant. De betaalservice meldt of de creditcard is goedgekeurd of is geweigerd. Wanneer de verkooporder wordt gefactureerd, wordt de creditcard met het factuurbedrag belast.

### <a name="card-verification-value"></a>Kaartverificatiewaarde

U kunt de kaartverificatiewaarde opvragen. Dit wordt ook wel de beveiligingscode van de kaart genoemd. Dit is een waarde van vier cijfers voor American Express. Voor Discover, MasterCard en Visa is dit een waarde van drie cijfers.

### <a name="address-verification"></a>Adresverificatie

Adresverificatiegegevens worden altijd verzonden naar de betalingsprovider. U kunt beslissen hoeveel informatie vereist is voordat een transactie wordt geaccepteerd. Raadpleeg uw provider om te bepalen of deze informatie wordt geaccepteerd. Hier volgen de opties voor adresverificatie:
-   **Transactie altijd accepteren**– Accepteer de transactie, ongeacht de resultaten van de adresverificatie.
-   **Rekeninghouder** – Vergelijk de naam van de kaarthouder die is betrokken bij de transactie met de gegevens van het creditcardmaatschappij.
-   **Factureringsadres** – Vergelijk de naam en het factuuradres van de kaarthouder die is betrokken bij de transactie met de gegevens van de creditcardmaatschappij.
-   **Postcode factuuradres** – Vergelijk de naam, het factuuradres en de postcode van de kaarthouder die is betrokken bij de transactie met de gegevens van de creditcardmaatschappij.

## <a name="data-support"></a>Gegevensondersteuning
Voor elk creditcardtype dat wordt ondersteund, kunt u het niveau van ondersteuning van gegevens instellen. Het niveau bepaalt hoeveel informatie over een transactie wordt overgebracht naar de betalingsservice. Raadpleeg uw provider om te controleren of deze de gewenste gegevens kan verstrekken. Hier volgen de opties voor het niveau van gegevensondersteuning:
-   **Niveau 1** – Draag de transactiedatum, het transactiebedrag en de omschrijving over.
-   **Niveau 2** – Draag alle informatie van niveau 1 over, plus de verzend- en handelsadressen en de belastinggegevens.
-   **Niveau 3** – Draag alle informatie van niveau 2, plus orderregelgegevens over.

## <a name="partial-payments"></a>Gedeeltelijke betalingen
Als een deel van een order te verzendt, wordt het bedrag van de gedeeltelijke order vastgelegd en wordt de autorisatie, die voor het bedrag van de totale order was, gesloten. Vervolgens wordt een nieuwe autorisatie ingediend voor het resterende bedrag van de order die niet is verzonden.

## <a name="voiding-an-authorization"></a>Een autorisatie ongeldig maken 
U kunt een creditcardautorisatie ongeldig maken door de betalingsmethode te wijzigen in een andere methode die een bepaald type creditcard niet heeft.







---
title: Leveranciers configureren
description: In dit artikel worden de pagina's beschreven die u gebruikt voor het instellen van algemene en optionele functionaliteit voor Leveranciers in Microsoft Dynamics 365 for Finance and Operations. Daarnaast worden de stappen beschreven die u moet uitvoeren voordat u Leveranciers kunt instellen.
author: abruer
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf3226060eddf01fb218e99cae4097fecfe56e25
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506590"
---
# <a name="configure-accounts-payable"></a>Leveranciers configureren

[!include [banner](../includes/banner.md)]

In dit artikel worden de pagina's beschreven die u gebruikt voor het instellen van algemene en optionele functionaliteit voor Leveranciers in Microsoft Dynamics 365 for Finance and Operations. Daarnaast worden de stappen beschreven die u moet uitvoeren voordat u Leveranciers kunt instellen.

<a name="prerequisites-for-accounts-payable-setup"></a>Vereisten voor het configureren van Leveranciers
----------------------------------------

Voordat u Leveranciers kunt configureren, moet u de volgende instellingen uitvoeren:

-   In Grootboek
    -   Als u betalingsjournalen wilt gebruiken, moet u betalingsjournalen configureren.
    -   Als u van plan bent wisselkoerscorrecties uit te voeren, moet valutacodes configureren op de pagina Valuta, wisselkoerstypen configureren op de pagina Wisselkoerstypen en de wisselkoersen voor de valuta configureren op de pagina Valutawisselkoersen.
-   Stel in Contant- en bankbeheer de bankrekeningen in die u wilt gebruiken in combinatie met bepaalde betalingswijzen.

## <a name="setup-pages-for-accounts-payable"></a>Configuratiepagina's voor Leveranciers

Gebruik de volgende pagina's om de basisfunctionaliteit van Leveranciers in te stellen voor elke rechtspersoon. De pagina's worden weergegeven in de aanbevolen volgorde van configuratie. Voor een eenvoudiger configuratieproces kunt u sjablonen maken op basis van de eerste records die u maakt. In een sjabloon worden meestal waarden ingevuld in veel velden, die de functies vertegenwoordigen die de organisatie wil implementeren voor een bepaald type leverancier.
1.  Definieer op de pagina Betalingsvoorwaarden de betalingsvoorwaarden die u toewijst aan verkooporders, inkooporders, klanten en leveranciers, en die de vervaldatums van facturen bepalen. Zie [Bijzondere kosten voor leveranciersbetalingen definiëren](tasks/define-vendor-payment-fees.md) voor meer informatie.
2.  Maak en beheer op de pagina Betalingsmethoden - leveranciers informatie over hoe de organisatie zijn leveranciers betaalt.
3.  Maak en beheer op de pagina Leveranciersgroepen leveranciersgroepen die belangrijke parameters delen voor boeking, vereffening en betaling, rapportage en prognoses.
4.  Definieer op de pagina Leveranciersboekingsprofiel hoe leverancierstransacties naar het grootboek worden geboekt.
5.  Configureer op de pagina Parameters van module Leveranciers de standaardinstellingen die worden toegepast als geen specifiekere instelling is opgegeven, parameters voor verschillende typen functionaliteit en de verschillende nummerreeksen voor Leveranciers.
6.  Definieer op de pagina Formulierinstelling de indeling van verschillende documenten die gerelateerd zijn aan leveranciers en die de organisatie gebruikt om ontvangsten van leveranciers bij te houden en redenen in te voeren voor de betalingsstroom naar leveranciers.
7.  Maak en beheer op de pagina Leveranciers leverancierrekeningen, waaronder de btw-dienst waarbij uw organisatie btw-aangifte doet

## <a name="optional-setup-pages-for-accounts-payable"></a>Optionele instellingspagina´s voor Leveranciers
Naast de basisfunctionaliteit heeft Leveranciers nog andere functionaliteit die u kunt configureren.

De aanvullende configuratiepagina's zijn geordend op functionaliteit.

**Beleid**
-   Configureer op de pagina Leveranciersfactuurbeleid de beleidsregels voor leveranciersfacturen.

**Factuurvereffening**

-   Configureer op de pagina Toleranties voor factuurtotalen de toleranties voor factuurtotalen.
-   Configureer op de pagina Overeenstemmingbeleid het beleid voor tweewegs- of driewegsovereenstemming.
-   Configureer op de pagina Prijstoleranties de toleranties voor eenheidsprijzen.
-   Configureer op de pagina Tolerantiegroepen voor artikelprijzen de tolerantiegroepen voor artikelprijzen.
-   Configureer op de pagina Tolerantiegroepen voor leveranciersprijzen de tolerantiegroepen voor leveranciersprijzen.
-   Configureer op de pagina Toeslagentoleranties de toleranties voor toeslagen.

**Workflow**

-   Configureer op de pagina Leveranciersworkflows de workflows voor journaalgoedkeuringen en inkoopopdrachten.

**Redenen**

-   Configureer op de pagina Leveranciersredenen de redencodes.

**Toeslagen**

-   Configureer op de pagina Toeslagcode de codes voor de toeslagen die in inkooporders worden gebruikt.
-   Maak en beheer op de pagina Toeslaggroep van leverancier de toeslagengroepen voor leveranciers.
-   Maak en beheer op de pagina Toeslaggroepen van artikel de toeslagengroepen voor artikelen.
-   Definieer op de pagina Automatische toeslagen de toeslagen die automatisch aan orders worden toegewezen.

**Bijkomende artikelen**

-   Maak en beheer op de pagina Bijkomende artikelengroepen - Leverancier de bijkomende artikelengroepen voor leveranciers.
-   Maak en beheer op de pagina Bijkomende artikelengroepen - Voorraad de bijkomende artikelengroepen voor artikelen.

**Verdeling**

-   Maak en beheer op de pagina Leveringsvoorwaarden de voorwaarden voor overdracht van artikelen van de verkoper aan de koper.
-   Maak en beheer op de pagina Leveringsmethoden de transportwijzen die worden gebruikt om artikelen te verzenden van de verkoper naar de koper.
-   Maak en beheer op de pagina Bestemmingscodes de ID's en beschrijvingen van bestemmingen voor levering.

**Formulieren**

-   Maak op de pagina Formuliernotities de standaardtekst die op verschillende pagina's wordt weergegeven.
-   Configureer op de pagina Sorteerparameters voor formulier de sorteervolgorde voor bestelopdrachten, ontvangstlijsten, pakbonnen en facturen.
-   Configureer op de pagina Instelling afdrukbeheer de afdrukbeheerinformatie voor originelen en kopieën van pagina's.

**Betalingen**

-   Configureer en beheer op de pagina Contantkortingen de voorwaarden voor het verkrijgen van contantkortingen. De contantkortingscodes worden gekoppeld aan leveranciers en toegepast op inkooporders.
-   Configureer op de pagina Betalingsschema's de betalingsschema's die worden gebruikt om betalingen in termijnen door leveranciers te beheren.
-   Definieer op de pagina pagina Betalingsdagen de betalingsdagen die worden gebruikt voor de berekening van vervaldatums, en geef hier de betalingsdagen voor een bepaalde dag van de week of maand.
-   Maak en beheer op de pagina Betalingskosten de betalingskosten die zijn gekoppeld aan leveranciers.
-   Maak en beheer op de pagina Betalingsopdracht de betalingsinstructies.

**Statistieken**

-   Configureer op de pagina Ouderdomsperiodedefinities door de gebruiker gedefinieerde intervallen om de verdeling van vervallen posten van leverancierrekeningen te analyseren .
-   Maak op de pagina Bedrijfstak de bedrijfstakcodes (LOB-codes) die aan leveranciers zijn toegewezen.

**1099-belasting**

-   Verifieer op de pagina **1099-velden** de minimumbedragen die moeten worden opgegeven aan de Internal Revenue Service (IRS), op basis van de meest recente IRS-vereisten. Werk ze bij wanneer nodig.

## <a name="optional-setup-for-other-modules"></a>**Optionele configuratie voor andere modules**
**Organisatiebeheer**

-   Configureer op de pagina Nummerreeksen de nummerreeksgroepen voor factuurnummers.
-   Configureer op de volgende pagina's de adresgegevens:
    -   Adresinstelling
    -   NAF-codes
    -   Postcodes importeren

**Grootboek**

-   Configureer op de pagina Financiële dimensies de financiële dimensies.
-   Configureer op de volgende pagina's de belastinginformatie:
    -   Btw-codes
    -   Btw-groepen
    -   Btw-groepen voor artikel
    -   Rekeninggroep
    -   Btw-vrijstellingscodes
    -   Btw-jurisdictie
    -   Btw-dienst
    -   Btw-vereffeningsperioden

**Contanten en bankbeheer**

-   Configureer op de pagina Betalingsdoelcodes de betalingsdoelcodes van de centrale bank.






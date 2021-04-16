---
title: Meerdere ophaal- en bezorgmethodes inschakelen voor klantorders
description: In dit onderwerp wordt de functionaliteit van Microsoft Dynamics 365 Commerce beschreven, waarmee u orders van klanten kunt klaarmaken voor ophalen in een winkel.
author: hhainesms
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: c32ffc8435c05c644bf836bb184400d067269208
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796870"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Meerdere ophaal- en bezorgmethodes inschakelen voor klantorders

[!include [banner](includes/banner.md)]


In Microsoft Dynamics 365 Commerce versie 10.0.16 en hoger kunnen organisaties meerdere leveringsmethoden definiëren die door kopers of verkoopvertegenwoordigers kunnen worden gekozen wanneer ze een order maken die wordt opgehaald in een winkel. Op deze manier kunnen organisaties meerdere afhaalopties aan hun klanten aanbieden. Veel detailhandelaren bieden een klant bijvoorbeeld de keuze voor ophalen in de winkel of bij een afhaalpunt. Commerce ondersteunt de configuratie van deze verschillende ophaalmethodes. Gebruikers kunnen daarvan profiteren wanneer ze klantorders maken in een ondersteund Commerce-kanaal (e-commerce, Call Center of winkel).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Ophaalmethoden configureren en inschakelen

Als u deze functie wilt gebruiken, schakelt u de optie **Ondersteuning voor meerdere ophaalmethodes** in de werkruimte **Functiebeheer** in Commerce Headquarters in. Nadat u de functie hebt ingeschakeld, is aanvullende configuratie vereist.

In Commerce versie 10.0.15 en eerder kunnen organisaties slechts één leveringsmethode definiëren als ophaalmethode. Deze definitie wordt uitgevoerd op de pagina **Commerce-parameters**. Wanneer u in versie 10.0.16 en hoger de functie **Ondersteuning voor meerdere ophaal- en bezorgmethodes** inschakelt, wordt de leveringsmethode die eerder is gedefinieerd als leveringsmethode voor het ophalen van artikelen op de pagina **Commerce-parameters** automatisch gekopieerd naar de nieuwe configuratie voor ophaal- en bezorgmethodes.

![Ophaal- en bezorgmethodes op de pagina Commerce-parameters](media/multiplepickupparameter.png)

Nadat u de functie **Ondersteuning voor meerdere ophaal- en bezorgmethodes** hebt ingeschakeld, kunt u meerdere ophaal- en bezorgmethodes definiëren in het rooster **Ophaalmodus van levering** op het sneltabblad **Leveringsmethoden** op het tabblad **Klantorders** van de pagina **Commerce-parameters**.

De velden **Leveringsmethode uitvoeren** en **Elektronische leveringsmethode** en de optie **Alleen opties voor vervoerdersmethoden weergeven voor verzendorders** zijn naar dit sneltabblad verplaatst.

Voordat u extra leveringsmethoden kunt instellen, moet u leveringsmethoden maken. Voeg op de pagina **Leveringsmethoden** in Commerce Headquarters de leveringsmethoden toe die moeten worden beschouwd als ophaalmethodes. Zorg ervoor dat alle configuraties zijn voltooid. Controleer bijvoorbeeld of de leveringsmethode is gekoppeld aan de desbetreffende kanalen en artikelen. Wanneer u klaar bent, voert u de taak **Leveringsmethoden verwerken** uit om de relaties tussen de leveringsmethode, kanalen en artikelen te maken. Wanneer de uitvoering van de taak is voltooid, opent u de pagina **Distributieplanning** in Commerce Headquarters en voert u de distributietaak **1120** om ervoor te zorgen dat de relevante Commerce-kanaaldatabases worden bijgewerkt met de nieuwe configuratie van de leveringsmethode.

![Voorbeeld van een modus voor leveringsconfiguratie voor een ophaalpunt](media/pickupmodes.png)

Nadat u de extra leveringsmethodes hebt gedefinieerd, voegt u deze toe aan het rooster **Ophaalmodus van levering** op de pagina **Commerce-parameters**. Voer vervolgens de juiste distributietaken uit om de relevante Commerce-kanaaldatabases bij te werken met de configuratiewijziging.

> [!NOTE]
> Afgezien van de bestaande afleveringsmethode die wordt gekopieerd naar het rooster **Ophaalmodus van levering** wanneer u de functie **Ondersteuning voor meerdere ophaalmethodes** inschakelt, moet u voor elke aanvullende modus voor leveringsconfiguraties die u maakt nieuwe leveringsmethoden configureren. Wanneer u leveringsmethoden toevoegt aan het rooster **Ophaalmodus van levering**, wordt door Commerce gecontroleerd of actieve openstaande verkoopregels deze al gebruiken. Als er openstaande verkoopregels worden gevonden, wordt er een fout bericht weergegeven. Leveringsmethoden worden niet beschouwd als leveringsmethoden, totdat alle openstaande verkoopregels die deze gebruiken zijn afgesloten (gefactureerd of geannuleerd).

> [!IMPORTANT]
> Nadat u meer dan één leveringsmethode hebt gedefinieerd op de pagina **Commerce-parameters**, wordt de functie **Ondersteuning voor meerdere ophaalmethodes** verplicht en kan deze niet meer worden uitgeschakeld. Als u de functie moet uitschakelen, verwijdert u alle, behalve één leveringsmethode in het rooster **Ophaalmodus van levering**. Als er slechts één afleveringsmethode is gedefinieerd, wordt de functie niet langer beschouwd als verplicht en kan deze worden uitgeschakeld.

### <a name="e-commerce-site-configurations"></a>Siteconfiguraties voor E-commerce

Wanneer de functie **Ondersteuning voor meerdere ophaalmethodes** is ingeschakeld, tonen de volgende modules op de pagina's van e-commerce de nieuwe leveringsmethodes zoals geconfigureerd:

- Koopvak
- Winkelselectie
- Winkelwagen
- Informatie over ophalen
- Orderbevestiging
- Orderdetails

Er zijn geen extra stappen vereist op e-commercepagina's om de afleveringsmethodes beschikbaar te maken.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Werken met meerdere ophaal- en bezorgmethodes

Wanneer meerdere leveringsmethodes schikbaar zijn voor een kanaal, wordt er een verbeterde ervaring aan klanten geleverd wanneer ze winkelen op producten die worden opgehaald. 

- In e-commercekanalen kunnen kopers elke geldige leveringsmethode selecteren die beschikbaar is. Een detailhandelaar definieert bijvoorbeeld twee leveringsmethodes (in de winkel ophalen of bij een afhaalpunt), die beide zijn geconfigureerd in het rooster **Ophaalmodus van levering** en beide zijn geldig voor het afhandelingskanaal van de order en het product dat een klant momenteel koopt. In dit geval kan de klant de gewenste leveringsmethode voor het ophalen van artikelen selecteren. De geselecteerde ophaalmethode wordt vervolgens de leveringsmethode die is gekoppeld aan de verkooporderregel wanneer de order wordt gemaakt in Commerce Headquarters.

    ![Een optie voor ophalen selecteren in e-commerce](media/pickupecommerce.png)

- Als in winkelkanalen een klantorder voor ophalen wordt gemaakt via de POS-toepassing, wordt de verkooppartner gevraagd om te kiezen uit de beschikbare leveringsmethodes, als deze zijn geconfigureerd. Als er slechts één geldige leveringsmethode beschikbaar is voor het kanaal en het item, wordt de verkooppartner niet gevraagd deze te selecteren. In plaats daarvan wordt de beschikbare leveringsmethode automatisch toegepast op de orderregels.

    ![Een optie voor ophalen selecteren in de POS-toepassing](media/pickuppos.png)

- Wanneer gebruikers in Call Center-kanalen een ophaalorder maken, kunnen ze handmatig een gedefinieerde leveringsmethode selecteren die is gekoppeld aan het Call Center-kanaal. Het systeem valideert vervolgens dat de geselecteerde leveringsmethode kan worden gebruikt wanneer het eraan gekoppelde item wordt besteld. Wanneer een leveringsmethode wordt geselecteerd in Call Center-kanalen, moeten de verkooporderregels worden gekoppeld aan een geldig winkelmagazijn. Als een niet-winkelmagazijn is gedefinieerd op een verkoopregel in het Call Center, kan de leveringsmethode niet worden ingesteld voor die verkoopregel.
- Verkoopmedewerkers kunnen de opdracht **Order intrekken** of **Orderafhandeling** in de POS-toepassing gebruiken om een lijst met orders of orderregels voor ophalen op te vragen. Als een verkoopmedewerker een vooraf gedefinieerde zoekfilter gebruikt om alle orders weer te geven die worden opgenomen in de huidige winkel, worden de query's gewijzigd om ervoor te zorgen dat de zoekresultaten alle orders bevatten die gebruikmaken van een leveringsmethode. POS-gebruikers kunnen ook bestaande filters gebruiken om de lijst met orders te beperken tot een bepaalde leveringsmethode. Ze kunnen bijvoorbeeld alleen orders weergeven voor ophalen bij een afhaalpunt.

    ![Leveringsmethodes die zijn toegepast op een lijst met ingetrokken orders filteren](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Overwegingen voor gedistribueerd orderbeheer

De [DOM-functies (gedistribueerd orderbeheer)](https://docs.microsoft.com/dynamics365/commerce/dom) in Commerce negeren alle verkoopregels die zijn gemarkeerd voor ophalen in een winkel. Deze functies zijn bijgewerkt om ervoor te zorgen dat verkoopregels die zijn gekoppeld aan geconfigureerde leveringsmethoden de DOM-logica omzeilen en niet opnieuw worden toegewezen aan een nieuw leveringsmagazijn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
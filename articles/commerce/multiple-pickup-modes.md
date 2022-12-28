---
title: Meerdere ophaal- en bezorgmethodes inschakelen voor klantorders
description: In dit artikel wordt de functionaliteit van Microsoft Dynamics 365 Commerce beschreven, waarmee u orders van klanten kunt klaarmaken voor ophalen in een winkel.
author: hhainesms
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e4d8883b3dc1c4a0e12bcb00b6441f76d73da92e
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831579"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Meerdere ophaal- en bezorgmethodes inschakelen voor klantorders

[!include [banner](includes/banner.md)]


In Microsoft Dynamics 365 Commerce kunnen organisaties meerdere leveringsmethoden definiëren die door kopers of verkoopvertegenwoordigers kunnen worden gekozen wanneer ze een order maken die wordt opgehaald in een winkel. Op deze manier kunnen organisaties meerdere afhaalopties aan hun klanten aanbieden. Veel detailhandelaren bieden een klant bijvoorbeeld de keuze voor ophalen in de winkel of bij een afhaalpunt. Commerce ondersteunt de configuratie van deze verschillende ophaalmethodes. Gebruikers kunnen daarvan profiteren wanneer ze klantorders maken in een ondersteund Commerce-kanaal (e-commerce, Call Center of winkel).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Ophaalmethoden configureren en inschakelen

De functie **Ondersteuning voor meerdere ophaalmethodes** in de werkruimte **Functiebeheer** in Commerce Headquarters is verplicht gesteld en moet worden ingeschakeld in de omgeving.

Als u eerder een leveringsmethode voor ophalen hebt gedefinieerd op de pagina **Commerce-parameters**, wordt die methode weergegeven in de huidige configuratie voor leveringsmethoden voor ophalen.

![Ophaal- en bezorgmethodes op de pagina Commerce-parameters.](media/multiplepickupparameter.png)

U kunt meerdere ophaalleveringsmethoden definiëren in het raster **Ophaalmodus van levering** via **Commerce-parameters** > tabblad **Klantorders** > sneltabblad **Leveringsmethoden**.  

De velden **Leveringsmethode uitvoeren** en **Elektronische leveringsmethode** en de optie **Alleen opties voor vervoerdersmethoden weergeven voor verzendorders** zijn naar dit sneltabblad verplaatst.

Voordat u extra leveringsmethoden kunt instellen, moet u leveringsmethoden maken. Voeg op de pagina **Leveringsmethoden** in Commerce Headquarters de leveringsmethoden toe die moeten worden beschouwd als ophaalmethodes. Zorg ervoor dat alle configuraties zijn voltooid. Als u bijvoorbeeld ophalen bij een afhaalpunt als leveringsoptie voor uw on line klanten aanbiedt voor bepaalde winkels, moet u hiervoor een nieuwe leveringsmethode maken. U kunt deze leveringsmethode maken en de omschrijving 'ophalen bij afhaalpunt' gebruiken. U wilt er zeker van zijn dat de leveringsmethode 'Ophalen bij afhaalpunt' wordt toegewezen aan alle Commerce-kanalen die dit kunnen aanbieden, waaronder online winkels die deze optie kunnen aanbieden en de afzonderlijke winkelkanalen die deze afhandelingsmethode kunnen aanbieden. Leveringsmethoden moeten ook aan de producten worden gekoppeld. Als er in dit voorbeeld bepaalde producten zijn die niet kunnen worden uitgevoerd met 'ophalen bij afhaalpunt', moet u ervoor zorgen dat die artikelen worden uitgesloten. Wanneer u nieuwe leveringsmethoden hebt toegevoegd, voert u de taak **Leveringsmethoden verwerken** uit om de relaties tussen de leveringsmethode, kanalen en artikelen te maken. Wanneer de taak is voltooid, opent u de pagina **Distributieplanning** in Commerce Headquarters en voert u de distributietaak **1120** uit om ervoor te zorgen dat de relevante Commerce-kanaaldatabases worden bijgewerkt met de configuratie van de nieuwe leveringsmethode.

![Voorbeeld van een modus voor leveringsconfiguratie voor een ophaalpunt.](media/pickupmodes.png)

Nadat u de extra leveringsmethodes hebt gedefinieerd, voegt u deze toe aan het rooster **Ophaalmodus van levering** op de pagina **Commerce-parameters**. Voer vervolgens de juiste distributietaken uit om de relevante Commerce-kanaaldatabases bij te werken met de configuratiewijziging.

> [!NOTE]
> Afgezien van de bestaande afleveringsmethode die wordt gekopieerd naar het rooster **Ophaalmodus van levering** wanneer u de functie **Ondersteuning voor meerdere ophaalmethodes** inschakelt, moet u voor elke aanvullende modus voor leveringsconfiguraties die u maakt nieuwe leveringsmethoden configureren. Wanneer u leveringsmethoden toevoegt aan het rooster **Ophaalmodus van levering**, wordt door Commerce gecontroleerd of actieve openstaande verkoopregels deze al gebruiken. Als er openstaande verkoopregels worden gevonden, wordt er een fout bericht weergegeven. Leveringsmethoden worden niet beschouwd als leveringsmethoden, totdat alle openstaande verkoopregels die deze gebruiken zijn afgesloten (gefactureerd of geannuleerd).


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

    ![Een optie voor ophalen selecteren in e-commerce.](media/pickupecommerce.png)

- Als in winkelkanalen een klantorder voor ophalen wordt gemaakt via de POS-toepassing, wordt de verkooppartner gevraagd om te kiezen uit de beschikbare leveringsmethodes, als deze zijn geconfigureerd. Als er slechts één geldige leveringsmethode beschikbaar is voor het kanaal en het item, wordt de verkooppartner niet gevraagd deze te selecteren. In plaats daarvan wordt de beschikbare leveringsmethode automatisch toegepast op de orderregels.

    ![Een optie voor ophalen selecteren in de POS-toepassing.](media/pickuppos.png)

- Wanneer gebruikers in Call Center-kanalen een ophaalorder maken, kunnen ze handmatig een gedefinieerde leveringsmethode selecteren die is gekoppeld aan het Call Center-kanaal. Het systeem valideert vervolgens dat de geselecteerde leveringsmethode kan worden gebruikt wanneer het eraan gekoppelde item wordt besteld. Wanneer een leveringsmethode wordt geselecteerd in Call Center-kanalen, moeten de verkooporderregels worden gekoppeld aan een geldig winkelmagazijn. Als een niet-winkelmagazijn is gedefinieerd op een verkoopregel in het Call Center, kan de leveringsmethode niet worden ingesteld voor die verkoopregel.
- Verkoopmedewerkers kunnen de opdracht **Order intrekken** of **Orderafhandeling** in de POS-toepassing gebruiken om een lijst met orders of orderregels voor ophalen op te vragen. Als een verkoopmedewerker een vooraf gedefinieerde zoekfilter gebruikt om alle orders weer te geven die worden opgenomen in de huidige winkel, worden de query's gewijzigd om ervoor te zorgen dat de zoekresultaten alle orders bevatten die gebruikmaken van een leveringsmethode. POS-gebruikers kunnen ook bestaande filters gebruiken om de lijst met orders te beperken tot een bepaalde leveringsmethode. Ze kunnen bijvoorbeeld alleen orders weergeven voor ophalen bij een afhaalpunt.

    ![Leveringsmethodes die zijn toegepast op een lijst met ingetrokken orders filteren.](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Overwegingen voor gedistribueerd orderbeheer

De [DOM-functies (gedistribueerd orderbeheer)](./dom.md) in Commerce negeren alle verkoopregels die zijn gemarkeerd voor ophalen in een winkel. Deze functies zijn bijgewerkt om ervoor te zorgen dat verkoopregels die zijn gekoppeld aan geconfigureerde leveringsmethoden de DOM-logica omzeilen en niet opnieuw worden toegewezen aan een nieuw leveringsmagazijn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Problemen met magazijnconfiguratie oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens het configureren van Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814387"
---
# <a name="troubleshoot-warehouse-configuration"></a>Problemen met magazijnconfiguratie oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens het configureren van Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Het volgende foutbericht wordt weergegeven: "De nummerplaat of locatie is niet geldig."

### <a name="issue-description"></a>Probleembeschrijving

Dit foutbericht wordt weergegeven wanneer u een nummerplaat-id of locatie scant.

### <a name="issue-resolution"></a>Probleemoplossing

Controleer of de id van de nummerplaat niet al is gereserveerd. Dit probleem doet zich voor wanneer de waarde die een gebruiker in de mobiele app Magazijnbeheer heeft gescand zowel een geldige locatie als een geldige id voor een nummerplaat is. Dit probleem is echter opgelost in versie 10.0.11.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Het volgende foutbericht wordt weergegeven: "De nummerplaat moet worden opgegeven voor deze locatie."

### <a name="issue-description"></a>Probleembeschrijving

Dit foutbericht wordt weergegeven als u een overboekingsorder maakt met behulp van een magazijn dat is ingeschakeld voor geavanceerd magazijnbeheer (WMS) en vervolgens, als het werk is voltooid, probeert u de zending te bevestigen.

### <a name="issue-resolution"></a>Probleemoplossing

Het veld **Standaardlocatie voor ontvangst** is leeg voor een transitmagazijn van het van-magazijn. U kunt dit probleem oplossen door een standaardlocatie voor ontvangst op te geven in het transitmagazijn. Zorg ervoor dat deze locatie een door nummerplaten beheerde locatie is.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Het volgende foutbericht wordt weergegeven: "U kunt geen werksjabloonregel maken voor Wijziging van voorraadstatus, omdat het werktype niet geldig is. Selecteer een ander werktype."

### <a name="issue-description"></a>Probleembeschrijving

Voor een werksjabloon kunt u *Wijziging van voorraadstatus* niet selecteren in de kolom **Werktype** van de sectie **Werksjabloongegevens**.

### <a name="issue-resolution"></a>Probleemoplossing

Dit is zo ontworpen. Het werktype *Wijziging van voorraadstatus* wordt alleen door systeemprocessen gebruikt. Deze waarde kan niet worden geconfigureerd. Omdat de lijst met werktypen vast ligt als opsomming, kunnen de extra vermeldingen niet worden gefilterd uit de vervolgkeuzelijst **Werktype**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Het volgende foutbericht wordt weergegeven: "De hoeveelheid is niet geldig voor eenheid 1%."

### <a name="issue-description"></a>Probleembeschrijving

De hoeveelheid is niet geldig voor de eenheid *ea* wanneer er orderverzamelingswerk is met meerdere nummerplaten op één locatie.

### <a name="issue-resolution"></a>Probleemoplossing

Controleer of de velden **Volgordegroep-id eenheid** en **Eenheidsomrekeningen** op het vrijgegeven product of de productvariant juist zijn ingesteld.

Het foutbericht is verbeterd in versie 10.0.15 (zie [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Het nieuwe foutbericht is, "De hoeveelheid is niet geldig. Verwacht wordt %1 %2."

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>In de locatie-instructies voor het wegzetwerk van verkooporders, worden met de optie voor meerdere SKU'S niet meerdere acties van een locatie-instructie geëvalueerd.

### <a name="issue-description"></a>Probleembeschrijving

Locatie-instructies van het werkordertype *Verkooporders* en het werktype *Wegzetten* evalueren meerdere acties van een locatie-instructie niet wanneer de optie **Meerdere SKU's** is geselecteerd. Alleen de eerste actie van een locatie-instructie wordt geëvalueerd.

### <a name="issue-resolution"></a>Probleemoplossing

Een nieuwe functie *Alle acties van locatie-instructies voor meerdere SKU's evalueren* is toegevoegd in versie 10.0.15 (zie [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Met deze functie worden alle acties van locatie-instructies voor meerdere SKU's geëvalueerd. Als u deze functie nodig hebt, kunt u deze met [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) inschakelen.

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a>Ik kan de mobiele app Magazijnbeheer niet gebruiken om gedeeltelijke orderverzameling uit te voeren.

### <a name="issue-description"></a>Probleembeschrijving

Voor verkoop- en overboekingsorders kunt u geen artikelen overslaan en gedeeltelijke orderverzameling uitvoeren.

### <a name="issue-resolution"></a>Probleemoplossing

Schakel op de pagina **Menuopties voor mobiel apparaat** voor elke menuopdracht die is ingesteld op het verwerken van verkooporders of overboekingsorders de optie **Splitsing van werk toestaan** op het sneltabblad **Algemeen** in op *Ja*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Hoe kan ik een voorraadstatus wijzigen voor een gedeeltelijke hoeveelheid werk?

### <a name="issue-description"></a>Probleembeschrijving

U wilt een voorraadstatus wijzigen voor een gedeeltelijke hoeveelheid van een batch.

### <a name="issue-resolution"></a>Probleemoplossing

Om werknemers in staat te stellen deze wijziging door te voeren, kunt u een menuopdracht maken voor de mobiele app Magazijnbeheer. Maak (of bewerk) op de pagina **Menuopties voor mobiel apparaat** een menuopdracht met een van de volgende instellingen:

- **Modus:** *werk*
- **Bestaand werk gebruiken:** *Nee*
- **Procedure voor het maken van werk:** *Verplaatsing*
- **Voorraadstatus weergeven:** *Ja*

U kunt desgewenst andere velden op de pagina instellen.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Het dockbeheerprofiel van een locatieprofiel zorgt er niet voor dat voorraadtypen niet worden gemengd.

### <a name="issue-description"></a>Probleembeschrijving

U maakt gebruik van *Beleidsregels voor samenvoegen van zendingen*. U hebt een *dockbeheerprofiel* ingesteld voor een *locatieprofiel*, maar wanneer er werk wordt gemaakt, worden de voorraadtypen gemengd op de laatste locatie.

### <a name="issue-resolution"></a>Probleemoplossing

Voor dockbeheerprofielen moet werk vooraf worden opgesplitst. Met andere woorden, het dockbeheerprofiel verwacht dat een werkkoptekst niet meerdere wegzetlocaties bevat.

Er moet een werkkoptekstopsplitsing worden ingesteld om het mengen van voorraad op een effectieve manier te beheren via het dockbeheerprofiel.

In dit voorbeeld is ons dockbeheerprofiel zo geconfigureerd dat **Voorraadtypen die niet mogen worden gemengd** wordt ingesteld op *Zending-id*. Hiervoor stellen we een werkkoptekstopsplitsing in:

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Selecteer het **Werkordertype** dat u wilt bewerken (bijvoorbeeld *Inkooporders*).
1. Selecteer de werksjabloon die u wilt bewerken.
1. Selecteer **Query bewerken** in het actievenster.
1. Open het tabblad **Sorteren** en voeg een rij toe met de volgende instellingen:
    - **Tabel** - *Tijdelijke werktransacties*
    - **Afgeleide tabel** - *Tijdelijke werktransacties*
    - **Veld** - *Zending-id*
1. Selecteer **OK**.
1. U keert terug naar de pagina **Werksjablonen**. Selecteer **Opsplitsingen voor werkkoptekst** in het actievenster.
1. Selecteer **Bewerken** in het actievenster.
1. Schakel het selectievakje in dat is gekoppeld aan de **veldnaam** *Zending-id*.
1. Selecteer **Opslaan** in het actievenster.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

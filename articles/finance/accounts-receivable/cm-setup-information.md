---
title: Instellingen voor kredietbeheer
description: In dit onderwerp worden de instellingen beschreven die zijn vereist voor kredietbeheer.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9e756b678786d2c5a8c5bb9e890ce988090c09
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753660"
---
# <a name="credit-management-setup"></a>Instellingen voor kredietbeheer 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Kredietbeheerwerkstromen

Ga naar **Crediteringen en aanmaningen \> Instellen \> Kredietbeheerworkflows** om de workflows te definiëren die worden gebruikt om kredietlimietcorrecties te beheren.

- U kunt een workflow maken waarmee u een batch met kredietlimietcorrecties kunt goedkeuren via één goedkeuring.
- U kunt een workflow toevoegen op regelniveau, zodat kredietlimietcorrecties afzonderlijk kunnen worden goedgekeurd.
- U kunt een vrijgaveworkflow maken waarmee blokkeringen automatisch naar een workflowproces worden gerouteerd.

## <a name="blocking-rules"></a>Blokkeringsregels

### <a name="ranking-payment-terms"></a>Betalingstermijnen rangschikken

U kunt een verkooporder blokkeren als de betalingsvoorwaarden op de order niet overeenkomen met de standaard betalingsvoorwaarden voor de klant. Soms zijn de betalingsvoorwaarden echter verschillend, maar niet zo afwijkend dat de order niet hoeft te worden geblokkeerd. U kunt betalingsvoorwaarden rangschikken, zodat sommige dezelfde rang hebben, terwijl andere een hogere of lagere rang hebben.

Als de rangschikking voor betalingsvoorwaarden is geactiveerd en als de betalingsvoorwaarden voor de order een hogere rang hebben dan de standaard betalingsvoorwaarden voor de klant, worden de verkooporders geblokkeerd.

Als u de positie van betalingsvoorwaarden wilt instellen, gaat u naar **Crediteringen en aanmaningen \> Instellen \> Kredietbeheer instellen \>Positie van betalingsvoorwaarden**  

### <a name="ranking-settlement-discounts"></a>Vereffeningskortingen rangschikken

U kunt een verkooporder blokkeren als de contantkorting op de order niet overeenkomt met de standaard contantkorting voor de klant. Soms zijn de contantkortingen echter verschillend, maar niet zo afwijkend dat de order niet hoeft te worden geblokkeerd. U kunt contantkortingen rangschikken, zodat sommige dezelfde rang hebben, terwijl andere een hogere of lagere rang hebben.

Als de rangschikking voor vereffeningskortingen is geactiveerd en als de contantkorting voor de order een hogere rang heeft dan de standaard contantkorting voor de klant, worden de verkooporders geblokkeerd.

Als u de positie van betalingsvoorwaarden wilt instellen, gaat u naar **Crediteringen en aanmaningen \> Instellen \> Kredietbeheer instellen \>Positie van vereffeningskortingen**  

## <a name="reasons"></a>Redenen

Er worden verschillende typen redenen gebruikt in kredietbeheer:

- Blokkeringsredenen geven aan waarom een verkooporder geblokkeerd is.
- Vrijgaveredenen worden toegewezen aan een order wanneer deze wordt vrijgegeven.
- Statusredenen geven aan waarom een rekeningstatus aan een klant is toegewezen.

U kunt redenen instellen op de pagina **Redenen voor kredietbeheer** (**Crediteringen en aanmaningen \> Instellen \> Kredietbeheer instellen \> Redenen voor kredietbeheer**).

1. Selecteer in het veld **Type reden** welk type reden u wenst: **Blokkeren**, **Vrijgeven** of **Status**.
2. Voer in het veld **Reden** een naam voor de reden in.
3. Voer in het veld **Beschrijving** een omschrijving van de redencode in.

## <a name="credit-management-groups"></a>Kredietbeheergroepen

Kredietbeheergroepen worden gebruikt om klanten of groepen klanten te identificeren die dezelfde eigenschappen voor het kredietbeheer hebben. Kredietbeheergroepen kunnen bijvoorbeeld worden gebruikt om de kredietbeheerregels voor blokkering en uitsluiting voor klanten te bepalen.

U kunt kredietbeheergroepen instellen op de pagina **Kredietbeheergroepen** (**Crediteringen en aanmaningen \> Instellen> Kredietbeheer instellen \> Kredietbeheergroepen**).

1. Selecteer **Nieuw** om een regel te maken.
2. Voer een id voor de groep in. De id kan maximaal 10 tekens bevatten.
3. Voer in het veld **Beschrijving** een naam voor de groep in. De naam kan maximaal 60 tekens bevatten.

De kredietbeheergroep wordt toegewezen aan een klant op het sneltabblad **Crediteringen en aanmaningen** van de pagina **Alle klanten** (**Klanten \> Klanten \> Alle klanten**).

## <a name="account-statuses"></a>Rekeningstatussen

U kunt rekeningstatussen maken om de kredietpositie van een klantrekening te identificeren. U kunt een status en het effect ervan voor de processen facturering en levering definiëren. Rekeningstatussen kunnen ook worden gebruikt om blokkeringsregels voor een klant te bepalen.

U kunt rekeningstatussen maken op de pagina **Rekeningstatussen** (**Crediteringen en aanmaningen \> Instellen > Kredietbeheer instellen \> Rekeningstatussen**).

1. Voeg een rekeningstatus toe en voer een omschrijving in voor de kredietpositie van een klant. Gebruik bijvoorbeeld **Normaal** om aan te geven dat een klant een goede positie heeft en dat openstaande orders standaard worden verwerkt via standaard kredietbeheer.
2. Selecteer in de velden **Facturering** en **Geblokkeerde levering** het type blokkering voor klanten die deze rekeningstatus hebben. U kunt alle verwerking, alleen factuurverwerking of geen verwerking blokkeren wanneer de kredietlimietregels worden toegepast.

## <a name="scoring-groups"></a>Scoregroepen

U kunt scoregroepen instellen om risicofactoren te definiëren en de criteria die worden gebruikt om ze te meten. Wanneer informatie over een klant wordt toegepast op een scoregroep, wordt voor elke risicofactor een score berekend en gebruikt om de klant in een risicogroep te plaatsen. De risicogroep kan worden gebruikt om kredietwaardigheid te identificeren en automatische kredietlimieten te berekenen.

U kunt scoregroepen maken op de pagina **Scoregroepen** (**Crediteringen en aanmaningen \> Instellen \> Kredietbeheer instellen \> Risico \> Scoregroepen**).

1. Maak een scoregroep en voer een naam in.
2. Voer een omschrijving in om de scoregroep nader te beschrijven.
3. Selecteer een groepstype. Er zijn acht vooraf gedefinieerde typen. U kunt ook **Door de gebruiker gedefinieerd** g selecteren om een groepstype te definiëren dat beter geschikt is voor uw organisatie.
4. Selecteer een scoretype om te definiëren hoe de scoregroep de risicoscore berekent. De volgende opties zijn beschikbaar:

    - **Bereik**: gebruik deze optie om een reeks waarden te definiëren die moeten worden gebruikt om een score te berekenen.
    - **Door de gebruiker gedefinieerd**: gebruik deze optie om handmatig een lijst met waarden te definiëren die voor de score moeten worden gebruikt.

5. Als u **Bereik** hebt geselecteerd als het scoretype, voegt u regels toe om het waardenbereik en de bijbehorende scores te definiëren.

    1. Geef in het veld **Beginwaarde** de laagste waarde in het bereik op.
    2. Geef in het veld **Eindwaarde** de hoogste waarde in het bereik op.
    3. Voer in het veld **Score** de score in die moet worden toegewezen wanneer de opgegeven waarde zich binnen het "Begin"/"Eind"bereik bevindt.

    Als u **Door de gebruiker gedefinieerd** hebt geselecteerd als het scoretype, voegt u regels toe om de door de gebruiker gedefinieerde waarden en de bijbehorende scores te definiëren.

    1. Voer in het veld **Waarde** de door de gebruiker gedefinieerde waarde in die bij de klantgegevens te vinden is.
    2. Voer in het veld **Score** de score in die moet worden toegewezen wanneer de opgegeven waarde zich binnen het "Begin"/"Eind"bereik bevindt.

## <a name="risk-classification"></a>Risicoclassificatie

U kunt risicobeoordelingen definiëren die aan klanten kunnen worden toegewezen op basis van hun risicoscore. Een risicoscore wordt berekend door klantgegevens te vergelijken met de verschillende scoregroepen. De scores worden opgeteld en de totale score wordt vergeleken met de waarden in de instellingen van de risicogroep om de risicogroep te identificeren waartoe de klant behoort. De score van de risicogroep wordt vervolgens gebruikt voor het definiëren van blokkerings- en uitsluitingsregels voor kredietbeheer voor de klant.

U kunt risicogroepen instellen op de pagina **Risicobeoordelingen** (**Crediteringen en aanmaningen \> Instellen \> Kredietbeheer instellen \> Risico \> Risicoclassificatie**).

1. Voer een risico groep-id in.
2. Voer een omschrijving in om de risicogroep nader te beschrijven.
3. Voer reeks scores in die wordt gebruikt om te bepalen welke klanten tot de risicogroep behoren.
4. Selecteer een risicogroepsindicator om het symbool op te geven dat de risicogroep vertegenwoordigt.

## <a name="guaranteeinsurance-types"></a>Typen garantie/verzekering

U kunt garantie- en verzekeringstypen instellen op de pagina **Typen garantie/verzekering** (**Crediteringen en aanmaningen \> Instellen \> Kredietbeheer instellen \> Garantie/verzekering \> Typen garantie/verzekering**).

1. Voer een garantie- of verzekeringstype in dat de naam van de borg- of verzekeringsmakelaar aangeeft.
2. Voer een omschrijving in om de borg-/verzekeringsmakelaar te beschrijven.

## <a name="coverage-types"></a>Dekkingstypen

Dekkingstypen kunnen worden gebruikt om verzekeringspolissen verder te classificeren. Ze kunnen niet met garanties worden gebruikt.

U kunt dekkingstypen toevoegen op de pagina **Dekkingstypen** (**Crediteringen en aanmaningen \> Instellen \> Kredietbeheer instellen \> Garantie/verzekering instellen \> Dekkingstypen**).

1. Voer een dekkingstype in waarmee wordt aangegeven welk dekkingstype moet worden toegevoegd als verzekering of garantie.
2. Voer een omschrijving in om het dekkingstype te beschrijven.

## <a name="automatic-credit-limits"></a>Automatische kredietlimieten

U kunt criteria voor automatische kredietlimieten maken op de pagina **Automatische kredietlimieten** (**Crediteringen en aanmaningen \> Instellen \> Kredietbeheer instellen \> Risico \> Automatische kredietlimieten**).

1. Selecteer een risicogroep waaraan de automatische kredietlimiet moet worden toegewezen.
2. Selecteer de valuta voor de automatische kredietlimiet. U kunt meerdere automatische kredietlimieten maken in verschillende valuta's voor dezelfde risicogroep.
3. Voer het opbrengstbedrag in dat de maximale bedrijfsopbrengst vertegenwoordigt die kan worden gebruikt voor deze automatische kredietlimiet. Wanneer kredietlimieten worden gemaakt, wordt het opbrengstbedrag vergeleken met een opbrengstwaarde van de pagina **Financiën** (**Klanten \> Alle klanten \> Een klant selecteren \> Algemeen \> Statistieken \> Financieel**). Het systeem gebruikt de meest recente waarde in de sectie **Overzicht**.

Volg deze stappen om regels toe te voegen die de kredietlimiet aangeven die wordt gegenereerd op basis van de geselecteerde criteria.

1. Selecteer de scoregroep waarmee de klantgegevens worden gedefinieerd die moeten worden gebruikt om de kredietlimiet te berekenen.
2. Selecteer de vergelijkingsoperator waarmee wordt gedefinieerd hoe de informatie over de scoregroep moet worden geëvalueerd.
3. Voer de waarde in die moet worden vergeleken met de waarde die is opgegeven voor de scoregroep.
4. Voer de kredietlimiet in die moet worden toegewezen als de klantgegevens overeenkomen met de waarde die is opgegeven voor de scoregroep. U kunt bijvoorbeeld een automatische kredietlimiet maken voor de scoregroep **Laag**. Als het aantal jaren in bedrijf een van de scoregroepen is, kunt u één regel definiëren die een kredietlimiet van 100.000 toewijst als de klant vijf jaar in bedrijf is en een andere regel die een kredietlimiet van 200.000 limiet toewijst als de klant 10 jaar in bedrijf is.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

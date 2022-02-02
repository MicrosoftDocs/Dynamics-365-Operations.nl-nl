---
title: Overzicht van Elektronische handtekeningen
description: Dit artikel bevat een overzicht van elektronische handtekeningen en een beschrijving van het gebruik.
author: maertenm
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.custom:
- "13611"
- intro-internal
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9f80ecef043a697d288fed99e3118e268d4f993
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983637"
---
# <a name="electronic-signatures-overview"></a>Overzicht van Elektronische handtekeningen

[!include [banner](../includes/banner.md)]

Dit artikel bevat een overzicht van elektronische handtekeningen en een beschrijving van het gebruik.

## <a name="what-is-an-electronic-signature"></a>Wat is een elektronische handtekening?

Met een elektronische handtekening wordt de identiteit bevestigd van een persoon die een computerproces wil starten of goedkeuren. In bepaalde bedrijfstakken is een elektronische handtekening in dezelfde mate juridisch bindend als een handtekening die met de hand is geschreven.

Elektronische handtekeningen zijn volgens de wetgeving vereist voor verschillende gereguleerde bedrijfstakken, zoals farmaceutische bedrijven, voedsel en drank, de ruimtevaartindustrie en defensie. Daarnaast zijn deze handtekeningen vereist voor de naleving van de wetgeving in 21 CFR Part 11 die is uitgevaardigd door de Food and Drug Administration (FDA) in de Verenigde Staten.

> [!NOTE]
> Een elektronische handtekening is niet hetzelfde als een digitale handtekening. Een elektronische handtekening is simpelweg een vervanging van een handtekening die met de hand is geschreven, terwijl een digitale handtekening is voorzien van extra beveiligingsmaatregelen. Met een digitale handtekening kan worden aangegeven of met de gegevens is geknoeid door een andere gebruiker of een ander proces. Een digitale handtekening kan ook worden geverifieerd en deze verificatie kan niet worden weerlegd door de eigenaar van het certificaat dat is gebruikt voor het ondertekenen van de gegevens. Zoals hierna wordt beschreven, bevatten elektronische handtekeningen ingebouwde functionaliteit voor digitale handtekeningen.

## <a name="electronic-signatures"></a>Elektronische handtekeningen

U kunt elektronische handtekeningen gebruiken voor belangrijke bedrijfsprocessen. Een aantal processen bevat ingebouwde functies voor elektronische handtekeningen. Daarnaast kunt u aangepaste vereisten voor handtekeningen maken voor databasetabellen en -velden.

Elektronische handtekeningen bevatten ingebouwde functionaliteit voor digitale handtekeningen. Elke gebruiker die documenten ondertekent, moet een geldig cryptografisch certificaat ophalen. Wanneer een document wordt ondertekend, wordt de persoonlijke sleutel die aan dit certificaat is gekoppeld, gevalideerd. Elektronische-handtekeninggegevens worden geregistreerd in een logboek voor de benodigde informatie voor een audittrail. Zie [Elektronische handtekeningen instellen](tasks/set-up-electronic-signatures.md) voor meer informatie over het instellen van elektronische handtekeningen.

## <a name="users-who-require-access-to-electronic-signatures"></a>Gebruikers die toegang tot elektronische handtekeningen nodig hebben

Drie soorten gebruikers vereisen doorgaans beveiligde toegang tot elektronische handtekeningen: elektronische handtekeningbeheerders ondertekenaars en auditors van elektronische handtekeningen.

### <a name="electronic-signature-administrator"></a>Elektronische handtekeningenbeheerder

De beheerder van elektronische handtekeningen stelt handtekeningvereisten, algemene parameters en fiatteurs in en ontvangt waarschuwingen wanneer de handtekeningverificatie is mislukt. Standaard is een gebruiker die toebehoort aan de beveiligingsrol **IT-manager** gemachtigd om elektronische handtekeningen te beheren.

### <a name="signer"></a>Ondertekenaar

Een ondertekenaar geeft elektronische handtekeningen op voor documenten en processen waarvoor handtekeningen zijn vereist. Standaard is een gebruiker die toebehoort aan de rol **Systeemgebruiker** gemachtigd om documenten elektronisch te tekenen.

> [!NOTE]
> De ondertekenaar heeft mogelijk extra machtigingen nodig voordat toegang wordt verleend tot gegevens die zijn gerelateerd aan het document of proces dat wordt ondertekend. Gebruikers die gegevens wijzigen en deze wijzigingen vervolgens moeten ondertekenen, moeten machtigingen hebben om de gegevens te wijzigen. Een gebruiker die namens een andere gebruiker tekent, vereist mogelijk geen toegang tot de gegevens. Een voorbeeld van dit type gebruiker is een toezichthouder die de wijzigingen van de werknemer ondertekent.

### <a name="electronic-signature-auditor"></a>Auditor voor elektronische handtekeningen

De auditor van elektronische handtekeningen controleert het databaselogboek en handtekeningcontrolelogboek dat beschikbaar is vanuit het databaselogboek. Standaard is een gebruiker die toebehoort aan de beveiligingsrol **IT-manager** gemachtigd om elektronische handtekeningen te controleren.

Als u een andere rol dan **IT-manager** gebruikt, zorg er dan voor dat aan de rol de volgende bevoegdheden zijn toegewezen:

- Fouten in elektronische handtekening weergeven
- Databaselogboek weergeven

## <a name="signing-documents-electronically"></a>Documenten elektronisch ondertekenen

### <a name="get-a-certificate"></a>Een certificaat ophalen

Voordat u documenten elektronisch kunt ondertekenen, moet u een certificaat aanvragen.

> [!NOTE]
> In Microsoft SQL Server worden functies gebruikt om certificaten te maken en elektronisch ondertekenen in te schakelen. Er is geen extra infrastructuur voor certificaten of openbare sleutels (PKI) vereist.

Wanneer u een certificaat aanvraagt, worden een openbare en persoonlijke sleutel voor u gemaakt. De persoonlijke sleutel wordt gecodeerd met een wachtwoord dat alleen u kent. Wanneer u een document elektronisch ondertekent, wordt uw identiteit geverifieerd wanneer u het wachtwoord invoert.

U kunt een certificaat aanvragen door op de pagina **Opties**, op het tabblad **Rekeningen**, op **Certificaat ophalen** te klikken.

U moet het wachtwoord dat u gebruikt voor het ondertekenen invoeren en bevestigen. Met het wachtwoord wordt uw persoonlijke sleutel beveiligd en wordt het gebruik van uw certificaat geautoriseerd. Dit wachtwoord wordt niet opgeslagen in de database en is niet beschikbaar voor anderen, inclusief de beheerder.

Als u het wachtwoord vergeet dat aan uw certificaat is gekoppeld, moet u het certificaat opnieuw instellen. Als u het certificaat opnieuw instelt, heeft dit geen invloed op documenten die u hebt ondertekend met het vorige certificaat. U kunt het certificaat opnieuw instellen door op de pagina **Opties** op **Certificaat opnieuw instellen** te klikken.

### <a name="sign-a-document-electronically"></a>Een document elektronisch ondertekenen

De pagina **Document ondertekenen** wordt weergegeven wanneer u een wijziging aanbrengt waarvoor een elektronische handtekening is vereist.

1. Klik op de pagina **Document ondertekenen** op het tabblad **Document** om de wijzigingen in het document te bekijken.
2. Selecteer een redencode op het tabblad **Handtekening**.
3. Voer een opmerking in als een opmerking is vereist.
4. Als uw gebruikers-id niet wordt weergegeven in het veld **Ondertekenaar**, selecteert u deze in de lijst.
5. Voer uw locatie in, als deze informatie is vereist.
6. Klik tot slot op **OK**.

### <a name="sign-for-another-users-changes"></a>Tekenen voor de wijzigingen van een andere gebruiker

Soms wilt u wellicht dat een gebruiker zijn handtekening zet onder de wijzigingen van een andere gebruiker. Zo zou bijvoorbeeld supervisor mogelijk verplicht kunnen zijn zijn handtekening te plaatsen onder wijzigingen die een werknemer aanbrengt in een stuklijst. Met deze procedure kunt u een gebruiker toewijzen als ondertekenaar voor een andere gebruiker.

> [!NOTE]
> Wanneer een gebruiker wijzigingen van een andere gebruiker ondertekent, moet de handtekening worden opgegeven op het werkstation van de gebruiker die de wijziging heeft aangebracht. De gebruiker kan de wijziging pas opslaan wanneer de handtekening is opgegeven.

Volg deze stappen om fiatteurs aan te wijzen.

1. Klik op de pagina **Opties** op het tabblad **Rekeningen** op **Fiatteur aangeven**.
2. Selecteer in het veld **Gebruikers-ID fiatteur** de ID van de gebruiker die moet ondertekenen voor de wijzigingen van een andere gebruiker.
3. Selecteer in het veld **Ondertekenen voor gebruikers-ID** de gebruiker voor wie de wijzigingen moeten worden ondertekend.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
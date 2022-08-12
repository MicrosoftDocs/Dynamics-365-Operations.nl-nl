---
title: Gegevens van Prospect naar contant geld vanuit Data Integrator migreren naar twee keer wegschrijven
description: In dit artikel wordt beschreven hoe u gegevens van Prospects naar contant geld vanuit Data Integrator kunt migreren naar twee keer wegschrijven
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 91cc0e59405bc085e09f01f05ef02e4a0260481e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111889"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Gegevens van Prospect naar contant geld vanuit Data Integrator migreren naar twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

De oplossing Van prospect naar contant geld die beschikbaar is voor Data Integrator, is niet compatibel met Twee keer wegschrijven. De reden hiervoor is de index msdynce_AccountNumber in de rekeningtabel die als onderdeel van de oplossing Van prospect naar contant geld is meegeleverd. Als deze index aanwezig is, kunt u niet hetzelfde klantrekeningnummer in twee verschillende rechtspersonen maken. U kunt ervoor kiezen om opnieuw te beginnen met twee keer wegschrijven door de gegevens van de oplossing Van prospect naar contant geld te migreren van Data Integrator naar twee keer wegschrijven of u kunt de laatste 'slapende' versie van de oplossing Van prospect naar contant geld installeren. In dit artikel worden beide benaderingen beschreven.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>De laatste 'slapende' versie van de oplossing Van prospect naar contant geld van Data Integrator installeren

**P2C versie 15.0.0.2** wordt beschouwd als de laatste 'slapende' versie van de oplossing Van prospect naar contant geld van Data Integrator. U kunt het downloaden via [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

U moet het handmatig installeren. Na de installatie blijft alles exact hetzelfde, behalve dat de index msdynce_AccountNumber is verwijderd.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Stappen om gegevens van Prospect naar contant geld vanuit Data Integrator te migreren naar Twee keer wegschrijven

Voer de volgende stappen uit om gegevens van Prospects naar contant geld vanuit Data Integrator te migreren naar twee keer wegschrijven.

1. Voer de Data Integrator-taken voor Prospect naar contant geld uit om één laatste volledige synchronisatie uit te voeren. Op deze manier zorgt u ervoor dat beide systemen (apps voor financiën en bedrijfsactiviteiten en Customer Engagement-apps) alle gegevens bevatten.
2. Als u potentieel gegevensverlies wilt voorkomen, exporteert u gegevens van Prospect naar contant geld van Microsoft Dynamics 365 Sales naar een Excel-bestand of een CSV-bestand (Comma Separated Values). Gegevens exporteren vanuit de volgende entiteiten:

    - [Rekening](#account-table)
    - [Contact](#contact-table)
    - [Factuur](#invoice-table)
    - Factuurproducten
    - [Order](#order-table)
    - [Orderproducten](#order-products-table)
    - [Producten](#products-table)
    - [Offerte](#quote-and-quote-product-tables)
    - [Offerteproducten](#quote-and-quote-product-tables)

3. Verwijder de oplossing Prospect naar contant geld vanuit de Sales-omgeving. Met deze stap verwijdert u de kolommen en bijbehorende gegevens die via de oplossing Prospect naar contant geld zijn ingevoerd.
4. Installeer de oplossing voor twee keer wegschrijven.
5. Maak een verbinding voor twee keer wegschrijven tussen de app voor financiën en bedrijfsactiviteiten en de Customer Engagement-app voor een of meer rechtspersonen.
6. Schakel tabeltoewijzingen voor twee keer wegschrijven in en voer de initiële synchronisatie voor de vereiste verwijzingsgegevens uit. (Zie voor meer informatie [Overwegingen voor initiële synchronisatie](initial-sync-guidance.md).) Voorbeelden van vereiste gegevens zijn klantgroepen, betalingstermijnen en betalingsschema's. Schakel de toewijzingen voor twee keer wegschrijven niet in voor tabellen die initialisatie vereisen, zoals de tabellen voor rekening, offerte, offerteregel, order en orderregel.
7. Ga in de Customer Engagement-app naar **Geavanceerde instellingen \> Systeeminstellingen \> Gegevensbeheer \> Dubbele detectieregels** en schakel alle regels uit.
8. Initialiseer de tabellen die worden weergegeven in stap 2. Zie de overige gedeelten van dit artikel voor instructies.
9. Open de app voor financiën en bedrijfsactiviteiten en schakel de tabeltoewijzingen in, zoals de tabeltoewijzingen voor rekening, offerte, offerteregel, order en orderregel. Voer vervolgens de initiële synchronisatie uit. (Zie voor meer informatie [Overwegingen voor initiële synchronisatie](initial-sync-guidance.md).) Met dit proces worden extra gegevens uit de app voor financiën en bedrijfsactiviteiten gesynchroniseerd, zoals verwerkingsstatus, verzend- en factuuradressen, locaties en magazijnen.

## <a name="account-table"></a>Rekeningtabel

1. Voer in de kolom **Bedrijf** de bedrijfsnaam in, zoals **USMF**.
2. Voer in de kolom **Relatietype** **Klant** in als een statische waarde. Het kan zijn dat u niet elke rekeningrecord wilt classificeren als een klant in uw bedrijfslogica.
3. Voer in de kolom **Klantgroep-id** het nummer van de klantgroep uit de app voor financiën en bedrijfsactiviteiten in. De standaardwaarde van de oplossing Prospect naar contant geld is **10**.
4. Als u de oplossing Prospect naar contant geld gebruikt zonder een aanpassing van **Rekeningnummer**, voert u een waarde voor **Rekeningnummer** in de kolom **Partijnummer** in. Als er aanpassingen zijn en u weet het partijnummer niet, haalt u deze informatie op uit de app voor financiën en bedrijfsactiviteiten.

## <a name="contact-table"></a>Contactpersoontabel

1. Voer in de kolom **Bedrijf** de bedrijfsnaam in, zoals **USMF**.
2. Stel de volgende kolommen in op basis van de waarde **IsActiveCustomer** in het CSV-bestand:

    - Als **IsActiveCustomer** is ingesteld op **Ja** in het CSV-bestand, stelt u de kolom **Verkoopbaar** in op **Ja**. Voer in de kolom **Klantgroep-id** het nummer van de klantgroep uit de app voor financiën en bedrijfsactiviteiten in. De standaardwaarde van de oplossing Prospect naar contant geld is **10**.
    - Als **IsActiveCustomer** is ingesteld op **Nee** in het CSV-bestand, stelt u de kolom **Verkoopbaar** in op **Nee** en stelt u de kolom **Contactpersoon voor** in op **Klant**.

3. Stel de volgende kolommen in als u de oplossing Prospect naar contant geld gebruikt zonder een aanpassing van **Contactnummer**:

    - Migreer het contactnummer vanuit het CSV-bestand (**msdynce\_contactnumber**) naar het contactnummer in de tabel **Contactpersoon** (**msdyn\_contactnumber**).
    - Gebruik waarden uit de tabel **Contactnummer** in de kolom **Partijnummer**.
    - Gebruik waarden uit de tabel **Contactnummer** in de kolom **Rekeningnummer/Contactpersoon-id**.

## <a name="invoice-table"></a>Factuurtabel

Omdat gegevens uit de tabel **Factuur** zijn ontworpen om op één manier te stromen vanuit de app voor financiën en bedrijfsactiviteiten naar de Customer Engagement-app, is initialisatie niet vereist. Voer de initiële synchronisatie uit om alle vereiste gegevens van de app voor financiën en bedrijfsactiviteiten te migreren naar de Customer Engagement-app. Zie [Overwegingen voor initiële synchronisatie](initial-sync-guidance.md) voor meer informatie.

## <a name="order-table"></a>Ordertabel

1. Voer in de kolom **Bedrijf** de bedrijfsnaam in, zoals **USMF**.
2. Kopieer de waarde van de kolom **Order-id** in het CSV-bestand naar de kolom **Verkoopordernummer**.
3. Kopieer de waarde van de kolom **Klant** in het CSV-bestand naar de kolom **Factuurklantnummer**.
4. Kopieer de waarde van de kolom **Land/regio van verzending** in het CSV-bestand naar de **Land/regio van verzending**. Voorbeelden van deze waarde zijn **VS** en **Verenigde Staten**.
5. Stel de kolom **Gevraagde ontvangstdatum** in. Als u geen ontvangstdatum gebruikt, gebruikt u de kolommen **Gevraagde leveringsdatum**, **Datum vervuld** en **Datum Ingediend** in het CSV-bestand. Een voorbeeld van deze waarde is **2020-03-27T00:00:00Z**.
6. Stel de kolom **Taal** in. Een voorbeeld van deze waarde is **en-us**.
7. Stel de kolom **Ordertype** in met behulp van de kolom **Op basis van artikel**.

## <a name="order-products-table"></a>Orderproducttabel

- Voer in de kolom **Bedrijf** de bedrijfsnaam in, zoals **USMF**.

## <a name="products-table"></a>Producttabel

Omdat gegevens uit de tabel **Producten** zijn ontworpen om op één manier te stromen vanuit de app voor financiën en bedrijfsactiviteiten naar de Customer Engagement-app, is initialisatie niet vereist. Voer de initiële synchronisatie uit om alle vereiste gegevens van de app voor financiën en bedrijfsactiviteiten te migreren naar de Customer Engagement-app. Zie [Overwegingen voor initiële synchronisatie](initial-sync-guidance.md) voor meer informatie.

## <a name="quote-and-quote-product-tables"></a>Offerte- en offerteproducttabellen

Volg voor de tabel **Offerte** de instructies in de sectie [Ordertabel](#order-table) eerder in dit artikel. Volg voor de tabel **Offerteproduct** de instructies in de sectie [Orderproducttabel](#order-products-table) eerder in dit onderwerp.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


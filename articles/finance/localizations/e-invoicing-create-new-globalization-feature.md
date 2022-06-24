---
title: Een globaliseringsfunctie maken
description: In dit artikel wordt uitgelegd hoe u een globaliseringsfunctie maakt.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c622b350f79d36b8fda12598ceae57ee9c7095e9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889825"
---
# <a name="create-a-globalization-feature"></a>Een globaliseringsfunctie maken

[!include [banner](../includes/banner.md)]

U kunt een functie voor elektronische facturering helemaal opnieuw maken of u kunt deze baseren op een bestaande functie. Wanneer u een functie opnieuw maakt, moet u handmatig de ER-configuraties en andere onderdelen toevoegen, zoals de instellingen van de functie en de toepassing. Wanneer u een functie maakt die op een bestaande functie is gebaseerd, neemt de nieuwe functie alle configuraties en parameters van de basisfunctie over. U kunt bekijken wat er van de basisfunctie naar de nieuwe functie is gekopieerd.

## <a name="create-a-feature-from-scratch"></a>Een functie opnieuw maken

In deze sectie wordt uitgelegd hoe u een functie voor elektronische facturering maakt wanneer er in de Algemene opslagplaats standaard geen globaliseringsfunctie beschikbaar is voor uw bedrijfsscenario.

Voer de volgende stappen uit om een functie voor elektronische facturering te maken.

1. Meld u aan bij uw RCS-account (Regulatory Configuration Service).
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
3. Selecteer **Toevoegen** en selecteer vervolgens in het dialoogvenster met vervolgkeuzemenu de optie **Nieuwe functie**.
4. Voer een naam en omschrijving voor de functie voor elektronische facturering in.
5. Selecteer **Functie maken**. De eerste versie van de nieuwe functie verschijnt aan de rechterkant van de pagina en heeft de status **Concept**.

    Vervolgens moet u ER-configuraties en functie-instellingen toevoegen. Voordat u nieuwe of bestaande ER-indelingsconfiguraties toevoegt, moet u controleren of deze aanwezig zijn in uw lokale RCS-opslagplaats.

6. Selecteer de functie voor elektronische facturering waarmee u werkt.
7. Selecteer **Toevoegen** op het tabblad **Configuraties**.
8. Blader in het raster **Configuraties** naar de indelingsconfiguraties die nodig zijn voor de verwerkingspijplijn (bijvoorbeeld om elektronische factuurbestanden of procesreacties van externe webservices) te genereren.
9. Selecteer **OK**. U kunt de configuraties nu gebruiken in acties van de verwerkingspijplijn. Raadpleeg [Werken met configuraties](e-invoicing-work-configurations.md) voor meer informatie.
10. Als u instellingen voor een elektronische factureringsfunctie wilt toevoegen, maakt u deze op het tabblad **Instellingen** van de pagina **Nieuwe functie**. Raadpleeg [Werken met functie-instellingen](e-invoicing-feature-setup.md) voor meer informatie.
11. Voltooi het instellen en implementeer de functie voor elektronische facturering in de serviceomgeving. Zie [Een globaliseringsfunctie voltooien, publiceren en implementeren](e-invoicing-complete-publish-deploy-globalization-feature.md) voor meer informatie.

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Bestandsindelingsconfiguraties maken die zijn afgeleid van het bestaande factuurmodel

U kunt deze sectie overslaan als u geen ER-configuraties hoeft te maken, maar bestaande versies als basis kunt gebruiken.

In deze procedure maakt u de bestandsindelingsconfiguraties die nodig zijn voor de nieuwe functie voor elektronische facturering die u wilt maken. Maak de configuratie van de bestandsindeling voor elektronische facturen en andere configuraties voor bestandsindelingen die uw nieuwe functie voor elektronische facturering nodig heeft.

1. Meld u aan bij uw RCS-account.
2. Selecteer in het werkgebied **Elektronische rapportage** de tegel **Rapportconfiguraties**.
3. Selecteer **Factuurmodel** of selecteer **Fiscaal model** voor Braziliaanse scenario's.
4. Selecteer **Configuratie maken** en selecteer in het vervolgkeuzemenu de optie **Indeling gebaseerd op gegevensmodel Factuur**.
5. Voer een naam en omschrijving voor de indelingsconfiguratie in.
6. Selecteer het bestandsextensietype in het veld **Type indeling**.
7. Selecteer in het veld **Gegevensmodeldefinitie** de basisstructuur waaraan u de indeling wilt toewijzen. **InvoiceCustomer** wordt bijvoorbeeld gebruikt voor de indelingen van klantfacturen.
8. Selecteer **Configuratie maken**.
9. Selecteer de nieuwe indelingsconfiguratie.
10. Selecteer **Ontwerper** en gebruik de functie Indelingsontwerper om de bestandsindeling zo te configureren dat deze voldoet aan de specificaties van de bestandsindeling.
11. Sluit de pagina.
12. Selecteer op het tabblad **Versies** **Status wijzigen** \> **Voltooid**.
13. Selecteer **Status wijzigen** \> **Delen** om de indelingsconfiguratie naar de algemene opslagplaats te publiceren.

De nieuwe configuraties van de bestandsindeling moeten worden gedeeld met het Microsoft-domein voordat ze kunnen worden gebruikt door de service voor elektronische facturering.

1. Selecteer de indelingsconfiguratie waarmee u werkt. De status van de configuratie moet **Gedeeld** zijn.
2. Selecteer op het tabblad **Versies** **Geavanceerd delen** \> **Algemene opslagplaats**.
3. Selecteer op het tabblad **Gedeeld met** de optie **Organisatie**.
4. Voer in het veld **Parameters** **microsoft.com** in om de indelingsconfiguratie te delen met het Microsoft-domein.
5. Selecteer **OK**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Een functie maken die is gebaseerd op een bestaande functie

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
3. Zorg dat uw actieve configuratieprovider is geselecteerd in het veld **Configuratieprovider**. Op deze manier wordt de nieuwe elektronische factureringsfunctie in de lijst weergegeven nadat deze is gemaakt. Als uw actieve configuratieprovider niet is geselecteerd, wordt de nieuwe functie uit de lijst gefilterd.
4. Selecteer **Toevoegen** en selecteer vervolgens in het dialoogvenster met vervolgkeuzemenu de optie **Op basis van bestaande versie**.
5. Voer een naam en beschrijving voor de functie in.
6. Selecteer in het veld **Basisfunctie** de basisversie van de functie.
7. Selecteer **Functie maken**. De functie wordt gemaakt met de status **Concept**.
8. Controleer de functieonderdelen om te bepalen of er updates nodig zijn:

    - Bekijk de configuraties voor het geval u de ER-indelingen (Elektronische rapportage) en hun binding met indelingstoewijzingen voor de functieversie moet aanpassen.
    - Controleer de instellingen voor het geval u het tabblad **Acties**, **Toepasbaarheidregels** of **Variabelen** voor de functieversie moet aanpassen.

9. Voltooi het instellen en implementeer de functie voor elektronische facturering in de serviceomgeving. Zie [Een globaliseringsfunctie voltooien, publiceren en implementeren](e-invoicing-complete-publish-deploy-globalization-feature.md) voor meer informatie.

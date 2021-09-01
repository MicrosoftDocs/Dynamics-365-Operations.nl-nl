---
title: Een nieuwe functie voor Elektronische facturering maken
description: In dit onderwerp wordt uitgelegd hoe u een nieuwe functie voor elektronische facturering maakt wanneer er geen configureerbare standaardfunctie beschikbaar is voor uw land of regio.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744930"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Een nieuwe functie voor Elektronische facturering maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een nieuwe functie voor elektronische facturering maakt wanneer er geen configureerbare standaardfunctie beschikbaar is voor uw land of regio.

Voer de volgende stappen uit om een nieuwe functie voor elektronische facturering te maken.

1. Maak een nieuwe bestandsindelingsconfiguratie door de geleverde factuurmodelconfiguratie te gebruiken en te profiteren van de bestaande factuurtoewijzing voor de functie die u wilt maken.
2. Voeg de bestandsindelingsconfiguraties aan de configuraties voor de functie voor elektronische facturering toe.
3. Maak de instelling voor de functie voor elektronische facturering.
4. Voltooi de nieuwe functie voor elektronische facturering en publiceer deze naar de algemene opslagplaats voor uw organisatie.
5. Implementeer de nieuwe functie voor elektronische facturering in de serviceomgeving.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Nieuwe bestandsindelingsconfiguraties maken die zijn afgeleid van het bestaande factuurmodel

In deze procedure maakt u de bestandsindelingsconfiguraties die nodig zijn voor de nieuwe functie voor elektronische facturering die u wilt maken. U kunt de configuratie van de bestandsindeling voor elektronische facturen en andere configuraties voor bestandsindelingen maken die uw nieuwe functie voor elektronische facturering wellicht nodig heeft.

Voordat u deze procedure start, moet u zich aanmelden bij uw RCS-account (Regulatory Configuration Service).

1. Selecteer in Microsoft Dynamics 365 Finance in het werkgebied **Elektronische rapportage** de optie **Opslagplaatsen** voor de configuratieprovider **Microsoft**.
2. Selecteer **Algemeen**, selecteer **Openen** en selecteer vervolgens in het linkerdeelvenster de configuratie **Factuurmodel**.

    > [!IMPORTANT]
    > Selecteer voor Brazilië in plaats daarvan de modelconfiguratie **Fiscale documenten**.

3. Selecteer **Importeren** op het tabblad **Configuraties**.
4. Sluit de pagina.
5. Sluit de pagina.
6. Selecteer de tegel **Rapportageconfiguraties** en selecteer vervolgens het factuurmodel dat u hebt geïmporteerd.
7. Selecteer **Configuratie maken** en selecteer vervolgens **Indeling op basis van factuurcontextmodel**.
8. Voer een naam en omschrijving voor de indelingsconfiguratie in.
9. Selecteer het bestandsextensietype in het veld **Type indeling**.
10. Selecteer **Configuratie maken** en selecteer vervolgens de indelingsconfiguratie die u hebt gemaakt.
11. Selecteer **Ontwerper** en gebruik de functie Indelingsontwerper om de bestandsindeling zo te configureren dat deze voldoet aan de specificaties van de bestandsindeling.
12. Sluit de pagina.
13. Selecteer op het tabblad **Versies** **Status wijzigen** \> **Voltooid**.
14. Selecteer **Status wijzigen** \> **Delen** om de indelingsconfiguratie naar de algemene opslagplaats te publiceren.

De nieuwe configuratie van de bestandsindeling moet worden gedeeld met het Microsoft-domein voordat de configuratie kan worden gebruikt door de service voor elektronische facturering.

1. Selecteer de indelingsconfiguratie waarmee u werkt. De status van de configuratie moet **Gedeeld** zijn.
2. Selecteer op het tabblad **Versies** **Geavanceerd delen** \> **Algemene opslagplaats**.
3. Selecteer op het tabblad **Gedeeld met** de optie **Organisatie**.
4. Voer in het veld **Parameters** **Microsoft.com** in om de indelingsconfiguratie te delen met het Microsoft-domein.
5. Selecteer **OK**.

## <a name="create-the-new-electronic-invoicing-feature"></a>De nieuwe functie voor elektronische facturering maken

1. Selecteer in RCS in het werkgebied **Globalisatiefuncties** in de sectie **Functies** de tegel **Elektronische facturering**.
2. Selecteer **Toevoegen** en vervolgens **Nieuwe functie**.
3. Voer een naam en omschrijving voor de functie voor elektronische facturering in.
4. Selecteer **Functie maken**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Configuraties voor de functie voor elektronische facturering toevoegen

1. Selecteer de functie voor elektronische facturering waarmee u werkt.
2. Selecteer **Toevoegen** op het tabblad **Configuraties**.
3. In het raster **Configuraties** bladert u naar en selecteert u de bestandsindelingconfiguraties die voor de functie voor elektronische facturering zijn vereist om het bestand voor elektronische facturen te genereren.
4. Selecteer **OK**.

## <a name="add-electronic-invoicing-feature-setups"></a>Instellingen van de functie voor elektronische facturering toevoegen

1. Selecteer **Toevoegen** op het tabblad **Instellingen** en selecteer **Aangepaste instellingen**.
2. Voer een naam en omschrijving voor de functie-instelling in.
3. Selecteer **Verwerkingspijplijn** in het veld **Instellingstype**.
4. Selecteer **Maken**.
5. Selecteer de instelling waaraan u werkt en selecteer **Bewerken**.
6. Selecteer **Nieuw** op het tabblad **Verwerkingspijplijn** om een pijplijnactie toe te voegen. Zie [Acties](e-invoicing-configuration-rcs.md#actions) voor meer informatie over pijplijnen.
7. Selecteer **Nieuw** op het tabblad **Toepasbaarheidsregels** om de toepasbaarheidsregelclausules toe te voegen. Zie [Toepasbaarheidsregels](e-invoicing-configuration-rcs.md#applicability-rules) voor meer informatie over toepasbaarheidsregels.
8. Selecteer **Nieuw** op het tabblad **Variabelen** om indien nodig variabelen toe te voegen.
9. Selecteer **Opslaan** en selecteer vervolgens **Valideren** om de consistentie van de configuratie te controleren.
10. Sluit de pagina.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>De functie voor elektronische facturering in de serviceomgeving implementeren

Zie [De functie voor elektronische facturering in de serviceomgeving implementeren](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) voor informatie over het uitvoeren van deze taak.

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>De functie voor elektronische facturering implementeren voor een verbonden toepassing

Zie [De toepassingsinstellingen configureren](e-invoicing-get-started.md#configure-the-application-setup) en [De functie voor elektronische facturering implementeren voor een verbonden toepassing](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) voor informatie over het uitvoeren van deze taak.

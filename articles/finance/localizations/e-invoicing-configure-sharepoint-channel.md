---
title: Een SharePoint-kanaal configureren
description: In dit artikel wordt uitgelegd hoe u een Microsoft SharePoint-kanaal configureert om binnenkomende elektronische facturen te verwerken.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 92eaa357c6d72cc637d4ce353702e5d41ecf4338
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272299"
---
# <a name="configure-a-sharepoint-channel"></a>Een SharePoint-kanaal configureren

[!include [banner](../includes/banner.md)]

Voor het configureren van een Microsoft SharePoint-kanaal voor het verwerken van inkomende documenten moet u de beschreven stappen voltooien in [Een SharePoint-verbinding configureren](e-invoicing-create-sharepoint-connection.md).

Vervolgens kunt u het SharePoint-kanaal gebruiken om elektronische leveranciersfacturen te importeren uit bestanden die in uw SharePoint-mappen zijn opgeslagen.

1. Maak op de SharePoint-site de volgende mappen:

    - **Hoofdmap**: de map waaruit de service de bestanden verwerkt.
    - **Archiefmap**: de map waarin verwerkte bestanden worden opgeslagen.
    - **Foutmap**: de map waarnaar bestanden worden verplaatst als de verwerking mislukt.

2. Selecteer in Regulatory Configuration Services (RCS) de elektronische factureringsfunctie die u hebt gemaakt. Zorg dat u de versie selecteert met de status **Concept**.
3. Selecteer **Toevoegen** op het tabblad **Instellingen**.
4. Selecteer in het dialoogvenster **Functie-instelling maken** in de veldgroep **Nieuw** de optie **Aangepaste instellingen**:
5. Selecteer de optie **Gegevenskanaal** in de veldgroep **Instellingstype**.
6. Selecteer **SharePoint-map** in het veld **Gegevenskanaal selecteren**.
7. Selecteer **Maken**.
8. Selecteer de regel die u eerder hebt gemaakt en selecteer **Bewerken**.
9. Stel op het tabblad **Gegevenskanaal** in de sectie **Parameters** de volgende vereiste velden in.

    | Veld                 | Description |
    |-----------------------|-------------|
    | Gegevenskanaal          | Voer een unieke naam in om het gegevenskanaal te identificeren. De naam mag maximaal 10 tekens lang zijn. Er wordt tijdens het communicatieproces naar verwezen in de toepasbaarheidsregels en in gekoppelde toepassingen. |
    | SharePoint-adres    | Voer de SharePoint-URL in. Voer bijvoorbeeld `<domain>.sharepoint.com` in. |
    | Toepassings-id        | Voer de naam in van het Azure Key Vault-geheim dat de id van het SharePoint-gebruikersaccount bevat. Dit geheim moet worden aangemaakt in de Key Vault en worden ingesteld in uw serviceomgeving. Dit is de waarde van de **Toepassings-id (client)** uit [SharePoint-verbinding configureren](e-invoicing-create-sharepoint-connection.md). |
    | Toepassingsgeheim    | Voer de naam in van het Azure Key Vault-geheim dat het wachtwoord van het SharePoint-gebruikersaccount bevat. Dit is de waarde van het **App-registratiegeheim** uit [SharePoint-verbinding configureren](e-invoicing-create-sharepoint-connection.md). |
    | Naam van vestiging             | Voer de naam van de SharePoint-site in. |
    | Naam van bibliotheek van document | Voer de naam van de SharePoint-documentbibliotheek in. |
    | Time-out               | Voer in milliseconden (ms) in hoe lang het systeem maximaal moet wachten op een antwoord. De standaardwaarde is 10.000 ms (10 seconden). |
    | Hoofdmap           | Geef de bestandsimportbron of de map op van waaruit de service de bestanden verwerkt. |
    | Archiefmap        | Geef de map op waar de verwerkte bestanden moeten worden opgeslagen. |
    | Map met fout          | Geef de map op waarnaar bestanden worden verplaatst als de verwerking mislukt. |
    | Maximum bestandsgrootte         | Voer de maximumgrootte in bytes in van één bestand dat wordt verwerkt. De standaardwaarde is 20.000.000 bytes. |
    | Maximum aantal bestanden      | Voer het maximum aantal bestanden in dat moet worden verwerkt voor één actie. Als u het aantal bestanden niet wilt beperken, stelt u de waarde in op **0** (nul). |
    | Bestandsfilter           | Voer een tekenreeks in om te filteren op bestandsnaam. Dit veld is optioneel. Een eenvoudig masker, zoals **\*smth\*.ext**, wordt ondersteund, waarbij elke asterisk (\*) nul of meer exemplaren van een teken vertegenwoordigt. Voer bijvoorbeeld **\*.pdf** in om het kanaal te configureren voor het lezen van PDF-bestanden. |
    | Aangepaste bestandsnaam      | Voer de aangepaste bestandsnaam van de client in. |

10. Controleer de criteria en werk deze zo nodig bij op het tabblad **Toepasbaarheidsregels**. De waarde van het veld **Kanaal** moet gelijk zijn aan de waarde die u in het veld **Gegevenskanaal** hebt ingevoerd in de vorige stap.
11. Selecteer **Opslaan** en sluit de pagina.

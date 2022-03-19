---
title: Een e-mailkanaal configureren
description: In dit onderwerp wordt uitgelegd hoe u een e-mailkanaal configureert om elektronische facturen te ontvangen.
author: dkalyuzh
ms.date: 02/09/2022
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
ms.openlocfilehash: 6a5896a033212cf0f29f686eec0ab6fb3bc1d2a6
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371552"
---
# <a name="configure-an-email-channel"></a>Een e-mailkanaal configureren

[!include [banner](../includes/banner.md)]

Als met de functie voor elektronische facturering die u hebt gemaakt, elektronische leveranciersfacturen worden geïmporteerd uit bijgevoegde bestanden die per e-mail worden ontvangen, moet u een mailaccountkanaal configureren.

1. Selecteer in Regulatory Configuration Services (RCS) de elektronische factureringsfunctie die u hebt gemaakt. Zorg dat u de versie selecteert met de status **Concept**.
2. Selecteer **Toevoegen** op het tabblad **Instellingen**.
3. Selecteer in het dialoogvenster **Functie-instelling maken** in de veldgroep **Nieuw** de optie **Aangepaste instellingen**:
4. Selecteer de optie **Gegevenskanaal** in de veldgroep **Instellingstype**.
5. Voer in het veld **Gegevenskanaal selecteren** **Inkomende e-mail** in.
6. Selecteer **Maken**.
7. Selecteer de regel die u eerder hebt gemaakt en selecteer **Bewerken**.
8. Stel op het tabblad **Gegevenskanaal** in de sectie **Parameters** de volgende vereiste velden in.

    | Veld                | Description |
    |----------------------|-------------|
    | Gegevenskanaal         | Voer een unieke naam in om het gegevenskanaal te identificeren. De naam mag maximaal 10 tekens lang zijn. Er wordt tijdens het communicatieproces naar verwezen in toepasbaarheidsregels en gekoppelde toepassingen. |
    | Serveradres       | Voer het serveradres van de provider van het e-mailaccount in. Het serveradres voor de provider `https://outlook.live.com` is bijvoorbeeld imap-mail.outlook.com. |
    | Serverpoort          | Voer het nummer van de poort in die de e-mailaccountprovider gebruikt. De serverpoort voor `https://outlook.live.com` is bijvoorbeeld 993. |
    | Geheim voor gebruikersnaam     | Voer de naam in van het Microsoft Azure Key Vault-geheim dat de id van het e-mailgebruikersaccount bevat. Dit geheim moet worden aangemaakt in de Key Vault en worden ingesteld in uw serviceomgeving. |
    | Geheim voor gebruikerswachtwoord | Voer de naam in van het Key Vault-geheim dat het wachtwoord van het e-mailgebruikersaccount bevat. |
    | Time-out              | Voer in milliseconden (ms) de maximale tijdslimiet in dat het systeem moet wachten op een antwoord. De standaardwaarde is 10.000 ms (10 seconden). |
    | Hoofdmap          | Geef de importbron voor e-mail of de map op van waaruit de service de e-mails verwerkt. |
    | Archiefmap       | Geef de map op waar de verwerkte e-mails moeten worden opgeslagen. Als u deze map niet opgeeft, wordt deze automatisch door het systeem gemaakt. |
    | Map met fout         | Geef de map op waarnaar e-mails worden verplaatst als de verwerking mislukt. Als u deze map niet opgeeft, wordt deze automatisch door het systeem gemaakt. |
    | Maximale berichtgrootte     | Voer de maximumgrootte in bytes in van één bericht dat wordt verwerkt. De standaardwaarde is 20.000.000 bytes. |
    | Maximaal berichtnummer   | Voer het maximum aantal berichten in dat moet worden verwerkt voor één actie. Als u het aantal berichten niet wilt beperken, stelt u de waarde in op **0** (nul). |
    | Vanaf-filter          | Voer een tekenreeks in om te filteren op afzenderadres. Alleen e-mails waarin het afzenderadres overeenkomt met het filter, worden verwerkt. Dit veld is optioneel. Als u meerdere afzenderadressen wilt opgeven, gebruikt u puntkomma's (;) als scheidingstekens. |
    | Onderwerpfilter       | Voer een tekenreeks in om te filteren op onderwerp. Alleen e-mails waarin het onderwerp overeenkomt met het filter, worden verwerkt. Dit veld is optioneel. Een eenvoudig masker, zoals **\*smth\*.ext**, wordt ondersteund, waarbij elke asterisk (\*) nul of meer exemplaren van een teken vertegenwoordigt. |
    | Datumfilter          | Geef een datum op om de maximumleeftijd in dagen te definiëren van berichten die worden verwerkt. Dit veld is optioneel. De standaardwaarde is 30 dagen. |
    | Verwerkingsmodus      | <p>Selecteer een van de volgende opties om op te geven of alle bijlagen in een e-mailbericht samen kunnen worden verwerkt of dat elke bijlage afzonderlijk moet worden verwerkt:</p><ul><li><b>Per bijlage</b>: er wordt een nieuw elektronisch document gemaakt voor elke bijlage in het e-mailbericht. Als één e-mailbericht bijvoorbeeld verschillende bestanden bevat die e-factuurgegevens bevatten, wordt elk bestand als een nieuwe e-factuur in het systeem beschouwd.</li><li><b>Per e-mail</b>: één bijlage wordt beschouwd als basisbijlage en wordt er één elektronische factuur in het systeem gemaakt. Andere bijlagen kunnen worden gebruikt als ondersteunende bestanden.</li></ul> |

9. Voeg in de sectie **Bijlagenfilter** de informatie voor het filteren van bestanden in. Alleen bijlagen die voldoen aan het gedefinieerde filter worden verwerkt. Met **\*.xml** wordt bijvoorbeeld gefilterd op bijlagen met de bestandsnaamextensie .xml. De naam van de bijlage wordt in Dynamics 365 Finance of Dynamics 365 Supply Chain Management gebruikt tijdens het instellen.

    - Als u in de vorige staphet veld **Verwerkingsmodus** hebt ingesteld op **Per e-mail**, kunt u hier meerdere filters toevoegen. De naam geeft het specifieke document aan.
    - Als u het veld **Verwerkingsmodus** instelt op **Per bijlage**, kunt u slechts één filter toevoegen.

10. Controleer de criteria en werk deze zo nodig bij op het tabblad **Toepasbaarheidsregels**. De waarde van het veld **Kanaal** moet gelijk zijn aan de waarde die u in het veld **Gegevenskanaal** hebt ingevoerd in stap 8.
11. Selecteer **Opslaan** en sluit de pagina.

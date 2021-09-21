---
title: Fout in certificeringspad bij het instellen van een app-verbinding
description: Als in de app Warehouse Management het foutbericht 'Vertrouwensrelatie voor certificeringspad niet gevonden' wordt weergegeven, gebruikt u deze pagina om het probleem op te lossen of te omzeilen.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476015"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Vertrouwensrelatie voor certificeringspad niet gevonden bij het instellen van een app-verbinding

## <a name="symptoms"></a>Symptomen

Wanneer u verbinding probeert te maken met Supply Chain Management, wordt mogelijk het volgende foutbericht weergegeven in de Warehouse Management-app:

> java.security.cert.certPathValidatorException: Vertrouwensanker voor certificeringspad niet gevonden.

Dit probleem kan gevolgen hebben voor apparaten met de volgende eigenschappen:

- **OS-versie**: Android 4.4.x (zoals Zebra TC55). Dit is geen probleem in recente Android-versies.
- **Locatie Supply Chain Management** : cloud
- **Verbindingsmodus**: clientgeheim of certificaat

## <a name="possible-cause"></a>Mogelijke oorzaak

Microsoft heeft mogelijk de SSL-certificaten op de server bijgewerkt die worden gebruikt door Supply Chain Management. Hierdoor kunnen het basiscertificaat en/of een van de tussenliggende certificaten zijn gewijzigd, waardoor het nieuwe certificaat niet wordt weergegeven in de lijst met vertrouwde systeemcertificaten voor het mobiele apparaat. Nieuwere versies van Android werken de lijsten met vertrouwde certificaten automatisch bij, maar Android 4.4.x doet dit niet.

## <a name="resolution"></a>Oplossing

Voer een van de volgende handelingen uit om het probleem op te lossen:

- Gebruik de workaround die in het volgende gedeelte wordt beschreven om elk relevant apparaat bij te werken.
- Het *kan* mogelijk zijn om contact op te nemen met Zebra of Google om een update te ontvangen van de vertrouwde certificerende instantie (CA)-certificaten. Dit is echter niet bevestigd.
- Overweeg indien mogelijk oudere apparaten te vervangen door apparaten met een recentere versie van Android (waarbij vertrouwde CA-certificaten automatisch worden bijgewerkt).

### <a name="workaround"></a>Tijdelijke oplossing

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>Stap 1: het nieuwe basiscertificaat exporteren vanuit Supply Chain Management

Download het nieuwe basiscertificaat handmatig met uw internetbrowser door het volgende uit te voeren:

1. Meld u aan bij Dynamics Supply Chain Management en open de voorpagina.

1. Selecteer in de adresbalk van uw browser het vergrendelingspictogram om het dialoogvenster **Locatie is veilig** te openen.
1. Selecteer in het dialoogvenster **Certificaat (geldig)** om het venster **Certificaat** te openen voor dat certificaat.
1. Open het tabblad **Certificaatpad** van het venster **Certificaat**.
1. Selecteer het hoogste certificaat in de hiërarchie. (dit is het hoofdcertificaat).
1. Open het tabblad **Details** van het venster **Certificaat**.
1. Selecteer de knop **Naar bestand kopiëren** onderaan het tabblad **Details**.
1. De **wizard Certificaat exporteren** wordt geopend. Selecteer **Volgende** om door te gaan.
1. De pagina **Exportbestandsindeling** wordt geopend. Selecteer **DER-gecodeerd binair X.509 (. CER)**. Selecteer vervolgens **Volgende** om door te gaan.
1. De pagina **Te exporteren bestanden** wordt geopend, geef een bestandsnaam en locatie op. Selecteer vervolgens **Volgende** om door te gaan.
1. De pagina **De exportwizard voor certificaten wordt voltooid** wordt geopend met het resultaat van de export. Selecteer **Voltooien**.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>Stap 2: het gedownloade certificaat installeren op de betrokken apparaten

Installeer het gedownloade certificaat door het volgende uit te voeren:

1. Breng het certificaat dat u in de vorige stap hebt gedownload, over naar het apparaat dat u wilt bijwerken. U kunt bijvoorbeeld een SD-kaart of netwerkverbinding gebruiken om het bestand beschikbaar te maken voor uw apparaat.
1. Open de beveiligingsinstellingen voor uw apparaat en kies de menuoptie om een certificaat vanuit een bestand te installeren. (De exacte stappen hiervoor variëren afhankelijk van het apparaat en de OS-versie.)
1. Het nieuwe certificaat moet nu worden getoond op het tabblad **Gebruiker** voor vertrouwde certificaten.
1. Herhaal deze procedure voor elk getroffen apparaat.

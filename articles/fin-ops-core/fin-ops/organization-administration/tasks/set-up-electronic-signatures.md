---
title: Elektronische handtekeningen instellen
description: Gebruik deze procedure om elektronische handtekeningen in te stellen.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be8d2c95b95be621c81d41fd98e5857caa8bbbcb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981765"
---
# <a name="set-up-electronic-signatures"></a>Elektronische handtekeningen instellen

[!include [banner](../../includes/banner.md)]

Gebruik deze procedure om elektronische handtekeningen in te stellen. Met een elektronische handtekening wordt de identiteit bevestigd van een persoon die een computerproces wil starten of goedkeuren. Het demobedrijf dat wordt gebruikt om deze procedure te maken is DAT.


## <a name="enable-the-electronic-signature-configuration-key"></a>Configuratiesleutel Elektronische handtekening inschakelen
1. Ga naar Systeembeheer > Instellingen > Licentieconfiguratie.
2. Vouw in de structuur 'Beheer' uit.
    * Controleer of het selectievakje Elektronische handtekening is ingeschakeld.  
    * Als het selectievakje Elektronische handtekening niet is ingeschakeld, moet u de onderhoudsmodus inschakelen. De onderhoudsmodus kan in deze omgeving worden ingeschakeld door een onderhoudstaak uit te voeren vanuit Lifecycle Services of door het hulpmiddel Deployment.Setup lokaal te gebruiken.  
3. Sluit de pagina.

## <a name="set-up-electronic-signature-parameters"></a>Parameters voor elektronische handtekeningen instellen
1. Ga naar Organisatiebeheer > Instellingen > Elektronische handtekening > Parameters voor elektronische handtekening.
2. Klik op Bewerken.
3. Typ een waarde in het veld Mededeling.
    * Voer de melding in die ondertekenaars ontvangen wanneer om een handtekening wordt gevraagd. U kunt hier elke gewenste tekst invoeren. Gewoonlijk laat u hiermee de gebruiker weten wat het betekent om een document elektronisch te ondertekenen.  
    * Als u de meldingstekst in aanvullende talen wilt invoeren, klikt u op de knop Vertalingen.  
4. Klik op Opslaan.
5. Sluit de pagina.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Redencodes voor elektronische handtekeningen instellen
1. Ga naar Organisatiebeheer > Instellingen > Elektronische handtekening > Redencodes elektronische handtekening.
2. Klik op Nieuw.
    * U moet redencodes instellen voordat u elektronische handtekeningen kunt gebruiken. Een geldige redencode is vereist voor het ondertekenen van een document.     Een ondertekenaar selecteert een redencode om het doel van een elektronische handtekening aan te geven. Een redencode kan bijvoorbeeld worden gebruikt om wettelijke goedkeuring aan te geven.  
3. Typ een waarde in het veld Redencode.
4. Typ een waarde in het veld Omschrijving.
    * Voer aanvullende redencodes in indien nodig.  
5. Klik op Opslaan.
6. Sluit de pagina.

## <a name="require-electronic-signatures-for-existing-processes"></a>Elektronische handtekeningen voor bestaande processen vereisen
1. Ga naar Organisatiebeheer > Instellingen > Elektronische handtekening > Vereisten elektronische handtekeningen.
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer een proces dat elektronische handtekeningen vereist  
3. Schakel het selectievakje Handtekening vereist desgewenst in of uit.
    * Herhaal deze stappen voor elk proces dat elektronische handtekeningen vereist.  
4. Klik op Opslaan.

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Een aangepaste vereiste voor elektronische handtekeningen maken
1. Klik op Nieuw.
2. Schakel het selectievakje Handtekening vereist desgewenst in of uit.
3. Geef in het veld Naam een naam op voor het proces dat elektronische handtekeningen vereist.
4. Klik in het veld Tabelnaam op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer in de lijst de tabel waarin de gegevens die moeten worden ondertekend, zijn opgeslagen.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik in het veld Veldnaam op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Zoek en selecteer in de lijst het veld in de tabel dat u wilt controleren.
9. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Geef op wanneer een handtekening is vereist.     Selecteer Altijd als een handtekening vereist is wanneer de gegevens in het veld worden gewijzigd.     Selecteer Alleen als een handtekening alleen onder bepaalde voorwaarden vereist is. Als u Alleen selecteert, moet u een van de volgende opties ook selecteren: Wanneer een record wordt ingevoegd, Wanneer een record wordt bijgewerkt of Wanneer een record wordt verwijderd.  
10. Klik op Opslaan.
11. Sluit de pagina.


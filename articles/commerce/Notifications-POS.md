---
title: Meldingen over orders op het verkooppunt (POS) weergeven
description: In dit onderwerp wordt beschreven hoe u ordermeldingen inschakelt in het POS en het framework voor meldingen.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 57f5d23533c2fd17593648a15745fa770fc01dc4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345203"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Meldingen over orders op het verkooppunt (POS) weergeven

[!include [banner](includes/banner.md)]

Aan winkelmedewerkers kunnen verschillende taken in hun winkel worden toegewezen, zoals het vervullen van orders of het uitvoeren van voorraadontvangsten of voorraadtellingen. De POS-client (Pont of Sale) biedt een enkele toepassing waarin medewerkers kunnen worden geïnformeerd over deze taken. Het framework voor meldingen in de POS-client stelt detailhandelaren in staat meldingen op basis van rollen te configureren. Vanaf Dynamics 365 Retail met toepassingsupdate 5 kunnen deze meldingen alleen voor POS-bewerkingen worden geconfigureerd.

Het systeem kan meldingen voor de bewerking *orderafhandeling* tonen en vanaf Commerce-versie 10.0.18 kunnen meldingen ook worden weergegeven voor de bewerking *Order intrekken*. Echter, omdat het framework kan worden verlengd, kunnen ontwikkelaars een [meldingenhandler schrijven](dev-itpro/extend-pos-notification.md) voor elke bewerking en de meldingen voor die bewerking weergeven in het POS.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Meldingen voor bewerkingen orderafhandeling of Order intrekken inschakelen

Voer deze stappen uit om meldingen voor de bewerkingen orderafhandeling of Order intrekken in te schakelen.

1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> Bewerkingen**.
1. Zoek de bewerking **Orderafhandeling** of de bewerking **Order intrekken** en schakel het selectievakje **Meldingen inschakelen** voor de bewerking in om op te geven dat het framework voor meldingen naar de handler voor deze bewerking moet luisteren. Als de handler is geïmplementeerd, worden meldingen voor deze bewerking vervolgens weergegeven in het POS.
1. Ga naar **Retail en commerce \> Werknemers \> Medewerkers**.
1. Selecteer het tabblad **Commerce**, selecteer een medewerkersrij en selecteer vervolgens **POS-machtigingen**. Selecteer het sneltabblad **Meldingen** om het uit te vouwen en voeg vervolgens de bewerkingen toe waarvoor u meldingen hebt ingeschakeld. Als u een enkele melding voor een medewerker configureert, moet u ervoor zorgen dat de waarde van **Weergavevolgorde** is ingesteld op **1**. Als u meerdere bewerkingen configureert, stelt u de waarden voor **Weergavevolgorde** in om de volgorde aan te geven waarin de meldingen moeten worden weergegeven. 

      Meldingen worden alleen weergegeven voor bewerkingen die zijn toegevoegd op het sneltabblad **Meldingen**. U kunt daar alleen bewerkingen toevoegen als de selectievakjes **Meldingen inschakelen** voor deze bewerkingen zijn ingeschakeld op de pagina **POS-bewerkingen**. Bovendien worden meldingen voor een bewerking alleen aan medewerkers weergegeven als de bewerking wordt toegevoegd aan de POS-machtigingen voor die medewerkers.

    > [!NOTE]
    > Meldingen kunnen worden overschreven op het gebruikersniveau. Hiertoe opent u de gegevens van de medewerker, selecteert u **POS-machtigingen** en bewerkt u vervolgens de meldingen waarop de gebruiker is geabonneerd.

1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**. Geef in het veld **Meldingsinterval** op hoe vaak meldingen moeten worden opgehaald. Voor sommige meldingen moet het POS real-time oproepen naar de back office-toepassing maken. Deze oproepen verbruiken rekencapaciteit van de back office-toepassing. Dus wanneer u het meldingsinterval instelt, moet u rekening houden met zowel de bedrijfsvereisten als de impact van real-time aanroepen voor de back office-toepassing. Een waarde van **0** (nul) schakelt meldingen uit.
1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**. Selecteer de planning **1060** (**Personeel**) om instellingen voor meldingsabonnementen te synchroniseren en selecteer **Nu uitvoeren**. Selecteer vervolgens de planning **1070** (**Kanaalconfiguratie**) om het machtigingsinterval te synchroniseren en selecteer **Nu uitvoeren**.

## <a name="view-notifications-in-the-pos"></a>Meldingen weergeven in POS

Nadat u de voorgaande stappen hebt voltooid, kunnen de werknemers de meldingen weergeven in het POS. Als u meldingen wilt weergeven, selecteert u het meldingspictogram in de rechterbovenhoek van het POS. Er wordt een venster met meldingen weergegeven voor de bewerkingen die voor de medewerker zijn geconfigureerd. 

Voor de bewerking **orderafhandeling** worden in het venster met meldingen de volgende groepen weergegeven:

- **Ophalen in de winkel**: voor deze groep wordt het aantal individuele orderregels weergegeven die zijn gepland met de huidige winkel als afhaallocatie. U kunt het nummer in de groep selecteren om de bewerking **Orderafhandeling** te openen met een filter, zodat alleen de actieve orderregels worden weergegeven die zijn ingesteld om te worden opgehaald uit de huidige winkel.
- **Verzenden vanuit winkel**: deze groep toont het aantal afzonderlijke orderregels dat is geconfigureerd voor verzenden vanuit de huidige winkel van de gebruiker. U kunt het nummer in de groep selecteren om de bewerking **Orderafhandeling** te openen met een gefilterde, zodat alleen de actieve orderregels worden weergegeven die zijn ingesteld voor verzending vanuit de huidige winkel.

Voor de bewerking **Order intrekken** worden in het venster met meldingen de volgende groepen weergegeven:

- **Af te handelen ordersz**: deze groep toont het aantal orders dat is geconfigureerd voor ophalen of afhandeling van verzending voor de huidige winkel van de gebruiker. U kunt het nummer in de groep selecteren om de bewerking **Order intrekken** te openen met een gefilterde weergave. In deze weergave worden alleen de openstaande orders weergegeven die moeten worden uitgevoerd door de huidige winkel van de gebruiker voor de scenario's voor afhalen in de winkel of verzenden vanuit de winkel.
- **Op te halen orders**: voor deze groep wordt het aantal orders weergegeven dat is gepland met de huidige winkel als afhaallocatie. U kunt het nummer in de groep selecteren om de bewerking **Order intrekken** te openen met een gefilterde weergave. In deze weergave worden alleen openstaande orders weergegeven die moeten worden vervuld voor afhalen door de klant vanuit de huidige winkel van de gebruiker.
- **Te verzenden orders**: in deze groep wordt het aantal orders dat moet worden verzonden vanuit de huidige winkel van de gebruiker. U kunt het nummer in de groep selecteren om de bewerking **Order intrekken** te openen met een gefilterde weergave. In deze weergave worden alleen openstaande orders weergegeven die moeten worden vervuld voor verzending vanuit de huidige winkel van de gebruiker.

Voor zowel de melding voor orderafhandeling als de melding voor het intrekken van orders geldt dat, terwijl er nieuwe orders worden opgepakt door het proces, het meldingspictogram verandert om aan te geven dat er nieuwe meldingen zijn. Tevens wordt het aantal bijbehorende groepen bijgewerkt. Hoewel de groepen met regelmatige tussenpozen worden vernieuwd, kunnen POS-gebruikers de groepen op elk gewenst moment handmatig vernieuwen met de knop **Vernieuwen** naast de groep. Tot slot geldt dat als een groep een nieuw artikel heeft dat de huidige medewerker niet heeft bekeken, bij de groep een symbool wordt vertoond om aan te geven dat er nieuwe inhoud is.

## <a name="enable-live-content-on-pos-buttons"></a>Live inhoud op de POS-knoppen inschakelen

POS-knoppen kunnen nu een aantal aangeven zodat de werknemers eenvoudig kunnen bepalen welke taken hun onmiddellijke aandacht vereisen. Als u dit aantal wilt weergeven op een POS-knop, moet u de instellingen voor berichtgeving invullen die eerder in dit onderwerp zijn beschreven (dat wil zeggen u moet meldingen voor een bewerking inschakelen, een meldingsinterval instellen en de POS-machtigingsgroep voor de werknemer bijwerken). Daarnaast moet u de ontwerper van het knoppenraster openen, de eigenschappen van de knop weergeven en het selectievakje **Live inhoud inschakelen** selecteren. In het veld **Uitlijning van inhoud** kunt u aangeven of de telling wordt weergegeven in de rechterbovenhoek van de knop (**Rechtsboven**) of in het midden (**Midden**).

> [!NOTE]
> De live inhoud kan alleen worden ingeschakeld voor bewerkingen als het selectievakje **Meldingen inschakelen** is ingeschakeld op de pagina **POS-bewerkingen**, zoals eerder in dit onderwerp is beschreven.

In de volgende afbeelding ziet u de instellingen voor live inhoud in de ontwerper van het knoppenraster.

![Instellingen voor live inhoud in de ontwerpfunctie voor het knoppenraster.](./media/ButtonGridDesigner.png "Instellingen voor live inhoud in de ontwerpfunctie voor het knoppenraster")

Als u het aantal meldingen op een knop wilt weergeven, moet u ervoor zorgen dat de juiste schermindeling wordt bijgewerkt. Als u wilt bepalen welke schermindeling door het POS wordt gebruikt, selecteert u het pictogram **Instellingen** in de rechterbovenhoek en noteert u de **schermindelings-id** en **indelingsresolutie**. Ga nu met de browser Edge naar de pagina **Schermindeling**, zoek de **schermindelings-id** en **indelingsresolutie** die hierboven wordt aangegeven en schakel het selectievakje **Live inhoud inschakelen** in. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning** en voer de taak 1090 (Kassa's) uit om indelingswijzigingen te synchroniseren.

![De schermindeling zoeken die door POS wordt gebruikt.](./media/Choose_screen_layout.png "De schermindeling zoeken")

De volgende afbeelding toont het effect van het selecteren van **Rechtsboven** versus **Midden** in de het del **Uitlijning van inhoud** voor knoppen van verschillende grootten.

![Live inhoud op de POS-knoppen.](./media/ButtonsWithLiveContent.png "Live inhoud op de POS-knoppen")

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Meldingen over orders op het verkooppunt (POS) weergeven
description: In dit onderwerp wordt beschreven hoe u ordermeldingen inschakelt in het POS en het framework voor meldingen.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: c3b8e2774a189f2afefa757e7c4f3885b674918c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976783"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Meldingen over orders op het verkooppunt (POS) weergeven

[!include [banner](includes/banner.md)]

In de moderne detailhandelomgeving worden er verschillende taken toegewezen aan winkelmedewerkers, zoals het helpen van klanten, het invoeren van transacties, het uitvoeren van voorraadtellingen en het ontvangen van orders in de winkel. De POS-client (Pont of Sale) biedt één toepassing waar de medewerkers alle taken en nog veel meer kunnen uitvoeren. Omdat ze gedurende de dag verschillende taken moeten uitvoeren, moeten medewerkers mogelijk op de hoogte worden gesteld wanneer iets hun aandacht vereist. Het framework voor meldingen in de POS-client stelt detailhandelaren in staat meldingen op basis van rollen te configureren. Vanaf Dynamics 365 for Retail met toepassingsupdate 5 kunnen deze meldingen kunnen alleen voor POS-bewerkingen worden geconfigureerd.


Op dit moment kan het systeem meldingen alleen weergeven voor orderafhandelingsbewerkingen. Echter, omdat het framework kan worden verlengd, kunnen ontwikkelaars uiteindelijk een meldingenhandler schrijven voor elke bewerking en de meldingen voor die bewerking weergeven in het POS.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Meldingen voor orderafhandelingsbewerkingen inschakelen

Ga als volgt te werk om meldingen voor de orderafhandelingsbewerkingen in te schakelen.

1. Ga naar **Retail en Commerce** &gt; **Afzetkanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Bewerkingen**.
2. Zoek de bewerking **Orderafhandeling** en selecteer het selectievakje **Meldingen inschakelen** om op te geven dat het framework voor meldingen naar de handler voor deze bewerking moet luisteren. Als de handler is geïmplementeerd, worden meldingen voor deze bewerking vervolgens weergegeven in het POS.
3. Ga naar **Retail en Commerce** &gt; **Werknemers** &gt; **Medewerkers** &gt; en open onder het tabblad Commerce de POS-machtigingen die aan de medewerker zijn gekoppeld. Vouw het sneltabblad **Meldingen** uit, voeg de bewerking **Orderafhandeling** toe en stel het veld **Weergavevolgorde** in op **1**. Als meer dan één kennisgeving is geconfigureerd, wordt dit veld gebruikt om de meldingen te ordenen. Meldingen met een lagere waarde voor **Weergavevolgorde** worden weergegeven boven de meldingen die een hogere waarde hebben. Meldingen die een waarde voor **Weergavevolgorde** hebben van **1**, staan bovenaan.

    Meldingen worden alleen weergegeven voor bewerkingen die zijn toegevoegd op het sneltabblad **Meldingen** en u kunt alleen bewerkingen toevoegen als het selectievakje **Meldingen inschakelen** voor deze bewerkingen is geselecteerd op de pagina **POS-bewerkingen**. Bovendien worden meldingen voor een bewerking alleen aan werknemers weergegeven als de bewerking wordt toegevoegd aan de POS-machtigingen voor die werknemers.

    > [!NOTE]
    > Meldingen kunnen worden overschreven op het gebruikersniveau. Open de gegevens van de medewerker, selecteer de **POS-machtigingen** en bewerk de meldingen waarop de gebruiker is geabonneerd.

4. Ga naar **Retail en Commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Functionaliteitsprofielen**. Geef in het veld **Meldingsinterval** op hoe vaak meldingen moeten worden opgehaald. Voor sommige meldingen moet het POS real-time oproepen naar de back office-toepassing maken. Deze oproepen verbruiken rekencapaciteit van de back office-toepassing. Dus wanneer u het meldingsinterval instelt, moet u rekening houden met zowel de bedrijfsvereisten als de impact van real-time aanroepen voor de back office-toepassing. Een waarde van **0** (nul) schakelt meldingen uit.
5. Ga naar **Retail en Commerce** &gt; **Retail en Commerce IT** &gt; **Distributieplanning**. Selecteer de planning **1060** (**Personeel**) om instellingen voor meldingsabonnementen te synchroniseren en selecteer **Nu uitvoeren**. Selecteer vervolgens de planning **1070** (**Kanaalconfiguratie**) om het machtigingsinterval te synchroniseren en selecteer **Nu uitvoeren**.

## <a name="view-notifications-in-the-pos"></a>Meldingen weergeven in POS

Nadat u de voorgaande stappen hebt voltooid, kunnen de werknemers de meldingen weergeven in het POS. Als u de meldingen wilt weergeven, klikt u op het meldingspictogram rechtsboven van het POS. Er verschijnt een meldingencentrum met meldingen voor de orderafhandelingsbewerking. Als het goed is, worden de volgende groepen in de orderafhandelingsbewerking weergegeven:

- **Ophalen in de winkel**: voor deze groep wordt het aantal orders weergegeven waarvoor de leveringsmethode **Afhalen** is ingesteld en die zijn gepland met de huidige winkel als afhaallocatie. Druk op het nummer van de groep om de pagina **Orderafhandeling** te openen. In dit geval wordt de pagina gefilterd zodat alleen de actieve orders worden getoond die zijn ingesteld voor ophalen uit de huidige winkel.
- **Verzenden uit winkel**: voor deze groep wordt het aantal orders weergegeven waarvoor de leveringsmethode **Verzenden** is ingesteld en die zijn gepland met de huidige winkel als verzendlocatie. Druk op het nummer van de groep om de pagina **Orderafhandeling** te openen. In dit geval wordt de pagina gefilterd zodat alleen de actieve orders worden getoond die zijn ingesteld voor verzending uit de huidige winkel.

Wanneer er nieuwe orders aan de winkel worden toegewezen voor afhandeling, verandert het meldingspictogram om aan te geven dat er nieuwe meldingen zijn en wordt het aantal bijbehorende groepen bijgewerkt. Ook al worden de groepen met regelmatige tussenpozen worden vernieuwd, kunnen POS-gebruikers de groepen op elk gewenst moment handmatig vernieuwen met de knop **Vernieuwen** naast de groep. Als een groep een nieuw artikel heeft dat de huidige werknemer niet heeft bekeken, wordt bij de groep een symbool om de nieuwe inhoud aan te geven.

## <a name="enable-live-content-on-pos-buttons"></a>Live inhoud op de POS-knoppen inschakelen

POS-knoppen kunnen nu een aantal aangeven zodat de werknemers eenvoudig kunnen bepalen welke taken hun onmiddellijke aandacht vereisen. Als u dit aantal wilt weergeven op een POS-knop, moet u de instellingen voor berichtgeving invullen die eerder in dit onderwerp zijn beschreven (dat wil zeggen u moet meldingen voor een bewerking inschakelen, een meldingsinterval instellen en de POS-machtigingsgroep voor de werknemer bijwerken). Daarnaast moet u de ontwerper van het knoppenraster openen, de eigenschappen van de knop weergeven en het selectievakje **Live inhoud inschakelen** selecteren. In het veld **Uitlijning van inhoud** kunt u aangeven of de telling wordt weergegeven in de rechterbovenhoek van de knop (**Rechtsboven**) of in het midden (**Midden**).

> [!NOTE]
> De live inhoud kan alleen worden ingeschakeld voor bewerkingen als het selectievakje **Meldingen inschakelen** is ingeschakeld op de pagina **POS-bewerkingen**, zoals eerder in dit onderwerp is beschreven.

In de volgende afbeelding ziet u de instellingen voor live inhoud in de ontwerper van het knoppenraster.

![Instellingen voor live inhoud in de ontwerpfunctie voor het knoppenraster](./media/ButtonGridDesigner.png "Instellingen voor live inhoud in de ontwerpfunctie voor het knoppenraster")

Als u het aantal meldingen op een knop wilt weergeven, moet u ervoor zorgen dat de juiste schermindeling wordt bijgewerkt. Als u wilt bepalen welke schermindeling door het POS wordt gebruikt, selecteert u het pictogram **Instellingen** in de rechterbovenhoek en noteert u de **schermindelings-id** en **indelingsresolutie**. Ga nu met de browser Edge naar de pagina **Schermindeling**, zoek de **schermindelings-id** en **indelingsresolutie** die hierboven wordt aangegeven en schakel het selectievakje **Live inhoud inschakelen** in. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning** en voer de taak 1090 (Kassa's) uit om indelingswijzigingen te synchroniseren.


![De schermindeling zoeken die door POS wordt gebruikt](./media/Choose_screen_layout.png "De schermindeling zoeken")

De volgende afbeelding toont het effect van het selecteren van **Rechtsboven** versus **Midden** in de het del **Uitlijning van inhoud** voor knoppen van verschillende grootten.

![Live inhoud op de POS-knoppen](./media/ButtonsWithLiveContent.png "Live inhoud op de POS-knoppen")


[!INCLUDE[footer-include](../includes/footer-banner.md)]
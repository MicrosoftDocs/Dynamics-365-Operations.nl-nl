---
title: Store Commerce-app voor mobiele platformen
description: In dit artikel wordt beschreven hoe u aan de slag kunt gaan met de Microsoft Dynamics 365 Commerce Store Commerce-app voor Android en iOS.
author: stuharg
ms.date: 10/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: 1f07a130629863ebd9d036378436cf360e90ac26
ms.sourcegitcommit: 98231ff810f41f9fcdc6b536d87e453028aa6db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/07/2022
ms.locfileid: "9642336"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Store Commerce-app voor mobiele platformen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u aan de slag kunt gaan met de Microsoft Dynamics 365 Commerce Store Commerce-apps voor Android en iOS.

Met de mobiele Dynamics 365 Commerce-apps voor Android en iOS kunt u op eenvoudige wijze en zonder veel moeite complete mobiele POS-apparaten implementeren voor uw detailhandelomgeving. De mobiele Store Commerce-apps bieden alle mogelijkheden en voordelen van de [Store Commerce-app voor Windows](store-commerce.md) in telefoon- en tabletformaat. De mobiele Store Commerce-apps kunnen rechtstreeks worden geïnstalleerd vanuit de Apple en Google Play app stores en ontwikkelaars hoeven geen nieuw toepassingspakket te maken om deze te implementeren of bij te werken. 

De mobiele Store Commerce-apps bieden dezelfde functionaliteit als de huidige hybride Retail-apps. Daarnaast bevat Store Commerce voor iOS ondersteuning voor een specifiek hardwarestation, zodat iOS-apparaten kunnen communiceren met netwerkbetalingsterminals, kassabonprinters en kassaladen zonder dat er een gezamenlijk hardwarestation hoeft te worden geïmplementeerd. 

> [!IMPORTANT]
> De Store Commerce-apps voor Windows, Android en iOS zijn de volgende generatie POS-toepassingen voor Dynamics 365 Commerce. De huidige MPOS-toepassing (Modern POS) [en de hybride Retail-apps](hybridapp.md) voor mobiel worden in oktober 2023 afgeschaft. Microsoft adviseert u Store Commerce of Cloud POS (CPOS) te gebruiken voor alle nieuwe POS-implementaties. Bestaande klanten kunnen het beste plannen maken voor het migreren van de hybride Retail-app naar Store Commerce. Zie [De Dynamics 365 Commerce-technologiestack binnen de winkel moderniseren](https://www.microsoft.com/download/details.aspx?id=103896) voor meer informatie over het afschaffingsschema voor MPOS en de hybride Retail-apps. 

## <a name="app-architecture"></a>App-architectuur

De mobiele Store Commerce-apps gebruiken dezelfde topologie als de Store Commerce-app voor Windows wanneer deze in de hybride modus wordt geïmplementeerd. De mobiele Store Commerce-apps zijn shell-toepassingen die CPOS rechtstreeks vanuit de Commerce Scale Unit (CSU) weergeven en via de CSU verbinding maken met Headless Commerce en Commerce Headquarters. Met het shell-toepassingsmodel kunnen Store Commerce-apps een specifiek hardwarestation ondersteunen voor directe integratie met een betalingsterminal, printer, kassalade en andere randapparatuur. U hoeft geen gedeeld hardwarestation in te stellen om hardwareapparaten te kunnen gebruiken. 

Als u een mobiele Store Commerce-app wilt bijwerken, werkt u simpelweg de CSU bij. Alle nieuwe POS-functionaliteit en -functies worden automatisch door de app opgehaald. Zie [Updates en uitbreidingen toepassen op Commerce Scale Unit (cloud)](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md) voor meer informatie over het bijwerken van de CSU.

De shell-apps worden aangeboden via updates in de app store. Wanneer een secundaire versie de algemene beschikbaarheid (GA) bereikt, publiceert Microsoft deze naar de app stores. Microsoft publiceert mogelijk ook patches tussen secundaire versie-updates om correcties met hoge prioriteit uit te brengen.

## <a name="prerequisites"></a>Vereisten

Voor de mobiele Store Commerce-apps is Dynamics 365 Commerce vereist, en dan met name de onderdelen Commerce Headquarters en CSU. De volgende tabel bevat de minimale besturingssysteem- (OS) en CSU-versies die zijn vereist zijn voor de mobiele Android- en iOS-apps. 

| Vereiste | Android      | iOS  |
| ------------ | ------------ | ---- |
| Besturingssysteemversie   | 7.0          | 15.0 |
| CSU-versie  | 9.38.22266.8 | Nog te doen  |

## <a name="install-the-app"></a>De app installeren

U kunt de mobiele Store Commerce-apps rechtstreeks installeren vanuit de Google Play Store of Apple App Store 

- [Store Commerce-app voor Android](https://aka.ms/storecommerceandroid)
- Store Commerce-app voor iOS (binnenkort beschikbaar)

De pakketten voor de Android-app (.apk) en Apple-app (.ipa) kunnen ook worden gedownload vanuit de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services. 

## <a name="device-and-register-setup"></a>Instelling van apparaten en kassa's

Voordat een kassa kan worden geactiveerd op de mobiele Store Commerce-apps, moet u een apparaat en een kassa instellen in Commerce Headquarters. Zie [Apparaten en kassa's](../implementation-considerations-devices.md) voor meer informatie. 

### <a name="device-setup"></a>Instelling van apparaten

Voer deze stappen uit om een nieuw apparaat te maken en in te stellen.

1. Ga in Commerce Headquarters naar **Retail en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> Apparaten**. 
1. Maak een nieuw apparaat en selecteer **Modern POS - Android** of **Modern POS - iOS** als het toepassingstype, afhankelijk van de mobiele app die u implementeert. 

    > [!NOTE] 
    > De toepassingstypen **Modern POS - Android** en **Modern POS - iOS** worden ook gebruikt voor de implementatie van de huidige hybride apps voor Android en iOS. Na de afschaffing van MPOS worden de labels voor deze toepassingstypen bijgewerkt naar **Store Commerce - Android** en **Modern POS - iOS**. 

### <a name="register-setup"></a>Kassa-instellingen

U kunt een nieuwe kassa maken en deze aan het apparaat koppelen dat u hebt gemaakt of u kunt een bestaande kassa aan uw nieuwe apparaat koppelen. Zie [Kassa's maken en koppelen](../tasks/create-associate-registers.md) voor meer informatie over kassa's.

### <a name="screen-layout-setup"></a>Instelling van schermindeling

Als u een schermindeling die is opgenomen in de demonstratiegegevens die worden meegeleverd met uw Dynamics 365 Commerce-licentie opnieuw gebruikt, selecteert de Store Commerce-app automatisch de opgenomen indeling als de schermoplossing van uw apparaat minder dan 480 &times; 853 pixels bedraagt in de staande richting. Als u echter een compleet nieuwe schermindeling maakt of als uw mobiele apparaat een hogere resolutie gebruikt dan wordt ondersteund door de compacte indeling, moet u zorgen voor een resolutie en bijbehorende knoppenrasters die geschikt zijn voor de telefoon of tablet waarop u van plan bent te implementeren. Zie [Zichtbare configuraties voor de POS-gebruikersinterface](../pos-screen-layouts.md) voor meer informatie over configuraties voor schermindelingen. 

Nadat apparaten en kassa's zijn geconfigureerd, gaat u in Commerce Headquarters naar **Retail en Commerce \> Retail en Commerce-id \> Distributieplanningen** en voert u de taak Kassa's uit.

## <a name="activate-a-device"></a>Een apparaat activeren

Volg deze stappen om een apparaat te activeren op een mobiele Store Commerce-app.

1. Open de app op het mobiele apparaat.
1. Voer de CPOS-URL in, die u kunt vinden op de pagina met details van de omgeving in Lifecycle Services of op de pagina **Kanaalprofielen** in Commerce Headquarters (**Retail en Commerce \> Afzetkanaalinstellingen \> Afzetkanaalprofielen**).
1. Meld u aan met de referenties van een werknemer die machtigingen heeft om apparaten te beheren.
1. Selecteer de winkel die is gekoppeld aan de kassa die u hebt gemaakt of opnieuw hebt gebruikt in Commerce Headquarters.
1. Selecteer de kassa die u aan het apparaat hebt gekoppeld dat u hebt gemaakt in Commerce Headquarters.
1. Uw apparaat moet nu zijn geactiveerd. U kunt zich aanmelden bij de kassa met de operator-id en het wachtwoord voor de werknemer die aan de winkel is gekoppeld die u hebt geselecteerd. 

Zie [POS-apparaatactivering (Point of sale)](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation) voor meer informatie over het activeren van apparaten.

## <a name="feature-parity-with-store-commerce-for-windows"></a>Functiepariteit met Store Commerce voor Windows

In de volgende tabel worden de mogelijkheden van de Store Commerce-app op de Windows-, Android- en iOS-platforms vergeleken.

| Functie                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Specifiek hardwarestation                                                            | Ja     | Ja     | Ja |
| Gedeeld hardwarestation                                                               | Ja     | Ja     | Ja |
| Communicatie met netwerkrandapparatuur (betalingsterminal, printer en kassalade) | Ja     | Ja     | Ja |
| OLE voor OPOS-randapparatuur (OLE for Point of Sale) via een lokaal hardwarestation             | Ja     | Nr.      | Nr.  |
| Offlinemodus                                                                          | Ja     | Nr.      | Nr.  |

## <a name="additional-resources"></a>Aanvullende bronnen

[Store Commerce-app](store-commerce.md)

[Kiezen tussen Store Commerce en Cloud POS](../mpos-or-cpos.md)

[Problemen met het instellen en installeren van Store Commerce oplossen](../troubleshoot/store-commerce-setup-installation.md)

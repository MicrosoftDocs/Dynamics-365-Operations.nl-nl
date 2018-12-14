---
title: URL openen in POS
description: Dit onderwerp biedt een overzicht van verbeteringen die zijn aangebracht in de functies voor het zoeken van producten en klanten in Microsoft Dynamics 365 for Retail.
author: AamirAllaq
manager: AnnBe
ms.date: 11/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: f7df0a91948a494465fbd55af99757e3890357ce
ms.openlocfilehash: 4b8a0291855460b79f3a241eccb4b55b009804bf
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---

# <a name="open-url-in-pos"></a>URL openen in POS

In dit onderwerp wordt beschreven hoe u een knop in Retail POS kunt configureren zodat hiermee een URL wordt geopend. Hiervoor hoeft geen code te worden aangepast en dit kan worden geconfigureerd door iemand die geen ontwikkelaar is.

Met deze functie kan een knop in POS zo worden geconfigureerd dat via de ontwerpfunctie van het knoppenraster een URL wordt geopend. Dit wordt op dit moment ondersteund in de volgende configuraties:

- Openen in nieuw venster.
- Openen in POS.
- Een native app openen. 

## <a name="open-in-new-window"></a>Openen in nieuw venster

Deze configuratie bepaalt of de URL in een nieuw venster of in de app wordt geopend. Als de knop is geconfigureerd om een web-URL in de app te openen, zijn het navigatievenster aan de zijkant en de bovenste balk van POS zichtbaar en beschikbaar voor gebruikersinteractie. Is de knop geconfigureerd om in een nieuw venster te worden geopend, dan wordt de URL geopend in een nieuw app-venster in Modern POS voor Windows en in een nieuw browsertabblad in alle andere POS-clients. Om dit mogelijk te maken, moet u de optie **Openen in nieuw venster** selecteren als u de URL configureert.

## <a name="open-within-pos"></a>Openen in POS
Het openen van een web-URL in POS wordt momenteel alleen ondersteund voor Modern POS in Windows. In andere clients wordt hieraan gewerkt en is dit in toekomstige updates wel mogelijk. Om dit mogelijk te maken, moet u de optie **Openen in nieuw venster** niet selecteren als u de URL configureert.

## <a name="open-a-native-app"></a>Een native app openen
Met deze functie kunt u niet-web-URL's opgeven om een native app te openen. U kunt bijvoorbeeld URL-protocollen, zoals MailTo, SIP, IM of MSTEAMS, opgeven. Deze kunnen vervolgens worden verwerkt door respectievelijke native apps op het hostapparaat. Om dit mogelijk te maken, moet u de optie **Openen in nieuw venster** selecteren als u de URL configureert. 

- Raadpleeg voor Windows-computers [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) om de standaardprotocolkoppelingen in te stellen als u uw computer instelt met Deployment Image Servicing and Management (DISM). 
- Als u MDM, bijvoorbeeld Intune, gebruikt voor het beheren van uw Windows-computers, raadpleegt u [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults). 
- Als u als ontwikkelaar een aangepaste website bouwt, raadpleegt u [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app). 

## <a name="open-a-native-app-seamlessly"></a>Naadloos een native app openen
Windows, iOS en Android bieden ook ondersteuning voor een vloeiendere methode voor het openen van apps, op basis van de koppeling van app-protocollen. Als uw app nog niet is geconfigureerd om vanuit een webbrowser te worden geopend, moet u hiervoor mogelijk de hulp van een ontwikkelaar inroepen.

- Raadpleeg voor Windows [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).
- Raadpleeg voor iOS [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).
- Raadpleeg voor Android [Handling Android App Links](https://developer.android.com/training/app-links/).  


|   Client                |Openen in nieuw venster |Native app openen | Openen in POS            | Details                           |
|-------------------------|-------------------|----------------|--------------------------|-----------------------------------|
| Modern POS in Windows   | ✓*                |    ✓          |       ✓                  | *Wordt geopend in nieuw Modern POS-venster   |
| Cloud-POS               | ✓*                |    ✓          |       X                   |  *Wordt geopend op nieuw browsertabblad       |
| Modern POS in iOS       | ✓*                |    ✓          |       X                  |  *Wordt geopend op nieuw browsertabblad        |
| Modern POS in Android   | ✓*                |    ✓          |       X                  |  *Wordt geopend op nieuw browsertabblad        |

## <a name="before-you-begin"></a>Voordat u begint
Controleer voordat u begint hoe u [schermindelingen voor het verkooppunt (POS)](pos-screen-layouts.md) configureert.

## <a name="open-url-in-pos"></a>URL openen in POS
Als u een URL wilt configureren om in POS te worden geopend, voert u de volgende stappen uit.

1.  Ga naar **Detailhandel > Kanaalinstellingen > POS-instellingen > POS > Schermindelingen**.
2.  Selecteer **Knoppenrasters > Ontwerper**.
3.  Maak een nieuwe knop.
4.  Selecteer **Knopeigenschappen**.
5.  Selecteer **URL openen** als de actie.
6.  Voer de URL in die u wilt gebruiken.
7.  Configureer of de URL in een nieuw venster wordt geopend.

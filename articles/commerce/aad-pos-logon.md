---
title: Authenticatie in Azure Active Directory voor POS-aanmelding configureren
description: In dit onderwerp wordt uitgelegd hoe u Azure Active Directory configureert als de verificatiemethode voor het Microsoft Dynamics 365 Commerce-verkooppunt.
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 63121a9b5f1b062b7ca927f6b9eb1689ce8aa698
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270678"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Authenticatie in Azure Active Directory voor POS-aanmelding configureren

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u Azure Active Directory (Azure AD) configureert als de verificatiemethode voor het Microsoft Dynamics 365 Commerce-verkooppunt (POS).

Detailhandelaren die Dynamics 365 Commerce gebruiken samen met andere Microsoft-cloudservices zoals Microsoft Azure, Microsoft 365 en Microsoft Teams, willen meestal Azure AD gebruiken voor centraal beheer van gebruikersreferenties voor een beveiligde en naadloze aanmeldingservaring in alle toepassingen. Als u de Azure AD-verificatie wilt gebruiken voor Commerce POS, moet u Azure AD eerst configureren als de verificatiemethode in Commerce Headquarters.

## <a name="configure-pos-authentication-method"></a>Methode voor configureren van POS-verificatie

Volg deze stappen om de POS-verificatiemethode te configureren in Commerce Headquarters.
    
1. Ga naar **Detailhandel en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen** en selecteer het functionaliteitsprofiel dat u wilt wijzigen.
1. Selecteer in de sectie **Aanmelding POS-personeel** van het sneltabblad **Functies** de gewenste optie voor de verificatiemethode voor aanmelding in de vervolgkeuzelijst **Verificatiemethode bij aanmelding**.

    De **verificatiemethode bij aanmelding** heeft drie opties:
    
    - **Personeels-id en wachtwoord**: Dit is de standaardoptie. POS-gebruikers moeten hierbij een personeels-id en wachtwoord invoeren om zich aan te melden bij het POS en voor toegang tot functies voor overschrijving door de beheerder.
    - **Azure AD zonder eenmalige aanmelding**: Voor deze optie moeten POS-gebruikers Azure AD-referenties gebruiken om zich aan te melden bij het POS en voor toegang tot de functionaliteit voor overschrijving door de beheerder. Wanneer de POS-client wordt vernieuwd of opnieuw wordt geopend, moet de POS-gebruiker Azure AD-referenties opgeven om zich opnieuw aan te melden.
    - **Azure AD met eenmalige aanmelding**: Wanneer deze optie is geselecteerd, kunnen POS-gebruikers zich aanmelden bij Cloud POS (CPOS) met actieve Azure AD-referenties die worden gebruikt door andere webtoepassingen in dezelfde webbrowser of zich aanmelden bij Modern POS (MPOS) met behulp van Azure AD-referenties waarmee bij Windows is aangemeld. Met beide methoden kunt u zich aanmelden zonder dat u Azure AD-referenties moet invoeren op het POS-aanmeldingsscherm. Voor het gebruik van de functionaliteit van voor overschrijving door de POS-beheerder moet u zich nog steeds aanmelden met Azure AD-referenties.

1. Ga naar **Retail en Commerce > IT Retail en Commerce > Distributieplanning** en voer de taak **1070 (Kanaalconfiguratie)** uit om de nieuwste functionaliteitsprofielinstellingen te synchroniseren met POS-clients.

> [!NOTE]
> - De optie voor de verificatiemethode **Azure AD zonder eenmalige aanmelding** vervangt de optie **Azure Active Directory** in de Commerce-versie 10.0.18 en eerder.
> - Voor Azure AD-verificatie is een actieve internetverbinding vereist en deze methode kan niet worden gebruikt als het POS offline is.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Azure AD-accounts koppelen aan POS-gebruikers

Als u Azure AD wilt gebruiken als de POS-verificatiemethode, moet u Azure AD-accounts koppelen aan POS-gebruikers in Commerce Headquarters. 

Volg deze stappen om Azure AD-accounts te koppelen aan POS-gebruikers in Commerce Headquarters.
    
1. Ga naar **Retail en Commerce > Werknemers > Medewerkers** en open een medewerkersrecord.
1. Selecteer in het actievenster op het tabblad **Commerce**, onder **Externe identiteit** de optie **Bestaande identiteit koppelen**. 
1. Selecteer in het dialoogvenster **Bestaande externe identiteit gebruiken** de optie **Zoeken met behulp van e-mail**, voer een Azure AD-e-mailadres in en selecteer **Zoeken**.
1. Selecteer de Azure AD- account die wordt geretourneerd en klik op **OK**.

Nadat u de bovenstaande configuratiestappen hebt uitgevoerd, worden de velden **Alias**, **UPN** en **Externe sub-id** op het tabblad **Commerce** van de pagina met werknemersgegevens ingevuld.

U moet de taak **1060 (Personeel)** uitvoeren in **Retail en Commerce > IT Retail en Commerce > Distributieplanning** om de nieuwste gegevens voor POS-gebruikers en Azure AD-accounts te synchroniseren met het kanaal.

> [!NOTE]
> Als best practice wordt het aangeraden om, nadat medewerkersgegevens zoals wachtwoord, POS-machtiging, gekoppelde Azure AD-account of adresboek van werknemers in Commerce Headquarters zijn bijgewerkt, de taak **1060 (Personeel)** uit te voeren om de meest recente medewerkersgegevens met het kanaal te synchroniseren. De POS-client kan dan de juiste gegevens ophalen voor gebruikersverificatie en verificatiecontroles.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>POS kassa vergrendelen en afmelden met Azure AD-verificatie

Het volgende gebeurt wanneer het POS is geconfigureerd voor gebruik van de Azure AD-verificatiemethode:

- De functie **Kassa vergrendelen** is niet beschikbaar in de POS-toepassing. 
- De functie **Automatisch vergrendelen** zal zich hetzelfde gedragen als de functie **Automatisch afmelden**.
- Als de POS-gebruiker **Afmelden** selecteert, wordt de gebruiker gevraagd zich de volgende keer dat het POS wordt gestart aan te melden met Azure AD-referenties, ongeacht of eenmalige aanmelding is ingeschakeld.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Functie Overschrijving door beheerder met Azure AD-verificatie

Wanneer het POS is geconfigureerd voor gebruik van Azure AD-verificatie, opent de functionaliteit voor het overschrijving door de beheerder een dialoogvenster geopend waarin wordt gevraagd om de Azure AD-referenties van de beheerdergebruiker. Nadat de aanmelding van de beheerder is goedgekeurd, worden de Azure AD-referenties van de beheerder niet meer gebruikt en worden de Azure AD-referenties van de vorige gebruiker gebruikt voor de volgende POS-bewerkingen.

> [!NOTE]
> - In Commerce, versies 10.0.18 en eerder, ondersteunt de functie voor overschrijving door de beheerder niet Azure AD. Een personeels-id en wachtwoord zijn vereist, zelfs als het POS is geconfigureerd om de Azure AD-verificatiemethode te gebruiken.
> - Wanneer u CPOS gebruikt met de browser Safari op een Apple iOS-apparaat, moet u eerst **Pop-ups blokkeren** in de instellingen van Safari uitschakelen, anders werkt de functionaliteit voor overschrijving door de beheerder niet met de Azure AD-verificatie. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Best practices voor beveiliging voor POS-verificatie op basis van Azure AD op gedeelde apparaten

Veel detailhandelaren configureren de winkelomgeving zodanig dat meerdere gebruikers toegang tot de POS-toepassing moeten hebben vanaf een gedeeld fysiek apparaat. In die context biedt eenmalige aanmelding een handige en naadloze verificatie-ervaring, maar kan het ook een beveiligingsrisico vormen als de huidige POS-gebruiker zich mogelijk niet realiseert dat de referenties van een andere gebruiker worden gebruikt om transacties of bewerkingen uit te voeren in het POS. Voordat u het POS configureert voor het gebruik van de Azure AD-verificatiemethode, wordt aangeraden om uw beveiligingsbeleid en de aanmeldingsinstellingen van het gedeelde apparaat te controleren om te bepalen welke optie het meest geschikt is.

- Als in uw detailhandelomgeving een gedeelde account wordt gebruikt (bijvoorbeeld een lokale account) voor aanmelding op een fysiek apparaat, wordt aangeraden om de optie **Azure AD zonder eenmalige aanmelding** te gebruiken. Op deze manier bent u er zeker van dat elke POS-gebruiker expliciet Azure AD-referenties opgeeft om zich aan te melden bij het POS.
- Als in uw detailhandelomgeving werknemers hun eigen Azure AD-accounts moeten gebruiken om zich aan te melden bij het POS en het fysieke apparaat waarop het draait, wordt aanbevolen om de optie **Azure AD met eenmalige aanmelding** te gebruiken.

## <a name="additional-resources"></a>Aanvullende bronnen

[ Een medewerker configureren](tasks/worker.md)

[Een functionaliteitsprofiel voor detailhandel maken](retail-functionality-profile.md)


[Uitgebreide aanmeldingsfunctionaliteit instellen voor MPOS en Cloud POS](extended-logon.md)

[Best practices voor beveiliging voor Cloud POS in gedeelde omgevingen](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

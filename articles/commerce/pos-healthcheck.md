---
title: Statuscontrole voor POS-randapparatuur en -services
description: Dit onderwerp geeft een overzicht van de statuscontrolebewerking in het verkooppunt (POS).
author: rubendel
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 37ec7d238b40c44891ff2a09a9db5a9265fb8321
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804352"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>Statuscontrole voor POS-randapparatuur en -services

[!include [banner](includes/banner.md)]

Dit onderwerp bevat een beschrijving van de statuscontrolebewerking in het verkooppunt (POS).

## <a name="overview"></a>Overzicht

Detailhandelwinkels kunnen complexe omgevingen zijn waarin veel toepassingen en apparaten worden gebruikt. Naarmate bewerkingen uitgebreider worden, kan het moeilijk worden om ervoor te zorgen dat de bewerkingen altijd probleemloos worden uitgevoerd, vanwege afhankelijkheden van bijvoorbeeld randapparatuur die gedurende een dag stuk kan gaan of onopzettelijk kan worden losgekoppeld. Het oplossen van problemen met betrekking tot apparaten en services kan kostbaar zijn voor grotere verkopers en even vervelend voor kleinere bedrijven.

Microsoft Dynamics 365 Commerce-versies 10.0.10 en hoger bevatten een statuscontrolebewerking die u kan helpen om enkele van deze kosten en frustraties te voorkomen. Deze bewerking biedt een methode om apparaten rechtstreeks vanuit het POS te bewerken buiten normale operaties. Hierdoor kunnen detailhandelaren problemen detecteren voordat ze zich voordoen.

## <a name="key-terms"></a>Belangrijke termen

| Voorwaarde | Omschrijving |
|---|---|
| Randapparaat | Elk apparaat dat door de POS-toepassing wordt gebruikt om transacties en andere bewerkingen in de winkel te faciliteren. Voorbeelden zijn kassalades, streepjescodescanners en betalingsterminals. |
| Service | In dit onderwerp is een service een hulptoepassing die de POS-toepassing nodig heeft voor het uitvoeren van transacties en dagelijkse bewerkingen. Voorbeelden zijn apps die helpen bij het berekenen van btw of verzending. |

## <a name="health-check-operation"></a>Statuscontrolebewerking

De statuscontrolebewerking is bewerking 717 op de pagina **POS-bewerkingen** in Commerce Headquarters. Deze kan worden gebruikt terwijl het POS zich in de niet-lademodus bevindt. Er moet echter een hardwarestation actief zijn.

Standaard worden met de statuscontrole alleen apparaten getest die in het hardwareprofiel zijn geconfigureerd voor het hardwarestation dat momenteel actief is voor een kassa. Als een kassa in de loop van een dag meerdere hardwarestations gebruikt om statuscontroles voor al deze hardwarestations uit te voeren, moet er met één hardwarestation tegelijk verbinding worden gemaakt. Er is geen statuscontrole op winkelniveau. Dit type controle kan echter wel worden uitgevoerd door middel van de uitbreidbaarheid van Commerce Server.

### <a name="out-of-box-health-checks"></a>Kant-en-klare statuscontroles

| Type | Verbinding | Details |
|---|---|---|
| Printer | OPOS | Met deze controle test u algemene objectkoppeling en -insluiting voor POS-functies (OPOS). Hieronder volgen een aantal voorbeelden:<ul><li>Openen: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sluiten: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Regelweergave | OPOS | Met deze controle test u algemene OPOS-functies. Hieronder volgen een aantal voorbeelden:<ul><li>Openen: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sluiten: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Twee schermen | Windows | Hiermee zorgt u ervoor dat het besturingssysteem een tweede Windows-scherm detecteert. | 
| MSR | OPOS | Met deze controle test u algemene OPOS-functies. Hieronder volgen een aantal voorbeelden:<ul><li>Openen: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sluiten: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Wisseluitschrijver | OPOS | Met deze controle test u algemene OPOS-functies. Hieronder volgen een aantal voorbeelden:<ul><li>Openen: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sluiten: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| Scanner | OPOS | Met deze controle test u algemene OPOS-functies. Hieronder volgen een aantal voorbeelden:<ul><li>Openen: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sluiten: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| Schaal | OPOS | Met deze controle test u algemene OPOS-functies. Hieronder volgen een aantal voorbeelden:<ul><li>Openen: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sluiten: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Pinapparaat | OPOS | Met deze controle test u algemene OPOS-functies. Hieronder volgen een aantal voorbeelden:<ul><li>Openen: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sluiten: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Betalingsterminal | Betalingen-SDK | Met deze controle test u algemene betalingsterminalfuncties die worden geleverd door Betalingen-SDK. <ul><li>Vergrendeld</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Afsluiten</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>De statuscontrolebewerking in het POS gebruiken

Wanneer de statuscontrolebewerking wordt gestart in het POS, worden in een deelvenster rechts de geconfigureerde apparaten weergegeven en wordt de status van elk apparaat weergegeven. Als u een statuscontrole wilt uitvoeren voor één apparaat, selecteert u het apparaat en selecteert u **Geselecteerde testen**. Selecteer **Alles testen** om een statuscontrole uit te voeren voor alle apparaten. Met de functie **Alles testen** kunt u alle apparaten één voor één testen en wordt de status van elk apparaat in de kolom **Status** bijgewerkt.

In de kolom **Laatste controle** wordt aangegeven wanneer de statuscontrole voor elk apparaat voor het laatst is uitgevoerd.

Bij een geslaagde statuscontrole van een apparaat (als er geen fouten zijn gevonden), is de status van het apparaat **OK**. Als de statuscontrole mislukt, geeft de status aan dat er een fout is opgetreden. In dit geval bevat het deelvenster rechts details over de fout of wordt de gebruiker gevraagd contact op te nemen met de systeembeheerder.

Sommige apparaten, zoals de OPOS-toetsenbordvergrendeling, hebben geen kant-en-klare controletests. Als geen test voor de statuscontrole wordt gedetecteerd voor een apparaat dat wordt gebruikt, wordt de status **Niet ondersteund** weergegeven.

### <a name="extending-health-checks"></a>Statuscontroles uitbreiden

De kant-en-klare controletests zijn geconfigureerd om enkele gebruikersvriendelijke berichten voor veelvoorkomende fouten te bieden. Niet alle scenario's worden echter gedekt. Via uitbreid baarheid kunnen verkopers gebruikersvriendelijke berichten toewijzen aan fouten die mogelijk specifiek zijn voor hun omgeving.

Er kunnen ook aangepaste statuscontroles worden gemaakt om apparaten te testen die niet standaard worden ondersteund of om de services te testen waarvan het POS afhankelijk is.

## <a name="related-articles"></a>Gerelateerde artikelen

[MPOS-triggers (Modern POS) en afdrukken](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
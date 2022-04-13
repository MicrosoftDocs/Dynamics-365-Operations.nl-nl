---
title: De uitgebreide aanmeldingsfunctie instellen en gebruiken
description: In dit onderwerp wordt beschreven hoe u de uitgebreide aanmeldingsmogelijkheid van de Microsoft Dynamics 365 Commerce POS-toepassing kunt instellen en gebruiken.
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d211ecfe1550f6093e1d35e7c2b37c036b50dd4a
ms.sourcegitcommit: 5aebb181004eb63210503fb566dcda5c55032bee
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/29/2022
ms.locfileid: "8491434"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>De uitgebreide aanmeldingsfunctie instellen en gebruiken

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de uitgebreide aanmeldingsmogelijkheid van de Microsoft Dynamics 365 Commerce POS-toepassing kunt instellen en gebruiken.

Cloud POS (CPOS) en Modern POS (MPOS) bieden een uitgebreide aanmeldingsmogelijkheid waarin detailhandelmedewerkers zich kunnen aanmelden bij de POS-toepassing door een streepjescode te scannen of een kaart door de lezer te halen met behulp van een magneetstriplezer (MSR).

## <a name="set-up-extended-logon"></a>Uitgebreide aanmelding instellen

Als u uitgebreide aanmelding voor POS-kassa's in een detailhandelwinkel wilt instellen, gaat u als volgt te werk.

1. Ga in Commerce Headquarters naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**. 
2. Selecteer in het linkernavigatievenster het functionaliteitsprofiel dat aan de detailhandelwinkel is gekoppeld.
3. Stel op het sneltabblad **Functies** onder **Aanvullende opties voor aanmeldingsverificatie** de volgende opties in op **Ja** of **Nee**:

    - **Personeel aanmelden met streepjescode**: stel deze optie in op **Ja** als u wilt dat uw werknemers zich aanmelden bij het POS door een streepjescode te scannen. 
    - **Voor het aanmelden van personeel met een streepjescode is een wachtwoord vereist**: stel deze optie in op **Ja** als u wilt dat uw werknemers een wachtwoord invoeren tijdens aanmelding bij het POS door een streepjescode te scannen.
    - **Personeel aanmelden met kaart**: stel deze optie in op **Ja** als u wilt dat uw werknemers zich aanmelden bij het POS door een kaart door een lezer te halen.
    - **Voor het aanmelden van personeel met een kaart is een wachtwoord vereist**: stel deze optie in op **Ja** als u wilt dat uw werknemers een wachtwoord invoeren tijdens aanmelding bij het POS door een kaart door de lezer te halen.

De streepjescode of kaart is gekoppeld aan referenties die aan een werknemer kunnen worden toegewezen. De referenties moeten minimaal zes tekens bevatten. De tekenreeks die de eerste vijf tekens bevat, moet uniek zijn en wordt beschouwd als een *referentie-id* die wordt gebruikt om een werknemer op te zoeken. De resterende tekens worden gebruikt voor beveiligingsverificatie. U hebt bijvoorbeeld twee kaarten, waarvan er één de referenties 12345DAJDEYTDW heeft en de ander de referenties 12345STUKUTBDAJH. Omdat deze twee kaarten dezelfde referentie-id 12345 hebben, kunnen ze niet beide aan werknemers worden toegewezen.

## <a name="assign-extended-logon"></a>Uitgebreide aanmelding toewijzen

Standaard kunnen alleen managers uitgebreide aanmelding aan werknemers toewijzen. Als u uitgebreide aanmelding wilt toewijzen, gaat u naar **Uitgebreid aanmelden** in POS. Zoek vervolgens naar een werknemer door diens operator-id in het zoekveld in te voeren. Selecteer de werknemer en klik vervolgens op **Toewijzen**. Op de volgende pagina haalt u de uitgebreide aanmelding door of scant u deze om de werknemer toe te wijzen. Als het doorhalen of scannen met succes is gelezen, wordt de knop **OK** beschikbaar. Klik op **OK** om de uitgebreide aanmelding voor die werknemer op te slaan.

## <a name="delete-extended-logon"></a>Uitgebreide aanmelding verwijderen

U kunt de uitgebreide aanmelding die aan een werknemer is toegewezen verwijderen door te zoeken naar de werknemer met de bewerking **Uitgebreide aanmelding**. Selecteer de werknemer en klik vervolgens op **Verwijderen**. Alle uitgebreide aanmeldreferenties die zijn gekoppeld aan die werknemer, worden verwijderd.

## <a name="use-extended-logon"></a>Uitgebreide aanmelding gebruiken

Nadat de uitgebreide aanmelding is geconfigureerd, en een werknemer een streepjescode of een magneetstrip is toegewezen aan een werknemer, hoeft de werknemer alleen zijn of haar kaart door de lezer te halen wanneer de POS-aanmeldingspagina wordt weergegeven. Als een wachtwoord ook vereist is voordat aanmelding kan doorgaan, wordt de werknemer gevraagd zijn of haar wachtwoord in te voeren.

## <a name="extend-extended-logon"></a>Uitgebreide aanmelding uitbreiden

Voor de kant-en-klare implementatie van de uitgebreide aanmeldingsmogelijkheid moeten referenties minimaal zes tekens lang zijn en moeten de eerste vijf tekens (de referentie-id) uniek zijn. Het was oorspronkelijk bedoeld als voorbeeld dat ontwikkelaars konden aanpassen om aan de vereisten van een specifieke implementatie te voldoen. (Het kan bijvoorbeeld worden aangepast om meer tekens te ondersteunen of om verschillende beveiligingsverificatieregels te gebruiken.) Zie [De uitgebreide aanmeldingsfunctionaliteit voor MPOS en Cloud POS uitbreiden](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/) voor gedetailleerde informatie over het bouwen van uitbreidingen voor uitgebreide aanmelding.

De aanmeldingsservice kan ook worden uitgebreid om extra aanmeldingsapparaten, zoals uitgebreide palmscanners te ondersteunen. Zie de [documentatie van POS-uitbreidbaarheid](dev-itpro/pos-extension/pos-extension-overview.md) voor meer informatie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

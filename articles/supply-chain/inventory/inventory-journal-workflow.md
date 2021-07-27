---
title: Goedkeuringswerkstromen voor voorraadjournalen
description: In dit onderwerp wordt beschreven hoe u goedkeuringswerkstromen voor voorraadjournalen instelt en gebruikt voor diverse typen fysieke voorraadtransacties. Met voorraadjournaalwerkstromen kunt u ervoor zorgen dat alleen goedgekeurde voorraadjournalen naar transacties kunnen worden geboekt.
author: sherry-zheng
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bcb242214efab3fd632ea0b9e0f3329bb7821dc0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354756"
---
# <a name="inventory-journal-approval-workflows"></a>Goedkeuringswerkstromen voor voorraadjournalen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u goedkeuringswerkstromen voor voorraadjournalen instelt en gebruikt voor verschillende typen fysieke voorraadtransacties, zoals uitgiften en ontvangsten, voorraadmutaties, stuklijsten (BOM's) en de afstemming van fysieke voorraad. Met voorraadjournaalwerkstromen kunt u ervoor zorgen dat alleen goedgekeurde voorraadjournalen naar transacties kunnen worden geboekt.

> [!NOTE]
> Goedkeuringswerkstromen voor voorraadjournalen zijn alleen van toepassing op transacties die zijn vastgelegd in de module Voorraadbeheer. Ze werken niet met voorraadjournalen die vanuit de module Magazijnbeheer zijn geactiveerd.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>De functie Goedkeuringswerkstromen voor voorraadjournalen inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Voorraad- en magazijnbeheer*
- **Functienaam:** *Goedkeuringswerkstroom voor voorraadjournaal*

## <a name="create-your-inventory-journal-approval-workflows"></a>Uw goedkeuringswerkstromen voor voorraadjournalen maken

Als u deze functie wilt instellen, moet u een werkstroom maken voor elk van de voorraadjournaaltypen die u wilt beheren. Aangezien verschillende voorraadjournaaltypen verschillende goedkeuringshiërarchieën en werkstroomstappen kunnen hebben, kunt u afzonderlijke werkstromen voor elk voorraadjournaaltype configureren.

Deze werkstromen ondersteunen versiebeheer en elk heeft een werkstroom-id en een actieve versie. U kunt ervoor kiezen om elke nieuwe werkstroomversie direct na het maken te activeren of deze versie inactief te houden. Als u verschillende werkstromen nodig hebt voor hetzelfde journaaltype, maakt u vervolgens meerdere werkstromen voor dat journaaltype en wijst u deze vervolgens toe aan een andere journaalnaam die dat type gebruikt.

Uw goedkeuringswerkstromen voor voorraadjournalen maken:

1. Ga naar **Voorraadbeheer \> Instellen\> Voorraadbeheerwerkstromen**.
1. Selecteer **Nieuw** in het actievenster.
1. Het type voorraadjournaal kiezen waarvoor u een werkstroom wilt instellen:
    - **Journaal voor voorraadlabeltelling**
    - **Journaal voor wijzigingen aan voorraadeigendom**
    - **Voorraadmutatiejournaal**
    - **Voorraadoverboekingsjournaal**
    - **Voorraadtellingsjournaal**
    - **Voorraadstuklijstjournaal**
    - **Voorraadcorrectiejournaal**

    ![Het dialoogvenster Werkstroom maken.](media/journal-workflow-create-workflow.png "Het dialoogvenster Werkstroom maken")

1. De werkstroomeditor-app wordt gestart op uw computer. (Mogelijk wordt u gevraagd deze actie goed te keuren.) Gebruik de editor om de werkstroom zo nodig te ontwerpen. Zie het [Overzicht van Werkstroomsysteem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) voor meer informatie over het gebruik van de werkstroomeditor.
1. Nadat u de werkstroomeditor hebt opgeslagen en gesloten, moet u kiezen of u deze werkstroomversie wilt activeren of dat u deze inactief wilt houden.

> [!NOTE]
> Werkstromen bieden versiebeheer, wat betekent dat u een lijst met versies kunt bekijken die u hebt gemaakt en kunt kiezen welk van deze versies actief is. Als u de lijst met beschikbare versies wilt weergeven en kiezen welke u wilt activeren, selecteert u een werkstroom die wordt vermeld op de pagina **Voorraadbeheerwerkstromen**. Open in het actievenster het tabblad **Werkstroom** en selecteer **Versies**. Voor elke werkstroom-id kan slechts één versie tegelijk actief zijn.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Goedkeuringswerkstromen toewijzen aan voorraadjournaalnamen

De volgende stap is het toewijzen van een voorraadjournaalwerkstroom aan elke voorraadjournaalnaam. Voor elk voorraadjournaaltype kunt u meerdere voorraadjournaalnamen instellen.

Een voorraadjournaalwerkstroom koppelen aan een voorraadjournaalnaam:

1. Ga naar **Voorraadbeheer \> Instellen \> Journaalnamen \> Voorraad**.
1. Selecteer een journaalnaam in de lijstkolom om de bijbehorende instellingenpagina te openen.
1. Stel op het sneltabblad **Algemeen** de optie **Goedkeuringsworkflow** in op **Ja**. Selecteer **Ja** als u wordt gevraagd de actie goed te keuren.

    ![Een werkstroom aan een journaalnaam toewijzen.](media/journal-workflow-journal-name.png "Een werkstroom aan een journaalnaam toewijzen")

1. Open de vervolgkeuzelijst **Werkstroom** en selecteer de juiste werkstroom. In de lijst staan alle actieve werkstromen die u hebt gemaakt met de werkstroomeditor-app.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Een voorraadjournaal maken en ter goedkeuring verzenden

Nadat u een voorraadjournaalnaam hebt gekoppeld aan de goedkeuringswerkstroom voor voorraadjournalen, kunt u nieuwe voorraadjournalen maken die deze naam gebruiken en deze journalen vervolgens verzenden voor goedkeuring met die werkstroom. U kunt het voorraadjournaal pas boeken nadat het is goedgekeurd door de fiatteurs die in de werkstroom zijn geconfigureerd.

1. Vouw in het navigatiedeelvenster **Voorraadbeheer \> Journaalposten \> Artikelen** uit en selecteer vervolgens een voorraadjournaaltype.
1. Selecteer **Nieuw** om een nieuw journaal van het geselecteerde type te maken.
1. Het dialoogvenster **Voorraadjournaal maken** wordt geopend. Vul het formulier naar behoefte in en selecteer **OK** om het journaal op te slaan.
1. Vul zo nodig het journaal in.
1. Wanneer u een voorraadjournaal maakt of opent waaraan een goedkeuringswerkstroom is gekoppeld, wordt de knop **Werkstroom** actief in het actievenster. Wanneer u klaar bent om het journaal voor goedkeuring in te dienen, selecteert u de knop **Werkstroom** om een vervolgkeuzelijst te openen en selecteert u vervolgens **Indienen**. Het goedkeuringsverzoek wordt vervolgens doorgestuurd naar de relevante fiatteur, die wordt gewaarschuwd met behulp van de meldingsmethode die voor de werkstroom is geconfigureerd.

    ![Een journaal ter goedkeuring indienen.](media/journal-workflow-inventory-journal.png "Een journaal ter goedkeuring indienen")

Als u een goedkeuringsaanvraag wilt intrekken, opent u het betreffende journaal, selecteert u de knop **Werkstroom** en selecteert u vervolgens **Intrekken**. Hierdoor wordt de werkstroom opnieuw ingesteld.

Wanneer het journaal is goedgekeurd, kunt u het boeken. Als u het journaal wilt boeken, selecteert u **Boeken** vanuit het actievenster. Als de knop **Boeken** niet actief is, is het journaal nog niet goedgekeurd.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Reageren op een aanvraag voor een goedkeuring van een voorraadjournaal

Als u een fiatteur bent, ontvangt u een bericht telkens wanneer uw goedkeuring nodig is (zoals geconfigureerd in de desbetreffende werkstroom). Vervolgens kunt u een journaalgoedkeuringsaanvraag goedkeuren of afwijzen door het volgende te doen:

1. Vouw in het navigatiedeelvenster **Voorraadbeheer \> Journaalposten \> Artikelen** uit en selecteer vervolgens een voorraadjournaaltype.
1. Open het betreffende journaal en controleer dit.
1. Selecteer de knop **Werkstroom** in het actievenster om een vervolgdialoogvenster te openen. Selecteer een van de volgende:
    - **Goedkeuren**: de aanvraag goedkeuren.
    - **Afkeuren**: de aanvraag weigeren.
    - **Meer \> Wijziging aanvraag**: een bericht verzenden naar de aanvrager om te vragen een specifieke wijziging aan te brengen en vervolgens opnieuw indienen.
    - **Meer \> Delegeren**: de goedkeuring delegeren aan een andere gebruiker.
    - **Meer \> Intrekken** : de goedkeuringsaanvraag intrekken (de werkstroom wordt opnieuw ingesteld).
    - **Meer \> Workflowhistorie**: de historie bekijken van deze goedkeuringswerkstroom tot nu toe.

## <a name="review-the-approval-history"></a>De goedkeuringshistorie controleren

Net als bij andere typen werkstromen kunt u de pagina **Werkstroomgeschiedenis** gebruiken om de historie van de werkstroomgoedkeuring voor elk journaal weer te geven.

De werkstroomhistorie voor een journaal controleren:

1. Vouw in het navigatiedeelvenster **Voorraadbeheer \> Journaalposten \> Artikelen** uit en selecteer vervolgens een voorraadjournaaltype.
1. Open het relevante journaal.
1. Selecteer de knop **Werkstroom** in het actievenster om een vervolgdialoogvenster te openen. Selecteer **Workflowhistorie**. Zie voor meer informatie [Werkstroomhistorie bekijken](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
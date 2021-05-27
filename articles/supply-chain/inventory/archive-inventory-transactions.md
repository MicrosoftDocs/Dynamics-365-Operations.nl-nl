---
title: Voorraadtransacties archiveren
description: In dit onderwerp wordt beschreven hoe u voorraadtransactiegegevens archiveert om de systeemprestaties te verbeteren.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8b61e65d3a641a1e3d73192853c832d57ed17401
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021263"
---
# <a name="archive-inventory-transactions"></a>Voorraadtransacties archiveren

[!include [banner](../../includes/banner.md)]

In de loop der tijd zal de tabel met voorraadtransacties (`InventTrans`) groter worden en meer databaseruimte verbruiken. Daarom worden query's voor de tabel steeds trager. In dit onderwerp wordt beschreven hoe u *de archieffunctie voor voorraadtransacties* kunt gebruiken om gegevens over voorraadtransacties te archiveren om de systeemprestaties te verbeteren.

> [!NOTE]
> Alleen financieel bijgewerkte voorraadtransacties kunnen in een geselecteerde afgesloten grootboekperiode worden gearchiveerd. Voor archivering moeten financieel bijgewerkte uitgaande voorraadtransacties de uitgiftestatus *Verkocht* hebben en moeten inkomende voorraadtransacties de ontvangststatus *Ingekocht* hebben.

Wanneer u voorraadtransacties archiveert, worden alle gerelateerde transacties naar de tabel `InventTransArchive` verplaatst. Voorraaduitgiftetransacties en voorraadontvangsttransacties worden afzonderlijk gearchiveerd op basis van de combinatie van de artikel-ID (`itemId`) en de voorraaddimensie-ID (`inventDimId`), en ze worden in de samengevatte uitgifte- en samengevatte ontvangsttransacties geplaatst.

Als een combinatie van `itemId` en `inventDimId` slechts één ontvangst- of uitgiftetransactie bevat, wordt de transactie niet gearchiveerd.

## <a name="turn-on-the-feature-in-your-system"></a>De functie inschakelen in uw systeem

Als de functies die in dit onderwerp worden beschreven, nog niet in het systeem aanwezig zijn, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de *archieffunctie voorraadtransacties* in. Deze functie kan niet meer worden uitgeschakeld nadat deze is ingeschakeld.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Waar u rekening mee moet worden houden voordat u voorraadtransacties archiveert

Voordat u voorraadtransacties archiveert, moet u rekening houden met de volgende zakelijke scenario's, omdat deze gevolgen zullen hebben van de bewerking:

- Wanneer u voorraadtransacties controleert uit gerelateerde documenten, zoals inkooporderregels, worden ze weergegeven als gearchiveerd. Als u de gearchiveerde transacties wilt controleren, gaat u naar **Voorraadbeheer \> Periodieke taken \> Opschonen \> Archief voorraadtransacties**.
- Voorraadsluiting kan niet worden geannuleerd voor gearchiveerde perioden. Voordat u een voorraadsluiting kunt annuleren, moet u het voorraadtransactiearchief voor de relevante periode terugdraaien.
- Standaardkostenconversie kan niet worden uitgevoerd voor gearchiveerde perioden. Voordat u een standaardkostenconversie kunt uitvoeren, moet u het voorraadtransactiearchief voor de relevante periode terugdraaien.
- Wanneer u voorraadtransacties archiveert, heeft dit gevolgen voor voorraadrapporten die afkomstig zijn uit voorraadtransacties. Deze rapporten omvatten het naar ouderdom gerangschikt voorraadrapport en voorraadwaarderapporten.
- Dit kan gevolgen hebben voor voorraadprognoses als deze worden uitgevoerd gedurende de periode van gearchiveerde perioden.

## <a name="prerequisites"></a>Vereisten

Voorraadtransacties kunnen alleen worden gearchiveerd tijdens perioden waarin aan de volgende voorwaarden is voldaan:

- De grootboekperiode moet zijn afgesloten.
- Voorraadsluiting moet worden uitgevoerd op of na de tot-datum van het archief.
- De periode moet ten minste één jaar vóór de beginperiodedatum van het archief liggen.
- Er mogen geen bestaande voorraadherberekeningen zijn.

## <a name="archive-inventory-transactions"></a>Voorraadtransacties archiveren

Voer de volgende stappen uit om voorraadtransacties te archiveren.

1. Ga naar **Voorraadbeheer** \> **Periodieke taken** \> **Opschonen** \> **Voorraadtransactiearchief**.

    De pagina **Voorraadtransactiearchief** verschijnt en toont een lijst met gearchiveerde procesrecords.

    ![Pagina Voorraadtransactiearchief](media/archive-inventory-empty.png "Pagina Voorraadtransactiearchief")

1. Selecteer in het actievenster **Voorraadtransactiearchief** om een voorraadtransactiearchief te maken.
1. Stel in het dialoogvenster **Voorraadtransactiearchief** op het sneltabblad **Parameters** de volgende velden in:

    - **Begindatum in afgesloten grootboekperiode** – selecteer de eerste transactiedatum die u in het archief wilt opnemen.
    - **Einddatum in afgesloten grootboekperiode** – selecteer de laatste transactiedatum die u in het archief wilt opnemen.

    ![Dialoogvenster Voorraadtransactiearchief](media/archive-inventory-dates.png "Dialoogvenster Voorraadtransactiearchief")

    > [!NOTE]
    > Alleen perioden die aan [de vereisten](#prerequisites) voldoen, kunnen worden geselecteerd.

1. Stel batchverwerkingsdetails in op het sneltabblad **Uitvoeren op de achtergrond**. Volg de gebruikelijke stappen voor batchtaken in Microsoft Dynamics 365 Supply Chain Management.
1. Selecteer **OK**.
1. Er wordt een bericht weergegeven waarin u wordt gevraagd te bevestigen dat u wilt doorgaan. Lees het bericht zorgvuldig en selecteer **Ja** als u wilt doorgaan.

    U ontvangt een bericht waarin wordt gemeld dat de archieftaak voor uw voorraadtransacties is toegevoegd aan de batchwachtrij. Met de taak worden nu voorraadtransacties uit de geselecteerde periode gearchiveerd.

## <a name="view-archived-inventory-transactions"></a>Gearchiveerde voorraadtransacties weergeven

Op de pagina **Voorraadtransactiearchief** wordt uw volledige archiveringshistorie weergegeven. Elke rij in het raster geeft informatie weer, zoals de datum waarop het archief is gemaakt, de gebruiker die het heeft gemaakt en de status.

![Archiefgeschiedenis op de pagina Voorraadtransactiearchief](media/archive-inventory-full.png "Archiefgeschiedenis op de pagina Voorraadtransactiearchief")

Selecteer een van de volgende waarden in de vervolgkeuzelijst boven aan de pagina om de archieven te filteren die in het raster worden weergegeven:

- **Actief:** alleen actieve archieven, niet teruggedraaide archieven, tonen.
- **Alle** – Alle archieven, zowel actief als teruggedraaid, tonen.

Voor elk archief in het raster wordt de volgende informatie geleverd:

- **Actief:** een vinkje geeft aan dat het archief actief is.
- **Vanaf-datum:** de datum van de oudste transactie die in het archief kan worden opgenomen.
- **Tot-datum:** de datum van de laatste transactie die in het archief kan worden opgenomen.
- **Gepland door** – De gebruikersaccount die het archief heeft gemaakt.
- **Uitgevoerd** – De datum waarop het archief is gemaakt.
- **Omkeren:** een vinkje geeft aan dat het archief is teruggedraaid.
- **Huidige update stoppen** – Een vinkje geeft aan dat het archief in uitvoering is, maar dat dit is onderbroken.
- **Status:** de verwerkingsstatus van het archief. De mogelijke waarden zijn *In afwachting*, *In uitvoering* en *Gereed*.

De werkbalk boven het raster bevat de volgende knoppen die u kunt gebruiken om met een geselecteerd archief te werken:

- **Gearchiveerde transacties** – Alle details van het geselecteerde archief weergeven. Op **de pagina Gearchiveerde transacties** die verschijnt, worden alle transacties in het archief weergegeven.

    ![Pagina Gearchiveerde transacties](media/archive-inventory-transactions.png "Pagina Gearchiveerde transacties")

    Als u meer informatie over een specifieke transactie op de pagina **Gearchiveerde transacties** wilt weergeven, selecteert u deze in het raster en selecteert u vervolgens in het actievenster **Details gearchiveerde transacties**. Op de pagina **Details gearchiveerde transactie** wordt informatie weergegeven, zoals de boeking in het grootboek, gerelateerde verwijzingen in de subadministratie en financiële dimensies.

- **Archivering onderbreken** – Een geselecteerd archief onderbreken dat momenteel wordt verwerkt. De pauze wordt pas van kracht nadat de archiveringstaak is gegenereerd. Het kan dus even duren voordat de pauze van kracht wordt. Als een archief is onderbroken, wordt er een vinkje weergegeven in het veld **Huidige update stoppen**.
- **Archivering hervatten** – Verwerking hervatten voor een geselecteerd archief dat momenteel is onderbroken.
- **Omkeren**: het geselecteerde archief terugdraaien. U kunt een archief alleen terugdraaien als het veld **Status** is ingesteld op *Voltooid*. Als een archief is teruggedraaid, wordt er een vinkje weergegeven in het veld **Omkeren**.

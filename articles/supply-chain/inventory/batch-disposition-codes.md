---
title: Batchbeschikkingscodes gebruiken om batches als beschikbaar of niet-beschikbaar te markeren
description: In dit artikel wordt beschreven hoe u batchbeschikkingscodes kunt instellen en gebruiken om batches te markeren als beschikbaar of niet beschikbaar voor gebruik in hoofdplanning, reservering, orderverzameling en/of verzending.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542467"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Batchbeschikkingscodes gebruiken om batches als beschikbaar of niet-beschikbaar te markeren

In dit artikel wordt beschreven hoe elke verbetering in wordt gesteld en hoe *batchbeschikkingscodes* gebruikt kunnen worden. Elke batchbeschikkingscode heeft de status *Beschikbaar* of *Niet beschikbaar*. U wijst batchbeschikkingscodes toe aan voorraadbatches om aan te geven of elke batch beschikbaar is voor hoofdplanning, reservering, orderverzameling en/of verzenden.

Als u batchbeschikkingscodes wilt gebruiken, moet u de codes instellen en deze toewijzen aan de batches die u wilt beheren.

## <a name="set-up-batch-disposition-codes"></a>Batchbeschikkingscodes instellen

U moet elke batchbeschikkingscode die u wilt gebruiken, instellen in het systeem. U kunt zoveel codes maken als u wilt. (U kunt bijvoorbeeld codes maken om de verschillende redenen aan te geven waarom een batch al dan niet beschikbaar is). U hebt echter meestal slechts twee codes: een voor *beschikbaar* en een voor *niet beschikbaar*. U kunt ook aangepaste codes maken waarmee een batch voor sommige bewerkingen kan worden gebruikt, maar voor andere niet.

Voer de volgende stappen uit om batchbeschikkingscodes in te stellen.

1. Ga naar **Voorraadbeheer \> Instellingen \> Batch \> Hoofdbatchbeschikking**.
1. Op de pagina **Hoofdbatchbeschikking** worden de huidige batchbeschikkingscodes weergegeven. U kunt deze codes ook maken, verwijderen en bewerken. Volg één van deze stappen:

    - Als u een bestaande code wilt bewerken, selecteert u deze in het lijstvenster.
    - Selecteer in het actievenster **Nieuw** om een nieuwe code te maken.

1. Stel in de koptekst van de nieuwe of geselecteerde code de volgende velden in:

    - **Batchbeschikkingscode** – geef de weergavenaam voor de code op.
    - **Beschrijving** – Omschrijf hoe de aangepaste code moet worden gebruikt.
    - **Batchbeschikkingsstatus**: selecteer de status die van toepassing is op batches waar de code aan is toegewezen:

        - *Niet beschikbaar*: de batches kunnen niet worden gebruikt voor hoofdplanning, reservering, orderverzameling en verzenden. Wanneer u deze waarde selecteert, worden alle opties **Blokkeren** op het sneltabblad **Instellen** ingesteld op *Ja*, en alle opties **Nettobehoeften** ingesteld op *Nee*. U kunt echter enkele van deze instellingen wijzigen om uitzonderingen toe te voegen.
        - *Beschikbaar*: de batches kunnen niet worden gebruikt voor hoofdplanning, reservering, orderverzameling en/of verzenden. Wanneer u deze waarde selecteert, worden alle opties voor **Blokkeren** op het sneltabblad **Instellen** ingesteld op *Ja*, en alle opties **Nettobehoeften** ingesteld op *Nee*. Deze instellingen zijn alleen-lezen, terwijl het veld **Batchbeschikkingsstatus** is ingesteld op *Beschikbaar*.

1. Als u het veld **Batchbeschikkingsstatus** instelt op *Niet beschikbaar*, kunt u de blokstatus van elke bewerking (reserveren, orderverzameling en verzenden) voor elk type order (verkoop, transfer en productie) aanpassen. Voor productieorders kunt u ervoor kiezen het productieverzameljournaal blokkeren of te deblokkeren. U kunt hoofdplanning ook blokkeren of de blokkering opheffen. Gebruik de opties op het sneltabblad **Instellingen** om naar gewenst elke bewerking te blokkeren of te deblokkeren. Stel de optie **Nettobehoeften** in op *Ja* om de hoofdplanning in te schakelen of stel de *optie Nee* in om de hoofdplanning te blokkeren.

## <a name="assign-batch-disposition-codes-to-batches"></a>Batchbeschikkingscodes toewijzen aan batches

Nadat u de batchbeschikkingscodes hebt gemaakt die u nodig hebt, gaat u als volgt te werk om de beschikkingscodes toe te wijzen aan batches.

1. Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> Batches**.
1. Een of meer batches selecteren om een batchbeschikkingscode aan toe te wijzen.
1. Selecteer op het tabblad **Opnieuw instellen** in het actiepaneel de optie **Batchbeschikkingscode opnieuw instellen**.
1. Stel in dialoogvenster **Beperkingen voor de voorraadbatch wijzigen** het veld **Nieuwe batchbeschikkingscode** in op de naam van de code die u wilt toewijzen.
1. Selecteer **OK** om de nieuwe instelling toe te passen en sla uw wijziging op.

    Op de pagina **Batches** worden de waarden in de **Batchbeschikkingscode** en de kolommen **Batchbeschikkingsstatus** bijgewerkt, zodat ze de nieuwe instellingen voor de geselecteerde batches weergeven.

## <a name="master-planning-example"></a>Voorbeeld Hoofdplanning

In dit voorbeeld kunt u zien hoe batchbeschikkingscodes van invloed kunnen zijn op de hoofdplanning.

In dit voorbeeld worden batchbeschikkingscodes als volgt ingesteld:

- *P-Beschikbaar:*

    - **Batchbeschikkingsstatus:** *Beschikbaar*
    - **Nettobehoeften:** *Ja*

- *P-Niet beschikbaar:*

    - **Batchbeschikkingsstatus:** *Niet beschikbaar*
    - **Nettobehoeften:** *Nee*

Er is een product (*Product-1*) met twee batches: *Batch-A* en *Batch-B*. Deze batches worden als volgt ingesteld:

- *Batch-A:*

    - **Batchbeschikkingscode:** *P-Beschikbaar*
    - **Voorhanden hoeveelheid** 1

- *Batch-B:*

    - **Batchbeschikkingscode:** *P-Niet beschikbaar*
    - **Voorhanden hoeveelheid** 1

Er is een verkooporder (*VO1*) voor 2 producten van *Product-1*. De leveringsdatum is drie dagen na vandaag.

U kunt de hoofdplanning uitvoeren en de volgende waarden instellen die relevant zijn voor dit voorbeeld:

- **Geplande inkooporder:** *Inkooporder*
- **Aanvullingsstrategie:** *Vereiste*
- **Levertijd:** *0*

Als gevolg van de planningsrun wordt de beschikbare batch (*Batch-A*) gebruikt om een hoeveelheid van 1 product *Product-1* voor verkooporder *VO1* te dekken. *Batch-B* kan echter niet worden gebruikt, omdat deze batch is gemarkeerd als niet beschikbaar voor planning. Daarom wordt voor de resterende hoeveelheid een geplande inkooporder (*PPO1*) gemaakt voor een nieuwe batch van product *Product-1*.

In de volgende afbeelding wordt de tijdlijn voor het planningsresultaat weergegeven.

![Voorbeeld geeft weer hoe batchbeschikkingscodes van invloed kunnen zijn op de hoofdplanning.](media/batch-codes-planning-example.png "Voorbeeld geeft weer hoe batchbeschikkingscodes van invloed kunnen zijn op de hoofdplanning")

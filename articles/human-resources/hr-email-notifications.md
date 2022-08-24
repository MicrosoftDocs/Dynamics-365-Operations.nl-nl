---
title: E-mailmelding voor vergoedingen
description: In dit artikel vindt u een overzicht van de functie E-mailmeldingen voor vergoedingenbeheer in Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d550cbb2f639535dbb43765c9fb0632a514fbe8c
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229893"
---
# <a name="benefits-email-notification"></a>E-mailmelding voor vergoedingen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

Met de functie voor e-mailmeldingen kunnen in de volgende scenario's e-mailmeldingen en -herinneringen naar werknemers worden verzonden:

- Inschrijving van nieuwe aanstelling
- Inschrijving openen
- Kwalificerende levensgebeurtenissen

U kunt meerdere e-mailsjablonen maken en instellen, en de meldingen verzenden via het werkgebied **Vergoedingenbeheer** en de pagina **Medewerkervergoedingen**. U kunt ook de geschiedenis van meldingen/herinneringen bijhouden.

## <a name="set-up-human-resources-shared-parameters"></a>Gedeelde Human resources-parameters instellen

Op de pagina **Gedeelde Human resources-parameters** kunt u e-mailsjablonen voor vergoedingen maken voor verschillende typen communicatie die worden verzonden naar werknemers of groepen werknemers.

## <a name="create-a-new-email-id-template"></a>Een nieuwe sjabloon voor e-mail-id's maken

Volg deze stappen om een nieuwe sjabloon voor e-mail-id's te maken.

1. Ga naar **E-mailsjablonen van systeem**.
2. Selecteer **Nieuw**.
3. Geef in het veld **E-mail-id** een naam op.
4. Stel de andere velden naar wens in.
5. Selecteer **E-mailbericht** om de sjabloon te uploaden.
6. Selecteer op de pagina **Gedeelde Human resources-parameters** de nieuwe sjabloon onder **Systeemsjablonen** en verplaats deze naar **Sjablonen voor vergoedingen**.

## <a name="send-email-to-employees"></a>E-mail verzenden aan werknemers

Volg deze stappen om een e-mailbericht te verzenden naar een nieuw aangenomen werknemer die nog niet is begonnen.

1. Open het werkgebied **Vergoedingenbeheer**.
2. Selecteer de tegel voor de groep werknemers aan wie u het e-mailbericht wilt verzenden.
3. Selecteer **E-mail verzenden**.
4. Selecteer de werknemers naar wie u de e-mail wilt verzenden.
5. Selecteer **E-mail verzenden**.
6. Selecteer de sjabloon die u wilt gebruiken.
7. Selecteer **OK** om de e-mail te verzenden.

    U kunt het e-mailbericht en de status bekijken via de pagina **Medewerkervergoedingen** van de medewerker of door **E-mailhistorie van vergoedingen** te selecteren in de sectie **Koppelingen** van het werkgebied **Vergoedingenbeheer**. U kunt het e-mailbericht ook verzenden vanaf de pagina **Vergoedingsplannen voor medewerker**.

8. Als u de e-mailhistorie van vergoedingen wilt weergeven, selecteert u **E-mailhistorie van vergoedingen** in de sectie **Koppelingen** in het werkgebied **Vergoedingenbeheer**.
9. Bekijk de volledige e-mailhistorie weergeven voor e-mails over vergoedingen die zijn verzonden. Als u de inhoud van het e-mailbericht wilt bekijken, selecteert u **Bericht weergeven**.
10. Selecteer **Medewerker**.
11. Op de pagina **Vergoedingsplannen voor medewerker** kunt u e-mailberichten verzenden en de e-mailhistorie voor de vergoedingen weergeven.

Het werkgebied **Vergoedingenbeheer** bevat verschillende tegels. U kunt e-mails verzenden door de gerelateerde sjabloon te selecteren. Als de e-mails voor de inschrijving van nieuw aangenomen werknemers zijn verzonden, selecteert u de tegel **Nieuw aangestelde werknemer - Niet gestart** en vervolgens selecteert u de koppeling **Herinnering verzenden**. U kunt een herinneringssjabloon selecteren en de titel van de melding instellen als een eerste, tweede of derde herinnering.

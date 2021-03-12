---
title: Intercompany-boekhouding instellen
description: In dit onderwerp wordt uitgelegd hoe u intercompany-boekhouding kunt instellen zodat u intercompany-journalen voor grootboektoewijzingen en financiële journalen, zoals dagelijkse journalen, factuurjournalen van leveranciers en betalingsjournalen, kunt gebruiken.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: roschlom
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed05b0814826442f22d4c3508c28b3c48080e8ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988847"
---
# <a name="intercompany-accounting-setup"></a>Intercompany-boekhouding instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u intercompany-boekhouding kunt instellen zodat u intercompany-journalen voor grootboektoewijzingen en financiële journalen, zoals dagelijkse journalen, factuurjournalen van leveranciers en betalingsjournalen, kunt gebruiken.

Intercompany-journalen kunnen in diverse scenario's worden gemaakt, zoals voor dagelijkse journalen, factuurjournalen voor leveranciers, grootboektoewijzingen en gecentraliseerde betalingen. Om deze scenario's in te schakelen moet u intercompany-boekhouding instellen.

## <a name="define-main-accounts"></a>Hoofdrekeningen definiëren
Eerst moet u de intercompany-hoofdrekeningen maken voor de boekhoudvermeldingen Te betalen aan en Te ontvangen van. Het is daarom handig om unieke hoofdrekeningen voor elk bedrijf te gebruiken, zodat de afstemming en verwijdering van intercompany-boekhoudingsvermeldingen wordt vereenvoudigd. Als u een handelspartner of tegenhangerdimensie gebruikt om de intercompany-partij te identificeren, kunt u deze dimensie als vaste dimensie op de hoofdrekening definiëren die in de intercompany-boekhouding is gedefinieerd. Wanneer u de hoofdrekeningen instelt, moet u het veld **Hoofdrekeningtype** instellen op **Balans** op de pagina **Hoofdrekeningen**.

## <a name="define-journal-names"></a>Journaalnamen definiëren
Vervolgens moet u een journaalnaam definiëren. Stel het veld **Journaaltype** in op **Dagelijks** op de pagina **Journaalnamen**. Het is daarom een goed idee om een journaalnaam voor intercompany-boekhouding te gebruiken.

## <a name="define-intercompany-accounting-setup"></a>Instellingen voor intercompany-boekhouding definiëren
De pagina **Intercompany-boekhouding** wordt gebruikt voor het maken van paren rechtspersonen die met elkaar kunnen samenwerken. De instellingen van de intercompany-boekhouding worden gedeeld, zodat de instellingen van alle rechtspersonen zichtbaar zijn. Wanneer u een nieuw paar van rechtspersonen maakt, moet u duidelijk hebben welke rechtspersoon is gedefinieerd als het oorspronkelijke bedrijf ten opzichte van het doelbedrijf. Bij het invoeren van intercompany-transacties bepaalt de transactie welke rechtspersoon de transactie initieert of van welke rechtspersoon de transactie afkomstig is. De intercompany-boekhouding is bijvoorbeeld ingesteld voor USMF (bronbedrijf) en USSI (doelbedrijf). Als een gebruiker actief is in USSI en een intercompany-transactie met USMF invoert, wordt de transactie niet geboekt omdat de intercompany-boekhouding alleen is gedefinieerd voor USMF als oorspronkelijk bedrijf. Als beide bedrijven een transactie kunnen initiëren, moet u een tweede paar van rechtspersonen maken voor de wederzijdse instellingen. 

Selecteer **Debetrekening (te ontvangen van)** en **Creditrekening (te betalen aan)** voor zowel de bron- als de doelrechtspersoon. Definieer welke **Journaalnaam** wordt gebruikt wanneer de transactie is gemaakt in het doelbedrijf. Het journaal voor het oorspronkelijke bedrijf is al bekend omdat het door de gebruiker is geselecteerd bij het maken van de intercompany-transactie. 

Selecteer ten slotte welke rechtspersoon de boekhouding voor ondersteuningsbedragen ontvangt, zoals contantkorting of gerealiseerde winsten of verliezen voor gecentraliseerde betalingen. 

Een wederkerige relatie kan eenvoudig worden ingesteld op de pagina **Intercompany-boekhouding** met behulp van de knop **Wederkerigheidsrelatie maken** nadat het eerste paar van rechtspersonen is gemaakt. Wanneer het wederkerige paar is gemaakt, wordt de informatie voor het doelbedrijf gekopieerd naar het oorspronkelijke bedrijf en vice versa. Het journaal dat is gedefinieerd voor het doelbedrijf blijft aanwezig. De meeste organisaties gebruiken de dezelfde naamgevingsconventie voor hun journaalnamen, zodat de journaalnaam hetzelfde is. Als de journaalnaam verschilt, wordt een waarschuwing in het veld weergegeven om u te informeren dat het journaal niet bestaat en een ander journaal kan worden geselecteerd.




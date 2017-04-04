---
title: Intercompany-boekhouding instellen
description: "In dit onderwerp wordt uitgelegd hoe u intercompany-boekhouding instellen zodat u intercompany-journalen voor grootboektoewijzingen en financiële journalen, zoals dagelijkse journalen, factuurjournalen van leverancier en betalingsjournalen kunt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Intercompany-boekhouding instellen

In dit onderwerp wordt uitgelegd hoe u intercompany-boekhouding instellen zodat u intercompany-journalen voor grootboektoewijzingen en financiële journalen, zoals dagelijkse journalen, factuurjournalen van leverancier en betalingsjournalen kunt.

Intercompany-journalen kunnen worden gemaakt in verschillende scenario's, zoals voor dagelijkse journalen, factuurjournalen van leverancier, grootboektoewijzingen en gecentraliseerde betalingen. Om deze scenario's in te schakelen moet u intercompany-boekhouding instellen.

## <a name="define-main-accounts"></a>Hoofdrekeningen definiëren
Eerst moet u de intercompany-hoofdrekeningen maken voor de boekhoudvermeldingen Te betalen aan en Te ontvangen van. Het is daarom handig om unieke hoofdrekeningen voor elk bedrijf te gebruiken, zodat de afstemming en verwijdering van intercompany-boekhoudingsvermeldingen wordt vereenvoudigd. Als u een handelspartner of equivalente dimensie gebruikt ter identificatie van de intercompany-partij, definieert u deze dimensie als een vaste dimensie op de hoofdrekening die is gedefinieerd in intercompany-boekhouding. Wanneer u de hoofdrekeningen instelt, stelt u de **hoofdtabel rekeningtype** veld **balans** op de **hoofdrekeningen** pagina.

## <a name="define-journal-names"></a>Namen definiëren
Vervolgens moet u een journaalnaam definiëren. Stel de **journaaltype** veld **dagelijkse** op de **journaalnamen** pagina. Het is daarom een goed idee om een journaalnaam voor intercompany-boekhouding te gebruiken.

## <a name="define-intercompany-accounting-setup"></a>Intercompany-boekhouding instellingen definiëren
De **intercompany-boekhouding** pagina wordt gebruikt voor het maken van de rechtspersonen die kunnen transact-paren met elkaar. De Intercompany-instellingen wordt gedeeld, zodat de instelling van alle rechtspersonen zichtbaar is. Wanneer u een combinatie van een nieuwe rechtspersoon maakt, moet u ervoor zorgen dat u weet welke rechtspersoon is gedefinieerd als het oorspronkelijke bedrijf ten opzichte van het doelbedrijf. Bij het invoeren van intercompany-transacties, wordt de transactie bepaalt welke rechtspersoon is gestart, of afkomstig zijn van de transactie. De intercompany-boekhouding is bijvoorbeeld ingesteld voor USMF (uit) en USSI (doel). Als een gebruiker actief in USSI is en voert een intercompany-transactie met USMF, de transactie niet geboekt omdat de intercompany-boekhouding is alleen gedefinieerd voor USMF wordt de opdrachtgever. Als een bedrijf afkomstig van een transactie zijn kan, moet u een tweede paar rechtspersoon voor de wederzijdse instelling maken. 

Selecteer de **rekening debiteren (verschuldigd uit)** en **creditrekening (verschuldigd aan)** voor zowel de oorspronkelijke als de bestemming rechtspersoon. Bepalen waardoor **journaalnaam** wordt gebruikt wanneer de transactie is gemaakt in het doelbedrijf. Het journaal voor het oorspronkelijke bedrijf is al bekend omdat het door de gebruiker geselecteerd bij het maken van de intercompany-transactie. 

Ten slotte kunt u selecteren welke rechtspersoon ontvangt de boekhouding voor de ondersteuning van bedragen, zoals korting voor contante betaling of gerealiseerde winsten of verliezen voor gecentraliseerde betalingen. 

Een onderlinge relatie kan eenvoudig worden ingesteld op de **intercompany-boekhouding** pagina met behulp van de **onderlinge relatie maken** knop nadat de eerste paar van de rechtspersoon is gemaakt. Wanneer de combinatie van wederzijdse wordt gemaakt, wordt de informatie voor het doelbedrijf gekopieerd naar het oorspronkelijke bedrijf en vice versa. Het journaal dat is gedefinieerd voor het doelbedrijf blijven. De meeste organisaties gebruiken de dezelfde naamgevingsconventie voor hun namen, zodat de journaalnaam hetzelfde is. Als de journaalnaam verschilt, wordt een waarschuwing wordt weergegeven in het veld bericht dat het journaal niet bestaat en een ander journaal kan worden geselecteerd.



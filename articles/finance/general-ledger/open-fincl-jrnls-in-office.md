---
title: Sjablonen voor financiële journalen openen in Office
description: In dit onderwerp worden problemen beschreven die kunnen optreden wanneer u aangepaste financiële journalen maakt met behulp van een Microsoft Excel-sjabloon.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089452"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="4bf89-103">Sjablonen voor financiële journalen openen in Office</span><span class="sxs-lookup"><span data-stu-id="4bf89-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bf89-104">In dit onderwerp worden problemen beschreven die kunnen optreden wanneer u aangepaste financiële journalen maakt met behulp van een Microsoft Excel-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="4bf89-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="4bf89-105">Symptoom</span><span class="sxs-lookup"><span data-stu-id="4bf89-105">Symptom</span></span>

<span data-ttu-id="4bf89-106">U hebt een aangepaste Excel-sjabloon voor financiële journalen gemaakt, maar deze sjabloon wordt niet weergegeven in het menu **Regels openen in Excel**.</span><span class="sxs-lookup"><span data-stu-id="4bf89-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="4bf89-107">Anders wordt de sjabloon wel in het menu weergegeven, maar wordt er een andere sjabloon geopend wanneer u deze selecteert.</span><span class="sxs-lookup"><span data-stu-id="4bf89-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="4bf89-108">Oplossing</span><span class="sxs-lookup"><span data-stu-id="4bf89-108">Resolution</span></span>

<span data-ttu-id="4bf89-109">De standaardfunctionaliteit Openen in Excel gebruikt de hoofdgegevensbron (tabel) van de huidige pagina om te bepalen welke Office-sjablonen of gegevensentiteiten als opties worden weergegeven in het menu **Openen in Excel**.</span><span class="sxs-lookup"><span data-stu-id="4bf89-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="4bf89-110">Dit gedrag is niet de ideale ervaring voor financiële journalen, omdat financiële journalen dezelfde tabellen (LedgerJournalTable en LedgerJournalTrans) gebruiken als de hoofdgegevensbron van veel andere journaaltypen.</span><span class="sxs-lookup"><span data-stu-id="4bf89-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="4bf89-111">Voor financiële journalen is de functie Regels openen in Excel bedoeld om sjablonen weer te geven die zijn ontworpen voor het journaal in de context waarvan u momenteel werkt, zoals het algemene journaal of een betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="4bf89-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="4bf89-112">Een sjabloon die moet worden gebruikt met een leverancierbetalingsjournaal wordt bijvoorbeeld zodanig ontworpen dat uw primaire rekening wordt afgedwongen als leverancierrekening.</span><span class="sxs-lookup"><span data-stu-id="4bf89-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="4bf89-113">Als u het niveau wilt verhogen van een sjabloon zodat deze beschikbaar is in de menu's **Regels openen in Excel** en **Openen in Excel**, is het voor ontwikkelaars eenvoudig om de interface **LedgerIJournalExcelTemplate** te implementeren en de klasse **DocuTemplateRegistrationBase** uit te breiden.</span><span class="sxs-lookup"><span data-stu-id="4bf89-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="4bf89-114">Er zijn vele voorbeelden van deze benadering in het systeem geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="4bf89-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="4bf89-115">Een voorbeeld dat ter referentie kan worden gebruikt, is de interface **LedgerDailyJournalExcelTemplate** die voor het algemene journaal (of dagelijks journaal) is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4bf89-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="4bf89-116">Wanneer de interface **LedgerIJournalExcelTemplate** is geïmplementeerd voor uw sjabloon, worden in het menu **Regels openen in Excel** sjablonen gefilterd op het journaaltype van uw journaal. Met deze interface worden alleen de sjablonen weergegeven die beschikbaar zijn voor dat journaal.</span><span class="sxs-lookup"><span data-stu-id="4bf89-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="4bf89-117">De interface biedt ook een validatiemethode die ervoor zorgt dat een sjabloon niet kan worden geopend voor een journaal als deze niet aan de vereisten van het rekeningtype voldoet.</span><span class="sxs-lookup"><span data-stu-id="4bf89-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="4bf89-118">U kunt bijvoorbeeld opgeven dat het rekeningtype van het type **Leverancier** of **Grootboek** moet zijn.</span><span class="sxs-lookup"><span data-stu-id="4bf89-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="4bf89-119">Zie [Sjablonen toevoegen aan het menu Regels openen in Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md) voor meer informatie over deze functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="4bf89-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>

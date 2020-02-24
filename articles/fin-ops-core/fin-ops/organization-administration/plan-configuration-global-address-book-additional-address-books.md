---
title: Het globale adresboek en andere adresboeken plannen
description: In dit onderwerpen worden de overwegingen en de beslissingen beschreven die u tijdens het planningsproces moet maken voordat u het globaal adresboek en enige aanvullende adresboeken instelt en configureert.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aeed503500abf4f4b7ccf166f589d09bba306689
ms.sourcegitcommit: 7a855deed9f95ca2589f38db214890464b2b9061
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/13/2020
ms.locfileid: "2951204"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="9adf4-103">Het globale adresboek en andere adresboeken plannen</span><span class="sxs-lookup"><span data-stu-id="9adf4-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9adf4-104">In dit onderwerpen worden de overwegingen en de beslissingen beschreven die u tijdens het planningsproces moet maken voordat u het globaal adresboek en enige aanvullende adresboeken instelt en configureert.</span><span class="sxs-lookup"><span data-stu-id="9adf4-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="9adf4-105">Voor enkele beslissingen moet u de beslissingen bevestigen die voor andere gebieden van het product zijn gemaakt, zoals de organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="9adf4-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="9adf4-106">Algemeen adresboek</span><span class="sxs-lookup"><span data-stu-id="9adf4-106">Global address book</span></span>

<span data-ttu-id="9adf4-107">Voordat u met het algemene adresboek begint te werken, moet u de standaardwaarden hiervoor definiëren.</span><span class="sxs-lookup"><span data-stu-id="9adf4-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="9adf4-108">Deze standaardwaarden worden vervolgens gebruikt voor alle aanvullende adresboeken die u maakt.</span><span class="sxs-lookup"><span data-stu-id="9adf4-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="9adf4-109">**Beslissingen**</span><span class="sxs-lookup"><span data-stu-id="9adf4-109">**Decisions**</span></span>

- <span data-ttu-id="9adf4-110">In welke volgorde wilt u namen weergeven voor partijregistraties van het type **Persoon**?</span><span class="sxs-lookup"><span data-stu-id="9adf4-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="9adf4-111">Eén volgorde is bijvoorbeeld achternaam, tweede voornaam, voornaam.</span><span class="sxs-lookup"><span data-stu-id="9adf4-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="9adf4-112">Moeten partijregistraties worden verwijderd uit het adresboek wanneer de rolregistratie wordt verwijderd?</span><span class="sxs-lookup"><span data-stu-id="9adf4-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="9adf4-113">Moet de partijregistratie bijvoorbeeld ook worden verwijderd als een klantregistratie wordt verwijderd?</span><span class="sxs-lookup"><span data-stu-id="9adf4-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="9adf4-114">Moeten gebruikers op de hoogte worden gesteld wanneer er een nieuwe registratie is gemaakt waardoor er een dubbele registratie voorkomt in het algemene adresboek?</span><span class="sxs-lookup"><span data-stu-id="9adf4-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="9adf4-115">Moet het DUNS-nummer (Data Universal Numbering System) in de partijregistratiegegevens worden opgenomen?</span><span class="sxs-lookup"><span data-stu-id="9adf4-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="9adf4-116">Moet de uniciteit van het nummer worden gecontroleerd als het DUNS-nummer in een partijregistratie wordt opgenomen?</span><span class="sxs-lookup"><span data-stu-id="9adf4-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="9adf4-117">Wilt u een standaardpartijtype, persoon of organisatie wanneer in het algemene adresboek een partijregistratie wordt gemaakt?</span><span class="sxs-lookup"><span data-stu-id="9adf4-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="9adf4-118">Welke gebruikersrollen moeten toegang kunnen krijgen tot privéadressen en contactgegevens van partijregistraties?</span><span class="sxs-lookup"><span data-stu-id="9adf4-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="9adf4-119">Extra adresboeken</span><span class="sxs-lookup"><span data-stu-id="9adf4-119">Additional address books</span></span>

<span data-ttu-id="9adf4-120">Nadat u het algemene adresboek hebt gemaakt, kunt u desgewenst extra adresboeken maken, zoals een apart adresboek voor elk bedrijf in uw organisatie of voor elke bedrijfstak.</span><span class="sxs-lookup"><span data-stu-id="9adf4-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="9adf4-121">Fabrikam is bijvoorbeeld een internationale organisatie met meerdere bedrijven en meerdere bedrijfstakken.</span><span class="sxs-lookup"><span data-stu-id="9adf4-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="9adf4-122">Fabrikam is van plan om een adresboek te maken voor elke bedrijfstak.</span><span class="sxs-lookup"><span data-stu-id="9adf4-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="9adf4-123">Voor bedrijfstakken die op meer dan één locatie voorkomen, zoals de bedrijfstak voor pneumatisch gereedschap, wil Fabrikam een adresboek maken voor elke locatie.</span><span class="sxs-lookup"><span data-stu-id="9adf4-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="9adf4-124">Chris, de IT-manager van Fabrikam, heeft de volgende lijst met adresboeken gemaakt die nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="9adf4-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="9adf4-125">In deze lijst worden de partijregistraties beschreven die elk adresboek moet bevatten.</span><span class="sxs-lookup"><span data-stu-id="9adf4-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="9adf4-126">**Contracten in de openbare sector (PubSC)**: partijregistraties voor alle partijen die betrokken zijn in contracten van Fabrikam met de openbare sector.</span><span class="sxs-lookup"><span data-stu-id="9adf4-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="9adf4-127">**Contracten in de privésector (PubSC)**: partijregistraties voor alle partijen die betrokken zijn bij contracten met de privésector.</span><span class="sxs-lookup"><span data-stu-id="9adf4-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="9adf4-128">**Elektronisch gereedschap (ET)**: partijregistraties voor alle partijen die betrokken zijn bij de aankoop of verkoop van elektronisch gereedschap of die op een andere manier omgaan met het elektronisch gereedschap dat wordt geleverd door of gekocht voor Fabrikam in het Japanse bedrijf van Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="9adf4-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="9adf4-129">**Pneumatisch gereedschap (PTJPN)**: partijregistraties voor alle partijen die betrokken zijn bij de aankoop of verkoop van pneumatisch gereedschap of die op een andere manier omgaan met het pneumatisch gereedschap dat wordt geleverd door of gekocht voor Fabrikam in het Japanse bedrijf van Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="9adf4-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="9adf4-130">**Pneumatisch gereedschap (PTJPN)**: partijregistraties voor alle partijen die betrokken zijn bij de aankoop of verkoop van pneumatisch gereedschap of die op een andere manier omgaan met het pneumatisch gereedschap dat wordt geleverd door of gekocht voor Fabrikam in het Amerikaanse bedrijf van Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="9adf4-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="9adf4-131">**Beslissing:**</span><span class="sxs-lookup"><span data-stu-id="9adf4-131">**Decision:**</span></span>

- <span data-ttu-id="9adf4-132">Hoeveel extra adresboeken maakt u?</span><span class="sxs-lookup"><span data-stu-id="9adf4-132">How many additional address books will you create?</span></span>

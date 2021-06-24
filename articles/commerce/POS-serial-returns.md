---
title: Producten met serienummers retourneren in POS
description: In dit onderwerp worden de mogelijkheden beschreven voor het valideren van geserialiseerde artikelen als onderdeel van het retourproces in de toepassing Microsoft Dynamics 365 Commerce POS (Point of Sale).
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129801"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="446c8-103">Producten met serienummers retourneren in POS</span><span class="sxs-lookup"><span data-stu-id="446c8-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="446c8-104">In dit onderwerp worden de mogelijkheden beschreven voor het valideren van geserialiseerde artikelen als onderdeel van het retourproces in de toepassing Microsoft Dynamics 365 Commerce POS (Point of Sale).</span><span class="sxs-lookup"><span data-stu-id="446c8-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="446c8-105">In versie 10.0.20 en hoger van Commerce is een nieuwe functie met de naam **Uniforme retourverwerkingservaring in POS** beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="446c8-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="446c8-106">Schakel deze functie in als u de validatie van serienummers wilt gebruiken tijdens de verwerking van retourorders in POS.</span><span class="sxs-lookup"><span data-stu-id="446c8-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="446c8-107">Zie [Retouren maken in POS](POS-returns.md) voor informatie over andere mogelijkheden die deze functie biedt wanneer deze is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="446c8-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="446c8-108">Nadat de functie is ingeschakeld, kan deze niet meer worden uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="446c8-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="446c8-109">Opties voor het valideren van geserialiseerde retouren</span><span class="sxs-lookup"><span data-stu-id="446c8-109">Options for validating serialized returns</span></span>

<span data-ttu-id="446c8-110">Wanneer de functie **Uniforme retourverwerkingservaring in POS** is ingeschakeld, kunnen organisaties een validatie uitvoeren op retouren van artikelen met serienummers via POS.</span><span class="sxs-lookup"><span data-stu-id="446c8-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="446c8-111">Deze mogelijkheid kan gebruikers waarschuwen als het serienummer dat wordt geretourneerd, afwijkt van het oorspronkelijke serienummer dat is verkocht.</span><span class="sxs-lookup"><span data-stu-id="446c8-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="446c8-112">In de release van Commerce versie 10.0.20 en hoger is het bericht dat gebruikers ontvangen slechts een waarschuwingsbericht.</span><span class="sxs-lookup"><span data-stu-id="446c8-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="446c8-113">Gebruikers kunnen een retour blijven verwerken voor een serienummer dat afwijkt van het serienummer dat oorspronkelijk is verkocht.</span><span class="sxs-lookup"><span data-stu-id="446c8-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="446c8-114">Als u validatie van serienummers voor een organisatie wilt configureren nadat de functie **Uniforme retourverwerkingservaring in POS** is ingeschakeld, gaat u naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters** in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="446c8-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="446c8-115">Stel op het tabblad **Voorraad** op het sneltabblad **Winkelvoorraadbewerkingen** de optie **Validatie van serienummers in POS-retouren inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="446c8-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="446c8-116">Retouren verwerken voor geserialiseerde artikelen in POS</span><span class="sxs-lookup"><span data-stu-id="446c8-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="446c8-117">Als de optie **Validatie van serienummers in POS inschakelen** is ingesteld op **Ja** wanneer een artikel met serienummer wordt geretourneerd via het POS, kan de gebruiker het serienummer voor de retourregel invoeren in het detaildeelvenster op de pagina **Retourneerbare producten**.</span><span class="sxs-lookup"><span data-stu-id="446c8-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="446c8-118">Als het ingevoerde serienummer niet gelijk is aan het oorspronkelijke serienummer dat is verkocht voor de verkooptransactie, wordt een waarschuwingsbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="446c8-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="446c8-119">De toepassing voorkomt echter niet dat de gebruiker de retour kan blijven boeken.</span><span class="sxs-lookup"><span data-stu-id="446c8-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="446c8-120">Op dit moment ondersteunt POS validatie van serienummers alleen voor retourregels waar de oorspronkelijke bestelde hoeveelheid niet meer dan één is.</span><span class="sxs-lookup"><span data-stu-id="446c8-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="446c8-121">Als de oorspronkelijke verkooporderregel is gemaakt in een niet-POS-kanaal en als de bestelde hoeveelheid voor het geserialiseerde artikel op een bepaalde verkoopregel meer dan één is, kan het artikel niet op de juiste manier worden geretourneerd via het POS.</span><span class="sxs-lookup"><span data-stu-id="446c8-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="446c8-122">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="446c8-122">Additional resources</span></span>

[<span data-ttu-id="446c8-123">Retouren maken in POS</span><span class="sxs-lookup"><span data-stu-id="446c8-123">Create returns in POS</span></span>](POS-returns.md)

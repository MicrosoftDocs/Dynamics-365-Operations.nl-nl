---
title: Online kanaal maken en kanaalkenmerken definiëren
description: Deze procedure doorloopt het maken van een nieuw online kanaal en het toevoegen ervan aan de organisatiehiërarchie.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e92e28c721692ed92fa931ed899c48678622349
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964789"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Online kanaal maken en kanaalkenmerken definiëren

[!include [banner](../includes/banner.md)]

Deze procedure doorloopt het maken van een nieuw online kanaal en het toevoegen ervan aan de organisatiehiërarchie. U moet de organisatiehiërarchie maken voordat u een nieuw online kanaal kunt maken. Deze procedure gebruikt het demobedrijf USRT.


## <a name="create-a-new-online-channel"></a>Een nieuw online kanaal maken
1. Ga naar Retail en Commerce > Kanalen > Online winkels.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ of selecteer een waarde in het veld Magazijn.
5. Selecteer een optie in het veld Winkeltijdzone.
6. Typ of selecteer een waarde in het veld Standaardklant.
7. Typ of selecteer een waarde in het veld Adresboek van klant.
8. Typ of selecteer een waarde in het veld Betalingstermijnen.
9. Typ of selecteer een waarde in het veld Betalingsmethode.
10. Typ of selecteer een waarde in het veld Profiel voor e-mailmelding.
11. Vouw de sectie Financiële dimensies uit.
12. Typ of selecteer een waarde in het veld Bedrijfseenheid.
    * Stel ook de waarde in voor alle andere standaarddimensies.  
13. Klik op Opslaan.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Het online kanaal toevoegen aan de organisatiehiërarchie
1. Sluit de pagina.
2. Ga naar Organisatiebeheer > Organisaties > Organisatiehiërarchieën.
3. Zoek en selecteer de gewenste record in de lijst.
4. Klik op Weergeven.
5. Klik op Bewerken.
    * U kunt elk hiërarchieknooppunt selecteren waaronder u het nieuwe kanaal wilt invoegen.  
6. Klik op Invoegen.
7. Klik op Commerce-kanaal.
8. Klik op OK.
9. Klik op Publiceren om het verwijderdialoogvenster te openen.
10. Typ in het veld Begindatum de datum en een tijd.
11. Klik op Publiceren.

## <a name="configure-orders-for-near-real-time-notification"></a>Orders configureren voor meldingen in bijna realtime
1. Ga naar Retail en Commerce > Instelling van hoofdkantoor > Parameters > Commerce-parameters.
2. Stel Real-time service gebruiken om eCommerce-orders te maken in op Ja.
3. Voer de distributieplanning 1070 uit om wijzigingen te synchroniseren naar de kanaaldatabase. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
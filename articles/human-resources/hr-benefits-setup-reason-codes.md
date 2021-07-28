---
title: Redencodes instellen
description: Dynamics 365 Human Resources gebruikt redencodes om uit te leggen waarom de vergoedingen van een werknemer veranderen.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 176ce59547456a14b494caa4dc3c2d8251920fe5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360539"
---
# <a name="set-up-reason-codes"></a>Redencodes instellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources gebruikt redencodes om uit te leggen waarom de vergoedingen van een werknemer veranderen.

> [!NOTE]
> Met ingang van januari 2021 migreren redencodes naar het werkgebied **Personeelsbeheer** in plaats van het werkgebied **Vergoedingenbeheer**. Meer informatie vindt u in [Redencodes handmatig migreren naar Personeelsbeheer](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Redencodes maken

1. Selecteer in het werkgebied **Personeelsbeheer** (of het werkgebied **Vergoedingenbeheer** als uw redencodes nog niet zijn gemigreerd), de optie **Koppelingen** en selecteer vervolgens **Redencodes**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Redencode** | Een unieke naam om de reden te identificeren die aangeeft waarom een werknemer een inschrijving van een vergoedingsplan wijzigt. |
   | **Beschrijving** | Een beschrijving van de redencode. |

4. Stel onder **Toepasselijke scenario's** de optie **Vergoedingenbeheer** in op **Ja**. (Niet van toepassing als uw redencodes nog niet zijn gemigreerd naar het werkgebied **Personeelsbeheer**.)

5. Selecteer **Opslaan**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Redencodes handmatig migreren naar Personeelsbeheer

In januari 2021 migreren redencodes naar het werkgebied **Personeelsbeheer** in plaats van het werkgebied **Vergoedingenbeheer**. De meeste redencodegegevens worden automatisch gemigreerd in uw omgeving. Sommige redencodegegevens worden mogelijk niet gemigreerd. Redencodes hebben nu bijvoorbeeld een maximum van 15 tekens, waardoor redencodes langer dan 15 tekens niet automatisch worden gemigreerd.

Er wordt een banner weergegeven op de pagina **Koppelingen** van het werkgebied **Vergoedingenbeheer** die u op de hoogte stelt van de migratie en of er mogelijk redencodes niet zijn gemigreerd.

1. Selecteer **Redencodes** voor meer informatie over de migratiestatus.

   [![Redencodes.](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Selecteer een redencode die niet kon worden gemigreerd.

   [![Migratiestatus van redencode.](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Selecteer **Redencode migreren**.

   [![Redencode migreren.](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. In het deelvenster **Migratie redencodes vergoedingen** hebt u twee opties voor toewijzing aan een redencode voor personeelsbeheer:

   - Als u een bestaande redencode wilt gebruiken in Personeelsbeheer, kiest u een code in de vervolgkeuzelijst **Bestaande redencode gebruiken**.
     > [!NOTE]
     > U kunt alleen een bestaande redencode gebruiken in Personeelsbeheer als een andere redencode voor Vergoedingenbeheer er nog niet naartoe is gemigreerd.
   - Als u een nieuwe redencode wilt maken in Personeelsbeheer, voert u een nieuwe code in het veld **Nieuwe redencode** in en voert u vervolgens een omschrijving in **Nieuwe omschrijving** in.

   [![Toewijzen aan een redencode voor Personeelsbeheer.](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Nadat redencodes naar Personeelsbeheer zijn gemigreerd, wordt de optie voor het gebruik ervan in Vergoedingenbeheer automatisch ingesteld op **Ja**.

[![Redencode gebruiken in Vergoedingenbeheer.](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: robots.txt-bestanden beheren
description: In dit artikel wordt beschreven hoe u robots.txt-bestanden beheert in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: b66d6f725c345ff82d3f3f8c33d609fa770addf1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286406"
---
# <a name="manage-robotstxt-files"></a>robots.txt-bestanden beheren

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u robots.txt-bestanden beheert in Microsoft Dynamics 365 Commerce.

De uitsluitingsstandaard voor robots, of robots.txt, is een standaard die websites gebruiken om te communiceren met webrobots. Hiermee worden webrobots geïnstrueerd over de gebieden van een website die niet bezocht mogen worden. Robots worden vaak gebruikt door zoekmachines om websites te indexeren.

Als u robots wilt uitsluiten van een server, maakt u een bestand op de server. In dit bestand geeft u een toegangsbeleid voor robots op. Het bestand moet toegankelijk zijn via HTTP op de lokale URL **/robots.txt**. Met het robots.txt-bestand kunnen zoekmachines de inhoud op uw site indexeren.

Met Dynamics 365 Commerce kunt u een robots.txt-bestand voor uw domein uploaden. Voor elk domein in uw Commerce-omgeving kunt u één robots.txt-bestand uploaden en aan dat domein koppelen.

Ga voor meer informatie over het robots.txt-bestand naar de [pagina's voor webrobots](https://www.robotstxt.org/).

## <a name="upload-a-robotstxt-file"></a>Een robots.txt-bestand uploaden

Nadat u uw robots.txt-bestand hebt gemaakt en bewerkt volgens de [standaard voor robotuitsluiting](https://www.robotstxt.org/orig.html), moet u ervoor zorgen dat het bestand toegankelijk is op de computer waarop u de Commerce-ontwerpfunctie gaat gebruiken. Het bestand moet de naam **robots.txt** hebben. Voor de beste resultaten moet deze in indeling hebben die wordt vermeld in de standaard. Elke Commerce-klant is verantwoordelijk voor het valideren en onderhouden van de inhoud van zijn of haar eigen robots.txt-bestand. Als u een robots.txt-bestand wilt uploaden, moet u bij Commerce zijn aangemeld als systeembeheerder.

Volg deze stappen om een robots.txt-bestand te uploaden in Commerce.

1. Meld u aan bij Commerce als systeembeheerder.
2. Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.
3. Selecteer **Robots.txt** onder **Tenantinstellingen**. In het hoofdgedeelte van het venster wordt een lijst weergegeven met alle domeinen die aan uw omgeving zijn gekoppeld.
4. Selecteer **Beheren** om een robots.txt-bestand te uploaden voor een domein in uw omgeving.
5. Selecteer in het menu aan de rechterkant de knop **Uploaden** (de omhoog wijzende pijl) naast het domein dat aan het robots.txt-bestand is gekoppeld. Er verschijnt een dialoogvenster waarin u naar het bestand kunt bladeren.
6. Selecteer in dit dialoogvenster het robots.txt-bestand dat u wilt uploaden voor het gekoppelde domein en selecteer vervolgens **Openen** om het uploaden te voltooien.

> [!NOTE] 
> Tijdens het uploaden wordt geverifieerd of het bestand een tekstbestand is, maar de inhoud van het bestand wordt niet gevalideerd.

## <a name="download-a-robotstxt-file"></a>Een robots.txt-bestand downloaden

Volg deze stappen om een robots.txt-bestand te downloaden in Commerce.

1. Meld u aan bij Commerce als systeembeheerder.
2. Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.
3. Selecteer **Robots.txt** onder **Tenantinstellingen**. In het hoofdgedeelte van het venster wordt een lijst weergegeven met alle domeinen die aan uw omgeving zijn gekoppeld.
4. Selecteer **Beheren** om een robots.txt-bestand te downloaden voor een domein in uw omgeving.
5. Selecteer in het menu aan de rechterkant de knop **Downloaden** (de omlaag wijzende pijl) naast het domein dat aan het robots.txt-bestand is gekoppeld. Er verschijnt een dialoogvenster waarin u naar het bestand kunt bladeren.
6. Ga in het dialoogvenster naar de gewenste locatie op uw lokale station, bevestig of voer een bestandsnaam in en selecteer vervolgens **Opslaan** om de download te voltooien.

> [!NOTE]
> Deze procedure kan alleen worden gebruikt om robots.txt-bestanden te downloaden die eerder zijn geüpload via de Commerce-ontwerpfunctie.

## <a name="delete-a-robotstxt-file"></a>Een robots.txt-bestand verwijderen

Volg deze stappen om een robots.txt-bestand te verwijderen in Commerce.

1. Meld u aan bij Commerce als systeembeheerder.
2. Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.
3. Selecteer **Robots.txt** onder **Tenantinstellingen**. In het hoofdgedeelte van het venster wordt een lijst weergegeven met alle domeinen die aan uw omgeving zijn gekoppeld.
4. Selecteer **Beheren** om een robots.txt-bestand te verwijderen voor een domein in uw omgeving.
5. Selecteer in het menu aan de rechterkant de knop **Verwijderen** (de prullenbak) naast het domein dat aan het robots.txt-bestand is gekoppeld. Er verschijnt een venster waarin u naar het bestand kunt bladeren.
6. Selecteer in dit venster het robots.txt-bestand dat u wilt verwijderen voor het gekoppelde domein en selecteer vervolgens **Openen**. Er verschijnt een waarschuwingsvenster.
7. Selecteer in dit berichtvak de optie **Verwijderen** om de verwijdering van het robots.txt-bestand te bevestigen.

> [!NOTE] 
> Deze procedure kan alleen worden gebruikt om robots.txt-bestanden te verwijderen die eerder zijn geüpload via de Commerce-ontwerpfunctie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md)

[Een e-commerce-site maken](create-ecommerce-site.md)

[Een Dynamics 365 Commerce-site koppelen aan een online kanaal](associate-site-online-store.md)

[URL-omleidingen in bulk uploaden](upload-bulk-redirects.md)

[Een B2C-tenant instellen in Commerce](set-up-B2C-tenant.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)

[Meerdere B2C-tenants configureren in een Commerce-omgeving](configure-multi-B2C-tenants.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

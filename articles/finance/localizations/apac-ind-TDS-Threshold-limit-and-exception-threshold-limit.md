---
title: Drempellimiet en uitzonderingsdrempellimiet
description: In dit artikel worden de drempel- en uitzonderingslimieten voor TDS (belasting ingehouden op bron) beschreven.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: aceebad08b5454b64059e7ef374b9634bad35c37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877931"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Drempellimiet en uitzonderingsdrempellimiet

[!include [banner](../includes/banner.md)]

In dit artikel worden de drempel- en uitzonderingslimieten voor TDS (belasting ingehouden op bron) beschreven. TDS op facturen en betalingen wordt altijd berekend rekening houdend met de drempellimiet en uitzonderingsdrempellimiet die gedefinieerd zijn voor de TDS-belastingcomponenten op de pagina **Bronbelastingcomponenten**. De TDS-belastingcomponenten zijn gekoppeld aan TDS-belastingcodes die zijn opgenomen in de TDS-belastinggroepen. De TDS-belastinggroepen worden gekoppeld aan leveranciers en klanten om TDS te berekenen op factuurniveau of betalingsniveau.

TDS wordt berekend als het bedrag voor een transactie of de cumulatieve transacties die met een specifieke TDS-groep voor een leverancier zijn geboekt, de drempellimiet overschrijdt die is opgegeven op de pagina **Bronbelastingcomponenten**. TDS wordt pas berekend als het cumulatieve transactiebedrag de opgegeven drempellimiet overschrijdt.

Als er een uitzonderingsdrempellimiet is opgegeven samen met de drempellimiet voor een TDS-onderdeel, wordt TDS berekend wanneer een specifiek transactiebedrag de uitzonderingsdrempellimiet overschrijdt, zelfs als het cumulatieve transactiebedrag de opgegeven drempellimiet niet overschrijdt.

### <a name="example"></a>Voorbeeld
Een belastingcomponent met de naam TDS wordt ingesteld en gekoppeld aan de TDS-belastinggroep met de naam Contractant. De drempel is gedefinieerd als 50.000 en de uitzonderingsdrempel is gedefinieerd als 20.000 voor TDS-belastingcomponent. De contractant van de TDS-groep is gedefinieerd als de standaard-TDS-groep voor leverancier 1.

Er wordt een inkoopfactuur 001 geboekt voor leverancier 1 voor 10.000. TDS wordt niet berekend voor de factuur omdat het factuurbedrag de drempellimiet of uitzonderingsdrempellimiet niet heeft overschreden. Er wordt een inkoopfactuur 002 geboekt voor leverancier 1 voor 25.000. TDS wordt berekend voor de factuur omdat het factuurbedrag de drempellimiet of uitzonderingsdrempellimiet heeft overschreden. Er wordt een inkoopfactuur 003 geboekt voor leverancier 1 voor 20.000. TDS wordt berekend voor de factuur omdat het totale factuurbedrag van de drie facturen die voor de leverancier zijn uitgegeven, de drempellimiet heeft overschreden. TDS wordt berekend op alle facturen die zijn uitgegeven voor de leverancier waarop TDS niet eerder is berekend. Daarom wordt TDS berekend op 30.000. Dit is het totale factuurbedrag van factuur 001 en 003.

De drempellimiet en uitzonderingsdrempellimiet worden niet meegenomen in de TDS-berekening als het selectievakje **Drempel overslaan** is ingeschakeld voor TDS-belastingcodes in de TDS-groep die aan de transactie is gekoppeld. De drempellimiet wordt niet gebruikt in de TDS-belastingcodes in de TDS-groep waar het selectievakje **Drempel overslaan** voor is.

Als het selectievakje **Drempel overslaan** is ingeschakeld voor een specifieke TDS-groep voor bepaalde facturen, maar niet is ingeschakeld voor andere facturen die voor een specifieke leverancier/klant zijn gemaakt, kan de berekening van TDS zonder de drempellimiet over te slaan voor enkele facturen plaatsvinden. Daarbij wordt het cumulatieve bedrag op alle facturen meegenomen waarop TDS niet eerder is berekend.

De drempellimiet is bijvoorbeeld 25.000. De volgende facturen worden voor de leverancier A gemaakt:

- Factuur 1 - 20.000: (selectievakje **Drempel overslaan** is niet ingeschakeld): TDS wordt niet berekend.

- Factuur 2 - 4.000: (selectievakje **Drempel overslaan** is ingeschakeld): TDS wordt berekend over 4.000.

- Factuur 2 – 3.000: (selectievakje **Drempel overslaan** is niet ingeschakeld): TDS wordt berekend als het cumulatieve factuurbedrag, dat wil zeggen 27.000 (20.000+4.000+3.000) dat de drempellimiet heeft overschreden. TDS wordt berekend op het cumulatieve bedrag van facturen waarover het TDS-bedrag niet eerder is berekend, dat wil zeggen 23.000 (20.000+3.000).

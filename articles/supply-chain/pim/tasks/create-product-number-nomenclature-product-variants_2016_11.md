---
title: Een nomenclatuur met productnummers maken voor geconfigureerde productvarianten
description: In deze procedure wordt getoond hoe u een productnummernomenclatuur instelt voor vooraf geconfigureerde productvarianten, en hoe u deze aan een configureerbaar productmodel koppelt.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921006"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Een nomenclatuur met productnummers maken voor geconfigureerde productvarianten

[!include [banner](../../includes/banner.md)]

In deze procedure wordt getoond hoe u een productnummernomenclatuur instelt voor vooraf geconfigureerde productvarianten, en hoe u deze aan een configureerbaar productmodel koppelt. In deze procedure ziet u ook hoe u een configuratienomenclatuur samenstelt voor een component van een productconfiguratiemodel. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. De nieuwe productnummernomenclatuur is toegewezen aan het productmodel D0004. Deze taak wordt meestal uitgevoerd door een productontwerper.

## <a name="create-a-product-number-nomenclature"></a>Een productvariantnummer-nomenclatuur maken

1. Ga naar **Productgegevensbeheer \> Instellingen \> Productnomenclatuur**.
1. Selecteer **Nieuw**.
1. Typ een waarde in het veld **Naam**.
1. Typ een waarde in het veld **Beschrijving**.
1. Selecteer **Toevoegen**.
1. Selecteer **Nummer van productmodel**.
1. Selecteer **Toevoegen**.
1. Selecteer **Tekstconstante**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ een waarde in het veld **Tekst**.
1. Selecteer **Toevoegen**.
1. Selecteer **Configuratie**.
1. Sluit de pagina.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>De productnummernomenclatuur toewijzen aan een productmodel

1. Ga naar **Productgegevensbeheer \> Producten \> Productmodellen**.
1. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld het veld **Productnummer** op de waarde 'D'.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Selecteer **Bewerken**.
1. Selecteer *Ja* in het veld **Nomenclatuur gebruiken**.
1. Typ of selecteer een waarde in het veld **Productvariantnummer-nomenclatuur**.
1. Sluit de pagina.
1. Sluit de pagina.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Een nomenclatuur maken voor een productconfiguratiemodelcomponent

1. Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.
1. Zoek en selecteer de gewenste record in de lijst.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Selecteer **Bewerken**.
1. Selecteer *Ja* in het veld **Configuratienomenclatuur gebruiken**.
1. Selecteer **Toevoegen**.
1. Selecteer **Kenmerkwaarde**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ of selecteer een waarde in het veld **Kenmerk**.
1. Selecteer **Toevoegen**.
1. Selecteer **Tekstconstante**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ een waarde in het veld **Tekst**.
1. Selecteer **Toevoegen**.
1. Selecteer **Kenmerkwaarde**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ of selecteer een waarde in het veld **Kenmerk**.
1. Selecteer **Toevoegen**.
1. Selecteer **Tekstconstante**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ een waarde in het veld **Tekst**.
1. Selecteer **Toevoegen**.
1. Selecteer **Kenmerkwaarde**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ of selecteer een waarde in het veld **Kenmerk**.
1. Selecteer **Toevoegen**.
1. Selecteer **Tekstconstante**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ een waarde in het veld **Tekst**.
1. Selecteer **Toevoegen**.
1. Selecteer **Kenmerkwaarde**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ of selecteer een waarde in het veld **Kenmerk**.
1. Selecteer **Toevoegen**.
1. Selecteer **Tekstconstante**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ een waarde in het veld **Tekst**.
1. Selecteer **Toevoegen**.
1. Selecteer **Nummerreekswaarde**.
1. Markeer in de lijst de geselecteerde rij.
1. Typ of selecteer een waarde in het veld **Nummerreeks**.
1. Sluit de pagina.
1. Sluit de pagina.
1. Sluit de pagina.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
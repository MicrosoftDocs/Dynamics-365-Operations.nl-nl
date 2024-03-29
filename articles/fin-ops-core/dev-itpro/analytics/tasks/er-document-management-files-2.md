---
title: 'ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 2: Gegevensmodel uitbreiden)'
description: In dit artikel wordt beschreven hoe u een indeling voor elektronische rapportage (ER) configureert om documentbeheerbestanden (bijlagen) te gebruiken in ER-uitvoer. (Deel 2)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 9d0d87d23bcdf537d638502fb5217f32fd1b328e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290989"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 2: Gegevensmodel uitbreiden)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de taakbegeleiding "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 1: Gegevensmodel voorbereiden)".

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Gegevensmodel uitbreiden om de Documentbeheerbestanden erin weer te geven
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Rapportconfiguraties.
3. Vouw in de structuur Klantfactuurmodel uit.
4. Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).
5. Klik op Ontwerper.
6. Selecteer in de structuur Klantfactuur (InvoiceCustomer).
    * Wij zullen dit gegevensmodel uitbreiden om daarin bestanden weer te geven die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.  
7. Klik op Nieuw om het verwijderdialoogvenster te openen.
8. Typ Factuurbijlagen in het veld Naam.
    * Factuurbijlagen  
9. Selecteer "Record list" in het veld Artikeltype.
10. Klik op Toevoegen.
11. Klik op Nieuw om het verwijderdialoogvenster te openen.
12. Typ Bestandsinhoud in het veld Naam.
    * Bestandsinhoud  
13. Selecteer Container in het veld Artikeltype.
14. Klik op Toevoegen.
15. Klik op Nieuw om het verwijderdialoogvenster te openen.
16. Typ Bestandsnaam in het veld Naam.
    * Bestandsnaam  
17. Selecteer "String" in het veld Artikeltype.
18. Klik op Toevoegen.

## <a name="map-new-data-model-elements-to-data-sources"></a>Nieuwe gegevensmodelelementen toewijzen aan gegevensbronnen
1. Klik op Model toewijzen aan gegevensbron.
2. Gebruik het snelfilter om op het veld Definitie te filteren met de waarde InvoiceCustomer.
    * InvoiceCustomer  
    * Wij zullen nieuwe modelelementen toewijzen aan tot geschikte gegevensbronnen.  
3. Klik op Ontwerper.
4. Selecteer in de structuur Factuurbijlagen.
5. Vouw in de structuur Factuurbijlagen uit.
6. Selecteer in de structuur Factuurbijlagen\Bestandsnaam.
7. Klik op Bewerken.
8. Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Klik op Opslaan.
10. Sluit de pagina.
11. Selecteer in de structuur Factuurbijlagen\Bestandsinhoud.
12. Klik op Bewerken.
13. Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Klik op Opslaan.
15. Sluit de pagina.
16. Selecteer in de structuur Factuurbijlagen.
17. Klik op Bewerken.
18. Typ in het veld Formule 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Klik op Opslaan.
20. Sluit de pagina.
21. Klik op Opslaan.
22. Sluit de pagina.
23. Sluit de pagina.
24. Sluit de pagina.
25. Klik op Status wijzigen.
26. Klik op Voltooien.
27. Klik op OK.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

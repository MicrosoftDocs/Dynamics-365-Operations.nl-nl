---
title: ER Uw indeling upgraden door een nieuwe basisversie van die indeling aan te nemen
description: In dit artikel wordt uitgelegd hoe u een indelingsconfiguratie voor Elektronische rapportage (ER) onderhoudt.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5dbf8ab2ea875e902709215e249871474b17230f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883504"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a>ER Uw indeling upgraden door een nieuwe basisversie van die indeling aan te nemen

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan onderhouden voor elektronische rapportage (ER). In deze procedure wordt uitgelegd hoe een aangepaste versie kan worden gemaakt op basis van een indeling die is ontvangen van een configuratieprovider (CP). Ook wordt beschreven hoe u een nieuwe basisversie van die indeling kunt aannemen.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedures "Een configuratieprovider maken en als actief markeren" en "Gemaakte indeling gebruiken om elektronische documenten voor betalingen te genereren". Deze stappen kunnen in het GBSI-bedrijf worden uitgevoerd.

## <a name="select-format-configuration-for-customization"></a>Indelingsconfiguratie voor aanpassing selecteren
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.

    In dit voorbeeld doet voorbeeldbedrijf Litware, Inc. (https://www.litware.com) dienst als een configuratieprovider die indelingsconfiguraties voor elektronische betalingen ondersteunt voor een bepaald land.    Het voorbeeldbedrijf Proseware, Inc. (http://www.proseware.com) fungeert als een gebruiker van de indelingsconfiguratie die is verstrekt door Litware, Inc. Proseware, Inc. gebruikt indelingen in bepaalde regio's van dat land.  
2. Klik op Rapportconfiguraties.
3. Klik op Filters weergeven.
4. Pas de volgende filter toe: voer in het veld 'Naam' de waarde "BACS (UK fictief)" in met de filteroperator 'begint met'.
  
    De geselecteerde indelingsconfiguratie BACS (UK fictief) is eigendom van de provider Litware Inc.  

5. Klik op Filters weergeven.
6. Zoek en selecteer de gewenste record in de lijst.

    De versie van de indeling met de status Voltooid wordt door Proseware, Inc. gebruikt om aan te passen.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Een nieuwe configuratie voor uw aangepaste indeling van elektronisch documenten maken
Proseware, Inc. heeft versie 1.1 van de configuratie (UK fictief) ontvangen die de oorspronkelijke indeling bevat om elektronische betalingsdocumenten van Litware, Inc. te genereren in overeenstemming met hun serviceabonnement. Proseware, Inc. wil deze als standaard gaan gebruiken voor hun land, maar er is enige aanpassing vereist om specifieke regionale vereisten te ondersteunen. Proseware, Inc. wil ook de mogelijkheid behouden om een aangepaste indeling als een nieuwe versie ervan te upgraden (met wijzigingen om nieuwe landspecifieke vereisten te ondersteunen) van Litware, Inc. en ze willen deze upgrade tegen zo laag mogelijke kosten uitvoeren.  

Hiervoor moet Proseware, Inc. een configuratie maken met behulp van de configuratie Litware, Inc. BACS (UK fictief) als basis.  

1. Sluit de pagina.
2. Selecteer Proseware, Inc. en maak hiervan een actieve leverancier.
3. Klik op Instellingen als actief.
4. Klik op Rapportconfiguraties.
5. Vouw 'Betalingen (vereenvoudigd model)' in de structuur uit.
6. Selecteer 'Betalingen (vereenvoudigd model)\BACS (UK fictief)' in de structuur uit.

    Selecteer de configuratie BACS (UK fictief) van Litware, Inc. Proseware, Inc. gebruikt versie 1.1 als basis voor de aangepaste versie.  

7. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.

    Zo kunt u een nieuwe configuratie voor een aangepaste betalingsindeling maken.  

8. Voer in het veld Nieuw "Afleiden van naam: BACS (UK fictief) Litware, inc." in.

    Selecteer de optie Afleiden om het gebruik van BACS (UK fictief) te bevestigen als basis voor het maken van de aangepaste versie.  

9. Typ "BACS (UK fictief en aangepast)" in het veld Naam.
10. Typ in het veld Beschrijving: "BACS voor leveranciersbetalingen (UK fictief en aangepast)".

    De actieve configuratieprovider (Proseware, Inc.) wordt hier automatisch ingevoerd. Deze provider kan deze configuratie onderhouden. Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.  

11. Klik op Configuratie maken.

## <a name="customize-your-format-for-the-electronic-document"></a>Uw indeling voor elektronisch documenten aanpassen
1. Klik op Ontwerper.
2. Klik op Uitvouwen/samenvouwen.
3. Klik op Uitvouwen/samenvouwen.
4. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank'.
5. Klik op Toevoegen om het dialoogvenster te openen.
6. Selecteer "XML\Element" in de structuur.
7. Typ "IBAN" in het veld Naam.
8. Klik op OK.
9. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.
10. Klik op Toevoegen om het dialoogvenster te openen.
11. Selecteer "Text\String" in de structuur.
12. Klik op OK.
13. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Name\String'.
14. Voer in het veld Maximumlengte '60' in.
15. Klik op het tabblad Toewijzing.
16. Vouw in de structuur "model" uit.
17. Vouw "model\Payments" uit in de structuur.
18. Vouw "model\Payments\Creditor" uit in de structuur.
19. Vouw "model\Payments\Creditor\Account" uit in de structuur.
20. Selecteer in de structuur 'model\Payments\Creditor\Account\IBAN'.
21. Selecteer in de structuur 'Xml\Message\Payments\Item = model.Payments\Vendor\Bank\IBAN\String'.
22. Klik op Binden.
23. Klik op Opslaan.

## <a name="validate-the-customized-format"></a>De aangepaste indeling valideren
1. Klik op Valideren.

    Valideer de aangepaste indeling en gegevenstoewijzingswijzigingen om ervoor te zorgen dat alle bindingen in orde zijn.  

2. Sluit de pagina.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>De status van de huidige versie van de configuratie van de aangepaste indeling wijzigen
Wijzig de status van de ontworpen indelingsconfiguratie van Concept in Voltooid om deze beschikbaar te maken voor het genereren van betalingsdocumenten.  

1. Klik op Status wijzigen.

    De huidige versie van de geselecteerde configuratie heeft de status Concept.  

2. Klik op Voltooien.
3. Typ een waarde in het veld Omschrijving.
4. Klik op OK.
5. Zoek en selecteer de gewenste record in de lijst.

    Merk op dat de gemaakte configuratie wordt opgeslagen als voltooide versie 1.1.1. Dit houdt in dat het versie 1 van de aangepaste BACS-indeling (UK fictief en aangepast) is, die is gebaseerd op versie 1 van de BACS-indeling (UK fictief), die is gebaseerd op versie 1 van het gegevensmodel Betalingen (vereenvoudigd model).  

## <a name="test-the-customized-format-to-generate-payment-files"></a>De aangepaste indeling testen om betalingsbestanden te genereren
Voer de stappen van de procedure 'Gemaakte indeling gebruiken om elektronische documenten voor betalingen te genereren' uit in een parallelle Finance and Operations-sessie. Selecteer de indeling BACS (UK fictief) in parameters voor elektronische betalingsmethoden. Zorg ervoor dat het gemaakte betalingsbestand het zojuist geïntroduceerde XML-knooppunt bevat dat de IBAN-code in overeenstemming met regionale vereisten weergeeft.  

## <a name="update-the-existing-country-specific-configuration"></a>De bestaande landspecifieke configuratie bijwerken
Litware, Inc. moet de configuratie BACS (UK fictief) bijwerken en nieuwe landvereisten aannemen voor het beheren van de indeling van het elektronische document. Later wordt deze in een nieuwe versie van deze configuratie ingesloten die wordt aangeboden voor serviceabonnees, inclusief Proseware, Inc.  

In de echte service-inrichtingsgerelateerde processen kan elke nieuwe versie van BACS (UK fictief) worden geïmporteerd door Proseware, Inc. uit de LCS-opslagplaats met configuraties van Litware, Inc. In deze procedure wordt dit gesimuleerd door BACS (UK fictief) namens een serviceprovider.  

1. Sluit de pagina.
2. Selecteer Litware, Inc. .
3. Klik op Instellingen als actief.
4. Klik op Rapportconfiguraties.
5. Vouw 'Betalingen (vereenvoudigd model)' in de structuur uit.
6. Selecteer 'Betalingen (vereenvoudigd model)\BACS (UK fictief)' in de structuur uit.

    De conceptversie in bezit van de provider Litware, Inc. BACS (UK fictief) wordt geselecteerd om wijzigingen aan te brengen ter ondersteuning van nieuwe landspecifieke vereisten.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>De basisindeling van elektronisch documenten lokaliseren
Stel dat er nieuwe land/regio-specifieke behoeften moeten worden ondersteund door Litware, Inc.:  

- Een waarde voor de bank-SWIFT-code van de crediteur in elke betalingstransactie.
- Een limiet van 100 tekens voor de lengte van de tekst voor de naam van de leverancier in een bestand dat wordt gegenereerd.  
- Nieuwe landspecifieke vereisten  
- Selecteer de conceptversie van de gewenste configuratie om de vereiste wijzigingen te introduceren.  


1. Klik op Ontwerper.
2. Klik op Uitvouwen/samenvouwen.
3. Klik op Uitvouwen/samenvouwen.
4. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank'.
5. Klik op Toevoegen om het dialoogvenster te openen.
6. Selecteer "XML\Element" in de structuur.
7. Typ "SWIFT" in het veld Naam.
8. Klik op OK.
9. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.
10. Klik op Toevoegen om het dialoogvenster te openen.
11. Selecteer "Text\String" in de structuur.
12. Klik op OK.
13. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Name\String'.
14. Voer in het veld Maximumlengte '100' in.
15. Klik op het tabblad Toewijzing.
16. Vouw in de structuur "model" uit.
17. Vouw "model\Payments" uit in de structuur.
18. Vouw "model\Payments\Creditor" uit in de structuur.
19. Vouw "model\Payments\Creditor\Agent" uit in de structuur.
20. Selecteer in de structuur 'model\Payments\Creditor\Agent\SWIFT'.
21. Selecteer in de structuur 'Xml\Message\Payments\Item = model.Payments\Vendor\Bank\SWIFT\String'.
22. Klik op Binden.
23. Klik op Opslaan.

## <a name="validate-the-localized-format"></a>De gelokaliseerde indeling valideren
1. Klik op Valideren.
2. Sluit de pagina.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>De status van de huidige versie van de basisindelingsconfiguratie wijzigen
Wijzig de status van de bijgewerkte configuratie van de basisindeling van Concept in Voltooid om deze beschikbaar te maken voor het genereren van betalingsdocumenten en updates van indelingsconfiguraties die ervan zijn afgeleid.  

1. Klik op Status wijzigen.

    De huidige versie van de geselecteerde configuratie heeft de status Concept.  

2. Klik op Voltooien.
3. Typ een waarde in het veld Omschrijving.
4. Klik op OK.
5. Zoek en selecteer de gewenste record in de lijst.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>De basisversie voor de configuratie van de aangepaste indeling wijzigen

Proseware, Inc. wordt geïnformeerd dat een nieuwe versie 1.2 van de configuratie BACS (UK fictief UK) beschikbaar is voor het genereren van elektronische betalingsdocumenten in overeenstemming met de recent aangekondigde landspecifieke vereisten. Proseware, Inc. wil deze als standaard voor het land gaan gebruiken.  

Hiervoor moet Proseware, Inc. de versie van de basisconfiguratie voor de aangepaste configuratie BACS (UK fictief en aangepast) wijzigen. Gebruik in plaats van versie 1.1 van BACS (UK fictief) de nieuwe versie 1.2.  

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Selecteer Proseware, Inc. en maak hiervan een actieve leverancier.
3. Klik op Instellingen als actief.
4. Klik op Rapportconfiguraties.
5. Vouw 'Betalingen (vereenvoudigd model)' in de structuur uit.
6. Vouw 'Betalingen (vereenvoudigd model)\BACS (UK fictief)' in de structuur uit.
7. Selecteer 'Betalingen (vereenvoudigd model)\BACS (UK fictief)\BACS (UK fictief en aangepast)' in de structuur.

    Selecteer de configuratie BACS (UK fictief en aangepast) waarvan Proseware, Inc. eigenaar is.  

    Gebruik de conceptversie van de geselecteerde configuratie om de vereiste wijzigingen te introduceren.  

8. Klik op Rebase.

    Selecteer de nieuwe versie 1.2 van de basisconfiguratie die als een nieuwe basis moet worden toegepast voor het bijwerken van de configuratie.  

9. Klik op OK.

    Er zijn enkele conflicten geconstateerd tussen het samenvoegen van de aangepaste versie en een nieuwe basisversie. Dit betreft enkele indelingswijzigingen die niet automatisch kunnen worden samengevoegd.  

## <a name="resolve-rebase-conflicts"></a>Rebaseconflicten oplossen
1. Klik op Ontwerper.
    
    Wijzigingen in de limiet voor de tekstlengte van de naam van de leverancier kunnen niet automatisch worden opgelost. Daarom wordt dit aangegeven in een lijst met conflicten. Voor elk conflict van het type Update zijn de volgende opties beschikbaar: - Pas een eerdere basiswaarde (knop boven aan het raster) toe om de vorige waarde van de basisversie te gebruiken (0 in ons geval).  - Pas een basiswaarde (knop boven aan het raster) om de nieuwe waarde van de basisversie te gebruiken (100 in ons geval).  - Behoud uw eigen (aangepaste) waarde (60 in dit geval).  Kik op Basiswaarde toepassen om een landspecifieke limiet van 100 tekens voor de tekstlengte van leveranciersnamen toe te passen.  

    Proseware, Inc. en Litware, Inc. hebben aangepaste en lokale versies van deze indeling waarin IBAN- en SWIFT-codes worden gebruikt met gerelateerde componenten die automatisch worden samengevoegd in de indeling.  

2. Klik op Basiswaarde toepassen.

    Kik op Basiswaarde toepassen om de landspecifieke limiet van 100 tekens voor leveranciersnamen toe te passen.  

3. Klik op Opslaan.

    Als u de indeling opslaat, worden opgeloste conflicten uit de lijst met conflicten verwijderd.  

4. Sluit de pagina.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>De status van de nieuwe versie van de configuratie van de aangepaste indeling wijzigen
1. Klik op Status wijzigen.

    Wijzig de status van de bijgewerkte, aangepaste indelingsconfiguratie van Concept in Voltooid. Hierdoor wordt de indelingsconfiguratie beschikbaar voor het genereren van betalingsdocumenten. De huidige versie van de geselecteerde configuratie heeft de status Concept.  

2. Klik op Voltooien.
3. Typ een waarde in het veld Omschrijving.
4. Klik op OK.

    De gemaakte configuratie wordt als voltooide versie 1.2.2 opgeslagen: versie 2 van de basisindeling BACS (UK fictief en aangepast), die is gebaseerd op versie 2 van basisindeling BACS (UK fictief), die is gebaseerd op versie 1 van het gegevensmodel Betalingen (vereenvoudigd model).  

## <a name="test-the-customized-format-for-payment-files-generation"></a>De aangepaste indeling testen om betalingsbestanden te genereren
Voer de stappen van de procedure 'Gemaakte indeling gebruiken om elektronische documenten voor betalingen te genereren' uit in een parallelle Finance and Operations-sessie. Selecteer de gemaakte indeling 'BACS (UK fictief en aangepast)' in parameters voor elektronische betalingsmethoden. Zorg ervoor dat het gemaakte betalingsbestand het zojuist door Proseware, Inc. geïntroduceerde XML-knooppunt bevat dat de IBAN-rekeningcode in overeenstemming met regionale vereisten weergeeft. Het bestand moet ook het onlangs door Litware, Inc. geïntroduceerde XML-knooppunt met de SWIFT-bankcode bevatten conform de landvereisten.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
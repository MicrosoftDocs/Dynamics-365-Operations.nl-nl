---
title: Een nieuwe ER-oplossing ontwerpen om ZPL-labels af te drukken
description: In dit artikel wordt uitgelegd hoe u een nieuwe oplossing voor elektronische rapportering (ER) kunt ontwerpen om ZPL-labels (Zebra Programming Language) af te drukken.
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7ef83cf4822ca129af3ca01fa6ddd05219fee0d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271758"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Een nieuwe ER-oplossing ontwerpen om ZPL-labels af te drukken

[!include [banner](../includes/banner.md)]


In dit artikel wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder, ER-ontwikkelaar of functioneel ER-consultant parameters van het [ER](general-electronic-reporting.md)-raamwerk kan configureren, de vereiste ER-[configuraties](general-electronic-reporting.md#Configuration) van een nieuwe ER-oplossing kan ontwerpen om toegang te krijgen tot de gegevens van het magazijnbeheersysteem en aangepaste magazijnlabels kan generen rapport in de ZPL II-indeling. Deze stappen kunnen in het **USRT**-bedrijf worden uitgevoerd.

## <a name="business-scenario"></a>Bedrijfsscenario

U vertegenwoordigt een bedrijf dat magazijnbeheer heeft geïmplementeerd in Microsoft Dynamics 365 Finance. Elke magazijnlocatie moet een zelfklevend label hebben met een streepjescode. Magazijnmedewerkers gebruiken handscanner om de streepjescodes te lezen.

Alle magazijnlocaties hebben een naam in het kader van pre-go-live activiteiten. U moet echter ook magazijnlocatielabels op aanvraag kunnen afdrukken als bestaande labels beschadigd raken of schappen opnieuw wordt geconfigureerd. Met de recent uitgebracht ER-functionaliteit kunt u een nieuwe ER-oplossing configureren waarmee een magazijnsupervisor labels rechtstreeks op een labelprinter kan afdrukken.

## <a name="configure-the-er-framework"></a>Het ER-raamwerk configureren

Voer de stappen in [Het ER-raamwerk configureren](er-quick-start2-customize-report.md#ConfigureFramework) uit om de minimale set ER-parameters in te stellen. U moet deze instellingen voltooien voordat u het ER-raamwerk gaat gebruiken om een nieuwe ER-oplossing te ontwerpen.

## <a name="design-a-domain-specific-data-model"></a>Domeinspecifiek gegevensmodel ontwerpen

Maak een nieuwe ER-configuratie die een onderdeel met een [gegevensmodel](er-overview-components.md#data-model-component) bevat voor het bedrijfsdomein Magazijnbeheer. Dit gegevensmodel wordt later gebruikt als gegevensbron wanneer u een ER-indeling ontwerpt om labels voor de magazijnlocatie te genereren.

### <a name="import-a-data-model-configuration"></a>Een gegevensmodelconfiguratie importeren

Volg deze stappen om het vereiste gegevensmodel te importeren uit een XML-bestand dat door Microsoft wordt geleverd. U kunt ook uw eigen gegevensmodel maken, zoals in de volgende sectie wordt beschreven.

1. Download het bestand [Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) en sla het op uw lokale computer op.
2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
4. Selecteer in het actievenster op de pagina **Configuraties** de optie **Uitwisselen** \> **Laden uit XML-bestand**.
5. Selecteer **Bladeren** en zoek en selecteer het bestand **Warehouse model.version.1.xml**.
6. Selecteer **OK** om de configuratie te importeren.

![Configuratie van het geïmporteerde ER-gegevensmodel op de pagina Configuraties.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Een gegevensmodelconfiguratie maken

In plaats van het door Microsoft geleverde gegevensmodelbestand te importeren, kunt u zelf een gegevensmodel maken. Zie [Een nieuwe configuratie van het gegevensmodel maken](er-quick-start1-new-solution.md#DesignDataModel) voor een voorbeeld hoe u deze taak kunt voltooien.

### <a name="review-the-data-model"></a>Het gegevensmodel controleren

U kunt een bewerkbare versie van het geconfigureerde gegevensmodel weergeven op de pagina **Gegevensmodelontwerper**.

![Structuur van het ER-gegevensmodel op de pagina Gegevensmodelontwerper.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Een modeltoewijzing voor het geconfigureerde gegevensmodel ontwerpen

Als gebruiker in de rol van ER-ontwikkelaar moet u een nieuwe ER-configuratie maken die een [modeltoewijzingsonderdeel](er-overview-components.md#model-mapping-component) bevat voor het gegevensmodel Magazijn. Dit onderdeel implementeert het geconfigureerde gegevensmodel voor Dynamics 365 Finance en is specifiek voor die app. U moet het configureren om de toepassingsobjecten op te geven die worden gebruikt voor het invullen met toepassingsgegevens van het geconfigureerde gegevensmodel tijdens runtime. Als u deze taak wilt voltooien, moet u begrijpen hoe de gegevensstructuur van het bedrijfsdomein Magazijnbeheer wordt geïmplementeerd in Finance.

### <a name="import-a-model-mapping-configuration"></a>Een configuratie voor de modeltoewijzing importeren

Volg deze stappen om het vereiste modeltoewijzing te importeren uit een XML-bestand dat door Microsoft wordt geleverd. U kunt ook uw eigen modeltoewijzing maken, zoals in de volgende sectie wordt beschreven.

1. Download het bestand [Warehouse model mapping.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) en sla het op uw lokale computer op.
2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
4. Selecteer in het actievenster op de pagina **Configuraties** de optie **Uitwisselen** \> **Laden uit XML-bestand**.
5. Selecteer **Bladeren** en zoek en selecteer het bestand **Warehouse model mapping.version.1.1.xml**.
6. Selecteer **OK** om de configuratie te importeren.

![Configuratie van geïmporteerde ER-modeltoewijzing op de pagina Configuraties.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Een configuratie voor de modeltoewijzing maken

In plaats van het door Microsoft geleverde modeltoewijzingsbestand te importeren, kunt u zelf een modeltoewijzing maken. Zie [Een nieuwe configuratie van het modeltoewijzing maken](er-quick-start1-new-solution.md#CreateModelMapping) voor een voorbeeld hoe u deze taak kunt voltooien.

### <a name="review-the-model-mapping"></a>De modeltoewijzing controleren

U kunt een bewerkbare versie van de geconfigureerde modeltoewijzing weergeven op de pagina **Ontwerper modeltoewijzing**.

![Structuur van de ER-modeltoewijzing op de pagina Ontwerper modeltoewijzing.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Een indeling ontwerpen

Als gebruiker in de rol van ER-functieconsultant moet u een nieuwe configuratie maken die een [indeling](er-overview-components.md#format-component)sonderdeel bevat. Als u dit onderdeel wilt configureren, gebruikt u ZPL II-code om de indeling van uw magazijnlocatielabel op te geven.

### <a name="import-a-format-configuration"></a>Een indelingsconfiguratie importeren

Volg deze stappen om de vereiste indeling te importeren uit een XML-bestand dat door Microsoft wordt geleverd. U kunt ook uw eigen indeling maken, zoals in de volgende sectie wordt beschreven.

1. Download het bestand [Warehouse location labels.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) en sla het op uw lokale computer op.
2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.
4. Selecteer in het actievenster op de pagina **Configuraties** de optie **Uitwisselen** \> **Laden uit XML-bestand**.
5. Selecteer **Bladeren** en zoek en selecteer het bestand **Warehouse location labels.version.1.1.xml**.
6. Selecteer **OK** om de configuratie te importeren.

![Configuratie van het geïmporteerde ER-indeling op de pagina Configuraties.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Een indelingsconfiguratie maken

In plaats van het door Microsoft geleverde indelingsbestand te importeren, kunt u zelf een indeling maken. Zie [Een nieuwe indelingsconfiguratie maken](er-quick-start1-new-solution.md#FormatCreate) voor een voorbeeld hoe u deze taak kunt voltooien.

### <a name="review-the-format"></a>De indeling controleren

U kunt een bewerkbare versie van de geconfigureerde indeling weergeven op de pagina **Indelingsontwerper**.

![Structuur van de ER-indeling op de pagina Indelingsontwerper.](./media/er-design-zpl-labels-format.png)

De `model.Location.Label`-gegevensbron van deze indeling wordt geconfigureerd voor het genereren van labels die de volgende informatie bevatten:

- De magazijnnaam als tekst
- De magazijnnaam als streepjescode
- De locatienaam
- Controlecijfers

De ER-formule die wordt gebruikt om labels te genereren, bevat op de pagina **Formuleontwerper** voor de gegevensbron een `CONCATENATE`-functie waarmee de informatie in de gewenste indeling wordt gecombineerd.

![Formule voor gegevensbron op de pagina Formuleontwerper.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> De labelindeling is zo ontworpen dat de locatienaam en de controlecijfers worden uitgelijnd op het midden van het label. In ZPL II wordt gecentreerde uitlijning voor streepjescodes echter niet ondersteund. Daarom wordt de formule van de `model.Location.Warehouse.Alignment`-gegevensbron gebruikt om de streepjescode uit te lijnen in het midden van het label. Met deze formule wordt de verschuiving vanaf links van de streepjescode berekend op basis van het aantal tekens in de magazijnnaam.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Uw omgeving voorbereiden voor het vooraf bekijken van gegenereerde labels

In het volgende voorbeeld wordt een printeremulatortoepassing voor ZPL-labels gebruikt om een voorbeeld van gegenereerde labels op het scherm weer te geven. Voer deze stappen uit om deze optie in te schakelen.

1. Voeg de ER-bestemming [Printer](er-destination-type-print.md) toe voor de ER-indeling **Magazijnlocatielabel** en configureer deze om gegenereerde labels van Finance te verzenden naar de [Document Routing Agent (DRA)](install-document-routing-agent.md).
2. Installeer en configureer DRA om gegenereerde labels uit Finance te routeren naar een lokale printer die toegankelijk is vanaf het huidige werkstation.
3. Voeg een lokale printer voor het huidige werkstation toe en configureer deze om gegenereerde labels uit DRA door te sturen naar een printeremulatortoepassing.
4. Installeer een printeremulatortoepassing als extensie van de Chrome-webbrowser en configureer deze om gegenereerde labels van een lokale printer door te sturen naar een webservice die gegenereerde labels weergeeft en ze terugstuurt naar de printeremulator om te bekijken.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER-rapport</p>
<p>Bestemming voor printers</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Documentrouteringsagent</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Lokale printer</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Printeremulator</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Webservice voor rendering</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Een printeremulatortoepassing installeren en configureren

Voeg een printeremulatortoepassing voor de ZPL-renderingengine toe aan uw Chrome-webbrowser. In dit voorbeeld wordt de emulator [ZPL-printer](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) gebruikt die is gebaseerd op de [webservice Labelary ZPL](http://labelary.com/service.html). Met de printeremulator worden gegenereerde labels in ZPL-indeling van een lokale printer naar de webservice gestuurd en vervolgens als PDF- of PNG-bestanden teruggestuurd als voorbeeld.

1. Zoek in de Chrome-webwinkel naar de printeremulatortoepassing die u wilt gebruiken en selecteer deze. Selecteer vervolgens **Toevoegen aan Chrome** om de toepassing aan uw Chrome-webbrowser toe te voegen.

    ![Het toevoegen van de printeremulatortoepassing aan de webbrowser Chrome vanuit de Chrome-webwinkel.](./media/er-design-zpl-labels-add-app.png)

2. Selecteer **App starten** om de printeremulatortoepassing uit te voeren via de Chrome-webbrowser.

    ![De printeremulatortoepassing uitvoeren via de Chrome-webbrowser.](./media/er-design-zpl-labels-run-app.png)

3. De toepassing in uitvoering configureren:

    1. Schakel de toepassing uit.
    2. Stel in de printerinstellingen de host in op **127.0.0.1**.
    3. Stel de poort in op **9100**.

        ![De printeremulatortoepassing configureren.](./media/er-design-zpl-labels-configure-app.png)

    4. Schakel de toepassing weer in. U moet een bericht ontvangen met de melding dat de printer is gestart op de opgegeven host en poort.

        ![De printeremulatortoepassing wordt weer ingeschakeld.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Aangezien de printeremulatortoepassing die in dit voorbeeld wordt gebruikt, op een webservice is gebaseerd om labels weer te geven, zorgt u ervoor dat de beveiligingsinstellingen toestaan dat u met de service kunt communiceren. Anders ontvangt de toepassing de weergegeven labels niet en is er geen voorbeeld van deze labels beschikbaar.

### <a name="add-and-configure-a-local-printer"></a>Een lokale printer toevoegen en configureren

[Voeg een nieuwe lokale printer toe](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b) waarmee het huidige apparaat gegenereerde labels uit DRA kan door sturen naar de printeremulatortoepassing.

1. Selecteer in Windows **Start** \> **Instellingen** \> **Apparaten** \> **Printers \& scanners**.
2. Selecteer **Instellingen van printers \& scanners**.
3. Als u een **printer of scanner wilt toevoegen**, selecteert u **Apparaat toevoegen**.
4. Voor **De gewenste printer staat niet in de lijst** selecteert u **Handmatig toevoegen**.
5. In het veld **Een printer zoeken met andere opties** selecteert u **Een lokale printer of netwerkprinter met handmatige instellingen toevoegen**.
6. Selecteer **Nieuwe poort maken** inhet veld **Printerpoort kiezen** en volg deze stappen:

    1. Selecteer **Standaard TCP/IP-poort** in het veld **Type poort**.
    2. Voer in het veld **Hostnaam of IP-adres** de waarde **127.0.0.1** in.
    3. Voer in het veld **Poortnaam** **ZPL** in.
    4. Wacht tot de bewerking **TCP/IP-poort detecteren** is voltooid.
    5. Selecteer **Aangepast** in het veld **Apparaattype** en vervolgens **Instellingen**.
    6. Zorg ervoor dat de volgende poortinstellingen zijn opgegeven:

        - **Poortnaam:** ZPL
        - **Printernaam of IP-adres:** 127.0.0.1
        - **Protocol:** Raw
        - **Poortnummer:** 9100

7. Selecteer **Algemeen/alleen tekst** in het veld **Printertuurprogramma installeren**.
8. Voer **ZebraPrinter** in het veld **Printernaam** in.

![Een lokale printer toevoegen voor het huidige apparaat.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>DRA installeren en configureren

Bereid de DRA voor om gegenereerde labels uit Finance door te sturen naar de geconfigureerde lokale printer.

1. [Installeer DRA](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Configureer DRA](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Registreer de lokale printer](install-document-routing-agent.md#register-network-printers) in DRA.
4. [Activeer de lokale printer](install-document-routing-agent.md#administer-network-printers) in uw Finance- omgeving.

![DRA voorbereiden om gegenereerde labels af te drukken.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>De ER-bestemming configureren

Bereid de ER-bestemming voor om gegenereerde labels uit Finance door te sturen naar de DRA.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Bestemming elektronische rapportage**.
2. Selecteer **Nieuw** in het actievenster op de pagina **ER-bestemming**.
3. Selecteer **Magazijnlocatielabels** in het veld **Verwijzing**.
4. Selecteer **Nieuw** op het sneltabblad **Bestandsbestemming**.
5. Voer in het veld **Naam** de tekst **Labels** in.
6. Selecteer in het veld **Naam bestandsonderdeel** de optie **Rapport**.
7. Selecteer **Instellingen**.
8. Stel in het dialoogvenster **Bestemmingsinstellingen** dat verschijnt op het tabblad **Printer** de optie **Ingeschakeld** in op **Ja**.
9. Selecteer **ZebraPrinter** in het veld **Printernaam**.
10. Selecteer **ZPL** in het veld **Documentrouteringstype**.
11. Selecteer **OK**.

![De ER-bestemming configureren voor magazijnlocatielabels op de pagina Bestemming elektronische rapportage.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Magazijnlocaties controleren

1. Ga naar **Magazijnbeheer** \> **Instellingen** \> **Magazijn** \> **Locaties**.
2. Filter de pagina **Locaties** om alleen locaties weer te geven die een waarde hebben in het veld **Controlecijfers** controleren.

![Magazijnlocaties controleren op de pagina Locaties](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Magazijnlocatielabels afdrukken

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur **Magazijnmodel** uit en selecteer **Magazijnlocatielabels**.
3. Selecteer **Uitvoeren** in het actievenster.
4. Selecteer in het dialoogvenster **ER-parameters** op het tabblad **Op te nemen records** de optie **Filter**.
5. Zoek op het tabblad **Bereik** de rij waar het veld **Tabel** is ingesteld op **Locaties** en het veld **Veld** is ingesteld op **Locatie**. Voer **LPEnabled** in het veld **Criteria** in.
6. Selecteer **OK**.
7. Selecteer **OK**. Er wordt een label gegenereerd en weergegeven op de voorbeeldpagina in de printeremulatortoepassing.

![Een gegenereerd label weergeven op de voorbeeldpagina in de ZPL-printeremulatortoepassing.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>De indeling van een label wijzigen

U kunt de huidige indeling van de magazijnlocatielabels wijzigen. In het volgende voorbeeld ziet u hoe u de indeling wijzigt, zodat gegenereerde labels een locatieprofiel-id bevatten.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Stel **Bestemmingen gebruiken voor conceptstatus** [ER-gebruikersparameter](electronic-reporting-destinations.md#applicability) in op **Ja**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur **Magazijnmodel** uit en selecteer **Magazijnlocatielabels**.
4. Selecteer **Ontwerper**.
5. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** de `model.Location.Label`-gegevensbron.
6. Selecteer in het dialoogvenster **Gegevensbroneigenschappen** **Bewerken** \> **Formule bewerken**.
7. Controleer op de pagina **Formuleontwerper** in het veld **Formule** de ER-formule waarmee labels worden gegenereerd.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Werk de formule bij om een locatieprofiel-id toe te voegen aan gegenereerde labels.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Selecteer **Opslaan**.
10. Selecteer **OK**.
11. Selecteer **Uitvoeren** in het actievenster.
12. Selecteer in het dialoogvenster **ER-parameters** op het tabblad **Op te nemen records** de optie **Filter**.
13. Zoek op het tabblad **Bereik** de rij waar het veld **Tabel** is ingesteld op **Locaties** en het veld **Veld** is ingesteld op **Locatie**. Voer **Vak** in het veld **Criteria** in.
14. Selecteer **OK**.
15. Selecteer **OK**. Er wordt een label gegenereerd en weergegeven op de voorbeeldpagina in de printeremulatortoepassing.

![Een gegenereerd label controleren dat een locatieprofiel-id bevat op de voorbeeldpagina van de toepassing ZPL-printeremulator.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Versleutelen

> [!NOTE]
> U moet de coderingsinstelling van het onderdeel **Common\\File** van de bewerkbare ER-indeling synchroniseren met de juiste instelling van het ontworpen label. De waarde van het veld **[Codering](er-suppress-bom-characters.md)** van het onderdeel **Common\\File** mag niet strijdig zijn met een ZPL-opdracht die wordt gebruikt om de codering van het label aan te geven (bijvoorbeeld de opdracht `^CI`). ER valideert niet of deze instellingen zijn gesynchroniseerd.

## <a name="additional-resources"></a>Aanvullende bronnen

[Bestemming voor printers](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

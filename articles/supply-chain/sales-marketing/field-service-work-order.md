---
title: Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations
description: In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt voor het synchroniseren van werkorders in Field Service met verkooporders in Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: 933d9755085d507310dd46d96a492d2124647ec3
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van werkorders in Microsoft Dynamics 365 for Field Service met verkooporders in Microsoft Dynamics 365 for Finance and Operations.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt voor het synchroniseren van werkorders in Field Service met verkooporders in Finance and Operations.

## <a name="templates-and-tasks"></a>Sjablonen en taken

De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van werkorders in Field Service met verkooporders in Finance and Operations.

### <a name="names-of-the-templates-in-data-integration"></a>Namen van de sjablonen in Gegevensintegratie

De sjabloon **Werkorders met verkooporders (Field Service met Finance and Operations)** wordt gebruikt voor synchronisatie.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Namen van de taken in het project Gegevensintegratie

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderproductLineEstimate
- WorkOrderproductLineUsed

De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkooporders kan plaatsvinden:

- Field Service-producten (Fin and Ops naar Field Service)
- Rekeningen (Sales naar Fin and Ops) - Direct

## <a name="entity-set"></a>Entiteitset

| **Field Service** | **Finance and Operations** |
|-------------------------|-------------------------|
| msdyn_workorders        | CDS-verkooporderkopteksten |
| msdyn_workorderservices | CDS-verkooporderregels   |
| msdyn_workorderproducts | CDS-verkooporderregels   |

## <a name="entity-flow"></a>Entiteitstroom

Werkorders worden gemaakt in Field Service. Als de werkorders alleen extern onderhouden producten bevatten en als de waarde **Werkorderstatus** verschilt van **Open - niet-gepland** en **Afgesloten – geannuleerd**, kunnen de werkorders worden gesynchroniseerd met Finance and Operations via een CDS-gegevensintegratieproject. Updates op de werkorders worden gesynchroniseerd als verkooporders in Finance and Operations. Deze updates bevatten de informatie over het oorspronkelijke type en de status.

## <a name="estimated-versus-used"></a>Geraamd versus gebruikt

In Field Service hebben producten en diensten op werkorders de waarden **Geraamd** en **Gebruikt** voor hoeveelheden en bedragen. In Finance and Operations hebben verkooporders echter niet hetzelfde concept van de waarden **Geraamd** en **Gebruikt**. Ter ondersteuning van de producttoewijzing die gebruikmaakt van de verwachte hoeveelheid op de verkooporder in Finance and Operations, maar om de gebruikte hoeveelheid te behouden die moet worden verbruikt en gefactureerd, worden met twee soorten taken de producten en services op de werkorder gesynchroniseerd. De ene set taken is voor **geraamde** waarden en de andere set taken voor **gebruikte** waarden.

Hierdoor worden scenario's mogelijk waarin de geschatte waarden worden gebruikt voor toewijzing of reservering in Finance and Operations, terwijl de gebruikte waarden worden gebruikt voor verbruik en de facturering.

### <a name="estimated"></a>Geraamd

Voor het synchroniseren van productregels worden de **geraamde** waarden gebruikt wanneer de **Regelstatus** de waarde **Geraamd** heeft, de optie **Toegewezen** is ingesteld op **Ja** en de waarde **Systeemstatus** niet **Afgesloten - geboekt** is.

Voor het synchroniseren van serviceregels worden de **geraamde** waarden gebruikt wanneer de **Regelstatus** de waarde **Geraamd** heeft en de waarde **Systeemstatus** niet **Afgesloten - geboekt** is.

### <a name="used"></a>Gebruikt

De **gebruikte** waarden worden gebruikt voor verbruik en facturering. In deze gevallen worden de **gebruikte** waarden gesynchroniseerd.

De volgende tabel bevat een overzicht van de verschillende combinaties voor productregels.

| Systeemstatus <br>(Field Service) | Regelstatus <br>(Field Service) | Toegewezen <br>(Field Service) |Gesynchroniseerde waarde <br>(Finance and Operations) |
|--------------------|-------------|-----------|---------------------------------|
| Open - gepland   | Geraamd   | Ja       | Geraamd                       |
| Open - gepland   | Geraamd   | Nee        | Gebruikt                            |
| Open - gepland   | Gebruikt        | Ja       | Gebruikt                            |
| Open - gepland   | Gebruikt        | Nee        | Gebruikt                            |
| Open - in uitvoering | Geraamd   | Ja       | Geraamd                       |
| Open - in uitvoering | Geraamd   | Nee        | Gebruikt                            |
| Open - in uitvoering | Gebruikt        | Ja       | Gebruikt                            |
| Open - in uitvoering | Gebruikt        | Nee        | Gebruikt                            |
| Open - voltooid   | Geraamd   | Ja       | Geraamd                       |
| Open - voltooid   | Geraamd   | Nee        | Gebruikt                            |
| Open - voltooid   | Gebruikt        | Ja       | Gebruikt                            |
| Open - voltooid   | Gebruikt        | Nee        | Gebruikt                            |
| Gesloten - geboekt    | Geraamd   | Ja       | Gebruikt                            |
| Gesloten - geboekt    | Geraamd   | Nee        | Gebruikt                            |
| Gesloten - geboekt    | Gebruikt        | Ja       | Gebruikt                            |
| Gesloten - geboekt    | Gebruikt        | Nee        | Gebruikt                            |

De volgende tabel bevat een overzicht van de verschillende combinaties voor serviceregels.

| Systeemstatus <br>(Field Service) | Regelstatus <br>(Field Service) | Gesynchroniseerde waarde <br>(Finance and Operations) |
|--------------------|-------------|-----------|
| Open - gepland   | Geraamd   | Geraamd |
| Open - gepland   | Gebruikt        | Gebruikt      |
| Open - in uitvoering | Geraamd   | Geraamd |
| Open - in uitvoering | Gebruikt        | Gebruikt      |
| Open - voltooid   | Geraamd   | Geraamd |
| Open - voltooid   | Gebruikt        | Gebruikt      |
| Gesloten - geboekt    | Geraamd   | Gebruikt      |
| Gesloten - geboekt    | Gebruikt        | Gebruikt      |

Synchronisatie van **geraamde** waarden versus **gebruikte** waarden wordt beheerd met de twee sets taken voor productregels en serviceregels. Vooraf gedefinieerde filters starten de juiste taak en de onderliggende toewijzing zorgt dat de juiste waarden voor **Verwacht** versus **Gebruikt** worden gesynchroniseerd.

### <a name="example"></a>Voorbeeld

1. Een werkorder wordt gemaakt en gepland in het Field Service.

    De waarde voor **Systeemstatus** is **Open - gepland**.

    - **Productregel:** geschatte hoeveelheid = 5 st, gebruikte hoeveelheid = 0 st, regelstatus = geraamd, toegewezen = nee
    - **Serviceregel:** geraamde hoeveelheid = 2 uur, gebruikte hoeveelheid = 0 uur, regelstatus = geraamd

    In dit voorbeeld wordt de **Gebruikte hoeveelheid** van het product van **0** (nul) en de **Geraamde hoeveelheid** van **2 uur** gesynchroniseerd met Finance and Operations.

2. Producten worden toegewezen in Field Service.

    De waarde voor **Systeemstatus** is **Open - gepland**.

    - **Productregel:** geschatte hoeveelheid = 5 st, gebruikte hoeveelheid = 0 st, regelstatus = geraamd, toegewezen = ja
    - **Serviceregel:** geraamde hoeveelheid = 2 uur, gebruikte hoeveelheid = 0 uur, regelstatus = geraamd

    In dit voorbeeld wordt de **Geraamde hoeveelheid** van het product van **5 st** en de **Geraamde hoeveelheid** van **2 uur** gesynchroniseerd met Finance and Operations.

3. De onderhoudsmonteur begint te werken aam de werkorder en regsitreert materiaalgebruik van 6.

    De waarde voor **Systeemstatus** is **Open - in uitvoering**.

    - **Productregel:** geschatte hoeveelheid = 5 st, gebruikte hoeveelheid = 6 st, regelstatus = verbruikt, toegewezen = ja
    - **Serviceregel:** geraamde hoeveelheid = 2 uur, gebruikte hoeveelheid = 0 uur, regelstatus = geraamd

    In dit voorbeeld wordt de **Gebruikte hoeveelheid** van het product van **6** en de **Geraamde hoeveelheid** van **2 uur** gesynchroniseerd met Finance and Operations.

4. De onderhoudsmonteur voltooit de werkorder en registreert 1,5 uur gebruikt.

    De waarde voor **Systeemstatus** is **Open - voltooid**.

    - **Productregel:** geschatte hoeveelheid = 5 st, gebruikte hoeveelheid = 6 st, regelstatus = verbruikt, toegewezen = ja
    - **Serviceregel:** geraamde hoeveelheid = 2 uur, gebruikte hoeveelheid = 1,5 uur, regelstatus = gebruikt

    In dit voorbeeld wordt de **Gebruikte hoeveelheid** van het product van **6** en de **Geraamde hoeveelheid** van **1,5 uur** gesynchroniseerd met Finance and Operations.

## <a name="sales-order-origin-and-status"></a>Herkomst en status van verkooporder

### <a name="sales-origin"></a>Verkoopoorsprong

Om verkooporders in Finance and Operations bij te houden die afkomstig zijn van werkorders, kunt u een verkoopoorsprong maken waarin de optie **Toewijzing van oorsprongtype** is ingesteld op **Ja** en het veld **Type verkoopoorsprong** is ingesteld op **Integratie werkorder**.

Standaard wordt door de toewijzing de verkoopoorsprong voor **Integratie werkorder** geselecteerd voor alle verkooporders die zijn gemaakt op basis van werkorders. Dit gedrag kan van pas komen wanneer u werkt met de verkooporder in Finance and Operations. U moet ervoor zorgen dat verkooporders die afkomstig zijn van werkorders, niet terug worden gesynchroniseerd met Field Service als werkorders.

Zie de sectie 'Voorwaarden en instellingen voor toewijzing' in dit onderwerp voor meer informatie over het maken van de juiste instellingen voor verkoopoorsprong in Finance and Operations.

### <a name="status"></a>Status

Wanneer de verkooporder afkomstig is van een werkorder, verschijnt het veld **Externe werkorderstatus** op het tabblad **Instellen** in de verkooporderkoptekst. Dit veld bevat de systeemstatus van de werkorder in Field Service om de status van de gesynchroniseerde werkorders van verkooporders bij te houden in Finance and Operations. Dit veld kan de gebruiker van Finance and Operations ook helpen bepalen wanneer de verkooporder moet worden verzonden of gefactureerd.

het veld **Externe werkorderstatus** kan de volgende waarden hebben:

- Open - gepland
- Open - in uitvoering
- Open - voltooid
- Gesloten - geboekt

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing

Ter ondersteuning van de integratie tussen Field Service en Finance and Operations is extra functionaliteit nodig in de CRM-oplossing Field Service. Het oplossing omvat de volgende wijzigingen.

### <a name="work-order-entity"></a>Werkorderentiteit

Het veld **Heeft alleen extern onderhouden producten** is toegevoegd aan de entiteit **Werkorder** en wordt op de pagina weergegeven. Het wordt gebruikt om consistent bij te houden of een werkorder geheel uit extern onderhouden producten bestaat. Een werkorder bestaat alleen uit extern beheerde producten, als alle samenhangende producten worden onderhouden in Finance and Operations. Met deze veldt garandeert u dat gebruikers geen werkorders synchroniseren die producten bevatten die onbekend zijn in Finance and Operations.

### <a name="work-order-product-entity"></a>Entiteit werkorderproduct

- Het veld **Order heeft alleen extern onderhouden producten** is toegevoegd aan de entiteit **Werkorderproduct** en wordt op de pagina weergegeven. Het wordt gebruikt om consistent bij te houden of het product van de werkorder wordt beheerd in Finance and Operations. Met deze veldt garandeert u dat gebruikers geen werkorderproducten synchroniseren die onbekend zijn in Finance and Operations.
- Het veld **Koptekst systeemstatus** is toegevoegd aan de entiteit **Werkorderproduct** en wordt op de pagina weergegeven. het wordt gebruikt om de systeemstatus van de werkorder consistent bij te houden en zorgt voor de juiste filtering wanneer werkorderproducten worden gesynchroniseerd in Finance and Operations. Wanneer de filters zijn ingesteld op de integratietaken, worden de gegevens in **Koptekst systeemstatus** ook gebruikt om te bepalen of de geschatte of gebruikte waarden moeten worden gesynchroniseerd.
- Het veld **Gefactureerd bedrag per eenheid** bevat het bedrag dat wordt gefactureerd per werkelijke verbruikte eenheid. De waarde wordt berekend als de waarde voor **Totaalbedrag** gedeeld door de waarde van **Werkelijke hoeveelheid**. Het veld wordt gebruikt voor de integratie met systemen die geen verschillende waarden ondersteunen voor de verbruikte hoeveelheid en de gefactureerde hoeveelheid. Dit veld wordt niet weergegeven in de gebruikersinterface (UI). 
- Het veld **Gefactureerd kortingsbedrag** wordt berekend als de waarde van **Kortingsbedrag** plus de afronding van de berekening van de waarde **Gefactureerd bedrag per eenheid**. Dit veld wordt gebruikt voor integratie en wordt niet weergegeven in de gebruikersinterface.
- Het veld **Decimale hoeveelheid** bevat de waarde van het veld **Hoeveelheid** als een decimaal getal. Dit veld wordt gebruikt voor integratie en wordt niet weergegeven in de gebruikersinterface. 
- De waarde in de velden **Gebruikt** wordt opnieuw ingesteld op **0** (nul) als de waarde bij **Regelstatus** van het werkorderproduct wordt gewijzigd van **Gebruikt** naar **Geraamd**. Deze wijziging helpt situaties voorkomen waar een gebruikte hoeveelheid die per ongeluk is ingevoerd, wordt gebruikt voor synchronisatie wanneer de waarde bij **Regelstatus** **Geraamd** is en de **Toegewezen** is ingesteld op **Nee**.

### <a name="work-order-service-entity"></a>Entiteit werkorderservice

- Het veld **Order heeft alleen extern onderhouden producten** is toegevoegd aan de entiteit **Werkorderservice** en wordt op de pagina weergegeven. Het wordt gebruikt om consistent bij te houden of de service van de werkorder wordt beheerd in Finance and Operations. Met deze veldt garandeert u dat gebruikers geen werkorderservices synchroniseren die onbekend zijn in Finance and Operations.
- Het veld **Koptekst systeemstatus** is toegevoegd aan de entiteit **Werkorderservice** en wordt op de pagina weergegeven. het wordt gebruikt om de systeemstatus van de werkorder consistent bij te houden en zorgt voor de juiste filtering wanneer werkorderservices worden gesynchroniseerd in Finance and Operations. Wanneer de filters zijn ingesteld op de integratietaken, worden de gegevens in **Koptekst systeemstatus** ook gebruikt om te bepalen of de geschatte of gebruikte waarden moeten worden gesynchroniseerd.
- Het veld **Duur in uren** bevat de waarde van het veld **Duur** nadat de waarde is omgezet van minuten in uren. Dit veld wordt gebruikt voor integratie en wordt niet weergegeven in de gebruikersinterface.
- Het veld **Geschatte duur in uren** bevat de waarde van het veld **Geschatte duur** nadat de waarde is omgezet van minuten in uren. Dit veld wordt gebruikt voor integratie en wordt niet weergegeven in de gebruikersinterface.
- Het veld **Gefactureerd bedrag per eenheid** slaat het bedrag op dat wordt gefactureerd per werkelijke verbruikte eenheid. De waarde wordt berekend als de waarde voor **Totaalbedrag** gedeeld door de waarde van **Werkelijke hoeveelheid**. Dit veld wordt gebruikt voor de integratie met systemen die geen verschillende waarden ondersteunen voor de verbruikte hoeveelheid en de gefactureerde hoeveelheid. Het veld wordt niet weergegeven in de gebruikersinterface.
- Het veld **Gefactureerd kortingsbedrag** wordt berekend als de waarde van **Kortingsbedrag** plus de afronding van de berekening van de waarde **Gefactureerd bedrag per eenheid**. Dit veld wordt gebruikt voor integratie en wordt niet weergegeven in de gebruikersinterface.
- Het veld **Externe regelorder** is een berekende ordernummer op een negatieve regel dat kan worden gebruikt in externe systemen waarbij werkorderproduct- en serviceregels worden gecombineerd. Dit veld maakt werkorderproducten mogelijk die worden ingevoegd voor positieve regelnummers en werkorderservices voor negatieve regelnummers. De waarde van dit veld wordt berekend als de waarde bij **Regelorder** vermenigvuldigd met -1. Dit veld wordt niet weergegeven in de gebruikersinterface.
- De waarde in de velden **Gebruikt** wordt opnieuw ingesteld op **0** (nul) als de waarde bij **Regelstatus** van het werkorderservice om een bepaalde reden wordt gewijzigd van **Gebruikt** naar **Geraamd**. Deze wijziging helpt situaties voorkomen waar een gebruikte hoeveelheid die per ongeluk is ingevoerd, wordt gebruikt voor synchronisatie wanneer de waarde bij **Regelstatus** **Geraamd** is en de **Koptekst systeemstatus** is ingesteld op **Gesloten - geboekt**.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

Voordat u werkorders synchroniseert, is het belangrijk de volgende instellingen in de systemen bij te werken.

### <a name="setup-in-field-service"></a>Instellen in Field Service

- Zorg ervoor dat de nummerreeks die wordt gebruikt voor werkorders in Field Service niet overlapt met de nummerreeks die wordt gebruikt voor verkooporders in Finance and Operations. Anders kunnen bestaande verkooporders niet goed worden bijgewerkt in Field Service of Finance and Operations.
- Het veld **Werkorderfactuur maken** moet worden ingesteld op **Nooit**, omdat de facturering vanuit Finance and Operations wordt uitgevoerd. Ga naar **Field Service** \> **Instellingen** \> **Beheer** \> **Instellingen Field Service**, en controleer of het veld **Werkorderfactuur maken** is ingesteld op **Nooit**.

### <a name="setup-in-finance-and-operations"></a>Instellingen In Finance and Operations

Werkorderintegratie vereist dat u de verkoopoorsprong instelt. De verkoopoorsprong wordt gebruikt om onderscheid te maken tussen verkooporders in Finance and Operations die zijn gemaakt op basis van werkorders in Field Service. Wanneer een verkooporder een verkoopoorsprong heeft van het type **Integratie werkorder**, wordt het veld **Externe werkorderstatus** weergegeven in de verkooporderkoptekst. Bovendien helpt de verkoopoorsprong om verkooporders die zijn gemaakt op basis van werkorders in Field Service, eruit te filteren tijdens de synchronisatie van verkooporders Finance and Operations met Field Service.

1. Ga naar **Verkoop en marketing** \> **Instellen** \> **Verkooporders** \> **Verkoopoorsprong**.
2. Selecteer **Nieuw** voor het maken van een nieuwe verkoopoorsprong.
3. Voer in het veld **Verkoopoorsprong** een naam in voor de verkoopoorsprong, zoals **Werkorder**.
4. Voer in het veld **Omschrijving** een omschrijving in zoals **Werkorder Field Service**.
5. Schakel het selectievakje **Toewijzing van oorsprongtype** in.
6. Stel het veld **Type verkoopoorsprong** in op **Integratie werkorder**.
7. Selecteer **Opslaan**.


### <a name="setup-in-data-integration"></a>Instellingen in Gegevensintegratie

Controleer of de **Integratiesleutel** aanwezig is voor **msdyn_workorders**
1. Ga naar Gegevensintegratie
2. Selecteer het tabblad **Verbindingsset**
3. Selecteer de verbindingsset die wordt gebruikt voor synchronisatie van werksorders
4. Selecteer het tabblad **Integratiesleutel**
5. Zoek msdyn_workorders en controleer of de sleutel **msdyn_name (werkordernummer)** wordt toegevoegd. Als deze niet wordt weergegeven, voegt u deze toe door te klikken op **Sleutel toevoegen** en klikt u op **Opslaan** bovenaan de pagina

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderheader"></a>Werkorders aan verkooporders (Field Service aan Fin en Ops): WorkOrderHeader

Filter: (msdyn_systemstatus ne 690970005) en (msdyn_systemstatus ne 690970000) en (msdynce_hasexternallymaintainedproductsonly eq true)

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineestimate"></a>Werkorders aan verkooporders (Field Service aan Fin en Ops): WorkOrderServiceLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) en (msdynce_headersystemstatus ne 690970000) en (msdynce_orderhasexternalmaintainedproductsonly eq true) en (msdyn_linestatus eq 690970000) en (msdynce_headersystemstatus ne 690970004)

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineused"></a>Werkorders aan verkooporders (Field Service aan Fin en Ops): WorkOrderServiceLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) en (msdynce_headersystemstatus ne 690970000) en (msdynce_orderhasexternalmaintainedproductsonly eq true) en ((msdyn_linestatus eq 690970001) of (msdynce_headersystemstatus eq 690970004))

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineestimate"></a>Werkorders aan verkooporders (Field Service aan Fin en Ops): WorkOrderProductLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) en (msdynce_headersystemstatus ne 690970000) en (msdynce_orderhasexternalmaintainedproductsonly eq true) en (msdyn_linestatus eq 690970000) en (msdynce_headersystemstatus ne 690970004) en (msdyn_allocated eq true)

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineused"></a>Werkorders aan verkooporders (Field Service aan Fin en Ops): WorkOrderProductLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) en (msdynce_headersystemstatus ne 690970000) en (msdynce_orderhasexternalmaintainedproductsonly eq true) en ((msdyn_linestatus eq 690970001) of (msdynce_headersystemstatus eq 690970004) of (msdyn_allocated ne true))

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


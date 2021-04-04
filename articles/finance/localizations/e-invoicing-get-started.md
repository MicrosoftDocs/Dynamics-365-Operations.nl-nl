---
title: Aan de slag met de invoegtoepassing voor elektronische facturering
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 56227e031f8205836bcae9ce26006fc8091c2863
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592545"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Aan de slag met de invoegtoepassing voor elektronische facturering

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering.

In de volgende tabel worden de functies voor elektronische facturering en de bedrijfsdocumenten vermeld waarin deze kunnen worden toegepast.

| Functienaam                         | Bedrijfsdocument |
|--------------------------------------|-------------------|
| Elektronische facturen Oostenrijk (AT)    | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Elektronische factuur België (BE)      | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Braziliaans NF-e (BR)                  | <p>Fiscaal model 55-document</p><p>Correctiebrief</p> |
| Braziliaans NFS-e ABRASF Curitiba (BR) | Service belastingdocument |
| Elektronische factuur Denemarken (DK)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Elektronische factuur Egypte (EG)     | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Elektronische factuur Estland (EE)     | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Finse Elektronische factuur (FI)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Elektronische factuur Frankrijk (FR)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Elektronische factuur Duitsland (DE)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| FatturaPA (IT)                       | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Mexicaanse CFDI Interfactura (MX)       | <p>Verkoopfactuur</p><p>Pakbon</p><p>Voorraadoverdracht</p><p>Betalingscomplement</p> |
| Elektronische factuur Nederland (NL)        | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Elektronische factuur Noorwegen (NO)    | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| Elektronische factuur Spanje (ES)      | <p>Verkoopfactuur</p><p>Projectfactuur</p> |
| PEPPOL Elektronische factuur            | <p>Verkoopfactuur</p><p>Projectfactuur</p> |

## <a name="prerequisites"></a>Vereisten

Voordat u de procedures in dit onderwerp voltooit, moet aan de volgende vereisten zijn voldaan:

- Configureer uw Regulatory Configuration Service (RCS) en uw Microsoft Dynamics 365 Finance- of Dynamics 365 Supply Chain Management-omgeving, zodat u de invoegtoepassing voor elektronische facturering kunt indienen.
- Maak een serviceomgeving en publiceer deze naar de invoegtoepassing voor elektronische facturering. Zie [Aan de slag met servicebeheer van de invoegtoepassing voor elektronische facturering](e-invoicing-get-started-service-administration.md) voor meer informatie.
- Maak een verbonden toepassing. Zie [Aan de slag met servicebeheer van de invoegtoepassing voor elektronische facturering](e-invoicing-get-started-service-administration.md) voor meer informatie.
- Maak een configuratieprovider voor uw organisatie. Zie [Configuratieprovider maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Een elektronische factureringsfunctie vanuit de Microsoft-configuratieprovider importeren 

1. Meld u aan bij uw RCS-account (Regulatory Configuration Service).
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Invoegtoepassing voor elektronische facturering**.
3. Selecteer **Importeren** en vervolgens **Synchroniseren**.
4. Filter de kolom **Configuratieprovider** op de term **Microsoft**.
5. Selecteer de naam van een elektronische factureringsfunctie in de tabel aan het begin van dit onderwerp en selecteer **Importeren**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Een omgeving voor de elektronische factureringsfunctie onder uw organisatieprovider maken

1. Selecteer in RCS, in de sectie **Functies** van het werkgebied **Globalisatiefunctie** de tegel **Invoegtoepassing voor elektronische facturering**.
2. Selecteer **Toevoegen** > **Gebaseerd op bestaande functie** en voer in het veld **Naam** de naam van de elektronische factureringsfunctie in.
3. Voer in het veld **Omschrijving** een omschrijving in voor de functie.
4. Selecteer in het veld **Basisfunctie** de geïmporteerde elektronische factureringsfunctie van de Microsoft-configuratieprovider.
5. Selecteer **Functie maken**.

## <a name="configure-the-electronic-invoicing-feature"></a>De elektronische factureringsfunctie configureren

Afhankelijk van het land of de regio heeft de elektronische factureringsfunctie mogelijk extra configuratie nodig. 

Zie de documentatie 'Aan de slag' die beschikbaar is voor uw land of regio voor de specifieke stappen.

## <a name="configure-the-application-setup"></a>De instellingen van de toepassing configureren

1. Selecteer de elektronische factureringsfunctie die u hebt gemaakt.
2. Controleer op het tabblad **Versie** of de **concept** versie is geselecteerd.
3. Selecteer op het tabblad **Setups** de optie **Setup van de toepassing**.

    > [!NOTE]
    > Controleer of uw organisatie is ingesteld als de **Actieve** configuratieprovider. Zie [Configuratieprovider maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.

4. Selecteer **Functie-instellingen** en selecteer vervolgens **Verbonden toepassing**.
5. Selecteer in de sectie **Elektronische documenttypen** de optie **Toevoegen**.
6. Selecteer voor elk bedrijfsdocument dat door de functie wordt ondersteund, een waarde voor **Tabelnaam** volgens de volgende tabel en voer deze in.

    | Functienaam                         | Bedrijfsdocument | Tabelnaam |
    |--------------------------------------|-------------------|------------|
    | Elektronische facturen Oostenrijk (AT)    | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Elektronische factuur België (BE)      | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Braziliaans NF-e (BR)                  | <p>Belastingdocument</p><p>Correctiebrief</p> | Belastingdocument |
    | Braziliaans NFS-e ABRASF Curitiba (BR) | Service belastingdocument | Belastingdocument |
    | Elektronische factuur Denemarken (DK)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Elektronische factuur Egypte (EG)     | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Elektronische factuur Estland (EE)     | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Finse Elektronische factuur (FI)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Elektronische factuur Frankrijk (FR)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Elektronische factuur Duitsland (DE)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | FatturaPA (IT)                       | <p>Verkoopfactuur</p><p>Projectfactuur | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Mexicaanse CFDI Interfactura (MX)       | <p>Verkoopfactuur</p><p>Pakbon</p><p>Voorraadoverdracht</p><p>Betalingscomplement</p> | Klantfacturenjournaal |
    | Elektronische factuur Nederland (NL)        | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Elektronische factuur Noorwegen (NO)    | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | Elektronische factuur Spanje (ES)      | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |
    | PEPPOL Elektronische factuur            | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Klantfacturenjournaal</p><p>Projectfactuur</p> |

7. Selecteer voor elk bedrijfsdocument dat door de functie wordt ondersteund, een waarde voor **Context** volgens de volgende tabel en voer deze in.

    | Functienaam                         | Bedrijfsdocument | Context |
    |--------------------------------------|-------------------|---------|
    | Elektronische facturen Oostenrijk (AT)    | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Elektronische factuur België (BE)      | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Braziliaans NF-e (BR)                  | <p>Belastingdocument</p><p>Correctiebrief</p> | <p>Contextmodel klantfactuur – Context belastingdocument</p><p>Contextmodel klantfactuur – FD-correctiebriefcontext</p> |
    | Braziliaans NFS-e ABRASF Curitiba (BR) | Service belastingdocument| Contextmodel klantfactuur – Context belastingdocument |
    | Elektronische factuur Denemarken (DK)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Elektronische factuur Egypte (EG)     | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Elektronische factuur Estland (EE)     | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Finse Elektronische factuur (FI)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Elektronische factuur Frankrijk (FR)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Elektronische factuur Duitsland (DE)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | FatturaPA (IT)                       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Mexicaanse CFDI Interfactura (MX)       | <p>Verkoopfactuur</p><p>Pakbon</p><p>Voorraadoverdracht</p><p>Betalingscomplement</p> | Contextmodel klantfactuur – Context klantfactuur |
    | Elektronische factuur Nederland (NL)        | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Elektronische factuur Noorwegen (NO)    | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | Elektronische factuur Spanje (ES)      | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |
    | PEPPOL Elektronische factuur            | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Contextmodel klantfactuur – Context klantfactuur</p><p>Contextmodel klantfactuur – Context projectfactuur</p> |

8. Selecteer voor elk bedrijfsdocument dat door de functie wordt ondersteund, een waarde voor **Zakelijke documenttoewijzing** volgens de volgende tabel en voer deze in.

    | Functienaam                         | Bedrijfsdocument | Bedrijfsdocumenttoewijzing |
    |--------------------------------------|-------------------|---------------------------|
    | Elektronische facturen Oostenrijk (AT)    | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Elektronische factuur België (BE)      | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Braziliaans NF-e (BR)                  | <p>Belastingdocument</p><p>Correctiebrief</p> | <p>Fiscale documenttoewijzing – Fiscale documenttoewijzing</p><p>Toewijzing belastingdocument – correctiebrieftoewijzing</p> |
    | Braziliaans NFS-e ABRASF Curitiba (BR) | Service belastingdocument | Fiscale documenttoewijzing – Fiscale documenttoewijzing |
    | Elektronische factuur Denemarken (DK)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Elektronische factuur Egypte (EG)     | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Elektronische factuur Estland (EE)     | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Finse Elektronische factuur (FI)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Elektronische factuur Frankrijk (FR)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Elektronische factuur Duitsland (DE)       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | FatturaPA (IT)                       | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Mexicaanse CFDI Interfactura (MX)       | <p>Verkoopfactuur</p><p>Pakbon</p><p>Voorraadoverdracht</p><p>Betalingscomplement</p> | Factuurmodeltoewijzing – Klantfactuur |
    | Elektronische factuur Nederland (NL)        | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Elektronische factuur Noorwegen (NO)    | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | Elektronische factuur Spanje (ES)      | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |
    | PEPPOL Elektronische factuur            | <p>Verkoopfactuur</p><p>Projectfactuur</p> | <p>Factuurmodeltoewijzing – Klantfactuur</p><p>Factuurmodeltoewijzing – Projectfactuur</p> |

Afhankelijk van het land of de regio heeft de elektronische factureringsfunctie mogelijk extra configuratie nodig.

Zie de documentatie 'Aan de slag' die beschikbaar is voor uw land of regio voor specifieke stappen.

## <a name="deploy-the-electronic-invoicing-feature"></a>De elektronische factureringsfunctie implementeren

1. Selecteer op het tabblad **Versies** de versie van de elektronische factureringsfunctie die u wilt implementeren.
2. Selecteer **Status wijzigen** \> **Voltooien**.
3. Selecteer **Status wijzigen** \> **Publiceren**.
4. Selecteer **Implementeren**.
5. Stel de optie **Implementeren op verbonden toepassing** in op **Ja**.
6. Selecteer op de pagina **Toepassing verbinden** de verbinding die is gekoppeld aan uw exemplaar van Finance of Supply Chain Management.
7. Stel de optie **Implementeren op serviceomgeving** in op **Ja**.
8. Selecteer in het veld **Serviceomgeving** de omgeving van de invoegtoepassing voor elektronische facturering waarin u de elektronische factureringsfunctie wilt implementeren.
9. Selecteer in het veld **Vanaf datum** de datum waarop de functie voor elektronische facturering moet ingaan in de invoegvoeging voor elektronische facturering.
10. Selecteer **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>De elektronische factureringsfunctie inschakelen in Finance of Supply Chain Management

1. Meld u aan bij Finance of Supply Chain Management en controleer of u bij de juiste rechtspersoon bent.
2. Ga naar **Organisatiebeheer** \> **Instellen** \> **Parameters voor elektronische documenten**.
3. Selecteer op het tabblad **Functies** de land-/regiospecifieke functie om de functie voor elektronische facturering in te schakel voor Finance of Supply Chain Management. In de volgende tabel vindt u een lijst met de beschikbare functies voor elektronische facturering voor specifieke landen/regio's. 

    | Functienaam                                          | Land/regio  |
    |-------------------------------------------------------|-----------------|
    | Elektronische facturen Oostenrijk (AT)                     | Oostenrijk         |
    | Elektronische factuur België (BE)                       | België         |
    | CFDI Mexicaanse elektronische factuur (MX)                  | Mexico          |
    | Elektronische factuur Denemarken (DK)                        | Denemarken         |
    | Elektronische factuur Nederland (NL)                         | Nederland |
    | Elektronische factuur Egypte (EG)                      | Egypte           |
    | Elektronische factuur Estland (EE)                      | Estland         |
    | Elektronische factuur Finland (FI)                       | Finland         |
    | Elektronische factuur Frankrijk (FR)                        | Frankrijk          |
    | Elektronische factuur Duitsland (DE)                        | Duitsland         |
    | Elektronische factuur Italië (IT)                       | Italië           |
    | NF-e Federal - Braziliaanse elektronische factuur (BR)      | Brazilië          |
    | NFS-e - Elektronische factuur voor Braziliaanse service (plaats)   | Brazilië          |
    | Elektronische factuur Noorwegen (NO)                     | Noorwegen          |
    | PEPPOL Elektronische factuur                             | Algemeen          |
    | Elektronische factuur Spanje (ES)                       | Spanje           |

4. Selecteer **Opslaan**.

## <a name="issue-electronic-invoices"></a>Elektronische facturen uitgeven

1. Ga naar **Organisatiebeheer** \> **Periodiek** \> **Elektronische documenten** \> **Elektronische documenten indienen**.
2. Selecteer **Filter** op het sneltabblad **Op te nemen record**.
3. Selecteer **Toevoegen** om een tabelnaam aan het queryfilter toe te voegen.
4. Selecteer de tabel met de facturen.

    > [!NOTE]
    > De tabelnaam moet worden weergegeven in de tabel in de sectie [De instellingen van de toepassing configureren](#configure-the-application-setup) eerder in dit onderwerp.

5. Selecteer de veldnaam in de tabel waarop u de query wilt uitvoeren.
6. Voer de tabelnaam en veldnaam in voor de criteria waarop een query moet worden uitgevoerd.
7. Herhaal stap 5 en 6 om meer velden en criteria aan de query toe te voegen en selecteer **OK**.
8. Selecteer **OK**.

## <a name="view-submission-logs"></a>Indieningslogboeken weergeven

1. Ga naar **Organisatiebeheer** \> **Periodiek** \> **Elektronische documenten** \> **Indieningslogboek voor elektronische documenten**.
2. Selecteer in het veld **Documenttype** de tabel die de facturen bevat.

    > [!NOTE]
    > De tabelnaam moet worden weergegeven in de tabel in de sectie [De instellingen van de toepassing configureren](#configure-the-application-setup) eerder in dit onderwerp.

3. Selecteer een factuur in het raster en selecteer **Informatie opvragen** \> **Details van indiening**.


## <a name="related-topics"></a>Verwante onderwerpen

- [Overzicht van de invoegtoepassing voor elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met servicebeheer via de invoegtoepassing voor elektronische facturering](e-invoicing-get-started-service-administration.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering voor Brazilië](e-invoicing-bra-get-started.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering voor Mexico](e-invoicing-mex-get-started.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering voor Italië](e-invoicing-ita-get-started.md)
- [Elektronische klantfacturen in Egypte](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Aan de slag met de invoegtoepassing voor elektronische facturering voor Brazilië
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Brazilië in Finance en Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: eaf9433ad2d9ccf3d3c5632d0f2d4fe772ff8bde
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592665"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Aan de slag met de invoegtoepassing voor elektronische facturering voor Brazilië 

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met de invoegtoepassing voor elektronische facturering voor Brazilië. De procedures in dit onderwerp helpen u bij de configuratiestappen die landafhankelijk zijn in Regulatory Configuration Services (RCS) en vullen de stappen aan die worden beschreven in het onderwerp [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landspecifieke configuratie voor de Braziliaanse functie NF-e (BR) voor elektronische facturering

Voor de configuratie van de Braziliaanse functie NF-e (BR) voor elektronische facturering zijn specifieke stappen vereist. Sommige parameters van de configuraties worden met standaardwaarden gepubliceerd, dus ze moeten worden gecontroleerd en bijgewerkt om beter bij uw bedrijfsactiviteiten te passen.

### <a name="prerequisites"></a>Vereisten

Voordat u de procedure in deze sectie voltooit, maakt u een Braziliaanse functie NF-e (BR) voor elektronische facturering voor uw organisatie zoals beschreven in de sectie **Een functie voor elektronische facturering maken onder uw organisatieprovider** van het onderwerp [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS, in de sectie **Functies** van het werkgebied **Globalisatiefunctie** de tegel **Invoegtoepassing voor elektronische facturering**.
2. Controleer op de pagina **Invoegtoepassing voor functies voor elektronische facturering** of de functie voor elektronische facturering **Braziliaanse NF-e (BR)** die u hebt gemaakt is geselecteerd.
3. Controleer op het tabblad **Versies** of de **concept** versie is geselecteerd.
4. Ga naar het tabblad **Instellingen** en selecteer **Indienen** en vervolgens **Bewerken** in het raster.
5. Selecteer op het tabblad **Acties** in de veldgroep **Acties** de actie **(Preview) Xml-document ondertekenen**.
6. Selecteer in de veldgroep **Parameters** de optie **Certificaatnaam** en voer in het veld **Waarde** de naam in van het certificaat dat aan uw Key Vault-parameter is gekoppeld.
7. Selecteer op het tabblad **Acties** in de veldgroep **Acties** de actie **(Preview) Braziliaanse SEFAZ-service aanroepen**.
8. Selecteer in de veldgroep **Parameters** de parameter **URL-adres**.
9. Controleer indien nodig in het veld **Waarde** de URL van de webservices die door de SEFAZ-documentatie zijn gepubliceerd en selecteer vervolgens **Opslaan**.
10. Controleer op het tabblad **Toepasbaarheidsregels** in de veldgroep **Instellingen voor toepasbaarheidsregel** de criteria voor het veld **Status** die nodig zijn voor dezelfde status als waar de URL van de webservices naar verwijst.
11. Selecteer **Opslaan** en sluit de pagina.
12. Zie [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md) om de toepassingsinstellingen te configureren.

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landspecifieke configuratie van toepassingsinstellingen voor de Braziliaanse functie NF-e (BR) voor elektronische facturering

Voor de configuratie van de toepassingsinstellingen voor de Braziliaanse functie NF-e (BR) voor elektronische facturering zijn specifieke stappen vereist. Voltooi deze stappen voordat u de functie Elektronische facturering implementeert in de serviceomgeving voor uw invoegtoepassing Elektronische facturering.

### <a name="prerequisites"></a>Vereisten

Voordat u de procedure in deze sectie voltooit, maakt en initieert u de toepassingsconfiguratie van de Braziliaanse functie NF-e (BR) voor elektronische facturering zoals beschreven in de sectie **De toepassingsinstellingen configureren** in het onderwerp [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS, in de sectie **Functies** van het werkgebied **Globalisatiefunctie** de tegel **Invoegtoepassing voor elektronische facturering**.
2. Controleer op de pagina **Invoegtoepassing voor functies voor elektronische facturering** of de functie voor elektronische facturering **Braziliaanse NF-e (BR)** is geselecteerd.
3. Controleer op het tabblad **Versies** of de **concept** versie is geselecteerd.
4. Selecteer op het tabblad **Instellingen** de optie **Toepassingsinstellingen** en selecteer in het veld **Verbonden toepassing** de toepassing waarop u wilt implementeren.
5. Controleer in het veld **Tabelnaam** of **Koptekst fiscaal document** is geselecteerd.
6. Selecteer **Responstypen** en selecteer vervolgens **Nieuw**.
7. Voer in het veld **Responstype** de tekst "Respons" in als een vaste waarde in en voer in het veld **Beschrijving** de tekst "Beschrijving" in.
8. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
9. Selecteer in het veld **Modeltoewijzing** de optie **Modeltoewijzing van responsbericht** bij **(Preview) Importindeling responsbericht** en selecteer vervolgens **Opslaan**.
10. Selecteer **Nieuw** en voer in het veld **Responstype** de tekst "ResponseData" in als een vaste waarde in en voer in het veld **Beschrijving** de tekst "Beschrijving" in.
11. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
12. Selecteer in het veld **Modeltoewijzing** de optie **Responsgegevens importeren** bij **(Preview) Importindeling NF-e-responsgegevens** en selecteer vervolgens **Opslaan**.
13. Zie [Aan de slag met de invoegtoepassing Elektronische facturering](e-invoicing-get-started.md) voor de implementatie van de functie Elektronische facturering.

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landspecifieke configuratie voor de Braziliaanse functie NFS-e ABRASF Curitiba (BR) voor elektronische facturering

Voor de configuratie van de Braziliaanse functie NFS-e ABRASF Curitiba (BR) voor elektronische facturering zijn specifieke stappen vereist. Sommige parameters van de configuraties worden met standaardwaarden gepubliceerd, dus ze moeten worden gecontroleerd en bijgewerkt om beter bij uw bedrijfsactiviteiten te passen.

### <a name="prerequisites"></a>Vereisten

Voordat u de procedure in deze sectie voltooit, maakt u een Braziliaanse functie NFS-e ABRASF Curitiba (BR) voor elektronische facturering uw organisatie. Dit wordt beschreven in de sectie **Elektronische factureringsfunctie configureren** in het onderwerp [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS, in de sectie **Functies** van het werkgebied **Globalisatiefunctie** de tegel **Invoegtoepassing voor elektronische facturering**.
2. Controleer op de pagina **Functies van invoegtoepassing voor elektronische facturering** of de functie voor elektronische facturering **Braziliaanse NFS-e ABRASF Curitiba (BR)** die u hebt gemaakt is geselecteerd.
3. Controleer het tabblad **Versies** of de **conceptversie** is geselecteerd en selecteer vervolgens op het tabblad **Instellingen** in het raster de optie **Indienen**.
4. Selecteer **Bewerken** en selecteer op het tabblad **Acties** in de veldgroep **Acties** het eerste exemplaar van **(Preview) Xml-document ondertekenen**.
5. Selecteer in de veldgroep **Parameters** de optie **Certificaatnaam**.
6. Voer in het veld **Waarde** de naam van het certificaat in dat is gekoppeld aan uw Key Vault-parameter.
7. Selecteer in de veldgroep **Acties** het tweede exemplaar van **(Preview) Xml-document ondertekenen**.
8. Selecteer in de veldgroep **Parameters** de optie **Certificaatnaam**.
9. Voer in het veld **Waarde** de naam van het certificaat in dat is gekoppeld aan uw Key Vault-parameter.
10. Selecteer op het tabblad **Acties** in de veldgroep **Acties** de actie **(Preview) Braziliaanse SEFAZ-service aanroepen**.
11. Selecteer in de veldgroep **Parameters** de parameter **URL-adres**.
12. Controleer en werk indien nodig in het veld **Waarde** de URL bij van de webservices die door de belastingafdeling zijn gepubliceerd voor de stad Curitiba en selecteer vervolgens **Opslaan**.
13. Ga naar het tabblad **Instellingen** en selecteer **Informatie opvragen** en vervolgens **Bewerken** in het raster.
14. Selecteer op het tabblad **Acties** in de veldgroep **Acties** de actie **(Preview) Braziliaanse SEFAZ-service aanroepen**.
15. Selecteer in de veldgroep **Parameters** de parameter **URL-adres**.
16. Controleer en werk indien nodig in het veld **Waarde** de URL bij van de webservices die door de belastingafdeling zijn gepubliceerd voor de stad Curitiba.
17. Selecteer **Opslaan** en sluit de pagina.
18. Zie [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md) om de toepassingsinstellingen te configureren.

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landspecifieke configuratie van de toepassingsinstellingen voor de Braziliaanse functie NFS-e ABRASF Curitiba (BR) voor elektronische facturering

Als u de toepassingsinstellingen voor de elektronische factureringsfunctie (NFS-e A LISASF Curitiba) voor elektronische facturering wilt configureren, moeten specifieke stappen worden uitgevoerd voordat u de functie voor elektronische facturering implementeert in de serviceomgeving voor uw invoegtoepassing voor elektronische facturering.

### <a name="prerequisites"></a>Vereisten

Voordat u de procedure in deze sectie voltooit, maakt en initieert u de toepassingsconfiguratie van de Braziliaanse functie NFS-e ABRASF Curitiba (BR) voor elektronische facturering zoals beschreven in de sectie **De toepassingsinstellingen configureren** in het onderwerp [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS, in de sectie **Functies** van het werkgebied **Globalisatiefunctie** de tegel **Invoegtoepassing voor elektronische facturering**.
2. Controleer op de pagina **Functies van invoegtoepassing voor elektronische facturering** of de functie voor elektronische facturering **Braziliaanse NFS-e ABRASF Curitiba (BR)** is geselecteerd.
3. Controleer het tabblad **Versies** of de **conceptversie** is geselecteerd en selecteer vervolgens op het tabblad **Instellingen** in het raster de optie **Toepassingsinstelling**.
4. Selecteer in het veld **Verbonden toepassing** de toepassing die u wilt implementeren.
5. Controleer in het veld **Tabelnaam** of de koptekst voor fiscaal document is geselecteerd.
6. Selecteer **Responstypen** en selecteer **Nieuw**.
7. Voer in het veld **Responstype** de tekst "ABRASFCuritibaSubmitResponse" in als een vaste waarde in en voer in het veld **Beschrijving** de tekst "Beschrijving" in.
8. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
9. Selecteer in het veld **Modeltoewijzing** de optie **Responsbericht importeren** bij **(Preview) Responsbericht importeren voorNFS-e ABRASF Curitiba (BR)** en selecteer vervolgens **Opslaan**.
10. Selecteer **Nieuw** en voer in het veld **Responstype** de tekst "ABRASFCuritibaSubmitResponseData" in als een vaste waarde in en voer in het veld **Beschrijving** de tekst "Beschrijving" in.
11. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
12. Selecteer in het veld **Modeltoewijzing** de optie **Responsgegevens importeren** bij **(Preview) Importindeling NFS-e ABRASF-responsgegevens** en selecteer vervolgens **Opslaan**.
13. Selecteer **Nieuw** en voer in het veld **Responstype** de tekst "ABRASFCuritibaInquireResponse" in als een vaste waarde in en voer in het veld **Beschrijving** de tekst "Beschrijving" in.
14. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
15. Selecteer in het veld **Modeltoewijzing** de optie **Responsbericht importeren** bij **(Preview) Responsbericht importeren voorNFS-e ABRASF Curitiba (BR)**.
16. Selecteer **Opslaan** en ga vervolgens terug naar het onderwerp [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md) om de functie voor elektronische facturering te implementeren.

## <a name="privacy-notice"></a>Privacyverklaring
Als u de functies **NF-e Federal - Braziliaanse elektronische factuur (BR)** en **NFS-e - Braziliaanse service (plaats) elektronische factuur** wilt inschakelen, moeten mogelijk beperkte gegevens worden verzonden, waaronder de belastingregistratie-id voor de organisatie. Deze gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd elektronische facturen naar de belastingdienst te verzenden in de vooraf gedefinieerde indeling die nodig is voor integratie met de webservice van de overheid. Als beheerder kunt u de functies **NF-e Federal - Braziliaanse Elektronische factuur (BR)** en **NFS-e - Braziliaanse service (plaats) elektronische factuur** in- of uitschakelen. Hiervoor moeten de volgende stappen worden uitgevoerd: 

1. Ga naar **Organisatiebeheer** > **Instellen** > **Parameters voor elektronische documenten**. 
2. Selecteer op het tabblad **Functies** de rij met de functie **NF-e Federal - Braziliaanse elektronische factuur (BR)** of **NFS-e - Braziliaanse service (plaats) elektronische factuur** en selecteer de functie. Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service , is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de secties met betrekking tot de Privacyverklaring in documentatie over landspecifieke functies voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van de invoegtoepassing voor elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met servicebeheer via de invoegtoepassing voor elektronische facturering](e-invoicing-get-started-service-administration.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

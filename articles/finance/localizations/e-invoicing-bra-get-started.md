---
title: Aan de slag met Elektronische facturering voor Brazilië
description: Dit artikel bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Brazilië in Finance en Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 74debbca4ee365e05f1c15d45179f0cd1d23c3e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846579"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>Aan de slag met Elektronische facturering voor Brazilië 

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Brazilië. Dit artikel leidt u door de configuratiestappen die landafhankelijk zijn in Regulatory Configuration Services (RCS) en vullen de stappen aan die worden beschreven in [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landspecifieke configuratie voor de Braziliaanse functie NF-e (BR) voor elektronische facturering

Sommige parameters van de **Braziliaanse functie NF-e (BR) voor elektronische facturering** worden met standaardwaarden gepubliceerd. Controleer de waarden en werk ze zo nodig bij zodat deze beter aansluiten bij uw zakelijke bewerkingsbehoeften voordat u de functie Elektronische facturering in de serviceomgeving implementeert.

Deze sectie is een aanvulling op de sectie **Landspecifieke configuratie voor de functie voor elektronische facturering** in het artikel [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
2. Controleer op de pagina **Functies voor elektronische facturering** of de functie voor elektronische facturering **Braziliaanse NF-e (BR)** die u hebt gemaakt, is geselecteerd.
3. Controleer op het tabblad **Versies** of de **concept** versie is geselecteerd.
4. Ga naar het tabblad **Instellingen** en selecteer **Indienen** en vervolgens **Bewerken** in het raster.
5. Selecteer op het tabblad **Acties** in de veldgroep **Acties** de actie **(Preview) Xml-document ondertekenen**.
6. Selecteer in de veldgroep **Parameters** de optie **Certificaatnaam** en voer in het veld **Waarde** de naam in van het certificaat dat aan uw Key Vault-parameter is gekoppeld.
7. Selecteer op het tabblad **Acties** in de veldgroep **Acties** de actie **(Preview) Braziliaanse SEFAZ-service aanroepen**.
8. Selecteer in de veldgroep **Parameters** de parameter **URL-adres**.
9. Controleer indien nodig in het veld **Waarde** de URL van de webservices die door de SEFAZ-documentatie zijn gepubliceerd en selecteer vervolgens **Opslaan**.
10. Controleer op het tabblad **Toepasbaarheidsregels** in de veldgroep **Instellingen voor toepasbaarheidsregel** de criteria voor het veld **Status** die nodig zijn voor dezelfde status als waar de URL van de webservices naar verwijst.
11. Selecteer **Opslaan** en sluit de pagina.
12. Zie [Aan de slag met de invoegtoepassing Elektronische facturering](e-invoicing-get-started.md) voor de implementatie van de functie Elektronische facturering in de sericeomgeving.

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landspecifieke configuratie van toepassingsinstellingen voor de Braziliaanse functie NF-e (BR) voor elektronische facturering

Voltooi deze stappen voordat u de toepassingsinstellingen implementeert naar uw verbonden toepassing Finance of Supply Chain Management.

Deze sectie is een aanvulling op de sectie **Landspecifieke configuratie van toepassingsinstellingen** in het artikel [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
2. Controleer op de pagina **Functies voor elektronische facturering** of de functie voor elektronische facturering **Braziliaanse NF-e (BR)** is geselecteerd.
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
13. Zie [Aan de slag met Elektronische facturering](e-invoicing-get-started.md) om de toepassingsinstellingen te implementeren in de verbonden toepassing Finance of Supply Chain Management.

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landspecifieke configuratie voor de Braziliaanse functie NFS-e ABRASF Curitiba (BR) voor elektronische facturering

Sommige parameters van de **Braziliaanse functie NFS-e ABRASF Curitiba (BR) voor elektronische facturering** worden met standaardwaarden gepubliceerd. Controleer deze waarden en werk ze zo nodig bij zodat deze beter aansluiten bij uw zakelijke bewerkingsbehoeften voordat u de functie Elektronische facturering in de serviceomgeving implementeert.

Deze sectie is een aanvulling op de sectie **Landspecifieke configuratie voor de functie voor elektronische facturering** in het artikel [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
2. Controleer op de pagina **Functies voor elektronische facturering** of de functie voor elektronische facturering **Braziliaanse NFS-e ABRASF Curitiba (BR)** die u hebt gemaakt, is geselecteerd.
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
18. Zie [Aan de slag met de invoegtoepassing Elektronische facturering](e-invoicing-get-started.md) voor de implementatie van de functie Elektronische facturering in de sericeomgeving.

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landspecifieke configuratie van de toepassingsinstellingen voor de Braziliaanse functie NFS-e ABRASF Curitiba (BR) voor elektronische facturering

Voltooi deze stappen voordat u de toepassingsinstellingen implementeert naar uw verbonden toepassing Finance of Supply Chain Management.

Deze sectie is een aanvulling op de sectie **Landspecifieke configuratie van toepassingsinstellingen** in het artikel [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
2. Controleer op de pagina **Functies voor elektronische facturering** of de functie voor elektronische facturering **Braziliaanse NFS-e ABRASF Curitiba (BR)** is geselecteerd.
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
16. Selecteer **Opslaan** en sluit de pagina.
17. Zie [Aan de slag met Elektronische facturering](e-invoicing-get-started.md) om de toepassingsinstellingen te implementeren in de verbonden toepassing Finance of Supply Chain Management.

## <a name="privacy-notice"></a>Privacyverklaring
Als u de functies **NF-e Federal - Braziliaanse elektronische factuur (BR)** en **NFS-e - Braziliaanse service (plaats) elektronische factuur** wilt inschakelen, moeten mogelijk beperkte gegevens worden verzonden, waaronder de belastingregistratie-id voor de organisatie. Deze gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd elektronische facturen naar de belastingdienst te verzenden in de vooraf gedefinieerde indeling die nodig is voor integratie met de webservice van de overheid. Als beheerder kunt u de functies **NF-e Federal - Braziliaanse Elektronische factuur (BR)** en **NFS-e - Braziliaanse service (plaats) elektronische factuur** in- of uitschakelen. Hiervoor moeten de volgende stappen worden uitgevoerd: 

1. Ga naar **Organisatiebeheer** > **Instellen** > **Parameters voor elektronische documenten**. 
2. Selecteer op het tabblad **Functies** de rij met de functie **NF-e Federal - Braziliaanse elektronische factuur (BR)** of **NFS-e - Braziliaanse service (plaats) elektronische factuur** en selecteer de functie. Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service , is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de secties met betrekking tot de Privacyverklaring in documentatie over landspecifieke functies voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van Elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met servicebeheer voor Elektronische facturering](e-invoicing-get-started-service-administration.md)
- [Aan de slag met Elektronische facturering](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

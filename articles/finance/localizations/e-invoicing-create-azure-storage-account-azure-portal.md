---
title: Een Azure-opslagaccount maken in de Azure-portal
description: In dit artikel wordt uitgelegd hoe u een Azure-opslagaccount voor Elektronische facturering maakt.
author: gionoder
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5eca23985c48f4e577bd4567cc2e324df5aa9690
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291631"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Een Azure-opslagaccount maken in de Azure-portal

[!include [banner](../includes/banner.md)]

Alle elektronische bestanden die worden gegenereerd door de Elektronische factureringsservice of naar de service gaan tijdens de verwerking, worden opgeslagen in uw Microsoft Azure-opslagaccountcontainers. Om ervoor te zorgen dat elektronische facturering toegang heeft tot deze containers, moet u het SAS-token (Shared Access Signature) van het opslagaccount aan de elektronische factureringsservice verstrekken. Geef het SAS-token bovendien niet rechtstreeks op om dit veilig op te slaan. Sla het token op in een Azure Key Vault en geef een Azure Key Vault-geheim op.

1. Open het opslagaccount dat u wilt gebruiken met de invoegtoepassing voor elektronische factureringsservice.
2. Ga naar **Instellingen** \> **Configuratie** en zorg ervoor dat de parameter **Openbare toegang tot blob toestaan** is ingesteld op **Ingeschakeld**.
3. Ga naar **Gegevensopslag** \> **Containers** en maak een nieuwe container aan.
4. Voer een naam in voor de container en stel het veld **Openbaar toegangsniveau** in op **Privé (geen anonieme toegang)**.
5. Open de container en ga naar **Instellingen** \> **Toegangsbeleid**.
6. Selecteer **Beleid toevoegen** om een opgeslagen toegangsbeleid toe te voegen.
7. Stel het veld **id** in op de juiste waarde.
8. In het veld **Machtigingen** moet u alle machtigingen selecteren.

    ![Alle machtigingen geselecteerd in het veld Machtigingen in het dialoogvenster Beleid toevoegen.](media/e-invoicing-azure-1.png)

9. Voer de begin- en einddatum in. De einddatum moet in de toekomst liggen.
10. Selecteer **OK** om het beleid op te slaan en sla uw wijzigingen vervolgens op in de container.
11. Ga naar **Instellingen** \> **Gedeelde toegangstokens** en stel de veldwaarden in.
12. Voer de begin- en einddatum in. De einddatum moet in de toekomst liggen.
13. In het veld **Machtigingen** moet u de volgende machtigingen selecteren:

    - Lezen
    - Toevoegen
    - Maken
    - Wegschrijven
    - Verwijderen
    - Lijst

14. Selecteer **HET SAS-token en de URL genereren**.
15. Kopieer de waarde en sla deze op in het veld **Blob SAS-URL**. Deze waarde wordt later in de deze procedure gebruikt en wordt de *Shared Access Signature-URI* genoemd.
16. Open de sleutelkluis die u wilt gebruiken met Elektronische facturering.
17. Ga naar **Instellingen** \> **Geheimen** en selecteer **Genereren/importeren** om een geheim te maken.
18. Selecteer op de pagina **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.
19. Voer de naam van het geheim in. Deze naam wordt gebruikt tijdens de installatie van de service in Regulatory Configuration Service (RCS) en wordt de *geheime naam van de sleutelkluis* genoemd. Zie [Regulatory Configuration Services (RCS)](e-invoicing-set-up-rcs.md) voor meer informatie over RCS.
20. Voer in het veld **Waarde** de Shared Access Signature-URI in die u eerder hebt gekopieerd.
21. Selecteer **Maken**.

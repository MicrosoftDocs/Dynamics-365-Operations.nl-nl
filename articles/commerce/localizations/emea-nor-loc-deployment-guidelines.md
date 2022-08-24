---
ms.openlocfilehash: b17bd56f9f3e4def341658626915adbd7f5aada6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281533"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Implementatierichtlijnen voor kassa's voor Noorwegen (verouderd)
---

titel: Implementatierichtlijnen voor kassa's voor Noorwegen (verouderd) [!include [banner](../includes/banner.md)]
omschrijving: Dit artikel is een implementatiehandleiding die laat zien hoe u de lokalisatie van Microsoft Dynamics 365 Commerce voor Noorwegen kunt inschakelen.

auteur: EvgenyPopovMBS Dit artikel is een implementatiehandleiding die laat zien hoe u de lokalisatie van Microsoft Dynamics 365 Commerce voor Noorwegen kunt inschakelen. De lokalisatie bestaat uit verschillende extensies van Commerce-onderdelen. Met de extensies kunt u bijvoorbeeld aangepaste velden afdrukken op ontvangstbewijzen, extra controlegebeurtenissen, verkooptransacties en betalingstransacties registreren in POS (Point-of-Sale), verkooptransacties digitaal ondertekenen en X- en Z-rapporten afdrukken in lokale indelingen. Zie [Kassafunctionaliteit voor Noorwegen](./emea-nor-cash-registers.md) voor meer informatie over de lokalisatie voor Noorwegen.
ms.datum: 20-12-2021

ms.topic: artikel Dit voorbeeld maakt deel uit van de Retail Software Development Kit (SDK). Zie de [Architectuur van Retail SDK (Software Development Kit)](../dev-itpro/retail-sdk/retail-sdk-overview.md) voor informatie over het installeren en gebruiken van de SDK.
doelgroep: Gebruiker toepassing, Developer, IT Pro

ms.reviewer: v-chgriffin Dit voorbeeld bestaat uit extensies voor Commerce runtime (CRT), Retail Server en POS. Als u dit voorbeeld wilt uitvoeren, moet u de CRT-, Retail Server- en POS-projecten wijzigen en bouwen. Het is raadzaam een niet-geverifieerde Retail SDK te gebruiken om de wijzigingen aan te brengen die in dit artikel worden beschreven. Het wordt ook aangeraden een broncontrolesysteem te gebruiken, zoals Microsoft Visual Studio Online (VSO) wanneer er nog geen bestanden zijn gewijzigd.
ms.search.region: Globaal

ms.author: josaw
> [!NOTE]
ms.search.validFrom:2018-02-28 In Commerce 10.0.8 en hoger staat Retail Server bekend als Commerce Scale Unit. Aangezien dit artikel van toepassing is op meerdere eerdere versies van de app, wordt overal in het artikel *Retail Server* gebruikt.
>
---
> Sommige stappen in de procedures in dit artikel verschillen, afhankelijk van de versie van Commerce die u gebruikt. Zie [Nieuwe of gewijzigde functies in Dynamics 365 Retail](../get-started/whats-new.md) voor meer informatie.


6. Werk het configuratiebestand voor Retail Server bij. Voeg de volgende regels toe aan de sectie **extensionComposition** van het configuratiebestand **RetailSDK\\Packages\\RetailServer\\Code\\web.config**.
### <a name="using-certificate-profiles-in-commerce-channels"></a>Certificaatprofielen gebruiken in Commerce-kanalen


    ``` xml
In Commerce-versies 10.0.15 en hoger kunt u de functie [Door gebruiker gedefinieerde certificaatprofielen voor winkels](./certificate-profiles-for-retail-stores.md) gebruiken die van failover tot offline ondersteunt wanneer de Sleutelkluis of Commerce Headquarters niet beschikbaar zijn. Met deze functie wordt de functie [Geheimen voor detailhandelkanalen beheren](../dev-itpro/manage-secrets.md) uitgebreid.
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />

    ```
Voer de volgende stappen uit om deze functionaliteit toe te passen in de CRT-extensie.


7. Voer **msbuild** uit voor de hele Retail SDK om implementeerbare pakketten te maken.
1. Maak een nieuw CRT-extensieproject (projecttype C#-klassebibliotheek). Gebruik de voorbeeldsjablonen van de Retail Software Development Kit (SDK) (RetailSDK\SampleExtensions\CommerceRuntime).
8. Pas de pakketten toe via Microsoft Dynamics Lifecycle Services (LCS) of handmatig. Zie [Implementeerbare pakketten maken](../dev-itpro/retail-sdk/retail-sdk-packaging.md) voor meer informatie.


2. Aangepaste handler toevoegen voor CertificateSignatureServiceRequest in het project SequentialSignatureRegister.
### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>De digitale handtekening inschakelen in de offline modus voor Modern POS


3. Voor het lezen van een geheime aanroep, `GetUserDefinedSecretCertificateServiceRequest` met behulp van een constructor met profileId-parameter. Hiermee wordt de functionaliteit gestart met instellingen uit certificaatprofielen. Op basis van de instellingen wordt het certificaat opgehaald uit Azure Key Vault of lokale machineopslag.
Als u de digitale handtekening wilt inschakelen in de offline modus voor Modern POS, moet u deze stappen volgen nadat u Modern POS hebt geactiveerd op een nieuw apparaat.


    ```csharp
1. Sign in to POS.
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
2. On the **Database connection status** page, make sure that the offline database is fully synchronized. When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);
3. Sign out of POS.

4. Wait a while for the offline database to be fully synchronized.
    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
5. Sign in to POS.
    ```
6. Zorg er op de pagina **Databaseverbindingsstatus** voor dat de offline database volledig is gesynchroniseerd. Wanneer de waarde van het veld **Transacties zijn in behandeling in offlinedatabase** gelijk is aan **0** (nul), is de database volledig gesynchroniseerd.

7. Start Modern POS opnieuw.
4. Ga door met het ondertekenen van gegevens nadat het certificaat is opgehaald.



5. Bouw het CRT-extensieproject.
[!INCLUDE[footer-include](../../includes/footer-banner.md)]

6. Kopieer de uitvoerklassebibliotheek en plak deze in ...\RetailServer\webroot\bin\Ext voor handmatig testen.

7. Werk in het bestand CommerceRuntime.Ext.config het gedeelte voor het samenstellen van de extensie bij met de aangepaste bibliotheekgegevens.

## <a name="development-environment"></a>Ontwikkelingsomgeving

Voltooi deze procedures om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

### <a name="the-crt-extension-components"></a>De onderdelen van de CRT-extensie

De CRT-extensieonderdelen zijn opgenomen in de CRT-voorbeelden. Als u de volgende procedures wilt uitvoeren, opent u de CRT-oplossing **CommerceRuntimeSamples.sln** onder **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>Onderdeel ReceiptsNorway

1. Zoek het project **Runtime.Extensions.ReceiptsNorway** en bouw het.
2. Zoek in de map **Extensions.ReceiptsNorway\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.ReceiptsNorway.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de Microsoft internet Information Services (IIS)-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="salespaymenttransext-component"></a>Onderdeel SalesPaymentTransExt

1. Zoek het project **Runtime.Extensions.SalesPaymentTransExt** en bouw het.
2. Zoek in de map **Extensions.SalesPaymentTransExt\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="xzreportsnorway-component"></a>Onderdeel XZReportsNorway

1. Zoek het project **Runtime.Extensions.XZReportsNorway** en bouw het.
2. Zoek in de map **Extensions.XZReportsNorway\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.XZReportsNorway.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

# <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>Voorbeeldonderdeel RegisterAuditEvent

1. Zoek het project **Runtime.Extensions.RegisterAuditEventSample** en bouw het.
2. Zoek in de map **Extensions.RegisterAuditEventSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="salestransactionsignature-sample-component"></a>Voorbeeldonderdeel SalesTransactionSignature

1. Zoek het project **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Wijzig het bestand **App.config** door de vingerafdruk, winkellocatie en winkelnaam op te geven voor het certificaat dat moet worden gebruikt om verkooptransacties te ondertekenen.
3. Bouw het project.
4. Zoek de volgende bestanden in de map **Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

    - Het assemblagebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Het configuratiebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopieer de bestanden naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

6. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

7. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

# <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>Voorbeeldonderdeel RegisterAuditEvent

1. Zoek het project **Runtime.Extensions.RegisterAuditEventSample** en bouw het.
2. Zoek in de map **Extensions.RegisterAuditEventSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="salestransactionsignature-sample-component"></a>Voorbeeldonderdeel SalesTransactionSignature

1. Zoek het project **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Wijzig het bestand **App.config** door de vingerafdruk, winkellocatie en winkelnaam op te geven voor het certificaat dat moet worden gebruikt om verkooptransacties te ondertekenen.
3. Bouw het project.
4. Zoek de volgende bestanden in de map **Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

    - Het assemblagebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Het configuratiebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopieer de bestanden naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

6. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

7. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="salestransactionsignaturesamplemessages-component"></a>Onderdeel SalesTransactionSignatureSample.Messages

1. Zoek het project **Runtime.Extensions.SalesTransactionSignatureSample.Messages**.
2. Zoek in de map **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>Voorbeeldonderdeel RegisterAuditEvent

1. Zoek het project **Runtime.Extensions.RegisterAuditEventSample** en bouw het.
2. Zoek in de map **Extensions.RegisterAuditEventSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="salestransactionsignature-sample-component"></a>Voorbeeldonderdeel SalesTransactionSignature

1. Zoek het project **Runtime.Extensions.SalesTransactionSignatureSample**.
2. Wijzig het bestand **App.config** door de vingerafdruk, winkellocatie en winkelnaam op te geven voor het certificaat dat moet worden gebruikt om verkooptransacties te ondertekenen.
3. Bouw het project.
4. Zoek de volgende bestanden in de map **Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

    - Het assemblagebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Het configuratiebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopieer de bestanden naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

6. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

7. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="sequentialsignatureregistercontracts-component"></a>Onderdeel SequentialSignatureRegister.Contracts

1. Zoek het project **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Zoek in de map **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>Voorbeeldonderdeel RegisterAuditEvent

1. Zoek het project **Runtime.Extensions.RegisterAuditEventSample** en bouw het.
2. Zoek in de map **Extensions.RegisterAuditEventSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="sequentialsignatureregister-component"></a>Onderdeel SequentialSignatureRegister

1. Zoek het project **Runtime.Extensions.SequentialSignatureRegister**.
2. Wijzig het bestand **App.config** door de vingerafdruk, winkellocatie en winkelnaam op te geven voor het certificaat dat moet worden gebruikt om verkooptransacties te ondertekenen.
3. Bouw het project.
4. Zoek de volgende bestanden in de map **Extensions.SequentialSignatureRegister\\bin\\Debug**:

    - Het assemblagebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Het configuratiebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopieer de bestanden naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

6. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

7. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="salestransactionsignaturenorway-component"></a>Onderdeel SalesTransactionSignatureNorway

1. Zoek het project **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Zoek in de map **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="sequentialsignatureregistercontracts-component"></a>Onderdeel SequentialSignatureRegister.Contracts

1. Zoek het project **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Zoek in de map **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

#### <a name="salespaymenttransextnorway-component"></a>Onderdeel SalesPaymentTransExtNorway

1. Zoek het project **Runtime.Extensions.SalesPaymentTransExtNorway** en bouw het.
2. Zoek in de map **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>Onderdeel RegisterAuditEventNorway

1. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

2. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="sequentialsignatureregister-component"></a>Onderdeel SequentialSignatureRegister

1. Zoek het project **Runtime.Extensions.SequentialSignatureRegister**.
2. Wijzig het bestand **App.config** door de vingerafdruk, winkellocatie en winkelnaam op te geven voor het certificaat dat moet worden gebruikt om verkooptransacties te ondertekenen.
3. Bouw het project.
4. Zoek de volgende bestanden in de map **Extensions.SequentialSignatureRegister\\bin\\Debug**:

    - Het assemblagebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Het configuratiebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopieer de bestanden naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

6. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

7. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="salestransactionsignaturenorway-component"></a>Onderdeel SalesTransactionSignatureNorway

1. Zoek het project **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Zoek in de map **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="sequentialsignatureregistercontracts-component"></a>Onderdeel SequentialSignatureRegister.Contracts

1. Zoek het project **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Zoek in de map **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

#### <a name="salespaymenttransextnorway-component"></a>Onderdeel SalesPaymentTransExtNorway

1. Zoek het project **Runtime.Extensions.SalesPaymentTransExtNorway** en bouw het.
2. Zoek in de map **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>Onderdeel RegisterAuditEventNorway

1. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

2. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="sequentialsignatureregister-component"></a>Onderdeel SequentialSignatureRegister

1. Zoek het project **Runtime.Extensions.SequentialSignatureRegister**.
2. Wijzig het bestand **App.config** door de vingerafdruk, winkellocatie en winkelnaam op te geven voor het certificaat dat moet worden gebruikt om verkooptransacties te ondertekenen.
3. Bouw het project.
4. Zoek de volgende bestanden in de map **Extensions.SequentialSignatureRegister\\bin\\Debug**:

    - Het assemblagebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Het configuratiebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopieer de bestanden naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

6. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

7. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="salestransactionsignaturenorway-component"></a>Onderdeel SalesTransactionSignatureNorway

1. Zoek het project **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. Zoek in de map **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

#### <a name="sequentialsignatureregistercontracts-component"></a>Onderdeel SequentialSignatureRegister.Contracts

1. Zoek het project **Runtime.Extensions.SequentialSignatureRegister.Contracts**.
2. Zoek in de map **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

#### <a name="salespaymenttransextnorway-component"></a>Onderdeel SalesPaymentTransExtNorway

1. Zoek het project **Runtime.Extensions.SalesPaymentTransExtNorway** en bouw het.
2. Zoek in de map **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Retail Server:** kopieer de assembly naar de map **\\bin\\ext** onder de locatie van de IIS-retailserver.
    - **Lokale CRT op Modern POS:** kopieer het assemblagebestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Retail Server:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Retail Server van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Bewerk de bestanden commerceruntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

---

### <a name="the-retail-server-extension-components"></a>De onderdelen van de Retail Server-extensie

#### <a name="salestransactionsignature-retail-server-sample-component"></a>Retail Server-voorbeeldonderdeel SalesTransactionSignature

1. Zoek in de map **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** naar het project **RetailServer.Extensions.SalesTransactionSignatureSample** en bouw het.
2. Zoek in de map **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** het assemblagebestand **Contoso.RetailServer.SalesTransactionSignatureSample.dll**.
3. Kopieer het assemblagebestand naar de map met Retail Server-extensies.

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    De map is de map **\\bin** onder de locatie van de IIS Retail Server-site.

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    De map is de map **\\bin** onder de locatie van de IIS Retail Server-site.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    De map is de map **\\bin\\ext** onder de locatie van de IIS Retail Server-site.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    De map is de map **\\bin\\ext** onder de locatie van de IIS Retail Server-site.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    De map is de map **\\bin\\ext** onder de locatie van de IIS Retail Server-site.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    De map is de map **\\bin\\ext** onder de locatie van de IIS Retail Server-site.

    ---

4. Zoek het configuratiebestand voor Retail Server. Het bestand heeft de naam **web.config** en bevindt zich in de hoofdmap onder de locatie van de IIS Retail Server-site.
5. Registreer de extensies voor Retail Server in de sectie **extensionComposition** van het configuratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Registeer de afhankelijkheden van de extensies van Retail Server.

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4/)

    1. Zoek de volgende bestanden in de map **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

        - Het assemblagebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
        - Het configuratiebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

    2. Kopieer de bestanden naar de map **\\bin** onder de locatie van de IIS Retail Server-site.
    3. Registreer de CRT-wijziging in het extensieconfiguratiebestand voor CRT. Dit bestand heeft de naam **commerceruntime.ext.config** en het bevindt zich in de map **bin** onder de locatie van de IIS Retail Server-site.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later/)

    1. Zoek in de map **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
    2. Kopieer het bestand naar de map **\\bin** onder de locatie van de IIS Retail Server-site.
    3. Registreer de CRT-wijziging in het extensieconfiguratiebestand voor CRT. Dit bestand heeft de naam **commerceruntime.ext.config** en het bevindt zich in de map **bin** onder de locatie van de IIS Retail Server-site.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Er zijn geen acties vereist.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    > [!NOTE]
    > Er zijn geen acties vereist.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    > [!NOTE]
    > Er zijn geen acties vereist.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    > [!NOTE]
    > Er zijn geen acties vereist.

    ---

### <a name="the-modern-pos-extension-components"></a>De onderdelen van Modern POS-extensies

#### <a name="implement-the-proxy-code-for-offline-mode"></a>De proxycode voor offlinemodus implementeren

Dit gedeelte is vergelijkbaar met de Retail Server-controller, maar is een uitbreiding van de lokale CRT die wordt gebruikt wanneer de client geen verbinding heeft gemaakt.

1. Wijzig in het bestand **customization.settings** de sectie **@(RetailServerLibraryPathForProxyGeneration)** zodat de nieuwe Retail Server-assembly wordt gebruikt voor het genereren van proxy's.
2. Implementeer de volgende interfacemethoden in de klasse **StoreOperationsManager**. Voeg de volgende code toe voor de eerste iteratie:

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    ---

3. Als u de proxycode opnieuw wilt maken, moet u de map **Proxy's** bouwen vanuit de opdrachtregel met behulp van de opdracht **msbuild /t:Rebuild**.
4. Los de afhankelijkheden van het project **Proxies.RetailProxy** op:

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, voeg het project **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** toe aan de oplossing en voeg een projectverwijzing toe aan het project **RetailProxy** om naar **SalesTransactionSignatureSample** te verwijzen.

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, voeg het project **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** toe aan de oplossing en voeg een projectverwijzing toe aan het project **RetailProxy** om naar **SalesTransactionSignatureSample.Messages** te verwijzen.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    ---

5. Pas de interfacemethoden in de klasse **StoreOperationsManager**:

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    > [!NOTE]
    > Deze stap is niet van toepassing op deze versie.

    ---

6. Werk het bestand **dllhost.exe.config** bij zodat de clientbroker de nieuwe RetailProxy-assembly laadt.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Onderdeel van retailproxy-extensie (Retail 7.3.1 en hoger)

Voltooi de volgende procedure alleen als u Retail 7.3.1 of hoger gebruikt.

1. Zoek in de map **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** naar het project **RetailServer.Extensions.SalesTransactionSignatureSample** en bouw het.
2. Zoek in de map **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample**.
3. Kopieer de assemblagebestanden naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.
4. Registreer de Retail proxy-wijziging in het extensieconfiguratiebestand. Het bestand heeft de naam **RetailProxy.MPOSOffline.ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Onderdelen van Modern POS-extensies

1. Open de oplossing op **RetailSdk\\POS\\ModernPOS.sln** en controleer of deze zonder fouten kan worden gecompileerd. Zorg er bovendien voor dat u Modern POS kunt uitvoeren vanuit Microsoft Visual Studio met de opdracht **Uitvoeren**.

    > [!NOTE]
    > Modern POS mag niet worden aangepast. U moet User Account Control (UAC) inschakelen en u moet de installatie van eerder geïnstalleerde exemplaren van Modern POS zo nodig ongedaan maken.

2. Voeg de volgende bestaande broncodemappen toe in het project **Pos.Extensions**.

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. U kunt deze functie gebruiken als u de extensies in **tsconfig.json** wilt compileren door de volgende mappen uit de lijst met uitgesloten mappen te verwijderen.

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Schakel de extensies in die in **extensions.json** moeten worden geladen door de volgende regels op de juiste plek toe te voegen.

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Zie de instructies in het bestand readme.md in het project **Pos.Extensions** voor meer informatie en voorbeelden over het opnemen van mappen met broncodes en het inschakelen van te laden extensies.

5. Bouw de oplossing opnieuw.
6. Voer Modern POS in de debugger uit en test de functionaliteit.

### <a name="cloud-pos-extension-components"></a>Onderdelen van Cloud POS-extensies

1. Open de oplossing op **RetailSdk\\POS\\CloudPOS.sln** en controleer of deze zonder fouten kan worden gecompileerd.
2. Voeg de volgende bestaande broncodemappen toe in het project **Pos.Extensions**.

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. U kunt deze functie gebruiken als u de extensies in **tsconfig.json** wilt compileren door de volgende mappen uit de lijst met uitgesloten mappen te verwijderen.

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Schakel de extensies in die in **extensions.json** moeten worden geladen door de volgende regels op de juiste plek toe te voegen.

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Zie de instructies in het bestand readme.md in het project **Pos.Extensions** voor meer informatie en voorbeelden over het opnemen van mappen met broncodes en het inschakelen van te laden extensies.

5. Bouw de oplossing opnieuw.
6. Voer de oplossing uit met de opdracht **Uitvoeren** en volg de stappen in de handleiding voor de Retail SDK.
7. Test de functionaliteit.

### <a name="set-up-required-parameters-in-headquarters"></a>Vereiste parameters instellen in Headquarters

Zie [Kassafunctionaliteit voor Noorwegen](./emea-nor-cash-registers.md) voor meer informatie.

## <a name="production-environment"></a>Productieomgeving

Volg deze stappen om implementeerbare pakketten te maken die Commerce-onderdelen bevatten en om deze pakketten toe te passen in een productieomgeving.

1. Voltooi de stappen in de sectie met de [Onderdelen van Cloud POS-extensies](#cloud-pos-extension-components) of [Onderdelen van Modern POS-extensies](#modern-pos-extension-components) eerder in dit artikel.
2. Breng de volgende wijzigingen aan in de pakketconfiguratiebestanden onder de map **RetailSdk\\Assets**:

    1. Voeg in de configuratiebestanden **commerceruntime.ext.config** en **CommerceRuntime.MPOSOffline.Ext.config** de volgende regels toe aan de sectie **Samenstelling**:

        # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Aanpassing Commerce-proxy inschakelen:

        # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

        Voeg in het configuratiebestand **dllhost.exe.config** de volgende regels toe aan de subsectie **appSettings** van de sectie **configuratie**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

        Voeg in het configuratiebestand **dllhost.exe.config** de volgende regels toe aan de subsectie **appSettings** van de sectie **configuratie**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Voeg de volgende regels toe aan de sectie **Samenstelling** van het configuratiebestand **RetailProxy.MPOSOffline.ext.config**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

        Voeg de volgende regels toe aan de sectie **Samenstelling** van het configuratiebestand **RetailProxy.MPOSOffline.ext.config**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

        Voeg de volgende regels toe aan de sectie **Samenstelling** van het configuratiebestand **RetailProxy.MPOSOffline.ext.config**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

        Voeg de volgende regels toe aan de sectie **Samenstelling** van het configuratiebestand **RetailProxy.MPOSOffline.ext.config**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Breng de volgende wijzigingen aan in het configuratiebestand voor pakketaanpassing **Customization.settings**:

    1. Schakel aanpassing van Retail-proxy in.

        # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

        Voeg de volgende regels toe aan de sectie **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

        Voeg de volgende regels toe aan de sectie **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Voeg de volgende regels aan de sectie **ItemGroup** toe om de Retail-proxy-extensie op te nemen in de implementeerbare pakketten:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

        Voeg de volgende regels aan de sectie **ItemGroup** toe om de Retail-proxy-extensie op te nemen in de implementeerbare pakketten:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

        Voeg de volgende regels aan de sectie **ItemGroup** toe om de Retail-proxy-extensie op te nemen in de implementeerbare pakketten:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

        Voeg de volgende regels aan de sectie **ItemGroup** toe om de Retail-proxy-extensie op te nemen in de implementeerbare pakketten:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Voeg de volgende regels aan de sectie **ItemGroup** toe om de CRT-extensies op te nemen in de implementeerbare pakketten:

        # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Voeg de volgende regels aan de sectie **ItemGroup** toe om de Retail Server-extensie op te nemen in de implementeerbare pakketten:

        # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Wijzig de volgende bestanden om de resourcebestanden voor Noorwegen op te nemen in implementeerbare pakketten:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - Voor het bestand **Sdk.ModernPos.Shared.csproj** 
    - Regel toevoegen aan de sectie **ItemGroup**
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > Geef in plaats van de <bestandsnaam> een naam van het resourcebestand op. Hetzelfde is relevant voor de overige onderstaande voorbeelden.
 
    - Regel toevoegen aan de sectie **Target Name="CopyPackageFiles"**
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - Voor het bestand **Sdk.RetailServerSetup.proj** 
    - Regel toevoegen aan de sectie **ItemGroup**
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Regel toevoegen aan de sectie **Target Name="CopyPackageFiles"**
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Wijzig het configuratiebestand van het certificaat door de vingerafdruk, winkellocatie en winkelnaam op te geven voor het certificaat dat moet worden gebruikt om verkooptransacties te ondertekenen. Kopieer vervolgens het configuratiebestand naar de map **Verwijzingen**.

    # <a name="application-update-4"></a>[Toepassingsupdate 4](#tab/app-update-4)

    Het bestand heeft de naam **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** en bevindt zich onder **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="application-update-5-and-later"></a>[Toepassingsupdate 5 and hoger](#tab/app-update-5-and-later)

    Het bestand heeft de naam **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** en bevindt zich onder **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Het bestand heeft de naam **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** en bevindt zich onder **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 en later](#tab/retail-7-3-2)

    Het bestand heeft de naam **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** en bevindt zich onder **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 en later](#tab/retail-7-3-5)

    Het bestand heeft de naam **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** en bevindt zich onder **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 en later](#tab/retail-8-1-1)

    Het bestand heeft de naam **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** en bevindt zich onder **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    ---

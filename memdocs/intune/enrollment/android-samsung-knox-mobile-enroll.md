---
title: Android-apparaten automatisch registreren met behulp van de Knox Mobile Enrollment van Samsung
titleSuffix: Microsoft Intune
description: Meer informatie over de registratie van Android-apparaten met behulp van Samsung KME
keywords: ''
author: ErikjeMS
ms.author: erikje
manager: ''
ms.date: 03/03/2020
ms.topic: how-to
ms.service: microsoft-intune
ms.subservice: enrollment
ms.localizationpriority: high
ms.technology: ''
ms.assetid: 30df0f9e-6e9e-4d75-a722-3819e33d480d
ms.reviewer: chmaguir
ms.suite: ems
search.appverid: MET150
ms.custom: seodec18
ms.collection: M365-identity-device-management
ms.openlocfilehash: 50c85a3b0ac84acf4243e9a5cdb74b95950a66a5
ms.sourcegitcommit: 302556d3b03f1a4eb9a5a9ce6138b8119d901575
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/27/2020
ms.locfileid: "83987533"
---
# <a name="automatically-enroll-android-devices-by-using-samsungs-knox-mobile-enrollment"></a>Android-apparaten automatisch registreren met behulp van de Knox Mobile Enrollment van Samsung

In dit onderwerp leest u hoe u Intune kunt instellen voor het registreren van Android-apparaten met behulp van Samsung KME (Knox Mobile Enrollment). Met Intune en Samsung KME kunt u een groot aantal Android-apparaten in bedrijfseigendom registreren wanneer eindgebruikers hun apparaten de eerste keer inschakelen en verbinding maken met een Wi-Fi- of mobiel netwerk. Apparaten kunnen ook met Bluetooth of NFC worden geregistreerd als de Knox-registratie-app wordt gebruikt.

Als u Intune-registratie met Samsung KME wilt inschakelen, gebruikt u de Intune- en Samsung Knox-portals in deze volgorde:

1. In de Knox-portal doet u het volgende:
    1. [Een MDM-profiel maken](#create-mdm-profile)
    2. [Apparaten toevoegen](#add-devices)
    3. [Een MDM-profiel toewijzen aan de apparaten](#assign-an-mdm-profile-to-devices)
2. In de Knox-portal [configureert u de aanmelding van eindgebruikers](#configure-how-end-users-sign-in).
3. [De apparaten distribueren](#distribute-devices).


Een lijst met apparaat-id's (serienummers en IMEI's) wordt automatisch aan de Knox-portal toegevoegd wanneer apparaten worden gekocht bij geautoriseerde resellers die deel uitmaken van het Knox Deployment Program.


## <a name="prerequisites"></a>Vereisten

Voor registratie bij Intune met KME moet u uw bedrijf eerst registreren op de Samsung Knox-portal met de volgende stappen:
1. [Controleer of KME beschikbaar is in uw land/regio](https://www.samsungknox.com/en/solutions/it-solutions/knox-configure/available-countries): KME is beschikbaar in meer dan 55 landen/regio's. Controleer of er ondersteuning wordt geboden voor het gewenste land of de gewenste regio van implementatie.

2. [Ondersteunde apparaten](https://www.samsungknox.com/en/knox-platform/supported-devices/2.4+): KME is beschikbaar op alle Samsung-apparaten met minimaal Knox 2.4 voor registratie bij Android en minimaal Knox 2.8 voor registratie bij Android Enterprise.

3. [Netwerkvereisten](https://docs.samsungknox.com/KME-Getting-Started/Content/firewall_exceptions.htm): Controleer of de benodigde firewall- en netwerktoegangsregels zijn toegestaan in uw netwerk.

4. [Registreren voor een Samsung-account](https://www2.samsungknox.com/en/user/register): U hebt een Samsung-account nodig om KME te registreren en in te schakelen en alle Knox Enterprise-rechten op één plaats te beheren.

5. Registratiecontrole: Wanneer uw profiel is voltooid en ingediend, controleert Samsung uw toepassing. De registratie wordt onmiddellijk goedgekeurd of krijgt de status Controle in behandeling voor verdere opvolging. Wanneer uw account is goedgekeurd, kunt u doorgaan met de overige stappen.

## <a name="create-mdm-profile"></a>MDM-profiel maken

Wanneer uw bedrijf is geregistreerd, kunt u uw MDM-profiel voor Microsoft Intune in de Knox-portal maken met behulp van de onderstaande informatie. In de Knox-portal kunt u MDM-profielen maken voor zowel Android als Android Enterprise.
- Als u een Android MDM-profiel wilt maken, selecteert u **Apparaatbeheerder** als het profieltype in de Knox-portal. 
- Als u een Android Enterprise MDM-profiel wilt maken, selecteert u **Apparaateigenaar** als het profieltype in de Knox-portal.  

### <a name="for-android-enterprise"></a>Voor Android Enterprise

| MDM-profielvelden| Vereist? | Waarden | 
|-------------------|-----------|-------| 
|Profile Name (Profielnaam)       | Ja       |Voer een profielnaam naar keuze in. |
|Beschrijving        | Nee        |Voer een beschrijvende tekst voor het profiel in. |
|MDM-informatie     | Ja        |Kies **Server-URI niet vereist voor mijn MDM**.| 
|MDM Agent APK (APK van MDM-agent)      | Ja       |https://aka.ms/intune_kme_deviceowner| 
|Custom JSON (Aangepaste JSON)        | Ja*        |{"com.google.android.apps.work.clouddpc.EXTRA_ENROLLMENT_TOKEN": "Token-tekenreeks voor Intune-registratie invoeren"}. Meer informatie over het maken van een inschrijvingstoken voor [toegewezen apparaten](android-kiosk-enroll.md) en [volledig beheerde apparaten](android-fully-managed-enroll.md). |
|Skip Setup wizard (Installatiewizard) overslaan  | Nee        |Kies deze optie als u de standaardvragen voor de installatie van het apparaat voor de gebruiker wilt overslaan.|
|Allow End User to Cancel Enrollment (Toestaan dat eindgebruiker de registratie annuleert) | Nee | Kies deze optie als gebruikers KME mogen annuleren.|
| Privacybeleid, Gebruiksrechtovereenkomsten en Servicevoorwaarden | Nee | Laat dit leeg. |
| Contactgegevens voor ondersteuning | Ja | Kies Bewerken om uw contactgegevens bij te werken |
|Associate a Knox license with this profile (Een Knox-licentie koppelen aan dit profiel) | Nee | Laat deze optie uitgeschakeld. Voor registratie bij Intune met KME is geen Knox-licentie vereist.|

\* Dit veld is niet vereist om het maken van een profiel in de Knox-portal te voltooien. Voor Intune is het echter wel vereist dat dit veld wordt ingevuld zodat het profiel het apparaat kan inschrijven bij Intune.

### <a name="for-android-device-administrator"></a>Voor de beheerder van Android-apparaten 

Raadpleeg de instructies in de [profielinstallatie van Samsung](https://docs.samsungknox.com/KME-Getting-Started/Content/create-profiles.htm) voor stapsgewijze richtlijnen.

| MDM-profielvelden| Vereist? | Waarden |
|-------------------|-----------|-------|
|Profile Name (Profielnaam)       | Ja       |Voer een profielnaam naar keuze in.|
|Beschrijving        | Nee        |Voer een beschrijvende tekst voor het profiel in.|
|Kies uw MDM | Ja | Kies Microsoft Intune. |
|MDM Agent APK (APK van MDM-agent)      | Ja       |https://aka.ms/intune_kme|
|MDM Server URI (URI van MDM-server)     | Nee        |Laat dit leeg.|
|Aangepaste JSON-gegevens        | Nee        |Laat dit leeg.|
|Dubbele DAR | Nee | Laat dit leeg.|
|QR-code voor inschrijving | Nee | U kunt een QR-code toevoegen om de inschrijving te versnellen.|
|Systeemtoepassingen | Ja | Kies de optie **Alle systeem-apps ingeschakeld laten** om te controleren of alle apps zijn ingeschakeld en beschikbaar zijn voor het profiel. Als deze optie niet is geselecteerd, wordt slechts een beperkt aantal systeem-apps weergegeven in het app-overzicht van het apparaat. Apps als de e-mail-app blijven verborgen. |
|Privacybeleid, Gebruiksrechtovereenkomsten en Servicevoorwaarden | Nee | Laat dit leeg.|
|Bedrijfsnaam | Ja | Deze naam wordt weergegeven tijdens de registratie van het apparaat. |

## <a name="add-devices"></a>Apparaten toevoegen

Als u MDM-profielen aan apparaten wilt toewijzen, moeten ondersteunde Samsung Knox-apparaten aan de Knox-portal worden toegevoegd. Daarvoor kunt u een van de volgende methoden gebruiken:
- **Door Samsung goedgekeurde reseller(s) gebruiken:** Gebruik deze methode als u apparaten van een van de door Samsung goedgekeurde resellers hebt gekocht. Resellers kunnen apparaten automatisch voor u uploaden wanneer dit is goedgekeurd. [Raadpleeg de gebruikershandleiding van Samsung Knox Enrollment voor meer informatie over het toevoegen van resellers](https://docs.samsungknox.com/KME-Getting-Started/Content/Register_resellers.htm).

- **De Knox Deployment App (KDA) gebruiken:** Gebruik deze methode als u bestaande apparaten wilt registreren met KME. Met deze methode kunt u zowel via Bluetooth als via NFC apparaten toevoegen aan de Knox-portal. [Raadpleeg de gebruikershandleiding van Samsung Knox Enrollment voor meer informatie over KDA](https://docs.samsungknox.com/KME-Getting-Started/Content/add-device-info.htm).

## <a name="assign-an-mdm-profile-to-devices"></a>Een MDM-profiel toewijzen aan apparaten
U moet een MDM-profiel aan toegevoegde apparaten toewijzen in de Knox-portal voordat ze kunnen worden geregistreerd. [Raadpleeg de gebruikershandleiding van Samsung Knox Enrollment voor meer informatie over apparaatconfiguratie](https://docs.samsungknox.com/KME-Getting-Started/Content/configure-devices.htm).

## <a name="configure-how-end-users-sign-in"></a>Configureren hoe eindgebruikers zich aanmelden

Voor apparaten die in Intune worden geregistreerd met KME voor Android, kunt u als volgt configureren hoe een eindgebruiker zich aanmeldt:

- **Zonder koppeling met gebruikersnaam:** Laat in de Knox-portal onder **Device details** (Apparaatdetails) de velden **User ID** (gebruikers-id) en **Password** (wachtwoord) leeg voor de toegevoegde apparaten. De gebruiker moet dan zijn gebruikersnaam en wachtwoord invoeren tijdens de registratie bij Intune.

- **Met koppeling met gebruikersnaam:** Geef in de Knox-portal onder **Device Details** (Apparaatdetails) een **gebruikers-id** op (bijvoorbeeld een gebruikersnaam voor de toegewezen gebruiker of een [Device Enrollment Manager](device-enrollment-manager-enroll.md)-account) voor de toegevoegde apparaten. De gebruikersnaam wordt dan al ingevuld en de gebruiker hoeft alleen een wachtwoord in te voeren tijdens de registratie bij Intune.

> [!NOTE]
>
>Koppeling van de gebruiker is alleen van toepassing op registratie van Android-apparaatbeheerder. Als een gebruikerskoppeling is gedefinieerd, kan alleen de gekoppelde gebruiker het apparaat met KME registreren. Dit geldt zelfs nadat de fabrieksinstellingen van het apparaat zijn teruggezet. Als in de Knox-portal geen gebruikerskoppeling is gedefinieerd, kan elke gebruiker met een geldige Intune-licentie het apparaat met KME registreren.
>Bij volledige beheerde Android Enterprise-apparaten, zelfs als een gebruikerskoppeling is gedefinieerd, wordt deze niet doorgegeven aan het apparaat of wordt het apparaat niet aan de gebruiker gekoppeld.
>

## <a name="distribute-devices"></a>Apparaten distribueren

Wanneer een MDM-profiel is gemaakt en toegewezen, een gebruikersnaam is gekoppeld en de apparaten in Intune als bedrijfseigendom zijn geïdentificeerd, kunt u apparaten aan gebruikers distribueren.

Nog hulp nodig? Bekijk de volledige [KME-gebruikershandleiding](https://docs.samsungknox.com/KME-Getting-Started/Content/get-started.htm).

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

- **Ondersteuning voor apparaateigenaar:**  - **Ondersteuning voor apparaateigenaar:** Intune biedt ondersteuning voor registratie van toegewezen en volledig beheerde apparaten met behulp van de KME-portal. Andere modi voor apparaateigenaren in Android Enterprise worden ondersteund zodra ze beschikbaar zijn in Intune.

- **Geen ondersteuning voor werkprofielen:** KME is een methode voor registratie van bedrijfsapparaten. Door apparaten te registeren in een Android-werkprofiel kunnen werk- en persoonlijke gegevens worden gescheiden op persoonlijke apparaten. Daarom wordt registratie van apparaten in een werkprofiel met KME niet ondersteund in Intune.

- **Fabrieksinstellingen terugzetten voor registratie bij Android Enterprise:** Als u apparaten die al zijn ingesteld opnieuw wilt inzetten, moeten op het apparaat de fabrieksinstellingen worden hersteld voordat het kan worden geregistreerd bij Android Enterprise.

- **Updates met behulp van een Google Play-account:** U hebt geen Google Play-account nodig om het apparaat te registreren bij Microsoft Intune. Maar voor toekomstige updates van de Intune-bedrijfsportal-app hebt u mogelijk wel een Google Play-account op het apparaat nodig voor het registreren van de Android-apparaatbeheerder. Een Google Play-account is niet vereist bij het registreren van de eigenaar van het Google-apparaat.

- **Veld Password (Wachtwoord) wordt genegeerd:** Als het veld **Password** (Wachtwoord) in **Device details** (Apparaatdetails) van de Knox-portal is ingevuld, wordt het genegeerd door de Intune-bedrijfsportal-app tijdens de registratie bij Android. De eindgebruiker moet een wachtwoord invoeren op het apparaat om registratie van het apparaat te voltooien.


## <a name="getting-support"></a>Ondersteuning
Meer informatie over [ondersteuning voor Samsung KME](https://docs.samsungknox.com/KME-Getting-Started/Content/to-get-kme-support.htm).



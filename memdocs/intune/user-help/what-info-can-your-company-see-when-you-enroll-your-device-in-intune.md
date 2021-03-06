---
title: Welke gegevens kan uw bedrijf zien wanneer u uw apparaat inschrijft?
description: Verklaart wat de IT-afdeling wel en niet kan zien op uw beheerde apparaat.
keywords: ''
author: lenewsad
ms.author: lanewsad
manager: dougeby
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: microsoft-intune
ms.subservice: end-user
ms.technology: ''
ms.assetid: 12655728-a1af-4d89-97bc-925fe36c0dc4
searchScope:
- User help
ROBOTS: ''
ms.reviewer: esmich
ms.suite: ems
ms.collection: ''
ms.openlocfilehash: ed3f9f6f01c8dc2df3a89daee991d9f8c61056b9
ms.sourcegitcommit: f94cdca69981627d6a3471b04ac6f0f5ee8f554f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2020
ms.locfileid: "82210312"
---
# <a name="what-information-can-my-organization-see-when-i-enroll-my-device"></a>Welke gegevens kan mijn organisatie zien wanneer ik mijn apparaat inschrijf?

Uw organisatie kan uw persoonlijke gegevens niet zien wanneer u een apparaat met Microsoft Intune inschrijft. Wanneer u een apparaat inschrijft, geeft u uw organisatie toestemming om bepaalde soorten informatie op uw apparaat weer te geven, zoals het apparaatmodel en serienummer. Uw organisatie gebruikt deze informatie om de zakelijke gegevens op het apparaat te beveiligen.

**Wat uw organisatie nooit kan zien:**

- Oproepen en browsegeschiedenis
- E-mail- en sms-berichten
- Contactpersonen
- Kalender
- Wachtwoorden
- Foto's, met inbegrip van wat er in de app Foto's of het camera-album staat
- Bestanden

**Wat uw organisatie altijd kan zien:**

- Apparaatmodel, zoals Google Pixel
- Apparaatfabrikant, zoals Microsoft
- Besturingssysteem en versie, zoals iOS 12.0.1
- Inventaris en namen van apps, zoals Microsoft Word. op persoonlijke apparaten kan uw organisatie alleen uw beheerde apps zien. Op apparaten waar het bedrijf eigenaar van is, kan uw organisatie al uw apps zien.
- Eigenaar van het apparaat
- Apparaatnaam
- Serienummer van apparaat
- IMEI

 > [!NOTE]
 > Voor volledig beheerde en toegewezen Android Enterprise-apparaten kunt u niet de hele app-inventaris weergeven.    
    
**Wat uw organisatie mogelijk kan zien:**

- Telefoonnummer: Op apparaten die eigendom zijn van de organisatie is uw volledige telefoonnummer zichtbaar. Voor persoonlijke apparaten zijn alleen de laatste vier cijfers van uw telefoonnummer zichtbaar voor uw organisatie. U kunt het eigendomstype van elk afzonderlijk apparaat zien op de pagina **Apparaatdetails** van dat apparaat.
- Apparaatopslagruimte: als u een vereiste app niet kunt installeren, kan uw organisatie kijken naar de opslagruimte van het apparaat om te controleren of er wellicht te weinig ruimte is.  
- Locatie: uw organisatie kan nooit de locatie van uw apparaat zien, tenzij u een verloren iOS-apparaat onder supervisie moet herstellen. Raadpleeg de [Apple iOS-documentatie](https://go.microsoft.com/fwlink/?linkid=853816) voor meer informatie over apparaten onder supervisie.  
- Details app-inventaris: als uw organisatie gebruikmaakt van Mobile Threat Defense, kunnen er details worden weergegeven over de apps die op uw iOS-apparaat zijn geïnstalleerd. Meer informatie over [Mobile Threat Defense](set-up-mobile-threat-defense.md). Als u een persoonlijk apparaat hebt, kan uw organisatie alleen uw beheerde apps zien. Als u een apparaat hebt dat eigendom is van het bedrijf waar u werkt, kan uw organisatie al uw apps zien.
- Netwerkgegevens: bepaalde informatie over netwerkverbindingen voor Android-apparaten kan voor de ondersteuning van uw organisatie beschikbaar zijn. Als uw organisatie bijvoorbeeld vereist dat apparaten binnen een bepaald gebouw blijven, herkent uw apparaat het netwerk waarmee het is verbonden. 

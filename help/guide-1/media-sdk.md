---
title: Häufig gestellte Fragen zum Ende der Nutzungsdauer von Adobe Media SDK (Versionen 1.x und 2.x)
description: Erhalten Sie Antworten auf häufig gestellte Fragen zum Ende der Lebensdauer von Adobe Media SDK Version 1.x und 2.x (ehemals Video Heartbeat Library).
source-git-commit: d014c200dd926ccf0116faa50c4bffb1d234e926
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 1%

---


# Häufig gestellte Fragen zum Ende der Nutzungsdauer von Adobe Media SDK (Versionen 1.x und 2.x)

Das Ende der Unterstützung für Adobe Media SDK **2.x wurde am 31. August 2021**. Video Heartbeat Library (VHL) **1.x ist veraltet** wird seit mehreren Jahren nicht mehr unterstützt.

## Was geschieht?

Die ursprüngliche Video Heartbeat Library (VHL), die später in Media SDK umbenannt wurde, bot Client-seitiges Tracking für Audio- und Videoanalysen. Adobe hat die Tracking-Funktionen auf neuere, leistungsfähigere Implementierungen umgestellt:

* **Media SDK 3.x (nur Analytics):** derzeit unterstützt. Verfolgt Medien mithilfe der Mediensammlungs-API. Empfohlen für bestehende 2.x-Benutzer, die noch nicht zur Edge Network wechseln können.
* **Streaming-Medien für Edge Network (empfohlen):** Die derzeit empfohlene Implementierung. Verwendet die Adobe Experience Platform Web SDK-, Mobile SDK- oder Media Edge-API zum Senden von Mediendaten über die Edge Network, wodurch die Verwendung in Adobe Analytics, Customer Journey Analytics, Real-Time CDP und Adobe Journey Optimizer ermöglicht wird.

## Was ist im End-of-Life enthalten und was nicht?

**Ende der Lebensdauer (nicht mehr unterstützt):**

* Video Heartbeat Library (VHL) 1.x — Alle Plattformen (Android, iOS, JavaScript, Apple TV, Chromecast, Roku, TVML)
* Media SDK 2.x - Android, iOS, JavaScript

**Nicht das Ende der Lebensdauer (wird weiterhin unterstützt):**

* Media SDK 3.x - JavaScript, Chromecast, Roku (nur Analytics)
* Streaming-Medien für Edge Network - alle unterstützten Plattformen

## Warum wurden die Versionen 1.x und 2.x eingestellt?

Ab Version 3.0 wurde Media SDK so umgestaltet, dass die Mediensammlungs-API direkt verwendet werden kann. Es ist kein Delegatmuster mehr erforderlich, und die Tracker-Erstellung wird vereinfacht. Die älteren 1.x- und 2.x-SDKs basieren auf einer Heartbeat-Serverarchitektur, die seitdem abgelöst wurde.

Adobe führte auch die Edge Network-Implementierung ein, um eine einzige Datenerfassungs-Pipeline bereitzustellen, die mehrere nachgelagerte Adobe-Anwendungen versorgen kann, die von den Legacy-Heartbeat-SDKs nicht unterstützt werden können.

## Wo finde ich die archivierte Dokumentation?

Die alte Dokumentation wurde auf GitHub archiviert und steht als Referenz zur Verfügung:

| Version | Status | Archivierte Dokumentation |
|---|---|---|
| 1.x (Video Heartbeat Library) | Veraltet | [`video-heartbeat` GitHub-Repository](https://github.com/Adobe-Marketing-Cloud/video-heartbeat/tree/master/docs) |
| 2.x (Media SDK) | Ende der Unterstützung 31. August 2021 | [`media-sdks` GitHub-Repository](https://github.com/Adobe-Marketing-Cloud/media-sdks/blob/master/docs/2.x/README.md) |

## Was sind meine Übergangsoptionen?

**Option 1: Migrieren zu Media SDK 3.x (nur Analytics)**

Wenn Sie 2.x verwenden und Adobe Analytics ausschließlich verwenden, ist die Migration zu 3.x der einfachste Pfad. Im Migrationshandbuch [2.x zu 3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html) finden Sie einen vollständigen API-Vergleich und Code-Beispiele.

**Option 2: Migrieren zu Streaming Media für Edge Network (empfohlen)**

Verwenden Sie für neue Implementierungen oder wenn Sie Daten in mehreren Adobe-Anwendungen verwenden möchten, die Adobe Experience Platform-Edge Network:

* [Media Edge Web SDK](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-web-sdk.html)
* [Media Edge Mobile SDK](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [Media Edge-API](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge-api.html)

## Häufig gestellte Fragen

+++**Wird die Unterstützung für Roku- und Chromecast-SDKs beeinträchtigt?**

Nein. Die Roku- und Chromecast-SDKs bleiben als Teil von Media SDK 3.x verfügbar und werden unterstützt (nur Analytics). Dieses Ende der Lebensdauer gilt nur für die Versionen 1.x und 2.x.

+++

+++**Sind Media Analytics JavaScript SDK-Implementierungen betroffen?**

Nein. Kunden, die JavaScript SDK für Media Analytics verwenden, können weiterhin die eigenständige SDK- oder Tag-Erweiterung verwenden.

+++

+++**Ich arbeite noch mit Media SDK 2.x. Was soll ich tun?**

Adobe empfiehlt für alle neuen Projekte die Migration zur Edge Network-Implementierung. Wenn Sie einen Zwischenschritt benötigen, [Migrieren Sie von JavaScript SDK 2.x zu 3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html) und planen Sie dann Ihren Wechsel zu Edge Network.

+++

+++**Wie viel Aufwand ist für die Migration auf eine unterstützte Implementierung erforderlich?**

Der Migrationsaufwand hängt von der jeweiligen Kundenimplementierung ab und variiert. Wenden Sie sich nach der Lektüre der Migrationsdokumentation an die Beratung oder Kundenunterstützung, um weitere Unterstützung zu erhalten:

* [Implementieren von Streaming-Medien mit dem mobilen Edge SDK - Android und iOS](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [Migration von JavaScript SDK 2.x zu 3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html)

+++

+++**Muss ich Adobe Experience Platform Tags als Tag-Management-System verwenden?**

Bei Implementierungen mobiler Apps werden Experience Platform-Tags nicht wie beim Web als Tag-Management-System verwendet. Die Tags-Benutzeroberfläche ist für die Konfiguration von SDK Extensions erforderlich. Dies ähnelt der Verwendung der Adobe Mobile Services-Benutzeroberfläche zum Konfigurieren von Mobile v4 SDK. Tags bietet benutzerdefinierte Installationsanweisungen basierend auf der von Ihnen ausgewählten Erweiterung.

+++

+++**Hat dieses Ende der Unterstützung Auswirkungen auf SDK für tvOS?**

Ja. Für tvOS (ab Version 10) wird empfohlen, mit dem Adobe Experience Platform Mobile SDK zu Streaming Media für Edge Network zu migrieren. Weitere [ finden Sie unter „Implementieren von Streaming](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)Medien mit der mobilen Edge SDK&quot;.

+++

+++**Hat dieses Ende der Unterstützung Auswirkungen auf SDK for Fire TV und Android TV?**

Ja. Für Fire TV und Android TV wird empfohlen, mit der Adobe Experience Platform Mobile SDK zu Streaming Media für Edge Network zu migrieren. Weitere [ finden Sie unter „Implementieren von Streaming](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)Medien mit der mobilen Edge SDK&quot;.

+++

+++**Wo finde ich Informationen zum Ende der Nutzungsdauer von Mobile v4 SDK?**

Siehe [ FAQ zum Ende der Nutzungsdauer von Mobile Services](mobile-services.md). Die Mobile Services-Plattform und die Mobile v4-SDKs wurden am 31. Dezember 2022 eingestellt.

+++

+++**Wo kann ich bei Fragen hingehen?**

Wenden Sie sich an Ihr Adobe-Account-Team oder die Adobe-Kundenunterstützung, um Unterstützung bei der Migration zu erhalten.

+++

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Streaming-Medien](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/overview.html)
>* [Streaming-Medien für Edge Network](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge.html)
>* [Media SDK 3.x - JavaScript-Einrichtung](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/web-implementation.html)

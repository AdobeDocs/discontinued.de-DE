---
title: Häufig gestellte Fragen zur Abschaffung der Adobe Mobile Services
description: Erhalten Sie Antworten auf häufig gestellte Fragen zur Ankündigung des Lebenszyklusendes für Adobe Mobile Services.
exl-id: c5f44341-7b87-4530-b86e-17e2911a7959
source-git-commit: 343e0a727c570c9eec503d7903d0477134fc6189
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Häufig gestellte Fragen zur Abschaffung der Adobe Mobile Services

Das Enddatum von Adobe Mobile Service war **31. Dezember 2022**.

## Was passiert?

Mobile Services endete am 31. Dezember 2022. Mobile Services, die eine mobilzentrierte Benutzeroberfläche unterstützen, werden nach diesem Datum nicht mehr unterstützt: Akquise, Deep-Linking, In-App-Nachrichten, Push-Benachrichtigungen und Geolokation.

## Was ist enthalten und was ist nicht enthalten?

Diese Einstellung betrifft nur Adobe Mobile Services, die eigenständige Plattform unter [mobilemarketing.adobe.com](https://mobilemarketing.adobe.com). Die Mobile Version 4 SDKs, die auf diese Schnittstelle angewiesen sind, wurden am 31. August 2021 eingestellt.

Dieses Ende der Lebensdauer umfasst NICHT Adobe Analytics für mobile Apps, Teil der Adobe Experience Platform Mobile SDKs. Diese Funktionen, darunter das In-App-Verhalten, die Lebenszyklusanalyse, das Tracking von Interaktionen mit Nachrichten und Zielgruppenprofile, werden von Adobe weiterhin unterstützt.

## Warum wird die Funktion eingestellt?

Da Adobe seine mobilen Marketingfunktionen weiter ausbaut, werden bereits in Mobile Services verfügbare Funktionen in Adobe Experience Cloud-Lösungen veröffentlicht oder über Adobe Exchange Premier Partners angeboten. Diese Transition bietet leistungsfähigere und flexiblere mobile Marketingfunktionen.

## Was passiert mit bestehenden, in Mobile Services erstellten Verarbeitungsregeln?

[Verarbeitungsregeln](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html) die in der Mobile Services-Benutzeroberfläche erstellt oder generiert wurden, werden vor dem Ende des Lebenszyklus von Mobile Services automatisch zu Adobe Analytics migriert. Migrierte Verarbeitungsregeln verhalten sich ähnlich wie andere Verarbeitungsregeln in Adobe Analytics, wo Sie sie frei anzeigen oder bearbeiten können. Für diese Migration ist keine Benutzeraktion erforderlich.

Nachdem Mobile Services eingestellt wurde, werden alle Verarbeitungsregellogiken ausschließlich innerhalb von Adobe Analytics verarbeitet, in der Regel einschließlich der Verwendung von [Kontextdatenvariablen](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/contextdata.html).

## Welche Übergangsoptionen sind verfügbar?

Adobe bietet je nach Anwendungsfall Ihres Unternehmens drei Übergangspfade.

1. **In-App-Nachrichten und Push-Benachrichtigungen**: Adobe kann Ihre Messaging-Workflows in Adobe Journey Optimizer überführen. Mit diesem Produkt können Unternehmen Erlebnisse auf der gesamten Journey optimieren und personalisieren, einschließlich mobiler Nachrichten.
1. **Akquise und Deep-Linking**: Akquise und Deep-Linking werden über das Adobe Exchange Premier Partners-Programm angeboten. Das Partnerteam der Adobe kann geeignete Einführungsmaßnahmen treffen, um sicherzustellen, dass Sie die für Ihre Anforderungen am besten geeignete Lösung finden.
1. **Places Service**: Der Places Service bietet zusätzliche Geolokationsfunktionen. Siehe [Places Service-Dokumentation](https://experienceleague.adobe.com/docs/places/using/home.html).

## Wo kann ich hingehen, wenn ich Fragen habe?

Siehe [Adobe Mobile Services - Spark-Seite zum Ende der Nutzungsdauer](https://spark.adobe.com/page/C6D30y09zaRpD/) für weitere Informationen. Wenden Sie sich bei weiteren Fragen an Ihren Kundenbetreuer.
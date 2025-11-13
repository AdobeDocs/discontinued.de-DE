---
title: Ausgeblendeter Test
description: Dies ist ein versteckter Test
hide: true
hidefromtoc: true
landing-page-breadcrumb-title: Test AEM 6.5
landing-page-name: experience-manager-65
feature: Annotations
exl-id: e6e5ba1c-98a5-4d7d-9913-426df31bc7a3
source-git-commit: dde6a1c269865b6baec6e073a25a3dbd817d3d07
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 2%

---

# Ausgeblendeter Test

Dies ist ein versteckter Test. Ich füge dieses `[` hinzu, um sicherzustellen, dass es beim v2-Rendering funktioniert.

&#x200B;12. November 2025

## Videotest

### Einfaches Video ohne Transkript - sollte Transkript anzeigen, da metadata.md nach unten durchsickert

>[!VIDEO](https://video.tv.adobe.com/v/3415782?captions=ger&hidetitle=true)

### Mit auf „true“ festgelegtem Transkript

>[!VIDEO](https://video.tv.adobe.com/v/3415782?captions=ger&hidetitle=true){transcript=true}

### Wenn das Transkript auf „false“ gesetzt ist, sollte das Videotranskript nicht angezeigt werden.

>[!VIDEO](https://video.tv.adobe.com/v/3415782?captions=ger&hidetitle=true){transcript=false}

## Relative Links

* [Überblick](overview.md)
* [Suchen und Bewerben](search-promote.md)
* [Social](social.md)

## Expliziter Deep-Link

[Zusätzliche Übersicht (Stamm)](/help/guide-1/overview.md#additional-products)

[Zusätzliche Übersicht](overview.md#additional-products)

## Hover-Test {#this-is-a-heading-anchor}

Kein Hover-Text

```
![alt text](assets/maui-flip.jpg)
```

![ALT-Text](assets/maui-flip.jpg)


Ja Hover-Text

```
![alt text](assets/maui-flip.jpg "Hover text")
```

![Alt-Text](assets/maui-flip.jpg "Hover-Text")

## Folie

Syntax:

```
>[!SLIDE](analyze-project)
https://experienceleague-stage.adobe.com/en/slides/analyze-project
```

Gerendert:

<!--
>[!SLIDE](analyze-project)
-->

Bob: Entfernen Sie den Folienkommentar, sobald Sie das Thema loc-Sache testen.


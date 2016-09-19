---
title: "&#39;Microsoft.VisualBasic.ComClassAttribute&#39; cannot be applied to &#39;&lt;classname1&gt;&#39; because its container &#39;&lt;classname2&gt;&#39; is not declared &#39;Public&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4138b639-88d6-4b51-afcd-c92a1be36f1c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Microsoft.VisualBasic.ComClassAttribute&#39; cannot be applied to &#39;&lt;classname1&gt;&#39; because its container &#39;&lt;classname2&gt;&#39; is not declared &#39;Public&#39;
A class using a `COMClassAttribute` attribute block is declared inside a class that is not `Public`. If a class is to be exposed as a COM object, its entire containment hierarchy must be declared with `Public` access.  
  
 **Error ID:** BC32504  
  
### To correct this error  
  
-   Declare all containing classes `Public`, or remove the `COMClassAttribute` attribute block.  
  
## See Also  
 [NOT IN BUILD: Attributes Used in Visual Basic](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [ComClassAttribute Class](assetId:///5c2f0835-9210-47dc-bc59-5c1769953574)   
 [Public](../vs140/Public--Visual-Basic-.md)
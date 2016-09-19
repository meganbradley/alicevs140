---
title: "&#39;Microsoft.VisualBasic.ComClassAttribute&#39; is specified for class &#39;&lt;classname&gt;&#39; but it has no public members that can be exposed to COM; therefore no COM interfaces are generated"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 39aed273-bf27-4667-8116-022c4dd8f3c5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Microsoft.VisualBasic.ComClassAttribute&#39; is specified for class &#39;&lt;classname&gt;&#39; but it has no public members that can be exposed to COM; therefore no COM interfaces are generated
A class using a `COMClassAttribute` attribute block does not define any `Public` properties or methods. If a class is to be exposed as a COM object, its properties and methods must be declared with `Public` access.  
  
 The message is a warning by default. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40011  
  
### To correct this error  
  
-   Add the `Public` keyword to one or more properties or methods in the class, or remove the `COMClassAttribute` attribute block.  
  
## See Also  
 [NOT IN BUILD: Attributes Used in Visual Basic](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [Public](../vs140/Public--Visual-Basic-.md)   
 [ComClassAttribute Class](assetId:///5c2f0835-9210-47dc-bc59-5c1769953574)
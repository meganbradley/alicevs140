---
title: "&#39;System.Runtime.InteropServices.DispIdAttribute&#39; value cannot be applied to &#39;&lt;typename&gt;&#39; because &#39;Microsoft.VisualBasic.ComClassAttribute&#39; reserves zero for the default property"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a7d5b948-2d72-48b1-8baf-bfaae36b0128
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;System.Runtime.InteropServices.DispIdAttribute&#39; value cannot be applied to &#39;&lt;typename&gt;&#39; because &#39;Microsoft.VisualBasic.ComClassAttribute&#39; reserves zero for the default property
A <xref:System.Runtime.InteropServices.DispIdAttribute?qualifyHint=False> attribute block specifies a DISPID value of 0, which is reserved by `COMClassAttribute` to represent the default property of the class to which it is applied.  
  
 The dispatch identifier (DISPID) is used in COM as an argument to the `IDispatch:Invoke` method to access the properties and methods exposed by a COM object.  
  
 **Error ID:** BC32505  
  
### To correct this error  
  
-   Specify a DISPID value greater than zero in <xref:System.Runtime.InteropServices.DispIdAttribute?qualifyHint=False>.  
  
## See Also  
 <xref:System.Runtime.InteropServices.DispIdAttribute?qualifyHint=False>   
 [NOT IN BUILD: Attributes Used in Visual Basic](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [ComClassAttribute Class](assetId:///5c2f0835-9210-47dc-bc59-5c1769953574)
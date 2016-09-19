---
title: "&#39;Microsoft.VisualBasic.ComClassAttribute&#39; and &#39;&lt;attribute&gt;&#39; cannot both be applied to the same class"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc1bf4f1-f030-4df3-aae8-524af9c2fda7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Microsoft.VisualBasic.ComClassAttribute&#39; and &#39;&lt;attribute&gt;&#39; cannot both be applied to the same class
A `COMClassAttribute` attribute block is used in conjunction with an attribute that does not apply to COM objects. One possible cause is mixing [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] and COM attributes.  
  
 **Error ID:** BC32501  
  
### To correct this error  
  
-   Remove either the `COMClassAttribute` attribute block or the attribute that does not apply to COM.  
  
## See Also  
 [NOT IN BUILD: Attributes Used in Visual Basic](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [ComClassAttribute Class](assetId:///5c2f0835-9210-47dc-bc59-5c1769953574)
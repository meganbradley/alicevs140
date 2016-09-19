---
title: "VbStrConv.Wide and VbStrConv.Narrow are not applicable to the locale specified"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5811098c-b124-4caf-8a2b-f81f12f1d5f5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VbStrConv.Wide and VbStrConv.Narrow are not applicable to the locale specified
The application is attempting to use the `VbStrConv` enumeration members `Wide` or `Narrow`, which are not applicable to the specified locale.  
  
### To correct this error  
  
1.  Remove either `VbStrConv.Wide` or `VbStrConv.Narrow`.  
  
## See Also  
 <xref:System.Globalization?qualifyHint=False>   
 [NOTINBUILD VbStrConv Enumeration](assetId:///59f83dd9-6361-47df-a836-02ba9d4cb936)   
 [Introduction to International Applications Based on the .NET Framework](../vs140/Introduction-to-International-Applications-Based-on-the-.NET-Framework.md)
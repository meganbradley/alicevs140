---
title: "Extender instance is no longer valid."
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6361ba35-f2c5-4024-9362-46d7d9daf651
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Extender instance is no longer valid.
The Extender instance could not be created successfully or was destroyed.  
  
### To correct this error  
  
1.  Get the Extender instance again from the Extendee Object  
  
     —or—  
  
     Get the Extender instance again by calling DTE.ObjectExtenders.GetExtender().  
  
## See Also  
 <xref:EnvDTE.ObjectExtenders?qualifyHint=False>   
 <xref:EnvDTE.ObjectExtenders.GetExtender?qualifyHint=False>
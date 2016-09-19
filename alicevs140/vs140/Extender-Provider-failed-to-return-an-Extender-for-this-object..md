---
title: "Extender Provider failed to return an Extender for this object."
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 96702669-b720-4076-91b6-bb29ec830a65
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Extender Provider failed to return an Extender for this object.
No Extender could be returned.  
  
### To correct this error  
  
1.  Verify that your implementation of IExtenderProvider::CanExtend() and IExtenderProvider::GetExtender() succeeded in returning a valid Extender Object.  
  
## See Also  
 <xref:EnvDTE.IExtenderProvider?qualifyHint=False>   
 <xref:EnvDTE.ObjectExtenders?qualifyHint=False>
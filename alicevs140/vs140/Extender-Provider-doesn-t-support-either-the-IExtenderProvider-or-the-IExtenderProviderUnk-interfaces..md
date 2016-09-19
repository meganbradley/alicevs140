---
title: "Extender Provider doesn&#39;t support either the IExtenderProvider or the IExtenderProviderUnk interfaces."
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 77d596cd-28db-4ad5-bd4d-e451276e869c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Extender Provider doesn&#39;t support either the IExtenderProvider or the IExtenderProviderUnk interfaces.
The Extender Provider in use does not support the interface you have implemented.  
  
### To correct this error  
  
1.  Implement IExtenderProvider if the Extendee Object supports the IDispatch automation interface.  
  
     —or—  
  
     Implement IExtenderProviderUnk if the Extendee Object is based on IUnknown.  
  
## See Also  
 <xref:EnvDTE.IExtenderProviderUnk?qualifyHint=False>   
 <xref:EnvDTE.IExtenderProvider?qualifyHint=False>   
 <xref:EnvDTE.ObjectExtenders?qualifyHint=False>
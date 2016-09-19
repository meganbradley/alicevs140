---
title: "_ATL_STATIC_REGISTRY"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 00a84b69-ef3c-4ae4-a123-2e7811fa8472
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_STATIC_REGISTRY
A symbol that indicates you want the registration code for your object to be in the object to avoid a dependency on ATL.DLL.  
  
## Syntax  
  
```  
  
#define _ATL_STATIC_REGISTRY  
  
```  
  
## Remarks  
 When you define **ATL_STATIC_REGISTRY**, you should use the following code:  
  
 [!CODE [NVC_ATL_EventHandlingSample#5](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_EventHandlingSample#5)]  
  
## See Also  
 [Registry Macros](../vs140/Registry-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [DECLARE_STATIC_REGISTRY_RESOURCEID](assetId:///65a4379f-b5cb-4513-8dbd-cd6ff17122a6)   
 [DECLARE_REGISTRY_RESOURCE](../vs140/DECLARE_REGISTRY_RESOURCE.md)   
 [DECLARE_STATIC_REGISTRY_RESOURCE](assetId:///27cfc841-15bd-45e7-8677-f7062b334dc9)   
 [DECLARE_REGISTRY_RESOURCEID](../vs140/DECLARE_REGISTRY_RESOURCEID.md)
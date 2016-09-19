---
title: "CAtlModule::AddCommonRGSReplacements"
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
ms.assetid: a8b7e6e0-1121-49e3-8694-c9ad67fd8458
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlModule::AddCommonRGSReplacements
Override this method to add parameters to the ATL Registry Component (Registrar) replacement map.  
  
## Syntax  
  
```  
  
      virtual HRESULT AddCommonRGSReplacements(  
   IRegistrarBase* /*pRegistrar*/  
) throw( ) = 0;  
```  
  
#### Parameters  
 *pRegistrar*  
 Reserved.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 Replaceable parameters allow a Registrar's client to specify run-time data. To do this, the Registrar maintains a replacement map into which it enters the values associated with the replaceable parameters in your script. The Registrar makes these entries at run time.  
  
 See the topic [Using Replaceable Parameters (The Registrar's Preprocessor)](../vs140/Using-Replaceable-Parameters--The-Registrar-s-Preprocessor-.md) for more details.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlModule Class](../vs140/CAtlModule-Class.md)   
 [Registry Component (Registrar)](../vs140/ATL-Registry-Component--Registrar-.md)
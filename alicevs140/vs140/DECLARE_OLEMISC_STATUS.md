---
title: "DECLARE_OLEMISC_STATUS"
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
ms.assetid: bcd80ae6-2ed3-4338-9ab1-4f0952e3dedb
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_OLEMISC_STATUS
Used in ATL ActiveX controls to set the OLEMISC flags.  
  
## Syntax  
  
```  
  
      DECLARE_OLEMISC_STATUS(   
   miscstatus    
)  
```  
  
#### Parameters  
 *miscstatus*  
 All applicable OLEMISC flags.  
  
## Remarks  
 This macro is used to set the OLEMISC flags for an ActiveX control. Refer to [IOleObject::GetMiscStatus](http://msdn.microsoft.com/library/windows/desktop/ms678521) for more details.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#124](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#124)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Object Status Macros](../vs140/Object-Status-Macros.md)   
 [OLEMISC](http://msdn.microsoft.com/library/windows/desktop/ms678497)
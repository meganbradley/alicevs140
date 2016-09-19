---
title: "CComPtrBase::IsEqualObject"
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
ms.assetid: 77c77285-13dc-45e8-a8d9-2dc482553199
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtrBase::IsEqualObject
Call this method to check if the specified **IUnknown** points to the same object associated with the `CComPtrBase` object.  
  
## Syntax  
  
```  
  
      bool IsEqualObject(  
   IUnknown* pOther   
) throw( );  
```  
  
#### Parameters  
 `pOther`  
 The **IUnknown \*** to compare.  
  
## Return Value  
 Returns true if the objects are identical, false otherwise.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)
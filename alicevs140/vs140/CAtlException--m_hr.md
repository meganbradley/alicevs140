---
title: "CAtlException::m_hr"
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
ms.assetid: ea639a33-0d36-4dff-88b6-fb418f2b6102
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlException::m_hr
The `HRESULT` data member.  
  
## Syntax  
  
```  
  
HRESULT m_hr;  
  
```  
  
## Remarks  
 The data member that stores the error condition. The HRESULT value is set by the constructor, [CAtlException::CAtlException](../vs140/CAtlException--CAtlException.md).  
  
## Requirements  
 **Header:** atlexcept.h  
  
## See Also  
 [CAtlException Class](../vs140/CAtlException-Class.md)   
 [AtlThrow](../vs140/AtlThrow.md)
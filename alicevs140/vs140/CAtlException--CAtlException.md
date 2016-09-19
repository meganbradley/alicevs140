---
title: "CAtlException::CAtlException"
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
ms.assetid: f40fe36b-722f-4e8b-bdbc-f9a3a991ff24
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlException::CAtlException
The constructor.  
  
## Syntax  
  
```  
  
      CAtlException(  
   HRESULT hr   
) throw( );  
CAtlException( ) throw( );  
```  
  
#### Parameters  
 `hr`  
 The `HRESULT` error code.  
  
## Requirements  
 **Header:** atlexcept.h  
  
## See Also  
 [CAtlException Class](../vs140/CAtlException-Class.md)   
 [AtlThrow](../vs140/AtlThrow.md)
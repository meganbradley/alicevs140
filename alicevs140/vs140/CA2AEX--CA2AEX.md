---
title: "CA2AEX::CA2AEX"
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
ms.assetid: 003073e0-f466-4211-bbf9-97263075fad3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2AEX::CA2AEX
The constructor.  
  
## Syntax  
  
```  
  
      CA2AEX(  
   LPCSTR psz,  
   UINT nCodePage   
) throw(...);  
CA2AEX(  
   LPCSTR psz  
) throw(...);  
```  
  
#### Parameters  
 `psz`  
 The text string to be converted.  
  
 `nCodePage`  
 Unused in this class.  
  
## Remarks  
 Creates the buffer required for the translation.  
  
## Requirements  
 **Header:** atlconv.h  
  
## See Also  
 [CA2AEX Class](../vs140/CA2AEX-Class.md)
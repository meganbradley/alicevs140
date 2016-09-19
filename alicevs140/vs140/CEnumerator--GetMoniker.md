---
title: "CEnumerator::GetMoniker"
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
ms.topic: article
ms.assetid: 69a5cf2d-4a94-41dc-812d-bc1661d516d2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEnumerator::GetMoniker
Parses the display name to extract the component of the string that can be converted into a moniker.  
  
## Syntax  
  
```  
  
      HRESULT GetMoniker(   
   LPMONIKER* ppMoniker    
) const throw( );  
HRESULT GetMoniker(   
   LPMONIKER* ppMoniker,   
   LPCTSTR lpszDisplayName    
) const throw( );  
```  
  
#### Parameters  
 *ppMoniker*  
 [out] The moniker parsed from the display name ([CEnumeratorAccessor::m_szParseName](../vs140/CEnumeratorAccessor--m_szParseName.md)) of the current row.  
  
 *lpszDisplayName*  
 [in] The display name to parse.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CEnumerator Class](../vs140/CEnumerator-Class.md)
---
title: "IEnumOnSTLImpl::m_pcollection"
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
ms.assetid: 9352365c-e4f2-40ec-ba76-57f917673131
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IEnumOnSTLImpl::m_pcollection
This member points to the collection that provides the data driving the implementation of the enumerator interface.  
  
## Syntax  
  
```  
  
CollType* m_pcollection;  
  
```  
  
## Remarks  
 This member is initialized by a call to [IEnumOnSTLImpl::Init](../vs140/IEnumOnSTLImpl--Init.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IEnumOnSTLImpl Class](../vs140/IEnumOnSTLImpl-Class.md)   
 [IEnumOnSTLImpl::Init](../vs140/IEnumOnSTLImpl--Init.md)
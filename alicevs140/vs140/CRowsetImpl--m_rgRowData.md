---
title: "CRowsetImpl::m_rgRowData"
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
ms.assetid: e4e75ca7-12e8-4a0b-94e8-e395c21385b2
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowsetImpl::m_rgRowData
By default, a `CAtlArray` that templatizes on the user record template argument to `CRowsetImpl`.  
  
## Syntax  
  
```  
  
ArrayType CRowsetBaseImpl::m_rgRowData;  
  
```  
  
## Remarks  
 **ArrayType** is a template parameter to `CRowsetImpl`.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [CRowsetImpl Class](../vs140/CRowsetImpl-Class.md)   
 [CRowsetImpl::m_strCommandText](../vs140/CRowsetImpl--m_strCommandText.md)   
 [CRowsetImpl::m_strIndexText](../vs140/CRowsetImpl--m_strIndexText.md)
---
title: "CEnumeratorAccessor::m_szParseName"
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
ms.assetid: 32e826b6-0890-4db4-aa92-fc1ea3f528b2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEnumeratorAccessor::m_szParseName
String to pass to [IParseDisplayName](http://msdn.microsoft.com/library/windows/desktop/ms680604) to obtain a moniker for the data source or enumerator.  
  
## Syntax  
  
```  
  
WCHAR m_szParseName[129];  
  
```  
  
## Remarks  
 See [ISourcesRowset::GetSourcesRowset](https://msdn.microsoft.com/en-us/library/ms711200.aspx) in the *OLE DB Programmer's Reference* for more information.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CEnumeratorAccessor Class](../vs140/CEnumeratorAccessor-Class.md)
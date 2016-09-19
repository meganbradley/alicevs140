---
title: "CFile::GetPosition"
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
ms.assetid: e4274a9d-c40d-4309-b5f6-e226c00fc8f9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::GetPosition
Obtains the current value of the file pointer, which can be used in subsequent calls to `Seek`.  
  
## Syntax  
  
```  
  
virtual ULONGLONG GetPosition( ) const;  
```  
  
## Return Value  
 The file pointer.  
  
## Example  
 [!CODE [NVC_MFCFiles#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#8)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)
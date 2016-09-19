---
title: "CDatabase::m_hdbc"
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
ms.assetid: 8f24d05e-7c65-443e-b2cb-f88bfaf48e32
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::m_hdbc
Contains a public handle to an ODBC data source connection — a "connection handle."  
  
## Remarks  
 Normally, you will have no need to access this member variable directly. Instead, the framework allocates the handle when you call `OpenEx` or **Open**. The framework deallocates the handle when you call the **delete** operator on the `CDatabase` object. Note that the **Close** member function does not deallocate the handle.  
  
 Under some circumstances, however, you may need to use the handle directly. For example, if you need to call ODBC API functions directly rather than through class `CDatabase`, you may need a connection handle to pass as a parameter. See the code example below.  
  
## Example  
 [!CODE [NVC_MFCDatabase#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#15)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::OpenEx](../vs140/CDatabase--OpenEx.md)   
 [CDatabase::Open](../vs140/CDatabase--Open.md)   
 [CDatabase::Close](../vs140/CDatabase--Close.md)
---
title: "CWinAppEx::GetObjectA"
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
ms.assetid: f3b4f17e-4645-40d7-98c0-1fd50e920d2e
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetObjectA
Reads `CObject`-derived data from the registry. This is the MBCS form of the [CWinAppEx::GetObject](../vs140/CWinAppEx--GetObject.md) function.  
  
## Syntax  
  
```  
 GetObjectA(  
    LPCSTR lpszEntry,  
    CObject& obj  
);  
  
```  
  
#### Parameters  
 [in] `lpszEntry`  
 A string that contains the relative path of a registry entry.  
  
 [out] `obj`  
 A reference to a CObject. The method uses this reference to store the registry data.  
  
## Return Value  
 Nonzero if the method was successful; otherwise 0.  
  
## Remarks  
 See [CWinAppEx::GetObject](../vs140/CWinAppEx--GetObject.md).  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)
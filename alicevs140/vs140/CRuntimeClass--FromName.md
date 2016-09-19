---
title: "CRuntimeClass::FromName"
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
ms.assetid: 513566ec-9d7e-43b5-a46c-2821af3d76c5
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRuntimeClass::FromName
Call this function to retrieve the `CRuntimeClass` structure associated with the familiar name.  
  
## Syntax  
  
```  
  
      static CRuntimeClass* PASCAL FromName(  
   LPCSTR lpszClassName   
);  
static CRuntimeClass* PASCAL FromName(  
   LPCWSTR lpszClassName   
);  
```  
  
#### Parameters  
 `lpszClassName`  
 The familiar name of a class derived from `CObject`.  
  
## Return Value  
 A pointer to a `CRuntimeClass` object, corresponding to the name as passed in `lpszClassName`. The function returns **NULL** if no matching class name was found.  
  
## Example  
 [!CODE [NVC_MFCCObjectSample#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#17)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRuntimeClass::m_lpszClassName](../vs140/CRuntimeClass--m_lpszClassName.md)
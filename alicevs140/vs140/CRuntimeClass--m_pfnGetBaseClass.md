---
title: "CRuntimeClass::m_pfnGetBaseClass"
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
ms.assetid: 621d83dc-ef9d-4742-872c-a5d7a16837e9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRuntimeClass::m_pfnGetBaseClass
If your application uses the MFC library as a shared DLL, this data member points to a function that returns the `CRuntimeClass` structure of the base class.  
  
## Remarks  
 If your application statically links to the MFC library, see [m_pBaseClass](../vs140/CRuntimeClass--m_pBaseClass.md).  
  
## Example  
 See the example for [IsDerivedFrom](../vs140/CRuntimeClass--IsDerivedFrom.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)
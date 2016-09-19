---
title: "CRuntimeClass::IsDerivedFrom"
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
ms.assetid: abc519e5-0048-4f83-af5d-9a02667ba106
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRuntimeClass::IsDerivedFrom
Call this function to determine if the calling class is derived from the class specified in the *pBaseClass* parameter.  
  
## Syntax  
  
```  
  
      BOOL IsDerivedFrom(  
   const CRuntimeClass* pBaseClass   
) const;  
```  
  
#### Parameters  
 *pBaseClass*  
 The familiar name of a class derived from `CObject`.  
  
## Return Value  
 **TRUE** if the class calling `IsDerivedFrom` is derived from the base class whose `CRuntimeClass` structure is given as a parameter; otherwise **FALSE**.  
  
## Remarks  
 The relationship is determined by "walking" from the member's class up the chain of derived classes all the way to the top. This function only returns **FALSE** if no match is found for the base class.  
  
> [!NOTE]
>  To use the `CRuntimeClass` structure, you must include the `IMPLEMENT_DYNAMIC`, `IMPLEMENT_DYNCREATE`, or `IMPLEMENT_SERIAL` macro in the implementation of the class for which you want to retrieve run-time object information.  
  
 For more information on using `CRuntimeClass`, see the article [CObject Class: Accessing Run-Time Class Information](../vs140/Accessing-Run-Time-Class-Information.md).  
  
## Example  
 [!CODE [NVC_MFCCObjectSample#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#18)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)
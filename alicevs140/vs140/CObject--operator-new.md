---
title: "CObject::operator new"
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
ms.assetid: 888e72b4-b6f0-4397-a4cb-b3251dd5b3e1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObject::operator new
For the Release version of the library, operator **new** performs an optimal memory allocation in a manner similar to `malloc`.  
  
## Syntax  
  
```  
  
      void* PASCAL operator new(   
   size_t nSize    
);  
void* PASCAL operator new(   
   size_t,   
   void* p    
);  
void* PASCAL operator new(   
   size_t nSize,   
   LPCSTR lpszFileName,   
   int nLine    
);  
```  
  
## Remarks  
 In the Debug version, operator **new** participates in an allocation-monitoring scheme designed to detect memory leaks.  
  
 If you use the code line  
  
 [!CODE [NVC_MFCCObjectSample#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#14)]  
  
 before any of your implementations in a .CPP file, then the second version of **new** will be used, storing the filename and line number in the allocated block for later reporting. You do not have to worry about supplying the extra parameters; a macro takes care of that for you.  
  
 Even if you do not use `DEBUG_NEW` in Debug mode, you still get leak detection, but without the source-file line-number reporting described above.  
  
> [!NOTE]
>  If you override this operator, you must also override **delete**. Do not use the standard library **_new_handler** function.  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in the `CObject` examples.  
  
 [!CODE [NVC_MFCCObjectSample#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#16)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CObject Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObject::operator delete](../vs140/CObject--operator-delete.md)
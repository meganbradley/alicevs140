---
title: "CObject::operator delete"
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
ms.assetid: b1b73e64-b2d4-4b22-82b4-5bc68d83507d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObject::operator delete
For the Release version of the library, operator **delete** frees the memory allocated by operator **new**.  
  
## Syntax  
  
```  
  
      void PASCAL operator delete(  
   void* p   
);  
void PASCAL operator delete(  
   void* p,  
   void* pPlace  
);  
void PASCAL operator delete(  
   void* p,  
   LPCSTR lpszFileName,  
   int nLine   
);  
```  
  
## Remarks  
 In the Debug version, operator **delete** participates in an allocation-monitoring scheme designed to detect memory leaks.  
  
 If you use the code line  
  
 [!CODE [NVC_MFCCObjectSample#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#14)]  
  
 before any of your implementations in a .CPP file, then the third version of **delete** will be used, storing the filename and line number in the allocated block for later reporting. You do not have to worry about supplying the extra parameters; a macro takes care of that for you.  
  
 Even if you do not use `DEBUG_NEW` in Debug mode, you still get leak detection, but without the source-file line-number reporting described above.  
  
 If you override operators **new** and **delete**, you forfeit this diagnostic capability.  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in the `CObject` examples.  
  
 [!CODE [NVC_MFCCObjectSample#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#15)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CObject Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObject::operator new](../vs140/CObject--operator-new.md)
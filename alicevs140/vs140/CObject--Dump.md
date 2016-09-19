---
title: "CObject::Dump"
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
ms.assetid: 209696a4-1623-489e-9324-c4f2e9a445e0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObject::Dump
Dumps the contents of your object to a [CDumpContext](../vs140/CDumpContext-Class.md) object.  
  
## Syntax  
  
```  
  
      virtual void Dump(  
   CDumpContext& dc   
) const;  
```  
  
#### Parameters  
 `dc`  
 The diagnostic dump context for dumping, usually `afxDump`.  
  
## Remarks  
 When you write your own class, you should override the `Dump` function to provide diagnostic services for yourself and other users of your class. The overridden `Dump` usually calls the `Dump` function of its base class before printing data members unique to the derived class. `CObject::Dump` prints the class name if your class uses the `IMPLEMENT_DYNAMIC` or `IMPLEMENT_SERIAL` macro.  
  
> [!NOTE]
>  Your `Dump` function should not print a newline character at the end of its output.  
  
 `Dump` calls make sense only in the Debug version of the Microsoft Foundation Class Library. You should bracket calls, function declarations, and function implementations with **#ifdef _DEBUG**/`#endif` statements for conditional compilation.  
  
 Since `Dump` is a **const** function, you are not permitted to change the object state during the dump.  
  
 The [CDumpContext insertion (<<) operator](../vs140/CDumpContext--operator---.md) calls `Dump` when a `CObject` pointer is inserted.  
  
 `Dump` permits only "acyclic" dumping of objects. You can dump a list of objects, for example, but if one of the objects is the list itself, you will eventually overflow the stack.  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all `CObject` examples.  
  
 [!CODE [NVC_MFCCObjectSample#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#9)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CObject Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)
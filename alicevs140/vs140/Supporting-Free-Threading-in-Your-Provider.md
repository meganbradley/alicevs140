---
title: "Supporting Free Threading in Your Provider"
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
ms.assetid: a91270dc-cdf9-4855-88e7-88a54be7cbe8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Supporting Free Threading in Your Provider
All the OLE DB provider classes are thread-safe, and registry entries are set accordingly. It is a good idea to support free threading to help provide a high level of performance in multiuser situations. To help keep your provider thread-safe, you must verify that your code is blocked properly. Whenever you write or store data, you must block the access with critical sections.  
  
 Each OLE DB provider template object has its own critical section. To make blocking easier, each new class you create should be a template class taking the parent class name as an argument.  
  
 The following example shows how to block your code:  
  
```  
template <class T>  
class CMyObject<T> : public...  
  
HRESULT MyObject::MyMethod(void)  
{  
   T* pT = (T*)this;      // this gets the parent class   
  
// You don't need to do anything if you are only reading information  
  
// If you want to write information, do the following:  
   pT->Lock();         // engages critical section in the object  
   ...;                // write whatever information you wish  
   pT->Unlock();       // disengages the critical section  
}  
```  
  
 For more information about how to protect critical sections with `Lock` and `Unlock`, see [Multithreading: How To Use the Synchronization Classes](../vs140/Multithreading--How-to-Use-the-Synchronization-Classes.md).  
  
 You must also verify that any methods you override (such as `Execute`) are thread-safe.  
  
## See Also  
 [Working with OLE DB Provider Templates](../vs140/Working-with-OLE-DB-Provider-Templates.md)
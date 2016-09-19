---
title: "How to: Implement the lock C# Keyword (C++-CLI)"
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
ms.topic: get-started-article
H1: How to: Implement the lock C# Keyword (C++/CLI)
ms.assetid: 436fe544-ffb7-49b9-9798-90794e9974de
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Implement the lock C# Keyword (C++-CLI)
This topic shows how to implement the C# `lock` keyword in Visual C++. For more information, see [lock Statement](../Topic/lock%20Statement%20\(C%23%20Reference\).md).  
  
 You can also use the `lock` class in the C++ Support Library. See [Synchronization (lock Class)](../vs140/Synchronization--lock-Class-.md) for more information.  
  
## Example  
  
```  
// CS_lock_in_CPP.cpp  
// compile with: /clr  
using namespace System::Threading;  
ref class Lock {  
   Object^ m_pObject;  
public:  
   Lock( Object ^ pObject ) : m_pObject( pObject ) {  
      Monitor::Enter( m_pObject );  
   }  
   ~Lock() {  
      Monitor::Exit( m_pObject );  
   }  
};  
  
ref struct LockHelper {  
   void DoSomething();  
};  
  
void LockHelper::DoSomething() {  
   // Note: Reference type with stack allocation semantics to provide   
   // deterministic finalization  
  
   Lock lock( this );     
   // LockHelper instance is locked  
}  
  
int main()  
{  
   LockHelper lockHelper;  
   lockHelper.DoSomething();  
   return 0;  
}  
```  
  
## See Also  
 [Interoperability with other .NET languages in C++](../vs140/Interoperability-with-Other-.NET-Languages--C---CLI-.md)
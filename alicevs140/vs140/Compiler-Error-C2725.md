---
title: "Compiler Error C2725"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 13cd5b1b-e906-4cd8-9b2b-510d587c665a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2725
'exception' : unable to throw or catch a managed or WinRT object by value or reference  
  
 The type of a managed or WinRT exception was not correct.  
  
## Example  
 The following sample generates C2725 and shows how to fix it.  
  
```  
// C2725.cpp  
// compile with: /clr  
ref class R {  
public:  
   int i;  
};  
  
int main() {  
   R % r1 = *gcnew R;  
   throw r1;   // C2725  
  
   R ^ r2 = gcnew R;  
   throw r2;   // OK     
}  
```  
  
## Example  
 The following sample generates C2725 and shows how to fix it.  
  
```  
// C2725b.cpp  
// compile with: /clr  
using namespace System;  
int main() {  
   try {}  
   catch( System::Exception%) {}   // C2725  
   // try the following line instead  
   // catch( System::Exception ^e) {}  
}  
```  
  
## Example  
 The following sample generates C2725 and shows how to fix it.  
  
```  
// C2725c.cpp  
// compile with: /clr:oldSyntax  
using namespace System;  
int main() {  
   try {}  
   catch( System::Exception&) {}   // C2725  
   // try the following line instead  
   // catch( System::Exception *e) {}  
}  
```
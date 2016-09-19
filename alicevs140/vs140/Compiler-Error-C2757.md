---
title: "Compiler Error C2757"
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
ms.assetid: 421f102f-8a32-4d47-a109-811ddf2c909d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2757
'symbol' : a symbol with this name already exists and therefore this name cannot be used as a namespace name  
  
 A symbol used in the current compilation as a namespace identifier is already being used in a referenced assembly.  
  
 The following sample generates C2757:  
  
```  
// C2757a.cpp  
// compile with: /clr /LD  
public ref class Nes {};  
```  
  
 And then,  
  
```  
// C2757b.cpp  
// compile with: /clr /c  
#using <C2757a.dll>  
  
namespace Nes {    // C2757  
// try the following line instead  
// namespace Nes2 {  
   public ref class X {};  
}  
```  
  
 The following sample generates C2757:  
  
```  
// C2757c.cpp  
// compile with: /clr:oldSyntax /LD  
#using <mscorlib.dll>  
public __gc class Nes {};  
```  
  
 And then,  
  
```  
// C2757d.cpp  
// compile with: /clr:oldSyntax /c  
#using <C2757c.dll>  
#using <mscorlib.dll>  
  
namespace Nes {    // C2757  
// try the following line instead  
// namespace Nes2 {  
   public __gc class X {};  
}  
```
---
title: "Compiler Error C3271"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 16d8bd1d-2e30-4c6a-a07f-0c4f3342fab5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3271
'member': invalid value 'value' for the FieldOffset attribute  
  
 A negative number was passed to the [FieldOffset](frlrfSystemRuntimeInteropServicesFieldOffsetAttributeClassTopic) attribute.  
  
 The following sample generates C3271:  
  
```  
// C3271.cpp  
// compile with: /clr /c  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
[StructLayout(LayoutKind::Explicit)]  
value class MyStruct1 {  
   public: [FieldOffset(0)] int a;  
   public: [FieldOffset(-1)] long b;   // C3271  
};  
```  
  
 The following sample generates C3271:  
  
```  
// C3271_2.cpp  
// compile with: /clr:oldSyntax  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
[StructLayout(LayoutKind::Explicit)]  
__value class MyStruct1 {  
   public: [FieldOffset(0)] int a;  
   public: [FieldOffset(-1)] long b;   // C3271  
};  
  
static int main() {  
   MyStruct1* a = __nogc new MyStruct1();  
};  
```
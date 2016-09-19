---
title: "Compiler Warning C4958"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e79b9e9c-d572-4a3a-a3b6-60962b70864a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning C4958
'operation' : pointer arithmetic is not verifiable  
  
 Using pointer arithmetic will produce an unverifiable image.  
  
 For more information, see [Pure / Verifiable](../vs140/Pure-and-Verifiable-Code--C---CLI-.md).  
  
 This warning is issued as an error and can be disabled with the [warning](../vs140/warning.md) pragma or the [/wd](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md) compiler option.  
  
 The following sample generates C4958:  
  
```  
// C4958.cpp  
// compile with: /clr:safe  
// #pragma warning( disable : 4958 )  
using namespace System;  
  
int main( ) {  
   Int32 arr[] = new Int32[10];  
   Int32* p = &arr[0];  
   p++;   // C4958  
}  
```  
  
 The compiler implements array operations with pointer arithmetic. Therefore, native arrays are not verifiable; use a CLR array instead. For more information, see [array](../vs140/Arrays--C---Component-Extensions-.md).  
  
 The following sample generates C4958:  
  
```  
// C4958b.cpp  
// compile with: /clr:safe  
// #pragma warning( disable : 4958 )  
  
int main() {  
   int array[5];  
   array[4] = 0;   // C4958  
}  
```
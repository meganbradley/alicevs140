---
title: "How to: Obtain a Pointer to Byte Array"
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
ms.assetid: aea18073-3341-47f4-9f0e-04e03327037e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Obtain a Pointer to Byte Array
You can obtain a pointer to the array block in a <xref:System.Byte?qualifyHint=False> array by taking the address of the first element and assigning it to a pointer.  
  
## Example  
  
```  
// pointer_to_Byte_array.cpp  
// compile with: /clr  
using namespace System;  
int main() {  
   Byte bArr[] = {1, 2, 3};  
   Byte* pbArr = &bArr[0];  
  
   array<Byte> ^ bArr2 = gcnew array<Byte>{1,2,3};  
   interior_ptr<Byte> pbArr2 = &bArr2[0];  
}  
```  
  
## See Also  
 [Using C++ Interop Features](../vs140/Using-C---Interop--Implicit-PInvoke-.md)
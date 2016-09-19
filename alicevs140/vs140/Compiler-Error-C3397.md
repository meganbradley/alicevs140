---
title: "Compiler Error C3397"
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
ms.assetid: a8536e87-79c4-4ed7-bd96-42704d06391f
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3397
Aggregate initialization is not allowed in default arguments  
  
 An array was declared incorrectly.  See [array](../vs140/Arrays--C---Component-Extensions-.md) for more information.  
  
## Example  
 The following sample generates C3397.  
  
```  
// C3397.cpp  
// compile with: /clr  
// /clr /c  
void Func(array<int> ^p = gcnew array<int> { 1, 2, 3 });   // C3397  
void Func2(array<int> ^p = gcnew array<int> (3));   // OK  
  
int main() {  
   array<int> ^p = gcnew array<int> { 1, 2, 3};   // OK  
}  
```
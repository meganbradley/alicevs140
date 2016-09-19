---
title: "Compiler Warning (level 4) C4629"
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
ms.assetid: 158cde12-bae5-4d43-b575-b52b35aaa0b9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4629
digraph used, character sequence 'digraph' interpreted as token 'char' (insert a space between the two characters if this is not what you intended)  
  
 Under [/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md), the compiler warns when it detects a digraph.  
  
 The following sample generates C4629:  
  
```  
// C4629.cpp  
// compile with: /Za /W4  
int main()  
<%   // C4629 <% digraph for {  
}  
```
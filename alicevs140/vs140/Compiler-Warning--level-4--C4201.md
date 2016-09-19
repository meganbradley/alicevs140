---
title: "Compiler Warning (level 4) C4201"
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
ms.topic: error-reference
ms.assetid: 6156f508-9393-4d77-9e73-1ec3e1c32d0d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4201
nonstandard extension used : nameless struct/union  
  
 Under Microsoft extensions (/Ze), you can specify a structure without a declarator as members of another structure or union. These structures generate an error under ANSI compatibility ([/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)).  
  
## Example  
  
```  
// C4201.cpp  
// compile with: /W4  
struct S  
{  
   float y;  
   struct  
   {  
      int a, b, c;  // C4201  
   };  
} *p_s;  
  
int main()  
{  
}  
```
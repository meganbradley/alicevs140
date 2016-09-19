---
title: "Compiler Warning (level 1) C4079"
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
ms.assetid: 549759f0-e168-47e9-8c9a-de93ac843689
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4079
unexpected token 'token'  
  
 An unexpected separator token occurs in a pragma argument list. The remainder of the pragma was ignored.  
  
 The following sample generates C4079:  
  
```  
// C4079.cpp  
// compile with: /W1  
#pragma warning(disable : 4081)  
#pragma pack(c,16)   // C4079  
  
int main() {  
}  
```
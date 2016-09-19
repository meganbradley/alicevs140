---
title: "Linker Tools Error LNK2033"
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
ms.assetid: d61db467-9328-4788-bf54-e2a20537f13f
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK2033
unresolved typeref token (token) for 'type'  
  
 A type doesn’t have a definition in MSIL metadata.  
  
 LNK2033 can occur when compiling with **/clr:safe** and where there is only a forward declaration for a type in an MSIL module, where the type is referenced in the MSIL module.  
  
 The type needs to be defined under **/clr:safe**.  
  
 For more information, see [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
## Example  
 The following sample generates LNK2033.  
  
```  
// LNK2033.cpp  
// compile with: /clr:safe  
// LNK2033 expected  
ref class A;  
ref class B {};  
  
int main() {  
   A ^ aa = nullptr;  
   B ^ bb = nullptr;   // OK  
};  
```
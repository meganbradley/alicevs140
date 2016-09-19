---
title: "Linker Tools Warning LNK4253"
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
ms.assetid: ec7433a9-aa9c-495a-a9f2-075e7bc3e7bc
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4253
section 'section1' not merged into 'section2'; already merged into 'section3'  
  
 The linker detected multiple, conflicting merge requests. The linker will ignore one of the requests.  
  
 A **/MERGE** option or directive is encountered and the `from` section has already been merged into a different section due to a previous **/MERGE** option or directive (or due to an implicit merge from the linker).  
  
 To resolve LNK4253, remove one of the merge requests.  
  
 When targeting x86 machines and Windows CE targets (ARM, MIPS, SH4, and Thumb) with Visual C++, the .CRT section is now read only. If your code depends on the previous behavior (.CRT sections are read/write), you could see unexpected behavior.  
  
 For more information, see,  
  
-   [/MERGE (Combine Sections)](../vs140/-MERGE--Combine-Sections-.md)  
  
-   [comment (C/C++)](../vs140/comment--C-C---.md)  
  
## Example  
 In the following sample, the linker is instructed to merge the `.rdata` section twice, but into different sections. The following sample generates LNK4253.  
  
```  
// LNK4253.cpp  
// compile with: /W1 /link /merge:.rdata=text2  
// LNK4253 expected  
#pragma comment(linker, "/merge:.rdata=.text")  
int main() {}  
```
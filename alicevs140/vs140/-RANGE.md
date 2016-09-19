---
title: "-RANGE"
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
ms.topic: article
H1: /RANGE
ms.assetid: 7eeba266-32be-49cc-a350-96bdf541f98a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -RANGE
Modifies the output of dumpbin when used with other dumpbin options, such as /RAWDATA or /DISASM.  
  
## Syntax  
  
```  
/RANGE:vaMin[,vaMax]  
```  
  
## Flags  
 **vaMin**  
 The virtual address at which you want the dumpbin operation to begin.  
  
 **vaMax** (optional)  
 The virtual address at which you want the dumpbin operation to end. If not specified, dumpbin will go to the end of the file.  
  
## Remarks  
 To see the virtual addresses for an image, use the map file for the image (RVA + Base), the **/DISASM** or **/HEADERS** option of dumpbin, or the disassembly window in the Visual Studio debugger.  
  
## Example  
 In this example, **/range** is used to modify the display of the **/disasm** option. In this example, the starting value is expressed as a decimal number and the ending value is specified as a hex number.  
  
```  
dumpbin /disasm /range:4219334,0x004061CD t.exe  
```  
  
## See Also  
 [DUMPBIN Options](../vs140/DUMPBIN-Options.md)
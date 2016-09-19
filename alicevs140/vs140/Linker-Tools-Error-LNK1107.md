---
title: "Linker Tools Error LNK1107"
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
ms.assetid: a37a893d-5efa-4eba-8f40-6c5518b4b9d0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1107
invalid or corrupt file: cannot read at location  
  
 The tool could not read the file. Recreate the file.  
  
 LNK1107 could also occur if you attempt to pass a module (.dll or .netmodule extension created with [/clr:noAssembly](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) or  [/NOASSEMBLY](../Topic/-NOASSEMBLY%20\(Create%20a%20MSIL%20Module\).md)) to the linker; pass the .obj file instead.  
  
 If you compile the following sample:  
  
```  
// LNK1107.cpp  
// compile with: /clr /LD  
public ref class MyClass {  
public:  
   void Test(){}  
};  
```  
  
 and then specify **link LNK1107.dll** on the command line, you will get LNK1107.  To resolve the error, specify **link LNK1107.obj** instead.
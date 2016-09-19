---
title: "const_seg"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1eb58ee2-fb0e-4a39-9621-699c8f5ef957
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# const_seg
Specifies the segment where [const](../vs140/const--C---.md) variables are stored in the .obj file.  
  
## Syntax  
  
```  
#pragma const_seg ( [ [ { push | pop}, ] [ identifier, ] ] [ "segment-name" [, "segment-class" ] )  
```  
  
## Remarks  
 The meaning of the terms *segment* and *section* are interchangeable in this topic.  
  
 OBJ files can be viewed with the [dumpbin](../vs140/DUMPBIN-Command-Line.md) application. The default segment in the .obj file for `const` variables is .rdata. Some `const` variables, such as scalars, are automatically inlined into the code stream. Inlined code will not appear in .rdata.  
  
 Defining an object requiring dynamic initialization in a `const_seg` results in undefined behavior.  
  
 `#pragma const_seg` with no parameters resets the segment to .rdata.  
  
 `push` (optional)  
 Puts a record on the internal compiler stack. A `push` can have an `identifier` and `segment-name`.  
  
 `pop` (optional)  
 Removes a record from the top of the internal compiler stack.  
  
 `identifier` (optional)  
 When used with `push`, assigns a name to the record on the internal compiler stack. When used with `pop`, pops records off the internal stack until `identifier` is removed; if `identifier` is not found on the internal stack, nothing is popped.  
  
 Using `identifier` enables multiple records to be popped with a single `pop` command.  
  
 "`segment-name`" (optional)  
 The name of a segment. When used with `pop`, the stack is popped and `segment-name` becomes the active segment name.  
  
 "`segment-class`" (optional)  
 Included for compatibility with C++ prior to version 2.0. It is ignored.  
  
## Example  
  
```  
// pragma_directive_const_seg.cpp  
// compile with: /EHsc  
#include <iostream>  
  
const int i = 7;               // inlined, not stored in .rdata  
const char sz1[]= "test1";     // stored in .rdata  
  
#pragma const_seg(".my_data1")  
const char sz2[]= "test2";     // stored in .my_data1  
  
#pragma const_seg(push, stack1, ".my_data2")  
const char sz3[]= "test3";     // stored in .my_data2  
  
#pragma const_seg(pop, stack1) // pop stack1 from stack  
const char sz4[]= "test4";     // stored in .my_data1  
  
int main() {  
    using namespace std;  
   // const data must be referenced to be put in .obj  
   cout << sz1 << endl;  
   cout << sz2 << endl;  
   cout << sz3 << endl;  
   cout << sz4 << endl;  
}  
```  
  
 **test1**  
**test2**  
**test3**  
**test4**   
## Comments  
 See [/SECTION](../vs140/-SECTION--Specify-Section-Attributes-.md) for a list of names you should not use when creating a section.  
  
 You can also specify sections for initialized data ([data_seg](../vs140/data_seg.md)), uninitialized data ([bss_seg](../vs140/bss_seg.md)), and functions ([code_seg](../vs140/code_seg.md)).  
  
## See Also  
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)
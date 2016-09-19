---
title: "Visual C++ Structures in Class Designer"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bad18ab6-d956-47a6-a413-811cc26db5f5
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Visual C++ Structures in Class Designer
Class Designer supports C++ structures, which are declared with the keyword `struct`. Following is an example:  
  
```  
struct MyStructure  
{  
   char a;  
   int i;  
   long j;  
};  
```  
  
 For more information about using the `struct` type, see [struct (C++)](../vs140/struct--C---.md).  
  
 A C++ structure shape in a class diagram looks and works like a class shape, except that the label reads **Struct** and it has square corners instead of rounded corners.  
  
|Code element|Class Designer view|  
|------------------|-------------------------|  
|`struct StructureName {};`|**StructureName**<br /><br /> Struct|  
  
## See Also  
 [Working with Visual C++ Code in Class Designer](../vs140/Working-with-Visual-C---Code--Class-Designer-.md)   
 [Classes, Structures, and Unions](../vs140/Classes-and-Structs--C---.md)   
 [struct (C++)](../vs140/struct--C---.md)
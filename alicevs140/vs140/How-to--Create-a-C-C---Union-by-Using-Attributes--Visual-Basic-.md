---
title: "How to: Create a C-C++ Union by Using Attributes (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
H1: How to: Create a C/C++ Union by Using Attributes (Visual Basic)
ms.assetid: 9352a7e4-c0da-4d07-aa14-55ed43736fcb
caps.latest.revision: 6
---
# How to: Create a C-C++ Union by Using Attributes (Visual Basic)
By using attributes you can customize how structs are laid out in memory. For example, you can create what is known as a union in C/C++ by using the `StructLayout(LayoutKind.Explicit)` and `FieldOffset` attributes.  
  
## Example  
 In this code segment, all of the fields of `TestUnion` start at the same location in memory.  
  
```vb  
' Add an Imports statement for System.Runtime.InteropServices.  
  
<System.Runtime.InteropServices.StructLayout(   
      System.Runtime.InteropServices.LayoutKind.Explicit)>   
Structure TestUnion  
    <System.Runtime.InteropServices.FieldOffset(0)>   
    Public i As Integer  
  
    <System.Runtime.InteropServices.FieldOffset(0)>   
    Public d As Double  
  
    <System.Runtime.InteropServices.FieldOffset(0)>   
    Public c As Char  
  
    <System.Runtime.InteropServices.FieldOffset(0)>   
    Public b As Byte  
End Structure  
```  
  
## Example  
 The following is another example where fields start at different explicitly set locations.  
  
```vb  
' Add an Imports statement for System.Runtime.InteropServices.  
  
 <System.Runtime.InteropServices.StructLayout(   
      System.Runtime.InteropServices.LayoutKind.Explicit)>   
Structure TestExplicit  
     <System.Runtime.InteropServices.FieldOffset(0)>   
     Public lg As Long  
  
     <System.Runtime.InteropServices.FieldOffset(0)>   
     Public i1 As Integer  
  
     <System.Runtime.InteropServices.FieldOffset(4)>   
     Public i2 As Integer  
  
     <System.Runtime.InteropServices.FieldOffset(8)>   
     Public d As Double  
  
     <System.Runtime.InteropServices.FieldOffset(12)>   
     Public c As Char  
  
     <System.Runtime.InteropServices.FieldOffset(14)>   
     Public b As Byte  
 End Structure  
```  
  
 The two integer fields, `i1` and `i2`, share the same memory locations as `lg`. This sort of control over struct layout is useful when using platform invocation.  
  
## See Also  
 <xref:System.Reflection?qualifyHint=False>   
 <xref:System.Attribute?qualifyHint=False>   
 [Visual Basic Programming Guide](../vs140/Visual-Basic-Programming-Guide.md)   
 [Extending Metadata Using Attributes](assetId:///30386922-1e00-4602-9ebf-526b271a8b87)   
 [Reflection (Visual Basic)](../Topic/Reflection%20\(Visual%20Basic\).md)   
 [Attributes (Visual Basic)](../vs140/Attributes--Visual-Basic-1.md)   
 [Creating Custom Attributes (Visual Basic)](../Topic/Creating%20Custom%20Attributes%20\(Visual%20Basic\).md)   
 [Accessing Attributes by Using Reflection (Visual Basic)](../Topic/Accessing%20Attributes%20by%20Using%20Reflection%20\(Visual%20Basic\).md)
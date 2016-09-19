---
title: "User-Defined Data Type"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: be913dca-a364-4a51-96a1-549a1b390b0a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# User-Defined Data Type
Holds data in a format you define. The `Structure` statement defines the format.  
  
 Previous versions of Visual Basic support the user-defined type (UDT). The current version expands the UDT to a *structure*. A structure is a concatenation of one or more *members* of various data types. Visual Basic treats a structure as a single unit, although you can also access its members individually.  
  
## Remarks  
 Define and use a structure data type when you need to combine various data types into a single unit, or when none of the elementary data types serve your needs.  
  
 The default value of a structure data type consists of the combination of the default values of each of its members.  
  
## Declaration Format  
 A structure declaration starts with the [Structure Statement](../Topic/Structure%20Statement.md) and ends with the `End``Structure` statement. The `Structure` statement supplies the name of the structure, which is also the identifier of the data type the structure is defining. Other parts of the code can use this identifier to declare variables, parameters, and function return values to be of this structure's data type.  
  
 The declarations between the `Structure` and `End``Structure` statements define the members of the structure.  
  
## Member Access Levels  
 You must declare every member using a [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md) or a statement that specifies access level, such as [Public (Visual Basic)](../vs140/Public--Visual-Basic-.md), [Friend (Visual Basic)](../Topic/Friend%20\(Visual%20Basic\).md), or [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md). If you use a `Dim` statement, the access level defaults to public.  
  
## Programming Tips  
  
-   **Memory Consumption.** As with all composite data types, you cannot safely calculate the total memory consumption of a structure by adding together the nominal storage allocations of its members. Furthermore, you cannot safely assume that the order of storage in memory is the same as your order of declaration. If you need to control the storage layout of a structure, you can apply the <xref:System.Runtime.InteropServices.StructLayoutAttribute?qualifyHint=False> attribute to the `Structure` statement.  
  
-   **Interop Considerations.** If you are interfacing with components not written for the .NET Framework, for example Automation or COM objects, keep in mind that user-defined types in other environments are not compatible with Visual Basic structure types.  
  
-   **Widening.** There is no automatic conversion to or from any structure data type. You can define conversion operators on your structure using the [Operator Statement](../vs140/Operator-Statement.md), and you can declare each conversion operator to be `Widening` or `Narrowing`.  
  
-   **Type Characters.** Structure data types have no literal type character or identifier type character.  
  
-   **Framework Type.** There is no corresponding type in the .NET Framework. All structures inherit from the .NET Framework class <xref:System.ValueType?qualifyHint=True>, but no individual structure corresponds to <xref:System.ValueType?qualifyHint=True>.  
  
## Example  
 The following paradigm shows the outline of the declaration of a structure.  
  
```  
[Public | Protected | Friend | Protected Friend | Private] Structure structname  
    {Dim | Public | Friend | Private} member1 As datatype1  
    ' ...  
    {Dim | Public | Friend | Private} memberN As datatypeN  
End Structure  
```  
  
## See Also  
 <xref:System.ValueType?qualifyHint=False>   
 <xref:System.Runtime.InteropServices.StructLayoutAttribute?qualifyHint=False>   
 [Data Types](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Conversion Summary](../vs140/Conversion-Summary--Visual-Basic-.md)   
 [Structure Statement](../Topic/Structure%20Statement.md)   
 [Widening](../vs140/Widening--Visual-Basic-.md)   
 [Narrowing](../vs140/Narrowing--Visual-Basic-.md)   
 [Structures](../vs140/Structures--Visual-Basic-.md)   
 [Efficient Use of Data Types](../Topic/Efficient%20Use%20of%20Data%20Types%20\(Visual%20Basic\).md)
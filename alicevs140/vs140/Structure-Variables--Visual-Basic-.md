---
title: "Structure Variables (Visual Basic)"
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
ms.assetid: 156872f8-aabc-4454-8e2d-f2253c3c13c9
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Structure Variables (Visual Basic)
Once you have created a structure, you can declare procedure-level and module-level variables as that type. For example, you can create a structure that records information about a computer system. The following example demonstrates this.  
  
```  
Public Structure systemInfo  
    Public cPU As String  
    Public memory As Long  
    Public purchaseDate As Date  
End Structure  
```  
  
 You can now declare variables of that type. The following declaration illustrates this.  
  
```  
Dim mySystem, yourSystem As systemInfo  
```  
  
> [!NOTE]
>  In classes and modules, structures declared using the [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md) default to public access. If you intend a structure to be private, make sure you declare it using the [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md) keyword.  
  
## Access to Structure Values  
 To assign and retrieve values from the elements of a structure variable, you use the same syntax as you use to set and get properties on an object. You place the member access operator (`.`) between the structure variable name and the element name. The following example accesses elements of the variables previously declared as type `systemInfo`.  
  
```  
mySystem.cPU = "486"  
Dim tooOld As Boolean  
If yourSystem.purchaseDate < #1/1/1992# Then tooOld = True  
```  
  
## Assigning Structure Variables  
 You can also assign one variable to another if both are of the same structure type. This copies all the elements of one structure to the corresponding elements in the other. The following declaration illustrates this.  
  
```  
yourSystem = mySystem  
```  
  
 If a structure element is a reference type, such as a `String`, `Object`, or array, the pointer to the data is copied. In the previous example, if `systemInfo` had included an object variable, then the preceding example would have copied the pointer from `mySystem` to `yourSystem`, and a change to the object's data through one structure would be in effect when accessed through the other structure.  
  
## See Also  
 [Data Types in Visual Basic](../vs140/Data-Types-in-Visual-Basic.md)   
 [Elementary Data Types](../vs140/Elementary-Data-Types--Visual-Basic-.md)   
 [Composite Data Types](../vs140/Composite-Data-Types--Visual-Basic-.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [Structures: Your Own Data Types](../vs140/Structures--Visual-Basic-.md)   
 [Troubleshooting Data Types](../Topic/Troubleshooting%20Data%20Types%20\(Visual%20Basic\).md)   
 [How to: Declare a Structure](../vs140/How-to--Declare-a-Structure--Visual-Basic-.md)   
 [Structures and Other Programming Elements](../vs140/Structures-and-Other-Programming-Elements--Visual-Basic-.md)   
 [Structures and Classes](../Topic/Structures%20and%20Classes%20\(Visual%20Basic\).md)   
 [Structure Statement](../Topic/Structure%20Statement.md)
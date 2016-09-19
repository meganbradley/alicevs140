---
title: "Records (F#)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 1c0ac404-c6d6-4b28-b2dc-c94213fc6f39
caps.latest.revision: 34
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Records (F#)
Records represent simple aggregates of named values, optionally with members.  
  
## Syntax  
  
```  
[ attributes ]  
type [accessibility-modifier] typename = {   
    [ mutable ] label1 : type1;  
    [ mutable ] label2 : type2;  
    ...  
    }  
    member-list  
```  
  
## Remarks  
 In the previous syntax, `typename` is the name of the record type, `label1` and `label2` are names of values, referred to as *labels*, and `type1` and `type2` are the types of these values. `member-list` is the optional list of members for the type.  
  
 Following are some examples.  
  
 [!CODE [FsLangRef1#1901](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1901)]  
  
 When each label is on a separate line, the semicolon is optional.  
  
 You can set values in expressions known as *record expressions*. The compiler infers the type from the labels used (if the labels are sufficiently distinct from those of other record types). Braces ({ }) enclose the record expression. The following code shows a record expression that initializes a record with three float elements with labels `x`, `y` and `z`.  
  
 [!CODE [FsLangRef1#1907](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1907)]  
  
 Do not use the shortened form if there could be another type that also has the same labels.  
  
 [!CODE [FsLangRef1#1903](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1903)]  
  
 The labels of the most recently declared type take precedence over those of the previously declared type, so in the preceding example, `mypoint3D` is inferred to be `Point3D`. You can explicitly specify the record type, as in the following code.  
  
 [!CODE [FsLangRef1#1908](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1908)]  
  
 Methods can be defined for record types just as for class types.  
  
## Creating Records by Using Record Expressions  
 You can initialize records by using the labels that are defined in the record. An expression that does this is referred to as a *record expression*. Use braces to enclose the record expression and use the semicolon as a delimiter.  
  
 The following example shows how to create a record.  
  
 [!CODE [FsLangRef1#1904](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1904)]  
  
 The semicolons after the last field in the record expression and in the type definition are optional, regardless of whether the fields are all in one line.  
  
 When you create a record, you must supply values for each field. You cannot refer to the values of other fields in the initialization expression for any field.  
  
 In the following code, the type of `myRecord2` is inferred from the names of the fields. Optionally, you can specify the type name explicitly.  
  
 [!CODE [FsLangRef1#1905](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1905)]  
  
 Another form of record construction can be useful when you have to copy an existing record, and possibly change some of the field values. The following line of code illustrates this.  
  
 [!CODE [FsLangRef1#1906](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1906)]  
  
 This form of the record expression is called the *copy and update record expression*.  
  
 Records are immutable by default; however, you can easily create modified records by using a copy and update expression. You can also explicitly specify a mutable field.  
  
 [!CODE [FsLangRef1#1909](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1909)]  
  
 Don't use the DefaultValue attribute with record fields. A better approach is to define default instances of records with fields that are initialized to default values and then use a copy and update record expression to set any fields that differ from the default values.  
  
```f#  
// Rather than use [<DefaultValue>], define a default record.  
type MyRecord =  
    {   
        field1 : int   
        field2 : int  
    }  
  
let defaultRecord1 = { field1 = 0; field2 = 0 }  
let defaultRecord2 = { field1 = 1; field2 = 25 }  
  
// Use the with keyword to populate only a few chosen fields  
// and leave the rest with default values.  
let rr3 = { defaultRecord1 with field2 = 42 }  
  
```  
  
## Pattern Matching with Records  
 Records can be used with pattern matching. You can specify some fields explicitly and provide variables for other fields that will be assigned when a match occurs. The following code example illustrates this.  
  
 [!CODE [FsLangRef1#1910](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1910)]  
  
 The output of this code is as follows.  
  
```  
Point is at the origin.  
Point is on the x-axis. Value is 100.000000.  
Point is at (10.000000, 0.000000, -1.000000).  
```  
  
## Differences Between Records and Classes  
 Record fields differ from classes in that they are automatically exposed as properties, and they are used in the creation and copying of records. Record construction also differs from class construction. In a record type, you cannot define a constructor. Instead, the construction syntax described in this topic applies. Classes have no direct relationship between constructor parameters, fields, and properties.  
  
 Like union and structure types, records have structural equality semantics. Classes have reference equality semantics. The following code example demonstrates this.  
  
 [!CODE [FsLangRef1#1911](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1911)]  
  
 If you write the same code with classes, the two class objects would be unequal because the two values would represent two objects on the heap and only the addresses would be compared (unless the class type overrides the `System.Object.Equals` method).  
  
## See Also  
 [F# Types](../vs140/F#-Types.md)   
 [Classes (F#)](../vs140/Classes--F#-.md)   
 [F# Language Reference](../Topic/F%23%20Language%20Reference.md)   
 [Patterns (F#)](../vs140/Pattern-Matching--F#-.md)
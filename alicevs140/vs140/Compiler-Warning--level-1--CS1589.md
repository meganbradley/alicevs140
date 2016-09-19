---
title: "Compiler Warning (level 1) CS1589"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bdc47124-93ae-4c6a-81b2-dde8ec4d0ab1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1589
Unable to include XML fragment 'fragment' of file 'file' -- reason  
  
 The syntax (*fragment*) of a [<include\>](../vs140/-include---C#-Programming-Guide-.md) tag, which referenced a file (`file`), was incorrect for the specified ***reason***.  
  
 A malformed line will be placed in the generated XML file.  
  
 The following sample generates CS1589:  
  
```  
// CS1589.cs  
// compile with: /W:1 /doc:CS1589_out.xml  
  
/// <include file='CS1589.doc' path='MyDocs/MyMembers[@name="test"]/' />   // CS1589  
// try the following line instead  
// /// <include file='CS1589.doc' path='MyDocs/MyMembers[@name="test"]/*' />  
class Test  
{  
   public static void Main()  
   {  
   }  
}  
```
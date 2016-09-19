---
title: "Compiler Error CS0616"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: ed60f7bb-40cf-4a93-b823-e29e83df7bf7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0616
'class' is not an attribute class  
  
 An attempt was made to use a non-attribute class in an attribute block. All the attribute types need to be inherited from <xref:System.Attribute?qualifyHint=True>.  
  
## Example  
 The following sample generates CS0616.  
  
```  
// CS0616.cs  
// compile with: /target:library  
[CMyClass(i = 5)]   // CS0616  
public class CMyClass {}  
```  
  
## Example  
 The following sample shows how you might define an attribute:  
  
```  
// CreateAttrib.cs  
// compile with: /target:library  
using System;  
  
[AttributeUsage(AttributeTargets.Class|AttributeTargets.Interface)]  
public class MyAttr : Attribute  
{  
   public int Name = 0;  
   public int Count = 0;  
  
   public MyAttr (int iCount, int sName)  
   {  
      Count = iCount;  
      Name = sName;  
   }  
}  
  
[MyAttr(5, 50)]  
class Class1 {}  
  
[MyAttr(6, 60)]  
interface Interface1 {}  
```
---
title: "Compiler Error CS0012"
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
ms.assetid: 5523e349-22f4-4b0b-b4b0-c4bf26c461f4
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0012
The type 'type' is defined in an assembly that is not referenced. You must add a reference to assembly 'assembly'.  
  
 The definition for a referenced type was not found. This could occur if a required .DLL file is not included in the compilation. For more information, see [Add Reference Dialog Box](assetId:///2feb0fe2-0805-4cc9-8cba-b0315849dfb7) and [/reference (Import Metadata) (C# Compiler Options)](../vs140/-reference--C#-Compiler-Options-.md).  
  
 The following sequence of compilations will result in CS0012:  
  
```  
// cs0012a.cs  
// compile with: /target:library  
public class A {}  
```  
  
 Then:  
  
```  
// cs0012b.cs  
// compile with: /target:library /reference:cs0012a.dll  
public class B  
{  
   public static A f()  
   {  
      return new A();  
   }  
}  
```  
  
 Then:  
  
```  
// cs0012c.cs  
// compile with: /reference:cs0012b.dll  
class C  
{  
   public static void Main()  
   {  
      object o = B.f();   // CS0012  
   }  
}  
```  
  
 You could resolve this CS0012 by compiling with `/reference:cs0012b.dll;cs0012a.dll`, or in Visual Studio by using the [Add Reference Dialog Box](assetId:///2feb0fe2-0805-4cc9-8cba-b0315849dfb7) to add a reference to cs0012a.dll in addition to cs0012b.dll.
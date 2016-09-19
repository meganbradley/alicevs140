---
title: "Compiler Warning (level 1) CS0657"
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
ms.topic: article
ms.assetid: d12d2efc-f44e-40e6-b825-5a66ead0c08e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS0657
'attribute modifier' is not a valid attribute location for this declaration. Valid attribute locations for this declaration are 'locations'. All attributes in this block will be ignored.  
  
 The compiler found an attribute modifier in an invalid location. See [Attribute Targets](assetId:///59a261f0-1cfb-4aa5-b610-6b735389882c) for more information.  
  
 The following sample generates CS0657:  
  
```  
// CS0657.cs  
// compile with: /target:library  
public class TestAttribute : System.Attribute {}  
[return: Test]   // CS0657 return not valid on a class  
class Class1 {}  
```
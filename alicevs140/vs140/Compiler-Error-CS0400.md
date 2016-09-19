---
title: "Compiler Error CS0400"
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
ms.assetid: 58f91f3b-30f4-433b-9a13-0cff258a2630
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0400
The type or namespace name 'identifier' could not be found in the global namespace (are you missing an assembly reference?)  
  
 The identifier scoped with the global scope operator (`::`) was not found in the global namespace. You may be missing an assembly reference that contains the identifier, or the identifier may be declared in a class or namespace other than the global namespace. This error could also occur if a globally scoped identifier is not declared or is misspelled.  
  
 To avoid this error, locate the declaration of the identifier, verify the correct spelling, and if the declaration is in a separate assembly, make sure that you have the appropriate assembly reference. If the identifier is declared inside another type or namespace, use the fully-qualified name after the ::. The following sample generates CS0400:  
  
```  
// CS0400.cs  
class C  
{  
    public static void Main()  
    {  
        // CS0400 - D could not be found   
        // in the global namespace.  
        global::D d = new global::D();  
   }  
}  
```
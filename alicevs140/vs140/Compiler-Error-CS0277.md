---
title: "Compiler Error CS0277"
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
ms.assetid: 8abec3eb-4d4c-4aab-87cc-d0444ab23535
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0277
'class' does not implement interface member 'accessor'. 'class accessor' is not public  
  
 This error occurs when you try to implement a property of an interface, but the implementation of the property accessor in the class is not public. Methods that implement interface members need to have public accessibility. To resolve, remove the access modifier on the property accessor.  
  
## Example  
 The following example generates CS0277:  
  
```  
// CS0277.cs  
public interface MyInterface  
{  
    int Property  
    {  
        get;  
        set;  
    }  
}  
  
public class MyClass : MyInterface   // CS0277  
{  
    public int Property  
    {  
        get { return 0; }  
        // Try this instead:  
        //set { }  
        protected set { }  
    }  
}  
```
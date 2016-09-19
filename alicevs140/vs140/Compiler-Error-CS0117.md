---
title: "Compiler Error CS0117"
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
ms.assetid: 2cbc7e66-75d6-4817-85ae-89c4b9adfded
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0117
'type' does not contain a definition for 'identifier'  
  
-   This error occurs in some situations when a reference is made to a member that does not exist for the data type.  
  
## Example  
 The following sample generates CS0117:  
  
```  
// CS0117.cs  
public class BaseClass { }  
  
    public class base021 : BaseClass  
    {  
        public void TestInt()  
        {  
            int i = base.someMember; //CS0117  
        }  
        public static int Main()  
        {  
            return 1;  
        }  
    }  
```
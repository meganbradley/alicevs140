---
title: "Compiler Error CS0524"
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
ms.assetid: a5cd8fb0-f5df-4580-9116-a6be4dffd1cb
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0524
'type' : interfaces cannot declare types  
  
 An [interface](../vs140/interface--C#-Reference-.md) cannot contain a user-defined type; it should contain only methods and properties.  
  
## Example  
 The following sample generates CS0524:  
  
```  
// CS0524.cs  
public interface Clx  
{  
    public class Cly   // CS0524, delete user-defined type  
    {  
    }  
}  
  
```
---
title: "How to: Use Indexed Properties in COM Interop Programming (C# Programming Guide)"
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
ms.assetid: 756bfc1e-7c28-4d4d-b114-ac9288c73882
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use Indexed Properties in COM Interop Programming (C# Programming Guide)
*Indexed properties* improve the way in which COM properties that have parameters are consumed in C# programming. Indexed properties work together with other features introduced in Visual C# 2010, such as [named and optional arguments](../Topic/Named%20and%20Optional%20Arguments%20\(C%23%20Programming%20Guide\).md), a new type ([dynamic](../vs140/dynamic--C#-Reference-.md)), and [embedded type information](../vs140/Walkthrough--Embedding-Types-from-Managed-Assemblies--C#-and-Visual-Basic-.md), to enhance Microsoft Office programming.  
  
 In earlier versions of C#, methods are accessible as properties only if the `get` method has no parameters and the `set` method has one and only one value parameter. However, not all COM properties meet those restrictions. For example, the Excel [Range](http://go.microsoft.com/fwlink/?LinkId=166053) property has a `get` accessor that requires a parameter for the name of the range. In the past, because you could not access the `Range` property directly, you had to use the `get_Range` method instead, as shown in the following example.  
  
 [!CODE [csProgGuideIndexedProperties#1](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideindexedproperties#1)]  
  
 Indexed properties enable you to write the following instead:  
  
 [!CODE [csProgGuideIndexedProperties#2](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideindexedproperties#2)]  
  
> [!NOTE]
>  The previous example also uses the [optional arguments](../Topic/Named%20and%20Optional%20Arguments%20\(C%23%20Programming%20Guide\).md) feature, introduced in Visual C# 2010, which enables you to omit `Type.Missing`.  
  
 Similarly, to set the value of the `Value` property of a [Range](http://go.microsoft.com/fwlink/?LinkId=179211) object in Visual C# 2008 and earlier, two arguments are required. One supplies an argument for an optional parameter that specifies the type of the range value. The other supplies the value for the `Value` property. Before Visual C# 2010, C# allowed only one argument. Therefore, instead of using a regular set method, you had to either use the `set_Value` method or a different property, [Value2](http://go.microsoft.com/fwlink/?LinkId=166050). The following examples illustrate these techniques. Both set the value of the A1 cell to `Name`.  
  
 [!CODE [csProgGuideIndexedProperties#3](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideindexedproperties#3)]  
  
 Indexed properties enable you to write the following code instead.  
  
 [!CODE [csProgGuideIndexedProperties#4](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideindexedproperties#4)]  
  
 You cannot create indexed properties of your own. The feature only supports consumption of existing indexed properties.  
  
## Example  
 The following code shows a complete example. For more information about how to set up a project that accesses the Office API, see [How to: Access Office Interop Objects by Using Visual C# 2010 Features](../Topic/How%20to:%20Access%20Office%20Interop%20Objects%20by%20Using%20Visual%20C%23%20Features%20\(C%23%20Programming%20Guide\).md).  
  
 [!CODE [csProgGuideIndexedProperties#5](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideindexedproperties#5)]  
  
## See Also  
 [Named and Optional Arguments](../Topic/Named%20and%20Optional%20Arguments%20\(C%23%20Programming%20Guide\).md)   
 [dynamic (C# Reference)](../vs140/dynamic--C#-Reference-.md)   
 [Using Type dynamic](../vs140/Using-Type-dynamic--C#-Programming-Guide-.md)   
 [How to: Use Named and Optional Arguments in Office Programming](../vs140/How-to--Use-Named-and-Optional-Arguments-in-Office-Programming--C#-Programming-Guide-.md)   
 [How to: Access Office Interop Objects by Using Visual C# 2010 Features](../Topic/How%20to:%20Access%20Office%20Interop%20Objects%20by%20Using%20Visual%20C%23%20Features%20\(C%23%20Programming%20Guide\).md)   
 [Walkthrough: Office Programming](../vs140/Walkthrough--Office-Programming--C#-and-Visual-Basic-.md)
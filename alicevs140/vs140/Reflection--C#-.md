---
title: "Reflection (C#)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f80a2362-953b-4e8e-9759-cd5f334190d4
caps.latest.revision: 5
---
# Reflection (C#)
Reflection provides objects (of type <xref:System.Type?qualifyHint=False>) that describe assemblies, modules and types. You can use reflection to dynamically create an instance of a type, bind the type to an existing object, or get the type from an existing object and invoke its methods or access its fields and properties. If you are using attributes in your code, reflection enables you to access them. For more information, see [Extending Metadata Using Attributes](assetId:///30386922-1e00-4602-9ebf-526b271a8b87).  
  
 Here's a simple example of reflection using the static method `GetType` - inherited by all types from the `Object` base class - to obtain the type of a variable:  
  
```c#  
// Using GetType to obtain type information:  
int i = 42;  
System.Type type = i.GetType();  
System.Console.WriteLine(type);  
```  
  
 The output is:  
  
 `System.Int32`  
  
 The following example uses reflection to obtain the full name of the loaded assembly.  
  
```c#  
// Using Reflection to get information from an Assembly:  
System.Reflection.Assembly info = typeof(System.Int32).Assembly;  
System.Console.WriteLine(info);  
```  
  
 The output is:  
  
 `mscorlib, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089`  
  
> [!NOTE]
>  The C# keywords `protected` and `internal` have no meaning in IL and are not used in the reflection APIs. The corresponding terms in IL are *Family* and *Assembly*. To identify an `internal` method using reflection, use the <xref:System.Reflection.MethodBase.IsAssembly?qualifyHint=False> property. To identify a `protected internal` method, use the <xref:System.Reflection.MethodBase.IsFamilyOrAssembly?qualifyHint=False>.  
  
## Reflection Overview  
 Reflection is useful in the following situations:  
  
-   When you have to access attributes in your program's metadata. For more information, see [Retrieving Information Stored in Attributes](assetId:///37dfe4e3-7da0-48b6-a3d9-398981524e1c).  
  
-   For examining and instantiating types in an assembly.  
  
-   For building new types at runtime. Use classes in <xref:System.Reflection.Emit?qualifyHint=False>.  
  
-   For performing late binding, accessing methods on types created at run time. See the topic [Dynamically Loading and Using Types](assetId:///db985bec-5942-40ec-b13a-771ae98623dc).  
  
## Related Sections  
 For more information:  
  
-   [Reflection Overview](assetId:///d1a58e7f-fb39-4d50-bf84-e3b8f9bf9775)  
  
-   [Viewing Type Information](assetId:///7e7303a9-4064-4738-b4e7-b75974ed70d2)  
  
-   [Reflection and Generic Types](assetId:///f7180fc5-dd41-42d4-8a8e-1b34288e06de)  
  
-   <xref:System.Reflection.Emit?qualifyHint=False>  
  
-   [Retrieving Information Stored in Attributes](assetId:///37dfe4e3-7da0-48b6-a3d9-398981524e1c)  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Assemblies in the Common Language Runtime](assetId:///2cfebe19-7436-49f1-bd99-3c4019f0b676)
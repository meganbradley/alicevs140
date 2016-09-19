---
title: "Compiler Error CS0669"
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
ms.assetid: c7f81869-79d7-481f-a026-2cef0e87df4c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0669
A class with the ComImport attribute cannot have a user-defined constructor  
  
 The COM interop layer in the common language runtime supplies the constructor for [ComImport](frlrfSystemRuntimeInteropServicesComImportAttributeClassTopic) classes. Consequently, a COM object can be used as a managed object in the runtime.  
  
 The following sample generates CS0669:  
  
```  
// CS0669.cs  
using System.Runtime.InteropServices;  
[ComImport, Guid("00000000-0000-0000-0000-000000000001")]  
class TestClass  
{  
   TestClass()   // CS0669, delete constructor to resolve  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
```
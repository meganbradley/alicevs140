---
title: "Compiler Warning (level 1) CS1058"
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
ms.topic: error-reference
ms.assetid: ed50590c-f130-47c3-976d-322a6c8f996d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1058
A previous catch clause already catches all exceptions. All exceptions thrown will be wrapped in a System.Runtime.CompilerServices.RuntimeWrappedException  
  
 This attribute causes CS1058 if a `catch()` block has no specified exception type after a `catch (System.Exception e)` block. The warning advises that the `catch()` block will not catch any exceptions.  
  
 A `catch()` block after a `catch (System.Exception e)` block can catch non-CLS exceptions if the `RuntimeCompatibilityAttribute` is set to false in the AssemblyInfo.cs file: `[assembly: RuntimeCompatibilityAttribute(WrapNonExceptionThrows = false)]`. If this attribute is not set explicitly to false, all thrown non-CLS exceptions are wrapped as Exceptions and the `catch (System.Exception e)` block catches them. For more information, see [How To: Catch a non-CLS Exception](../Topic/How%20to:%20Catch%20a%20non-CLS%20Exception.md).  
  
## Example  
 The following example generates CS1058.  
  
```  
// CS1058.cs  
// CS1058 expected  
using System.Runtime.CompilerServices;  
  
// the following attribute is set to true by default in the C# compiler  
// set to false in your source code to resolve CS1058  
[assembly: RuntimeCompatibilityAttribute(WrapNonExceptionThrows = true)]  
  
class TestClass   
{  
   static void Main()   
   {  
      try {}  
  
      catch (System.Exception e) {   
         System. Console.WriteLine("Caught exception {0}", e);  
      }  
  
      catch {}   // CS1058. This line will never be reached.  
   }  
}  
```
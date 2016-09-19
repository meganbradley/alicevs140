---
title: "CA2221: Finalizers should be protected"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bda03aee-4cce-45d3-907d-17f4ee030acc
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2221: Finalizers should be protected
|||  
|-|-|  
|TypeName|FinalizersShouldBeProtected|  
|CheckId|CA2221|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A public type implements a finalizer that does not specify family (protected) access.  
  
## Rule Description  
 Finalizers must use the family access modifier. This rule is enforced by the C#, Visual Basic, and Visual C++ compilers.  
  
## How to Fix Violations  
 To fix a violation of this rule, change the finalizer to be family-accessible.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 This rule cannot be violated in any high-level .NET language; it can be violated if you are writing Microsoft Intermediate Language.  
  
```  
// =============== CLASS MEMBERS DECLARATION ===================  
//   note that class flags, 'extends' and 'implements' clauses  
//          are provided here for information only  
  
.namespace UsageLibrary  
{  
  .class public auto ansi beforefieldinit FinalizeMethodNotProtected  
         extends [mscorlib]System.Object  
  {  
    .method public hidebysig instance void  
            Finalize() cil managed  
    {  
  
      // Code size       1 (0x1)  
      .maxstack  0  
      IL_0000:  ret  
    } // end of method FinalizeMethodNotProtected::Finalize  
  
    .method public hidebysig specialname rtspecialname  
            instance void  .ctor() cil managed  
    {  
      // Code size       7 (0x7)  
      .maxstack  1  
      IL_0000:  ldarg.0  
      IL_0001:  call       instance void [mscorlib]System.Object::.ctor()  
      IL_0006:  ret  
    } // end of method FinalizeMethodNotProtected::.ctor  
  
  } // end of class FinalizeMethodNotProtected  
} // end of namespace  
```  
  
## See Also  
 [Implementing Finalize and Dispose](assetId:///31a6c13b-d6a2-492b-9a9f-e5238c983bcb)
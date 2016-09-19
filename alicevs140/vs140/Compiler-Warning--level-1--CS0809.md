---
title: "Compiler Warning (level 1) CS0809"
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
ms.assetid: 2c2f0248-ab3a-4cdc-a1b0-2f0e05eac4c9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS0809
Obsolete member 'memberA' overrides non-obsolete member 'memberB'.  
  
 Typically, a member that is marked as obsolete should not override a member that is not marked as obsolete. This warning is generated in [!INCLUDE[vs_orcas_long](../vs140/includes/vs_orcas_long_md.md)] but not in [!INCLUDE[vsprvslong](../vs140/includes/vsprvslong_md.md)].  
  
### To correct this error  
  
1.  Remove the `Obsolete` attribute from the overriding member, or add it to the base class member.  
  
## Example  
  
```  
// CS0809.cs  
public class Base  
{  
    public virtual void Test1()  
    {  
    }  
}  
public class C : Base  
{  
    [System.Obsolete()]  
    public override void Test1() // CS0809  
    {  
    }  
}  
```
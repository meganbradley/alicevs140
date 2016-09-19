---
title: "Underlying type &lt;typename&gt; of Enum is not CLS-compliant"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 32bf1949-fd73-456c-a323-bf1ffe1320ed
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Underlying type &lt;typename&gt; of Enum is not CLS-compliant
The data type specified for this enumeration is not part of the [Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6) (CLS). This is not an error within your component, because the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] and [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] support this data type. However, another component written in strictly CLS-compliant code might not support this data type. Such a component might not be able to interact successfully with your component.  
  
 The following [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] data types are not CLS-compliant:  
  
-   [SByte Data Type (Visual Basic)](../Topic/SByte%20Data%20Type%20\(Visual%20Basic\).md)  
  
-   [UInteger Data Type](../vs140/UInteger-Data-Type.md)  
  
-   [ULong Data Type (Visual Basic)](../vs140/ULong-Data-Type--Visual-Basic-.md)  
  
-   [UShort Data Type (Visual Basic)](../Topic/UShort%20Data%20Type%20\(Visual%20Basic\).md)  
  
 By default, this message is a warning. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40032  
  
### To correct this error  
  
-   If your component interfaces only with other [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] components, or does not interface with any other components, you do not need to change anything.  
  
-   If you are interfacing with a component not written for the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)], you might be able to determine, either through reflection or from documentation, whether it supports this data type. If it does, you do not need to change anything.  
  
-   If you are interfacing with a component that does not support this data type, you must replace it with the closest CLS-compliant type. For example, in place of `UInteger` you might be able to use `Integer` if you do not need the value range above 2,147,483,647. If you do need the extended range, you can replace `UInteger` with `Long`.  
  
-   If you are interfacing with Automation or COM objects, keep in mind that some types have different data widths than in the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)]. For example, `uint` is often 16 bits in other environments. If you are passing a 16-bit argument to such a component, declare it as `UShort` instead of `UInteger` in your managed [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] code.  
  
## See Also  
 [Reflection (C# and Visual Basic)](../vs140/Reflection--C#-and-Visual-Basic-.md)   
 [Reflection Overview](assetId:///d1a58e7f-fb39-4d50-bf84-e3b8f9bf9775)   
 [<PAVE OVER\> Writing CLS-Compliant Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3)
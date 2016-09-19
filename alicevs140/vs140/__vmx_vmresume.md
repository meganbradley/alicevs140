---
title: "__vmx_vmresume"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 233fe1b6-c727-493a-a484-1b2363732281
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __vmx_vmresume
**Microsoft Specific**  
  
 Resumes VMX non-root operation by using the current virtual machine control structure (VMCS).  
  
## Syntax  
  
```  
unsigned char __vmx_vmresume(  
   void);  
```  
  
## Return Value  
  
|Value|Meaning|  
|-----------|-------------|  
|0|The operation succeeded.|  
|1|The operation failed with extended status available in the `VM-instruction error field` of the current VMCS.|  
|2|The operation failed without status available.|  
  
## Remarks  
 An application can perform a VM-enter operation by using either the [__vmx_vmlaunch](../vs140/__vmx_vmlaunch.md) or `__vmx_vmresume` function. The `__vmx_vmlaunch` function can be used only with a VMCS whose launch state is `Clear`, and the `__vmx_vmresume` function can be used only with a VMCS whose launch state is `Launched`. Consequently, use the [__vmx_vmclear](../vs140/__vmx_vmclear.md) function to set the launch state of a VMCS to `Clear`, and then use the `__vmx_vmlaunch` function for your first VM-enter operation and the `__vmx_vmresume` function for subsequent VM-enter operations.  
  
 The `__vmx_vmresume` function is equivalent to the `VMRESUME` machine instruction. This function supports the interaction of a host's virtual machine monitor with a guest operating system and its applications. For more information, search for the PDF document, "Intel Virtualization Technical Specification for the IA-32 Intel Architecture," document number C97063-002, at the [Intel Corporation](http://go.microsoft.com/fwlink/?LinkId=127) site.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__vmx_vmresume`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [__vmx_vmlaunch](../vs140/__vmx_vmlaunch.md)   
 [__vmx_vmclear](../vs140/__vmx_vmclear.md)
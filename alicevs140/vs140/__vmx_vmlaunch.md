---
title: "__vmx_vmlaunch"
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
ms.assetid: 708f7c38-b7c1-4ee7-bfc4-0daeb9cc9360
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __vmx_vmlaunch
**Microsoft Specific**  
  
 Places the calling application in VMX non-root operation state (VM enter) by using the current virtual-machine control structure (VMCS).  
  
## Syntax  
  
```  
unsigned char __vmx_vmlaunch(  
   void);  
```  
  
## Return Value  
  
|Value|Meaning|  
|-----------|-------------|  
|0|The operation succeeded.|  
|1|The operation failed with extended status available in the `VM-instruction error field` of the current VMCS.|  
|2|The operation failed without status available.|  
  
## Remarks  
 An application can perform a VM-enter operation by using either the [__vmx_vmlaunch](../vs140/__vmx_vmlaunch.md) or [__vmx_vmresume](../vs140/__vmx_vmresume.md) function. The [__vmx_vmlaunch](../vs140/__vmx_vmlaunch.md) function can be used only with a VMCS whose launch state is `Clear`, and the [__vmx_vmresume](../vs140/__vmx_vmresume.md) function can be used only with a VMCS whose launch state is `Launched`. Consequently, use the [__vmx_vmclear](../vs140/__vmx_vmclear.md) function to set the launch state of a VMCS to `Clear`, and then use the [__vmx_vmlaunch](../vs140/__vmx_vmlaunch.md) function for your first VM-enter operation and the [__vmx_vmresume](../vs140/__vmx_vmresume.md) function for subsequent VM-enter operations.  
  
 The `__vmx_vmlaunch` function is equivalent to the `VMLAUNCH` machine instruction. This function supports the interaction of a host's virtual machine monitor with a guest operating system and its applications. For more information, search for the document, "Intel Virtualization Technical Specification for the IA-32 Intel Architecture," document number C97063-002, at the [Intel Corporation](http://go.microsoft.com/fwlink/?LinkId=127) site.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__vmx_vmlaunch`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [__vmx_vmresume](../vs140/__vmx_vmresume.md)   
 [__vmx_vmclear](../vs140/__vmx_vmclear.md)
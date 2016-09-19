---
title: "__svm_vmrun"
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
ms.assetid: ae98a781-fc17-47b2-b40f-86fcebf1867b
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __svm_vmrun
**Microsoft Specific**  
  
 Starts execution of the virtual machine guest code that corresponds to the specified virtual machine control block (VMCB).  
  
## Syntax  
  
```  
void __svm_vmrun(  
   size_t VmcbPhysicalAddress  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `VmcbPhysicalAddress`|The physical address of the VMCB.|  
  
## Remarks  
 The `__svm_vmrun` function uses a minimal amount of information in the VMCB to begin executing the virtual machine guest code. Use the [__svm_vmsave](../vs140/__svm_vmsave.md) or [__svm_vmload](../vs140/__svm_vmload.md) function if you require more information to handle a complex interrupt or to switch to another guest.  
  
 The `__svm_vmrun` function is equivalent to the `VMRUN` machine instruction. This function supports the interaction of a host's virtual machine monitor with a guest operating system and its applications. For more information, search for the document, "AMD64 Architecture Programmer's Manual Volume 2: System Programming," document number 24593, revision 3.11 or later, at the [AMD corporation](http://go.microsoft.com/fwlink/?LinkId=23746) site.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__svm_vmrun`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [__svm_vmsave](../vs140/__svm_vmsave.md)   
 [__svm_vmload](../vs140/__svm_vmload.md)
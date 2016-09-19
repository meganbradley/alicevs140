---
title: "IWorkerThreadClient Interface"
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
ms.topic: reference
ms.assetid: 56f4a2f5-007e-4a33-9e20-05187629f715
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IWorkerThreadClient Interface
`IWorkerThreadClient` is the interface implemented by clients of the [CWorkerThread](../vs140/CWorkerThread-Class.md) class.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
__interface IWorkerThreadClient  
  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[CloseHandle](../vs140/IWorkerThreadClient--CloseHandle.md)|Implement this method to close the handle associated with this object.|  
|[Execute](../vs140/IWorkerThreadClient--Execute.md)|Implement this method to execute code when the handle associated with this object becomes signaled.|  
  
## Remarks  
 Implement this interface when you have code that needs to execute on a worker thread in response to a handle becoming signaled.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Classes](../vs140/ATL-Classes.md)   
 [CWorkerThread Class](../vs140/CWorkerThread-Class.md)
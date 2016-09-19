---
title: "IDebugObject2::IsEncOutdated"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d3a8c02d-895b-478c-9957-d663130f308e
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugObject2::IsEncOutdated
This method determines whether the Edit and Continue status of this object or of the parent container is out of date. A custom expression evaluator does not implement this method and always returns `E_NOTIMPL`.  
  
## Syntax  
  
```cpp  
HRESULT IsEncOutdated(  
   BOOL* pfEncOutdated  
);  
```  
  
```c#  
int IsEncOutdated(  
   out int pfEncOutdated  
);  
```  
  
#### Parameters  
 `pfEncOutdated`  
 [out] Nonzero (`TRUE`) if the Edit and Continue state is out of date, zero (`FALSE`) if it is not.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
> [!NOTE]
>  A custom expression evaluator should always return `E_NOTIMPL`.  
  
## See Also  
 [IDebugObject2](../vs140/IDebugObject2.md)
---
title: "SccUninitialize Function"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 17cf5337-d251-4422-bc96-93fe7d48f2ae
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# SccUninitialize Function
This function cleans up any allocations or open connections created by a previous call to the [SccInitialize Function](../vs140/SccInitialize-Function.md) in preparation for shutting down the source control plug-in.  
  
## Syntax  
  
```cpp#  
SCCRTN SccUninitialize (  
   LPVOID pvContext  
);  
```  
  
#### Parameters  
 pvContext  
 [in] The pointer to the source control plug-in context structure created in the [SccInitialize Function](../vs140/SccInitialize-Function.md).  
  
## Return Value  
 The source control plug-in implementation of this function is expected to return one of the following values:  
  
|Value|Description|  
|-----------|-----------------|  
|SCC_OK|The clean-up completed successfully.|  
  
## Remarks  
 The source control plug-in is responsible for preparing to be shut down and for freeing memory that the plug-in has allocated for the context structure. The function is called once for each given instance of a plug-in. A call to the [SccInitialize Function](../vs140/SccInitialize-Function.md) precedes this call. No projects can still be open at the time of the call to `SccUninitialize`.  
  
## See Also  
 [Source Control Plug-in API Functions](../vs140/Source-Control-Plug-in-API-Functions.md)   
 [SccInitialize Function](../vs140/SccInitialize-Function.md)
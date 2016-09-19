---
title: "IEEVisualizerService::GetCustomViewerList"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 249d26ca-914f-43af-a400-8162477223f4
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEEVisualizerService::GetCustomViewerList
This method returns a list of type visualizers that this service knows about.  
  
## Syntax  
  
```cpp  
HRESULT GetCustomViewerList(  
   ULONG                celtSkip,  
   ULONG                celtRequested,  
   DEBUG_CUSTOM_VIEWER* rgViewers,  
   ULONG*               pceltFetched  
);  
```  
  
```c#  
int GetCustomViewerList(  
   uint                  celtSkip,  
   uint                  celtRequested,  
   DEBUG_CUSTOM_VIEWER[] rgViewers,  
   out uint              pceltFetched  
);  
```  
  
#### Parameters  
 `celtSkip`  
 [in] Number of visualizers to skip over.  
  
 `celRequested`  
 [in] Number of visualizers to retrieve (also specifies size of the `rgViewers` array).  
  
 `rgViewers`  
 [in, out] Array of [DEBUG_CUSTOM_VIEWER](../vs140/DEBUG_CUSTOM_VIEWER.md) structures to be filled in.  
  
 `pceltFetched`  
 [out] Number of visualizers actually retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 [IDebugProperty3::GetCustomViewerList](../vs140/IDebugProperty3--GetCustomViewerList.md) passes the request to this method as part of its support for type visualizers. If the expression evaluator also supplies custom viewers for the same type, it can append appropriately filled-out [DEBUG_CUSTOM_VIEWER](../vs140/DEBUG_CUSTOM_VIEWER.md) structures for those custom viewers to the list. Make sure that [IDebugProperty3::GetCustomViewerCount](../vs140/IDebugProperty3--GetCustomViewerCount.md) reflects those additional viewers.  
  
 See [Type Visualizer and Custom Viewer](../vs140/Type-Visualizer-and-Custom-Viewer.md) for details on the differences between visualizers and viewers.  
  
## See Also  
 [IEEVisualizerService](../vs140/IEEVisualizerService.md)   
 [DEBUG_CUSTOM_VIEWER](../vs140/DEBUG_CUSTOM_VIEWER.md)   
 [IDebugProperty3::GetCustomViewerList](../vs140/IDebugProperty3--GetCustomViewerList.md)   
 [IDebugProperty3::GetCustomViewerCount](../vs140/IDebugProperty3--GetCustomViewerCount.md)   
 [Type Visualizer and Custom Viewer](../vs140/Type-Visualizer-and-Custom-Viewer.md)
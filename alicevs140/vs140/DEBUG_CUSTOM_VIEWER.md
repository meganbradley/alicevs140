---
title: "DEBUG_CUSTOM_VIEWER"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8e0ef3f0-0107-48e8-a037-6e52b4c4ed9d
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# DEBUG_CUSTOM_VIEWER
A structure that identifies a custom viewer or type visualizer.  
  
## Syntax  
  
```cpp  
typedef struct tagDEBUG_CUSTOM_VIEWER {  
   DWORD dwID;  
   BSTR  bstrMenuName;  
   BSTR  bstrDescription;  
   GUID  guidLang;  
   GUID  guidVendor;  
   BSTR  bstrMetric;  
} DEBUG_CUSTOM_VIEWER;  
```  
  
```c#  
public struct DEBUG_CUSTOM_VIEWER {  
   public uint   dwID;  
   public string bstrMenuName;  
   public string bstrDescription;  
   public Guid   guidLang;  
   public Guid   guidVendor;  
   public string bstrMetric;  
};  
```  
  
## Members  
 dwID  
 An ID to differentiate multiple viewers or visualizers implemented by one `GUID`.  
  
 bstrMenuName  
 The text that will appear in the drop-down menu.  
  
 bstrDescription  
 A description of the custom viewer or type visualizer (must be a null value if not used).  
  
 guidLang  
 Language of the providing expression evaluator.  
  
 guidVendor  
 Vendor of the providing expression evaluator.  
  
 bstrMetric  
 Metric under which the custom viewer or type visualizer `CLSID` is stored.  
  
## Remarks  
 A list of this structure is returned by a call to the [IDebugProperty3::GetCustomViewerList](../vs140/IDebugProperty3--GetCustomViewerList.md) method (and, by extension, the [IEEVisualizerService::GetCustomViewerList](../vs140/IEEVisualizerService--GetCustomViewerList.md) method).  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [IDebugProperty3::GetCustomViewerList](../vs140/IDebugProperty3--GetCustomViewerList.md)   
 [IEEVisualizerService::GetCustomViewerList](../vs140/IEEVisualizerService--GetCustomViewerList.md)
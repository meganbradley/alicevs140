---
title: "IDebugCustomViewer::DisplayValue"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7a538248-5ced-450e-97cd-13fabe35fb1c
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCustomViewer::DisplayValue
This method is called to display the specified value.  
  
## Syntax  
  
```cpp#  
HRESULT DisplayValue(  
   HWND             hwnd,  
   DWORD            dwID,  
   IUnknown *       pHostServices,  
   IDebugProperty3* pDebugProperty);  
);  
```  
  
```c#  
int DisplayValue(  
   IntPtr          hwnd,   
   uint            dwID,   
   object          pHostServices,   
   IDebugProperty3 pDebugProperty  
);  
```  
  
#### Parameters  
 `hwnd`  
 [in] Parent window  
  
 `dwID`  
 [in] ID for custom viewers that support more than one type.  
  
 `pHostServices`  
 [in] Reserved. Always set to null.  
  
 `pDebugProperty`  
 [in] Interface that can be used to retrieve the value to be displayed.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns error code.  
  
## Remarks  
 The display is "modal" in that this method will create the necessary window, display the value, wait for input, and close the window, all before returning to the caller. This means the method must handle all aspects of displaying the property's value, from creating a window for output, to waiting for user input, to destroying the window.  
  
 To support changing the value on the given [IDebugProperty3](../vs140/IDebugProperty3.md) object, you can use the [IDebugProperty3::SetValueAsStringWithError](../vs140/IDebugProperty3--SetValueAsStringWithError.md) method —if the value can be expressed as a string. Otherwise, it is necessary to create a custom interface—exclusive to the expression evaluator implementing this `DisplayValue` method—on the same object that implements the `IDebugProperty3` interface. This custom interface would supply methods for changing the data of an arbitrary size or complexity.  
  
## See Also  
 [IDebugCustomViewer](../vs140/IDebugCustomViewer.md)   
 [IDebugProperty3](../vs140/IDebugProperty3.md)   
 [IDebugProperty3::SetValueAsStringWithError](../vs140/IDebugProperty3--SetValueAsStringWithError.md)
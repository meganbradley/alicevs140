---
title: "CDC::ResetDC"
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
ms.assetid: b54a395c-6e2d-4304-8253-1e954510cdcd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::ResetDC
Call this member function to update the device context wrapped by the `CDC` object.  
  
## Syntax  
  
```  
  
      BOOL ResetDC(  
   const DEVMODE* lpDevMode   
);  
```  
  
#### Parameters  
 *lpDevMode*  
 A pointer to a Windows `DEVMODE` structure.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The device context is updated from the information specified in the Windows `DEVMODE` structure. This member function only resets the attribute device context.  
  
 An application will typically use the `ResetDC` member function when a window processes a `WM_DEVMODECHANGE` message. You can also use this member function to change the paper orientation or paper bins while printing a document.  
  
 You cannot use this member function to change the driver name, device name, or output port. When the user changes the port connection or device name, you must delete the original device context and create a new device context with the new information.  
  
 Before you call this member function, you must ensure that all objects (other than stock objects) that had been selected into the device context have been selected out.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::m_hAttribDC](../vs140/CDC--m_hAttribDC.md)   
 [ResetDC](http://msdn.microsoft.com/library/windows/desktop/dd162925)   
 [WM_DEVMODECHANGE](http://msdn.microsoft.com/library/windows/desktop/dd145209)   
 [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565)
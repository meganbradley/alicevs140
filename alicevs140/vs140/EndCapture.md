---
title: "EndCapture"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 06084c3b-e065-49b6-968e-d578762fb871
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EndCapture
Ends a capture interval that was started with `BeginCapture`.  
  
## Syntax  
  
```cpp  
void EndCapture();  
```  
  
## Remarks  
 A capture interval typically spans a subset of one frame, such as when you want to capture graphics information only about a certain kind of draw call. If the capture interval spans a call to present, then two frames of graphics information are captured. The first frame spans the interval between the call to `BeginCapture` and the call to present; the second frame spans the interval between the first Direct3D event after the call to present and the call to `EndCapture`.  
  
 To capture an interval, you must prepare your app to capture and record graphics information—that is, you must have called [Init](../vs140/Init.md) through an instance of the `VsgDbg` class before you call `BeginCapture` or `EndCapture`.  
  
## See Also  
 [BeginCapture](../vs140/BeginCapture.md)   
 [CaptureCurrentFrame](../vs140/CaptureCurrentFrame.md)
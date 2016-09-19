---
title: "Changing the Drawing Code (ATL Tutorial, Part 4)"
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
ms.topic: get-started-article
ms.assetid: 08ff14e8-aa49-4139-a110-5d071939cf1e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Changing the Drawing Code (ATL Tutorial, Part 4)
By default, the control's drawing code displays a square and the text **PolyCtl**. In this step, you will change the code to display something more interesting. The following tasks are involved:  
  
-   Modifying the Header File  
  
-   Modifying the `OnDraw` Function  
  
-   Adding a Method to Calculate the Polygon Points  
  
-   Initializing the Fill Color  
  
## Modifying the Header File  
 Start by adding support for the math functions `sin` and `cos`, which will be used calculate the polygon points, and by creating an array to store positions.  
  
#### To modify the header file  
  
1.  Add the line `#include <math.h>` to the top of PolyCtl.h. The top of the file should look like this:  
  
     [!CODE [NVC_ATL_Windowing#47](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#47)]  
  
2.  Once the polygon points are calculated, they will be stored in an array of type `POINT`, so add the array after the definition of `m_nSides` in PolyCtl.h:  
  
     [!CODE [NVC_ATL_Windowing#48](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#48)]  
  
## Modifying the OnDraw Method  
 Now you should modify the `OnDraw` method in PolyCtl.h. The code you will add creates a new pen and brush with which to draw your polygon, and then calls the `Ellipse` and `Polygon` Win32 API functions to perform the actual drawing.  
  
#### To modify the OnDraw function  
  
1.  Replace the existing `OnDraw` method in PolyCtl.h with the following code:  
  
     [!CODE [NVC_ATL_Windowing#49](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#49)]  
  
## Adding a Method to Calculate the Polygon Points  
 Add a method, called `CalcPoints`, that will calculate the coordinates of the points that make up the perimeter of the polygon. These calculations will be based on the RECT variable that is passed into the function.  
  
#### To add the CalcPoints method  
  
1.  Add the declaration of `CalcPoints` to the `IPolyCtl` public section of the `CPolyCtl` class in PolyCtl.h:  
  
     [!CODE [NVC_ATL_Windowing#50](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#50)]  
  
     The last part of the public section of the `CPolyCtl` class will look like this:  
  
     [!CODE [NVC_ATL_Windowing#51](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#51)]  
  
2.  Add this implementation of the `CalcPoints` function to the end of PolyCtl.cpp:  
  
     [!CODE [NVC_ATL_Windowing#52](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#52)]  
  
## Initializing the Fill Color  
 Initialize `m_clrFillColor` with a default color.  
  
#### To initialize the fill color  
  
1.  Use green as the default color by adding this line to the `CPolyCtl` constructor in PolyCtl.h:  
  
     [!CODE [NVC_ATL_Windowing#53](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#53)]  
  
 The constructor now looks like this:  
  
 [!CODE [NVC_ATL_Windowing#54](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#54)]  
  
## Building and Testing the Control  
 Rebuild the control. Make sure the PolyCtl.htm file is closed if it is still open, and then click **Build Polygon** on the **Build** menu. You could view the control once again from the PolyCtl.htm page, but this time use the ActiveX Control Test Container.  
  
#### To use the ActiveX Control Test Container  
  
1.  Build and start the ActiveX Control Test Container. For more information, see [TSTCON Sample: ActiveX Control Test Container](../vs140/Visual-C---Samples.md).  
  
2.  In Test Container, on the **Edit** menu, click **Insert New Control**.  
  
3.  Locate your control, which will be called `PolyCtl Class`, and click **OK**. You will see a green triangle within a circle.  
  
 Try changing the number of sides by following the next procedure. To modify properties on a dual interface from within Test Container, use **Invoke Methods**.  
  
#### To modify a control's property from within the Test Container  
  
1.  In Test Container, click **Invoke Methods** on the **Control** menu.  
  
     The **Invoke Method** dialog box is displayed.  
  
2.  Select the **PropPut** version of the **Sides** property from the **Method Name** drop-down list box.  
  
3.  Type `5` in the **Parameter Value** box, click **Set Value**, and click **Invoke**.  
  
 Note that the control does not change. Although you changed the number of sides internally by setting the `m_nSides` variable, this did not cause the control to repaint. If you switch to another application and then switch back to Test Container, you will find that the control has repainted and has the correct number of sides.  
  
 To correct this problem, add a call to the `FireViewChange` function, defined in `IViewObjectExImpl`, after you set the number of sides. If the control is running in its own window, `FireViewChange` will call the `InvalidateRect` method directly. If the control is running windowless, the `InvalidateRect` method will be called on the container's site interface. This forces the control to repaint itself.  
  
#### To add a call to FireViewChange  
  
1.  Update PolyCtl.cpp by adding the call to `FireViewChange` to the `put_Sides` method. When you have finished, the `put_Sides` method should look like this:  
  
     [!CODE [NVC_ATL_Windowing#55](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#55)]  
  
 After adding `FireViewChange`, rebuild and try the control again in the ActiveX Control Test Container. This time when you change the number of sides and click `Invoke`, you should see the control change immediately.  
  
 In the next step, you will add an event.  
  
 [Back to Step 3](../vs140/Adding-a-Property-to-the-Control--ATL-Tutorial--Part-3-.md) &#124; [On to Step 5](../vs140/Adding-an-Event--ATL-Tutorial--Part-5-.md)  
  
## See Also  
 [Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md)   
 [Testing Properties and Events with Test Container](../vs140/Testing-Properties-and-Events-with-Test-Container.md)
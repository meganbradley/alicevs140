---
title: "Introduction to the Line and Shape Controls (Visual Studio)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5c4e8b1a-0733-4020-af6c-f582f4026728
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Introduction to the Line and Shape Controls (Visual Studio)
The Visual Basic Power Packs Line and Shape controls are a set of three graphical controls that enable you to draw lines and shapes on forms and containers. The <xref:Microsoft.VisualBasic.PowerPacks.LineShape?qualifyHint=False> control is used to draw horizontal, vertical, and diagonal lines. The <xref:Microsoft.VisualBasic.PowerPacks.OvalShape?qualifyHint=False> control is used to draw circles and ovals, and the <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape?qualifyHint=False> control is used to draw rectangles and squares.  
  
## Line and Shape Controls  
 Line and Shape controls encapsulate many of the graphics methods that are contained in the <xref:System.Drawing?qualifyHint=False> namespace. This enables you to draw lines and shapes in a single step without having to create graphics objects, pens, and brushes. Complex graphics techniques such as gradient fills can be accomplished by just setting some properties.  
  
 Although it is also possible to draw lines and shapes by using graphics methods, there are several advantages to using the Line and Shape controls:  
  
-   Graphics methods can be called only at run time. Line and Shape controls can be added to a form at design time. This enables you to see what they look like and to position them exactly; they can also be added at run time.  
  
-   Line and Shape controls are selectable at run time, providing events such as <xref:Microsoft.VisualBasic.PowerPacks.Shape.Click?qualifyHint=False> and <xref:Microsoft.VisualBasic.PowerPacks.Shape.OnDoubleClick?qualifyHint=False>. The outputs of graphics methods are not selectable and do not provide events.  
  
-   Line and Shape controls provide <xref:Microsoft.VisualBasic.PowerPacks.Shape.BringToFront?qualifyHint=False> and <xref:Microsoft.VisualBasic.PowerPacks.Shape.SendToBack?qualifyHint=False> methods that enable you to control their z-order at design time and at run time. The z-order of graphics methods can be controlled only by changing their order of execution at run time.  
  
-   Line and Shape controls are windowless controls; they have no window handles and therefore use less system resources.  
  
### Object Model  
 Line and Shape controls derive from a base <xref:Microsoft.VisualBasic.PowerPacks.Shape?qualifyHint=False> class that defines their shared properties, methods, and events.  
  
 The following illustration shows the Line and Shape object hierarchy.  
  
 ![A diagram of the Line and Shape object hierarchy](../vs140/media/LineShapeObject.png "LineShapeObject")  
Line and Shape object hierarchy  
  
 The derived <xref:Microsoft.VisualBasic.PowerPacks.LineShape?qualifyHint=False> class contains properties, methods, and events that are unique to lines. The derived <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape?qualifyHint=False> class is the base class for <xref:Microsoft.VisualBasic.PowerPacks.OvalShape?qualifyHint=False> and <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape?qualifyHint=False>; it contains properties, methods, and events common to all shapes. You can also derive from <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape?qualifyHint=False> to create your own `Shape` controls.  
  
 The <xref:Microsoft.VisualBasic.PowerPacks.OvalShape?qualifyHint=False> and <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape?qualifyHint=False> classes can be used to draw circles, ovals, rectangles, and rectangles with rounded corners.  
  
 When a Line or Shape control is added to a form or container, an invisible <xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer?qualifyHint=False> object is created. The <xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer?qualifyHint=False> acts as a canvas for the shapes within each container control; each <xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer?qualifyHint=False> has a corresponding <xref:Microsoft.VisualBasic.PowerPacks.ShapeCollection?qualifyHint=False> that enables you to iterate through the Line and Shape controls. You can move shapes from one container to another by using cut and paste or by dragging and dropping. When the last shape is removed from a container, the <xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer?qualifyHint=False> is removed also.  
  
> [!NOTE]
>  Not all container controls support the Line and Shape controls. You cannot host a Line or Shape control on a <xref:System.Windows.Forms.TableLayoutPanel?qualifyHint=False> or a <xref:System.Windows.Forms.FlowLayoutPanel?qualifyHint=False>.  
  
## See Also  
 <xref:Microsoft.VisualBasic.PowerPacks?qualifyHint=False>   
 [How to: Draw Lines with the LineShape Control (Visual Basic)](../Topic/How%20to:%20Draw%20Lines%20with%20the%20LineShape%20Control%20\(Visual%20Studio\).md)   
 [How to: Draw Shapes with the OvalShape and RectangleShape Controls (Visual Basic)](../Topic/How%20to:%20Draw%20Shapes%20with%20the%20OvalShape%20and%20RectangleShape%20Controls%20\(Visual%20Studio\).md)   
 [How to: Enable Tabbing Between Shapes (Visual Basic)](../vs140/How-to--Enable-Tabbing-Between-Shapes--Visual-Studio-.md)
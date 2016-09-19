---
title: "Creating a UI by using Blend for Visual Studio"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: efd12263-cc2d-4081-a2bb-9a2cc17c442c
caps.latest.revision: 33
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating a UI by using Blend for Visual Studio
Blend for Visual Studio helps you design XAML-based Windows desktop, web, [Windows Phone](http://msdn.microsoft.com/library/windowsphone/develop/jj683071.aspx), and [Windows Store](http://msdn.microsoft.com/library/windows/apps/jj129478.aspx) apps. It provides the same basic XAML design experience as Visual Studio and adds visual designers for advanced tasks such as animations and behaviors.  
  
 Since Blend for Visual Studio is included as a part of Visual Studio, you don't need to download it. However, you need to select it in the Visual Studio installer for it to install on your system.  
  
 If you’re new to Blend for Visual Studio, take a moment to become familiar with the unique features of the workspace. This topic takes you on a quick tour.  
  
> [!NOTE]
>  To tour the shared design features such as the artboard, Document Outline window, and Device window, see [Creating a UI by using XAML Designer](../vs140/Creating-a-UI-by-using-XAML-Designer-in-Visual-Studio.md).  
  
 **In this topic**:  
  
-   [Tour of the Tools panel](#Tools)  
  
-   [Tour of the Assets panel](#Assets)  
  
-   [Tour of the Objects and Timeline panel](#Objects)  
  
-   [Tour of the Properties panel](#Properties)  
  
##  <a name="Tools"></a> Tour of the Tools panel  
 You can use the **Tools** panel in Blend for Visual Studio to create and modify objects in your application. You create the objects by selecting a tool and drawing on the artboard with your mouse.  
  
 ![Tools panel](../vs140/media/Blend5Toolspanel.png "Blend5Toolspanel")  
  
|||||  
|-|-|-|-|  
|![](../vs140/media/B1_1.png "B1_1")|**Selection tools** Select objects and paths.<br /><br /> Use the **Direct Selection** tool to select nested objects and path segments.|![Callout A](../vs140/media/b5_label_A.png "b5_label_A")|**Gradient and brush tools**|  
|![](../vs140/media/B1_2.png "B1_2")|**View tools** Adjust the view of the artboard, such as for panning and zooming.|![Callout B](../vs140/media/b5_label_B.png "b5_label_B")|**Path tools**|  
|![](../vs140/media/B1_3.png "B1_3")|**Brush tools** Work with the visual attributes of an object, such as transforming a brush, painting an object, or selecting the attributes of one object to apply them to another object.|![Callout C](../vs140/media/b5_label_C.png "b5_label_C")|**Shape tools**|  
|![](../vs140/media/B1_4.png "B1_4")|**Object tools** Draw the most common objects on the artboard, such as paths, shapes, layout panels, text, and controls.|![Callout D](../vs140/media/b5_label_D.png "b5_label_D")|**Layout panels**|  
|![](../vs140/media/B1_5.png "B1_5")|**Asset tools** Access the **Assets** panel and to show the most recently used asset from the library.|![Callout E](../vs140/media/b5_label_E.png "b5_label_E")|**Text controls**|  
|||![Callout F](../vs140/media/b5_label_F.png "b5_label_F")|**Common controls**|  
  
 **Watch a short video:** ![Configure Installed Features](../vs140/media/BldAdminConsoleInitialConfigIcon.PNG "BldAdminConsoleInitialConfigIcon") [The Toolbar](https://www.youtube.com/watch?v=VkdUJcvoo54&list=PLBDF977B2F1DAB358&index=4).  
  
##  <a name="Assets"></a> Tour of the Assets panel  
 You can find all controls in the **Assets** panel, similar to the **Toolbox** in Visual Studio. In addition to controls, you’ll find everything you can add to your artboard in the **Assets** panel, including styles, media, behaviors, and effects.  
  
 ![Assets panel](../vs140/media/Blend5_Assets_panel.png "Blend5_Assets_panel")  
  
|||  
|-|-|  
|![](../vs140/media/B1_1.png "B1_1")|**Search box** Type in the **Search** box to filter the list of assets.|  
|![](../vs140/media/B1_2.png "B1_2")|**Grid mode and List mode** Switch between the **Grid mode** view and the **List mode** view of assets.|  
|![](../vs140/media/B1_3.png "B1_3")|**Assets categories** Click a category or subcategory to view the list of assets in that category.|  
|![](../vs140/media/B1_4.png "B1_4")|**Styles** Show all the styles that are contained in the resource dictionary.|  
|![](../vs140/media/B1_5.png "B1_5")|**Description** View a description of the selected assets category or subcategory.|  
  
##  <a name="Objects"></a> Tour of the Objects and Timeline panel  
 Use this panel to organize the objects on your artboard and, if you want, to animate them.  
  
 ![Object and Timeline panel in animation mode](../vs140/media/b5_object_timeline_animation.png "b5_object_timeline_animation")  
  
|||  
|-|-|  
|![](../vs140/media/B1_1.png "B1_1")|**Objects view** View a visual tree of a document. You can drill down to varying levels of detail. You can also add layers to further organize objects on the artboard. That way you can lock and hide them as a group.|  
|![](../vs140/media/B1_2.png "B1_2")|**Record mode indicator** See whether you’re recording property changes in a timeline.|  
|![](../vs140/media/B1_3.png "B1_3")|**Storyboard picker** View a list of storyboards that you’ve created.|  
|![](../vs140/media/B1_4.png "B1_4")|**Close storyboard** Close the current storyboard.|  
|![](../vs140/media/B1_5.png "B1_5")|**Storyboard options** Create, duplicate, reverse, delete, rename, or close a storyboard.|  
|![](../vs140/media/B1_6.png "B1_6")|**Playback controls** Navigate through the timeline. You can also drag the playhead to navigate through (or *scrub*) the timeline.|  
|![](../vs140/media/B1_7.png "B1_7")|**Return scope to** Scope the objects view back to the previous root object or previous scope. You can do this only when you’re modifying a style or template.|  
|![](../vs140/media/B1_8.png "B1_8")|**Record a keyframe** Record a snapshot of the properties of the selected object at the current point in time.|  
|![](../vs140/media/B1_9.png "B1_9")|**Snapping options** Set timeline snapping, snap resolution, and turn off timeline snapping.|  
|![](../vs140/media/97fa60b9-0caf-4387-9225-b57510d32209.png "97fa60b9-0caf-4387-9225-b57510d32209")|**Show/hide**, **Lock/unlock** Show or hide the visibility and locking options for the objects view.|  
|![](../vs140/media/B1_11.png "B1_11")|**Playhead position on the timeline** Show the current time in milliseconds. You can also enter a time value directly in this field to jump to a particular point in time. The precision depends on the snap resolution set in the **Snapping Options**.|  
|![](../vs140/media/B1_12.png "B1_12")|**Playhead** Determine what point in time the animation is at. You can drag the playhead across the timeline to preview animation.|  
|![](../vs140/media/B1_13.png "B1_13")|**Keyframes set on timelines** Change a property value at a specific point in time.|  
|![](../vs140/media/d839d12c-07a1-4127-a830-4a8e7069f4fe.png "d839d12c-07a1-4127-a830-4a8e7069f4fe")|**Change order of objects** Set the display order of objects. Click this button to arrange objects in the structure view by Z order (front-to-back) or by markup order (the order in which they appear in **XAML** view).|  
|![](../vs140/media/B1_15.png "B1_15")|**Timeline zoom** Set the zoom resolution of the timeline. Zooming in lets you edit an animation with more detail, and zooming out shows more of an overview of what is happening over longer periods of time. If you zoom in but can't set a keyframe at the position in time that you want, verify that the snap resolution is set high enough.|  
|![Callout 16](../vs140/media/b5_label_16.png "b5_label_16")|**Timeline composition area** View the timeline, and move keyframes around by dragging them or using their shortcut menus.|  
  
##  <a name="Properties"></a> Tour of the Properties panel  
 Use this panel to view and modify the properties of an object. You can also set them directly on the artboard. If you do, the property changes will be reflected in the **Properties** panel.  
  
 ![Properties panel](../vs140/media/Blend5_properties_panel.png "Blend5_properties_panel")  
  
 **Categories** Expand and collapse categories of properties. Click **Expand** ![](../vs140/media/6375953d-074c-421a-bbb3-6f5055b67b64.png "6375953d-074c-421a-bbb3-6f5055b67b64") and **Collapse** ![Collapse](../vs140/media/b5_collapse_button.png "b5_collapse_button") to show or hide category details.  
  
|||  
|-|-|  
|![](../vs140/media/B1_1.png "B1_1")|**Name and Type** View the icon, name and type of the selected object.|  
|![](../vs140/media/B1_2.png "B1_2")|**Arrange by** Arrange properties alphabetically by name, source, or category.|  
|![](../vs140/media/B1_3.png "B1_3")|**Brush properties** Set the visual properties for brushes such as Fill brush, Stroke brush, and Foreground brush.|  
|![](../vs140/media/B1_4.png "B1_4")|**Color editor** Use for solid color and gradient brushes.|  
|![](../vs140/media/B1_5.png "B1_5")|**Color picker** Select a color.|  
|![](../vs140/media/B1_6.png "B1_6")|**Color chips** View the initial color, current color, and last color|  
|![](../vs140/media/B1_7.png "B1_7")|**Eyedroppers** Use the color of any element on your screen. The **Color eyedropper** is available when the **Solid color brush** is selected. The **Gradient eyedropper** is available when the **Gradient brush** is selected.|  
|![](../vs140/media/B1_8.png "B1_8")|**Properties and Events** Set properties or choose events for a selected element.|  
|![](../vs140/media/B1_9.png "B1_9")|**Search box** Search for properties. Filter the properties that are displayed by typing in the **Search** box.||  
|![](../vs140/media/97fa60b9-0caf-4387-9225-b57510d32209.png "97fa60b9-0caf-4387-9225-b57510d32209")|**Brush editor tabs** Use to select a brush editor. You can choose **No brush**, **Solid Color brush**, **Gradient brush**, **Tile brush**, or **Brush resource**.|  
|![](../vs140/media/B1_11.png "B1_11")|**Color resources** Apply the exact same color to different properties. The **Color Resources** tab includes **Local Resources** and **System Resources**.|  
|![](../vs140/media/B1_12.png "B1_12")|**RGB color space** Modify the color by adjusting the values for the **R**,  **G**, or **B** (red, green, blue) number editors.|  
|![](../vs140/media/B1_13.png "B1_13")|**Alpha channel** Modify the Alpha value by using the number editor next to **A**.|  
|![](../vs140/media/d839d12c-07a1-4127-a830-4a8e7069f4fe.png "d839d12c-07a1-4127-a830-4a8e7069f4fe")|**Convert color to resource** Convert the selected color to a color resource. Color resources are available when you click the Color resources tab.|  
|![](../vs140/media/B1_15.png "B1_15")|**Hex value** View the hexadecimal value of the color displayed.|  
|![Callout 16](../vs140/media/b5_label_16.png "b5_label_16")|**Gradient slider** Appears only if a gradient brush is selected.|  
|![](../vs140/media/d50027a1-6824-4ad8-8b4e-558b0756dcf8.png "d50027a1-6824-4ad8-8b4e-558b0756dcf8")|**Show advanced properties** View categories of properties that are less commonly used.|  
  
 **Watch a short video:** ![Configure Installed Features](../vs140/media/BldAdminConsoleInitialConfigIcon.PNG "BldAdminConsoleInitialConfigIcon") [Properties panel](https://www.youtube.com/watch?v=HCqQfiobdag&list=PLBDF977B2F1DAB358&index=7).  
  
## See Also  
 [Insert controls and modify their behavior in Blend](../vs140/Insert-controls-and-modify-their-behavior-in-XAML-Designer.md)   
 [Animate objects in Blend](../vs140/Animate-objects-in-XAML-Designer.md)   
 [Draw shapes and paths in Blend](../vs140/Draw-shapes-and-paths.md)   
 [Designing XAML in Visual Studio](../vs140/Designing-XAML-in-Visual-Studio.md)
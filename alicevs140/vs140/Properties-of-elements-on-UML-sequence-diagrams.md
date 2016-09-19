---
title: "Properties of elements on UML sequence diagrams"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 475c10f3-a2d2-4a1e-b366-dc28997d437e
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Properties of elements on UML sequence diagrams
In a UML sequence diagram, each element on the diagram has properties. To see the properties of an element, right-click the element on the diagram or in **UML Model Explorer** and then click **Properties**. The properties appear in the **Properties** window.  
  
> [!NOTE]
>  This topic is about the properties of elements in UML sequence diagrams. For more information about how to read UML sequence diagrams, see [UML Sequence Diagrams: Overview](../vs140/UML-Sequence-Diagrams--Reference.md). For more information about how to draw UML sequence diagrams, see [UML Sequence Diagrams: Guidelines](../vs140/UML-Sequence-Diagrams--Guidelines.md).  
  
## Properties of Elements  
  
|Property|Default|Element|Description|  
|--------------|-------------|-------------|-----------------|  
|**Name**|A default name|All|Identifies the element.|  
|**Qualified Name**|Package :: Name|All|Identifies the element uniquely. Prefixed with the qualified name of the package that contains it.|  
|**Work Items**|0 associated|All|The number of work items associated with this element. To associate work items, see [How to: Link Work Items to Model Elements](../vs140/Link-model-elements-and-work-items.md).|  
|**Description**|(blank)|All|You can make general notes about the item here.|  
|**Color**|(default for element type)|Lifeline, Message|The color of the shape. This is a property of the shape, rather than the element it displays.|  
|**Type**|(blank)|Lifeline|The type of the instance that the lifeline represents.<br /><br /> If there is a reference symbol displayed in the header of the lifeline, then this class or interface exists separately in UML Model Explorer, and can be displayed on a class diagram.|  
|**Actor**|False|Lifeline|Indicates whether the lifeline represents a user, device or software component that is external to the component that the diagram is about.|  
|**Kind**|**Complete** - a message that has both sender and receiver.<br /><br /> **Found** - a message that has an unspecified sender.<br /><br /> **Lost** - a message that has an unspecified receiver.|Message|Indicates which ends of a message are attached to a lifeline.<br /><br /> You cannot change this property. It is set when you create the message.|  
|**Sort**|**AsynchCall** - an asynchronous message.<br /><br /> **SynchCall** - a synchronous message.<br /><br /> **Reply** - the return part of a synchronous message.<br /><br /> **CreateMessage** - an instance creation message.|Message|The type of message. You cannot change this property. It is determined by the tool that you use to create the message.|  
|**Operation**|(empty)|Message|A method called by the message in the receiving lifeline.<br /><br /> Visible only if the receiving lifeline is linked to an interface or a class.|  
|**Refers to**|A sequence diagram|Interaction Use|The sequence diagram called by this interaction use.|  
|**Interaction Operator**|Set when you used the **Surround With** command|Combined Fragment|The operator represented by this fragment or collection of fragments.|  
|**Guard**|(empty)|Interaction Operand in a Combined Fragment|The sequence in the fragment will not occur unless the guard is true.<br /><br /> To select the top fragment of any combined fragment, click underneath the fragment title.|  
|**Min, Max**|(no restriction)|Loop Combined Fragment|The minimum and maximum number of times the loop is executed.|  
|**Messages**|(empty)|Consider and<br /><br /> Ignore Combined Fragments|The messages that are considered or ignored in this fragment.|  
  
## See Also  
 [UML Sequence Diagrams: Overview](../vs140/UML-Sequence-Diagrams--Reference.md)   
 [UML Sequence Diagrams: Guidelines](../vs140/UML-Sequence-Diagrams--Guidelines.md)   
 [Alternative Flows: Combined Fragments in UML Sequence Diagrams](../vs140/Describe-control-flow-with-fragments-on-UML-sequence-diagrams.md)
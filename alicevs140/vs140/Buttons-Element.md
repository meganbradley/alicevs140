---
title: "Buttons Element"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9f2cf94d-dec5-4776-a836-9a89c75f0c87
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Buttons Element
Groups [Button](../vs140/Button-Element.md) elements, which represent individual commands.  
  
## Syntax  
  
```  
<Buttons>  
  <Button>... </Button>  
  <Button>... </Button>  
</Buttons>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|Condition|Optional. See [Conditional Attributes](../vs140/VSCT-XML-Schema-Conditional-Attributes.md).|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Buttons Element](../vs140/Buttons-Element.md)|Groups Button elements.|  
|[Button Element](../vs140/Button-Element.md)|Defines a command that the user can interact with.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Commands](../vs140/Commands-Element.md)|Represents the collection of commands on the VSPackage toolbar.|  
  
## Example  
  
```  
<Buttons>  
  <Button guid="guidMenuAndCommandsCmdSet" id="cmdidMyCommand"     priority="0x100" type="Button">  
    <Parent guid="guidMenuAndCommandsCmdSet" id="MyMenuGroup"/>  
    <Icon guid="guidGenericCmdBmp" id="bmpArrow"/>  
    <Strings>  
      <ButtonText>C# Command Sample</ButtonText>  
    </Strings>  
  </Button>  
</Buttons>  
```  
  
## See Also  
 [How VSPackages Contribute User Interface Elements](../Topic/How%20VSPackages%20Add%20User%20Interface%20Elements.md)   
 [Menu and Toolbar Commands](../Topic/Commands,%20Menus,%20and%20Toolbars.md)
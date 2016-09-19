---
title: "CLinearTransitionFromSpeed Class"
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
ms.assetid: 8f159a1c-8893-4017-951e-09e5758aba7d
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinearTransitionFromSpeed Class
Encapsulates a linear-speed transition.  
  
## Syntax  
  
```  
class CLinearTransitionFromSpeed : public CBaseTransition;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CLinearTransitionFromSpeed::CLinearTransitionFromSpeed](#clineartransitionfromspeed__clineartransitionfromspeed)|Constructs a linear-speed transition object and initializes it with speed and final value.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CLinearTransitionFromSpeed::Create](#clineartransitionfromspeed__create)|Calls the transition library to create encapsulated transition COM object. (Overrides [CBaseTransition::Create](../vs140/CBaseTransition-Class.md#cbasetransition__create).)|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CLinearTransitionFromSpeed::m_dblFinalValue](#clineartransitionfromspeed__m_dblfinalvalue)|The value of the animation variable at the end of the transition.|  
|[CLinearTransitionFromSpeed::m_dblSpeed](#clineartransitionfromspeed__m_dblspeed)|The absolute value of the variable's velocity.|  
  
## Remarks  
 During a linear-speed transition, the value of the animation variable changes at a specified rate. The duration of the transition is determined by the difference between the initial value and the specified final value. Because all transitions are cleared automatically, it's recommended to allocated them using operator new. The encapsulated IUIAnimationTransition COM object is created by CAnimationController::AnimateGroup, until then it's NULL. Changing member variables after creation of this COM object has no effect.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CBaseTransition](../vs140/CBaseTransition-Class.md)  
  
 [CLinearTransitionFromSpeed](../vs140/CLinearTransitionFromSpeed-Class.md)  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
##  <a name="clineartransitionfromspeed__clineartransitionfromspeed"></a>  CLinearTransitionFromSpeed::CLinearTransitionFromSpeed  
 Constructs a linear-speed transition object and initializes it with speed and final value.  
  
```  
CLinearTransitionFromSpeed(  
   DOUBLE dblSpeed,  
   DOUBLE dblFinalValue  
);  
```  
  
### Parameters  
 `dblSpeed`  
 The absolute value of the variable's velocity.  
  
 `dblFinalValue`  
 The value of the animation variable at the end of the transition.  
  
##  <a name="clineartransitionfromspeed__create"></a>  CLinearTransitionFromSpeed::Create  
 Calls the transition library to create encapsulated transition COM object.  
  
```  
virtual BOOL Create(  
   IUIAnimationTransitionLibrary* pLibrary,  
   IUIAnimationTransitionFactory* */  
);  
```  
  
### Parameters  
 `pLibrary`  
 A pointer to transition library, which is responsible for creation of standard transitions.  
  
### Return Value  
 TRUE if transition is created successfully; otherwise FALSE.  
  
##  <a name="clineartransitionfromspeed__m_dblfinalvalue"></a>  CLinearTransitionFromSpeed::m_dblFinalValue  
 The value of the animation variable at the end of the transition.  
  
```  
DOUBLE m_dblFinalValue;  
```  
  
##  <a name="clineartransitionfromspeed__m_dblspeed"></a>  CLinearTransitionFromSpeed::m_dblSpeed  
 The absolute value of the variable's velocity.  
  
```  
DOUBLE m_dblSpeed;  
```  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)
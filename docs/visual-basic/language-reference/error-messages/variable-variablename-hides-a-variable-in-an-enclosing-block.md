---
title: La variable '<variablename>' oculta una variable en un bloque de inclusión
ms.date: 07/20/2015
f1_keywords:
- vbc30616
- bc30616
helpviewer_keywords:
- BC30616
ms.assetid: e7658ebc-da45-451b-a409-a0f8915f0beb
ms.openlocfilehash: 68ec1aac7ee8d292e2a433e0fb35039d4fb317b4
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278504"
---
# <a name="variable-variablename-hides-a-variable-in-an-enclosing-block"></a>Variable '\<NombreDeVariable >' oculta una variable en un bloque de inclusión
Una variable incluida en un bloque tiene el mismo nombre que otra variable local.  
  
 **Identificador de error:** BC30616  
  
## <a name="to-correct-this-error"></a>Para corregir este error  
  
-   Cambiar el nombre de la variable del bloque contenedor para que no sea igual que cualquier otra variable local. Por ejemplo:  
  
    ```  
    Dim a, b, x As Integer  
    If a = b Then  
       Dim y As Integer = 20 ' Uniquely named block variable.  
    End If  
    ```  
  
-   Una causa común de este error es el uso de `Catch e As Exception` dentro de un controlador de eventos. Si este es el caso, el nombre del `Catch` variable de bloque `ex` lugar `e`.  
  
-   Otra fuente común de este error es un intento para tener acceso a una variable local declarada dentro de un `Try` bloquear en otro `Catch` bloque. Para corregir este problema, declare la variable fuera del `Try...Catch...Finally` estructura.  
  
## <a name="see-also"></a>Vea también
- [Try...Catch...Finally (instrucción)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [Declaración de variables](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)

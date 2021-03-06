---
title: multiplicidad de extremo de asociación
ms.date: 03/30/2017
ms.assetid: 340926ee-aefb-4bef-92cc-453e5251fd03
ms.openlocfilehash: 6d1b31c5b5ead701fbe808b91d7191fb84dc86c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54502642"
---
# <a name="association-end-multiplicity"></a>multiplicidad de extremo de asociación
*Multiplicidad de extremo de asociación* define el número de [tipo de entidad](../../../../docs/framework/data/adonet/entity-type.md) instancias que pueden estar en un extremo de un [asociación](../../../../docs/framework/data/adonet/association-type.md).  
  
 Una multiplicidad de extremo de asociación puede tener uno de los valores siguientes:  
  
-   uno (1): Indica que esa instancia de tipo exactamente una entidad existe en el extremo de asociación.  
  
-   cero o uno (de 0.. 1): Indica que hay cero o una instancia de tipo de entidad en el extremo de asociación.  
  
-   muchos (*): indica que el cero, uno o más instancias del tipo de entidad existen en el extremo de asociación.  
  
 Normalmente, una asociación se caracteriza por sus multiplicidades de extremo de asociación. Por ejemplo, si los extremos de una asociación tienen multiplicidades uno (1) y varios (*), la asociación se denomina una asociación uno a varios. En el ejemplo siguiente, la asociación `PublishedBy` es una asociación uno a varios (un publicador publica muchos libros y un libro solo puede ser publicado por un publicador). La asociación `WrittenBy` es una asociación varios a varios (un libro puede tener varios autores y un autor puede escribir varios libros).  
  
## <a name="example"></a>Ejemplo  
 El diagrama siguiente muestra un modelo conceptual con dos asociaciones: `PublishedBy` y `WrittenBy`. Los extremos de asociación para la asociación `PublishedBy` son los tipos de entidad `Book` y `Publisher`. La multiplicidad del extremo `Publisher` es uno (1) y la multiplicidad del extremo `Book` es muchos (*).  
  
 ![Ejemplo de modelo](../../../../docs/framework/data/adonet/media/examplemodel.gif "ExampleModel")  
  
 ADO.NET Entity Framework usa un lenguaje específico de dominio (DSL) denominado lenguaje de definición de esquemas conceptuales ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) para definir los modelos conceptuales. El código CSDL siguiente define la asociación `PublishedBy` mostrada en el diagrama anterior:  
  
 [!code-xml[EDM_Example_Model#AssociationExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#associationexample)]  
  
## <a name="see-also"></a>Vea también
- [Conceptos clave de Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)

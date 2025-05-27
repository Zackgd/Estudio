### Uso
Las clases se declaran mediante la palabra clave *Class*
`class TestClass
{
    //Methods, properties, fields, events, delegates
    // and nested classes go here.
}` 
### Cosas a Tener en cuenta.
Solo la herencia simple se permite en C'#', en otras palabras, una clase puede heredar la implementación solo de **Una** Clase **Base**. En cambio, una clase puede implementar **mas de una** Interfaz

| Herencia                             | Ejemplo                                         |
| ------------------------------------ | ----------------------------------------------- |
| Nada                                 | `class ClassA { }`                              |
| Única                                | `class DerivedClass : BaseClass { }`            |
| Ninguna, Implementación 2 Interfaces | `class ImplClass : IFace1, IFace2 { }`          |
| Única, Implementación 1 Interfaz     | `class ImplDerivedClass : BaseClass, IFace1 {}` |

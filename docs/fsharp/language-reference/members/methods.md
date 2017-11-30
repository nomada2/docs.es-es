---
title: "Métodos (F#)"
description: "Obtenga información acerca de cómo un método de F # es una función asociada a un tipo que se utilizan para exponer e implementar la funcionalidad y el comportamiento de objetos y tipos."
keywords: "visual f#, f#, programación funcional"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 1febab3b-c922-49c6-889f-c22db107710c
ms.openlocfilehash: dae31abe6bb0773671b889646c9cceb410a492cd
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="methods"></a><span data-ttu-id="8a197-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a197-104">Methods</span></span>

<span data-ttu-id="8a197-105">A *método* es una función que está asociada a un tipo.</span><span class="sxs-lookup"><span data-stu-id="8a197-105">A *method* is a function that is associated with a type.</span></span> <span data-ttu-id="8a197-106">En la programación orientada a objetos, los métodos se utilizan para exponer e implementar la funcionalidad y el comportamiento de objetos y tipos.</span><span class="sxs-lookup"><span data-stu-id="8a197-106">In object-oriented programming, methods are used to expose and implement the functionality and behavior of objects and types.</span></span>


## <a name="syntax"></a><span data-ttu-id="8a197-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a197-107">Syntax</span></span>

```fsharp
// Instance method definition.
[ attributes ]
member [inline] self-identifier.method-nameparameter-list [ : return-type ]=
    method-body

// Static method definition.
[ attributes ]
static member [inline] method-nameparameter-list [ : return-type ]=
    method-body

// Abstract method declaration or virtual dispatch slot.
[ attributes ]
abstract member self-identifier.method-name : type-signature

// Virtual method declaration and default implementation.
[ attributes ]
abstract member [inline] self-identifier.method-name : type-signature
[ attributes ]
default member [inline] self-identifier.method-nameparameter-list[ : return-type ] =
    method-body

// Override of inherited virtual method.
[ attributes ]
override member [inline] self-identifier.method-nameparameter-list [ : return-type ]=
    method-body

// Optional and DefaultParameterValue attributes on input parameters
[ attributes ]
[ modifier ] member [inline] self-identifier.method-name ([<Optional; DefaultParameterValue([ default-value ])>] input) [ : return-type ]
```

## <a name="remarks"></a><span data-ttu-id="8a197-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a197-108">Remarks</span></span>
<span data-ttu-id="8a197-109">En la sintaxis anterior, puede ver las distintas formas de definiciones y declaraciones de método.</span><span class="sxs-lookup"><span data-stu-id="8a197-109">In the previous syntax, you can see the various forms of method declarations and definitions.</span></span> <span data-ttu-id="8a197-110">En los cuerpos de método más largos, el signo igual (=) después de un salto de línea y se aplica sangría al cuerpo del método completo.</span><span class="sxs-lookup"><span data-stu-id="8a197-110">In longer method bodies, a line break follows the equal sign (=), and the whole method body is indented.</span></span>

<span data-ttu-id="8a197-111">Atributos se pueden aplicar a cualquier declaración de método.</span><span class="sxs-lookup"><span data-stu-id="8a197-111">Attributes can be applied to any method declaration.</span></span> <span data-ttu-id="8a197-112">Que preceden a la sintaxis para una definición de método y normalmente se muestran en una línea independiente.</span><span class="sxs-lookup"><span data-stu-id="8a197-112">They precede the syntax for a method definition and are usually listed on a separate line.</span></span> <span data-ttu-id="8a197-113">Para obtener más información, consulte [Attributes](../attributes.md) (Atributos).</span><span class="sxs-lookup"><span data-stu-id="8a197-113">For more information, see [Attributes](../attributes.md).</span></span>

<span data-ttu-id="8a197-114">Se pueden marcar métodos `inline`.</span><span class="sxs-lookup"><span data-stu-id="8a197-114">Methods can be marked `inline`.</span></span> <span data-ttu-id="8a197-115">Para más información sobre `inline`, vea [Inline Functions](../functions/inline-functions.md) (Funciones insertadas).</span><span class="sxs-lookup"><span data-stu-id="8a197-115">For information about `inline`, see [Inline Functions](../functions/inline-functions.md).</span></span>

<span data-ttu-id="8a197-116">Métodos de inline no se pueden utilizar de forma recursiva dentro del tipo; no es necesario utilizar explícitamente la `rec` palabra clave.</span><span class="sxs-lookup"><span data-stu-id="8a197-116">Non-inline methods can be used recursively within the type; there is no need to explicitly use the `rec` keyword.</span></span>


## <a name="instance-methods"></a><span data-ttu-id="8a197-117">Métodos de instancia</span><span class="sxs-lookup"><span data-stu-id="8a197-117">Instance Methods</span></span>
<span data-ttu-id="8a197-118">Métodos de instancia se declaran con la `member` palabra clave y un *self-identifier*, seguido de un punto (.) y el nombre de método y parámetros.</span><span class="sxs-lookup"><span data-stu-id="8a197-118">Instance methods are declared with the `member` keyword and a *self-identifier*, followed by a period (.) and the method name and parameters.</span></span> <span data-ttu-id="8a197-119">Como es el caso de `let` enlaces, el *lista de parámetros* puede ser un modelo.</span><span class="sxs-lookup"><span data-stu-id="8a197-119">As is the case for `let` bindings, the *parameter-list* can be a pattern.</span></span> <span data-ttu-id="8a197-120">Por lo general, incluya método parámetros entre paréntesis en forma de tupla, que lo constituyen los métodos de manera aparecen en F # cuando se crean en otros lenguajes de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8a197-120">Typically, you enclose method parameters in parentheses in a tuple form, which is the way methods appear in F# when they are created in other .NET Framework languages.</span></span> <span data-ttu-id="8a197-121">Sin embargo, el formulario currificado (parámetros separados por espacios) también es común y se admiten también otros patrones.</span><span class="sxs-lookup"><span data-stu-id="8a197-121">However, the curried form (parameters separated by spaces) is also common, and other patterns are supported also.</span></span>

<span data-ttu-id="8a197-122">En el ejemplo siguiente se muestra la definición y uso de un método de instancia no abstracta.</span><span class="sxs-lookup"><span data-stu-id="8a197-122">The following example illustrates the definition and use of a non-abstract instance method.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3401.fs)]

<span data-ttu-id="8a197-123">Dentro de los métodos de instancia, no utilice el identificador propio para campos de acceso definidos mediante enlaces.</span><span class="sxs-lookup"><span data-stu-id="8a197-123">Within instance methods, do not use the self identifier to access fields defined by using let bindings.</span></span> <span data-ttu-id="8a197-124">Use el identificador propio al obtener acceso a otros miembros y propiedades.</span><span class="sxs-lookup"><span data-stu-id="8a197-124">Use the self identifier when accessing other members and properties.</span></span>


## <a name="static-methods"></a><span data-ttu-id="8a197-125">Métodos estáticos</span><span class="sxs-lookup"><span data-stu-id="8a197-125">Static Methods</span></span>
<span data-ttu-id="8a197-126">La palabra clave `static` se utiliza para especificar que un método se pueda llamar sin una instancia y no está asociado a una instancia de objeto.</span><span class="sxs-lookup"><span data-stu-id="8a197-126">The keyword `static` is used to specify that a method can be called without an instance and is not associated with an object instance.</span></span> <span data-ttu-id="8a197-127">De lo contrario, son métodos de instancia.</span><span class="sxs-lookup"><span data-stu-id="8a197-127">Otherwise, methods are instance methods.</span></span>

<span data-ttu-id="8a197-128">El ejemplo en la siguiente sección muestra los campos declarados con la `let` palabra clave, los miembros de propiedad declarados con la `member` palabra clave y un método estático que se declara con el `static` palabra clave.</span><span class="sxs-lookup"><span data-stu-id="8a197-128">The example in the next section shows fields declared with the `let` keyword, property members declared with the `member` keyword, and a static method declared with the `static` keyword.</span></span>

<span data-ttu-id="8a197-129">En el ejemplo siguiente se muestra la definición y uso de métodos estáticos.</span><span class="sxs-lookup"><span data-stu-id="8a197-129">The following example illustrates the definition and use of static methods.</span></span> <span data-ttu-id="8a197-130">Se supone que estas definiciones de método están en la `SomeType` clase en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="8a197-130">Assume that these method definitions are in the `SomeType` class in the previous section.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3402.fs)]

## <a name="abstract-and-virtual-methods"></a><span data-ttu-id="8a197-131">Métodos abstractos y virtuales</span><span class="sxs-lookup"><span data-stu-id="8a197-131">Abstract and Virtual Methods</span></span>
<span data-ttu-id="8a197-132">La palabra clave `abstract` indica que un método tiene una entrada de distribución virtual y no puede tener una definición de la clase.</span><span class="sxs-lookup"><span data-stu-id="8a197-132">The keyword `abstract` indicates that a method has a virtual dispatch slot and might not have a definition in the class.</span></span> <span data-ttu-id="8a197-133">A *entrada de distribución virtual* es una entrada en una tabla de funciones mantenida internamente que se utiliza en tiempo de ejecución para buscar una función virtual a la que se llama en un tipo orientado a objetos.</span><span class="sxs-lookup"><span data-stu-id="8a197-133">A *virtual dispatch slot* is an entry in an internally maintained table of functions that is used at run time to look up virtual function calls in an object-oriented type.</span></span> <span data-ttu-id="8a197-134">El mecanismo de distribución virtual es el que implementa *polimorfismo*, una característica importante de la programación orientada a objetos.</span><span class="sxs-lookup"><span data-stu-id="8a197-134">The virtual dispatch mechanism is the mechanism that implements *polymorphism*, an important feature of object-oriented programming.</span></span> <span data-ttu-id="8a197-135">Es una clase que tiene al menos un método abstracto sin una definición de un *clase abstracta*, lo que significa que no se puede crear ninguna instancia de esa clase.</span><span class="sxs-lookup"><span data-stu-id="8a197-135">A class that has at least one abstract method without a definition is an *abstract class*, which means that no instances can be created of that class.</span></span> <span data-ttu-id="8a197-136">Para obtener más información sobre las clases abstractas, vea [clases abstractas](../abstract-classes.md).</span><span class="sxs-lookup"><span data-stu-id="8a197-136">For more information about abstract classes, see [Abstract Classes](../abstract-classes.md).</span></span>

<span data-ttu-id="8a197-137">Declaraciones de métodos abstractos no incluyen un cuerpo de método.</span><span class="sxs-lookup"><span data-stu-id="8a197-137">Abstract method declarations do not include a method body.</span></span> <span data-ttu-id="8a197-138">En su lugar, el nombre del método va seguido de dos puntos (:) y una signatura de tipo para el método.</span><span class="sxs-lookup"><span data-stu-id="8a197-138">Instead, the name of the method is followed by a colon (:) and a type signature for the method.</span></span> <span data-ttu-id="8a197-139">La firma de tipo de un método es el mismo que se muestra con IntelliSense cuando sitúe el puntero del mouse sobre un nombre de método en el Editor de código de Visual Studio, excepto sin nombres de parámetro.</span><span class="sxs-lookup"><span data-stu-id="8a197-139">The type signature of a method is the same as that shown by IntelliSense when you pause the mouse pointer over a method name in the Visual Studio Code Editor, except without parameter names.</span></span> <span data-ttu-id="8a197-140">Las signaturas de tipo también se muestran el intérprete, fsi.exe, cuando se trabaja de forma interactiva.</span><span class="sxs-lookup"><span data-stu-id="8a197-140">Type signatures are also displayed by the interpreter, fsi.exe, when you are working interactively.</span></span> <span data-ttu-id="8a197-141">La firma de tipo de un método está formada por enumerando los tipos de los parámetros, seguidos por el tipo de valor devuelto, con símbolos separadores adecuados.</span><span class="sxs-lookup"><span data-stu-id="8a197-141">The type signature of a method is formed by listing out the types of the parameters, followed by the return type, with appropriate separator symbols.</span></span> <span data-ttu-id="8a197-142">Currificadas parámetros se separan mediante `->` y parámetros de tupla se separan mediante `*`.</span><span class="sxs-lookup"><span data-stu-id="8a197-142">Curried parameters are separated by `->` and tuple parameters are separated by `*`.</span></span> <span data-ttu-id="8a197-143">El valor devuelto siempre se separa de los argumentos mediante un `->` símbolos.</span><span class="sxs-lookup"><span data-stu-id="8a197-143">The return value is always separated from the arguments by a `->` symbol.</span></span> <span data-ttu-id="8a197-144">Puede utilizar paréntesis para agrupar parámetros complejos, por ejemplo, cuando un tipo de función es un parámetro, o para indicar cuándo una tupla se trata como un solo parámetro y no como dos parámetros.</span><span class="sxs-lookup"><span data-stu-id="8a197-144">Parentheses can be used to group complex parameters, such as when a function type is a parameter, or to indicate when a tuple is treated as a single parameter rather than as two parameters.</span></span>

<span data-ttu-id="8a197-145">También puede proporcionar las definiciones default de métodos abstractos agregando la definición a la clase y usando el `default` palabra clave, como se muestra en el bloque de sintaxis en este tema.</span><span class="sxs-lookup"><span data-stu-id="8a197-145">You can also give abstract methods default definitions by adding the definition to the class and using the `default` keyword, as shown in the syntax block in this topic.</span></span> <span data-ttu-id="8a197-146">Un método abstracto que tiene una definición de la misma clase es equivalente a un método virtual de otros lenguajes de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8a197-146">An abstract method that has a definition in the same class is equivalent to a virtual method in other .NET Framework languages.</span></span> <span data-ttu-id="8a197-147">Si no existe una definición, la `abstract` palabra clave, crea un nuevo espacio de envío en la tabla de funciones virtuales para la clase.</span><span class="sxs-lookup"><span data-stu-id="8a197-147">Whether or not a definition exists, the `abstract` keyword creates a new dispatch slot in the virtual function table for the class.</span></span>

<span data-ttu-id="8a197-148">Independientemente de si una clase base implementa sus métodos abstractos, las clases derivadas pueden proporcionar implementaciones de métodos abstractos.</span><span class="sxs-lookup"><span data-stu-id="8a197-148">Regardless of whether a base class implements its abstract methods, derived classes can provide implementations of abstract methods.</span></span> <span data-ttu-id="8a197-149">Para implementar un método abstracto en una clase derivada, defina un método que tiene el mismo nombre y la firma de la clase derivada, excepto el uso del `override` o `default` (palabra clave) y proporcionar el cuerpo del método.</span><span class="sxs-lookup"><span data-stu-id="8a197-149">To implement an abstract method in a derived class, define a method that has the same name and signature in the derived class, except use the `override` or `default` keyword, and provide the method body.</span></span> <span data-ttu-id="8a197-150">Las palabras clave `override` y `default` significan exactamente lo mismo.</span><span class="sxs-lookup"><span data-stu-id="8a197-150">The keywords `override` and `default` mean exactly the same thing.</span></span> <span data-ttu-id="8a197-151">Usar `override` si el nuevo método reemplaza la implementación de una clase base; use `default` al crear una implementación en la misma clase que la declaración abstracta original.</span><span class="sxs-lookup"><span data-stu-id="8a197-151">Use `override` if the new method overrides a base class implementation; use `default` when you create an implementation in the same class as the original abstract declaration.</span></span> <span data-ttu-id="8a197-152">No utilice la `abstract` palabra clave en el método que implementa el método que se declaró como abstracto en la clase base.</span><span class="sxs-lookup"><span data-stu-id="8a197-152">Do not use the `abstract` keyword on the method that implements the method that was declared abstract in the base class.</span></span>

<span data-ttu-id="8a197-153">En el ejemplo siguiente se muestra un método abstracto `Rotate` que tiene una implementación de forma predeterminada, el equivalente de un método virtual de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8a197-153">The following example illustrates an abstract method `Rotate` that has a default implementation, the equivalent of a .NET Framework virtual method.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3403.fs)]

<span data-ttu-id="8a197-154">En el ejemplo siguiente se muestra una clase derivada que reemplaza un método de clase base.</span><span class="sxs-lookup"><span data-stu-id="8a197-154">The following example illustrates a derived class that overrides a base class method.</span></span> <span data-ttu-id="8a197-155">En este caso, el reemplazo cambia el comportamiento para que el método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="8a197-155">In this case, the override changes the behavior so that the method does nothing.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3404.fs)]

## <a name="overloaded-methods"></a><span data-ttu-id="8a197-156">Métodos sobrecargados</span><span class="sxs-lookup"><span data-stu-id="8a197-156">Overloaded Methods</span></span>
<span data-ttu-id="8a197-157">Métodos sobrecargados son métodos que tienen nombres idénticos en un tipo determinado, pero que tiene argumentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="8a197-157">Overloaded methods are methods that have identical names in a given type but that have different arguments.</span></span> <span data-ttu-id="8a197-158">En F #, los argumentos opcionales se suelen utilizar en lugar de métodos sobrecargados.</span><span class="sxs-lookup"><span data-stu-id="8a197-158">In F#, optional arguments are usually used instead of overloaded methods.</span></span> <span data-ttu-id="8a197-159">Sin embargo, se permiten métodos sobrecargados en el lenguaje, siempre que los argumentos estén en forma de tupla, no currificada formulario.</span><span class="sxs-lookup"><span data-stu-id="8a197-159">However, overloaded methods are permitted in the language, provided that the arguments are in tuple form, not curried form.</span></span>

## <a name="optional-arguments"></a><span data-ttu-id="8a197-160">Argumentos opcionales</span><span class="sxs-lookup"><span data-stu-id="8a197-160">Optional Arguments</span></span>

<span data-ttu-id="8a197-161">A partir de F # 4.1, también puede tener argumentos opcionales con un valor de parámetro predeterminado en métodos.</span><span class="sxs-lookup"><span data-stu-id="8a197-161">Starting with F# 4.1, you can also have optional arguments with a default parameter value in methods.</span></span>  <span data-ttu-id="8a197-162">Esto sirve para ayudar a facilitar la interoperación con código C#.</span><span class="sxs-lookup"><span data-stu-id="8a197-162">This is to help facilitate interoperation with C# code.</span></span>  <span data-ttu-id="8a197-163">En el ejemplo siguiente se muestra la sintaxis:</span><span class="sxs-lookup"><span data-stu-id="8a197-163">The following example demonstrates the syntax:</span></span>

```fsharp
// A class with a method M, which takes in an optional integer argument.
type C() =
    __.M([<Optional; DefaultParameterValue(12)>] i) = i + 1
```

<span data-ttu-id="8a197-164">Tenga en cuenta que el valor pasado en para `DefaultParameterValue` debe coincidir con el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8a197-164">Note that the value passed in for `DefaultParameterValue` must match the input type.</span></span>  <span data-ttu-id="8a197-165">En el ejemplo anterior, es un `int`.</span><span class="sxs-lookup"><span data-stu-id="8a197-165">In the above sample, it is an `int`.</span></span>  <span data-ttu-id="8a197-166">Intenta pasar un valor no entero en `DefaultParameterValue` produciría un error de compilación.</span><span class="sxs-lookup"><span data-stu-id="8a197-166">Attempting to pass a non-integer value into `DefaultParameterValue` would result in a compile error.</span></span>

## <a name="example-properties-and-methods"></a><span data-ttu-id="8a197-167">Ejemplo: Propiedades y métodos</span><span class="sxs-lookup"><span data-stu-id="8a197-167">Example: Properties and Methods</span></span>
<span data-ttu-id="8a197-168">El ejemplo siguiente contiene un tipo que tiene ejemplos de campos, funciones privadas, propiedades y un método estático.</span><span class="sxs-lookup"><span data-stu-id="8a197-168">The following example contains a type that has examples of fields, private functions, properties, and a static method.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3406.fs)]

## <a name="see-also"></a><span data-ttu-id="8a197-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a197-169">See Also</span></span>
[<span data-ttu-id="8a197-170">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a197-170">Members</span></span>](index.md)
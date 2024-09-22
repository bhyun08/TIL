Classes, objects, interfaces, constructors, and functions, as well as properties and their setters, can have visibility modifiers. There are four visibility modifiers in Kotlin: `private`, `protected`, `internal`, and `public`. The default visibility is `public`.
### public(default)
Public has the widest range of access and is accessible from anywhere. Unless you explicitly write public, by default, all declarations are set to public.
### private
Private is only accessible within the declared range. If an element is declared private in a class, file, etc., it can only be accessed within that class or within the file.
### protected
Protected is accessible to a class and its inherited subclasses. In Kotlin, protected is not available at the package level, and can only be accessed within the class inheritance layer.
### internal
Internal is only accessible within the same module. Kotlin's module is a unit of a project or library, or multiple files. Elements declared internal are accessible within the module but not outside the module.

---
Reference link 🙂       
https://kotlinlang.org/docs/visibility-modifiers.html


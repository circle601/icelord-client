# Code Style

  * soft tabs of 4 spaces
  * fancy indenting is allowed to make the code more clear

## Naming
NOTE: in CamelCase acronyms should be treated as normal words (CPU becomes Cpu)

  * types (enums, classes, etc.) - CamelCase
  * variables - snake\_case
  * functions - snake\_case
  * namespaces - snake\_case
  * constants - SCREAMING\_SNAKE\_CASE
  * files - snake\_case

## Headers
  * in headers, use `#pragma once`
  * in headers, use forward declarations as often as possible
  * headers should be in a namespace corresponding to its path for example
    * `world/entity/type.hpp` defines a class `Type` in a namespace `world::entity` so it becomes
    * `world::entity::Type`
  * if the header defines a class that has the same name as the namespace for example
    * `world/entity/entity.hpp` would normally define the class `Entity` in the namespace but additionaly
    * add a typedef in the parent namespace defining `world::entity::Entity` as `world::Entity`

## Design
  * classes should generally follow the rule of encapsulation and declare no public member variables
  * pointers should be replaced with references where they can

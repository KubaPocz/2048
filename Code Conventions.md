# Code Conventions

## Naming Conventions

### Variables
- **Public and internal variables** should always start with a capital letter (`PascalCasing`), for example: `ChannelName`.
- **Private variables** should start with a lowercase letter and a leading underscore (`_camelCasing`), for example: `_background`.

### Class, Method, and Property Names
- Use **PascalCasing** for class names, method names, and property names, for example: `SomeClass`, `CalculateSomething`, `IsActive`.

### Constants
- Constants should be written in **UPPERCASE**, regardless of the access modifier, for example: `public const int ShippingType = 123;` or `const float Pi = 3.14f`.
- Avoid writing constants in lowercase or with underscores for private constants.

### Method Arguments and Local Variables
- Use **camelCasing** for method arguments and local variables, for example: `someMsg`, `_localVariable`.

### Avoid Hungarian Notation
- Do not use Hungarian notation (e.g., `strName`, `iCounter`, `m_time`). Instead, use meaningful names without unnecessary prefixes.
- Example:
  - **Correct**: `int counter;`
  - **Avoid**: `int iCounter;`, `float m_time;`

### Abbreviations
- Avoid unnecessary abbreviations unless they are widely understood, such as `Id`, `XML`, `NPC`, etc.
- Example:
  - **Correct**: `UserGroup userGroup;`, `Assignment employeeAssignment;`
  - **Avoid**: `UserGroup usrGrp;`, `Assignment empAssignment;`
- Abbreviations such as `AR`, `UI` can be written in uppercase, but ensure consistency.

### Underscores
- Do not use underscores in identifiers unless for private fields or method variants (when a better name can't be found).
- Example:
  - **Correct**: `DateTime _registrationDate;`
  - **Avoid**: `DateTime Client_Appointment;`, `float _time_left;`
- Exception: Variants like `HandleTap_Gameplay()` are acceptable.

### Config Naming
- If there is only one config in the class, it should be named `_config`. If multiple configs exist, their names should match the type, for example: `_playerConfig`, `_npcConfig`.

---

## Types, Namespaces, and Attributes

### Namespaces
- Each script should start with a `namespace` that matches the folder structure. Do not start with `Assets.Scripts`, and omit the root namespace (`GameLogic`, `UI`).

### Access Modifiers
- Use the `private` keyword only when necessary (for example, with getters/setters). For internal classes, `internal` is not needed.

### Precise Variable Types
- Always use the most precise type for a variable. For example, if a game object has an `Image` component, declare it as `Image _image`, not `GameObject _image`.

### Attributes
- Place attributes on their own line, not inline with the property or class.

Example:
```csharp
[DisallowMultipleComponent]
public class SomeView : MonoBehaviour
{
    [SerializeField] Image _icon;
    [SerializeField] Button _button;
}

# Project Structure

## Root Organization

```
/
├── src/                          # 1C configuration sources (EDT format)
├── .settings/                    # Eclipse/EDT project settings
├── .kiro/                        # Kiro AI assistant configuration
├── DT-INF/                       # EDT project metadata
├── README.md                     # Main documentation (Russian)
└── МЕТОДЫ_КОНСОЛИ.md            # Console methods reference (Russian)
```

## Source Code Structure (`src/`)

### Configuration Metadata
- `Configuration/` - Main configuration descriptor

### Common Modules (Общие модули)
All modules use `конс_` prefix:
- `конс_ОбщийМодульКлиент/` - Client-side API and editor integration
- `конс_ОбщийМодульСервер/` - Server-side form initialization
- `конс_ОбщийМодульВызовСервера/` - Server call wrapper

### Common Forms (Общие формы)
- `конс_РедактированиеКода/` - Main code editor form
- `конс_КаталогИсходников/` - Source directory configuration

### Data Processors (Обработки)
Demo/example processors:
- `конс_ДемоКонсоль/` - Basic console demo
- `конс_ДемоКонсольКоманды/` - Commands demonstration (33 commands)
- `конс_ДемоСтраницы/` - Multi-page editing demo

### Supporting Objects
- `CommonTemplates/конс_src/` - Monaco Editor source files (ZIP archive)
- `CommonPictures/конс_КартинкаПодсистемы/` - Subsystem icon
- `CommonCommands/kaf_ОбновитьКонсоль/` - Console refresh command
- `Constants/конс_КаталогИсходников/` - Source directory constant
- `Roles/конс_ОсновнаяРоль/` - Main role for access rights
- `Subsystems/конс_КонсольКода/` - Code console subsystem

## Naming Conventions

### Prefixes
- **конс_** (cons_) - All extension objects use this prefix
- **kaf_** - Alternative prefix for some commands

### Language
- All code, comments, and identifiers are in **Russian**
- Metadata names use Cyrillic characters
- Form elements, procedures, and functions use Russian names

### Module Structure
BSL modules follow standard 1C regions:
- `#Область ПрограммныйИнтерфейс` - Public API
- `#Область СлужебныйПрограммныйИнтерфейс` - Internal API
- `#Область СлужебныеПроцедурыИФункции` - Private procedures/functions
- `#Область ОбработчикиСобытийФормы` - Form event handlers
- `#Область ОбработчикиКомандФормы` - Form command handlers

## File Types

- `.mdo` - Metadata object descriptors (XML)
- `.bsl` - BSL source code files
- `.form` - Form layout files (XML)
- `.bin` - Binary template files
- `.cmi` - Command interface files
- `.html` - Help files (Russian)

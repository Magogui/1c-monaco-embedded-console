# Technology Stack

## Platform

- **1C:Enterprise 8.3** (1С:Предприятие 8.3)
- **Language**: BSL (Built-in Script Language) - Russian variant
- **Configuration Type**: Extension (расширение)
- **Application Mode**: Managed Application (управляемое приложение)

## Core Technologies

- **Monaco Editor**: Embedded web-based code editor
- **HTML Document Field**: Used to host Monaco Editor in 1C forms
- **File Extension API**: Required for file operations (not available in web client)

## Project Structure

- Configuration extension with prefix `конс_` (cons_)
- Common modules for client/server architecture:
  - `конс_ИнициализацияРедактораКлиент` - Client-side logic
  - `конс_ИнициализацияРедактораСервер` - Server-side logic  
  - `конс_ИнициализацияРедактораВызовСервера` - Server call module
- Common forms for reusable UI components
- Data processors for demo/testing purposes
- Template storage for Monaco Editor source files

## Build & Deployment

This is a 1C configuration extension. No traditional build process exists.

### Working with the project:

1. **Load extension**: Import into 1C:Enterprise Designer (Конфигуратор)
2. **Test**: Use demo data processors `конс_ДемоКонсоль`, `конс_ДемоКонсольКоманды`, `конс_ДемоСтраницы`
3. **Integration**: Copy form elements and code from demo processors to your objects

### Source code location:

- Configuration sources are in EDT format under `src/`
- Monaco Editor sources are packaged in `src/CommonTemplates/конс_src/Template.bin`
- Sources are extracted to temp directory at runtime

## Code Style Settings

- Eclipse/EDT preferences in `.settings/`
- Module structure creation enabled
- Strict types annotation enabled

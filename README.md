# REPOSITORIO DE LIBROS EN VISUAL BASIC 6

## Descripción del Proyecto

Este es un sistema de gestión de biblioteca personal desarrollado en **Visual Basic 6.0** que permite a los usuarios organizar y administrar su colección de libros de manera eficiente.

<!-- agrega imagen  -->
![Imagen del Proyecto](https://github.com/IVAN-DALI-GARCIA/repositorioDelibros/blob/master/Imagenes/ice_screenshot_20250623-153710.png)

## Características Principales

### 🏠 **Formulario Principal (Form1.frm)**
- **Hub de Lectura**: Interfaz principal con vista de lista que muestra todos los libros
- **Filtros de Búsqueda**: Múltiples opciones para filtrar la colección:
  - 📚 **Catálogo Completo**: Muestra todos los libros
  - ✅ **Ya Leídos**: Libros marcados como leídos
  - 📖 **Quiero Leer**: Lista de libros pendientes por leer
  - ⭐ **Favoritos**: Libros marcados como recomendados
  - 🎭 **Géneros Favoritos**: Filtro por géneros marcados como favoritos
  - 👎 **No Me Gustaron**: Libros con calificación ≤ 2

### 📚 **Gestión de Libros (frmLibro.frm)**
- **Agregar Nuevos Libros**: Formulario completo para registrar libros
- **Editar Libros Existentes**: Modificación de información de libros
- **Campos Disponibles**:
  - Título (obligatorio)
  - Autor (obligatorio)
  - Género (selección desde base de datos)
  - Calificación (1-5, solo para libros leídos)
  - Estado de lectura (Ya leído / Quiero leer)
  - Marcadores especiales (Recomendado, Prestado)
  - Información de préstamo (A quién y fecha)

### 🔄 **Funcionalidades de Gestión**
- **CRUD Completo**: Crear, leer, actualizar y eliminar libros
- **Validación de Datos**: Verificación de campos obligatorios y formatos
- **Confirmación de Eliminación**: Diálogo de seguridad antes de borrar
- **Gestión de Préstamos**: Control de libros prestados con fecha y persona

## Estructura de la Base de Datos

### 📊 **Conexión a SQL Server**
- **Servidor**: `.\MYSERVER` (instancia local)
- **Base de Datos**: `LibreriaMega`
- **Autenticación**: Windows Integrada
- **Proveedor**: SQLOLEDB.1

### 🗂️ **Tablas Principales**
- **Libros**: Almacena toda la información de los libros
- **Géneros**: Catálogo de géneros literarios con opción de favoritos

## Arquitectura del Código

### 📁 **Archivos del Proyecto**
- `Form1.frm` - Formulario principal (Hub de lectura)
- `frmLibro.frm` - Formulario de gestión de libros
- `modConnection.bas` - Módulo de conexión a base de datos
- `Project1.vbp` - Archivo de proyecto principal

### 🔧 **Componentes Técnicos**
- **ADO (ActiveX Data Objects)**: Para conexión y manejo de base de datos
- **ListView Control**: Para mostrar la lista de libros
- **Validación de Entrada**: Control de tipos de datos y rangos
- **Manejo de Errores**: Captura y manejo de excepciones

## Funcionalidades Especiales

### ⚡ **Características Avanzadas**
- **Filtros Dinámicos**: Consultas SQL dinámicas según el filtro seleccionado
- **Interfaz Intuitiva**: Botones con iconos y descripciones claras
- **Validación Inteligente**: 
  - Campos mutuamente excluyentes (Leído/Por Leer)
  - Calificación obligatoria solo para libros leídos
  - Información de préstamo solo cuando está marcado como prestado

### 🎯 **Casos de Uso**
- Bibliotecas personales
- Gestión de colecciones de lectura
- Control de préstamos entre amigos
- Seguimiento de progreso de lectura
- Organización por géneros y preferencias

## Requisitos Técnicos

- **Visual Basic 6.0**
- **SQL Server** (con instancia MYSERVER)
- **Controles ADO** habilitados
- **Microsoft Common Controls 6.0** (mscomctl.ocx)

Este sistema proporciona una solución completa y fácil de usar para cualquier persona que desee organizar su biblioteca personal de manera digital y eficiente.

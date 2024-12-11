# adhd_survival_cs
tips and tricks 

# Script `adhd_survival.sh`

## Propósito

Este script tiene como propósito educativo ayudar a los estudiantes a economizar tiempo mientras trabajan en sus proyectos de programación, en este caso, proyectos de C#. Automatiza tareas repetitivas como la creación, edición, compilación, ejecución, limpieza de archivos temporales y la gestión del repositorio en GitHub. Al hacer esto, los estudiantes pueden concentrarse en desarrollar el contenido del proyecto sin preocuparse por los detalles técnicos de configuración.

---

## Requisitos previos

1. **Herramientas necesarias:**
   - .NET SDK (para usar `dotnet`).
   - Editor de texto como `vim` (instalado por defecto en muchas distribuciones de Linux).
   - Git configurado en tu entorno, si planeas subir el código a GitHub.

2. **Permisos del archivo:**
   Asegúrate de que el script sea ejecutable. Usa el siguiente comando:
   ```bash
   chmod +x adhd_survival.sh
   ```

3. **Ejecución del script:**
   Ejecuta el script desde la terminal con:
   ```bash
   ./adhd_survival.sh
   ```

---

## Pasos del script

### 1. Crear un nuevo proyecto en .NET
- Solicita el nombre del proyecto/tarea.
- Crea una aplicación de consola en .NET utilizando:
  ```bash
  dotnet new console -n <nombre_del_proyecto>
  ```
- Cambia al directorio del proyecto creado.

### 2. Renombrar `Program.cs`
- Renombra el archivo `Program.cs` a `<nombre_del_proyecto>.cs`.

### 3. Crear y editar `main.cs`
- Crea un archivo llamado `main.cs` y te permite editarlo manualmente usando `vim`.

### 4. Editar el archivo principal renombrado
- Abre `<nombre_del_proyecto>.cs` para que lo edites manualmente.

### 5. Compilar el proyecto
- Utiliza `dotnet build` para compilar el proyecto.
- Si hay errores en la compilación, el script se detendrá.

### 6. Ejecutar el proyecto
- Ejecuta el proyecto con `dotnet run` para verificar su funcionamiento.

### 7. Limpiar archivos temporales
- Elimina los directorios `obj`, `bin` y el archivo `main.cs` para mantener limpio el directorio del proyecto.

### 8. Editar el archivo `.csproj`
- Abre el archivo `.csproj` en `vim` para que puedas personalizar su contenido.
- Asegúrate de que contenga lo siguiente:

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp2.1</TargetFramework>
    <RootNamespace>_2_replace_element</RootNamespace>
  </PropertyGroup>

</Project>
```

### 9. Felicitar al usuario
- El script muestra un mensaje de felicitación al completar el proceso exitosamente.

### 10. Subir el código a GitHub (opcional)
- Si decides subir el proyecto, el script ejecuta los comandos:
  ```bash
  git add .
  git commit -m "task"
  git push
  ```

---

## Propósito educativo

Este script está diseñado para simplificar el flujo de trabajo de los estudiantes y reducir distracciones durante el desarrollo de proyectos en C#. Automatizando tareas repetitivas, los estudiantes pueden enfocarse en aprender y mejorar sus habilidades de programación.

---

## Notas importantes

1. **Tiempo de espera entre pasos:** Si necesitas más tiempo para cada paso, puedes agregar más retrasos utilizando el comando `sleep` en el script.
2. **Errores comunes:** Verifica que todos los comandos como `dotnet`, `vim` y `git` estén instalados correctamente si el script falla.
3. **Flexibilidad:** Puedes personalizar el script si hay pasos que no necesitas.

---

## Ejemplo de uso

Si tu tarea se llama `MyTask`:
1. Ejecuta el script e ingresa `MyTask` como el nombre del proyecto.
2. Sigue las indicaciones para:
   - Editar los archivos necesarios.
   - Compilar y ejecutar tu proyecto.
   - Personalizar el archivo `.csproj`.
3. Si decides subir el código a GitHub, asegúrate de que tu repositorio esté configurado previamente.

---

Si necesitan ayuda adicional o más aclaraciones, ¡no duden en preguntar! 😊
att.SGC91

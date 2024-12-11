# Script `adhd_survival.sh`

## Purpose

This script has an educational purpose: to help students save time while working on their programming projects, specifically C# projects. It automates repetitive tasks such as creating, editing, compiling, running, cleaning temporary files, and managing the repository on GitHub. This allows students to focus on developing the project's content without worrying about technical configuration details. Remember to run this code in the directory where the project folders will be created, and not inside each project folder.

---

## Prerequisites

1. **Required tools:**
   - .NET SDK (to use `dotnet`).
   - Text editor like `vim` (installed by default on many Linux distributions).
   - Git configured in your environment if you plan to push the code to GitHub.

2. **File permissions:**
   Make sure the script is executable. Use the following command:
   ```bash
   chmod +x adhd_survival.sh
   ```

3. **Run the script:**
   Run the script from the terminal with:
   ```bash
   ./adhd_survival.sh
   ```

---

## Script Steps

### 1. Create a new .NET project
- Prompts for the project/task name.
- Creates a .NET console application using:
  ```bash
  dotnet new console -n <project_name>
  ```
- Navigates to the created project directory.

### 2. Rename `Program.cs`
- Renames the `Program.cs` file to `<project_name>.cs`.

### 3. Create and edit `main.cs`
- Creates a file named `main.cs` and allows you to edit it manually using `vim`.

### 4. Edit the renamed main file
- Opens `<project_name>.cs` for manual editing.

### 5. Build the project
- Uses `dotnet build` to compile the project.
- Stops the script if there are build errors.

### 6. Run the project
- Runs the project with `dotnet run` to verify functionality.

### 7. Clean temporary files
- Deletes the `obj` and `bin` directories and the `main.cs` file to keep the project directory clean.

### 8. Edit the `.csproj` file
- Opens the `.csproj` file in `vim` for manual customization.
- Ensure it contains the following:

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp2.1</TargetFramework>
    <RootNamespace>_2_replace_element</RootNamespace>
  </PropertyGroup>

</Project>
```

### 9. Congratulate the user
- Displays a congratulatory message upon successful completion of the process.

### 10. Push the code to GitHub (optional)
- If you decide to push the project, the script executes the following commands:
  ```bash
  git add .
  git commit -m "task"
  git push
  ```

---

## Educational Purpose

This script is designed to simplify students' workflow and reduce distractions during the development of C# projects. By automating repetitive tasks, students can focus on learning and improving their programming skills.

---

## Important Notes

1. **Time delay between steps:** If you need more time for each step, you can add more delays using the `sleep` command in the script.
2. **Common errors:** If the script fails, verify that all commands like `dotnet`, `vim`, and `git` are installed correctly.
3. **Flexibility:** You can customize the script if there are steps you do not need.

---

## Example Usage

If your task is called `MyTask`:
1. Run the script and enter `MyTask` as the project name.
2. Follow the prompts to:
   - Edit the necessary files.
   - Compile and run your project.
   - Customize the `.csproj` file.
3. If you decide to push the code to GitHub, make sure your repository is configured beforehand.

---

If you need additional help or further clarifications, don’t hesitate to ask! 😊


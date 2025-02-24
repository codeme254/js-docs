# Package Managers

A package manager is a tool that automates the process of installing, updating, configuring, and removing software 
dependencies (packages) in JavaScript projects.

**Dependencies** in programming refer to the scenario where one piece of software relies on another to function
correctly.

If program A requires program B to run, then program B is a dependency of program A.

There are two types of Dependencies **Direct dependencies** and **transitive dependencies**:
- **Direct dependencies**: Direct dependencies are the core frameworks, modules, and libraries that the code directly 
calls to perform specific functionalities These dependencies are explicitly mentioned in the code and are essential for 
the software to operate. For example, in a JavaScript project, these dependencies are listed in the `package.json` file.
- **Transitive dependencies**: Transitive dependencies are the dependencies of direct dependencies. These are not 
directly used in the code but are required by the components that the developer uses. For instance, if software 
directly depends on module A, and module A depends on module B, then the software indirectly depends on module B and
module B is a transitive dependency.

Dependencies are used to avoid reinventing the wheel and speed up the development process. By leveraging pre-written and 
tested code, developers can focus on building new features rather than writing everything from scratch. This approach 
increases efficiency and allows for the creation of complex applications in a shorter time.

JavaScript has three major package managers (for managing dependencies):
1. **npm (Node Package Manager)**-The default package manager for Node.js.
2. **Yarn**-Developed by Facebook as an alternative to npm, offering better performance and security.
3. **pnpm**-A modern package manager that uses a more efficient way of handling dependencies by creating a global store.
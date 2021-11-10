# [**Node Package Manager**](https://www.npmjs.com)
In this repository you'll find the entire process through learning how to use Npm thanks to the **Oscar Barajas**' couse of Npm on the **Platzi** platform.

## **Table of contents**
- [Installation of Node.js](#installation-of-node.js)
- [Resources](#resources)

![](https://static.platzi.com/media/courses/Opengraph-gestion-dependencias-paquetes-NPM.png)

### **Installation of Node.js**
* First you'll need to install [**Node.js**](https://nodejs.org/en/) (**Npm is installed alongside it**). There are two versions for download, the *Long Term Support* version which's worth for production enviroments and the *Latest* version which's ideal for us, developers.

* Then, once you've installed Node in your machine, you can test the Node and Npm versions that you have installed globally by runnin the **npm -v** and **node -v** commands.

```
    npm -v
```
```
    node -v
```

* Now you'll need to initialize the Npm project, you can do so by running the **npm init** command.

```
    npm init
```

- Here the console will throw you through a basic configuration process where you'll need to fill some fields with information about your package. But, you can ommit this process by using the **-y** (yes) flag when running **npm init**.

```
    npm init -y
```

> **Note:** there are some fields that can be filled automatically by setting a default value for them. You get so by using the **npm set init.** command followed by the field you'd like to fill with default information such as **author./name**, **author./email**, **license**, etc. For more information [check the documentation](https://docs.npmjs.com/cli/v7/commands/npm-config#set)

```
    npm set init.author.name "Said Alejandro"
```

```
    npm set init.author.email "saidmift@outlook.es"
```

```
    npm set init.licese "MIT"
```

Now the next time you skip the whole configuration process you'll get a package.json file with a few fields already specified (the fields you set in the **init** configuration).

## Resources
[Curso de Gestión de Dependencias y Paquetes con NPM](https://platzi.com/cursos/npm/)
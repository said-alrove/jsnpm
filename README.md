# [**Node Package Manager**](https://www.npmjs.com)
In this repository you'll find the entire process through learning how to use Npm thanks to the **Oscar Barajas**' couse of Npm on the **Platzi** platform.

## **Table of contents**
- [Installation of Node.js](#installation-of-node.js)
- [Initialize the project](#initialize-the-project)
    - [Default init configuration](#default-init-configuration)
- [Types of dependencies](#types-of-dependencies)
- [Resources](#resources)

![](https://static.platzi.com/media/courses/Opengraph-gestion-dependencias-paquetes-NPM.png)

## **Installation of Node.js**
First you'll need to install [**Node.js**](https://nodejs.org/en/) (**Npm is installed alongside it**). There are two versions for download, the *Long Term Support* version which's worth for production enviroments and the *Latest* version which's ideal for us, developers.
Then, once you've installed Node in your machine, you can test the Node and Npm versions that you have installed globally by runnin the **npm -v** and **node -v** commands.

```
    npm -v
```
```
    node -v
```

## **Initialize the project**
Now you'll need to initialize the Npm project, you can do so by running the **npm init** command.

```
    npm init
```

- Here the console will throw you through a basic configuration process where you'll need to fill some fields with information about your package. But, you can ommit this process by using the **-y** (yes) flag when running **npm init**.

```
    npm init -y
```

#### **Default init configuration**
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

## **Types of dependencies**
When you're installing a dependency to use it into your project you have a variety of options to save it, here I'll try to explain them shortly and clearly, but if you'd like to dive more into this, [check this out](https://javascript.plainenglish.io/what-the-dependency-types-of-dependencies-in-a-node-js-application-explained-904a5424fbd3).

* **default**: these are dependencies that are required for the production enviroment, here you can put the dependencies the project uses when working. You can save a dependency as a production one by running the **npm i <dependency> -S** command. You can also ommit the **-S** flag, include it or not is the same.

```
    npm i mondogdb -S
```

* **devDependencies**: these are dependencies that are needed in the development enviroment, but not for production. You can save a dependency as a dev one by running the **npm i <dependency> -D** or **npm i <dependency> --save-dev** commands.

```
    npm i postcss-cli -D
```

```
    npm i postcss-cli --save-dev
```

* **optionalDependencies**: these are those dependencies that aren't essential, without them the project still works perfectly, in case of any error when installing the packages, npm will ignore them and won't throw an error or something similar that could stop the installation of the whole project's dependencies. You can save a dependency as a optional one by running the **npm i <dependency> -O** or **npm i <dependency> --save-optional** commands.

```
    npm i chalk -O
```

```
    npm i chalk --save-optional
```

* **peerDependencies**: these are those packages or host tools that are expected the user to having them already installed in its machine, let's imagine we're creating a package for the **car 3.5.0** host tool, so, the user is expected to have the **car** tool in its **3.5.0** version installed for properly performance of our package. These kind of packages/tools can be specified from the console by using the **npm i <dependency> --save-peer** command or directly from the package.json file.

> **Note:** in most of the cases you'll have to do it manually by writing the tool from the **package.json** file giving to the fact that some tools cannot be installed with Npm such as, for example, Node.

```
    npm i <dependency> --save-peer
```

Then we have the **bundledDependencies** which have to be specified manually, in this case I'm not totally sure about how to explain it due to I couldn't understand it at all, this may be because I'm just starting to learn Npm, maybe in the future this will be clarified, by now I'll skip this part, for more information, as I mentioned above, you can check [the article about this topic](https://javascript.plainenglish.io/what-the-dependency-types-of-dependencies-in-a-node-js-application-explained-904a5424fbd3).

## **Resources** 📚
* [Curso de Gestión de Dependencias y Paquetes con NPM](https://platzi.com/cursos/npm/)
* [Different types of dependencies in a Node.js application explained](https://javascript.plainenglish.io/what-the-dependency-types-of-dependencies-in-a-node-js-application-explained-904a5424fbd3)
- [Advantages of bundled dependencies over normal dependencies in npm](https://stackoverflow.com/questions/11207638/advantages-of-bundleddependencies-over-normal-dependencies-in-npm)

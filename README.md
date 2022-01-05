
#Tire Center Modernization UI
Code Repository for the Tire Modernization Front-End
<br>

##Table of Contents
- [About The Project](#about-the-project)
  - [Built With](#built-with)
  - [Other Libraries](#other-libraries)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Suggested Tools](#suggested-tools)
- [How to Contribute](#how-to-contribute)
  - [Git Flow Process](#git-flow-process)
  - [Git Branches Overview](#git-branches-overview)
    - [Main Branches](#main-branches)
    - [Supporting Branches](#supporting-branches)
  - [Git Branch Naming Convention](#git-branch-naming-convention)
    - [General Naming](#general-naming)
    - [Branch-Specific Naming](#branch-specific-naming)
- [Coding Guide](#coding-guide)
  - [File Naming Convention](#file-naming-convention)
  - [Source Structure](#source-structure)
    - [Angular Components](#angular-components)
    - [Angular Services](#angular-services)
    - [Angular Models](#angular-models)
    - [Angular ViewModels](#angular-viewmodels)
    - [Angular Mappers](#angular-mappers)
    - [Angular Locales](#angular-locales)
  - [Code Standards](#code-standards)
    - [TypeScript Coding Standards](#typescript-coding-standards)
    - [HTML Coding Standards](#html-coding-standards)
    - [LESS/CSS Coding Standards](#lesscss-coding-standards)
- [Contact](#contact)
<br>

## About The Project
This project is the front-end component of the Tire Center Modernization project.
<br>

### Built With

* [Angular](https://angular.io/)
* [LESS](https://lesscss.org/)
* [TypeScript](https://www.typescriptlang.org/)

### Other Libraries
* [Angular Material](https://material.angular.io/)
* [Material Icons](https://fonts.google.com/icons)



## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

* Install [npm](https://nodejs.org/en/)
  ```sh
  npm install npm@latest -g
  ```

### Installation

1. Install [Angular CLI](https://angular.io/cli)
   ```sh
   npm install -g @angular/cli
   ```
   If you encounter an error about certificates, execute this command:
   ```sh
   npm config set strict-ssl false
   ```
2. Download [git](https://git-scm.com/downloads) _(or use an IDE like [GitHub Desktop](https://desktop.github.com/))_
   

3. Clone the repo using your IDE of choice.
   ```sh
   git clone https://costcocloudops@dev.azure.com/costcocloudops/Tire%20Center%20Modernization/_git/tires-spa
   ```

4. Create or checkout your branch. Make sure you are not working in `develop`.

5. Install NPM packages
   ```sh
   npm install
   ```
   **NOTE:** You need to be in the angular app directory.It is the same directory as the `package.json` file.
   <br>

6. Done. Start coding. Make sure to follow the [git flow process]().

### Suggested Tools

* [Visual Studio Code](https://code.visualstudio.com/)
* [GitHub Desktop](https://desktop.github.com/)



## How to Contribute

### Git Flow Process
1. Fetch and pull latest `develop` version.*
2. Create your new `feature` branch from `develop`.*
3. Commit your Changes
4. Push or publish your `feature` branch to origin.
5. Open a Pull Request to `develop`

\* `hotfix` branches can branch out from either of the [main branches](#main-branches), usually `master`.

### Git Branches Overview

[Main Branches](#main-branches) | [Supporting Branches](#supporting-branches)

#### Main Branches
There are two main branches: `master` and `develop`. There is only one `master` branch and one `develop` branch.

1. **MASTER Branch**
The `master` branch.
<br>
1. **DEVELOP Branch**
The `develop` branch. This branch is parallel to the `master` branch.
<br>

#### Supporting Branches
In addition to the main branches, we do use supporting branches. We have the following supporting branches: `feature`, `hotfix`, `release`, and `staging`.

1. **FEATURE Branches**
This is used for general user story features. Our current workflow requires us to branch and create our features from `develop`.
<br>
1. **HOTFIX Branches**
This is used for bug fixes after release. This can also be used for non-story code patches *(e.g. git-related, or project-files related changes)*. This branches out of `master`, and directly merges back to `master` *(which can then be used for creating a `release` branch)*. This should also merge to `develop`.
<br>
1. **RELEASE Branches**
This is a dedicated branch line for creating `release` packages which will be deployed to production environment. This merges back to `master` and `develop`.
<br>

### Git Branch Naming Convention

[General Naming](#general-naming) | [Branch Specific Naming](#branch-specific-naming)

#### General Naming

It is recommended to use the following naming convention for our branches. The general recommendation is to use all lower cased characters, separated by dashes *(aka. hyphen, **i.e. this character in double-quotes: "`-`"**)*.

> *e.g. `branch/this-is-my-branch-name`*

The branch name must be as descriptive, and short as possible. For example, if a branch calls for some gitignore changes, the branch can be named as: **`hotfix/gitignore-update-exclude-libraries`**. Or it can even be shortened to just **`hotfix/gitignore-exclude-libraries`** because it does not really lose it's intended purpose.

#### Branch-Specific Naming

1. **Feature Branch**
	A `feature` branch should always be appended with `feature/` followed by the branch name.
	> *e.g. `feature/this-is-my-branch-name`*
	
	A `feature` that is tied to an user story (almost always), should start with the user story prefix and number. In our case, almost all user stories begin with **us** followed by the number.
	> *e.g. `feature/us1234-my-branch-name`*
  
2. **Hotfix Branch**
	A `hotfix` branch should always be appended with `hotfix/` followed by the branch name.
	> *e.g. `hotfix/this-is-my-branch-name`*
	
4. **Release Branch**
	A `release` branch should always be appended with `release/` followed by the branch name, which is the sprint name/ID formatted as `sprint` followed by a dash/hyphen, (`-`), and the numbered ID as provided by Costco.
	> *e.g. `release/sprint-00.00`*
	
	In the example above, `00.00` is the sprint ID provided by Costco. The first number is the year, and the second number is a sprint number. For instance, **sprint 11** in the year **2021** will have a sprint ID of **21.11**, which would be used in naming the branch.
	> *i.e. `release/sprint-21.11`*

## Coding Guide

Note: This portion will be updated when necessary.<br>
[File Naming](#file-naming-convention) | [Structure](#source-structure)

### File Naming Convention

1. Use lowercase characters
2. Use dashes (`-`) to separate words.
   > *e.g.* Tire Center ➤ `tire-center`
3. Do not use PascalCase or camelCase.
4. Do not use underscores (`_`).
5. Use dots (`.`) to separate context in a file.
   > *e.g.*<br>
   > Tire Center Component HTML ➤ `tire-center.component.html`<br>
   > User Name service script ➤ `user-name.service.ts`


### Source Structure
[Components](#angular-components) | [Services](#angular-services) | [Models](#angular-models) | [ViewModels](#angular-viewmodels) | [Mappers](#angular-mappers) | [Locales](#angular-locales)

- Everything resides within the `src` directory.
  - The main `index.html` file is in this directory.
  - the main `styles.less` file is in this directory.
- Put assets inside the `src\assets` directory.
- All components will be inside the `app` directory.
- Use your best judgement to create OOP structure.
- For major Features, create a top-level directory.
  > *e.g.*<br>
  > -`src\app\common`<br>
  > -`src\app\administration`<br>
  > -`src\app\tire-center`

<br>
#### Angular Components

- All components reside under `components` subdirectory.
  > *e.g.*<br>
  > `src\app\common\components\component-name-1`<br>
  > `src\app\common\components\component-name-2`
- Create a directory for each component.
  > *e.g.* `src\app\common\components\component-name-1\file-name.component.extension`
- Each component directory should have four (4) files.
    1. Markup (HTML) `component-name.component.html`
    2. Script (TS) `component-name.component.ts`
    3. Style (LESS) `component-name.component.less`
    4. Test (TS) `component-name.component.spec.ts`
- Only component-specific code are allowed inside the script file. For most things, put it in a [service script file](#angular-services).


#### Angular Services

- A service contains business logic code.
- All services must reside under `services` subdirectory.
- Services should have a test (spec) file.
- Directory structure is flat.
- Follow the following naming convention: `service-name.service.ts` / `service-name.service.spec.ts`
  > *e.g.*<br>
  > `src\app\common\services\service-name-1.service.ts`<br>
  > `src\app\common\services\service-name-1.service.spec.ts`<br>
  > `src\app\common\services\service-name-2.service.ts`<br>
  > `src\app\common\services\service-name-2.service.spec,ts`

#### Angular Models

- A model is defined by a web service JSON response.
- Use a [viewmodel](#angular-viewmodels) for use in components.
- All models must reside under `models` subdirectory.
- Directory structure is flat.
- Follow the following naming convention: `model-name.model.ts`
  > *e.g.*<br>
  > `src\app\common\models\model-name-1.model.ts`<br>
  > `src\app\common\models\model-name-2.model.ts`
- The properties' names might not adhere to ESLint naming conventions.

#### Angular ViewModels

- A viewmodel is used by the components. The reason we are not using models directly is for code-reability and decreased dependency.
- All viewmodels are [mapped](#angular-mappers) from the Models.
- The properties **should** must adhere ESLint naming convention best practices.
- All viewmodels must reside under `viewmodels` subdirectory.
- Directory structure is flat.
- Follow the following naming convention: `viewmodel-name.viewmodel.ts`
  > *e.g.*<br>
  > `src\app\common\viewmodels\viewmodel-name-1.viewmodel.ts`<br>
  > `src\app\common\viewmodels\viewmodel-name-2.viewmodel.ts`

#### Angular Mappers

- A mapper is a type of code used to map a model to a viewmodel.
- All viewmodels must reside under `mappers` subdirectory.
- Directory structure is flat.
- Follow the following naming convention: `mapper-name.mapper.ts`
  > *e.g.*<br>
  > `src\app\common\mappers\mapper-name-1.mapper.ts`<br>
  > `src\app\common\mappers\mapper-name-2.mapper.ts`

#### Angular Locales

- The solution adheres to [internationalization (i18n)](https://angular.io/guide/i18n) process.
- The default language files are located in the following directory: `src\locale\`
  > *e.g.*<br>
  > `src\locale\messages.en-CA.xlf`<br>
  > `src\locale\messages.fr-CA.xlf`<br>
  > `src\locale\messages.xlf`

<br>

### Code Standards

Use your best judgement in implementing best practices. Implement OOP practices whenever possible.

[TypeScript](#typescript-coding-standards) | [HTML](#branch-specific-naming) | [LESS/CSS](#lesscss-coding-standards)

#### TypeScript Coding Standards
- **Linting** - Use [ESLint](https://eslint.org/).
Highly Recommened: [ESLint Plugin](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) for Visual Studio Code.
- **Documentation** - Use [TSDoc](https://tsdoc.org/)
- Do not use double-quotes (`"`) for literals. Use backticks (`` ` ``) or single-quotes (`'`). Be consistent.

#### HTML Coding Standards
- Use HTML5 find when possible.
- Follow the [Angular developer guides and best practices](https://angular.io/start).
- Avoid inline CSS styles.
- Follow [this guide](https://www.w3schools.com/html/html5_syntax.asp) for conventions.

#### LESS/CSS Coding Standards
- Do not use Bootstrap or any third-party layout library.
- Use component-level CSS (LESS).
  - Do not use everything from the main `styles.less` file.
- **Inherit** from the main `styles.less` (LESS).
- Prioritize Flexbox over Media Queries.
- Naming Convention:
  > `.class-name` ✓ Use dashes.<br>
  > `.class_name` ✗ Don't use underscores.<br>
  > `.className` ✗ Don't use camelCase.<br>
  > `.ClassName` ✗ Don't use PascalCase.<br>


<!-- CONTACT -->
## Contact

Jay Mendoza - [@jaymendoza](mailto:jaymendoza@costco.com)<br>
Carlos Menjivar - [@cmenjivar](mailto:cmenjivar@costco.com)

Project Link: [https://dev.azure.com/costcocloudops/Tire%20Center%20Modernization/_git/tires-spa](https://dev.azure.com/costcocloudops/Tire%20Center%20Modernization/_git/tires-spa)
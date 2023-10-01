# Angular + Single Spa

> This project contains a basic structure for microfontends using single spa and angular

## Table of contents

- [Folder structure](#folder-structure)
- [Creating the application](#creating-the-application)
    - [Root](#root)
    - [Sidebar](#sidebar)

## Folder structure
```
|- root
```

- root: contains the single spa application

## Creating the application

### Root

> Run this command in the terminal and answer the configuration questions shown
```shell
npm init single-spa
```
<img src="assets/creating-root-application.png" alt="Creating root application"/>

### Sidebar

> Run this command in the terminal and answer the configuration questions shown
```shell
ng new sidebar
```
<img src="assets/creating-sidebar-application.png" alt="Creating sidebar application"/>

<br />
<br />

> Run this command to add the single spa in the sidebar application inside the sidebar folder
```shell
ng add single-spa-angular
```
<img src="assets/adding-single-spa-sidebar.png" alt="Adding sinle spa to sidebar application"/>
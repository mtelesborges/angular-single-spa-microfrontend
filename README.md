# Angular + Single Spa

> This project contains a basic structure for microfontends using single spa and angular

## Table of contents

- [How to execute](#how-to-execute)
- [Folder structure](#folder-structure)
- [How to reproduce application development](#how-to-reproduce-application-development)
    - [Root](#root)
    - [Sidebar](#sidebar)
    - [Sample app 1](#sample-app-1)
    - [Sample app 2](#sample-app-2)

## How to use

> For running the application, in different terminals, run the above command within all project folder: root, sidebar, sample-app1 and sample-app2
```shell
yarn start
```

> So, open this url in the browser [http://localhost:9000](http://localhost:9000)
## Folder structure
```
|- root
|- sample-app1
|- sample-app2
|- sidebar
```

- root: contains the single spa application
- sample-app1: contains the sample app 1 application
- sample-app2: contains the sample app 2 application
- sidebar: contains the sidebar application

## How to reproduce application development

### Root

> Run this command in the terminal and answer the configuration questions shown
```shell
npm init single-spa
```
<img src="assets/creating-root-application.png" alt="Creating root application"/>

### Sidebar

> Run this command in the terminal and answer the configuration questions shown
```shell
ng new sidebar --prefix sidebar
```
<img src="assets/creating-sidebar-application.png" alt="Creating sidebar application"/>

<br />

> Run this command to add the single spa in the sidebar application inside the sidebar folder
```shell
ng add single-spa-angular
```
<img src="assets/adding-single-spa-sidebar.png" alt="Adding sinle spa to sidebar application"/>

### Sample app 1
> Run this command in the terminal and answer the configuration questions shown
```shell
ng new sample-app1 --prefix sample-app1
```
<img src="assets/creating-sample-app1-application.png" alt="Creating sample app 1 application"/>

<br />

> Run this command to add the single spa in the sample app 1 application inside the sample-app1 folder
```shell
ng add single-spa-angular
```
<img src="assets/adding-single-spa-sample-app1.png" alt="Adding sinle spa to sample app 1 application"/>

### Sample app 2
> Run this command in the terminal and answer the configuration questions shown
```shell
ng new sample-app2 --prefix sample-app2
```
<img src="assets/creating-sample-app2-application.png" alt="Creating sample app 2 application"/>

<br />

> Run this command to add the single spa in the sample app 2 application inside the sample-app2 folder
```shell
ng add single-spa-angular
```
<img src="assets/adding-single-spa-sample-app2.png" alt="Adding sinle spa to sample app 2 application"/>

## Configurations

> In each project (sidebar, sample-app1 and sample-app2) update the AppRoutingModule adding APP_BASE_HREF

```typescript
providers: [
  { provide: APP_BASE_HREF, useValue: '/' },
]
```

> In each project (sidebar, sample-app1 and sample-app2) add EmptyComponent configuration for 404 routes

```typescript
// Update AppModule
@NgModule({
  declarations: [
    EmptyRouteComponent,
    // ...
  ],
  imports: [
    BrowserModule,
    AppRoutingModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

```typescript
// Update AppRoutingModule
const routes: Routes = [
  { path: '**', component: EmptyRouteComponent },
  // ...
];
```
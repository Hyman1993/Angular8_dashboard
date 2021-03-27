# Dashboard (2021.01.22 ~ 2021.03.28)

This project was learned from [Angular 8 Admin Dashboard Panel from scratch using Angular Material, highcharts and flex-layout.](https://youtu.be/FP7Hs8lTy1k)

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## App Image
![Dashboard](https://github.com/Hyman1993/Angular8_dashboard/blob/master/app-image.png)

## The problems I met 

1.error:
    Error occurs in the template of component DashboardComponent.
    src/app/modules/dashboard/dashboard.component.html:17:9 - error NG8001: 'app-widget-card' is not a known element:
    1. If 'app-widget-card' is an Angular component, then verify that it is part of this module.
    2. If 'app-widget-card' is a Web Component then add 'CUSTOM_ELEMENTS_SCHEMA' to the '@NgModule.schemas' of this component to suppress this message.

  原因分析及对策:app-widget-card这个组件是属于shared模块的，但是在layout模块里面用了它，因此需要将app-widget-card这个组件从shared模块中导出


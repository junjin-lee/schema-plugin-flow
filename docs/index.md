---
hero:
  title: schema-plugin-flow
  desc: A highly extensible JavaScript library, abbreviated as Sifo.
  actions:
    - text: Guideline 
      link: /guide
features:
    - title: Schema
      desc: schema to describe page's structures
    - title: Plugins
      desc: modelPlugins、pagePlugins、componentPlugins as logic controller
    - title: Extensions
      desc: to extend business logic and page layout without touching source code
footer: Open-source MIT Licensed
---

## Introduction
schema-plugin-flow, abbreviated as Sifo ([sɪfɔ])，is a highly extensible JavaScript library. This library allows developers to extend business logic and page layout without touching source code, when the source code is written in Sifo.

* `sifo-model` is the core of Sifo, which using JSON (as Schema) to describe page's structures and using plugins as logic controller. There are three kinds of plugin: modelPlugin、pagePlugin and componentPluign. You can learn about Sifo's basic information and the usage patterns by reading this package's README.
* `sifo-react` is a React Component encapsulates sifo-model and sifo-singleton. sifo-react also support `sifoAppDecorator`, with which a normal React Commponent will has extension ability. You can learn about that via package's README or online demos.
* `sifo-vue` is a Vue Component encapsulates sifo-model and sifo-singleton. sifo-vue also support `sifoAppDecorator`, with which a normal Vue Commponent will has extension ability. You can learn about that via package's README or online demos.
* `sifo-singleton` is a global extensions holder. All kinds of extend-plugins and extend-components are registered to it.

### modelPlugins
* `sifo-mplg-react-optimize` is a modelPlugin for React optimize.
* `sifo-mplg-form-core` is a sifo form-core model plugin. This model plugin, basing on simple schema setting, realized the form fields' control and supplied form operations with a serial of api.
* `sifo-mplg-form-antdv` is a sifo form with ant-design-vue, works with sifo-mplg-form-core and sifo-vue.
* `sifo-mplg-form-antd` is a sifo form with ant-design, works with sifo-mplg-form-core and sifo-react.

## Installation

```shell
$ npm i @schema-plugin-flow/sifo-model --save
$ npm i @schema-plugin-flow/sifo-react --save
$ npm i @schema-plugin-flow/sifo-vue --save
```

## Try in local
* React
  *  clone code and start
  ```shell
  $ git clone https://github.com/alibaba/schema-plugin-flow.git
  $ cd schema-plugin-flow
  $ npm run i
  $ npm run start
  ```
  *  then visit `http://localhost:8000`.

* Vue
  *  clone code and start
  ```shell
  $ git clone https://github.com/alibaba/schema-plugin-flow.git
  $ cd schema-plugin-flow
  $ npm run i
  $ npm run i-vue
  $ npm run start-vue
  ```
  *  then visit `http://localhost:8080`.

## Try online (codesandbox.io)
* sifo-react
  * [sifo-react-quick-start](https://codesandbox.io/s/sifo-react-quick-start-lhmyu)    
  * [sifo-react-decorator](https://codesandbox.io/s/sifo-react-test-decorator-sef79)    
  * [sifo-mplg-form-antd](https://codesandbox.io/s/sifo-react-form-antd-o0hoq)     
  * [sifo-react-mplg-optimize](https://codesandbox.io/s/sifo-react-mplg-optimize-sfmts)    

* sifo-vue
  * [sifo-vue-quick-start](https://codesandbox.io/s/sifo-vue-quick-start-7668x)    
  * [sifo-vue-decorator](https://codesandbox.io/s/sifo-vue-test-decorator-4b9j4)    
  * [sifo-vue-use-optimize](https://codesandbox.io/s/sifo-vue-use-optimize-4n6nz)    
  * [sifo-mplg-form-antdv](https://codesandbox.io/s/sifo-vue-form-antdv-q4yc4)    


## SifoApp (sifo-react/sifo-vue) Demo
In this demo, there are seven extend-plugins in seven independent js. The checkbox set which plugin should be registered. Each plugin control different logic and all registered plugins make up a integrated page.    

  ![demo](https://img.alicdn.com/tfs/TB1HOQYe6MZ7e4jSZFOXXX7epXa-1264-698.gif)
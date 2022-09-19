# Tezjs with Ant Design Vue

- Ant-Design-Vue is an enterprise-class UI design language for web applications.

- A set of high-quality Vue components out of the box.

- We can use Ant-Design-Vue with the Tezjs through the below steps.

- Create fresh tezjs project

```
 npm create tez@latest
```


- Install package for **Ant-Design-Vue**

```
 npm install ant-design-vue --save
```

- Now add it as a plugin, make a plugins directory and add index.ts inside it and add the below code


```
/plugins/index.ts

import Antd from "ant-design-vue"; 
```
- make one export default funciton and add imported modules inside it just as below.

```
export default function(vue:any){
    vue.use(Antd)
}
```

- It's done with tezjs. Now, you can use it inside your project.

- In current project all components and pages are designed with an Ant-Design-Vue framework.

- **Note :** For more Understanding about Ant-Design-Vue read it's docs here https://2x.antdv.com/components/overview/


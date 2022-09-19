<template>
<div style="padding:0 ">

  <a-layout style="padding:0">
    <a-page-header style="background-color:white; padding:0;min-width: 375px;">
      
      <a-row  justify="space-between">
        <a-col :span="2">
        <a-image
          style="width: 45px; height: 55px; margin-left: 20px;"
          src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg"
        />
          
        </a-col>
        <a-col  :span="8" style="margin-right: 0px;">
            <a-menu
              theme="light"
              mode="horizontal"
              :style="{ lineHeight: '64px', borderBottom : '0px'}"
            >
              <a-menu-item key="1" >
                <tez-link to="/"> Home </tez-link>
              </a-menu-item>
              <a-menu-item key="2">
                <tez-link to="/ant-design"> Ant Design Form </tez-link>
                </a-menu-item>
              <a-menu-item key="3">
                  <a href="https://github.com/tezjs/tezjs" >TezJs </a>
                
              </a-menu-item>
            </a-menu>
        </a-col>
      </a-row>
    </a-page-header>
   
  </a-layout>
</div>
</template>

<script>

</script>

<style>
.ant-page-header{
  border-bottom: solid silver 1px;
}
.ant-page-header-content {
  padding-top: 0px;
  
}

.ant-layout {
background: white;
}
</style>
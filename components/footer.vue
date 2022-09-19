<template>
<div>
    <a-layout-footer style="text-align: center; min-width: 375px;">
      <a-row  justify="space-between">
        <a-col>
          <span>
          Copyright © 2022 TezJS.  
          </span>
        </a-col>
        <a-col>
          <div class="icons-list">
            <a href="https://github.com/tezjs/tezjs" style="color:gray ">
              Github
              <GithubOutlined style="font-size:20px" /> 
              </a>
          </div>
        </a-col>
      </a-row>
    </a-layout-footer>
</div>

</template>
<script>
import { defineComponent } from 'vue';
import {GithubOutlined} from '@ant-design/icons-vue';
export default defineComponent({
    components:{
      GithubOutlined
    },
});
</script>
<style>
.ant-layout-footer {
  padding: 24px 0;
  background:white;
  border-top:solid silver 1px ;
}
a:hover{
  color: black;
}

</style>
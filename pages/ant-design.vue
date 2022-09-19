<script>
import { defineComponent, reactive, ref, toRaw } from "vue";
export default defineComponent({
  layoutName: "default",
  head: {
    title: "tezjs:Ant Design Vue",
  },
  setup() {
    const formRef = ref();
    const formState = reactive({
      name: "",
      region: undefined,
      date1: undefined,
      delivery: false,
      type: [],
      resource: "",
      desc: "",
    });
    const rules = {
      name: [
        {
          required: true,
          message: "Please insert name",
          trigger: "blur",
        },
        {
          min: 3,
          max: 5,
          message: "Length should be 3 to 5",
          trigger: "blur",
        },
      ],
      region: [
        {
          required: true,
          message: "Please select Activity zone",
          trigger: "change",
        },
      ],
      date1: [
        {
          required: true,
          message: "Please pick a date",
          trigger: "change",
          type: "object",
        },
      ],
      type: [
        {
          type: "array",
          required: true,
          message: "Please select at least one activity type",
          trigger: "change",
        },
      ],
      resource: [
        {
          required: true,
          message: "Please select activity resource",
          trigger: "change",
        },
      ],
      desc: [
        {
          required: true,
          message: "Please enter activity description",
          trigger: "blur",
        },
      ],
    };

    const onSubmit = () => {
      formRef.value
        .validate()
        .then(() => {
          console.log("values", formState, toRaw(formState));
        })
        .catch((error) => {
          console.log("error", error);
        });
    };

    const resetForm = () => {
      formRef.value.resetFields();
    };

    return {
      formRef,
      labelCol: {
        span: 4,
      },
      wrapperCol: {
        span: 14,
      },
      other: "",
      formState,
      rules,
      onSubmit,
      resetForm,
    };
  },
});
</script>

<template>
  <div>
    <a-form
      ref="formRef"
      :model="formState"
      :rules="rules"
      :label-col="labelCol"
      :wrapper-col="wrapperCol"
      style="padding: 50px 30px; min-width: 375px"
    >
      <a-form-item ref="name" label="User Name" name="name">
        <a-input v-model:value="formState.name" />
      </a-form-item>
      <a-form-item label="Activity zone" name="region">
        <a-select v-model:value="formState.region" placeholder="please select your zone">
          <a-select-option value="Ahmedabad">Ahmedabad</a-select-option>
          <a-select-option value="Surat">Surat</a-select-option>
        </a-select>
      </a-form-item>
      <a-form-item label="Activity time" required name="date1">
        <a-date-picker v-model:value="formState.date1" show-time type="date" placeholder="Pick a date" style="width: 100%" />
      </a-form-item>
      <a-form-item label="Instant delivery" name="delivery">
        <a-switch v-model:checked="formState.delivery" />
      </a-form-item>
      <a-form-item label="Activity type" name="type">
        <a-checkbox-group v-model:value="formState.type">
          <a-checkbox value="1" name="type">Online</a-checkbox>
          <a-checkbox value="2" name="type">Promotion</a-checkbox>
          <a-checkbox value="3" name="type">Offline</a-checkbox>
        </a-checkbox-group>
      </a-form-item>
      <a-form-item label="Resources" name="resource">
        <a-radio-group v-model:value="formState.resource">
          <a-radio value="1">Sponsor</a-radio>
          <a-radio value="2">Venue</a-radio>
        </a-radio-group>
      </a-form-item>
      <a-form-item label="Activity" name="desc">
        <a-textarea placeholder="Description" v-model:value="formState.desc" />
      </a-form-item>
      <a-form-item :wrapper-col="{ span: 14, offset: 4 }">
        <a-button type="primary" @click="onSubmit">Create</a-button>
        <a-button style="margin-left: 10px" @click="resetForm">Reset</a-button>
      </a-form-item>
    </a-form>
  </div>
</template>
<script></script>

<style>
@media (max-width: 1030px) {
  .ant-form-item .ant-form-item-label {
    padding: 0 0 8px;
    line-height: 1.5715;
    white-space: initial;
    text-align: left;
  }

  .ant-form-item-label {
    display: inline-block;
    flex-grow: 0;
    overflow: hidden;
    white-space: nowrap;
    text-align: right;
    vertical-align: middle;
  }

  .ant-form .ant-form-item .ant-form-item-label,
  .ant-form .ant-form-item .ant-form-item-control {
    flex: 0 0 100%;
    max-width: 100%;
  }
}
</style>

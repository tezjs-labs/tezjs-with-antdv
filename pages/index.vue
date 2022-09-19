<script >

export default {
  layoutName:'default',
  head: {
    title: "tezjs: starter vue project",
  },
};
</script>
<template>
<div >
   <a-layout-content style="align-content: center;min-width: 375px;">
     <h1 
     style="
            text-align: center;
            font-size: 40px;
            font-weight: bolder;
            margin: 0 auto;
            margin-top: 30px;
            display: block;"
            >
          Build ultra-modern, super-fast, secure, and scalable websites
        </h1>
        <p  style="font-size: x-large; margin: 20px auto; text-align:center;">
          The fastest and future-proof framework that enables developers to build blazing-fast websites.
        </p>

        <div style="margin-top: 40px;">

        <a-row>
          <a-col :lg="24" :xl="12" >
            <a-row type="flex">
              <a-col :span="2" >
                <div class="description-logo" >

                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="2"
                  stroke="currentColor"
                  aria-hidden="false"
                  style="height:25px ; padding:0 10px"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"
                  ></path>
                </svg>
                </div>
                
              </a-col>
              <a-col :span="22" style="padding:0 10px">
                <p class="title-text">An Open-Source Framework with Endless Possibilities</p>
                <p class="description-text">The primary goal of TezJS is to improve core web vitals without compromising the user experience. This provides endless possibilities for every team member</p>
              </a-col>
            </a-row>
          </a-col>


          <a-col :lg="24" :xl="12">
            <a-row type="flex">
              <a-col :span="2">
                <div class="description-logo">
                  <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="2"
                  stroke="currentColor"
                  aria-hidden="true"
                  style="height:25px"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M3 6l3 1m0 0l-3 9a5.002 5.002 0 006.001 0M6 7l3 9M6 7l6-2m6 2l3-1m-3 1l-3 9a5.002 5.002 0 006.001 0M18 7l3 9m-3-9l-6-2m0-2v2m0 16V5m0 16H9m3 0h3"
                  ></path>
                </svg>
                </div>
              </a-col>
              <a-col :span="22" style="padding:0 10px">
                <p class="title-text">Development and Deployment in the Blink of an Eye</p>
                <p class="description-text">The incredible community, broad ecosystem, headless framework, and component-driven architecture of TezJS help you develop and deploy your website in minutes.</p>
              </a-col>
            </a-row>
          </a-col>
        </a-row>

        <a-row>
          <a-col :lg="24" :xl="12">
            <a-row type="flex">
              <a-col :span="2">
                <div class="description-logo">
                  <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="2"
                  stroke="currentColor"
                  aria-hidden="true"
                  style="height:25px"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M13 10V3L4 14h7v7l9-11h-7z"
                  ></path>
                </svg>
                </div>
              </a-col>
              <a-col :span="22" style="padding:0 10px">
                <p class="title-text">Short Page Load Time for Amazing User Experience</p>
                <p class="description-text">When every millisecond counts and every byte is precious, you must ensure that you’re only loading the data your users need. TezJS lets you load only the required data which is asked.</p>
              </a-col>
            </a-row>
          </a-col>
          <a-col :lg="24" :xl="12">
            <a-row type="flex" >
              <a-col :span="2">
                <div class="description-logo">
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke-width="2"
                      stroke="currentColor"
                      aria-hidden="true"
                      style="height:25px"
                    >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"
                    ></path>
                </svg>
                </div>
              </a-col>
              <a-col :span="22" style="padding:0 10px">
                <p class="title-text">Combine Data and Create Rich Web Experiences</p>
                <p class="description-text">TezJS has a common data layer that makes it simple for developers to combine data from various sources and render it side by side. It’s easy to consistently add content to your site from Strapi, etc.</p>
              </a-col>
            </a-row>
          </a-col>

        </a-row>
      </div>
    </a-layout-content>
</div>
  
</template>

<style >
body{
  color: #555555;
  
}

.title-text{
    font-size: 22px;
    font-weight:bold;
}

.description-text {
    font-size: 18px;
    color: rgb(91, 88, 88);
    font-weight: normal;
}

.description-logo {
    background-color: #6366f1;
    border-radius: 0.5rem;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    width: 45px;
    height: 45px;
    flex: 0 0 auto;
    flex-wrap: wrap;
    margin-right: 20px;
}
</style>
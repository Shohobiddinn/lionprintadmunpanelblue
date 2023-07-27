<template>
    <div>
      <div class="login_page">
        <div class="container">
          <div class="login_page_content">
            <div class="login_page_content_logo">
              <img src="../assets/images/g10 (1).png" alt="logo" />
            </div>
            <div class="login_page_content_title">Sing in</div>
            <div class="login_page_content_inputs">
              <div class="login_page_content_inputs_input">
                <input type="text" v-model="username" placeholder="Username" />
                <input
                  type="password"
                  v-model="password"
                  @keyup.enter="loginApi"
                  placeholder="Password"
                />
              </div>
            </div>
            <div class="login_page_content_icon" @click="loginApi()">Login</div>
          </div>
        </div>
      </div>
    </div>
  </template>
      
  <script setup>
  definePageMeta({
    layout: "login",
  });
  const router = useRouter();
  if (localStorage.getItem("userToken")) {
    router.push("/");
  }
  const baseUrl = useRuntimeConfig().public.baseUrl;
  const login = ref(null);
  const username = ref("");
  const password = ref("");
  async function loginApi() {
    const data = await $fetch(baseUrl + "/auth/login", {
      method: "POST",
      body: JSON.stringify({
        username: username.value,
        password: password.value,
      }),
    });
    login.value = data;
    localStorage.setItem("userToken", data.result.token);
    router.push("/");
    console.log(data, "salom");
  }
  </script>
  
  
<template>
  <div>
    <div class="page_information">
      <div class="container">
        <div class="index_page_info">
          <div class="categories">
            <div class="categorie">
              <input type="radio" id="cat-1" name="categorie" />
              <label for="cat-1"> ishlayotgan </label>
            </div>
            <div class="categorie">
              <input type="radio" id="cat-2" name="categorie" />
              <label for="cat-2"> rad etilgan </label>
            </div>
          </div>
          <div class="peoples">
            <div class="peoples_nav">
              <div class="peoples_nav_icons">
                <div class="peoples_nav_icons_add">
                  <div class="peoples_nav_icons_add_plus item">
                    <NuxtLink class="item" to="new">
                      <div class="peoles_nav_icons_add_plus_icon item_icon">
                        <svg
                          width="20"
                          height="20"
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <path
                            d="M256 80c0-17.7-14.3-32-32-32s-32 14.3-32 32V224H48c-17.7 0-32 14.3-32 32s14.3 32 32 32H192V432c0 17.7 14.3 32 32 32s32-14.3 32-32V288H400c17.7 0 32-14.3 32-32s-14.3-32-32-32H256V80z"
                          />
                        </svg>
                      </div>
                      <div class="peoles_nav_add_plus_title item_title">
                        qo'shish
                      </div>
                    </NuxtLink>
                  </div>
                  <div class="peoples_nav_add_edit item">
                    <div class="peoles_nav_add_edit_icon item_icon">
                      <svg
                        width="20"
                        height="20"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 512 512"
                      >
                        <path
                          d="M362.7 19.3L314.3 67.7 444.3 197.7l48.4-48.4c25-25 25-65.5 0-90.5L453.3 19.3c-25-25-65.5-25-90.5 0zm-71 71L58.6 323.5c-10.4 10.4-18 23.3-22.2 37.4L1 481.2C-1.5 489.7 .8 498.8 7 505s15.3 8.5 23.7 6.1l120.3-35.4c14.1-4.2 27-11.8 37.4-22.2L421.7 220.3 291.7 90.3z"
                        />
                      </svg>
                    </div>
                  </div>
                  <div class="peoples_nav_add_minus item">
                    <div class="peoles_nav_add_minus_icon item_icon">
                      <svg
                        width="20"
                        height="20"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 448 512"
                      >
                        <path
                          d="M432 256c0 17.7-14.3 32-32 32L48 288c-17.7 0-32-14.3-32-32s14.3-32 32-32l352 0c17.7 0 32 14.3 32 32z"
                        />
                      </svg>
                    </div>
                  </div>
                </div>
                <div class="peoples_nav_icons_block">
                  <div class="peoples_nav_icons_block_item">
                    <div class="peoples_nav_icons_block_item_icon">
                      <svg
                        width="15"
                        height="15"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 448 512"
                      >
                        <path
                          d="M144 144v48H304V144c0-44.2-35.8-80-80-80s-80 35.8-80 80zM80 192V144C80 64.5 144.5 0 224 0s144 64.5 144 144v48h16c35.3 0 64 28.7 64 64V448c0 35.3-28.7 64-64 64H64c-35.3 0-64-28.7-64-64V256c0-35.3 28.7-64 64-64H80z"
                        />
                      </svg>
                    </div>
                  </div>
                  <div class="peoples_nav_icons_block_item"></div>
                  <div class="peoples_nav_icons_block_item_icon">
                    <svg
                      width="15"
                      height="15"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 576 512"
                    >
                      <path
                        d="M352 144c0-44.2 35.8-80 80-80s80 35.8 80 80v48c0 17.7 14.3 32 32 32s32-14.3 32-32V144C576 64.5 511.5 0 432 0S288 64.5 288 144v48H64c-35.3 0-64 28.7-64 64V448c0 35.3 28.7 64 64 64H384c35.3 0 64-28.7 64-64V256c0-35.3-28.7-64-64-64H352V144z"
                      />
                    </svg>
                  </div>
                </div>
                <div class="peoples_nav_icons_messeges">
                  <div class="peoples_nav_icons_messeges_messege">
                    <div class="peoples_nav_icons_messeges_messege_icon">
                      <svg
                        width="15"
                        height="15"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 512 512"
                      >
                        <path
                          d="M64 0C28.7 0 0 28.7 0 64V352c0 35.3 28.7 64 64 64h96v80c0 6.1 3.4 11.6 8.8 14.3s11.9 2.1 16.8-1.5L309.3 416H448c35.3 0 64-28.7 64-64V64c0-35.3-28.7-64-64-64H64z"
                        />
                      </svg>
                    </div>
                  </div>
                  <div class="peoples_nav_icons_messeges_messege">
                    <div class="peoples_nav_icons_messeges_messege_icon">
                      <svg
                        width="15"
                        height="15"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 512 512"
                      >
                        <path
                          d="M164.9 24.6c-7.7-18.6-28-28.5-47.4-23.2l-88 24C12.1 30.2 0 46 0 64C0 311.4 200.6 512 448 512c18 0 33.8-12.1 38.6-29.5l24-88c5.3-19.4-4.6-39.7-23.2-47.4l-96-40c-16.3-6.8-35.2-2.1-46.3 11.6L304.7 368C234.3 334.7 177.3 277.7 144 207.3L193.3 167c13.7-11.2 18.4-30 11.6-46.3l-40-96z"
                        />
                      </svg>
                    </div>
                  </div>
                </div>
                <div class="peoples_nav_icons_filters">
                  <div class="peoples_nav_icons_filters_icon">
                    <svg
                      width="15"
                      height="15"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 512 512"
                    >
                      <path
                        d="M3.9 54.9C10.5 40.9 24.5 32 40 32H472c15.5 0 29.5 8.9 36.1 22.9s4.6 30.5-5.2 42.5L320 320.9V448c0 12.1-6.8 23.2-17.7 28.6s-23.8 4.3-33.5-3l-64-48c-8.1-6-12.8-15.5-12.8-25.6V320.9L9 97.3C-.7 85.4-2.8 68.8 3.9 54.9z"
                      />
                    </svg>
                  </div>
                  <div class="peoples_nav_icons_filters_title">
                    <span></span><span></span><span></span>
                  </div>
                </div>
              </div>
              <div class="peoples_nav_content">
                <div
                  class="peoples_nav_content_departaments"
                  :class="{ active: deparModal }"
                >
                  <div
                    class="departament_option"
                    @click="deparModal = !deparModal"
                  >
                    <div class="departament_option_all_icon">
                      <span></span><span></span><span></span>
                    </div>
                    <div class="departament_option_title">
                      <!-- <input type="text" placeholder="bo'lim" /> -->
                      bo'lim
                    </div>
                    <div class="departament_option_icon">
                      <svg
                        width="15"
                        height="10"
                        viewBox="0 0 20 10"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M10 0.00022316C10.8076 0.00022316 11.6152 0.311733 12.2267 0.923214L19.7491 8.44553C20.0836 8.78012 20.0836 9.33391 19.7491 9.6685C19.4145 10.0031 18.8607 10.0031 18.5261 9.6685L11.0038 2.14617C10.45 1.59238 9.55006 1.59238 8.99627 2.14617L1.4739 9.6685C1.13931 10.0031 0.58552 10.0031 0.250937 9.6685C-0.0836468 9.33391 -0.0836468 8.78012 0.250937 8.44553L7.7733 0.923214C8.38478 0.311733 9.1924 0.00022316 10 0.00022316Z"
                          fill="#8FA8C7"
                        />
                      </svg>
                    </div>
                  </div>
                  <div class="departament_content">
                    <div
                      class="departament_content_title"
                      v-for="c in 4"
                      :key="c"
                      @click="deparModal = false"
                    >
                      it generator
                    </div>
                  </div>
                </div>
                <div class="peoples_nav_content_search">
                  <div class="peoples_nav_content_search_icon">
                    <svg
                      width="18"
                      height="18"
                      viewBox="0 0 30 31"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M14.3037 28.6074C6.41923 28.6074 0 22.1882 0 14.3037C0 6.41923 6.41923 0 14.3037 0C22.1882 0 28.6074 6.41923 28.6074 14.3037C28.6074 22.1882 22.1882 28.6074 14.3037 28.6074ZM14.3037 2.09323C7.56353 2.09323 2.09323 7.57748 2.09323 14.3037C2.09323 21.03 7.56353 26.5142 14.3037 26.5142C21.0439 26.5142 26.5142 21.03 26.5142 14.3037C26.5142 7.57748 21.0439 2.09323 14.3037 2.09323Z"
                        fill="#8FA8C7"
                      />
                      <path
                        d="M28.9569 30.0029C28.6918 30.0029 28.4266 29.9052 28.2173 29.6959L25.4263 26.9049C25.0216 26.5002 25.0216 25.8304 25.4263 25.4257C25.831 25.021 26.5008 25.021 26.9055 25.4257L29.6965 28.2167C30.1012 28.6214 30.1012 29.2912 29.6965 29.6959C29.4872 29.9052 29.222 30.0029 28.9569 30.0029Z"
                        fill="#8FA8C7"
                      />
                    </svg>
                  </div>
                  <div class="peoples_nav_content_search_input">
                    <input type="text" placeholder="qidirmoq..." />
                  </div>
                </div>
              </div>
            </div>
            <div class="peoples_users">
              <div class="peoples_users_nav">
                <div class="item">№</div>
                <div class="item">F.I.O</div>
                <div class="item">
                  <svg
                    width="15"
                    height="15"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                  >
                    <path
                      d="M144 144v48H304V144c0-44.2-35.8-80-80-80s-80 35.8-80 80zM80 192V144C80 64.5 144.5 0 224 0s144 64.5 144 144v48h16c35.3 0 64 28.7 64 64V448c0 35.3-28.7 64-64 64H64c-35.3 0-64-28.7-64-64V256c0-35.3 28.7-64 64-64H80z"
                    />
                  </svg>
                </div>
                <div class="item">bo'lim</div>
                <div class="item">lavozim</div>
                <div class="item">jadval</div>
                <div class="item">ishga keldi</div>
                <div class="item">ishdan ketdi</div>
                <div class="item">kechikkan vaqti</div>
                <div class="item">surat</div>
              </div>
              <div class="peoples_users_user" v-for="p in peoples" :key="p?.id">
                <div class="user_no user">
                  {{ p?.id }}
                </div>
                <div class="user_name user">
                  {{ p?.firstName }} {{ p?.lastName }}
                </div>
                <div class="user_block user"></div>
                <div class="user_departament user">
                  {{ p?.department?.name }}
                </div>
                <div class="user_position user">{{ p?.job?.name }}</div>
                <div class="user_data user">
                  {{ p?.schedule?.startTime }} {{ p?.schedule?.endTime }}
                </div>
                <div class="user_acces user">
                  {{
                    p?.workingDay == null ? "--:--" : p?.workingDay?.arrivalTime
                  }}
                  <div class="user_icon">
                    <svg
                      width="20"
                      height="20"
                      viewBox="0 0 38 36"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M9.06818 10.8393C9.32091 10.663 9.6386 10.5797 9.97734 10.64C10.6322 10.7566 11.0777 11.3951 10.9611 12.05L8.73373 24.5606L21.2443 26.7879C21.8992 26.9045 22.3447 27.543 22.2281 28.1979C22.1115 28.8528 21.473 29.2983 20.8181 29.1817L7.11069 26.7412C6.4558 26.6246 6.01032 25.9862 6.12692 25.3313L8.56739 11.6238C8.6277 11.2851 8.81545 11.0156 9.06818 10.8393Z"
                        fill="#FCA311"
                      />
                      <path
                        d="M6.85264 24.39L29.2389 8.77028C29.7843 8.38977 30.5521 8.52646 30.9326 9.07182C31.3131 9.61718 31.1764 10.385 30.6311 10.7655L8.24477 26.3852C7.69942 26.7657 6.93162 26.629 6.5511 26.0837C6.17059 25.5383 6.30729 24.7705 6.85264 24.39Z"
                        fill="#FCA311"
                      />
                    </svg>
                  </div>
                </div>
                <div class="user_exit user">
                  {{
                    p?.workingDay == null || p?.workingDay?.exitTime == null
                      ? "--:--"
                      : p?.workingDay?.exitTime
                  }}
                  <div class="user_icon">
                    <svg
                      width="20"
                      height="20"
                      viewBox="0 0 38 36"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M28.2037 24.461C27.9513 24.6378 27.6337 24.7216 27.2949 24.6618C26.6398 24.5463 26.1932 23.9086 26.3088 23.2535L28.5154 10.7392L16.0011 8.53265C15.346 8.41714 14.8995 7.77941 15.015 7.12434C15.1305 6.46926 15.7682 6.02272 16.4233 6.13822L30.1348 8.5559C30.7899 8.67141 31.2364 9.30914 31.1209 9.96422L28.7032 23.6757C28.6434 24.0145 28.4561 24.2843 28.2037 24.461Z"
                        fill="#292D32"
                      />
                      <path
                        d="M30.3966 10.9067L8.0363 26.5636C7.49158 26.945 6.72355 26.8096 6.34213 26.2648C5.96071 25.7201 6.09613 24.9521 6.64086 24.5707L29.0012 8.9138C29.5459 8.53238 30.3139 8.66781 30.6953 9.21253C31.0768 9.75726 30.9413 10.5253 30.3966 10.9067Z"
                        fill="#292D32"
                      />
                    </svg>
                  </div>
                </div>
                <div class="user_lar user">01:25</div>
                <div class="user_image user">
                  <img :src="p?.imageUrl" alt="user" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const deparModal = ref(false);
const baseUrl = useRuntimeConfig().public.baseUrl;
const router = useRouter();
const peoplesNumber = ref(null);
const peoples = ref(null);
async function usersApi() {
  const data = await $fetch(baseUrl + "/employees", {
    method: "GET",
    params: {
      size: 10,
      page: 0,
    },
    headers: {
      Authorization: `Bearer ${localStorage.getItem("userToken")}`,
    },
  });
  peoples.value = data.result;
 peoplesNumber.value = Number(peoples.value.length);
 console.log(peoplesNumber.value);
}
usersApi();
// onMounted(() => {
//   if (!localStorage.getItem("userToken")) {
//     router.push("/login");
//   }
// });
onMounted(() => {
  for(let i = 0; i < peoplesNumber.value; i += 2) {
    document.querySelectorAll('.peoples_users_user')[i].style.background = 'red'
  }
});
</script>

<style lang="scss" scoped>
</style>
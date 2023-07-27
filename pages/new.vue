<template>
  <div>
    <div class="new_account_add">
      <div class="container">
        <div class="new_nav">
          <div class="new_nav_title">xodim qo'shish</div>
          <div class="new_nav_content">
            <div class="new_nav_content_exit">
              <NuxtLink to="/" class="new_nav_content_exit_title">
                xodimlar ro'yhatiga qaytish
              </NuxtLink>
            </div>
            <div class="new_nav_content_save" @click="userAdd">
              o'zgarishlarni saqlash
            </div>
          </div>
        </div>
        <div class="new_bottom">
          <!-- <button @click="tekshiruv()">tekshiruv</button> -->
          <div class="new_bottom_category">
            <div class="category_content">
              <div class="category_content_icon">
                <svg
                  width="30"
                  height="30"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 448 512"
                >
                  <path
                    d="M370.7 96.1C346.1 39.5 289.7 0 224 0S101.9 39.5 77.3 96.1C60.9 97.5 48 111.2 48 128v64c0 16.8 12.9 30.5 29.3 31.9C101.9 280.5 158.3 320 224 320s122.1-39.5 146.7-96.1c16.4-1.4 29.3-15.1 29.3-31.9V128c0-16.8-12.9-30.5-29.3-31.9zM336 144v16c0 53-43 96-96 96H208c-53 0-96-43-96-96V144c0-26.5 21.5-48 48-48H288c26.5 0 48 21.5 48 48zM189.3 162.7l-6-21.2c-.9-3.3-3.9-5.5-7.3-5.5s-6.4 2.2-7.3 5.5l-6 21.2-21.2 6c-3.3 .9-5.5 3.9-5.5 7.3s2.2 6.4 5.5 7.3l21.2 6 6 21.2c.9 3.3 3.9 5.5 7.3 5.5s6.4-2.2 7.3-5.5l6-21.2 21.2-6c3.3-.9 5.5-3.9 5.5-7.3s-2.2-6.4-5.5-7.3l-21.2-6zM112.7 316.5C46.7 342.6 0 407 0 482.3C0 498.7 13.3 512 29.7 512H128V448c0-17.7 14.3-32 32-32H288c17.7 0 32 14.3 32 32v64l98.3 0c16.4 0 29.7-13.3 29.7-29.7c0-75.3-46.7-139.7-112.7-165.8C303.9 338.8 265.5 352 224 352s-79.9-13.2-111.3-35.5zM176 448c-8.8 0-16 7.2-16 16v48h32V464c0-8.8-7.2-16-16-16zm96 32a16 16 0 1 0 0-32 16 16 0 1 0 0 32z"
                  />
                </svg>
              </div>
              <div class="category_content_title">umumiy ma'lumot</div>
            </div>
          </div>
          <div class="new_information">
            <div class="new_information_info">
              <div class="info_title">asosiy ma'lumot</div>
              <div class="info_content">
                <div class="info_content_input">
                  <div class="info_content_input_title">familya</div>
                  <input
                    type="text"
                    v-model="firstName"
                    placeholder="familya"
                  />
                </div>
                <div class="info_content_input">
                  <div class="info_content_input_title">ism</div>
                  <input type="text" v-model="lastName" placeholder="ism" />
                </div>
                <div class="info_content_input">
                  <div class="info_content_input_title">otasining ismi</div>
                  <input
                    type="text"
                    v-model="middleName"
                    placeholder="otasining ismi"
                  />
                </div>
                <div class="info_content_input">
                  <div class="info_content_input_title">telefon raqami</div>
                  <input
                    type="text"
                    v-model="phoneNumber"
                    ref="phone"
                    placeholder="telefon raqami"
                  />
                </div>
                <div class="info_content_input">
                  <div class="gender">
                    <div class="gender_content">
                      <input
                        type="radio"
                        @change="genderInfo($event)"
                        id="gen-1"
                        name="gender"
                      />
                      <label for="gen-1">male</label>
                    </div>
                    <div class="gender_content">
                      <input
                        type="radio"
                        @change="genderInfo($event)"
                        id="gen-2"
                        name="gender"
                      />
                      <label for="gen-2">female</label>
                    </div>
                  </div>
                </div>
                <div class="info_content_input">
                  <div class="info_content_input_title">tug'ilgan kuni</div>
                  <input type="date" ref="birthday" value="2001-01-01" />
                </div>
              </div>
              <div class="new_accounts">
                <div class="new_account">
                  <div class="new_account_title">xisob ma'lumotlari</div>
                  <div class="new_account_content">
                    <div class="new_account_content_input">
                      <div class="new_account_content_input_title">
                        yashash manzili
                      </div>
                      <input
                        type="text"
                        v-model="adress"
                        placeholder="yashash manzili"
                      />
                    </div>
                    <div class="new_account_content_input">
                      <div class="new_account_content_input_title">bo'lim</div>
                      <div class="selected" :class="{ active: departament }">
                        <div
                          class="selected_option"
                          @click="departament = !departament"
                        >
                          <div class="selected_option_btns">
                            <span></span><span></span><span></span>
                          </div>
                          <div class="selected_option_title">
                            {{ bolimContent }}
                          </div>
                          <div class="selected_option_icon">
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
                        <div class="selected_content">
                          <div
                            class="selected_content_title"
                            v-for="b in bolimInfo"
                            :key="b?.id"
                            @click="(departament = false), departaments(b)"
                          >
                            {{ b?.name }}
                          </div>
                        </div>
                      </div>
                    </div>
                    <div class="new_account_content_input">
                      <div class="new_account_content_input_title">lavozim</div>
                      <div class="selected" :class="{ active: poosition }">
                        <div
                          class="selected_option"
                          @click="poosition = !poosition"
                        >
                          <div class="selected_option_btns">
                            <span></span><span></span><span></span>
                          </div>
                          <div class="selected_option_title">
                            {{ lavozimContent }}
                          </div>
                          <div class="selected_option_icon">
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
                        <div class="selected_content">
                          <div
                            class="selected_content_title"
                            v-for="l in lavozimInfo"
                            :key="l?.id"
                            @click="(poosition = false), poositions(l)"
                          >
                            {{ l?.name }}
                          </div>
                        </div>
                      </div>
                    </div>
                    <div class="new_account_content_input">
                      <div class="new_account_content_input_title">jadval</div>
                      <div class="selected" :class="{ active: table }">
                        <div class="selected_option" @click="table = !table">
                          <div class="selected_option_btns">
                            <span></span><span></span><span></span>
                          </div>
                          <div class="selected_option_title">
                            {{ jadvalContent }}
                          </div>
                          <div class="selected_option_icon">
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
                        <div class="selected_content">
                          <div
                            class="selected_content_title"
                            v-for="j in jadvalInfo"
                            :key="j?.id"
                            @click="(table = false), tables(j)"
                          >
                            {{ j?.startTime }} {{ j?.endTime }}
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="new_account_date">
                  <div class="new_account_date_title">kirish</div>
                  <div class="new_account_date_input">
                    <div class="new_account_date_input_title">
                      ishga qabul qilingan sana
                    </div>
                    <input type="date" ref="beginTime" value="2023-01-01" />
                  </div>
                  <div class="new_account_date_input">
                    <div class="new_account_date_input_title">
                      yaroqlilik muddati
                    </div>
                    <input type="date" ref="endTime" value="2023-01-01" />
                  </div>
                </div>
              </div>
            </div>
            <div class="new_information_image">
              <input id="img" ref="int" type="file" @change="imgFunc($event)" />
              <label class="imglabel" for="img">
                <img
                  id="uploadedImage"
                  src="../assets/images/Group 15.png"
                  alt=""
                />
              </label>
            </div>
          </div>
        </div>
        <!-- <pre>{{ jadvalInfo }}</pre>s -->
      </div>
    </div>
  </div>
</template>

<script setup>
import IMask from "imask";
const departament = ref(false);
const poosition = ref(false);
const table = ref(false);
const baseUrl = useRuntimeConfig().public.baseUrl;
const int = ref();
const file = ref(null);
const firstName = ref("");
const lastName = ref("");
const middleName = ref("");
const phoneNumber = ref("");
const birthday = ref();
const adress = ref("");
const departamentId = ref("");
const jobId = ref("");
const beginTime = ref();
const endTime = ref();
const gender = ref("femele");
const scheduleId = ref("");
const phone = ref();
function imgFunc(e) {
  if (e.target.files[0]) {
    file.value = e.target.files;
    var picture = new FileReader();
    picture.readAsDataURL(e.target.files[0]);
    picture.addEventListener("load", function (event) {
      document
        .getElementById("uploadedImage")
        .setAttribute("src", event.target.result);
    });
  }
}
const jadvalInfo = ref(null);
async function getScheduleApi() {
  const data = await $fetch(baseUrl + "/schedules", {
    headers: {
      Authorization: `Bearer ${localStorage.getItem("userToken")}`,
    },
  });

  jadvalInfo.value = data.result;
}
getScheduleApi();
const bolimInfo = ref(null);
async function gatDepartmentApi() {
  const data = await $fetch(baseUrl + "/departments", {
    headers: {
      Authorization: `Bearer ${localStorage.getItem("userToken")}`,
    },
  });
  bolimInfo.value = data.result;
}
gatDepartmentApi();
const lavozimInfo = ref(null);
async function getJobApi() {
  const data = await $fetch(baseUrl + "/jobs", {
    headers: {
      Authorization: `Bearer ${localStorage.getItem("userToken")}`,
    },
  });
  lavozimInfo.value = data.result;
}
getJobApi();
const jadvalContent = ref("jadval");
function tables(t) {
  jadvalContent.value = t.startTime + " " + t.endTime;
  scheduleId.value = t.id;
}
const lavozimContent = ref("lavozim");
function poositions(l) {
  lavozimContent.value = l.name;
  jobId.value = l.id;
}
const bolimContent = ref("bo'lim");
function departaments(b) {
  bolimContent.value = b.name;
  departamentId.value = b.id;
}

function genderInfo(e) {
  if (e.target.id === "gen-1") {
    gender.value = "MALE";
    console.log(gender.value);
  } else {
    gender.value = "FEMALE";
    console.log(gender.value);
  }
  // console.log(e.target.id);
}
async function userAdd() {
  var formdata = new FormData();
  formdata.append("firstName", `${firstName.value}`);
  formdata.append("lastName", `${lastName.value}`);
  formdata.append("middleName", `${middleName.value}`);
  formdata.append("phoneNumber", `${phoneNumber.value}`);
  formdata.append("address", `${adress.value}`);
  formdata.append("file", file.value[0]);
  formdata.append("departmentId", departamentId.value);
  formdata.append("jobId", jobId.value);
  formdata.append("beginTime", `${beginTime.value.value}T07:03:45`);
  formdata.append("endTime", `${endTime.value.value}T07:03:45`);
  formdata.append("gender", `${gender.value}`);
  formdata.append("scheduleId", scheduleId.value);
  formdata.append("dateOfBirth", `${birthday.value.value}`);
  const res = await fetch(baseUrl + "/employees", {
    method: "POST",
    headers: {
      Authorization: `Bearer ${localStorage.getItem("userToken")}`,
    },
    body: formdata,
  });
  const data = await res.json();
  console.log(data);
}
function tekshiruv() {
  if (firstName.value && lastName.value && middleName.value) {
    console.log("hello");
  } else {
    console.log("bug");
  }

  // console.log(firstName.value);
}

onMounted(() => {
  var maskOptions = {
    mask: "+{998}(00) 000-00-00",
    lazy: false,
  };
  var mask = new IMask(phone.value, maskOptions);
});
</script>

<style lang="scss" scoped>
</style>
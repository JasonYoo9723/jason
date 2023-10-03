<template>
    <div>
      <div class="tabmenu">
      <div class="big_tab">
        <ul>
          <li><div @click='tabChange(1)'>돌잔치 동영상</div></li>
          <li><div @click='tabChange(2)'>성장 동영상</div></li>
          <li><div @click='tabChange(3)'>하이라이트 동영상</div></li>
          <li><div @click='tabChange(4)'>문의</div></li>
        </ul>
      </div>
      
      <div class="sm_select">
        <select id="tabmenu" @change="tabChangeSelect($event)">
          <option value=1>돌잔치 동영상</option>
          <option value=2>성장 동영상</option>
          <option value=3>하이라이트 동영상</option>
          <option value=4>문의</option>
        </select>
      </div>
    </div>
    <div id="tab01" class="tab-contents" v-if="tabIndex == 1">
      <h2>돌잔치 영상</h2>
        <div class="video-wrapper">
          <video class="video" ref="video" autoplay controls loop controlsList='nodownload'>
            <source src="../../src/assets/video/firstBirthdayVideo1.mp4" type="video/mp4"/>
          </video>
        </div>
    </div>
    <div id="tab02" class="tab-contents" v-if="tabIndex == 2">
      <h2>성장 동영상</h2>
        <div class="video-wrapper">
            <video class="video" ref="video" autoplay controls loop controlsList='nodownload'>
              <source src="../../src/assets/video/firstBirthdayVideo1.mp4" type="video/mp4"/>
            </video>
          </div>
    </div>
    <div id="tab03" class="tab-contents" v-if="tabIndex == 3">
      <h2>하이라이트 동영상</h2>
        <div class="video-wrapper">
            <video class="video" ref="video" autoplay controls loop controlsList='nodownload'>
              <source src="../../src/assets/video/firstBirthdayVideo1.mp4" type="video/mp4"/>
            </video>
          </div>
    </div>
    <div id="tab04" class="tab-contents" v-if="tabIndex == 4">
      <h2>문의</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      tabIndex : 1,
    };
  },
  methods: {
    tabChange(type) {
      this.tabIndex = type;
      return this.tabIndex;
    },
    tabChangeSelect(event) {
      this.tabChange(event.target.value);
    }, 
  }
}
</script>
<style scoped>
@import "../../src/assets/styles.css";
</style>

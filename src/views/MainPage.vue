<template>
  <div>
    <v-toolbar app class="appbar">
      <v-btn icon class="hidden-xs-only">
        <v-icon>mdi-chevron-left</v-icon>
      </v-btn>
      <v-toolbar-title>주인공 만들기</v-toolbar-title>
    </v-toolbar>

    <div class="photo">
      <div>사진을 등록해주세요</div>
    </div>

    <div>
      <div class="radio">
        <span class="radio-name">장르</span>
        <v-radio-group v-model="genre" row>
          <v-radio label="로맨스 판타지" value="romance-fantasy"></v-radio>
          <v-radio label="로맨스" value="romance"></v-radio>
          <v-radio label="판타지" value="fantasy"></v-radio>
        </v-radio-group>
      </div>

      <div class="radio">
        <span class="radio-name">성별</span>
        <v-radio-group v-model="sex" row>
          <v-radio label="남자" value="male"></v-radio>
          <v-radio label="여자" value="female"></v-radio>
        </v-radio-group>
      </div>

      <v-btn class="btn" color="error">확인</v-btn>
    </div>

    <v-bottom-navigation absolute v-model="value">
      <v-btn value="recent">
        <span>Recent</span>

        <v-icon>mdi-history</v-icon>
      </v-btn>

      <v-btn value="favorites">
        <span>Favorites</span>

        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn value="nearby">
        <span>Nearby</span>

        <v-icon>mdi-map-marker</v-icon>
      </v-btn>

      <v-btn value="nearby">
        <span>Nearby</span>

        <v-icon>mdi-map-marker</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </div>
</template>
<script>
export default {
  data() {
    return {
      genre: "romance-fantasy",
      sex: "male",
    };
  },
};
</script>
<style scoped>
.photo {
  display: flex;
  height: 500px;
  background-color: gray;
}
.radio {
  display: flex;
}
.radio-name {
  margin: auto 0;
}
.btn {
  margin: 0 auto;
}
</style>

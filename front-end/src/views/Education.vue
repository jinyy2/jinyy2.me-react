<template>
    <v-container>
        <h1> 교육 이수 </h1>
        <v-divider />
        <br />
        <v-row dense>
          <v-col
            v-for="(item, i) in items"
            :key="i"
            cols="12"
          >
            <v-card
              :color="item.color"
              dark
            >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title
                  class="text-h5"
                  v-text="item.title"
                ></v-card-title>

                <v-card-subtitle v-text="item.date"></v-card-subtitle>
                <v-card-text v-html="item.content"></v-card-text>
                <v-card-actions>
                  <v-btn
                    class="ml-2 mt-5"
                    outlined
                    rounded
                    small
                    :href="item.siteLink"
                  >
                    사이트 바로가기
                  </v-btn>
                </v-card-actions>
              </div>

              <v-avatar
                class="ma-3"
                size="125"
                tile
              >
                <v-img :src="item.src"></v-img>
              </v-avatar>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
</template>


<script>
import SSAFY_LOGO from "@/assets/ssafy.png";
import KITRI_LOGO from "@/assets/kitri.png";
export default {
    name:'Education',
    data: ()=>({
        items:[{
            color: '#cc66ff',
            src: KITRI_LOGO,
            title:  '정보보안전문가양성 - 모의해킹',
            date: '2018.02.23 ~ 2018.07.31',
            content: '기업 내 IT자산에 대한 지속적인 위협에 대비하여 보안 취약점을 사전에 찾아내고,<br />내 외부 관점에서 침투 테스트를 시도하여 해킹 위협 및 내부 보안 사고를 예방할 수 있는 교육',
            siteLink: 'http://academy.kitri.re.kr/academy/main/main.web',
        },
        {
          color: '#0066ff',
          src: SSAFY_LOGO,
          title: '삼성 청년 SW 아카데미',
          date: '2020.01.06 ~ 2020.12.31',
          content: '- 1학기 집중 코딩교육 (20.01.06 ~ 20.06.19)<br /> - 2학기 심화 프로젝트 (20.07.08 ~ 20.11.27)',
          siteLink: 'https://ssafy.com/ksp/jsp/swp/swpMain.jsp',
        },
        ]
    }),
}
</script>

<style>

</style>
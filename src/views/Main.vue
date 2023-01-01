<template>
  <div class="Main">
    <div class="Main--content">
      <LayerContent>
        <template #header>
          <Stack contentId="about" title="About" />
        </template>
        <template #content>
          <div>test</div>
          <div class="About">
            <div class="AboutProfileArea">
              <div class="Profile">
                <div class="ProfileRadius">
                  <div class="ProfileContetnt">
                    <p class="ProfileContetnt--txt">生年月日：1999年1月23日</p>
                    <p class="ProfileContetnt--txt">出身地：宮城県仙台市</p>
                    <p class="ProfileContetnt--txt">血液型：AB型</p>
                    <p class="ProfileContetnt--txt">身長：186cm</p>
                    <p class="ProfileContetnt--txt">最終学歴：東北福祉大学</p>
                    <p class="ProfileContetnt--txt">職業：無職☆</p>
                    <p class="ProfileContetnt--txt">趣味：ファッション、スポーツ</p>
                  </div>
                </div>
              </div>
              <div class="ProfileImgArea">
                <img class="ProfileImg" src="../assets/img/img_profile.jpg" alt="">
              </div>
            </div>
            <div class="AboutMessageArea">
              <div class="MessageHeader">
                Message
              </div>
              <p class="Message--txt">
                こんにちは、安藤と申します。
                中学時代に自分に自信がなくなったことがきっかけで、高校で未経験ながらラグビー部に所属。その後、多くの方々に支えられられらたことから今度は自分が目の前の人に自信を与えられるような人になりたいという夢ができました。そんな思いから、ファーストキャリアではリンクアカデミーという会社で叶えたい夢・目指す姿を実現したいというお客様のキャリアに寄り添うお仕事に従事して参りました。
                無形のものを提供するお仕事でしたが、これからは大学時代から好きだったファッションを通じて、目の前の人が自分に自信を持ってキラキラしてほしいというコンセプトのもと邁進して参ります。
              </p>
            </div>
          </div>
        </template>
      </LayerContent>
      <LayerContent>
        <template #header>
          <Stack contentId="career" title="Career" />
        </template>
        <template #content>
          <div class="Career">
            <div class="CareerContent">
              test
            </div>
          </div>
        </template>
      </LayerContent>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import router from "@/router";
import LayerContent from "@/components/Layer.vue";
import Stack from "@/components/Stack.vue";

export default defineComponent({
  name: "Main",
  components: {
    Stack,
    LayerContent,
  },
  setup(props) { },
});
</script>

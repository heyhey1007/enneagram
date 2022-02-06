<template>
  <v-container class="px-6">
    <v-row align="center" justify="center">
      <div class="bg pl-12 pb-12 pr-7 py-12 mt-10">
        <v-row align="center" justify="center">
          <v-row justify="center">
            <v-col cols="12" class="pl-4 mt-12">
              <p>あなたに当てはまるものを選んでください！</p>
              <!-- <p>{{ no1 }}</p> -->
            </v-col>
          </v-row>
          <div class="question_container pl-10">
            <v-row align="end">
              <v-col align-self="center" cols="12">
                <v-radio-group class="" v-model="radioGroup">
                  <v-radio
                    v-for="item in questions"
                    :key="item.no"
                    :label="item.question"
                    :value="item.no"
                    class="py-6 px-4"
                  ></v-radio>
                </v-radio-group>
              </v-col>
            </v-row>
          </div>
          <v-row>
            <v-col align="end" class="pb-12" cols="8">
              <v-btn x-large to="/question?one=1" color="success" dark
                >次の質問に答える</v-btn
              >
            </v-col>
          </v-row>
        </v-row>
      </div>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      //   result: {
      //     //TODO: querystringが取れていない
      //     no1: this.$route.query.one,
      //   },
      questions: [
        {
          no: 1,
          question: `これは質問1です。これは質問1です。これは質問1です。これは質問1です。これは質問1です。`,
        },
        {
          no: 2,
          question: `質問2質問2質問2質問2質問2質問2`,
        },
        {
          no: 3,
          question: `質問3ですよね？`,
        },
      ],
    };
  },
};
</script>

<style>
p {
  font-size: 2rem;
}
.bg {
  max-width: 700px;
  min-height: 400px;
  background-image: url("/image/question_background.png");
  background-size: 100% 100%;
}
.question-container {
}
</style>

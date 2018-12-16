<template>
  <div>
    <p>{{title}}</p>
    <!-- v-model を使ってimput_msgにimputタグで入力した値を都度反映する -->
    <p><input v-model="input_msg"></P>
    <!-- 子コンポーネントのmessageに反映した値を設定して呼び出す -->
    <hello-child :message="input_msg"/>
  </div>
</template>

<script>
import HelloChild from './HelloChild'
export default {
  data: function () {
    return {
      title: 'はろー！わーるど！',
      input_msg: ''
    }
  },
  components: {
    HelloChild
  }
}
  </script>


<!-- src/components/MemoApp.vue-->
<template>
  <div class="memo-app">
      <memo-form />
      <memo />
  </div>
</template>

<script>
import MemoForm from './MemoForm.vue';
import Memo from './Memo.vue';

export default {
    name: 'MemoApp',
    data () {
        return{
            memos: [],
        };
    },
    created (){
        //1.만약 기존에 추가된 localStorage에 데이터가 있다면 created훅에서 localStorage의 데이터를 컴포넌트 내의 memos 데이터에 넣어주고, 그렇지 않다면 그대로 빈 배열로 초기화한다.
        this.memos = localStorage.memos ? JSON.parse(localStorage.memos) : [];

    }

}
</script>

<style>

</style>
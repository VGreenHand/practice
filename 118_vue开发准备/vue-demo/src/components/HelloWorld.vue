<template>
  <div class="hello">
    <h1>学习vue</h1>
    <p>{{ message }}</p>
    <div v-html="rawHtml"></div>
    <div :id="ID"></div>
    <button @click="increment" @contextmenu.prevent="clearCount">点击:{{ count }}</button>
    <!-- v-if -->
    <p v-if="flag">Im Batman</p>
    <p v-else>Im not Batman</p>
    <!-- v-show -->
    <p v-show="flag">Im Batman</p>
    <p v-show="!flag">Im not Batman</p>
    <ul>
      <li v-for="item in newList" :key="item.id">
        {{ item.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      message: 'Hello Vue!',
      rawHtml: "<a href = 'http://www.baidu.com'>这是一个链接</a>",
      id: 'test',
      flag: false,
      newList:[
        {id:1,name:'张三'},
        {id:2,name:'李四'},
        {id:3,name:'王五'},
      ],
      count: 0

    }
  },
  methods: {
          increment() {
            this.count++
          },
          clearCount() {
            this.count = 0
          }
  }
}

</script>



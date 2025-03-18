<template>
  <div class="hello">
    <h1>学习vue：模板语法</h1>
    <p>{{ message }}</p>
    <div>{{ rawHtml }}</div>
    <div v-html="rawHtml"></div>
    <div :id="ID"></div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      message: 'Hello Vue!',
      rawHtml: "<a href = 'http://www.baidu.com'>这是一个链接</a>",
      id: 'test'
    }
  }
}
</script>



<template>
  <div class="container">
    <div>
      <h1 class="title">
        Zenn-app
      </h1>
      <h2 class="subtitle">
        {{ subTitle }}
      </h2>
      <button @click="getSomething">
        タスク取得
      </button>
      <ul v-for="task in tasks" :key="task.id">
        <li style="text-align: left;">{{ task.title }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      subTitle: 'Zenn is good service!!',
      tasks: []
    }
  },
  methods: {
    async getSomething() {
      const response = await this.$axios.$get('http://localhost:3001/api/v1/tasks')
      this.tasks = JSON.parse(response.tasks)
    }
  },
}
</script>

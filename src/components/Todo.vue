<template>
  <div>
    <form action="">
      <input type="text" v-model="text">
      <input type="submit" value="Add" v-on:click.prevent="add">
    </form>
    <ul>
      <li v-for="(item, key) in list" v-if="item.status === 0">
        {{ item.text }} <button v-on:click="done(key)">Done</button>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'Todo',
    data() {
      return {
        text: '',
        list: [],
      }
    },
    methods: {
      add: function () {
        this.list.push({
          text: this.text,
          status: 0,
        });
        this.text = '';
      },
      done: function (key) {
        this.list[key].status = 1;
      },
    },
  }
</script>

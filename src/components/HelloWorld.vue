<template>
  <div>
    <h1>VueJS Application using Web Components</h1>

    <p>
      {{show ? 'open' : 'closed'}}
    </p>

    <x-dropdown :title="myTitle" @show="log">
      Hello from Web Component in Vue!
    </x-dropdown>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function () {
    return {
      myTitle: 'project-vue',
      show: false
    }
  },
  methods: {
    log: function (event) {
      console.log(event);
      this.show = event.detail;
    }
  }
}
</script>

<style scoped>

</style>

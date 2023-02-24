<script lang="ts">
import {
  defineComponent,
  ref
} from 'vue'
import { someType } from '@/types/user'

export default defineComponent({
  name: 'HelloWorld',
  components: {},
  setup () {
    const someVar = ref<someType>({})

    someVar.value = {
      firstName: 'adasd',
      lastName: 'adasd',
      middleName: 'adasd',
      phoneNumber: 'adasd'
    }

    return {
      someVar
    }
  }
})
</script>

<template>
  <div class="hello">
    <h1>{{ someVar }}</h1>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>

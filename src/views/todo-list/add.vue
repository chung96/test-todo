<template>
  <div>
    <div class="container-fluid">
      <div class="box" style="padding:4rem">
        <form-add
          @cancel="cancelForm"
          @done="doneAdd"
        />
      </div>
    </div>
  </div>
</template>

<script>
import FormAdd from '@/components/pages/todo/FormAdd'

export default {
  name: 'TodoList',
  components: {
    FormAdd
  },
  data() {
    return {
    }
  },
  watch: {
  },
  methods: {
    cancelForm() {
      this.goList()
    },
    doneAdd() {
      this.goList()
    },
    goList() {
      this.$router.push({ name: 'TodoList' })
    }
  }
}
</script>

<style lang="scss" scoped>

</style>

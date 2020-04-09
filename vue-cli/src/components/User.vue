<template>
  <div class="component">
    <h1>The User Component</h1>
    <p>I'm {{ name }}!</p>
    <p>{{ age }} years old!</p>
    <button @click="reverseName">reverseName</button>
    <hr />
    <div class="row">
      <div class="col-xs-12 col-sm-6">
        <app-user-detail
          :name="name"
          :age="age"
          @nameChanged="name = $event"
          :resetName="resetName"
         ></app-user-detail>
        <!-- <app-user-detail></app-user-detail> -->
      </div>
      <div class="col-xs-12 col-sm-6">
        <app-user-edit :name="name" :age="age" @ageChanged="age = $event"></app-user-edit>
      </div>
    </div>
  </div>
</template>

<script>
import UserDetail from "./UserDetail.vue";
import UserEdit from "./UserEdit.vue";

export default {
  data: function () {
    return {
      name: "Max",
      age: 24
    };
  },
  methods: {
    reverseName() {
      this.name = this.name.split("").reverse().join("");
    },
    resetName() {
      this.name = 'Max'
    }
  },
  components: {
    appUserDetail: UserDetail,
    appUserEdit: UserEdit,
  },
};
</script>

<style scoped>
div {
  background-color: lightblue;
}
</style>

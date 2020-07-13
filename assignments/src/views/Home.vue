<template>
  <div class="home">
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-1">
          <div>
            <h4>הגדרות</h4>
          </div>
          <div>
            <b-button class="col-lg-12">פרטי</b-button>
          </div>
          <div>
            <b-button class="col-lg-12">ציבורי</b-button>
          </div>
        </div>
        <div class="col-lg-8">
          <h1 class="col-lg-12">כאן ניתן לכתוב את כל ההודעות</h1>
          <b-table striped hover :items="items"></b-table>
          <b-input class="col-lg-12" placeholder="הוסף הודעה" />
        </div>
        <div class="col-lg-3 red">
          <h4 class="col-lg-12">:נושאים</h4>
          <b-button class="col-lg-12 btn btn-default">HTML</b-button>
          <b-button class="col-lg-12 btn btn-default">js</b-button>
          <b-button class="col-lg-12 btn btn-default">css</b-button>
          <b-button class="col-lg-12 btn btn-default">node</b-button>
          <b-button class="col-lg-12 btn btn-default">mongoose</b-button>
          <b-button class="col-lg-12 btn btn-default">express</b-button>
          <b-button class="col-lg-12 btn btn-default">vue.js</b-button>
          <b-button class="btn btn-default col-lg-6 b">הוסף נושא</b-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      items: [
        { age: 40, first_name: "Dickerson", last_name: "Macdonald" },
        { age: 21, first_name: "Larsen", last_name: "Shaw" },
        { age: 89, first_name: "Geneva", last_name: "Wilson" },
        { age: 38, first_name: "Jami", last_name: "Carney" }
      ]
    };
  }
};
</script>
<style scoped>
.container-fluid {
  margin-top: 30px;
}
.btn-secondary {
  margin-bottom: 15px;
  background-color: #8299ae;
}
</style>

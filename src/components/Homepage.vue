<template>
  <div>
      <div class="split right">
        <div>Hello</div>
        <p>Name is {{author}}</p>
      </div>
      <div class="split left">
        <h1 style="text-align:center;margin-top:10px;margin-bottom:20px;">Reading List</h1>
        <div class="added-books">
          <span style="border-style:groove;padding:5px;">{{name}}</span>
        </div>
        <div class="add-book">
          <div>
            <form class="add-book-form">
              <div id="name-section" class="form-group row">
                <label id="l-1" class="col-sm-3 col-form-label" for="book-name">Name:</label>
                <div class="col-sm-6">
                  <input type="text" v-model="name" style="margin-left:-50px;" class="form-control form-control-sm" id="book-name">
                </div>
              </div>
              <div id="genre-section" class="form-group row">
                <label id="l-2" class="col-sm-3 col-form-label" for="genre">Genre:</label>
                <div class="col-sm-6">
                  <input type="text" v-model="genre" style="margin-left:-50px;" class="form-control form-control-sm" id="genre">
                </div>
              </div>
              <div id="author-section" class="form-group row">
                <label id="l-3" for="author" class="col-sm-3 col-form-label">Author:</label>
                <div class="col-sm-6">
                <select name="author" v-model="author" style="margin-left:-50px;" class="form-control form-control-sm" id="author">
                  <option value="Fred">Fred</option>
                  <option value="Tom">Tom</option>
                  <option value="Tony">Tony</option>
                </select>
                </div>
              </div>
            </form>
          </div>
        </div>
        <img class="img-button" src="@/assets/button.png" alt="no image">
      </div>
    </div>
</template>

<script>
export default {
  name: 'Homepage',
  data () {
    return {
      name: '',
      genre: '',
      author: 'Fred'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.split {
  height: 100%;
  position: fixed;
  top:0;
  overflow-x: hidden;
  width: 100%;
}

.left {
  left: 0;
  width: 60%;
  background-color: whitesmoke;
}

.right {
  right: 0;
  width: 40%;
  background-color: red;
}

.add-book {
  position: absolute;
  z-index: 1;
  width: 60%;
  background-color: white;
  padding-top: 2%;
  padding-bottom: 2%;
  bottom: 0px;
}

#l-1 {
  margin-left: 25%;
  margin-right: 0%;
}

#l-2 {
  margin-left: 25%;
}

#l-3 {
  margin-left: 24%;
  margin-right: 1%;
}

#genre-section {
  margin-top: -15px;
}

#author-section {
  margin-top: -15px;
}

.img-button {
  position: absolute;
  z-index: 2;
  margin-top:10%;
  margin-left: 1%;
  margin-bottom: 1%;
  bottom: 0px;
}

.added-books {
  margin: 10px;
}
</style>

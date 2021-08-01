<template>
  <div >
    <div id="logout">
<button text small v-on:click="signOut" class="mr-16" id="sign-out">Sign Out</button>
    </div>
    <div id="create-post">
    <h1>Creating a New Post</h1>
   <form>
     <label id="title-text"> Post Title:
     </label>
     <input type="text" v-model="title" required/>
     <label id="title-text" > Post Content: </label>
     <textarea v-model="content"></textarea>
   </form>
   <div id="show-posts">
     <h3 id="title">Preview Posts</h3>
     <p id="title">Post title:{{title}}</p>
     <p id="title">Post content:{{content}}</p>
   </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
    title:"",
    content:""
    }
  },
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods:{
    signOut() {
      this.$router.push({name: 'login'})
        
    }
  }
}
</script>

<style scoped lang="scss">
#create-post*{
  box-sizing: border-box;
}

#create-post{
  margin: 20px auto;
  max-width: 500px;
}

#label{
  display: block;
  margin: 20px 0 10px;
}

input[type="text"], textarea{
  display: block;
  width: 100%;
  padding: 8px;
}

#show-posts{
  margin: 30px 0;
  border: 1px dotted #cccc;
  padding: 10px 20px;
}

#h3{
  margin-top: 10px;
}
#title{
  text-align: left;
}
#title-text{
  float: left;
}

#logout{
  float: right;
  margin-right: 100px;
}

</style>


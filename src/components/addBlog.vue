<template>
  <div id="add-blog">
    <h1>Blog by Tomasz Waligóra</h1>
    <form action="#">
      <label for="title">Blog Title</label>
      <input type="text" id="title" placeholder="Title" v-model="blog.title" />
      <label for="content">Blog Content</label>
      <textarea
        name=""
        id=""
        cols="30"
        rows="10"
        v-model="blog.content"
        placeholder="Message"
      ></textarea>
    </form>
    <div class="preview">
      <h2>Preview Blog</h2>
      <div class="preview-style">
        <p><b>Blog Title:</b> {{ blog.title }}</p>
        <p><b>Blog Content:</b></p>
        <p v-if="show">{{ blog.content }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      blog: {
        title: "",
        content: "",
      },
      show: false,
    };
  },
};
</script>
<style scoped>
* {
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

#add-blog {
  width: 520px;
  margin: 0 auto;
}
#add-blog h1 {
  text-align: center;
}
form {
  text-align: center;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
  padding: 1rem;
  border-radius: 10px;
  width: 100%;
  display: block;
}
label {
  display: block;
  margin: 20px 0 10px;
  text-align: center;
}

input,
textarea {
  width: 100%;
  outline: none;
  padding: 0.5rem;
  font-family: Fira Code;
  border: none;
  background: lightgray;
  border-radius: 10px;
}

input:focus,
textarea:focus {
  background: #f4b95f;
}

.preview {
  margin-top: 5rem;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
  padding: 1rem;
  border-radius: 10px;
}

.preview h2 {
  margin-bottom: 3rem;
  text-align: center;
}

.preview p {
  height: 2rem;
}

.preview-style {
  border: 1px dotted lightgray;
  padding: 1rem;
}
</style>

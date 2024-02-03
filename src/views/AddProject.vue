<template>
  <form @submit.prevent="handleSubmit">
    <label>Title:</label>
    <input type="text" required v-model="title" />
    <label>Details:</label>
    <textarea required v-model="details"></textarea>
    <button>Add Project</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      title: "",
      details: "",
    };
  },
  methods: {
    handleSubmit() {
      let project = {
        title: this.title,
        details: this.details,
        complete: false,
      };
      fetch("http://localhost:3000/projects", {
        method: "POST",
        headers: { "Content-Type": "aplication/json" },
        body: JSON.stringify(project),
      })
        .then(() => {
          this.$router.push("/");
        })
        .catch((err) => console.log(err));
    },
  },
};
</script>

<style>
form {
  background: #4444;
  padding: 20px;
  border-radius: 10px;
  border: 4px solid #00ce89;
}
label {
  display: block;
  color: #bbb;
  text-transform: uppercase;
  font-size: 14px;
  font-weight: bold;
  letter-spacing: 1px;
  margin: 20px 0 10px 0;
}
input {
  padding: 10px;
  border: 0;
  border-bottom: 1px solid #00ce89;
  width: 100%;
  box-sizing: border-box;
  background-color: #4444;
  color: #bbb;
}
textarea {
  border: 1px solid #00ce89;
  border-radius: 4px;
  padding: 10px;
  width: 100%;
  box-sizing: border-box;
  height: 100px;
  resize: vertical;
  background-color: #4444;
  color: #bbb;

}
form button {
  display: block;
  margin: 20px auto 0;
  background: #00ce89;
  color: #444;
  padding: 10px;
  border: 0;
  border-radius: 6px;
  font-size: 16px;
  font-weight: 600;
}
</style>

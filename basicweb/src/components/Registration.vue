<template>
    <section class="grid-container">
        <div class="grid bg-red"></div>
        <div class="grid"> 
            <form class="">
                <h1>Hello <span class="deco-name">{{displayUser}},</span> Sign In</h1>
                <input type="text" placeholder="Username" v-model="user" required="" maxlength="30">
                <input type="password" placeholder="Password" required>
                <input type="submit">
                <sub>Don't Have an account? Sign Up <a class="hyperlink">here</a></sub>
            </form>
        </div>
    </section>
</template>

<script>
/* eslint-disable */
export default {
  name: 'RegistrationVue',
  data() {
    return {
        user : "",
        displayUser: "user"
    }
  },
  methods: {
    // Your functions
  },
  created() {
    // Start event (do something when started)
  },
  updated() {
    if (this.user == "")
    {
        this.displayUser = "user";
    }
    else {
        if (this.user.length < 15) {
            this.displayUser = this.user
        }
        else {
            this.displayUser = this.user.slice(0, 15) + "...";
        }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only (local styles) -->
<style scoped>
* {
    color: white;
}

input {
    width: 70%;
    height: 30px;
    border-radius: 10px;
    border: 1px solid black;
    padding: 5px 15px;
    margin: 10px auto;
    color: black;
}

.grid-container {
    display: grid;
    height: 100vh;
    grid-template-columns: 50vw 50vw;
}

.grid {
    height: 100%;
    display: flex;
}

form {
    display: flex;
    flex-direction: column;
    background-color: rgba(128, 128, 128, 0.452);
    width: 50%;
    aspect-ratio: 2/3;
    margin: auto;
    padding: 10px;
    border-radius: 5px;
}

.deco-name {
    color: yellow;
    text-decoration: underline;
    font-size: 14pt;
}

sub {
    margin: 5px auto;
}

.hyperlink {
    color: blue;
    text-decoration: underline;
    cursor: pointer;
}
</style>

<template>
  <section>
    <header><h1>My friends</h1></header>
    <ul>
      <friend-contact 
      v-for="f in friend"
      :key="f.id"
      :name="f.name" 
      :phone-number="f.mobile" 
      :email-address="f.email" 
      :is-favorite="f.isFavorite"
      @toggle-fav="toggleFavStatus">
      </friend-contact>
      
    </ul>
  </section>
</template>

<script >
export default {
  data() {
    return {
      friend: [
        {
          id: "Yash",
          name: "yash Sharma",
          mobile: "9876543210",
          email: "yash@gmail.com",
        },
        {
          id: "Vinay",
          name: "Vinay Sharma",
          mobile: "9876556789",
          email: "vinay@gmail.com",
        },
      ],
    };
  },
  methods:{
    toggleFavStatus(){}
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Jost&display=swap");
* {
  box-sizing: border-box;
}

html {
  font-family: "Jost", sans-serif;
}

body {
  margin: 0;
}

header {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem auto;
  border-radius: 10px;
  padding: 1rem;
  background-color: #58004d;
  color: white;
  text-align: center;
  width: 90%;
  max-width: 40rem;
}

#app ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

#app li {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 1rem auto;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
  width: 90%;
  max-width: 40rem;
}

#app h2 {
  font-size: 2rem;
  border-bottom: 4px solid #ccc;
  color: #58004d;
  margin: 0 0 1rem 0;
}

#app button {
  font: inherit;
  cursor: pointer;
  border: 1px solid #ff0077;
  background-color: #ff0077;
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
}

#app button:hover,
#app button:active {
  background-color: #ec3169;
  border-color: #ec3169;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.26);
}
</style>
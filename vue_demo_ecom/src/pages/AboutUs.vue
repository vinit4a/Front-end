<template>
    <section>
        <!--Header Start-->
            <the-header></the-header>
        <!--Header End-->
        <bread-crumb></bread-crumb>
        <section>
             <div class="container">
               <div class="about-section">
                <h1 class="text">About Us</h1>
                <p>Some text about who we are and what we do.</p>
                <p>Resize the browser window to see that this page is responsive by the way.</p>
                </div>

                <h2 style="text-align:center">Our Team</h2>
                <div class="row">
                <div class="column">
                    <div class="card">
                    <img src="https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg" alt="Jane" style="width:100%">
                    <div class="container">
                        <h2>Vinit</h2>
                        <p class="title">CEO & Founder</p>
                        <p>Some text that describes me lorem ipsum ipsum lorem.</p>
                        <p>vinit@example.com</p>
                        <p><button class="button">Contact</button></p>
                    </div>
                    </div>
                </div>

                <div class="column">
                    <div class="card">
                    <img src="https://fakestoreapi.com/img/71-3HjGNDUL._AC_SY879._SX._UX._SY._UY_.jpg" alt="Mike" style="width:100%">
                    <div class="container">
                        <h2>Avni</h2>
                        <p class="title">Art Director</p>
                        <p>Some text that describes me lorem ipsum ipsum lorem.</p>
                        <p>avni@example.com</p>
                        <p><button class="button">Contact</button></p>
                    </div>
                    </div>
                </div>

                <div class="column">
                    <div class="card">
                    <img src="" alt="John" style="width:100%">
                    <div class="container">
                        <h2>Devarsh</h2>
                        <p class="title">Designer</p>
                        <p>Some text that describes me lorem ipsum ipsum lorem.</p>
                        <p>devarsh@example.com</p>
                        <p><button class="button">Contact</button></p>
                    </div>
                    </div>
                </div>
                </div> 
             </div>
        </section>
        <!--Footer Start-->
            <the-footer></the-footer>
        <!--Footer End-->
    </section>
</template>



<script>
import TheHeader from "../components/layouts/TheHeader.vue";
import TheFooter from "../components/layouts/TheFooter.vue";
import BreadCrumb from '../pages/BreadCrumb.vue'

export default {
  components: { TheHeader, TheFooter,BreadCrumb },
  name: "Home",
  TheHeader,
  TheFooter,
};
</script>

 
<style scoped>

.text{
    color: black;
}
   
*, *:before, *:after {
  box-sizing: inherit;
}

.column {
  float: left;
  width: 33.3%;
  margin-bottom: 16px;
  padding: 0 8px;
}

.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  margin: 8px;
}

.about-section {
  padding: 50px;
  text-align: center;
  background-color: #ffffff;
  color: white;
}

.container {
  padding: 0 16px;
}

.container::after, .row::after {
  content: "";
  clear: both;
  display: table;
}

.title {
  color: rgb(148, 138, 138);
}

.button {
  border: none;
  outline: 0;
  display: inline-block;
  padding: 8px;
  color: white;
  background-color: #000;
  text-align: center;
  cursor: pointer;
  width: 100%;
}

.button:hover {
  background-color: #555;
}

@media screen and (max-width: 650px) {
  .column {
    width: 100%;
    display: block;
  }
}

</style>

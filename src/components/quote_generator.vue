<template>
  <div>
      <div>
        <button class="button" @click="fetchData">Click on me for a quote</button>
      </div>
      <div v-if="data">
        <pre class="datacontent">{{ data.content }}</pre>
      </div>
  </div>
  
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      data: null
    };
},
methods: {
  fetchData() {
    //Define apiUrl
    const apiUrl = 'https://api.quotable.io/random';

    //axios to make get request
    axios.get(apiUrl)
      .then(response => {
        this.data = response.data;
      })
      //handle error case
      .catch(error => {
        console.error('Error fetching data:', error);
      });
  }
}
};
</script>

<style>
.datacontent{
  width: 400px;
  height: auto;
  white-space: normal;
  word-wrap: break-word;
  vertical-align: top;
}

.button {
  background-image: linear-gradient(92.88deg, #6fe1f5 9.16%, #5643CC 43.89%, rgb(76, 181, 226));
  border-radius: 8px;
  border-style: none;
  box-sizing: border-box;
  color: #FFFFFF;
  cursor: pointer;
  flex-shrink: 0;
  font-family: "Inter UI","SF Pro Display",-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen,Ubuntu,Cantarell,"Open Sans","Helvetica Neue",sans-serif;
  font-size: 16px;
  font-weight: 500;
  height: 4rem;

  text-align: center;
  text-shadow: rgba(0, 0, 0, 0.25) 0 3px 8px;
  transition: all .5s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  border-radius: 10%;

  position: absolute;
  margin-top: 240px;
  margin-right: 60px;
  right: 50px;

}

.button:hover {
  box-shadow: rgba(80, 63, 205, 0.5) 0 1px 30px;
  transition-duration: .1s;
}
</style>

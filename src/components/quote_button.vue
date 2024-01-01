<template>
    <div class="quote-button">
      <button class="button" @click="fetchData">Click on me for a quote</button>
    </div>
  </template>
  
  <script>
  import axios from 'axios';
  
  export default {
    methods: {
      fetchData() {
        // Define apiUrl
        const apiUrl = 'https://api.quotable.io/random';
  
        // Axios to make get request
        axios.get(apiUrl)
          .then(response => {
            // Emit an event with the quote data
            this.$emit('quote-fetched', response.data);
          })
          // Handle error case
          .catch(error => {
            console.error('Error fetching data:', error);
          });
      }
    }
  };
  </script>
  
  <style scoped>
  /* Styles for the button component */
  .quote-button {
    position: absolute;
    margin-top: 120px; /* Adjust the margin as needed */
  }
  
  /* Include your button styling here */
  .button {
    background-image: linear-gradient(92.88deg, #455EB5 9.16%, #5643CC 43.89%, #673FD7 64.72%);
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
    margin-top: 120px;
  }
  </style>
  
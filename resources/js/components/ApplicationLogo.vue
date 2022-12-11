<template>
         <div alt="" class="tm">
            <h1>J &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</h1>
            <h1 class="O">O</h1>
            <h1>PE</h1>
         </div>
</template>
<style scoped>

h1 {
   font-size: 3em;
   letter-spacing: 1px;
   font-weight: bold;
   font-family: 'Montserrat', fantasy;
}

@keyframes text{
   0%{
      background-position: 0% 50%;
      color: rgba(230, 210, 97, 0.961);
   } 
   
   50%{
      background-position: 0% 100%;
      color: rgb(193, 120, 51);
   }

   75%{
      background-position: 0% 50%;
      color: rgb(228, 43, 43);
   }
   100%{
      background-position: 0% 50%;
      color: rgba(230, 210, 97, 0.961);
   } 
   
}
 .tm{
   background: black;
   padding: 4px 53px 10px ;
   border-radius: 8px;   
	animation: text 2.5s infinite linear;
    width: 226px;
    display: flex;
 }
 .O{
   margin-top: 8px;
    margin-left: 5px;
    margin-right: -18px;
    font-size: 75px;
    /* margin-bottom: 0px; */
    transform: rotate(90deg);


 }
</style>

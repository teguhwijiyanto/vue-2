<template>

<body>

<div id="app">
  <!--
  <ul>
    <li v-for="data in records">
      {{ data.id }} <br>
      {{ data.first_release_date }} <br>
      {{ data.name }} <br>
      {{ data.rating }} <br>
      {{ data.summary }} <br>
    </li>
  </ul>
  -->

  <div class="container_order_by">
  <div class="grandparent">
    <div class="parent">
    <router-link :to="`/`">VIDEO</router-link>
        <div class="child">&nbsp;</div>
    </div>
  </div>
  <div class="menu-separator">&nbsp;</div>
  <div class="grandparent">
    <div class="parent">
    CONTACT
        <div class="child">CONTACT</div>
    </div>
  </div>
</div>


  <div class="row">

      <div class="midcolumn">

            <div class="form2" style="background: transparent;">
              <div class="form-box" style="">GET IN TOUCH</div>
              <div class="form-box-text" style="font-size:5px;">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.
              </div>
            </div>

            <div class="form2" style="">
              <div class="form-box" style="">Contact Form</div>
              <br>
              <form>

            <div>
                <div class="form-left" style="padding-right:10px;">
                  <label>Name</label>
                  <input type="text" placeholder="">
                </div>
                <div class="form-right" style="padding-left:10px;">
                  <label>E-mail address</label>
                  <input type="text" placeholder="">
                </div>
        </div>
<br>
<br>
<br>
                  <label>Message</label>
                    <textarea rows=5 style="width:100%;"></textarea>
                    <br><br>
                    <button class="btn-clear" style="">Send</button>   
                    <br>
               </form>
            </div>
            
      </div> <!-- END midcolumn -->
  

  </div> <!-- END row -->



</div>

</body>

</template>



<script>
export default {
  data() {
    return {
      posts: []
    };
  },
  methods: {
    fetchPosts() {
      fetch("http://localhost/applicant_test.json")
        .then(response => response.json())
        .then(data => (this.posts = data));
    }
  },
  mounted() {
    this.fetchPosts();
  }
};
</script>


<style>
    
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100&display=swap');
  /*
  font-family: 'Montserrat', sans-serif;
  */

  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100&family=Mulish:wght@200&display=swap');
  /*
  font-family: 'Mulish', sans-serif;
  */

  * {
    box-sizing: border-box;
  }

 

.menu-separator {
  display: inline;
  margin-left:100px;
}

  body {
    font-family: 'Mulish', sans-serif;
    font-size:10px;
    padding: 20px;
    background: #f1f1f1;
    background-image: linear-gradient(to bottom, #081221, #03080f);
    color: #ffffff;
  }

  input, select, textarea{
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    background: #182c47;
    color: #ffffff;
	width:100%;
  }

  button{
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    background: #5692e8;
    color: #ffffff;
	float:right;
  }
 
 .btn-arrow {
   font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    background: #5692e8;
    color: #ffffff;
 width:20px;
 padding:0px;
 }
 
  .btn-clear {
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    background: #5692e8;
    color: #ffffff;
 padding:5px;
 }
 
 
.form2 {
	padding:20px;
	background-color: #0e1a2b;
}
 
 .form-box {
 font-weight:bold; 
 font-family: 'Montserrat', sans-serif;
 }
 
 
 
  .header {
    padding: 30px;
    font-size: 40px;
    text-align: center;
    opacity: 0.3;
	text-align:left;
  }
  
  .header-bg {
     opacity: 0.2;
	 font-weight:bold; 
	 font-family: 'Montserrat', sans-serif;
  }
  
    
  /* Right column */
  .midcolumn {
    float: left;
    width:40%;
	padding:20px;
  margin-left: 30%;
  }
  
  /* Fake image */
  .fakeimg {
    background-color: #aaa;
    width: 100%;
    padding: 20px;
  }
  
  /* Add a card effect for articles */
  .card {
     background-color: #0e1a2b ;
     padding: 20px;
     margin-top: 20px;
	 padding-top:0px;
   padding-left:0px;
   padding-bottom:0px;
  }
  
  /* Clear floats after the columns */
  .row:after {
    content: "";
    display: table;
    clear: both;
  }
  
  /* Footer */
  .footer {
    padding: 20px;
    text-align: center;
    background: #ddd;
    margin-top: 20px;
  }
  
  .container2{
        width: 100%;
        border: 0px solid black;
  }
      
  .form-left{
      width: 50%;
      float: left;
      padding-right:10px;
  }
       
 .form-right{
      width: 50%;
      float: left;
      padding-left:10px;
  }
  
  .badge2{
      height: 100%;
        float: right;
  }
  
  .badge2-mobile{
      height: 100%;
      background-color: yellow;
        float: right;
  }
  
  .circle {
    display: inline-table;
    vertical-align: middle;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    margin-top:80px;
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    background: #5692e8;
    color: #ffffff;
  }

  
  .circle-content {
    display: table-cell;
    vertical-align: middle;
    text-align: center;
  }
  
  .container_order_by{
      width: 100%;
      height: 100px;
  }
      
  .arrow_up{
      width: 10%;
      float: left;
	  text-align:center;
  }
       
  .select_order{
      width: 90%;
      height: 100%;
        float: left;
  }
  
  .firstchild {
              top: 0;
              left: 0;
			  top:75px;margin-left:110px; font-family: 'Montserrat', sans-serif;
  }
      
  .childClass {
              position: absolute;
              color: #ffffff;
  }
  
  .content  {
  height:172px;padding:20px;border:0px solid yellow; overflow:hidden;
  font-family: 'Montserrat', sans-serif;
  }
  
  .mobile-spacer {
  width:100%;border:0px solid red;
  }
  
  
  /* Responsive layout - when the screen is less than 800px wide, make the two columns stack on top of each other instead of next to each other */
  @media screen and (max-width: 800px) {
  
      .midcolumn {   
      width: 100%;
      padding: 0;
      margin-left: 0%;
      }
  
  
.menu-separator {
  display: block;
  margin-left:0px;
}

.card {
  background-color: transparent;
  width: 100%;
  padding-right: 0px;
}

    .img2 {
      width:0px;
    padding: 0px;
    border-spacing: 0px;
    }
  
     .badge2{
      width: 100%;
      height: 100%;
        float: right;
        background: #03080f;
        border-spacing: 0px;
        padding:10px;
    }
  
    .circle {
      float: right;
    }

      .text2 {
         width: 100%;
         background-color: transparent;
      }
  
      .content{
         background-color: #0e1a2b;
      }

      .circle {
         margin-top:5px;
      }
  
  }
  
  </style>

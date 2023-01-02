<h1>footerMenu</h1>
<p>this  branch for the menuheader component as it contains following files</p>






 <h1 style="border:0px !important"><strong>&nbsp &nbsp&nbsp &nbspMainFooter.vue<strong></h1>
 
 
<span>this is our main Container for the header menu holds two subcontainers for desktop and mobile</span>
  
 <h1 style="border:0px !important"><strong>&nbsp &nbsp&nbsp &nbsp props <strong></h1>


   <table>
    <tr><td>NAME</td><td>childprops</td><td>TYPE</td><td>DESCRIPTION</td></tr>
    <tr><td>HeaderOptions</td><td></td><td>Object</td><td>Holds all menu data we want as following</td></tr>
       <tr></td><td><td>logo</td><td>String</td><td>the logo filename  (if you are not  saving images src/assets please got to headerMobile.vue and HeaderDesktop.vue and changepath in computed method  getImgSrc) </td></tr>
       <tr></td><td><td>menu</td><td>Array of Objects</td><td>holds each menu item details as following
 <ul>
  <li>title:String=> name of each menu item <li>
  <li>list:Array of objects=> contains submenu items details as following
   <ul>
   <li>
    title:String=> submenu item title</li>
    <li>url:String=> url for each submenu item</li> 
     </ul></li>
   </ul>
  
  
 </td></tr>
    
      <tr></td><td><td>menu</td><td>Array of Objects</td><td>holds each menu item details as following
 <ul>
  <li>title:String=> name of each menu item <li>
  <li>list:Array of objects=> contains submenu items details as following
   <ul>
   <li>
    title:String=> submenu item title</li>
    <li>url:String=> url for each submenu item</li> 
     </ul></li>
   </ul>
  
  
 </td></tr>
 

    
 
   <tr><td></td><td>cart</td><td>Object</td><td> contain cart info as following 
     <ul>
          <li>
    count:Number=> count of items in cart</li>
    <li>url:String=> url for cart</li>
    <li>image:String=> icon filename for cart</li></ul></td>   </tr>  <tr></td><td><td>mobile_menu_icon </td><td>String</td><td>the menu icon filename  (if you are not  saving images src/assets please got to headerMobile.vueand changepath in computed method  getIconSrc) </td></tr>
 
 
       
     
 
 
   </table>

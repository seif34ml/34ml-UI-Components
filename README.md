<h1>footerMenu</h1>
<p>this  branch for the menufooter component as it contains following files</p>






 <h1 style="border:0px !important"><strong>&nbsp &nbsp&nbsp &nbspMainFooter.vue<strong></h1>
 
 
<span>this is our main Container for the header menu holds two subcontainers for desktop and mobile</span>
  
 <h1 style="border:0px !important"><strong>&nbsp &nbsp&nbsp &nbsp props <strong></h1>


   <table>
    <tr><td>NAME</td><td>childprops</td><td>TYPE</td><td>DESCRIPTION</td></tr>
    <tr><td>footerOptions</td><td></td><td>Object</td><td>Holds all menu data we want as following</td></tr>
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
 </ul></td></tr>
  

  
 </td></tr>
  <tr><td></td><td>AppStore</td><td>Array of Objects</td><td>holds App Store imgs and links for each as following
   <ul>
     
    url:String=> url for store
    img:String=> icon filename for storelink
 </ul>
   </td></tr>
    
  <tr><td></td><td>socialMedia</td><td>Array of Objects</td><td>holds social media imgs and links for each as following
   <ul>
     
    url:String=> url for social media platform
    img:String=> icon filename for socialmedia platform link<</ul>
   </td></tr>
 

 
 <tr></td><td><td>copyrightHtml</td><td>String</td><td>represent the Html of copyrights message</td></tr>
 
       
     
 
 
 
   </table>

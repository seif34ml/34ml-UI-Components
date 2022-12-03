<h1>headerMenu</h1>
<p>this  branch for the menuheader component as it contains following files</p>






 <h1 style="border:0px !important"><strong>&nbsp &nbsp&nbsp &nbspMainHeader.vue<strong></h1>
   <img src="https://user-images.githubusercontent.com/116160182/205442350-ad8ade4a-d974-4428-95f6-5afda69932dd.png"/>
<img src="https://user-images.githubusercontent.com/116160182/205442352-abad92b1-cf23-4390-99ab-bcba303e835e.png"/>
<img src="https://user-images.githubusercontent.com/116160182/205442354-0240ab23-d762-47f6-bc99-e9080b101221.png"/>
 
<span>this is our main Container for the header menu holds two subcontainers for desktop and mobile</span>
  
 <h1 style="border:0px !important"><strong>&nbsp &nbsp&nbsp &nbsp props <strong></h1>


   <table>
    <tr><td>NAME</td><td>childprops</td><td>TYPE</td><td>DESCRIPTION</td></tr>
    <tr><td>HeaderOptions</td><td></td><td>Object</td><td>Holds all menu data we want as following</td></tr>
       <tr></td><td><td>logo</td><td>String</td><td>the logo filename  (if you are not  saving images src/assets please got to headerMobile.vue and HeaderDesktop.vue and changepath in computed method  getImgSrc) </td></tr>
       <tr></td><td><td>menu</td><td>Array of Objects</td><td>holds each menu item details as following
 <ul>
  <li>main_title:String=> name of each menu item <li>
  <li>url:String=> url of each menu item <li>
  <li>has_submenu:Boolen=> check if menu item contains submenu <li>
  <li>submenu:Array of objects=> contains submenu items details as following
   <ul>
   <li>
    title:String=> submenu item title</li>
    <li>url:String=> url for each submenu item</li> 
    <li>list:Array of Objects=>list of items in each submenu item includes</li>
     <ul>
          <li>
    title:String=> submenu item title</li>
    <li>url:String=> url for each submenu item</li> 
    </ul>
   </ul>
  
  </ul>
 </td></tr>
    <tr><td></td><td>menu_submenu_style</td><td>Boolean</td><td>if true the dropdown style style will be set to be as rahetbally menu style else default dropdon menu style will be applied</td></tr>
 
 
  <tr>
     <td></td>
     <td>languageOptions</td> 
     <td>Object</td>
   <td>includes languages info used in localization as following
   <ul>
    <li> selectedLanguage:String=> determine selected language by code example "en for english"</li>
    <li> languages:Array of objects=> determine languages details as following
     <ul>
      <li>languageName:String=> determine the language name example english</li>
       <li>code:String=> determine the language code </li>
     </ul>
    </li>
    <\ul></td></tr>
    
 
   <tr><td></td><td>cart</td><td>Object</td><td> contain cart info as following 
     <ul>
          <li>
    count:Number=> count of items in cart</li>
    <li>url:String=> url for cart</li>
    <li>image:String=> icon filename for cart</li></ul></td>   </tr>  <tr></td><td><td>mobile_menu_icon </td><td>String</td><td>the menu icon filename  (if you are not  saving images src/assets please got to headerMobile.vueand changepath in computed method  getIconSrc) </td></tr>
 
 
       
     
 
 
   </table>






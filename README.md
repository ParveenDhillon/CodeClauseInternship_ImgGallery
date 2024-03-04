<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Gallery</title>
    <link rel="stylesheet" href="iproject.css">
    
</head>
<body>
    
<section class="mygallry">
    <div class="container">
        <div class="row">
            <div class="gallery-filter">
              <span class="filter-item active" data-filter="all">all</span>
              <span class="filter-item" data-filter="watch">Bats</span>
              <span class="filter-item" data-filter="headphone">Balls</span>
              <span class="filter-item" data-filter="camera">T-shirts</span>
              <span class="filter-item" data-filter="phone">Shoes</span>
               
            </div>
           </div>
    </div>
<div class="row">
<!--1st gallery item start -->
    <div class="gallery-item Bats">
        <div class="gallery-item-inner">
           <img src="cricket bat.jpg" height="300px" alt="Bats">
        </div>
      </div>

<!--2nd gallery item start -->
      <div class="gallery-item Balls">
        <div class="gallery-item-inner">
          <img src="ball1.jpg" height="300px" alt="Balls">
        </div>

       </div>
       
<!--3rd gallery item start -->
 <div class="gallery-item T-shirts">
    <div class="gallery-item-inner">
      <img src="tshirt1.jpg" height="300px" alt="T-shirts">
    </div>
   </div>
  
  
  <!--4th gallery item start -->
   <div class="gallery-item Bats">
    <div class="gallery-item-inner">
      <img src="bat2.jpg" height="300px" alt="Bats">
    </div>
   </div>
  
  
  <!--5th gallery item start -->
   <div class="gallery-item Balls">
     <div class="gallery-item-inner">
       <img src="ball2.jpg" height="300px" alt="Balls">
     </div>
   </div>
  
  
   <!--6th gallery item end -->
   <div class="gallery-item T-shirts">
     <div class="gallery-item-inner">
       <img src="tshirt3.jpg" height="300px" alt="T-shirts">
     </div>
   </div>
  
  
  <!--7th gallery item end -->
   <div class="gallery-item Shoes">
     <div class="gallery-item-inner">
       <img src="shoes3.avif" height="350px" alt="Shoes">
     </div>
   </div>
  
  
  <!--8th gallery item end -->
   <div class="gallery-item tshirt">
    <div class="gallery-item-inner">
      <img src="accers1.jpg" height="350px" alt="accers">
    </div>
   </div>
  
  
   <!--9th gallery item start -->
   <div class="gallery-item shoes">
     <div class="gallery-item-inner">
       <img src="shoes2.avif" height="350px" alt="shoes">
     </div>
   </div>
</div>
</section>

<script type="text/javascript">
const filterContainer =
 document.querySelector(".gallery-filter");
const galleryItems = 
document.querySelectorAll(".gallery-item");

filterContainer.addEventListener("click", (event) =>{
    if(event.target.classList.contains("filter-item")){
 
      // deactivate existing active 'filter-item'
     filterContainer.querySelector(".active").classList.remove("active");
 
      // activate new 'filter-item'
     event.target.classList.add("active");
 
     const filterValue = event.target.getAttribute("data-filter");
 
     galleryItems.forEach((item) =>{
 
        if(item.classList.contains(filterValue) || filterValue === 'all'){
         item.classList.remove("hide");
          item.classList.add("show");
        }
 
        else{
         item.classList.remove("show");
         item.classList.add("hide");
        }
 
      });
    }
  });
</script>
</body>
</html>

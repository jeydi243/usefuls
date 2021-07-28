# Index Linux tips
## Methode 1: Set background stripe in css (not animated)
```{.css}
background-image: linear-gradient(45deg, #ffffff 25%, #f0f0f0 25%, #f0f0f0 50%, #ffffff 50%, #ffffff 75%, #f0f0f0 75%, #f0f0f0 100%);
background-size: 40.00px 40.00px;
```


## Methode 2: Set background stripe in css (not animated)
1. In html
   ```{.html}
   <div class="background"></div>
   ```
2. In css
   ```{.css}
   .background {
        width: 100%;
        height: 400px;
        display: block;
        // horizontal 3 color sripes
        //background: linear-gradient(#fb3 33.3%, #58a 0, #58a 66.6%, yellowgreen 0);
        //background-size: 100% 50px;
        
        // vertical 2 color stripes
        //background: linear-gradient(to right, #fb3 50%, #58a 0);
        //background-size: 60px 100%;
        
        //diagonal stripes a failed one though
        //background: linear-gradient(45deg, #fb3 50%, #58a 0);
        //background-size:30px 30px;
        
        
        //diagonal stripes a good one!
        //background: linear-gradient(45deg, 
            //#fb3 25%, #58a 0, #58a 50%, 
            //#fb3 0, #fb3 75%, #58a 0);
        //background-size: 100px 100px;
        
        // other diagonal stripes
        //background: repeating-linear-gradient(60deg, #fb3, #fb3 12px, #58a 0, #58a 50px);
        
        //diagonal with traparent overlay
        background: #58a;
        background-image: repeating-linear-gradient(30deg, rgba(#FFF, .2), rgba(#FFF, .2) 30px, transparent 0, transparent 60px);

    }
   ```
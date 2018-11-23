
### Responsive banner images
```html
<picture>
  <source media="(max-width: 659px)" srcset="banner-portrait-sm">
  <source media="(min-width: 660px) and (max-width:999px)"
    srcset="banner-landscape-md.jpg 1x,
            banner-landscape-md-2x.jpg 2x,
            banner-landscape-md-3x.jpg 3x">
 <source media="(min-width: 1000px)"
    srcset="banner-landscape-lg.jpg,
            banner-landscape-lg-2x.jpg 2x,
            banner-landscape-lg-3x.jpg 3x">
 <img src="fallback.jpg"
      srcset="head-fb-2x.jpg 2x"
      alt="a head carved out of wood">
</picture>
```

### Combined Media and pixel density
```html
<figure>
    <picture>
      <source media="(min-width: 750px)"
              srcset="images/horses-1600_large_2x.jpg 2x,
                      images/horses-800_large_1x.jpg" />
      <source media="(min-width: 500px)"
              srcset="images/horses_medium.jpg" />
      <img src="images/horses_small.jpg"
           alt="Horses in Hawaii">
    </picture>
    <figcaption>Horses in Hawaii</figcaption>
</figure>
```

### Combined Media and width/size attribute
```html
<picture>
 <source media="(min-width: 800px)"
         sizes="80vw"
         srcset="lighthouse-landscape-640.jpg 640w,
                 lighthouse-landscape-1280.jpg 1280w,
                 lighthouse-landscape-2560.jpg 2560w">
 <img src="lighthouse-160.jpg" alt="lighthouse"
      sizes="80vw"
      srcset="lighthouse-160.jpg 160w,
              lighthouse-320.jpg 320w,
              lighthouse-640.jpg 640w,
              lighthouse-1280.jpg 1280w">
</picture>
```

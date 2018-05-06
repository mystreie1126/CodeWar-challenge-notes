# Responsive SASS notes 

### 1. Using `mixins`to write effective media quries 

```
@mixin respond($breakpoint){
    @if $breakpoint == phone{
        @media (max-width:600px){@content};
    }
     @if $breakpoint == tab_port{
        @media (max-width:900px){@content};
    }
    
    html{
     font-size:62.5%
       @include respond(phone){
         font-size: 30%;
       }
       @include respond(tab_port){
         font-size: 50%;
       }
  }
```

### 2. `em` and `rem` in media quries are not effected by root font-size setting, `em` is the best option for font-size in media quires


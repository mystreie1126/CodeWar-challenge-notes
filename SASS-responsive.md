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

**alwayas larger media queries place before the smallers**
```
	font-size: 62.5%; //1rem = 10px 10px/16px = 62.5%;

	@include respond(tab-land){ //width < 900px
		font-size: 56.25%; //1rem = 9px 9px/16px 
	}

	@include respond(tab-port){ //width < 600px
		font-size: 50%; //1rem = 8px 8px/16px
	}
```


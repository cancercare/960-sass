# 960-sass

## What?
A collection of [SASS mixins](http://sass-lang.com/) (specifically, SCSS) to allow you to easily and more-sematically use [960.gs](http://960.gs/) for fixed or flexible grids.

## Why?
Because using non-semantic, strictly-presentational grid classes like `<div class="grid_4 alpha">` rubs me the wrong way, and because SASS is *awesome*.

## How?
First, choose whether you want a flexible grid or a fixed grid, and save the appropriate file in your SASS directory.

Then, in your main SASS file, you can do things like this:

    @import "flexible_grid";
    
    section{
      @include container_12;
      
      article{
        @include grid(8);
        
        img{
          @include grid(2);
          @include alpha;
        }
        
        p{
          @include grid(6);
          @include omega;
        }
        
      }
      
      nav{
        @include grid(4);
        @include push(8);
      }
      
    }

Just like 960.gs, included options are 

 - `container_12` 
 - `grid(#)`
 - `push(#)`
 - `pull(#)`
 - `prefix(#)`
 - `suffix(#)`
 - `alpha`
 - `omega`

## Where?
You can see it in action in [the stylesheet source of tjschuck.com](https://github.com/tjschuck/tjschuck.com/tree/master/css/sass)

## Who?
T.J. Schuck   
[http://tjschuck.com](http://tjschuck.com)   
[@tjschuck](http://twitter.com/tjschuck)   

## License
Copyright &copy; 2011 T.J. Schuck  
Released under the [MIT license](http://www.opensource.org/licenses/MIT).

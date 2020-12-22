Keeps track of time and memory and displays it sort of nicely for you.

I wrote it quickly. It seems to work. It's been helpful. If you want to use it or contribute, feel free. I'm sure there are more comprehensive solutions out there.

Basic Usage:

```php
use JMasci\Time_Mem_Tracker;

$track = new Time_Mem_Tracker();

some_code();

$track->breakpoint();

some_more_code();

$track->breakpoint();

some_more_code();

$track->breakpoint();

echo $track->display_summary();
```

Gets you something like:

```
                     Time                 Mem                  Peak Mem            
START                1608596511.0759      9,873,360            10,020,344          
copy                 +0.028213024139404   +904                 10,020,344          
unlink               +0.0014500617980957  +416                 10,020,344          
fopen                +1.0013580322266E-5  +496                 10,020,344          
image_resize         +1.3510720729828     +93,422,672          168,335,224         
image_resize         +1.343220949173      +496                 261,757,816         
image_resize         +0.89372611045837    +496                 261,758,312         
END                  1608596514.6936      103,298,840          261,758,312         
TOTAL_DIFF           +3.617692232132      +93,425,480          +251,737,968    
```

There's 3 options for displaying, or you can write your own. See the code for more info.
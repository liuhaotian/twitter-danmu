# twitter-danmu

Play youtube with damu using realtime twitter search results

## HOWTO

* Add the following bookmarklet in your browser
* Copy the Youtube Video Id that you want to play (Live video is also supported)
* Search **live** tweets using keywords or hashtag on [Twitter](https://twitter.com/hashtag/nevertrump?f=tweets)
* Click the bookmarklet and paste Video Id in prompt

## Bookmarklet

```javascript
javascript:$('body').css('overflow-x', 'hidden');var videoId = prompt("Please enter the YouTube Id", "FpkDL3G7AoY");$('#page-container h1').html('<iframe height="'+(innerHeight-$('.global-nav-inner').innerHeight())+'" width="'+$('#page-container h1').innerWidth()+'" data-src="https://www.youtube.com/embed/'+videoId+'" frameborder="0" scrolling="no" allowtransparency="true" src="https://www.youtube.com/embed/'+videoId+'?autoplay=1&amp;auto_play=true"></iframe><ul><li class="popup" style="position:absolute; top:50px; text-align: left;"></li><li class="popup" style="position:absolute; top:75px; text-align: left;"></li><li class="popup" style="position:absolute; top:100px; text-align: left;"></li></li><li class="popup" style="position:absolute; top:125px; text-align: left;"></li></li><li class="popup" style="position:absolute; top:150px; text-align: left;"></li></li><li class="popup" style="position:absolute; top:175px; text-align: left;"></li></li><li class="popup" style="position:absolute; top:200px; text-align: left;"></li></ul>');setInterval(function(){$('.new-tweets-bar').click();$('.popup:empty').first().each(function(idx, el){tweet = $('.js-stream-item').first();$(el).animate({left: innerWidth}, 0).html($(tweet).find('.tweet-text').text());$(el).animate({left: -$(el).innerWidth()}, ($(el).innerWidth()+innerWidth)*(10*Math.random()+3), 'linear',function(){$(el).html('')});tweet.remove();});}, 1000);
```

## WHAT IS DANMU

[Google danmu](https://www.google.com/search?q=danmu)

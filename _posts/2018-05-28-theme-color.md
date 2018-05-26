---
layout: post
title: "Theme Color"
date: 2018-05-28
tags: [development]
---

Just found out a way of switching Theme Color of the Android Chrome. If you don't know what is Theme Color, this is the color of the Chrome toolbar, this is customizable to match with the theme of your web site.

![Theme Color](https://developers.google.com/web/updates/images/2014/11/theme-color-ss.png)

There is another cool way of using the Theme Color with animation. I am using an animation script to drive a flashing alert effect, on site error. You can try out [here](/no-such-page.html) .

Script of the Theme Color Animation Effect
```
    		<script>
			var themeColorTest = new function () {
				var me = this;
				me.init = function () {
					//$title = document.querySelector("title");
					$themeColor = document.querySelector("meta[name='theme-color']");
					startAnim();
				};
				function startAnim() {
					if($themeColor.content === '#fc4445') {
						$themeColor.content = '#ff0000';
					} else {
						$themeColor.content = '#fc4445';
					}
					setTimeout(startAnim, 500);
				}
			}
			themeColorTest.init();
		</script>
```

---
layout: default
title: Welcome
---

# The Long Loneliness

## Firstly, I invited you to enjoy the famous song "Time" by Pink Floyd.

_Tips: Click to pause or resume the music playing._

<script>
    var YtbControls = {
        __playstart__ : performance.now(),
        __playedSec: 0,
        __onFrameLoaded: () => {
        },
        __onFrameClick : (event) => {
            const mask = event.currentTarget;
            const datas = mask.dataset;
            const iframe= mask.previousElementSibling;

            let autoPlay = datas['autoplay'];
            autoPlay = autoPlay === '1' ? '0' : '1';

            const offset = Number(datas["start"]);

            datas['autoplay'] = autoPlay;

            if (autoPlay === '0') {
                const now = performance.now();
                YtbControls.__playedSec += Math.ceil((now - YtbControls.__playstart__) / 1000);
                YtbControls.__playstart__ = now;
            }
      
            iframe.src = `https://www.youtube.com/embed/yl-Ms_ek-kE?si=jV1KTgHVw8-2jjFR&amp;controls=0&amp;autoplay=${autoPlay}&amp;start=${offset + YtbControls.__playedSec}`;
        }
    }
</script>

<div class="Iframe">
    <iframe onload="YtbControls.__onFrameLoaded()" width="724" height="407"  src="https://www.youtube.com/embed/yl-Ms_ek-kE?si=jV1KTgHVw8-2jjFR&amp;controls=0&amp;autoplay=1&amp;start=20" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    <div class="Iframe__mask" data-autoplay="1" data-start="20" onclick="YtbControls.__onFrameClick(event)">
        <a id="Switcher" class="switcher" href="#"></a>
        <div class="screen glitch">
            <div class="clock is-off"><span class="time" data-time=""></span></div>
            <div class="figure"></div>
            <div class="figure-mask"></div>
        </div>
    </div>
</div>

{%- include time.html -%}

## Welcome

Where are you from? What do you do for living? Are you single or married? Are you feeling lonely? Or, you just get better now, but, you still remember that period of hard time you were feeling lonely very much. What's your story? Will you tell it to me?

<img src="https://cdn.midjourney.com/cee7d707-c407-484b-82b2-7b866ec7e689/0_2.webp" class="image">

Welcome!

I created this site to **share** the feeling of loneliness from human beings. But, furthermore, I also hope one day a warm community would be formed to comfort the lonely hearts all around the world.

What motivates me to do this is _I AM LONELY_.

## The story of me in brief

I am from the mainland of China, a man, 35 years old, still be single, a programmer with 10 years' experience. I've been sick, a sickness I'm ashamed to tell my friends and family, since 4 years ago. I know I could be loved and welcomed by many of my colleagues and girls. However, the disease makes me afraid to socialize with them too much. So, I keep a distance, both psychologically and physically, away from them to live in a solitude way. Few people can talk to me, and no girl will come to me to say hello, for which I feel sorry.

(I'll keep writing down more details...)

## To know me more,

1. [about](https://zhangxinghai.cn/about-en)
2. [singhi's blog](https://zhangxinghai.cn)
3. [videos](https://www.youtube.com/channel/UCOvEajUHgigi_lO3wKgpJvw)

## The story of you

If you will, you can write down your story of being lonely. Don't worry about your privacy, you don't need to say anything of your private information. I don't know who you are, and you don't know me either.

But, let's be honest first.

Check my email address (<label>zhangxinghai79@gmail.com</label>), and tell me your story by composing an email to me, or directly filling the form. I will publish it on the page, then every lonely one will read it and connect to you. It may help to ease your pain.

Keep in mind, you are not alone! At least, I am here with you.

## Share with me, anything. Yes, I'm hearing you, really!

My Email: zhangxinghai79@gmail.com

## Alternatively, fill the form to Tell Your Story

{% include post.html %}
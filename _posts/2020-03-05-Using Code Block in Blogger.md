---
title: "Using Code Block in Blogger"
date: 2020-03-05T00:00:00-00:00
categories:
  - Web
tags:
  - Blogger
---

I have done some researching on how to use code blocks in blogger and I found this [awesome tutorial article](http://kdh74616.blogspot.com/2017/03/code-display-block-fixes-strange-ie.html) in Chinese.

I tried the steps they provide, and it work perfectly.

So I'm just gonna make the steps more clear with some screen shots!

### What you should do
1. Go to Prismjs.com and download both js and css files of the theme you like
2. Paste the content of the css file to: Theme->Customise->Advanced->Add Css->Add custom CSS
![step2]({{ site.baseurl }}/assets/images/2020/03/20200301.PNG)
![step2]({{ site.baseurl }}/assets/images/2020/03/20200302.PNG)
3. Wrap the content of prism.js with <script></script>
4. Paste it to Layout->Sidebar->Add a Gadget->HTML/Javascript
![step4]({{ site.baseurl }}/assets/images/2020/03/20200303.PNG)
![step4]({{ site.baseurl }}/assets/images/2020/03/20200304.PNG)

### How to use
when you write the article, go to html mode and paste the following dom.
```
<pre><code class="language-javascript">
...
Your code here
...
</code></pre>
```

it will looks like this:
```
Your code here
```

and with some code content:
```javascript
let helloString='Hello World!';
console.log(helloString);
console.log('Yoda!');
```
There you go!
Enjoy!











# Hosting Fonts on Github for Production

While browsing r/DND I came across [someone trying to figure out a way to use a custom font](https://www.reddit.com/r/DnD/comments/ayv6ot/roll20_handout_templates/eietuij/?context=3) for an online DND styled book generator. Since the generator allowed the use of html/css code, I decided to find a way to do such a thing. 

Essentially this is a way to host fonts on Github and use them else where. Why would you want to do this? I'm not sure but here you are more than likely looking for this solution, well hopefully. 

Now you can either read below or read the Reddit post to figure out how to do this.


## How to do this

<ul>
 <li>Find the font you want and download it.</li>

 <li>Use Transfonter or some other @font-face generator as long as you have two file types, woff and woff2. </li>
 <ul>
 <li>Upload the font you downloaded </li>
 <li>Leave everything as is</li></ul>

 <li>Upload the files from Transfonter to a new repository in Github.</li>

 <li>For each font file, there should be two (woff and woff2), copy their link and paste each at GitHack.</li>

 <li>Copy the link on the left side or "the link for production." That link, for each file, goes into spreadsheet.css. woff link goes with woff and woff2 link goes with woff2. Hit commit and let it do its thing.</li>

 <li>Now go to the spreadsheet.css file and copy its link. We're going back to GitHack and paste it. Then copy the link on the left for "production."</li>

 <li>Now we move to where you want the font to be used (at least this part is for HTML). Here's the code. Everything with a [word] is to be replaced by your stuff.</li>
</ul>

```html
<link href="[link_to_cdn_of_stylesheet" rel="stylesheet">

<style> .font { font-family: '[font_family_Name]'!important; } </style>
```

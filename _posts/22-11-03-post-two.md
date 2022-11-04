---
title: Swift UI Lesson 1
author: cotes
date: 2022-11-03 12:00:00 +0800
layout: page
categories: [Javascript Courses ,lesson 1]
tags: [typography]
math: true
mermaid: true
image:
  path: /assets/dc.png
  width: 800
  height: 500
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

<style>

/* FUNC NAME */
html:not([data-mode]) .highlight .nf, html:not([data-mode]) .highlight .nx, html[data-mode="light"] .highlight .language-swift .nf, .language-javascript .nx{
    color:#a6e22e ;
  font-weight:normal;
}

.highlight .p {
color:white
}

html:not([data-mode]) .highlight .nv, html[data-mode="light"] .highlight .language-swift   .nv {
    color: white;
    font-weight:normal;
}

/* FUNC DECLARATION */
html:not([data-mode]) .highlight .kd, html[data-mode="light"] .highlight .language-swift   .kd {
    color: #66d9ef;
    font-weight:normal;
}
/* SELF */
html:not([data-mode]) .highlight .kt, html[data-mode="light"] .highlight .language-swift .kt {
  color: #1ABC9C;
}

html:not([data-mode]) .highlight .k, html[data-mode="light"] .highlight .language-swift .k {
    color: #66d9ef;
   font-weight:normal;
}

/* DOT */
html:not([data-mode]) .highlight .o, html[data-mode="light"] .highlight .language-swift .k {
  color: #f92672;
   font-weight:bold;
}


 html[data-mode="dark"] figure.highlight, .highlight, .highlighter-rouge {
   background:#252525;;
   /* border:1px solid #eee */
}

/* TEXT INSIDE QUOTES */
html:not([data-mode]) .highlight .s, html[data-mode="light"] .highlight .s{
  color: #FA6E23;
  font-weight:bold;
}

 pre {
    display: block;
    font-size: 87.5%;
    color: white;
}




</style>

## Paragraph

Quisque egestas convallis ipsum, ut sollicitudin risus tincidunt a. Maecenas interdum malesuada egestas. Duis consectetur porta risus, sit amet vulputate urna facilisis ac. Phasellus semper dui non purus ultrices sodales. Aliquam ante lorem, ornare a feugiat ac, finibus nec mauris. Vivamus ut tristique nisi. Sed vel leo vulputate, efficitur risus non, posuere mi. Nullam tincidunt bibendum rutrum. Proin commodo ornare sapien. Vivamus interdum diam sed sapien blandit, sit amet aliquam risus mattis. Nullam arcu turpis, mollis quis laoreet at, placerat id nibh. Suspendisse venenatis eros eros.

---


<h2 data-toc-skip>Code Blocks</h2>


```swift
 public func updatePlayingTime(){
        self.currentPlayerTimeSeconds[self.currentTrack] = self.getCurrentTimeSeconds()
        self.currentPlayerTimePercents[self.currentTrack] = self.getCurrentTimePercents()
        self.currentTrackDuration = self.getTrackDuration()
    }
    
    private func onTrackFinshed() -> Void {
        didPlayFinishedSubscription =  self.trackFinishPublisher.sink{ value in
            KLOG(String(describing: value))
            /* IF USER SET maxPlayListRange VARIABLE IT WILL STOP PLAYER ON TRACK = maxPlayListRange  */
            if let _ = self.maxPlayListRange {
                self.currentTrack == self.maxPlayListRange ? self.stopAllTracks() :  self.playBack()
            } else {
                self.playBack()
                return
            }
        }
    }
```

```swift
 Text("#All Tracks")
   .font(.title)
   .foregroundColor(Color("kelteno_font"))
   .fontWeight(.bold)
   .frame(maxWidth: .infinity, alignment: titlesAlignment)

```


```javascript

let Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name); // "Rectangle"

// named
Rectangle = class Rectangle2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name); // "Rectangle2"

```

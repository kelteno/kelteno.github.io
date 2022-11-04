---
title: Text and Typography
author: cotes
date: 2022-11-03 12:00:00 +0800
layout: page
categories: [Demo]
tags: [typography]
math: true
mermaid: true
image:
  path: /commons/devices-mockup.png
  width: 800
  height: 500
  alt: Responsive rendering of Chirpy theme on multiple devices.
---


This post is to show Markdown syntax rendering on [**Chirpy**](https://github.com/cotes2020/jekyll-theme-chirpy/fork), you can also use it as an example of writing. Now, let's start looking at text and typography.


## Titles
---
# H1 - heading

<h2 data-toc-skip>H2 - heading</h2>

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


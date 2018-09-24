# Working with HTML5 Media

## Problem Statement

The internet is a highly interactive environment, with almost as many different
devices and platforms as users. As HTML authors, we might be given a media file
and be told to put it on the internet. How can we display media inside of a web
page and make sure that it's viewable to the most people possible on the most
devices?

## Overview

1.  Demonstrate how to embed audio elements in HTML5
2.  Demonstrate how to embed video elements in HTML5
3.  Link to audio and video converters

## Demonstrate How to Embed Audio Elements in HTML5

To include audio in a website, use the `<audio>` element. Inside the element,
we provide `<source>` elements whose `src` attributes point to a file on the
server and whose `type` attributes specify what type of media it is.

Let's look at an example:

```
<audio controls>
  <source src="purrr.mp3" type="audio/mp3">
  <source src="purrr.ogg" type="audio/ogg">
  <p>Sorry your browser doesn't support HTML5 Audio! Please <a href="http://browsehappy.com/?locale=en">upgrade your browser</a>.</p>
</audio>
```

On the first line we open the `<audio>` tag with the `controls` attribute
present. This displays the audio controls to start and pause playback, adjust
the recording's volume, and other standard audio functions. The presence of the
`controls` attribute name tells the browser to display the control panel. There
are optional attributes you can provide such as `autoplay` and `loop`. These
start the audio on page load and repeat the audio after it ends. The
[documentation][audio] lists all available options.

In lines two and three, we provide two different source files for playback. If
the browser does not recognize the first file type, it will ignore it and move
on to the next. If neither of the formats are supported it will instead display
the message on line four. If the browser is able to play one of the source
files it will ignore any other code below until it reaches the closing
`</audio>` tag.

## Demonstrate How To Embed Video Elements in HTML5

Embedding a video is very similar to embedding audio. This can be done by
including the `<video>` tag. Inside the video tag are source tags that point to
the location of the video file formats and specify their MIME types.

```
<video controls>
  <source src="real-estate.mp4" type="video/mp4">
  <source src="real-estate.ogv" type="video/ogg">
  <p>Sorry your browser doesn't support HTML5 Video! Please <a href="http://browsehappy.com/?locale=en">upgrade your browser</a>.</p>
</video>
```

Like `<audio>`, we will open the `<video>` tag with the controls attribute.
For the full list of accepted attributes, you can check the [MDN documentation][video].

On lines two and three we provide two different source files for playback. If
the browser does not recognize the first filetype it will ignore it and move on
to the next as it does for the audio element. If neither of the
formats are supported it will display the message instead on line four. If
the browser is able to play one of the source files, it will. The others
sources within the `<video>` tag will be ignored.

## Link to Audio and Video Converters

In order to provide a wide variety of different file types, we'll need to
convert our original files. There are a number of free tools that have been
trusted to convert audio files when needed.
[MediaHuman - Free Audio Converter][converter] and
[Audacity - Free Audio Editor/Converter][audacity] are
two we recommend.

## Conclusion

With `audio` and `video` tags, the W3C gives us an open way to ensure that
media remain accessible and open to all platforms.

[audio]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio
[video]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video
[converter]: http://www.mediahuman.com/audio-converter/
[audacity]: https://sourceforge.net/projects/audacity/

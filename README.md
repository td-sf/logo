# logo
assets for logo and reels!

## Project overview

<img src="readme_images/tdsf_project_preview.png" width="1000">

I built the logo using Keynote, the default MacOS PowerPoint alternative.

These are the `.key` files in the `assets/` directory.

Confusingly, I'm also using `RGB Key` TOPs in TouchDesigner.

I use RGB keying so that different layers can be made transparent based on their color.
and replaced with video or images using `Composite` TOPs.


## RGB keying guide

<img src="rgb_keying_guide.png" width="1000">

To isolate the *white elements* of the image, use an `RGB Key`, 
and increase `Red Min` or `Blue Min` slightly, until the white is the only non-transparent layer. 

You can then use a `Composite` TOP set to `Multiply` to replace the white elements with any video.

To *isolate the green background* with an `RGB Key` TOP,
increase `Green Min` and decrease `Red Max` slightly,
until now the green background is the only thing that's non-transparent.

Make it white with an `HSV Adjust` TOP by setting `Saturation Multiplier` to 0.
Then you can replace this layer with any video using a `Composite` TOP with operation set to `Multiply`


And to *isolate the black graphic elements*, decrease the `RGB Key`'s `Green Max` parameter.  


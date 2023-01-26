# Face Forward v1

_Last edited: 2023-01-26 by [Peter Kaminski](mailto:kaminski@istori.com). Please email me with comments or questions._  
[permalink](https://peterkaminski.wiki/face_forward_v1) to this page

To see each of the 144 synthesized human faces of Face Forward v1 at full 768x512 pixel (0.3 megapixel) resolution, visit this Flickr album: [Face Forward v1 - Flickr](https://www.flickr.com/photos/pixelthesia/sets/72177720305544773).

Here is a montage of the 144 synthesized human faces of Face Forward v1. See below for more information about the project.

![[Face Forward v1 montage.jpg]]

Face Forward v1 is a small project to briefly assess how good current versions of Stable Diffusion and wavymulder's Analog Diffusion model are at synthesizing portraits of human faces.

I wanted to generate reasonably realistic faces, with a diversity of types of faces and photography styles. I wanted to see how good the faces would be without anything fancy; so I used fairly minimal prompts, didn't use fancy prompt engineering, didn't use any face improvement post-processing, and didn't upscale the images. Each image is as-generated, no fixes at all.

I cherry picked images that I felt hit sort of a "95%" quality mark. In cherry picking, I included some images that need rectangular cropping to remove stray objects or a duplicate person, because that's an easy transform. I didn't crop the images, so you can see the entire as-generated set. I also included some images that had some incidental problems with non-face objects - hair, hands, jewelry, or background objects. Hiding or masking those things is harder than a rectangular transform, but still not too hard with straightforward image editing techniques.

Out of about 825 images generated, I ended up with 144 images in this "95%" quality range – a ~17.5% yield. Very good, considering.

The biggest problem Stable Diffusion had was generating eyes -- sometimes eye shape, but more often, problems with the iris, pupil, reflections, or bilateral symmetry between both eyes. Many of the images I didn't select would meet my quality bar just by fixing one eye, which would increase the yield by a lot.

None of the images is 100% perfect; they all need touch-up work of one kind or another. But I'm impressed at the number and variety of pretty solid faces. I'm also always amazed at how well complex 3D objects and lighting are synthesized by 2D pixel manipulation, with no real understanding of light or 3D structure. I think some day all virtual photography will use 3D modeling, lighting, and rendering, but for now, even 2D synthesis works very well.

## Technical Details

I used [Draw Things](https://drawthings.ai/) version 1.20230114.2 on a MacBook Pro (14-inch, 2021) with an M1 Max CPU and lots of memory and disk space. Each image took about 35 seconds to generate.

Steps: 35, Sampler: DPM++ 2M Karras, Guidance Scale: 7.5, Size: 768x512, Model: analog_v1_f16.ckpt (wavymulder's [Analog Diffusion](https://huggingface.co/wavymulder/Analog-Diffusion) model, I believe).

## Prompt Keywords

To create the prompts, I used the following keywords in varying combinations. You may not see all of these keywords represented in the 144 faces included in Face Forward v1.

No artist or photographer names were used in any prompt.

A typical prompt: "analog style selfie of a happy, interesting person, masterpiece, matching eyes, sunlight, eye light, bright face, in focus, lens flare".

"analog style" is the activation string for Analog Diffusion, and doesn't count as part of the prompt keywords.

Left to its own devices, the model tended to put beards on men, so I often added "beard" as a negative prompt.

### Gender

man, nonbinary, person, woman

### Facial Appearance

attractive, friendly, handsome, happy, interesting, kind, lovely

### Photo Type / Lighting

bright, close up, close up, eyelight, face, film, headshot, ideal, in focus, lens flare, masterpiece, matching eyes, motion blur, photograph, portrait, selfie, snapshot, sunlight, sunlit

### Ethnicity

african american, american, diverse, eastern european, ethnically diverse, middle eastern, mixed race, native american, northern european, south american, southern european

### Age

middle-aged, old, older, young

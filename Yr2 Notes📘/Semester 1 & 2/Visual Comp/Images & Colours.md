# Images & Colours
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  30-09-2024
> > *Module :* [[Visual Computing]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[]]
> [[]]
> [[]]
> [[]]

--- 
> [!danger]+ *Speed run* 
> Break down of topic 
> > $a)$ -  In general, access pixel $(𝑥,𝑦)$ at address $3×(𝑦×w +𝑥)$ where $w$ is the width in pixel
> >  $ai)$ -  3 comes from byte for each $RGB$ but can be 4 for $RGBO$ (==opacity==)
> > $b)$ - RGB additive & CMY subtractive 
> > $bi)$ - 
> $c)$ - 

---
### Colour spaces 

- **RGB** (Red, Green, Blue) 
	- monitors § 
- **CMY** (Cyan, Magenta, Yellow)
	- printers 
- **HSV/HSL** (Hue, Saturation, Value/Lightness)
	- user-friendly, common for colour pickers in graphics packages 
- **CIEXYZ** and CIE xyY
	- specifying colours and their ranges absolutely

### CMY vs CMYK

$K$ stands for **Key** and is a cheaper way for doing printing jobs. The key value is determined by the negative brightness which is equal to the minimum value of C M or Y 

![[CMYK explanation.png| 400]]


### Brightness 

As seen below, the human vision responds differently to different $\lambda$ of light. Hence the apparent light level $l$ can be worked out using the following equation

![[Greyscale.png| 400]]

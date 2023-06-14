# TexturesPackerTutorial

## Open the tool

- Navigate to the 'TexturesPacker' utility widget which is located in : 'TexturesPacker > Widgets > TexturesPacker'.

- Right click on it and select 'Run Editor Utility Widget'.

![alt text](/src/0.png)

## Using the tool

Once you have opened the tool, you are able to use it to pack textures.

![alt text](/src/1.png)

### Global settings

**Those settings can be changed after texture creation : name, compression settings, virtual texture.**

- **Resolution width / heigh :** This is the resolution x, y of the generated texture. To maximize the tool's effectiveness, make sure that the dimensions chosen are not larger than the dimensions of the textures that will be used for the pack (textures size are displayed in each channel).
- **Texture Name :** The name of the exported texture.
- **Compression Settings :** 
  - If you want to pack RGB (base  color) with Alpha, select 'Default'
  - For an individual channels usage in material (R = occlusion, G = roughness, B = displacement ...), select 'Masks'
  - If you pack as a normal map destination, select 'Normalmap'
  - ...
- **Virtual Texture :** Check it if you want to use this generated asset as virtual texture.

### Per channel settings

Per channel settings (red = R, green = G, blue = B, white = A) :
- **Use Export Path :** Check it if you want to export the generated texture at this texture channel location in content browser. If uncheck, texture will be exported at the root of your content.
- **Multiplier :** Intensity of the current channel texture. Put this value at 0 with the default white texture to make a black channel.
- **Texture :** The texture you want to place in channel.
- **Channel :** Choose a channel to extract from the property 'Texture'.

Then press 'Generate texture'.

## Example

In the example below, I want to pack a RGB (base color) texture with an alpha to make a RGBA texture. I've chosen to keep the resolution similar to my base color (2048) to keep details.
In each RGB channel, I dropped my base color. 
Then dropped the alpha texture in the alpha channel (my alpha texture don't have 'alpha channel', then I choose the red channel to extract pixels).
I want to keep the following naming convention (T_TextureName_TextureDesignation) : T_Foliage_BC
Finally I checked the 'Use Export path' on the red channel to export this texture at the content location of the red channel texture.

![alt text](/src/2.png)
![alt text](/src/3.png)

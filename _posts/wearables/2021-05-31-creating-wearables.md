---
date: 2022-09-15
title: Creating Wearables
redirect_from:
description: Tips and guidelines for creating Decentraland wearables
categories:
  - Decentraland
type: Document
---

### What are wearables?

Wearables are the different clothing items, accessories, and body features that can be used to customize the appearance of a Decentraland avatar. While there are some default wearables available to all users, Decentraland also supports the use of custom wearables. These custom wearables can be created by both brands and users, and are often distributed in competitions and giveaways. Decantraland’s growing marketplace for user-generated content also includes support for wearables, which can be bought, sold, or traded as NFTs (non-fungible tokens).

There’s a growing range of available wearables including cyberpunk themed sneakers, fashionable jackets, fun tophats, and more! All of these stylistic choices give users an exciting and meaningful way to invest in, and express, their own unique personalities. By allowing wearables to be minted, and then sold, as NFTs, Decentraland provides content creators with a fun way to monetize their creative work.

This guide introduces the basics of creating custom 3D models for Decentraland wearables. It explains how the Decentraland “avatar system” works, and it illustrates how to properly model your own wearables.

**Note: this guide assumes that you already have some basic to intermediate knowledge of 3D modeling. If you’re new to 3D modeling, [start here]. Free assets or downloaded assets will not be accepted and may be asked to change.**


### The Decentraland Avatar System

The Decentraland “avatar system” is the broad collection of different body components and subcomponents that can be decorated with custom wearables. These components are:

- Body shape
- Head
  - Head shape
  - Eyebrows
  - Eyes
  - Mouth
- Upper body
- Lower body
- Feet

#### Body shape

The basic form of an avatar. Wearables can be assigned to one, or both, body shapes. Currently, there are two body shapes: A or B. With the addition of Skin category you can build full body outfits with these body shapes and weighting considered to create a unique digital representation in your own art style!

The new update allows for a lot but be mindful to avoid a shape and form that might cause issues with gameplay and platform efficiency. Ensure to include hand, feet and body representation in your design for xompatibility with VR or other clients. Please avoid making things like vehichles, large scale objects (like a chair instead of a person), floating accessories that aren't weighted to the body (like swinging pets, clipping auras). 

As we grow as a creator community, new ways of creating will be realeased!

![image](https://user-images.githubusercontent.com/111281530/184624179-89cd9573-cd35-4af3-b976-78ca2f1d2a25.png)


#### Max Width, Height and Depth of the Wearables
To avoid other users having issues in game, there is a maximum size restriction for wearables. This will avoid screens being blocked, events having issues and gamified events not working well. Minimum size is the base structure of the armature.

**`Height: 2.42 m`**

**`Width: 2,42 m`**

**`Depth: 1,4 m`**

![image](https://user-images.githubusercontent.com/111281530/184622947-b1c738e6-ddfc-407a-a8fb-3b18bad55f64.png)

![image](https://user-images.githubusercontent.com/111281530/184623127-8b8afcb6-9b5f-40c3-aba4-b99a9c59aef6.png)


#### Head

The head includes several different meshes:

**Head Shape**  
This is the base mesh of the head on which all other head features attach to.

**Eyebrow**  
The Eyebrow mesh functions as a transparency mask. It is used to create different eyebrow styles.

**Eye Mesh**  
The Eye mesh functions as a transparency mask, and is used to create different eye styles.

**Mouth**  
The mouth mesh functions as a transparency mask, and is used to create different mouth styles.

![image](https://user-images.githubusercontent.com/111281530/184624453-7975b66f-e47c-4971-844b-089232830edf.png)

#### Upper Body

The upper body, or torso, of an avatar includes the arms and hands. All upper body wearables are applied to the entire torso.

![image](https://user-images.githubusercontent.com/111281530/184624498-a5ec9d29-0671-46ee-a42f-da303214cfb9.png)

#### Lower Body

The lower body includes the pelvis, legs, and ankles of an avatar.

![image](https://user-images.githubusercontent.com/111281530/184624521-364c3d56-acdb-499b-89f4-d1ea26b23b82.png)

#### Feet

Just the feet! All boots, shoes, sandals, socks, etc. are applied to the feet, not the lower body.

![image](https://user-images.githubusercontent.com/111281530/184624565-a0ed6eb3-273a-4dc4-9aca-017e32eb6fab.png)

### Wearable Categories

Each wearable has a specific category that determines which body part in the avatar system (e.g. head, upper body, etc.) the wearable will be applied to. Certain wearables will impact whether or not other wearables are rendered, depending on the specific category. Some wearables will entirely replace others with sometimes unexpected and surprising results. See the list below for details.

The different categories are:

- **Body_shape:** Replaces the entire avatar’s body.
- **Skin:** Replaces the entire avatar (head, upper body, lower body and feet except accesories)
- **Hat:** Replaces the avatar’s hair. For hats that leave some hair exposed, it must be attached to the hair in the mesh to prevent the avatar from going bald whenever they put on their hat.
- **Helmet:** Overrides the avatar’s entire head, replacing both hair and facial_hair.
- **Hair:** Replaces an avatar’s hat.
- **Facial_hair:** facial hair won’t replace or override any other wearables.
- **Head:**
  - Mouth
  - Eyes
  - Eyebrows
- **Upper_body**
- **Lower_body**
- **Feet**

There are also accessories that can be applied to different areas of an avatar. Some of these accessories can impact other wearables. The accessories are:

- **Mask:** Replaces helmet, tiara, eye_wear and it will override facial_hair.
- **Eye_wear:** Replaces helmet and mask.
- **Earring:** Replaces helmet.
- **Tiara:** Replaces mask and helmet.
- **Top_head:** This is rendered on the top of an avatar’s hard. For example, an angel’s halo.

### Building 3D models for wearables

Let’s start to create some wearables!

To ensure that Decentrand runs smoothly for all users, it is important to create wearable models without using too many triangles. The goal is to keep models as simple as possible so that they can easily be rendered, without sacrificing too much detail.

The same goes for textures. It’s critical that we use as few textures as possible.

There are limits for the number of triangles and textures that can be used for each wearable or accessory:

- No more than 1.5K triangles per wearable
- No more than 500 triangles per accessories
- No more than 2 textures (at a resolution of 512x512px or lower) per wearable. All textures must be square. In the case of shirts, hoodies or basic clothes, an extra texture of skin is acceptable.
- In the case of skin wearable, the amount of tris allowed are 5k and 5 textures.

Before you get started, download the example files for reference meshes and textures.

#### Upper body, Lower body, and Feet

After downloading the example files, load the models into your 3D editor, like Blender.

You’ll notice that each model contains 7 different meshes related to an armature. These meshes represent the head, eyebrows, eyes, mouth, upper body, lower body and feet. You can use these example models as a reference and starting point for your own custom wearable.

**Important: Do not modify the “cuts” or the “stitches” between categories (unless you want to create an unusual “floating head” effect or something similar).**

You’ll also notice that each category has caps, making them “water tight”. These caps exist to prevent unsightly glitches if there are any animation clipping problems due to bad skin weighting. It’s best to leave these caps on.

![image](https://user-images.githubusercontent.com/111281530/184626031-a66fe554-8626-4f79-9306-5abd0780fda7.png)

There are two basic materials for avatar models. One is the material used for the wearable itself and the other one is used for the skin.

![image](https://user-images.githubusercontent.com/111281530/184625986-e1316dba-623b-40bc-91be-734423d44869.png)

Each base mesh comes with its own skin texture.

![image](https://user-images.githubusercontent.com/111281530/184626083-5e927bea-d833-4e84-92bc-1d82c2ab89dc.png)
_Skin for Avatar Shape A_

![image](https://user-images.githubusercontent.com/111281530/184626149-fe3dc2dc-6c5b-42c2-9ecd-6e1f2cd1b460.png)
_Skin for Avatar Shape B_

You’ll notice that each skin texture is rendered grayscale in your editor. This allows us to tint the skin later in the avatar editor according to the user’s preference.

![image](https://user-images.githubusercontent.com/111281530/184626212-ed13a608-eb75-4076-aa8d-bc64351ebe53.png)

**Important: always preserve the UV mapping for any body part left exposed by a wearable, like the bottom of the legs left exposed by shorts and skirts. We want to leave any skin material meshes unmodified so that the user's skin tone is rendered correctly.**

![image](https://user-images.githubusercontent.com/111281530/184626266-6249dfd5-c7d7-481b-ace9-054f6dfb1b6d.png)

We want to leave the skin mesh alone and use the default AvatarWearable_MAT texture provided in the example files whenever possible to select colors for our wearables. This will guarantee that your wearables are performant. However, you can create custom textures for our wearables! It’s always best to use a single, very small, texture file for each wearable.

![image](https://user-images.githubusercontent.com/111281530/184626320-665d752b-8254-46ea-a4d2-35c62de35d29.png)

#### Eyebrows, Eyes and Mouth

These meshes work with a transparent shader so you don’t have to do anything aside from creating your own png texture for the new eyebrow, eye, or mouth style you want and placing it correctly into the UV map. These textures should be 256x256px and need to have, of course, an alpha channel (for transparency). These pngs can be dragged and dropped into builder directly without the need of a 3D file making it easy to upload.

Here are some example png textures:

![image](https://user-images.githubusercontent.com/111281530/184626592-979c84a7-d982-4a53-be51-2e6fb8da4647.png)
_Eyes_

![image](https://user-images.githubusercontent.com/111281530/184626621-78eb9a1a-b7e8-4f14-9389-7ff1a838f712.png)
_Eyebrows_

![image](https://user-images.githubusercontent.com/111281530/184626654-bc683c74-be04-41cb-aa15-dd6028e7c766.png)
_Eyebrows_

![image](https://user-images.githubusercontent.com/111281530/184626681-a739cde7-8295-40f4-b083-14234b6ec8d3.png)
_Mouth_

![image](https://user-images.githubusercontent.com/111281530/184626743-6b32ff1e-e529-4480-97b3-d6cb6e447b2c.png)
_Mouth_

**Nodes:**  
To visualize the final result you’ll need to use these nodes (in Blender):

![image](https://user-images.githubusercontent.com/111281530/184626784-5d6d6d3b-6a50-471f-8c67-7e09cb3e132a.png)

![image](https://user-images.githubusercontent.com/111281530/184626828-4179f9c4-741c-446b-9e41-fbb31c27a2e5.png)

**Masks:**  
You will notice that the Avatar Editor has different color options users can choose from when selecting different wearables.

![image](https://user-images.githubusercontent.com/111281530/184626890-98fbef28-91de-45f2-82d7-065e2410165f.png)

These color choices are applied to a specific mask in the wearable.

![image](https://user-images.githubusercontent.com/111281530/184626968-12a3c095-c0b1-494e-ab05-58ea8a4a4b59.png)
_Eyes Mask_

![image](https://user-images.githubusercontent.com/111281530/184627002-4749f936-8389-4fa1-8f5d-26a3566fb367.png)
_Eyes Base_

The black area in the image on the left (Eyes Mask) indicates the area of the texture on the right (Eyes Base) that will be colored. It’s important to remember that irises always have a grey band scale (if the iris is pure black, the tint isn't going to work).

### Hair and Facial Hair

There are two important things to remember when creating custom hair wearables.

First, try to follow the shape of the head. You can always refer to the head mesh provided in the example files if you need a place to start.

![image](https://user-images.githubusercontent.com/111281530/184627084-01b7c084-8e49-46fb-b397-f271391f7190.png)

Second, if you want users to be able to change the color of your custom hair or facial hair using the avatars editor, then you must paint the hair in grayscale. Lower shades of gray will appear darker and higher shades of gray will appear brighter, but always in the color selected by the user in the avatar editor.

### Skins

Skins are an opportunity to create and show off your skills!
Ensure your design is close to the representation form of Base Shape A and B to ensure smooth gameplay within any situation (avoid representation shapes like vehicles, bugs, floating cubes or pet shapes)

### Skin Weighting

Skin weighting is the process of determining which bones in the avatar’s rigging affect which wearables during an animation.

When skin weighting our new wearables, there are several considerations we need to keep in mind.
Try to weight evenly to the base armature as well as possible, avoid clipping of the mesh and environment. Curators can advise how this can be fixed if there are weighting issues.

Each asset must be weighted to the full skeleton. For example, an upper body asset will look like this when applying skin weights:

![image](https://user-images.githubusercontent.com/111281530/184627139-5c09e10b-0fa2-4a0a-bd16-9f975b8d84d1.png)

Wearables that meet at intersections between body parts must be fully weighted to the same bone. For example, in these two green zones, the vertices in the neck need to be fully weighted to the “Neck” bone only.

![image](https://user-images.githubusercontent.com/111281530/184627174-50fb3630-7933-4225-94a7-85ad3b9a0803.png)


The “key” bones to use when skin weighting are:

**Head Bone:** for the hair, earrings, tiaras, eyes, eyebrows, mouth and any accessory that needs to follow the head’s movement.

**Neck Bone:** for the main head and upper body’s intersecting vertices.

**Hips Bone:** for the upper body and lower body’s intersecting vertices.

**Right Leg and Left Leg Bones:** for the lower body and feet intersecting vertices.

If you keep these guidelines in mind when skinning your avatar meshes, everything will work as with the native avatars.

Remember, you can use any bone to influence any mesh’s vertices! For example, you could create a new foot mesh for a tall pair of boots, and skin weight the top of the boot to the “Leg Bones”. Or, you could create some long hair and use the “Shoulder” or “Spine” bones to influence the hair when the avatar moves around.

### File Handling
If uploading a custom thumbnail ensure it is a png 1024x1024 pixles, transparent background and clean design. Avoid opacity backgrounds and large design elements. If the thumbnail is too noisy it maybe be asked to change to meet guidelines.

Files being uploaded into builder must be under 1.8mb in size.

Once published Collection name and wearable rarity are minted to the blockchain so ensure these details are correct with no spelling mistake or IP infringement prior to publishing.

### Resources

In this shared folder you can find base models, textures, and various other resources, including examples of fully-created wearables. Feel free to leverage these resources when creating your own.

[Wearables Reference Models](https://drive.google.com/drive/u/1/folders/12hOVgZsLriBuutoqGkIYEByJF8bA-rAU)

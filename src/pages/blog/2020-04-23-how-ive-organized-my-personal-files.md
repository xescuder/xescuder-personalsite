---
templateKey: blog-post
title: Organize your photo files
date: 2020-04-24T14:04:10.000Z
description: Do you need to organize your photo files
featuredpost: true
featuredimage: /img/adult-apple-devices-blur-camera-442573.jpg
tags:
  - lifehacker
---
![](/img/adult-apple-devices-blur-camera-442573.jpg)

A lot of times I've wanted to sort all my photo files (thousands!). Finally I decided to do it this month. But I didn't expect that the most difficult is to know how:

* What file naming convention should I use?
* How to organize them in folders?
* Do I need to do all changes by hand? There's a lot of files named DSCN2394.jpg,   img348358.jpg (it depends on camera, mobile, ...)

## Chronological or Thematical?

The first that it comes to my mind was to organize folders by year and then by theme or event inside. I started with this strategy but I realize different things:

\- I don't always remember on which year I was in some place

\- There are some events that repeat every year, like home photos, vacancies (I've spent my last 20 years going at the same place, ...). For these photos if I am interested I want to see them all in one, not by year (I don't want to navigate by year and by place then).  

Finally I decided to use a mix of thematical and chronological:

```bash
├── Birthdays
│   ├── 1980s
│   ├── 1990s
│   ├── 2000s
│   │   ├── 2008-06-01 Noa's Birthday
│   │   ├── 2008-10-04 Xavier's Birthday
│   ├── 2010s
│   ├── 2020s
├── Everyday
│   ├── Home
├── Sports
│   ├── 2010s
│   ├── 2020s
├── Holidays
│   ├── Sant Salvador
```

All media content (I use Onedrive) is organized in:

```bash
├── Media
│   ├── Photos
│   ├── Videos
│   ├── Audio
```

## File naming

Now the big question. How do I name the files? I've seen some people that does not use a full name for these files, and use only sequential numbers, pretending they are always to be at the parent folder.

What happens if I use search? The files have no information about the event, place or year, so they are not easily searched. 

I prefer to use the next naming convention

`<Folder name>-<nnnn>`

## How I've massively organized my photos

Starting for a big number (thousand) of photos, what can I do? I've used two tools that saved my life!

### Remove duplicated and similar photos

Sure you've a lot of repeated photos that you don't know... (backups,...). I've used the tool **Duplicate finder**. It helps to find and remove:

* Repeated photos (it detects the exact content, despite of different naming or location)
* Similar photos. How many photos do you've that are practically exactly the same, but only changing a little the position of an arm, head, one hair? ;)

### Rename your files

I recommend **Renamer**. It does worth to pay 25$. 

I do these steps:

1. Drag the folder with the files you want to rename and select to change folder contents
2. Use and apply 'Enumeration' with:

   * Numeración: 001,002,003...
   * Formato: Texto - Número
3. Use and apply (after previous one) 'Apply folder name':

   * Carpeta: Padre
   * Separador: - (I remove all trailing spaces)

* **Amazon Photos** (my backup). If you've Amazon Premium you can upload unlimited photos. You'll see it's great, as it has some Artificial Intelligence and detected faces, hats, water, so you can filter and see all photos by specific person, for many persons, ...
---
title: "Project Title"
date: YYYY-MM-DD
categories: [category1, category2]  # Options: motorsport, aviation, uas, agriculture, electronics, 3d-printing
tags: [Tag1, Tag2, Tag3, Tag4]  # Add relevant tags
status: "Planning"  # Options: Planning, In Progress, Complete, Testing
image: "assets/images/PROJECT_FOLDER/placeholder.jpg"
excerpt: "Brief description for the project preview card (keep it concise)."
---

## Overview

**Hook statement or key takeaway.**

Brief description of the project, the problem being solved, and the context.

---

## Technical Approach

Description of the technical solution, materials used, and rationale.

---

## Execution

Detailed explanation of the design process, challenges faced, and how they were overcome.

---

## Images & Media

### Single Image

<img src="{{ '/assets/project_photos/FOLDER/image.jpg' | relative_url }}" alt="Alt text">

### Single Image with Caption

<figure>
  <img src="{{ '/assets/project_photos/FOLDER/image.jpg' | relative_url }}" alt="Description">
  <figcaption>Image caption description</figcaption>
</figure>

### Side-by-Side Images (2 columns)

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem;">
  <figure>
    <img src="{{ '/assets/project_photos/FOLDER/image1.jpg' | relative_url }}" alt="Description 1">
    <figcaption>Caption 1</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/FOLDER/image2.jpg' | relative_url }}" alt="Description 2">
    <figcaption>Caption 2</figcaption>
  </figure>
</div>

### Image Grid (3 columns)

<div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem;">
  <figure>
    <img src="{{ '/assets/project_photos/FOLDER/image1.png' | relative_url }}" alt="Description 1">
    <figcaption>Caption 1</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/FOLDER/image2.png' | relative_url }}" alt="Description 2">
    <figcaption>Caption 2</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/FOLDER/image3.png' | relative_url }}" alt="Description 3">
    <figcaption>Caption 3</figcaption>
  </figure>
</div>

### Image Grid (4 columns)

<div style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 1rem;">
  <img src="{{ '/assets/project_photos/FOLDER/image1.jpg' | relative_url }}" alt="Description 1">
  <img src="{{ '/assets/project_photos/FOLDER/image2.jpg' | relative_url }}" alt="Description 2">
  <img src="{{ '/assets/project_photos/FOLDER/image3.jpg' | relative_url }}" alt="Description 3">
  <img src="{{ '/assets/project_photos/FOLDER/image4.jpg' | relative_url }}" alt="Description 4">
</div>

### Video Embed (YouTube)

<iframe width="560" height="315" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe>

### Video File (Local)

<video width="640" height="360" controls>
  <source src="{{ '/assets/project_photos/FOLDER/video.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

### GIF Animation

![Alt text]({{ '/assets/project_photos/FOLDER/animation.gif' | relative_url }})

### Before/After Comparison Slider

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;">
  <div>
    <p><strong>Before</strong></p>
    <img src="{{ '/assets/project_photos/FOLDER/before.jpg' | relative_url }}" alt="Before">
  </div>
  <div>
    <p><strong>After</strong></p>
    <img src="{{ '/assets/project_photos/FOLDER/after.jpg' | relative_url }}" alt="After">
  </div>
</div>

---

## Specifications

| Parameter | Value |
|-----------|-------|
| Material | Material Name |
| Dimensions | L x W x H (mm) |
| Weight | X grams |
| Operating Temperature | -X°C to +X°C |
| Lead Time | X days |

---

## Project Files

- [Download CAD Files](#) (Coming soon)
- [Download Technical Report](#) (Coming soon)

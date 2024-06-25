---
title: Home
layout: home
---

# Documentation
**Workflows used in the production of Volumetric Interview #4 Now You See Me Moria**

### Software used
- Brekel
- Unity
    - Toy Gaussian package
    - Cinemachine package
- Touchdesigner
- Premiere Pro

```mermaid
%%{init: {'theme':'base'}}%%
flowchart TD 
    A[Instagram video] -->|download .mp4| B(Luma AI)
    D -->|export video| G
    D -->|export camera| G
    H --->|export depth + color maps| G(Touchdesigner)
    B --> C[Gaussian Splat]
    C -->|export .PLY splat| D(Unity 3d)

    I[Kinect recording]--->|record volumetric data| H(Brekel)

    G--->|export combined video|K
    
    J[interview recording]------->K(Adobe Premiere Pro)
    L[various image + video sources]------->K 
		
		O[audio by Skander]------->K    
    
    
subgraph Final
        N([documentation])
        M([final film])
        P([release event?])
    end
    
    K --> Final
```
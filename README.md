# OVD
Occluded Vehicle Detection Dataset
## Introduction
This is a dataset that focuses on occluded vehicle detection.

Based on the [UA-DETRAC](https://detrac-db.rit.albany.edu/) dataset, we obtained the dataset UADETRA-OVD consisting of 8677 images that are abundant in instances of mutual vehicle occlusion and vehicles being occluded by other objects, through IOU threshold filtering and manual labeling.

## Comparison
UA-DETRAC stands out as a challenging large-scale dataset for real-world vehicle detection and tracking, which was mainly captured on road overpasses in Beijing and Tianjin and manually annotated with 8250 vehicles and 1.21 million object boxes. However, directly applying UA-DETRAC to our occluded vehicle detection task suffers from the following drawbacks: 
-  The UA-DETRAC dataset is a video sequence frame dataset with short inter-frame intervals, resulting in image redundancy;
-  The dataset contains instances of duplicate annotations; 
-  A majority of the images lack scenarios with vehicle occlusion;
-  The annotations contain numerous invalid vehicles that are completely occluded;
-  Vehicles occluded by other objects or situated at the image periphery (which can also be considered as occluded) are frequently unlabeled.
  
To address these issues, we employ methods such as IOU filtering and manual annotation, resulting in a refined occluded vehicle detection (OVD) dataset. Specifically, we retain only the images from every fifth frame, discarding those without occlusion objects or where objects are completely obscured. Furthermore, we have meticulously annotated all instances of occluded vehicles within the UA-DETRAC dataset.
![image](https://github.com/LittleGrey-hjp/OVD/blob/main/example%20of%20dataset.png)
 Examples of different scenarios in the OVD dataset(right) compred with the initial dataset(left).  The red box indicates the original annotation box, the green box represents the newly annotated box, and the orange dashed box denotes the discarded box.

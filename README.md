# Basic-Camera-Specification-Study

## Contents

Basic concept of camera
Baseline for camera specification
Illumination types
Light
Camera

## Basic concept of camera

### Pixel
Digital image’s smallest unit.

### Pixel size
Each pixel’s physical size(μm unit).  
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/f171c89c-c8c2-47ea-8cbe-64ae0bdc6533" />  

Fig. Pixel and sensor size

### Resolution
Pixel’s total counts that organize images. 
Sometimes express like Mega Pixel unit(ex. 5MP).
Megal Pixel is total pixel numbers.  
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/3431936d-3aa2-464b-9d93-3119bb0afca3" />  
   
Fig. Resolutions

### Sensor size

sensor size(H) = resolution(H) * pixel size(H)
sensor size(W) = resolution(W) * pixel size(W)

### Frame rate
Number of frames that camera can get each second.
  
<img width="340" height="211" alt="image" src="https://github.com/user-attachments/assets/b571f081-b823-4196-bd25-1684998dd6d5" />
  
Fig. Example of frame rate

### Shutter speed
Amount of time that the sensor receives light.
The longer exposure time, image will be more brighter by accepting more light, but motion blur can occur on moving objects.
On the contrary, short exposure time can darken image, but you can get clear image by reducing motion blur.

### FOV
Field Of View. Size of area that camera can check at once.

### Working distance
Physical distance from the front of camera lens to the object to be inspected.

### DOF
Depth Of Field. Range of clear view of camera back and forth th the focal point.
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/27684c0e-4d8a-496c-937f-01ff04b19a42" />
  
Fig. Example of DOF
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/55f36985-ad29-48b0-b8da-ac4c50065de7" />
  
Fig. Example of camera setting

## Baseline for camera specification

### Camera type

- Area scan camera

Feature
Camera for capturing 2D images at once.

Pros
Able to apply a wide range of applications.

Cons
Inappropriate for pretty long object or continuous surface inspection. That kind of objects can’t capture at once.

- Line scan camera

Feature
Using 1D linear sensor. Take a picture in line units to obtain 2D image.

Pros
A detailed inspection of long objects with high resolution.

Cons
Should synchronize with camera’s capture time and object’s movement time.
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/d474413d-7d0d-43c8-8e38-80c23cf2992a" />  
  
Fig. Area scan and line scan camera

- 3D camera

Feature
Camera for capturing 3D datas including depth information.
There are some type of principle to get 3D information.

Pros
Able to analyze objects with complex shapes or structures with 3D scanning.

Cons
Projected pattern could be disturbed by bright light environment.
Distortion can occured in surface that has high reflection.
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/ab1dea7c-4453-4bfa-b024-559f526ff49a" />  
  
Fig. 3D camera image

### Color type

- Monochrome

Feature
Use a sensor that detects only the brightness intensity.

Pros
High sensitivity and performance in low illumination.
Fast data processing due to single channel.
Wide spectrum range (including IR and UV).

Cons
No color information -> Limited application area.

- Color

Feature
Bayer filter that each pixel can get only one color.
Post-processing that we call demosaicing.

Pros
Able to get color information.
Intuitive visualization by using color channel.

Cons
Low sensitivity and performance in low illumination.
More datas to process than monochrome camera.

### Sensor type

- CMOS
Mainstream sensor technology currently used in most machine vision cameras.
Offer more faster, flexible than CCD.

- CCD
Generally used in the past, but nowadays underused by CMOS.
Excellent light sensitivity and image quality, but limited in high speed application.

### Shutter technology

- Global shutter
This is how all pixels on the sensor are exposed at the same time.
It is useful for high speed movement object inspection because there is no distortion.

- Rolling shutter
How each line of the sensor is exposed sequentially.
Distortion can occur When photographing moving objects.
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/3cf4227d-8187-41b6-b30c-92adee1d817f" />
  
Fig. global and rolling shutter

- Frame rate
High frame rates are essential when inspecting high-speed moving objects or processing many images in real time.

- Resolution
The minimum identifiable feature (detail) size of the subject determines the required resolution.

- Pixel size
Generally, larger pixel sizes can accept more light, which is advantageous in low light environments, with less noise and wider dynamic range.
However, larger pixel sizes at the same sensor size result in lower resolution.

### Lens

- Focal length
The longer focal length, the larger narrow area is.
The shorter focal length, the wider area you can see.
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/668b45d7-e103-4a5f-b437-99aec8453ca6" />
  
Fig. Example of focal length
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/5fa78b59-defc-4475-bf53-152859dbde07" />
  
Fig. Example of focal length



- Working distance

- Aperture
The part that controls the amount of light passing through the lens.
The smaller the F-stop value, the larger the aperture, the more light comes in, and the depth of field becomes shallower.
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/ab623cfc-fe81-43d5-934b-5d621253ca21" />
  
Fig. Example of adjusting aperture
  
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/b07b5a2d-941b-40cc-9676-dede2bde6477" />
  
Fig. DOF change along to aperture

- Lens mount
S-mount, CS-mount, C-mount, etc.
Ensure that the camera and lens are compatible.

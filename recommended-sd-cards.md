#Recommended microSD Storage for Kernel Cameras

##*Results below are not final. We just identified a driver issue with the memory card capture speed and should have it fixed soon, resulting in 2x rates.*

Kernel cameras were designed to allow for max continuous RAW image capture. To allow for these capture speeds it is important to use a memory card capable of keeping up with the required write speeds. While any microSD card up to 128GB can be used, we recommended the ones tested below for optimal results:

| Card Capacity | Card Brand | Card Model Number                      | Kernel Sensor | Kernel Image Mode | Photos Per Second | Image Size | Card Capacity | Card Capture Length |
|---------------|------------|----------------------------------------|---------------|-------------------|-------------------|------------|---------------|---------------------|
| 64GB          | Lexar      | 1000x                                  | 1.2MP         | MAPIR (RAW)       | **?fps**       | 1.75MB     | ~34,057 photos| 2 hours 42 minutes  |
| 64GB          | Lexar      | 1000x                                  | 1.2MP         | TIFF              | **?fps**       | 2.34MB     | ~25,470 photos| 2 hours 54 minutes  |
| 128GB         | SanDisk    | Extreme Plus 95MB/s SDSQXVF-128G-GN6MA | 1.2MP         | MAPIR (RAW)       | **?fps**       | 1.75MB     | ~68,000 photos| 3 hours 19 minutes  |
| 128GB         | SanDisk    | Extreme Plus 95MB/s SDSQXVF-128G-GN6MA | 1.2MP         | TIFF              | **?fps**       | 2.34MB     | ~50,854 photos| 4 hours 7 minutes   |
| 128GB         | SanDisk    | Extreme 90MB/s SDSQXVF-128G-GN6MA      | 1.2MP         | MAPIR (RAW)       | **7.58fps**       | 1.75MB     | ~68,000 photos| 3 hours 10 minutes  |
| 128GB         | SanDisk    | Extreme 90MB/s SDSQXVF-128G-GN6MA      | 1.2MP         | TIFF              | **?fps**       | 2.34MB     | ~50,854 photos| 3 hours 49 minutes  |
| 64GB          | SanDisk    | Extreme 90MB/s SDSQXVF-064G-GN6MA      | 1.2MP         | .mapir (RAW)      | **?fops**              | 1.75MB     | ~34,057 photos|                     |
| 64GB          | SanDisk    | Extreme 90MB/s SDSQXVF-064G-GN6MA      | 1.2MP         | TIFF              | **?fps**              | 2.34MB     | ~25,470 photos|                     |
| 64GB          | SanDisk    | Extreme Plus 95MB/s SDSSQXSG-064G-GN6MA| 1.2MP         | .mapir (RAW)      | **7.09fps**       | 1.75MB     | ~34,057 photos|                     |
| 64GB          | SanDisk    | Extreme Plus 95MB/s SDSSQXSG-064G-GN6MA| 1.2MP         | TIFF              | **?fps**              | 2.34MB     | ~25,470 photos|                     |
| 64GB          | SanDisk    | Extreme Plus 95MB/s SDSSQXWG-064G-ANCMA| 1.2MP         | .mapir (RAW)      | **7.63fps**       | 1.75MB     | ~34,057 photos|                     |
| 64GB          | SanDisk    | Extreme Plus 95MB/s SDSSQXWG-064G-ANCMA| 1.2MP         | TIFF              | **5.92fps**       | 2.34MB     | ~25,470 photos|                     |
| 128GB         | Lexar      | 1800x                                  | 1.2MP         | .mapir (RAW)      | **7.46fps**              | 1.75MB     | ~34,057 photos|                     |
| 128GB         | Lexar      | 1800x                                  | 1.2MP         | TIFF              | **4.98fps**              | 2.34MB     | ~25,470 photos|                     |



###How We Test Capture Speeds

We put the camera in the configuration and image mode listed above with a formatted SD card. We then capture 1000 photos and divide by the time it takes to capture them to determine the photos per second (fps).